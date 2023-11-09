---
title: "Post Title"
author: "Michael Strick"
date: {{ .Date }}
image: "https://img.youtube.com/vi/{{ replace .TranslationBaseName "-" " " | title }}/0.jpg"
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
