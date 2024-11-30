---
title: Trooper's Projects
featured_image: /images/home-collage.png
---
{{ range where .Site.Pages "Section" "main" }} {{ .Render "summary" }} {{ end }}
This website hosts many of the projects I have made and some that are in progress. Whether it's a drone or small Arduino project, it's here.