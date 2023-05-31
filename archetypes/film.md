---
title: "Post Title"
author: "Michael Strick"
date: {{ .Date }}
image: "img/content/film/default.jpg"
draft: false
weight: 100
tags: [
    "film",
]
keywords: [
]
lang: en
---

{{< youtube "{{ replace .TranslationBaseName "-" " " | title }}" >}}
