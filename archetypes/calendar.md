---
date: {{ .Date }} # Hiernach werden die Einträge sortiert nach YYYY-MM-DD
title: "{{ replace .Name "-" " " | title }}" # Das ist die zweite Zeile (der Titel)
summary: "" # Das ist die erste Zeile (der Zeitraum)
start: "{{ (now.AddDate 0 0 (add 1 (sub 0 now.Day) | int)).Format "2006-01-02" }}" # Das Startdatum im Format YYYY-MM-DD
end: "{{ (now.AddDate 0 1 (sub 0 now.Day | int)).Format "2006-01-02" }}" # Das Enddatum im Format YYYY-MM-DD
---

