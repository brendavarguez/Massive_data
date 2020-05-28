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
<h5 id="why-it-is-important-to-evolve-your-the-schema">5. - Why it is important to evolve your the schema?</h5>
<p>Because as your business requirements change you’ll need to add new kinds of data, and you’ll want to do so as effortlessly as possible.</p>
<h5 id="why-numeric-identifiers-are-so-important-in-thrift">6. -Why numeric identifiers are so important in Thrift?</h5>
<p>Because  they are used to identify fields in their serialized form and are the key to evolving Thrift schemas.</p>
<h5 id="mention-the-rules-that-must-be-followed-when-you-want-to-change-the-schema-but-still-be-backward-compatible-with-existing-data.">7.- Mention the rules that must be followed when you want to change the schema but still be backward compatible with existing data.</h5>
<ul>
<li>
<p>Fields may be renamed. This is because the serialized form of an object uses the field IDs, not the names, to identify fields.</p>
</li>
<li>
<p>A field may be removed, but you must never reuse that field ID. When deserializing existing data, Thrift will ignore all fields with field IDs not included in the schema. If you were to reuse a previously removed field ID, Thrift would try to deserialize that old data into the new field, which will lead to either invalid or<br>
incorrect data.</p>
</li>
<li>
<p>Only optional fields can be added to existing structs. You can’t add required fieldscbecause existing data won’t have those fields and thus won’t be deserializable.</p>
</li>
</ul>
<h4 id="chapter-4">Chapter 4</h4>
<h5 id="how-can-vertical-partitioning-data-on-a-distributed-file-system-can-be-done">1.- How can vertical partitioning data on a distributed file system can be done?</h5>
<p>By sorting your data into separate folders.</p>
<h5 id="mention-a-big-problem-with-regular-file-systems.">2.- Mention a big problem with regular file systems.</h5>
<p>It exists on just a single machine, so you can only scale to the storage limits and processing power of that one machine.</p>
<h5 id="mention-some-differences-between-distributed-filesystems-and-regular-filesystems.">3.- Mention some differences between distributed filesystems and regular filesystems.</h5>
<p>Distributed filesystems spread their storage across a cluster of computers. They scale by adding more machines to the cluster and are designed so that you have fault tolerance when a machine goes down, meaning that if you lose one machine, all your files and data will still be accessible.</p>
<p>The operations you can do with a distributed filesystem are often more limited than you can do with a regular filesystem. For instance, you may not be able to write to the middle of a file or even modify a file at all after creation.</p>
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

