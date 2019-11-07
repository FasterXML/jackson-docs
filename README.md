This project is the main hub to all kinds of documentation related to the
Jackson JSON Processor.

# Tutorials

For your first steps in understanding how to use Jackson, following tutorials are good places to start:

* [Baeldung Jackson JSON Tutorial](https://www.baeldung.com/jackson)
* [Jackson in N minutes](https://github.com/FasterXML/jackson-databind/) (`README` for `jackson-databind` project)
* [Jenkov.com Jackson Tutorial](http://tutorials.jenkov.com/java-json/index.html)
* [JournalDev JacksonTutorial](https://www.journaldev.com/2324/jackson-json-java-parser-api-example-tutorial)
* [LogicBig.com Jackson Tutorial](https://www.logicbig.com/tutorials/misc/jackson.html)
* [Mkyong.com's Jackson Tutorial](https://www.mkyong.com/java/jackson-how-to-parse-json/) (part of larger [Java JSON Tutorials](https://www.mkyong.com/tutorials/java-json-tutorials)
* [StudyTrails Jackson Introduction](http://www.studytrails.com/java/json/java-jackson-introduction/)

# General

## Annotations

* [Jackson Annotations](../../wiki/JacksonAnnotations) (links to core/databind/JAXB annotations)
* [Customize your Java-JSON serialization using Jackson Annotations](https://medium.com/trabe/customize-your-serialization-using-jackson-annotations-d6b81c4785a6)
* [Advanced Jackson annotations](http://www.baeldung.com/jackson-advanced-annotations)

## Frameworks, Platforms

* [Jackson on Android](../../wiki/JacksonOnAndroid) (proguard definitions)

## JVM Languages beyond Java

(need links to Scala, Kotlin, Clojure tutorials, articles)

## Other

* [Where are the Javadocs?](../../wiki/Finding-Javadoc)
* [Presentations by Jackson Team, friends](../../wiki/Presentations)

# Documentation under Jackson GH projects

[Jackson project hub](../../../jackson) has links to all active Jackson projects.
These projects contain plenty of project-specific documentation, such as:

* [Core Annotations](../../../jackson-annotations)
    * [List of Jackson Core Annotations](../../../jackson-annotations/wiki/Jackson-Annotations)
* [Streaming API](../../../jackson-core/)
    * On/off features: [JsonFactory.Feature](../../../jackson-core/wiki/JsonFactory-Features)s, [JsonGenerator.Feature](../../../jackson-core/wiki/JsonGenerator-Features)s,[JsonParser.Feature](../../../jackson-core/wiki/JsonParser-Features)s.
* [Databind](../../../jackson-databind/)
    * [Databind Annotations](../../../jackson-databind/wiki/Databind-Annotations)
    * On/off features: [DeserializationFeature](../../../jackson-databind/wiki/Deserialization-Features)s, [SerializationFeature](../../../jackson-databind/wiki/Serialization-Features)s, [MapperFeature](../../../jackson-databind/wiki/Mapper-Features)s.

# External (off-GitHub) documentation

Blogs that regularly write about Jackson include:

* [Cowtowncoder @Medium](https://medium.com/@cowtowncoder)
* [CowTalk Blog](http://cowtowncoder.com/blog/blog.html) (old, getting obsolete)

And here are good articles around the web:

* General usage
    * [Jackson JSON Tutorial by Eugen Paraschiv](http://www.baeldung.com/jackson)
    * [Jackson - Installation](http://tutorials.jenkov.com/java-json/jackson-installation.html) at Jenkov.com
    * [Processing JSON with Jackson](https://dzone.com/articles/processing-json-with-jackson) (DZone)
    * [Jackson jr for casual JSON processing](https://medium.com/@cowtowncoder/jackson-jr-for-casual-json-reading-writing-from-java-f5d379d4bcb6#.i2j15cce8)
* Jackson annotations:
    * [A Guide to Jackson Annotations](http://www.baeldung.com/jackson-annotations) by Baeldung
    * [Jackson Annotations](http://tutorials.jenkov.com/java-json/jackson-annotations.html) at Jenkov.com
* Streaming reading/writing
    * [Customize serialization with Jackson Annotations](https://medium.com/trabe/customize-your-serialization-using-jackson-annotations-d6b81c4785a6)
* Streaming API
    * [Jackson - JsonParser](http://tutorials.jenkov.com/java-json/jackson-jsonparser.html)
    * [Jackson - JsonGenerator](http://tutorials.jenkov.com/java-json/jackson-jsongenerator.html)
* Polymorphic type handling:
    * [Custom polymorphic type handling with Jackson](http://www.thomaskeller.biz/blog/2013/09/10/custom-polymorphic-type-handling-with-jackson/) (2013 Sep)
* Data formats beyond JSON
    * [Writing CSV using Jackson CSVMapper & Mixin annotations](http://demeranville.com/writing-csv-using-jackson-csvmapper-mixin-annotations)
    * [Reading, Writing Java Properties with Jackson](https://medium.com/@cowtowncoder/reading-writing-java-properties-files-using-jackson-2-8-efd7a8da9d4c#.mv82no23b)
    * [Read YAML in Java with Jackson](https://dzone.com/articles/read-yaml-in-java-with-jackson)
* Platform-specific Jackson integration
    * [Apache CXF](http://cxf.apache.org/)
        * [Configuring Snake Case naming](https://mahichir.wordpress.com/2015/07/08/cxf-configuration-to-produce-json-snake-case-underscore-case-formatted-data-using-jackson-json-library/)

# Participating

The easiest ways to participate is to join one of Jackson mailing lists (Jackson google groups):

* [Jackson Announce](https://groups.google.com/forum/#!forum/jackson-announce): Announcement-only list for new Jackson releases, meetups and other events related to Jackson
* [Jackson User](https://groups.google.com/forum/#!forum/jackson-user): List dedicated for discussion on Jackson usage
* [Jackson Dev](https://groups.google.com/forum/#!forum/jackson-dev): List for developers of Jackson core components and modules, discussing implementation details, API changes.

There are other related lists and forums as well:

* [Smile Format Discussion](https://groups.google.com/forum/#!forum/smile-format-discussion): List for discussing details of the binary JSON format called [Smile](https://en.wikipedia.org/wiki/Smile_%28data_interchange_format%29) (see [Smile Specificat\
ion](http://wiki.fasterxml.com/SmileFormat))
* [Jackson Users](http://jackson-users.ning.com) is a Jackson-specific discussion forum for usage questions.

# Sample code

See [(External) Jackson Sample Code](../../wiki/ExternalJacksonSampleCode).

# On Jackson versioning

Note that there are two **major** Jackson versions: 1.x (1.0 - 1.9) and 2.x (2.0 - 2.9).
These versions can co-exist as they are located in different Java packages and use different jar naming and Maven group/artifact ids.
But this means that you have to make sure that all components in use have matching major versions: specifically, Jackson 2.x code does NOT understand or support Jackson 1.x annotations, or vice versa.

Minor versions (like 2.1 and 2.2) are backwards compatible with respect to public API: old code should work without recompilation, if (but only if) it relies on external API; public methods, annotations. When overriding internal functionality, we try hard to maintain backwards compatibility between adjacent minor versions; need for changes is indicated by deprecating internal methods. Recompilation is thus recommended when extending by sub-classing, for example.

# Misc other

* [Old Jackson home](http://jackson.codehaus.org) is still occasionally linked to from various places -- please DO NOT link from new documentation.
* [Jackson Git Hub](../../../jackson/) is the... The Hub for all stuff, including this project.
