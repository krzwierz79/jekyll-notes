---
layout: post
title: Python List Comprehension
categories: [Python]
tags: [python]
---

### all elements

new_list = [element.method() for element in old_list]

### if

new_list = [element.method() for element in old_list if element = "chosen"]

### if/else

new_list = [element.method() if element != "exception" else element.exception_method() for element in old_list]
