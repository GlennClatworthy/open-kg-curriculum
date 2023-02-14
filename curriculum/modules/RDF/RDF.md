# RDF
## Details
* Category: [Standards](../../categories/Standards.md), [Markup Languages](../../categories/Markup_Languages.md)
* Module Prerequisites: None
* Audience: [Student](../../audiences/Student.md), [Developer](../../audiences/Developer.md)
* Level: [Beginner](../../levels/Beginner.md)

## Content


#### What Is RDF?

RDF, or the **Resource Description Framework**, is ["a standard model for data interchange on the Web."](https://www.w3.org/RDF/) Maintained and promoted by the [World Wide Web Consortium (W3C)](https://www.w3.org), RDF helps organizations, companies, and individuals organize information from multiple websites and other internet sources in a structured format supporting advanced knowledge sharing and discovery.

#### The Structure of RDF

RDF's structure is comprised of three-part statements, known as *triples*, which point to resources on the web and assign values to properties describing them.  For example, the statement:

    William Shakespeare | wrote | Hamlet
    
tells us that an individual (Shakespeare) has a property (wrote), the value of which is "Hamlet." That statement also can be expressed as:

    <https://en.wikipedia.org/wiki/William_Shakespeare>  <https://schema.org/author>  "Hamlet".
    
In the RDF lexicon, the three columns in the above triple are called **subject**, **predicate**, and **object**. The *subject* column points to a web resource that the triple is describing, in this case the Wikipedia entry for William Shakespeare. The predicate column defines some aspect, or *property*, that you want to attribute to the subject. Here it points to a property called "author" that is documented at a website called schema.org. The third column, *object*, contains the value of the property, namely "Hamlet."

Notice that the first two columns above are written as [**URIs**](../../modules/What_is_an_Identifier/What_is_an_Identifier.md), which are a more generalized form of URLs, and the last is a text string in quotation marks. A fundamental rule of RDF is that *subject and predicate columns must always contain URIs*. The object column may be written either as a text string (as above) or as another URI.

URIs serve as unique identifiers, similar to a U.S. Social Security number or the item number of a component in a warehouse. Although there's no rule stating that a URI *has* to point to a real resource on the web, it is considered best practice to do so, allowing a user to follow a URI to its source in order to find out more about it.

RDF's structure is similar to rows in spreadsheets in that it allows the repetition of elements. For example:

    <https://en.wikipedia.org/wiki/William_Shakespeare>  <https://schema.org/author>  "Hamlet".
    <https://en.wikipedia.org/wiki/William_Shakespeare>  <https://schema.org/author>  "Macbeth".

are two perfectly valid triples, differing only in the works to which they refer.

Finally, notice that the first two columns refer to resources available at two different locations. The true power of RDF lies in its ability to seemlessly combine information, whether it be Wikipedia pages, articles from commercial websites, or terms from a variety of online vocabularies. Thus the disparate, chaotic world wide web can be interconnect and organized using the simple structural components of RDF.

#### Serializations

It's important to note that RDF is *not* a file format. A variety of formats, known as [serializations](../../../curriculum/modules/RDF_Serializations/RDF_Serializations.md), are available, each differing in the way triples are structured in text files. For example, the above examples are written as [**N-Triples**](https://www.w3.org/TR/n-triples/), which arguably is the simplest and most straightforward RDF serialization format.

Users choose serializations based on their needs and compatibility with other systems. One of the most compact and therefore popular formats is called [**Turtle**](https://www.w3.org/TR/turtle/). Here is the above example expressed in Turtle form:

    @prefix wiki: <https://en.wikipedia.org/wiki/>.
    @prefix sch: <https://schema.org/>.
    
    wiki:William_Shakespeare sch:author "Hamlet", "Macbeth".

#### Composing RDF documents

Composing an RDF document can be as simple as opening up a text editor and writing triples in the author's preferred format. However, a wide variety of commercial and open source [modeling tools](../../../curriculum/modules/Survey_of_Modeling_Tools/Survey_of_Modeling_Tools.md) are available to assist the user in composing RDF. Third party software offers two advantages: it provides a standard interface that can simplify the construction of triples; and it may provide checking capabilities to prevent the user from committing structural and logical errors.

#### RDF and Triplestores

RDF's value begins to emerge when it is loaded into a special kind of database called a [triple store.](../../../curriculum/modules/Survey_of_Triplestores/Survey_of_Triplestores.md) Triple stores can be used to import, combine, update, query, and often [visualize](../../../curriculum/modules/Survey_of_Visualization_Tools/Survey_of_Visualization_Tools.md) the information stored in RDF formats. Similar to modelling tools, triple stores are available as paid commercial, free commercial, and open source versions distributed by various companies and organizations. These applications employ a query language called [**SPARQL**](../../../curriculum/modules/SPARQL/SPARQL.md), which is similar in structure to the Turtle example above. For example, the query:

    PREFIX wiki: <https://en.wikipedia.org/wiki/>.
    PREFIX sch: <https://schema.org/>.

    SELECT ?Play
    WHERE {
        wiki:William_Shakespeare sch:author ?Play .
          }

returns the results:

| ?Play         |
| :---          |
| Hamlet        |
| Macbeth       |

       

The number of triples you can store in one database repository is limited only to the software itself and the amount of room you have on your local drive. Importing triples from a variety of sources--and defining connections between subjects, predicates, and objects from those sources--is the first step in the the consolidation of disparate collections and subsequent knowledge discovery.

#### Beyond Basic RDF

While RDF provides the template for organizing linked data in the form of triples, it's only a starting point. RDF-based standards like [**RDFS**](../../../curriculum/modules/RDFS/RDFS.md), [**SKOS**](../../../curriculum/modules/SKOS/SKOS.md), and [**OWL**](../../../curriculum/modules/OWL/OWL.md) extend the framework to allow for grouping resources into classes as well as defining basic restrictions on relationships (RDFS); creating hierarchical taxonomies of vocabulary terms (SKOS); and developing complex relationships and constraints among resources based on advanced principles of logic (OWL).

## Related KGC Media
* Knowledge Graph Conference Bookclub Session: [Semantic Web for the Working Ontologist, Third Edition, Chapters 1-3](https://watch.knowledgegraph.tech/packages/kgc-21-attendees/videos/bookclub2)

* Tutorial Example

## References
[1] [RDF](https://www.w3.org/RDF/) at the W3C
[2] [N-Triples](https://www.w3.org/TR/n-triples/)
[3] [RDF 1.1 Turtle](https://www.w3.org/TR/turtle/) at the W3C

## Contributors
* Cogan Shimizu
* Glenn Clatworthy
