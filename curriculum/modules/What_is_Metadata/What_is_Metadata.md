# What is Metadata
## Details
* Category: [Foundational](../categories/Foundational.md)
* Module Prerequisites: None
* Audience: [Any](../audiences/Any.md)
* Level: [Beginner](../levels/Beginner.md)

## Content

### What is Metadata?

Metadata is simply *data about data*. Just as data enables humans to organize, track, and take intelligent action on objects in the real world, metadata empowers knowledge workers to organize, track, and act intelligently on data itself.

It is sometimes claimed that the first metadata was a library catalog system—specifically, if one is looking for firsts, the catalog of the ancient Library of Alexandria. Supposedly, metadata kept at Alexandria listed genre, title, author, and length for each book [1]. In fact, books remained one of the most important domains of metadata even at the opening of the 21st century. Amazon’s website, even from its humble beginnings when it was only a digital bookstore, used many of the same pieces of information. It added the sorts of information tracked by the library of Alexandria to more modern administrative metadata such as ISBN. Amazon's early adoption of this metadata has been cited as a contributing factor in its success. And not only did it succeed wildly as one of the world's first digital booksellers, its practices quickly spread to brick-and-mortar stores as well as libraries. Metadata enabled stores to efficiently organize their own inventory, and for consumers to efficiently discover titles they wanted to read. [2]


<img src="alexandria_book.png" width="50%" align="left"/>  

---

_The Amazon store listing for a book about the Library of Alexandria contains a panel with the most important metadata: The book's length, language, publisher, publication data, physical size, and ISBN._ 

---


But we now know that the internet was, by that time, in the process of replacing books as humanity’s largest store of information. Enter the Semantic Web movement in the early 2000's. Espoused by digital luminaries such as Tim Berners-Lee, the Semantic Web was partly a vision for websites--already proliferating to a degree that made web search challenging--to be annotated with metadata not unlike those used by our booksellers. But it was also so much more. It is the Semantic Web which birthed the concept of the URI, or Universal Resource Indicator, a uniquely identifying string for _any_ resource, physical or digital. Imagine an ISBN, but for _anything you can imagine_. Complete adoption of these URIs would enable software to perform nearly any task, and locate any information, that human beings performed or located by surfing the web themselves. [1]

Though many individual ideas from the Semantic Web have been realized, and influenced the internet's development since, the full vision of the Semantic Web is one in which essentially all information online is made machine-readable--in a single universal language--as well as human-readable. It is a sweeping vision, one which, it is largely acknolwedged, remains unrealized. [1]

There are different types of metadata that can be categorized based on the intended usage of metadata or on the method of generation of metadata. When categorized based on usage, metadata broadly falls into three categories[4]:
* Descriptive metadata: metadata that provides information on data to facilitate discovery, source-verification, significance and identification such as tile, author, genre, date published etc.. 
* Structural metadata: metadata that provides information on technical specifications, structure of data such as file format, page number, file sizeetc..
* Administrative metadata: metadata used for organizatonal purposes. This can include unique identifiers, genre, keywords etc...

Metadata is also categorized into three types based on the methods of generation[1]:
* Deliberate metadata: metadata that is created deliberately either manually or computer generated to be used by the resource. These include name (to provide verification), alias (to provide anonymity), ISBN (for resource identification).
* Data Exhaust: metadata that is created as a by-product of conducting operations or day-to-day activities. Data exhaust is metadata that is produced as a by-product of other processes. This type of metadata include items you buy, when items were purchased, what items were searched for  etc...
* Paradata: metadata that is produced as a result of using resources. This type of metadata includes search history, access logs, cookies.

A wide-spread application of metadata is targeted-marketing. Targeted marketing is the strategy of using metadata to make inferences about individuals and personalizing ads for the specific individual. Targeted marketing can be benefical and harmful to both the advertiser and the individual being targeted. A famous example of harmful targeted advertising to the consumer is the case of Target (the store) sending a flyer of coupons for baby-related items to an individual that was most-likely pregnant based on metadata of recent purchases. The harm being that Target had announced the pregnancy of a minor to her parents. 

### What is Metadata as it Relates to Knowledge Graphs?

<img src="alexandria_panel.png" width="40%" align="left"/>  

---

_A Google web search for "Library of Alexandria" brings up this panel of information sourced from Wikipedia's Wikidata. Many of the entries in this metadata, such as the library's country of origin, are in fact links to other entities in Wikidata with identifiers (and more metadata) of their own._ 

---

Knowledge graphs are data structures, containing interlinked descriptions of concepts, entities, relationships, and events, which may be analyzed and queried like databases. (See "What are Knowledge Graphs?" for more.) Diverse pieces of data can be described and related to one another by making connections between their metadata, in what is called the knowledge model [3]. For example, the search result shown to the left provides metadata about the historical entity "The Library of Alexandria", including its country of origin, "The Ptolemaic Kingdom". But what if the searcher does not know what the Ptolomaic Kingdom is? Without connections, this piece of metadata might not be very useful. But because it is embedded in a knowlege graph, the searcher can discover what other pieces of metadata are connected to it, discovering more about what the Ptolomaic Kingdom is (in this case, by following a Wikipedia link). The developer of a knowledge graph collects and contextualizes metadata, which makes it more effective at communicating the meaning of the related data and entitites to users. A knowledge graph can be used to discover new related information, understand how information fits into a larger whole, and even highlight inconsistencies between related data that might otherwise remain disparate. 

<br><br>

<img src="slavery_schema.png" width="50%" align="right"/>  

---

_This diagram shows a portion of "The Enslaved Ontology", the ontology for the knowledge graph hosted at enslaved.org [7]. We can see here that a "ParticipantRoleRecord" is the class of all records of agents (such as people) participating or otherwise being part of a particular event. Their participation in that event can be one of several types, and records of participation in events are one of several kinds of "AgentRecords"--all the possible kinds of historical records of an agent. It may look pedantic, but this machine-readable, unambiguous taxonomization of historical records enables powerful semantic search queries (such as "What are all the events where Frederick Douglass participated as a speaker?") to be answered precisely, including many that may not have been forseen when the database was assembled._ 

---

However, one man's metadata is another man's data. The metadata of, say, a published book is merely the "data" of a knowledge graph. A knowledge graph's "metadata" typically refers to the even-higher-level descriptions of that data in turn, what is often called a knowledge graph's ontology or schema [5].
A schema or ontology is a formal description of knowledge within a certain domain. This schema includes restrictions, rules and axioms governing how pieces of information in the knowledge graph exist in relation to one another. If data on a published book was contained in a knowledge graph, for example, metadata for that graph might include the assertion that Book and Publisher are relevant categories of information, and that every Book must have a Publisher.

A schema is the formal description that is used when conducting inferencing and reasoning by automatic reasoners. These automatic reasoners highlight inconsistencies and showcases the context of the knowledge graph. A schema provides a sharable and resusable representation of a knowledge graph that also provides a format, standards for the addition of new knowledge to the knowledge graph. 

Creating an ontology can be seen as transferring knowledge into a computer-accessible form. It is clear that a thorough requirement analysis is crucial for the development of an ontology that is appropriate for a given purpose [8]. One of the initial questions that should be answered when developing an ontology is whether a semantic representation adds any value to the subject or not. If no value is being added, maybe a different representation is needed instead. One advantage of an ontology-based system is that the knowledge represented in a semantic format can be more easily incorporated knowledge from other sources. Additionally, the semantic format reveals implicit knowledge that may be useful. Another question that should be answered when creating an ontology is whether a representation based on formal logic is rational for the intended purpose of the ontology. 

Once it is decided that semantic, formal logic-based formalism will be used, there are multiple tool options to choose from, including RDF(S) or OWL DL depending on the requirements for the given subject or scenario. After the tool is determined, the knowledge worker can determine which domain(s) need to be modeled and what aspects of the domain must be captured. This includes the level of detail in the ontology and the explicit and implicit tasks being answered by the ontology. Because there are many ways to model a situation in an ontology correctly, it may not be apparent how to do so. If a single word has many different, but related, meanings, the decision about how the word should be modeled in the system will depend on the purpose of the ontology. Ultimately, there is no perfectly correct manner in which to build a system that satisfies the requirements. Although there are certain methods can prove more viable or useful when building a system, design decisions typically need to be made in order represent the purpose of the ontology. 


## Related KGC Media
* Workshop Example
* Tutorial Example

## References
[1] Pomerantz, Jeffrey. *Metadata*. The MIT Press, 2015. https://doi.org/10.7551/mitpress/10237.001.0001

[2] Dawson, Laura. "What We Talk About When We Talk About Metadata". Chapter from *A Futurist's Manifesto*. O'Reilly Media, 2012

[3] "What is a Knowledge Graph". ontotext.com. https://www.ontotext.com/knowledgehub/fundamentals/what-is-a-knowledge-graph/ (accessed Feb. 5, 2023)

[4] "Metadata and Its Importance in a Data Driven World". villanovau.com. https://www.villanovau.com/resources/bi/metadata-importance-in-data-driven-world/ (accessed Feb. 5, 2023)

[5] Shimizu, Cogan. (2023). CS7810, Metadata Representation Languages: Modular Ontology Modeling. [Wright State University campus 2/2/2023].

[6] "What are Ontologies?". ontotext.com. https://www.ontotext.com/knowledgehub/fundamentals/what-are-ontologies/ (accessed Feb. 8, 2023)

[7] Shimizu, Cogan et al. "The enslaved ontology: Peoples of the historic slave trade". _The Journal of Web Semantics_. 2019. https://doi.org/10.1016/j.websem.2020.100567

[8] P. Hitzler, M. Krotzsch, and S. Rudoplh, _Foundations of Semantic Web Technologies_. Boca Raton, FL, USA: CRC Press, 2010. https://doi.org/10.1201/9781420090512

## External Media References
Canto. What is metadata? (and why does it matter?). (Mar. 10, 2021). Accessed: Feb. 5, 2023. [Online Video]. Available: https://www.youtube.com/watch?v=fZWg0ClQkYQ

## Contributors
* Jehan Fernando
* Christopher Menart
* Alexander Moore
* Cogan Shimizu

