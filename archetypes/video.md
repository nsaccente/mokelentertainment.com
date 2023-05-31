---
title: "Post Title"
author: "Michael Strick"
date: {{ .Date }}
image: "img/content/video/default.jpg"
draft: false
weight: 100
tags: [
    "video",
]
keywords: [

]
lang: en
---

{{< youtube "{{ replace .TranslationBaseName "-" " " | title }}" >}}
