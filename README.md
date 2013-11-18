# Overview

This project is the main hub to all kinds of documentation related to
Jackson JSON Processor.

# Structure

Documentation within this project is categorized under:

* [Presentations by Jackson Team, friends](../../wiki/Presentations)
* [Where the #%($#^ are Javadocs?](../../wiki/Finding-Javadoc)
* [List of Jackson 2.x Annotations](../../wiki/JacksonAnnotations)

# Tutorials

For your first steps in understanding how to use Jackson, following tutorials are good places to start:

* [Jackson Tutorial by StudyTrails](http://www.studytrails.com/java/json/java-jackson-introduction.jsp)
* [Jackson in N minutes](https://github.com/FasterXML/jackson-databind/) (`README` for `jackson-databind` project)
* Older [Jackson in 5 minutes](http://wiki.fasterxml.com/JacksonInFiveMinutes) version (useful for 1.x)

# Documentations within related GH projects

[Jackson project hub](../../../jackson) has links to all active Jackson projects.

And those projects have some 'local' documentation, such as:

* [Streaming API](../../../jackson-core/), on/off features
    * [JsonFactory.Feature](../../../jackson-core/wiki/JsonFactory-Features)s.
    * [JsonGenerator.Feature](../../../jackson-core/wiki/JsonGenerator-Features)s.
    * [JsonParser.Feature](../../../jackson-core/wiki/JsonParser-Features)s.
* [Databind](../../../jackson-databind/), on/off features
    * [DeserializationFeature](../../../jackson-databind/wiki/Deserialization-Features)s.
    * [SerializationFeature](../../../jackson-databind/wiki/Serialization-Features)s.
    * [MapperFeature](../../../jackson-databind/wiki/Mapper-Features)s.

# External (off-github) documentation

Following sites are good sources for documentation:

* Old [FasterXML Jackson Wiki](http://wiki.fasterxml.com/JacksonHome) -- will be replaced by this project!
* [Jackson Users forum](http://jackson-users.ning.com)
* [CowTalk Blog](http://cowtowncoder.com/blog/blog.html)

And here are good one-off articles from around the web:

* [Custom polymorphic type handling with Jackson](http://www.thomaskeller.biz/blog/2013/09/10/custom-polymorphic-type-handling-with-jackson/) (2013 Sep)

# On Jackson versioning

Note that there are two **major** Jackson versions: 1.x (1.0 - 1.9) and 2.x (2.0 - 2.3).
These versions can co-exist as they are located in different Java package and use different jar naming and Maven group/artifact ids.
But this means that you have to make sure that all components in use have matching major versions: specifically, Jackson 2.x code does NOT understand or support Jackson 1.x annotations, or vice versa.

Minor versions (like 2.1 and 2.2) are backwards compatible with respect to public API: old code should work without recompilation, if (but only if) it relies on external API; public methods, annotations. When overriding internal functionality, we try hard to maintain backwards compatibility between adjacent minor versions; need for changes is indicated by deprecating internal methods. Recompilation is thus recommended when extending by sub-classing, for example.

# Misc other

* [Old Jackson home](http://jackson.codehaus.org) is still occasionally linked to from various places -- please DO NOT link from new documentation.
* [Jackson Git Hub](../../../jackson/) is the... The Hub for all stuff, including this project.

