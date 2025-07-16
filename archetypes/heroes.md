---
date: '{{ .Date }}'
lastmod: '{{ .Date }}'
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
description: >
  {{ replace .File.ContentBaseName "-" " " | title }}
categories:
  - "Heróis brasileiros"
{{/* playing with templates */}}
{{- $heroes := slice nil "mg-cultural.jpg" "analytics-hero.jpg" "coding-hero.svg" "winner-hero.jpg" nil nil }}
{{- with index $heroes (int (math.Floor (math.Rand | mul 5)))}}
hero: "/images/heroes/{{ . }}"
{{- end}}
---

## {{ replace .File.ContentBaseName "-" " " | title }}
{{/* playing with templates */}}
{{- $images := slice "antonieta-barros.png" "memorial-jk.jpg" "brazil-national-day-banner-design-vector-eps-flag.jpg" "santos-dumont.jpg" "chico-mendes.png" "tiradentes.jpg" "getulio-vargas.jpg" "zumbi-dandara-palmares.jpg" }}
{{- with index $images (int (math.Floor (math.Rand | mul 7)))}}
<img src="/images/{{ . }}" height="250" style="float: right; border:5; border-radius: 15%; padding: 10px;" />
{{- end }}
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras egestas lectus sed leo ultricies ultricies. 

Praesent tellus risus, eleifend vel efficitur ac, venenatis sit amet sem. Ut ut egestas erat. Fusce ut leo turpis. 
Morbi consectetur sed lacus vitae vehicula. Cras gravida turpis id eleifend volutpat.
Suspendisse nec ipsum eu erat finibus dictum. Morbi volutpat nulla purus, vel maximus ex molestie id.
Nullam posuere est urna, at fringilla eros venenatis quis.

Fusce vulputate dolor augue, ut porta sapien fringilla nec. Vivamus commodo erat felis, a sodales lectus finibus nec. In a pulvinar orci. Maecenas suscipit eget lorem non pretium. Nulla aliquam a augue nec blandit. Curabitur ac urna iaculis, ornare ligula nec, placerat nulla. Maecenas aliquam nisi vitae tempus vulputate.
