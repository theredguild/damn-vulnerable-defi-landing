---
{{ $amount := len (os.ReadDir "content/challenges") }}
{{ $title := replace .Name "-" " " | title }}
id: {{ $amount }}
title: "{{ $title }}"
contractsDir: "{{ .Name }}"
challengeFile: "{{ replace $title " " "" }}.t.sol"
draft: true
aliases:
    - /challenges/{{ $amount }}.html
---

{{< readprompt challenge="{{.Name}}" >}}
