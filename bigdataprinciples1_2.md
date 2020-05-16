---


---

<h1 id="chapter-1">Chapter 1</h1>
<h3 id="who-were-the-pioneers-in-creating-big-data-systems">1.- Who were the pioneers in creating big data systems?</h3>
<p>Google &amp; Amazon</p>
<h3 id="mention-some-examples-of-big-data-systems">2.- Mention some examples of big data systems</h3>
<ul>
<li>
<p>Google: distributed filesystems, the MapReduce computation framework, and distributed locking service</p>
</li>
<li>
<p>Amazon: Dynamo</p>
</li>
<li>
<p>Open source community: Hadoop, HBase, MongoDB, Cassandra, RabbitMQ, etc.</p>
</li>
</ul>
<h3 id="what-rdbms-stands-for">3.- What RDBMs stands for?</h3>
<p>Relational database management systems</p>
<h3 id="in-the-first-example-you-must-create-a-database-to-track-the-amount-of-pageviews-a-webpage-has.-why-the-rdbms-approach-didnt-work">4.- In the first example you must create a database to track the amount of pageviews a webpage has. Why the RDBMs approach didn’t work?</h3>
<p>I have to say that the stucture was good for a small amount of data. The problem arraived when the number of requests started to increase which means that it was not thought for big data application.</p>
<h3 id="when-the-database-can’t-keep-up-with-the-load-it-is-purposed-to-scale-with-a-queue.-how-does-this-fix-our-issue-and-what-is-the-poblem-to-use-a-queue-for-that">5.- When the database can’t keep up with the load, it is purposed to scale with a queue. How does this fix our issue and what is the poblem to use a queue for that?</h3>
<p>When a new pageview is received it is added to the queue and batches them into a single database update. If the database ever gets overloaded again, the queue will just get bigger instead of timing out to the web server and potentially losing data. However, if the number of requests keeps increasing and again the database gets overloaded, the worker will not be able to continue with the writes.</p>
<p>What is horizontal partitioning and, if we decided to do this, why it can represent a problem? Horizontal partitioning, also known as *sharding, involves splitting data from a database into smaller parts. If the number of requests increases, the complexity of this technique will also increase and it will be more difficult to manage.</p>
<h3 id="is-hadoop-always-a-good-tool-for-big-data">6.- Is Hadoop always a good tool for big data?</h3>
<p>It is true that Hadoop is capable to parallelize large-scale batch computations on very large amounts of data, but the computations have high latency. Therefore, if low-latency result are expected, Hadoop it is not recommended to be implemented.</p>
<h3 id="what-is-a-purpose-of-lambda-architecture">7.- What is a purpose of lambda architecture?</h3>
<p>The Lambda Architecture provides a general-purpose approach to implementing an arbitrary function on a dataset and having the function return its results with low latency.</p>
<p>The main idea of the Lambda Architecture is to build Big Data systems as a series of layers. Each layer satisfies a subset of the properties and builds upon the functionality provided by the layers beneath it.</p>
<h3 id="what-are-properties-are-desired-in-a-big-data-system">8.- What are properties are desired in a big data system?</h3>
<ul>
<li><strong>Robustness and fault tolerance</strong>: Systems need to behave correctly despite machines’ behaviors.</li>
<li><strong>Low latency reads and updates</strong>: It must access in a matter of milliseconds.</li>
<li><strong>Scalability</strong>: is the ability to maintain performance in the face of increasing data or load by adding resources to the system</li>
<li><strong>Generalization</strong>: It is desired for a system to support a variety of applications.</li>
<li><strong>Extensibility</strong>: Allow functionality to be added with a minimal development cost.</li>
<li><strong>Ad hoc queries</strong>: Ability to mine a dataset arbitrarily.</li>
<li><strong>Minimal maintenance</strong>: Minimum requirements to keep a system running</li>
<li><strong>Debuggability</strong>: Must provide the information necessary to debug the system when things go wrong.</li>
</ul>
<h3 id="mention-some-problems-regarding-the-fully-incremental-architectures.">9.- Mention some problems regarding the fully incremental architectures.</h3>
<ul>
<li>Operational complexity</li>
<li>Extreme complexity of achieving eventual consistency</li>
<li>Lack of human-fault tolerance</li>
</ul>
<h3 id="describe-the-different-layers-of-lambda-architecture">10.- Describe the different layers of lambda architecture:</h3>
<ul>
<li>
<p>Batch layer: Stores master dataset (very large list of records) and computes arbitrary views.</p>
</li>
<li>
<p>Serving layer: Random access to batch views and it is updated by batch layer. Doesn’t need to support random writes which makes these kind of databases very simple due to random writes cause most of the complexity in databases.</p>
</li>
<li>
<p>Speed layer: Compensate for high latency of updates to serving layer. Fast, incremental algorithms. Batch layer eventually overrides speed layer</p>
</li>
</ul>
<h3 id="why-elastic-clouds-are-so-popular-nowadays">11.- Why elastic clouds are so popular nowadays?</h3>
<p>Allow to rent hardware on demand rather than own your own hardware in your own location. They let you increase or decrease the size of your cluster nearly instantaneously and dramatically simplify system administration. Elastic clouds also provide additional storage and hardware allocation options that can significantly drive down the price of your infrastructure.</p>
<h3 id="what-are-the-five-categories-of-open-source-project">12.- What are the five categories of open source project?</h3>
<ul>
<li>
<p>Batch computation systems: They are high latency systems and they can do nearly arbitrary computations.</p>
</li>
<li>
<p>Serialization frameworks: Provide tools and libraries for using objects between languages. They can serialize an object into a byte array from any language, and then desirialize that byte array into an object in any language.</p>
</li>
<li>
<p>Random-access NoSQL databases: They sacrifice the full expressiveness of SQL and instead specialize in certain kind of operations and they all have specific purposes.</p>
</li>
<li>
<p>Messaging/quering systems: They provide a way to send and consume messages between processes in a fault-tolerant and asynchronous manner. A massage queue is a key component for doing realtime processing.</p>
</li>
<li>
<p>Realtime computation system: They can’t do the range of computations a batch-processing system can, however they have the advantage to process messages extremely quickly.</p>
</li>
</ul>
<h1 id="chapter-2">Chapter 2</h1>
<h3 id="provide-a-brief-explanation-of-the-following-terms-information-data-queries-and-views.">1.- Provide a brief explanation of the following terms: information, data, queries and views.</h3>
<p><strong><em>Information</em></strong><em>:</em> is the general collection of knowledge relevant to your Big Data system.<br>
<em><strong>Data:</strong></em> Information that can’t be derived from anything else.<br>
<strong><em>Queries:</em></strong>  are questions you ask of your data.<br>
<strong><em>Views:</em></strong>  are information that has been derived from your base data.</p>
<h3 id="when-the-author-mentions-that-data-is-immutable-what-does-it-means">2.- When the author mentions that data is immutable, what does it means?</h3>
<p>It means that data cannot be changed or deleted but it is possible to add more data.</p>
<h3 id="mention-two-advantages-of-immutable-data.">3.- Mention two advantages of immutable data.</h3>
<p>The most important advantages are Human-fault tolerance and simplicity.</p>
<h3 id="what-is-the-fact-based-model">4.- What is the fact-based model?</h3>
<p>In the fact-based model, data is deconstructed into fundamental units called <em>facts</em> and sores raw data as atomic facts. The fact-based model keeps the facts immutable and eternally true by using timestamps and ensures each fact is identifiable so that query processing can identify duplicates.</p>
<h3 id="mention-some-advantages-of-the-fact-based-model.">5.- Mention some advantages of the fact-based model.</h3>
<ul>
<li>Data is queryable at any time in its history</li>
<li>Data tolerates human errors</li>
<li>The dataset handles partial information</li>
<li>Has the advantages of both normalized and denormalized forms</li>
</ul>
<h3 id="what-is-a-graph-schema">6.- What is a graph schema?</h3>
<p>Graphs that capture the structure of a dataset stored using the fact-based model.</p>
<h3 id="mention-some-components-of-a-graph-schema.">7.- Mention some components of a graph schema.</h3>
<ul>
<li><strong>Nodes</strong>: are the entities in the system.</li>
<li><strong>Edges</strong>: are relationships between nodes.</li>
<li><strong>Properties</strong>: are information about entities.</li>
</ul>

