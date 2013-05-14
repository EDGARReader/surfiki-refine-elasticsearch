Surfiki Refine for Elasticsearch (Non Distributed Version)


Python Map-Reduce Transformation Tier for Elasticsearch Indices


##What is Refine?


Originally designed to work with Elasticsearch indices and API. Refine allows you to take an input stream, transform and or manipulate it for your needs, then output it in a variety of formats.


With the variety of uses of Elasticsearch being seen in the its ecosystem (Search, Data Stores, API), a powerful and extensible processing tier was needed to meet Intridea’s needs. Our belief, is this can fit in to your Elasticsearch environment as well. And in turn, provide you with additional transformation and or manipulation capabilities.


At its heart, Refine is a collection of scripts, written by you in Python.


##How does it work?


Technically, Refine is Map-Reduce, which for each job you define incorporates:


A stream script defines the source of your data. A query’s results (In the case of Elasticsearch) A file or files, or a Web API such as Twitter.


 - A mapper script takes the input, divides it into smaller sub-problems, and distributes them to workers. 


 - A worker may do this again in turn, leading to a multi-level tree structure. The worker processes the smaller problem, and passes the answer back to its master.


 - A reducer script collects the answers to all the sub-problems and combines them in some way to form the output – the answer to the problem it was originally trying to solve.


 - You can add as many scripts that your job may require, however the core is the stream, mapper and reducer scripts.


##What are some examples?


- Combining data from multiple indices in to a new index. With Refine you can either do this ad hoc or on a scheduled basis.


- Splitting data from a single index in to new indices based upon some criteria. Refine makes this relatively simple to perform.


- Statistical facets can be taxing on the heap. You can use Refine to process/transform/count this data and expose within a new index on a set schedule.


- Transforming data already indexed with additional data. For example, some data has location information (lat, long) however you also want to store meta data associated with those locations Such as State, City and County information. While it makes sense to do some of this in line, with Refine you can do it after the initial data is already indexed.


- Accessing third party API's to append data to existing indexed data. With Refine, accessing those API’s, injecting and or manipulating is a core feature.


- Given a body of text, you can use Refine to split your stream into its separate words, perform a word count for the given word, then reduce it to a de-duped sorted array.


- Given a collection of results, you can use Refine to further score each result against a series of 

validation criteria such as geographic region or category.


- Need text to appear in various ways, before it can be processed further? Use Refine to prepend suffixes or concatenate strings, and dynamically add these as new attributes.


###Open Source Projects utilized:


- redis

- Paramedic

- Sense

- r3

- Python Dev Bootstrap

- Lookout

- Flask

- Twitter Bootstrap

- Cloud9

- Python

- PyFlakes

- ujson


---


##Installation Instructions


##Usage Instructions


--
Anthony Nyström
Fellow, Managing Director of Engineering
Intridea, Inc. | www.intridea.com
anthony@intridea.com
(o) 888.968.4332 x502
(c) 650.417.3203