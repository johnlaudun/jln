---
layout: post
title: "Speaking Subjects, Subjects Spoken: Using TED Talks to Understand Discursive Gender Formations"
date: 2023-12-11
tags: research
---

*K.M. Kinnaird, Allison Chaney, and I have submitted our latest work with/on TED talks to the [Journal of Cultural Analytics](https://culturalanalytics.org/). For those interested and wanting to know more about what we have been up to for all these many months, here’s the introduction:* 

Mappings of texts to assigned or assumed genders qua gendered have been a part of studies of linguistic expressivity since Robin Lakoff speculated about the differences between men and women’s ways of speaking (Lakoff 1975). Like others, we find such explorations of differences in expression between men and women compelling, whether it is focused on modal meaning — expressions of a speaker’s certainty, or uncertainty found in tentative language like hedges, tag questions, intensifiers — or in affective meaning — expressions of a speaker’s attitude toward his/her audience which can be mapped to group composition, the relationship among participants, and their status.1 Few studies have been as clear-cut in their findings as Robin Lakoff’s initial speculations suggested, but the larger field of inquiry she engaged has enriched a variety of philological domains both in terms of gender but also in terms of power dynamics across and within groups. This inquiry has run either parallel to or resulted in far more nuanced appreciations of the ways that texts occur, the situations in which they occur, and how the texts themselves are either shaped by an event or shape the event in some fashion. As Patricia Sawin notes in her consideration of gender and power in situations where texts feature: “esthetic performance cannot be bracketed from social action,” and not only that but we must realize that “emergent performance can transform cultural models or social structures, [and] that esthetic performance is a central arena in which gender identities and differential social power based on gender are engaged” (Sawin 2002:48). That is, gender is in many instances as much a product of discourse as it is the producer of discourse.

Fascinated by the intertwined nature of gender and discourse, we wanted to explore what contri- bution the TED talks data set (Kinnaird and Laudun 2019), previously released through this journal, could provide to understandings of language use and gender. There is always, of course, the matter of what one is called, or how one is imagined by others, and then what one calls oneself, if anything at all, and/or how that self projects itself into the world in and through language. Here, we attempt to apply two lenses to explore the role of gender within discourse as manifested in TED talks. First, we investigate the representation of speakers by gender. Second, we explore how others (by gender) are being spoken of. Put another way, we first concern ourselves with *who* is speaking and second *how* they are speaking of others and of themselves. These twinned investigations represent two (of many) di- mensions of cultural analytics: established topics of concern to the humanities and the human sciences and possible applications of machine learning to those topics, inviting either novel answers to familiar questions or new kinds of questions. Here we use techniques from supervised machine learning and statistical inference to explore the gender of the speakers. Having done that, we explore the gendering of agency in hopes of establishing a continuum across which speakers project themselves.

In the essay that follows, we begin by surveying recent work in cultural analytics that has explored the gendering of *character spaces* (Underwood, Bamman, and Lee 2018 and Jockers and Kiriloff 2016). Grounding our own consideration in semiotics and seizing upon the opportunity of working with spoken material, we examine how character spaces intersect with *speaking subjects* and *subjects spoken*. With our theoretical program laid out, we proceed with the difficult, and tendentious, matter of gendering the speakers of our texts, making it possible to divide the TED talks corpus into two subcorpora, one by women speakers and one by men speakers. In the third section of the essay we explore what actions are available to gendered subjects as well as how, using those subjects, we can gender verbs in such a way as to explore the continuum of gender as presented in the *I*s of speakers.

For this present purpose, only texts from TED main events—i.e. not TEDx or other special events—are examined. First, we extend the speaker dataset within the TED talk data to include the gender of each speaker (as can be detected from public materials). We then use these identified genders to “gender” each TED talk. We then use these gendered texts to explore agency in the TED talks and how they differ based on both the speaker’s presented gender and the gender of represented subjects within the texts. In doing so, we seek to demonstrate the value in considering gender in an exploration of a text corpora as well as to connect computational text analysis to the broader conversation about TED talks. While the TED talk corpus is small, and, as we will explore more later, unbalanced, it does offer us an opportunity to examine a well-established, and popular, discourse stream that could offer us insights into gendered subject positions in English.

By mapping out the actions available to gendered agents, principally *he* and *she*, we hope to establish a continuum within which speakers may or may not engender themselves (as the *I* in their speech). We are not particularly happy with the fact that the work only reflects binary gender, but the fact remains that for much of the discourse of the last few decades in which TED talks have occurred, which are themselves affected by the decades (and centuries) which preceded them, the English language has largely offered two genders. Individuals operating within such a discursive regime are largely left to their own linguistic devices to represent themselves as well as to represent others. If we can establish some baselines, we might also be able to discover interesting experiments and innovations occurring in texts in a myriad of places.

Finally, we concede that our analysis is limited in a few ways; most notably that this work *only* focuses on *gender* (as currently presented) and not other axes of diversity, including race, income status, sexual orientation, and religious background/identity. Gender was easier to study, in that we could detect a speaker’s outward presentation of gender using computational techniques on the written documentation that was available on the TED website, relying on gendered pronouns about speakers in the documentation as a signal for gender. Examining other axes of diversity would require additional data (either self-reported surveys or additional press materials with explicit references to diversity markers) on each speaker or slightly different data scraping techniques with more explicit ‘rules’ for detecting diversity (such as euphemisms or cultural synonyms). This is not to say that other axes of diversity should not be studied, but rather to explain why our analysis is not immediately transferable to other markers of diversity. Instead we see our work as a first step, one that can provide a framework for extending these kinds of questions to more areas of diversity.