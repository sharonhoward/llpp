The London Lives Petitions Project
=====================

Contents
---------

-   Description
-   Background
-   The petitions
-   Methods and caveats
    -   Essential background reading:
    -   The source data
    -   Data collection
    -   Issues and limitations
    -   Keyword tagging
    -   Considerations for further analysis
-   Data summary
    -   Text files
    -   Metadata tables
-   Acknowledgments
-   License
-   Citation
-   Future plans

Description
----------------

Textual data and documentation relating to approximately 10,000 eighteenth-century petitions addressed to London magistrates, originally digitised as part of [London Lives](http://www.londonlives.org).


Background
------------

[London Lives 1690-1800: Crime, Poverty and Social Policy in the
Metropolis](http://www.londonlives.org) is an online resource
providing 'a wide range of primary sources about eighteenth-century
London, with a particular focus on plebeian Londoners'. It contains more
than 240,000 manuscript and printed pages from eight London archives,
including records from four of London's main courts: the Sessions of the
Peace for Middlesex, Westminster and City of London, and the Old Bailey.

In the eighteenth century, magistrates were responsible for a wide range of
administrative duties in addition to criminal justice, including the
administration of poor relief and the settlement laws, economic regulation (including for example, wages, alehouses and fairs), the maintenance of highways, and much local government besides. [Sessions
Papers](http://www.londonlives.org/static/PS.jsp) are products of this work, bundles of assorted documents which clerks of
the peace would file together after each court session.

There are nearly 100,000 pages of material in 1300 session files in London Lives' four series of session papers. Not only are they the largest single body of manuscript material in London Lives, they are also by far the most diverse. They include
many types of document, but probably the most important and numerous
are: witness examinations and depositions; lists of those appearing
before the court; court orders; and petitions.


The petitions
--------------

Petitions are ubiquitous in early modern legal archives across England
and Wales and they are rich and important sources that many social
historians have used extensively. As physical objects, they range from high-quality professional products to scrawled scraps of paper, reflecting the diversity of petitioners. The language of petitions is
deferential, and often highly formulaic; it can also be florid,
melodramatic, poignant, distressing, and manipulative. Petitions are not by any means straightforward, authentic
'[voices of the
people](https://manyheadedmonster.wordpress.com/2015/07/29/petitions-of-the-people/)', but they can provide insights into plebeian experience, as well as being rich source material for local government and poor relief administration. 

The petition was a standard method of
communication with early modern representatives of authority. Petitions were instigated by institutions and by individuals, by elites
and by paupers, and all sorts of people in between. They were
used by convicted criminals to beg for the royal pardon; by officials and contractors to
claim expenses for government work; by private individuals to complain about
abusive behaviour by neighbours, employers, apprentices, husbands or
local officials; by parishes to appeal official decisions about paupers and
vagrants; to claim exemptions from local office or taxes; and more.  Individuals also wrote less formal letters to officials similarly requesting some kind of relief, aid or mitigation, and this project attempts to gather those documents as well as 'proper' petitions, for a fuller picture of the culture and practices of petitioning. (Additionally, there are related documents for many petitions, particularly court orders, which I have not attempted to document at this stage.)

The London Lives Sessions Papers contain at least 10,000 petitions and petitioning letters addressed to London magistrates (and a few to the judges of the Old Bailey). The sheer scale and heterogeneity of the Sessions
Papers, especially the Middlesex Sessions, and the organisation (or lack of it) of the
material in London Lives means that they have not been easily accessible
as a body of texts for in-depth and systematic investigation of their
language and their creators. I have begun the London Lives Petitions Project as an attempt to remedy this.




Methods and caveats
-------------------

### Essential background reading: 

- [London Lives technical methods](http://www.londonlives.org/static/Project.jsp#toc7)
- [Sessions Papers](http://www.londonlives.org/static/PS.jsp)


### The source data

1300 XML files, part of the data for the searchable online resource at www.londonlives.org (v1.1, released April 2012). These files represent four record series held at the London Metropolitan Archives: the Sessions Papers for the City of London (SL), Middlesex (SM), Westminster (WJ) and the Old Bailey (OB) (the latter contains only a tiny handful of petitions).

The material in London Lives was transcribed using a method known as [double rekeying](http://www.londonlives.org/static/Project.jsp#toc9), in which two (non-academic) typists transcribe text, the two versions are compared and only where they differ does any further manual checking take place. It is not as accurate as traditional academic standards of transcription and proofreading, but unfortunately that is not a practical option for transcription of such large amounts of text. The accuracy rate for London Lives is approximately 98-99% (at character level), but it can vary considerably between documents.

The rekeyed texts were then marked up for searching, using a combination of automated and manual tagging, for various types of information: the names of people and places, occupations and dates. There is also structural markup for features such as text in margins, deleted, obscured or illegible text, text continuing across page breaks, and so on. 

The markup did not, however, include information about document structures and types, beyond general document categorisations such as 'Sessions Papers' or 'Accounts Books' which were based essentially on the original document series' archival organisation. There is no real structuring information between this type of generic classification and the single page. This is quite problematic in the Sessions Papers because they are both much more varied and much larger than the other documents in the resource (many of which are bound volumes rather than loose papers). Thus, simply finding the petitions was the project's first challenge.

### Data collection

There are far too many pages of material in the Sessions Papers for me 
to identify petitions manually, and so I employed a number of
semi-automated search strategies. The likely result of this is that I
have not found every petition in the original data, and there may be a
few documents that are not petitions at all. Moreover, there is a degree of bias built in to the method, in favour of certain kinds of documents, which users of the data should be aware of.

The main strategy for identifying likely petitions was based on
searching for certain keywords and phrases. In particular:

1.  The preamble: "To The Right Honourable/Worshipful/similar title..."
2.  Less formal letters often begin with phrases like 'May it please you/your honour'
3.  At the beginning of the document or immediately following the preamble: "The humble petition/prayer of..."
4.  In the body of the document: "your (humble) petitioner(s)" (also "humbly sheweth")
5.  The sign off: "And your petitioner(s) (as in duty bound) shall ever pray etc"

The list above presents the phrases in standard modern English. But in
reality the forms of the words in the data files can vary considerably, making them much harder to find:

1.  spelling variations and the use of abbreviations in the original
    documents
2.  damage to the original documents which has obscured parts of the
    text
3.  rekeying errors 

This necessitated the use of some complex [regular expressions](http://www.regular-expressions.info/) searches. For
example, a search query for 'The humble petition of' would in fact look like `(th|y)e.? humb(le|ell?) peti(t|c)i?on of`


### Issues and limitations

I initially underestimated how many pages that were not in fact
petitions might also contain some of the same phrases (particularly, for
example, in orders relating to petitions). I had to cull around 300
items from my original results list and there may still be a few stray
non-petitions (although it's highly likely that they will be closely
related material). But the few remaining false positives are less problematic than the documents that these searches might have *missed*.

The method is biased, obviously, towards documents that contain those
phrases. It is most effective for finding
professionally-produced petitions that adhere closely to the formal conventions
of petitioning language and use consistent spelling. Non-professional petitions from individuals of lower social status are more likely to 

- depart to some extent from those forms
- use unpredictable and inconsistent spelling
- have less well-formed handwriting (which in turn made them harder to rekey accurately) 

I think I have now found the vast
majority of petitions. However, I am much less certain about the search for petitioning letters. In both cases, though, future additions are likely.


### Keyword tagging

The keyword tagging should be regarded with considerable caution, merely as rough indicators of likely content and/or petitioner types. In most cases a tag simply means the petition refers to that subject but . Eg, the tag 'apprentice' may mean the petition was on behalf of an apprentice or simply that it mentions one. 

Moreover, some of the tagging is probably unhelpful or simply wrong, and much of it is inconsistent (it should not be assumed that the existence of a tag means I have indentified all petitions that could have that tag). Additionally, I have focused on keywords that are of interest to me; so, for example, crime-related keywords are over-represented. 

I would emphasise that the tagging is **not** reliable enough to use in any statistical analysis. 

I felt that *some* kind of tagging would be better than nothing, but future updates can be expected to improve significantly on this aspect of the data.


### Considerations for further analysis

All of the issues described need to be taken into account for anyone trying to use the data. I have created a 'corpus' of plain text files but I do not yet know exactly what it will be possible to do with them, given the two compounding factors of transcription errors and spelling variations in the original documents. Corpus linguistic approaches to early modern *printed* texts - which are considerably more standardised than these non-elite manuscript sources - have to work hard to deal with [their orthographic variations](http://www.linguisticdna.org/2015/07/10/eebo-tcp-and-standard-spelling/). The petitions texts might be more comparable to OCRed printed texts (such as ECCO) than to the rekeyed EEBO-TCP corpus.


To give one brief example: the top 10 variants from a search of the Middlesex Sessions petitions texts for the word "relief", using the regex `rel[ie]+f`:

| word | count | 
|-------|--------|
| relief | 1100 | 
| releife | 536 | 
| releif | 171 | 
| reliefe | 101 | 
| relife | 20 | 
| releiffe | 8 | 
| releifed | 4 | 
| reliefs | 4 | 
| releiff | 3 | 
| releift | 2 |

Rekeying errors are frequently hard to distinguish from spelling variations without closer examination of the text. For example, the word 'agoe' ('ago') has been rekeyed on a number of occasions as 'aged'. In the 'relief' example above, 'relieft' *could* be an unusual spelling of 'relieved' - or simply a random rekeying error.

However, at the very least the fact that the petitions exist as a corpus makes it possible to explore just how 'bad' the data is, whether it is possible to distinguishing spelling variation from transcription error, and potentially improve the text in the future.


Data summary
--------

Please read the *methods and caveats* section carefully before using the data! 


### Texts

**10130 plain text files**: one .txt file for each petition, in subfolders organised by court. (13.5mb)

File naming: the name of each file corresponds to the image reference on London Lives and to the ll_img field in each of the metadata tables.

The text files are intended primarily to enable textmining (bearing in mind all the problems already discussed) or import into a database for advanced searching. 

Nearly all of the London Lives
XML markup has been removed for this version of the files, but certain markup elements are still indicated:

-   paragraph breaks have been retained
-   markup for obscured or illegible text has been replaced with [...]
-   deleted text (between \<deleted\> tags) has been replaced with [---]
-   the \<mark\> tag, denoting that someone signed a document with a mark, has been replaced with [x] 

### Metadata

The data tables are supplied in .csv format.

#### LL_petitions_v1_data

Contains summary information for each petition, including tags and data to enable linking to the petitions on London Lives. A minority of petitions covered multiple pages and this is also indicated.

| field | description |
|------|--------------|
| pid | table ID |
| ll_img | London Lives (first) image reference |
| ll_url | London Lives URL for the (first) page |
| mpage | 0 = a single page petition; 1 = multiple pages |
| mpimgs | list of all image references for multiple page petitions |
| tags | list of tags for the petition |
| court | two letter court code |
| year | year of session |


#### LL_petitions_v1_tags

This file provides the tags data separately for use in a database. 

| field | description |
|------|------------------|
| tid | table ID |
| ll_img | (first) image reference |
| tag | tag name |

Most of the tag names should be self-explanatory, so I am not documenting them all here. But note the following:

* **churchwardens_petition** - petitions *by* churchwardens and overseers of the poor on behalf of their parishes, usually concerning disputed settlement cases. 
* **churchwardens_overseers** - unsorted mentions of churchwardens/overseers of the poor; some will probably end up in the churchwardens_petition category
* **is_poor** - petitions from people who cite their poverty as a reason for their petition. 
* **poor** - unsorted references to the poor/poverty (again, some of these should probably be in is_poor)
* **disability** - another work in progress, and does not distinguish physical incapacity caused by old age from other impairments. It includes both physical and mental disabilities.
* **office** -  usually petitions by office holders (concerning expenses, attempts to avoid obligations or to explain negligence, etc); covers a wide range of offices (eg gaolers, constables, scavengers, and also jurymen)




Acknowledgments
---------------------

The dataset has been created using the transcriptions of the Sessions Papers published at London Lives. I am deeply grateful to Tim Hitchcock and Bob Shoemaker, the London Lives project directors, for agreeing to share the data.

The original documents are held at the London Metropolitan Archives.

The London Lives project (under the name Plebeian Lives) was funded by the Economic and Social Research Council.

License
---------

The dataset and all accompanying documentation are licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

This means that you are free to copy and redistribute the material in any medium or format; and to remix, transform, and build upon the material for any purpose, even commercially, providing you follow the terms of the licence:

-    You must give appropriate credit, provide a link to the license, and indicate if changes were made.
-    If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.


Citation
--------

Suggested citation:

Sharon Howard, The London Lives Petitions Project, version 1.0 (2015), based on data from *www.londonlives.org*.


Future plans
-------------

* Identify and add missing petitions and letters.
* Better subject tagging.
* TEI-XML files, incorporating some subset of the London Lives structural and semantic markup.
* A web search at earlymodernweb.org, linking directly to the documents on the London Lives website.


