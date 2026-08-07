At the center of most humanistic endeavors lies text. It can be a single text, or it can be many texts. And the texts themselves can be any length, from the few words of a particular utterance from a particular individual in a particular moment to the thousands of words that make us all of Shakespeare's work or the millions of words that make up the novels published in England in the nineteenth century. 

But what is the nature of such texts? Folklorists, for example, have long made the nature of spoken texts as represented in written form one of the central considerations of our disciplinary practice. We have, for example, worried over the proper way to represent to readers differences in pronunciation or rhythm within a text or the way a story was actually told, while at the same time also trying how best to think about the ontology of texts within a given speech community: where does one text end and another begin within the flow of spoken discourse during such tellings? Folklorists are not alone in their considerations about the nature of a given text or set of texts. Scholars of written communication face similar questions in trying to come to grips with how to think about the relationship between the physical pagination of a text versus the flow of words. 

Such questions about what makes a book, for example, have become especially interesting as information technologies have made new forms of textuality possible as well as offering alternative vehicles for traditional forms of textuality (e.g., ebooks). Information technologies have also opened up entirely new means not only for the exchange of analyses, but also for texts themselves, and that returns us to the question of textuality with which we began: how do we best share texts with each other?

While there have been a number of experiments over the past three two decades, two principle formats have emerged as dominant for humanities scholars seriously interested in taking full advantage of the internet, and, perhaps, ignoring, for the moment the de facto standards of Microsoft Word file formats and Adobe PDF.[^1] most importantly, they are not in conflict. The first is plain text, and it is exactly what it says: a sequential file of characters encoded in one of a few widely-known standards, typically ASCII or one of the Unicodes, that is readable as textual material pretty much as is. That is, you do not need any particular application to open a plain text file. Plain text documents are distinguished from formatted text documents, which often contain not only information on how to format text—italics or bold, for example—but also sometimes how to structure the text in a fashion that goes beyond simple formatting. One can do both in Microsoft Word, for example: simply format text in situ, using the many styling options available, and/or tie that formatting to particular parts of a document or its structure. That is, a line in word can be bolded, because the author wishes it be bolded, or it can be bolded and noted, within the file format, that it is a certain level heading. The problem with Microsoft Word is that it is a proprietary format, subject to change without notice, and often easily broken. (Fortunate indeed is she who hasn't had a Word document go suddenly wonky.)

*See "What Files Actually Look Like" below.*

There is, of course, a middle ground, one that most of us use on an almost daily basis, even if we know relatively little about it, and that is HTML.[^2] As it name makes clear, HTML offers authors the ability to markup their texts using a specific set of tags, that are indicated by being enclosed within angle brackets. While the text, as the illustration makes clear, may look complex, it remains encoded in plain text and thus readable by machines, and thus humans, in a wide variety of contexts. What HTML does is provide a standard way of describing how documents should be presented. Encoding bits of text, or links or images, is relatively straightforward, and because it is all based in plain text, the chances of things getting garbled, as files bounce around the internet from transmission point through a series of computers and cables until reaching the browser in our own devices, is relatively small. (And usually the garbled bits are fairly local: it is rarely the case that an entire document will be scrambled because a bit got dropped here or there. That is the fundamental strength of HTML and, thus, of the web.) 

What you may not know about HTML is that it is actually a specific variant of a more generalized form of encoding known as Standard Generalized Markup Language, or SGML, and was developed by Tim Berners-Lee in order to facilitate communications among physicists.[^3] The original set of HTML tags was very small and focused mostly on presentational matters: this *word* should be italicized and this one should be in **bold** was indicated in the original HTML markup by the words being enclosed by `<i>word</i>` and `<b>one</b>`. There were a limited set of tags that indicated the structure of a document, like whether a line of text was a heading or a paragraph.

As the number of computers serving HTML documents increased and the number of people exchanging such documents increased, the web was born, and while HTML has increased in its presentational richness, its semantic dimensions have remained, for the most part, rather limited. Perhaps the best example of semantic poverty can be found in the use of italics, which are a typographical convention used to indicate the titles of books and works of art, to indicate a particular emphasis by the author, the introduction of a new term, or the use of a word or phrase from another language. That is, HTML, in replicating the printed page, also preserved its semantic impoverishment, which seems rather a waste of time given how much more computers should be able to do for us. 

Fortunately, for humanists especially, at the same time Tim Berners-Lee and Robert Cailliau were developing HTML, humanities scholars and archivists were working in parallel to develop a robust system for capturing not only texts themselves in an electronic form but also for capturing the wide array of information to which users of such information regularly like to have access. Such information varies by domain and by practitioner, and TEI, as the markup system for the Text Encoding Initiative has come to be called, has the ability to adapt to those differences. TEI refers both to the consortium behind the project, the project itself, and, in general, to the flexible set of schema that the project produces. 

The goal of TEI is to "develop and maintain a standard for the representation of texts in digital form."[^4] The standard itself is spelled out in the guidelines, which attempt to "define and document a markup language for representing the structural, renditional, and conceptual features of texts." The most recent version of the guidelines is P5, with the P standing, as I understand it, for proposal, since each version of the guidelines undergoes extensive discussion and revision before being approved for publication.

### What Files Actually Look Like

Below is a representative sample of the same document in plain text, HTML, PDF, RTF, and Word's DOCX format. All were based on the following text and then accessed using the unix `head` command. Here's the original text:

> He was in the excavating business,  
> so he called me to come up and showed me the job.  
> And we dug house basements.  
> And that was when they were remodeling a lot filling stations,  
> making them super service and that sort of thing,  
> so I said, yeah, I’ll take it.  
> So I worked there about two years and a half.  
> And then we came back to Bloomington.  
> At that time, my brother-in-law--  
> he’s passed away--  
> but at that time he owned a furniture store, United furniture.  ￼

The text is 11 lines long, and `head` shows the user the first ten lines of a file by default. Compare the size of the documents in the table below and then compare where the "data" -- the actual text above -- occurs in each of the files below. (Or, where it doesn't.) It makes you wonder about what kind of vessel into which you are pouring your hard work, no? (My friend Henry Glassie is nodding his head vigorously at this moment, and for all the right reasons.)

Here's a simple list of the files and their sizes:

    goble-text.txt    468 bytes
	goble-html.html   592 bytes
	goble-tei.tei     660 bytes
	goble-pdf.pdf      16 KB ... or 16,000 bytes for 34X the original text
	goble-rtf.rtf      18 KB ... or 18,000 bytes for 38X the original text
	goble-docx.docx    45 KB ... or 45,000 bytes for 96X the original text

In short, Word creates a document exponentially larger -- almost one hundred times! -- than the information that it contains. Moreover, none of that metadata, the stuff going with your data, your text, add anything of semantic value: anything added here is simply additional text added by the analyst herself.

Now to what these things look like from the computer's point of view. As Mike Rowe would say, get ready to get dirty. It's not pretty:

    % head goble-text.txt 
	    
	    He was in the excavating business, 
	    so he called me to come up and showed me the job. 
	    And we dug house basements. 
	    And that was when they were remodeling a lot filling stations, 
	    making them super service and that sort of thing, 
	    so I said, yeah, I’ll take it. 
	    So I worked there about two years and a half. 
	    And then we came back to Bloomington. 
	    At that time, my brother-in-law--
	    he’s passed away--
	    
		
	% head goble-html.html 
	    
		<html>
	    <head>
	    </head>
	    <body>
	    <p>He was in the excavating business, <br />
	    so he called me to come up and showed me the job. <br />
	    And we dug house basements. <br />
	    And that was when they were remodeling a lot filling stations, <br />
	    making them super service and that sort of thing, <br />
	    so I said, yeah, I’ll take it. <br />
	    
		
    % head goble-tei.tei 
	
	    <TEI xmlns="http://www.tei-c.org/ns/1.0">
	    <!DOCTYPE TEI.2 system 'tei2.dtd' [<!ENTITY % TEI.spoken 'INCLUDE' >]>
	    	
	    <teiHeader>
	    	<!-- TEI Header Info -->
	    </teiHeader>	 
	    <text>
	    
	    He was in the excavating business, 
	    so he called me to come up and showed me the job. 
	    
	    
    % head goble-pdf.pdf 
	
	    %PDF-1.3
	    %?????????
	    4 0 obj
	    << /Length 5 0 R /Filter /FlateDecode >>
	    stream
	    x?V?r?0??+?Q??S۩krlf(?f80H?$???:???oA??V?	
	    m??`E??}??j?{\??????i???Q???.?|?Z?6o?`???:{/????6?Т??ֹH2̷?(хk?3dHS?[??ej??%?@??'?
	    ?:R????-B???n?N?~???
	    p?k??(??\??DYzz?i?IP??"? ??+?xWv???q?+-q
	           l?E?"-1??)??T?Z@??[Y??k?????w?lf?%QG?`2H}?
	    [pR~"¢Yaml?|?0#'!D?P???????ֽ?p??g?5Qq#P?E????????7???c???͂??<??+??f?o?&?T?w\????}M%??[??Y?[sV(MvLx{C?VA???ӛ;??)[
	                                  ?
	                                   ???d}????J?,,?R?zZ?t??I?pf?|?
	                                                                l
	    endstream
	    endobj
	    5 0 obj
	    
		
    % head goble-rtf.rtf 
    
	    {\rtf1 \mac \ansicpg10000 \nisusversion40007 \deff0 {\fonttbl {\f0 \froman 
	    \fcharset77 Times-Roman{\*\falt Times};}{\f1 \fnil \fcharset77 
	    Tahoma-Bold{\*\falt Tahoma};}{\f2 \fswiss \fcharset77 Tahoma;}}{\colortbl 
	    ;\red0 \green0 \blue0 ;}{\*\nisustoctable {\nisustoc \tcf68 {\nisustocname 
	    Default TOC}{\*\nisustoctabrep  }{\*\nisustocretrep  }{\nisustoclevelstyle TOC 
	    1}{\nisustoclevelstyle TOC 2}{\nisustoclevelstyle TOC 3}{\nisustoclevelstyle 
	    TOC 4}{\nisustoclevelstyle TOC 5}{\nisustoclevelstyle TOC 
	    6}{\nisustoclevelstyle TOC 7}{\nisustoclevelstyle TOC 8}{\nisustoclevelstyle 
	    TOC 9}}\nisusactivetoc68
	    
	    
    % head goble-docx.docx 
	
	    ?"M??5h>?$??S?)/))?6:?????|7`??MO?@??&??f??]?`??pP<*???v
	    ?ݏ?,_??i?I?(zi?N??}fڝ?`??h?5)??7?6Sf????c|?"
	    ?l???????:0Tɭ?"Э?p'䧘??tn??&?   QS?X????!.???,?_?WF?L8W()???
	    ??}'????F?????G????? ?Y,Ķ??c??? ?sB`
	                                  ????Ih??/YfS
	                                          ?3?Yٜ9??wr??F??JB?/ݜ??;?"?+Z(?e?ȁaU?=?????7??<I?H?<4?e??:bG۞!АN	????mCǍs+??_??bǼ$??&??????_?ao??.8??t????Ûq????Uc??H<2??l???o??P!??B??word/document.xml?YKs?6?w??ó%Q??H???Ќ'J??ED?b?S?F?^I?DK??Q?:??b_?v?x??dΌ堆Q???                ?
	    d?Z\9?ђ????I?????')W-?m?@3??`$u?????Nr?*ɔ#?B٤??0*??I?g??Ij??g,????AQ???j0yo???
	    

[^1]: The Portable Document Format remained proprietary until 2008, when it was officially made open source, so historically it was not a good choice for information archives. It remains, for many, a problematic file format, plagued as it is with a variety of weaknesses.

[^2]: The same could be said of the Microsoft Word document: I don't know a single person, besides myself who has ever actually peered into a Word file to see what their data looks like.)

[^3]: There is a lot more to this elliptical history that is well worth a quick read, if only in an encyclopedia entry somewhere. The roots of SGML, for example, stretch back to the 1960s and the work of IBM scientists to develop a way to enable the sharing of documents attached to large-scale projects. Be design, the documents had to be both widely distributable as well as be able to persevere for several decades.

[^4]: As an initiative dedicated to facilitating the creation of /open access content, the TEI consortium makes a great deal of information available via its website: http://www.tei-c.org/.