---


---

<h2 id="big-data-principles-chapters-3-and-4-questions">Big Data Principles Chapters 3 and 4 Questions</h2>
<ul>
<li>
<p><a href="#chapter-3">Chapter 3</a></p>
</li>
<li>
<p><a href="#chapter-4">Chapter 4</a></p>
</li>
</ul>
<h4 id="chapter-3">Chapter 3</h4>
<h5 id="what-is-apache-thrift">1. - What is Apache Thrift?</h5>
<p>Apache Thrift is a tool that can be used to define statically typed, enforceable schemas. It provides an interface definition language to describe the schema in terms of generic data types, and this description can later be used to automatically generate the actual implementation in multiple programming languages.</p>
<h5 id="what-is-a-union">2. - What is a union?</h5>
<p>A single value that may have any of several representations and are useful for representing nodes.</p>
<h5 id="what-is-a-union-in-thrift">3. - What is a union in Thrift?</h5>
<p>Unions are defined by listing all possible representations.</p>
<h5 id="what-is-an-edge">4. - What is an edge?</h5>
<p>An edge can be represented as a struct containing two nodes. The name of an edge struct indicates the relationship it represents, and the fields in the edge struct contain the entities involved in the relationship.</p>
<h5 id="why-it-is-important-to-evolve-the-schema">5. - Why it is important to evolve the schema?</h5>
<p>Because as your business requirements change you’ll need to add new kinds of data, and you’ll want to do so as effortlessly as possible.</p>
<h5 id="why-numeric-identifiers-are-so-important-in-thrift">6. -Why numeric identifiers are so important in Thrift?</h5>
<p>There are two reason. The first one is because  they are used to identify fields in their serialized form, and the second one is because they are the key to evolving Thrift schemas.</p>
<h5 id="why-enforceable-schemas-are-consider-to-be-good-when-talking-about-finding-data">7.- Why enforceable schemas are consider to be good when talking about finding data?</h5>
<p>Because they allows to find the problem, if it’s the case, when writing the data as well as it provides full context of how and why the data become corrupted.</p>
<h5 id="why-only-optional-fields-can-be-added-to-existing-structs">8.- Why only optional fields can be added to existing structs?</h5>
<p>It is only possible to add optional fields because if you try to add required fields because, existing data won’t have those fields and thus won’t be deserializable.</p>
<h5 id="why-fields-may-be-renamed-when-you-want-to-change-the-schema-but-still-be-backward-compatible-with-existing-data">9.- Why fields may be renamed when you want to change the schema but still be backward compatible with existing data?</h5>
<p>This is because the serialized form of an object uses the field IDs, not the names, to identify fields.</p>
<h5 id="why-when-a-field-is-removed-you-cannot-reuse-that-field-id">10.- Why when a field is removed you cannot reuse that field ID?</h5>
<p>Because If you try to reuse a previously removed field ID, Thrift would try to deserialize that old data into the new field, which at the end will lead to invalid data.</p>
<h4 id="chapter-4">Chapter 4</h4>
<h5 id="how-can-vertical-partitioning-data-on-a-distributed-file-system-can-be-done">1.- How can vertical partitioning data on a distributed file system can be done?</h5>
<p>By sorting your data into separate folders.</p>
<h5 id="mention-a-big-problem-with-regular-file-systems.">2.- Mention a big problem with regular file systems.</h5>
<p>It exists on just a single machine, so you can only scale to the storage limits and processing power of that one machine.</p>
<h5 id="mention-some-differences-between-distributed-filesystems-and-regular-filesystems.">3.- Mention some differences between distributed filesystems and regular filesystems.</h5>
<p>Distributed filesystems spread their storage across a cluster of computers, and in that way we can have fault tolerance when a machine goes down. In other words, if you lose one machine, all your files and data will still be accessible.</p>
<p>The operations you can do with a distributed filesystem are often more limited than you can do with a regular filesystem.</p>
<p>Oftentimes having small files can be inefficient, so you must make sure you keep your file sizes relatively large to make use of the distributed filesystem properly.</p>
<h5 id="what-are-some-requirements-of-master-dataset-storage">4.- What are some requirements of master dataset storage</h5>
<ul>
<li>Write:
<ul>
<li>Efficient appends of new data.</li>
<li>Scalable storage</li>
</ul>
</li>
<li>Read: Support for parallel processing</li>
<li>Both:
<ul>
<li>Tuneable storage and processing cost</li>
<li>Enforceable immutability</li>
</ul>
</li>
</ul>

