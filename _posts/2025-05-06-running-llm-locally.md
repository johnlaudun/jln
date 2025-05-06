---
layout: post
title: Running an LLM Locally
date: 2025-05-06
tags: computing, ai
---

I spent a portion of today following Cody Wabiszewski’s guide on how to [download and run the Dolphin Llama 3 model](https://www.gsnetwork.com/author/cbw50077/). His directions are quite good, but they miss a few things, especially when it comes to setting things up on a Mac. So for those Mac users who want expand the scope of running an LLM locally beyond Apple Intelligence, I suggest the following:

Head over to the [Ollama website](https://ollama.com/) to download one of the available models. Wabiszewski recommends **`dolphin-llama3`** and that’s what I went with.

When I downloaded the Dolphin Llama 3 model, it was not located where any of the posts I read suggested. Instead, I needed to use `locate` to find the directory. (If you have not run `locate` before, you will need to let it build its database, but that does not take long -- less than 10 minutes on my M1 MacBook Air with 1TB storage.)

