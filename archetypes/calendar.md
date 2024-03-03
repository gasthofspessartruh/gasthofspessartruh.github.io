---
date: {{ .Date }}
title: "{{ replace .Name "-" " " | title }}"
summary: ""
start: "{{ (now.AddDate 0 0 (add 1 (sub 0 now.Day) | int)).Format "2006-01-02" }}"
end: "{{ (now.AddDate 0 1 (sub 0 now.Day | int)).Format "2006-01-02" }}"
---

