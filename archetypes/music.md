---
title: "Post Title"
date: {{ .Date }}
image: "img/content/music/default.jpg"
draft: false
weight: 100
author: "Michael Strick"
---

{{< youtube "{{ replace .TranslationBaseName "-" " " | title }}" >}}
