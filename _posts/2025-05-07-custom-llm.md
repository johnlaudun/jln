---
layout: post
title: Customizing an LLM
date: 2025-05-07
tags: ai
---

There are a few of ways to customize an LLM to allow you to bring your own library of sources to bear on a problem. This could be anything from that collection of manuals for all your home appliances to scholarship on conspiracy theories. What matters is that you have the documents available in machine-readable form. For most people, this will be PDFs with text layers embedded either because they were produced that way or they were later OCRed. (Note to fellow scholars: early OCR was pretty ragged. I often re-OCR documents from JSTOR that are from its early days.)

From hardest to easiest, your customization options are: retraining an LLM, retrieval augments generation (RAG), and adding context documents. For most, the first option is not really one for a number of reasons. First, a lot of the LLMs, like ChatGPT, are proprietary. Second, retraining requires hardware that is expensive, and, third, it also requires the ability to work in Python. (Python is a very friendly language, but no matter how friendly it is, creating or customizing something as complex as a transformer is bit mind-boggling.) 

A simple example might help: last year as part of an introduction to text analytics class, I thought I would see how do-able it would be for students to train a GPT on a small data set. I downloaded a collection of around a thousand jokes from Reddit and started the training process. Following the recommendation that I should have at least 30 *epoch*s, I hit return and initiated the process: each epoch used all 8 of my M1 Macbook’s CPUs and took an hour. By the end of the second hour, the thing was getting so hot that I called it quits. So, yeah, you at least need dedicated hardware.

With retraining an LLM off the table, the easiest option is to provide **context** for your session. You can do this by uploading documents to a particular session or, with some LLMs like ChatGPT, you can create a custom GPT which references a collection of documents which you upload. (These can even be shared either to the public or via a link.) The advantage of providing context documents is that it is straightforward and relatively easy. But the information exists in the model’s information space, and so it works best with relatively small collections: the model goes through the entire context each time it answers a question. 

The somewhat more involved move is to set up **retrieval augmented generation**. RAG allows an LLM to be more selective. It is better for larger, and more dynamic, data sets. 