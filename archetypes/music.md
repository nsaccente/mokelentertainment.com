---
title: "Post Title"
author: "Michael Strick"
date: {{ .Date }}
image: "img/content/music/default.jpg"
draft: false
weight: 100
tags: [
    "music",
]
keywords: [

]
lang: en
---

{{< youtube "{{ replace .TranslationBaseName "-" " " | title }}" >}}
