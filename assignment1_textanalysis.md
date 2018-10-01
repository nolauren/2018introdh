# Assignment 1 - Topic Modeling 

By analyzing academic journals, we can see what scholars have been interested in studying over time. A prime example is the work of Goldstone and Underwood on the PMLA, which we are reading for class. The goal of this assignment to apply a particular text analysis method - topic modeling - to provide a "distant reading"/ "macroanalysis" of a scholarly journal.  The assingment has two components: (1) topic mhttps://amandac93.github.io/dh-topic-models/odeling interactive visualizaiton and (2) a reflection piece on the method and what you can learn about the journal using text analysis.  The final assignment should be a markdown file in your repository: https://github.com/introdh/intro-dh2018-YOURUSERNAME 

Each person must do a different academic journal. Please email me once you have selected a journal. I will upate the list here: 

| Name | Journal | Site | 
|-------|--------| ---------| 
| Dr. Tilton | American Quaterly | https://nolauren.github.io/dh-topic-models/ |
| Amanda Corbosiero | Discourse Studies | https://amandac93.github.io/dh-topic-models/ |
| Kobi White | Journal of African American Studies| https://kaydub14.github.io/dh-topic-models/ | 
| Emily Song |  The Journal of Criminal Law and Criminology| https://emilysong15.github.io/dh-topic-models/  |
| Kristi Mukk | The American Archivist | https://kristi-m.github.io/dh-topic-models/| 
| Kylie Britt | The Slavivonic & Eastern European Review | https://kyliebritt.github.io/dh-topic-models/ |
| Matt Fichera |  Journal of Financial Education |  |
| Alexis Williams | Gender and Development | |
| Luke Malcynsky | The Annals of the American Academy of Political and Social Science |  |
| Sal Girma | Afro-Hispanic Review | salgirma.github.io/dh-topic-models |
| Raven Baugh | The American Poetry Review|  |
| Kayla Corbin | American Music Journal | https://kc5gs.github.io/dh-topic-models/ |
| Jordan Cannady | The American Sociologist |  |




A note about collaboration:   You may work with each to help get the code working and to build your interactive visualization. You MAY NOT work with each other on the reflection. This should be your interpretation of the course readings and discussions as applied to your particular scholarly journal. 

## Corpus / Data

### Jstor
[JStor Data for Research (DFR)](http://about.jstor.org/service/data-for-research) provides machine-readable data from JStor, 
a digital library of academic journals, books, and primary sources.


### Downloading Data

It takes several days for Jstor to send the data. Make sure to make this request immediately. 
The main page for Jstor DFR is [here](http://dfr.jstor.org).  Set up an account [here](https://www.jstor.org/register?redirectUri=/dfr/results) and select your data [here](https://www.jstor.org/dfr/results).  To select a particular journal, [here are the instructions](https://www.jstor.org/dfr/about/creating-datasets?loggedin=true&facet_journal=am91cm5hbA%3D%3D&ed=&searchType=facetSearch&Query=american+quarterly&page=1&sd=). 
One you have selected a journal, make sure there are at least 500 records to use; otherwise, 
we can't use topic modeling as there aren't enough records. There are two more categories to consider:
 
- Year of Publication: You might consider just looking at a journal during a specific period. For example, did *American Quarterly* (the journal of  the field of American Studies) look at specific topics during the 1960s in the middle of the U.S. social movements?


Select All of the Data Types including XML and three types of N-Grams. 

Make sure to download the data. It should include four folders:

![](https://github.com/nolauren/2018introdh/blob/master/img/Screen%20Shot%202018-09-25%20at%208.38.29%20AM.png)

Make sure the folders have the proper materials. For example:

![](https://github.com/nolauren/2018introdh/blob/master/img/Screen%20Shot%202018-09-25%20at%208.38.41%20AM.png)

What are you seeing in these folders?

Each file corresponds to an article in your journal.  For each article, you have an XML file, ngram1, ngram2, and ngram3. For example, journal-article-10.2307_23317634.xml, journal-article-10.2307_23317634-ngram1.txt, journal-article-10.2307_23317634-ngram2.txt and journal-article-10.2307_23317634-ngram3.txt are in their respective folders. These are the same article and we know this because of the identifier "10.2307_23317634".  We will only be using the XML files (which describe the articles including Article Title, Author, and Publication) and ngram1 in this assignment. 

## Converting Data

One challenge is that the data Jstor sends us needs to be turned into a "bag of words" in order to do topic modeling. Topic modeling looks at word co-occurance across documents (in our case articles), so the exact order in the document (i.e. article) does not matter.  The way Jstor gives us the data looks like this:

![](https://github.com/nolauren/2018introdh/blob/master/img/Screen%20Shot%202018-09-25%20at%208.39.03%20AM.png)


So, we need to take each word in our list and write it out according to the corresponding number. For example, "humanism 9" needs to become "humanism humanism humanism humanism humanism humanism humanism humanism humanism humanism". To do this, following the instructions in our [JStor R Conversion Lab](https://github.com/nolauren/2018introdh/blob/master/lab04_jstorconversion.R). 

Once you done with the Jstor R Conversation Lab, you should have four new folders (all_txt, all_xml, all_topicmodel, data). Check the files in all_topicmodel to make sure the words are unlisted. For example, "dr 16" should now be  "dr" written out 16 times. 

![](https://github.com/nolauren/2018introdh/blob/master/img/Screen%20Shot%202018-09-25%20at%208.48.27%20AM.png)


Note: A common issue is that R says that you do not have a package. No problem! Just install it by typing:
```{r}
install.packages("nameofpackage")
```


### Upload Data to Box
Because Box does not handle little files very well, you need to ZIP your data. You can do this by right clicking on your folder with your data.  On a mac, select "Compress 'NAMEOFFILE'.  On a PC, select 'ZIP NAMEOFFILE'. Rename it "lastname_data". 

Go to [our box folder](https://richmond.box.com/s/av74idfgrnlwzldd5oop0yi5c0ulalfo) and upload the compressed file.  
This should be on Box by Friday, September 28 at 5. 

----------
## 

The final assignment is comprised of two components:

1. Topic Modeling Visualization
2. Written Response 

Due: Saturday, October 6th

------------------

### Topic Modeling Visualization

Using an adapted version of the [Signs@40 interface](http://signsat40.signsjournal.org/topic-model/), build a site that visualizes your corpus. 
The corpus is an academic journal of your choice. The data should come from JSTOR's Data For Research (info below). 

The information for how to build the interface is available [here](https://github.com/statsmaths/dh-topic-models). Make sure to give descriptive names for the topics. 

Make sure to include a link to your site in your written response. It should be https://github.com/YOURGITHUBUSERNAME/dh-topic-models.


### Written Response

The 500-1500 word response should explain the data set, the initial findings, 
and how one would go about further exploring the data set/ findings/ arguments. 
In other words, the response should show that you understand what topic modeling is, 
how it works, and what we can learn from this method by way of applying it to a journal, which can 
be accomplished by addressing the following questions:

- What is the scope of the journal?
- What question(s) are you trying to answer?
- Which data did you select for the corpus? Make sure to specify the kind of data and periodization. 
- Why the number of topics? 
- What are the initial findings and/or possible arguments? In other words, what do these topics tell us? Certain patterns? Trends?
- Drawing on the readings, what are the possibilities and limitations of text analysis and topic modeling?


More details:

- Citations: Use a modified format since citations will be drawn from course readings. Cite relevant readings using in-text/ parenthetical citations: (author, publication, date). Ex. (Blevins, personal blog, 09-09-2009) or (Goldstone and Underwood, JDH, 2012). 

- Save as "assignment2_YOURLASTNAME.md" in your repository (https://github.com/introdh/intro-dh2018-YOURUSENAME). 

- Grading: [Rubric](https://github.com/nolauren/2018introdh/blob/master/assignment1_rubric.pdf)

------------------------------------------------------------------------------------------------



  






