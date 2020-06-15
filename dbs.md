<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>types of dbs</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__left">
    <div class="stackedit__toc">
      
<ul>
<li><a href="#types-of-databases">Types of databases</a>
<ul>
<li><a href="#in-memory">In-memory</a></li>
<li><a href="#graph">Graph</a></li>
<li><a href="#document-oriented">Document-oriented</a></li>
<li><a href="#references">References</a></li>
</ul>
</li>
</ul>

    </div>
  </div>
  <div class="stackedit__right">
    <div class="stackedit__html">
      <h1 id="types-of-databases">Types of databases</h1>
<p>This document was created by:<br>
Alexa Canché, Carolina Garma &amp; Brenda Martín</p>
<ul>
<li><a href="#in-memory">In-memory</a>
<ul>
<li><a href="#how-does-it-works">How does it works?</a></li>
<li><a href="#advantages-and-disadvantages-of-in-memory-databases"> Advantages and disadvantages of In-memory databases</a></li>
<li><a href="#common-use-cases">Common use cases</a></li>
<li><a href="#traditional-database-vs-in-memory-database">Traditional database vs In-memory database</a></li>
<li><a href="#how-do-i-know-my-business-needs-a-in-memory-database">How do I know my business needs a in-memory database?</a></li>
<li><a href="#popular-in-memory-databases">Popular in-memory databases</a></li>
<li><a href="#comparison-between-imdbs">Comparison between IMDBs</a></li>
</ul>
</li>
<li><a href="#graph">Graph</a>
<ul>
<li><a href="#description">Descriptions</a></li>
<li><a href="#eExample">Example</a></li>
<li><a href="#aApplications">Applications</a></li>
<li><a href="#cCapabilities">Capabilities</a></li>
<li><a href="#lLimitations">Limitations</a></li>
<li><a href="#popular-open-source-graph-databases">Popular open-source graph databases</a></li>
<li><a href="#comparison-matrix-between-graph-databases">Comparison matrix between graph databases</a></li>
</ul>
</li>
<li><a href="#document-oriented">Document-oriented</a>
<ul>
<li><a href="#document-features">Document features</a></li>
<li><a href="#addresing-documents">Addresing documents</a></li>
<li><a href="#organization">Organization</a></li>
<li><a href="#api-%E2%80%93--query-language">API – Query language</a></li>
<li><a href="#applications">Applications</a></li>
<li><a href="#limitations">Limitations</a></li>
<li><a href="#popular-open-source-document-oriented-databases">Popular open-source document-oriented databases</a></li>
<li><a href="#comparison-matrix-between-document-oriented-databases">Comparison matrix between document-oriented databases</a></li>
</ul>
</li>
<li><a href="#references">References</a></li>
</ul>
<h2 id="in-memory">In-memory</h2>
<p>A in-memory database (IMDB, also known as a main memory database or MMDB) is a type of database management system which storage data on the main memory. One of the big differences between a database management system that uses a disk storage mechanism and a in-memory database, is that a in-memory database is considerable faster when talking about response time due to disk access is slower than memory access. An important disadvantage of IMDBs is that it exists a great risk to lose data upon a process or server failure because all data is stored and managed in the main memory. However, a IMDB is also capable to save data on a disk by storing each operation in a log or by taking snapshots.</p>
<h3 id="how-does-it-works">How does it works?</h3>
<p>According to information provided by Margaret Rouse in her blog post <a href="https://whatis.techtarget.com/definition/in-memory-database"> in-memory database</a>: “Source data is loaded into system memory in a compressed, non-relational format”.  This means that there is no need to decompress, decrypt or decode data, which allows direct navigation.</p>
<p>The quick response of a in-memory database is possible because is not necessary to translate and cache data, which means that data is used in the same form as the in-memory database management system.</p>
<p>According to OmniSci: “An in-memory database system can also act as an read-only analytic database that stores historical data on metrics for business intelligence (BI) applications. This eliminates data indexing, which can reduce IT costs”.</p>
<h3 id="advantages-and-disadvantages-of-in-memory-databases">Advantages and disadvantages of In-memory databases</h3>

<table>
<thead>
<tr>
<th>Advantages</th>
<th>Disadvantages</th>
</tr>
</thead>
<tbody>
<tr>
<td>There is no need to deal with secondary storage since it manages all data in the RAM</td>
<td>The type of memory used is not persistent</td>
</tr>
<tr>
<td>Optimized for high-performance</td>
<td>The volume of data that can be stored tends to be much smaller</td>
</tr>
<tr>
<td>Quicker data analysis</td>
<td>The data stored is only temporary</td>
</tr>
<tr>
<td>Better transfer speed of unstructured data</td>
<td>It is not the best option in terms of security</td>
</tr>
</tbody>
</table><h3 id="common-use-cases">Common use cases</h3>
<ul>
<li>Real time bidding</li>
<li>Online interactive gaming</li>
<li><a href="https://www.omnisci.com/learn/geospatial">Geospatial</a>/<a href="https://www.omnisci.com/technical-glossary/gis">GIS</a> processing</li>
</ul>
<h3 id="traditional-database-vs-in-memory-database">Traditional database vs In-memory database</h3>

<table>
<thead>
<tr>
<th>Traditional database</th>
<th>In-memory database</th>
</tr>
</thead>
<tbody>
<tr>
<td>Retrieves data from disk drives</td>
<td>Keeps all data in the main memory</td>
</tr>
<tr>
<td>Data can be more easily restored from the disks</td>
<td>Data is lost when there is a loss of power</td>
</tr>
<tr>
<td>When one part refers to another part, a different block must be read from the disk</td>
<td>Different parts of the database can be managed through direct pointers</td>
</tr>
<tr>
<td>Store redundant data as the system creates a copy of it for each component added to the system</td>
<td>Allow real-time analysis and reporting of data</td>
</tr>
</tbody>
</table><h3 id="how-do-i-know-my-business-needs-a-in-memory-database">How do I know my business needs a in-memory database?</h3>
<p>According to Ionos, if you consider the following statements are true, then you need a IMDB:</p>
<ul>
<li>You need fast and frequent access to your data.</li>
<li>Your existing database management systems or servers are overloaded,</li>
<li>Data persistence is not your highest priority.</li>
<li>Loss of data (or at least the possibility of this) is workable for you.</li>
</ul>
<h3 id="popular-in-memory-databases">Popular in-memory databases</h3>
<ul>
<li>Redis</li>
<li>Aerospike</li>
<li>TimesTen</li>
<li>SAP HANA</li>
</ul>
<h3 id="comparison-between-imdbs">Comparison between IMDBs</h3>

<table>
<thead>
<tr>
<th></th>
<th align="center"><br>Redis</th>
<th>Aerospike</th>
<th>OmniSci</th>
<th>MonetDB</th>
</tr>
</thead>
<tbody>
<tr>
<td><br>Best used</td>
<td align="center">For rapidly changing data with a foreseeable database size (should fit mostly in memory)</td>
<td>Eliminates tradeoffs in consistency and scale for always-on globally distributed business transactions.</td>
<td>High performance, rapid query compilation, query vectorization and advanced memory management.</td>
<td></td>
</tr>
<tr>
<td><br>Usage example</td>
<td align="center">Stock prices. Analytics. Real-time data collection. Real-time communication.</td>
<td>Fight fraud. Increase shopping cart size. Deploy global digital payment networks.</td>
<td>Track ships. Visualize hundreds of millions of tweets in real time. View historical flight data such as delays and other activity.</td>
<td>Online analytical processing. Data mining. Geographic information system (GIS). Resource Description Framework (RDF). Text retrieval.</td>
</tr>
<tr>
<td><br>Known Shortcomings</td>
<td align="center">Sizes limited by amount of RAM.</td>
<td>Size is limited in the community edition.<br>No transactions.</td>
<td>Supports Web Mercator projection only.<br><br>Some operators are not able to be used with certain data types.<br><br>There is an issue with automatic migration if the source database was migrated through any of the following releases: 3.2.1, 3.2.2 or 3.2.3.</td>
<td>Lack of documentation<br></td>
</tr>
<tr>
<td><br>Main focus</td>
<td align="center">Speed</td>
<td>Speed and storage</td>
<td></td>
<td></td>
</tr>
<tr>
<td><br>License</td>
<td align="center">BSD</td>
<td>AGPL</td>
<td>Apache</td>
<td>Mozilla Public License</td>
</tr>
<tr>
<td><br>Pricing</td>
<td align="center">Free download</td>
<td>Free download<br>Enterprise ed</td>
<td>Free download<br>Enterprise ed</td>
<td>Free download</td>
</tr>
<tr>
<td><br>Projects using it</td>
<td align="center"><a href="http://craigslist.org">craigslist.org</a><br> <br><a href="http://github.com">github.com</a><br> <br><a href="http://guardian.co.uk">guardian.co.uk</a><br> <br>Disqus<br> <br><a href="http://stackoverflow.com">stackoverflow.com</a><br> <br><a href="http://flickr.net">flickr.net</a><br> <br><a href="http://tweetdeck.com">tweetdeck.com</a><br> <br><a href="http://blizzard.com">blizzard.com</a></td>
<td>paytm<br><br>Naukri.com<br><br>JustWatch<br><br>Tiamat.Tech<br><br>mParticle<br><br>Snapdeal</td>
<td>Simulmedia<br><br>MPM<br><br>Skyhook</td>
<td>SciLens project<br><br>COMMIT<br><br>LDBC</td>
</tr>
<tr>
<td>Technical details</td>
<td align="center"></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><br>Latest version</td>
<td align="center">5.0.9</td>
<td>4.8.0.3</td>
<td>5.2.2</td>
<td>11.37.7</td>
</tr>
<tr>
<td><br>Release date</td>
<td align="center">2020 Apr 17</td>
<td>2020 Jan 6</td>
<td>2020 May 7</td>
<td>2020 Jun</td>
</tr>
<tr>
<td><br>Initial release date</td>
<td align="center">2009</td>
<td>2012</td>
<td>2013</td>
<td>2004</td>
</tr>
<tr>
<td><br>Consistency</td>
<td align="center"></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><br>Replication</td>
<td align="center">Master/slave</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><br>Protocol</td>
<td align="center">Telnet-like</td>
<td>HTTP</td>
<td>HTTP</td>
<td>SAPARQL</td>
</tr>
<tr>
<td><br>Data Presentation</td>
<td align="center"></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><br>Development language</td>
<td align="center">C/C++</td>
<td>C</td>
<td></td>
<td>C</td>
</tr>
<tr>
<td><br>Platforms</td>
<td align="center">Cross-platform</td>
<td></td>
<td>Cross-platform</td>
<td>Cross-platform</td>
</tr>
<tr>
<td><br>API Language</td>
<td align="center"></td>
<td></td>
<td></td>
<td>Ruby<br>Python</td>
</tr>
<tr>
<td><br>Embedded Language</td>
<td align="center">None</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Additional</td>
<td align="center"></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><br>Website</td>
<td align="center"><a href="http://redis.io">redis.io</a></td>
<td><a href="https://www.aerospike.com/">https://www.aerospike.com/</a></td>
<td><a href="https://www.omnisci.com/">https://www.omnisci.com/</a></td>
<td><a href="http://www.monetdb.org">www.monetdb.org</a></td>
</tr>
<tr>
<td><br>Wikipedia</td>
<td align="center"><a href="http://wikipedia.org/">wikipedia.org/</a>…</td>
<td><a href="https://en.wikipedia.org/wiki/Aerospike_(database)">https://en.wikipedia.org/wiki/Aerospike_(database)</a></td>
<td><a href="https://en.wikipedia.org/wiki/OmniSci">https://en.wikipedia.org/wiki/OmniSci</a></td>
<td><a href="https://en.wikipedia.org/wiki/MonetDB">https://en.wikipedia.org/wiki/MonetDB</a></td>
</tr>
<tr>
<td><br>Additional link</td>
<td align="center"></td>
<td></td>
<td><a href="https://github.com/omnisci/omniscidb/wiki/Architecture">https://github.com/omnisci/omniscidb/wiki/Architecture</a></td>
<td></td>
</tr>
<tr>
<td>Features</td>
<td align="center"></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><br>Cloud DB</td>
<td align="center"></td>
<td>Yes</td>
<td>Yes</td>
<td></td>
</tr>
<tr>
<td><br>Transaction support</td>
<td align="center">Yes</td>
<td>No</td>
<td></td>
<td></td>
</tr>
<tr>
<td><br>Domain-model Aggregation</td>
<td align="center"></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><br>GeoSpatial</td>
<td align="center"></td>
<td></td>
<td>Yes</td>
<td>Yes</td>
</tr>
<tr>
<td><br>FullText</td>
<td align="center"></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><br>Commercial Support</td>
<td align="center"></td>
<td></td>
<td>Yes</td>
<td></td>
</tr>
</tbody>
</table><h2 id="graph">Graph</h2>
<p>Graph databases are purpose-built to store and navigate relationships. Relationships are first-class citizens in graph databases, and most of the value of graph databases is derived from these relationships. Graph databases use nodes to store data entities, and edges to store relationships between entities.</p>
<h3 id="description">Description</h3>
<p>To better grasp the concept of graph databases, it’s important to understand the following terms:</p>

<table>
<thead>
<tr>
<th>Terms</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>Node</td>
<td>A node is a representation of an individual entity tracked by a graph database. For example, in a graph database of music recording artists, a node might represent a single performer or band.</td>
</tr>
<tr>
<td>Property</td>
<td>A property is relevant information related to individual nodes. Building on our recording artist example, some properties might be “vocalist,” “jazz,” or “platinum-selling artist,” depending on what information is relevant to the database.</td>
</tr>
<tr>
<td>Edge</td>
<td>A property is relevant information related to individual nodes. Building on our recording artist example, some properties might be “vocalist,” “jazz,” or “platinum-selling artist,” depending on what information is relevant to the database.</td>
</tr>
<tr>
<td>Directed Graph</td>
<td>In a directed graph, edges can have different meanings based on which direction the relationship originates from. In this case, edges are “one-way” relationships. For example, a directed graph database might specify a relationship from Sammy to the Seaweeds showing that Sammy produced an album for the group but might not show an equivalent relationship from The Seaweeds to Sammy.</td>
</tr>
<tr>
<td>Undirected Graph</td>
<td>In an undirected graph, the edges between nodes exist just to show a connection between them. In this case, edges can be thought of as “two-way” relationships — there’s no implied difference between how one node relates to the other.</td>
</tr>
</tbody>
</table><h3 id="example">Example</h3>
<p>Twitter is a perfect example of a graph database connecting 330 million monthly active users.</p>
<p>In the illustration below, we have a small slice of Twitter users represented in a graph database. Each node (labeled User) belongs to a single person and is connected with relationships describing how each user is connected. As we see below, Peter and Emil follow each other, as do Emil and Johan, but although Johan follows Peter, Peter hasn’t (yet) reciprocated.</p>
<p><img src="https://dist.neo4j.com/wp-content/uploads/20180711200201/twitter-users-graph-database-model-peter-emil-johan.png" alt="Twitter users represented in a graph database model"></p>
<h3 id="applications">Applications</h3>
<ul>
<li><strong>Fraud detection:</strong> Graph databases are capable of sophisticated fraud prevention. With graph databases, you can use relationships to process financial and purchase transactions in near-real time. With fast graph queries, you are able to detect that, for example, a potential purchaser is using the same email address and credit card as included in a known fraud case.  **Recommendation engines:**Graph databases can also help you easily detect relationship patterns such as multiple people associated with a personal email address, or multiple people sharing the same IP address but residing in different physical addresses.</li>
<li><strong>Recommendation engines:</strong> Graph databases are a good choice for recommendation applications. With graph databases, you can store in a graph relationships between information categories such as customer interests, friends, and purchase history. You can use a highly available graph database to make product recommendations to a user based on which products are purchased by others who follow the same sport and have similar purchase history. Or, you can identify people who have a friend in common but don’t yet know each other, and then make a friendship recommendation.</li>
</ul>
<h3 id="capabilities">Capabilities</h3>
<ul>
<li>Models graphs consisting of nodes and edges with properties (meta-data) describing them.</li>
<li>Implement very fast graph traversal operations.</li>
<li>Also, support indexing of metadata to enable graph traversal combined with search queries.</li>
</ul>
<h3 id="limitations">Limitations</h3>
<ul>
<li>Difficult to scale for large data sets for generic graphs.</li>
<li><a href="http://giraph.apache.org/">Giraph</a> uses the <a href="https://en.wikipedia.org/wiki/Bulk_synchronous_parallel">Bulk Synchronous Parallel model</a> to overcome some of the scalability limitations.</li>
</ul>
<h3 id="popular-open-source-graph-databases">Popular open-source graph databases</h3>

<table>
<thead>
<tr>
<th>Database</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="https://neo4j.com/">Neo4j</a></td>
<td>An <a href="https://en.wikipedia.org/wiki/ACID">ACID</a>-compliant DBMS with native graph storage and processing. As of this writing, Neo4j is <a href="https://db-engines.com/en/ranking/graph+dbms">the most popular graph database in the world</a>.</td>
</tr>
<tr>
<td><a href="https://www.arangodb.com/">ArangoDB</a></td>
<td>Not exclusively a graph database, ArangoDB is a multi-model database that unites the graph, document, and key-value data models in one DBMS. It features AQL (a native SQL-like query language), full-text search, and a ranking engine.</td>
</tr>
<tr>
<td><a href="https://orientdb.com/">OrientDB</a></td>
<td>Another multi-model database, OrientDB supports the graph, document, key-value, and object models. It supports SQL queries and ACID transactions.</td>
</tr>
</tbody>
</table><h3 id="comparison-matrix-between-graph-databases">Comparison matrix between graph databases</h3>

<table>
<thead>
<tr>
<th></th>
<th align="center">Neo4j</th>
<th align="center">OrientDB</th>
<th align="center">ArangoDB</th>
<th align="center">Amazon Neptune</th>
<th align="center">AllegroGraph</th>
</tr>
</thead>
<tbody>
<tr>
<td>Description</td>
<td align="center">Open-source, supports ACID, has high-availability clustering for enterprise deployments, and comes with a web-based administration that includes full transaction support and visual node-link graph explorer; accessible from most programming languages using its built-in REST web API interface, and a proprietary Bolt protocol with official drivers</td>
<td align="center">Second-generation distributed graph database with the flexibility of documents in one product (i.e., it is both a graph database and a document NoSQL database).</td>
<td align="center">NoSQL native multi-model database system developed by ArangoDB Inc. The database system supports three important data models (key/value, documents, graphs) with one database core and a unified query language called AQL (ArangoDB Query Language)</td>
<td align="center">Amazon Neptune is a fully managed graph database by <a href="http://Amazon.com">Amazon.com</a>. It is used as a web service and is part of Amazon Web Services. Supports popular graph models property graph and W3C’s RDF, and their respective query languages Apache TinkerPop Gremlin and SPARQL</td>
<td align="center">Resource Description Framework (RDF) and graph database</td>
</tr>
<tr>
<td>Query example</td>
<td align="center">LOAD CSV WITH HEADERS FROM “<a href="https://raw.githubusercontent.com/neo4j/neo4j/2.3/manual/cypher/cypher-docs/src/docs/graphgists/query-tuning/movies.csv">https://raw.githubusercontent.com/neo4j/neo4j/2.3/manual/cypher/cypher-docs/src/docs/graphgists/query-tuning/movies.csv</a>” AS line 	MERGE (m:Movie {title:line.title}) 	ON CREATE SET m.released = toInt(line.released), m.tagline = line.tagline</td>
<td align="center">Traverse records from a root node:    orientdb&gt; SELECT FROM 11:4 WHERE ANY() TRAVERSE(0,10) (address.city = ‘Rome’)</td>
<td align="center">FOR i IN 1…1000               INSERT {                     name: CONCAT(“test”, i),                     status: 1 + (i % 5)                   } IN myCollection</td>
<td align="center">Gremlin: Add vertex with label and property:  g.addV(‘person’).property(‘name’, ‘justin’)</td>
<td align="center">Here’s a sample query which locates all rulers whose grandchildren inherited the crown: conn.setNamespace(’’, ‘ex://’) query = conn.prepareTupleQuery(query="""     SELECT DISTINCT ?name WHERE {         ?grandchild :child_of/:child_of ?name .     } ORDER BY ?name “”") with query.evaluate() as result:     for bindings in result:                   print(bindings.getValue(‘name’))</td>
</tr>
<tr>
<td>Pricing</td>
<td align="center">Community edition: free. Depending on the license will be the cost.</td>
<td align="center">Community: free, Standard: 5970 USD, Enterprise: 9750 USD</td>
<td align="center">Community: free. Enterprise: need to contact.</td>
<td align="center">On-Demand Instances let you pay for your database by the hour with no long-term commitments or upfront fees</td>
<td align="center">free, development and enterprise</td>
</tr>
<tr>
<td>Projects using it</td>
<td align="center">Associated-rules, Baryon, Graph Algorithm Visualization Tool, Visualize Breast Cancer with GraphXR</td>
<td align="center"><a href="http://www.baasbox.com">www.baasbox.com</a>, Cisco, United Nations, Dell, Sky, Accenture</td>
<td align="center">Refinitiv: Fast &amp; Secure Single-View of Everything with ArangoDB, Liaison’s healthy Data Platform as a Service, Enterprise-Level Digital Certificate and Cryptographic Key Management, Oxford University to Reduce Hospital Attendance, Healthcare Costs and Improve Tests’ Results</td>
<td align="center">Samsung PaySense Pearson Amazon Alexa</td>
<td align="center"></td>
</tr>
<tr>
<td>Version</td>
<td align="center">Version: 4.0.5 (June 2020)</td>
<td align="center">3.0.28 (Feb 2020)</td>
<td align="center">3.3.11 (June 28, 2018)</td>
<td align="center">1.0.1.0.200237.0 (September 2018)</td>
<td align="center">7.0.0 (April 2020)</td>
</tr>
<tr>
<td>License</td>
<td align="center">GPLv3 Community Edition, commercial &amp; AGPLv3</td>
<td align="center">Community Edition is Apache 2, Enterprise Edition is commercial</td>
<td align="center">Free Apache 2, Proprietary</td>
<td align="center">Proprietary</td>
<td align="center">Proprietary, clients: Eclipse Public License v1</td>
</tr>
<tr>
<td>Release date</td>
<td align="center">2007</td>
<td align="center">September 3rd, 2013</td>
<td align="center">2011</td>
<td align="center">May 30, 2018</td>
<td align="center">March 4, 2019</td>
</tr>
<tr>
<td>Protocol</td>
<td align="center">binary Bolt Protocol</td>
<td align="center">Binary protocol</td>
<td align="center">Async binary protocol</td>
<td align="center">HTTP/Rest, SPARQL 1.1 and RDF 1.1</td>
<td align="center">HTTP</td>
</tr>
<tr>
<td>Data presentation</td>
<td align="center">Cypher queries</td>
<td align="center">JSON format, abbreviated syntax, sql-92 syntax</td>
<td align="center">resemble the JSON format</td>
<td align="center">OSGP index</td>
<td align="center">JSON-LD</td>
</tr>
<tr>
<td>Laguages</td>
<td align="center">Java, .NET, JavaScript, Python, Go, Ruby, PHP, R, Erlang/Elixir, C/C++, Clojure, Perl, Haskel</td>
<td align="center">Java</td>
<td align="center">C++, JavaScript, .NET, Java, Python, Node.js, PHP, Scala, Go, Ruby, Elixi</td>
<td align="center">Not disclosed</td>
<td align="center">C#, C, Common Lisp, Java, Python</td>
</tr>
<tr>
<td>Platforms</td>
<td align="center">Cross-platform</td>
<td align="center">cross-platform, java platform</td>
<td align="center"></td>
<td align="center"></td>
<td align="center">cross-platform</td>
</tr>
<tr>
<td>Creator</td>
<td align="center">Neo Technology</td>
<td align="center">Luca Garulli</td>
<td align="center">Michael Hackstein</td>
<td align="center">Amazon</td>
<td align="center">Franz Inc.</td>
</tr>
<tr>
<td>Website</td>
<td align="center"><a href="https://neo4j.comWeb">https://neo4j.comWeb</a></td>
<td align="center"><a href="https://orientdb.comWeb">https://orientdb.comWeb</a></td>
<td align="center"><a href="https://www.arangodb.com/">https://www.arangodb.com/</a></td>
<td align="center"><a href="https://aws.amazon.com/neptune">https://aws.amazon.com/neptune</a></td>
<td align="center"><a href="https://allegrograph.com/">https://allegrograph.com/</a></td>
</tr>
</tbody>
</table><h2 id="document-oriented">Document-oriented</h2>
<p><em>Document-oriented</em> databases store their data in the form of <em>documents</em>. But what are <em>documents</em>? According to Mark Drake (2019):</p>
<blockquote>
<p>“<em>Document-oriented databases</em>, or <em>document stores</em>, are NoSQL databases that store data in the form of documents. Document stores are a type of <a href="https://web.archive.org/web/20190813163612/https://www.digitalocean.com/community/tutorials/a-comparison-of-nosql-database-management-systems-and-models#key-value-databases">key-value store</a>: each document has a unique identifier — its key — and the document itself serves as the value."</p>
</blockquote>
<p>It’s something in the form:<br>
<img src="https://miro.medium.com/max/1532/1*k663iOSw0Kj_4ctQjwrLcQ.png" alt="document_example"><br>
<a href="https://miro.medium.com/max/1532/1*k663iOSw0Kj_4ctQjwrLcQ.png">document form example link</a></p>
<p>Or in the form:<br>
<img src="https://www.researchgate.net/profile/Tok_Ling/publication/220787904/figure/fig1/AS:669041488306196@1536523329820/Sample-bibliography-XML-document.png" alt="XML_example"><br>
<a href="https://www.researchgate.net/profile/Tok_Ling/publication/220787904/figure/fig1/AS:669041488306196@1536523329820/Sample-bibliography-XML-document.png">XML form example link</a></p>
<h3 id="document-features">Document features</h3>
<ul>
<li>
<p>A document is a roughly application of an <em>object</em> in programming and all its features - such as many optional fields.</p>
</li>
<li>
<p>They aren’t required to follow a standard schema</p>
</li>
<li>
<p>As you can see, documents encapsulate data in some standard forms of encoding such as <code>JSON</code>, <code>BSON</code>, <code>XML</code> and <code>YAML</code> to mention a few.</p>
</li>
<li>
<p>You can nest documents into other documents.</p>
</li>
</ul>
<h3 id="addresing-documents">Addresing documents</h3>
<p>Documents are addressed in the database via a <em>unique key</em> that represents that document, i.e. an unique  <code>ID</code> field for each document, typically a <code>string</code>, a <code>URI</code>, or a <code>path</code>.</p>
<h3 id="organization">Organization</h3>
<p>We can organize our documents in different ways or implementations, for example:</p>
<ul>
<li>
<p>Collections: a group of documents that are stored in a collection is similar to a group of tables inside a relational database.</p>
</li>
<li>
<p>Tags and non-visible metadata: additional data outside the document content, for example comments.</p>
</li>
<li>
<p>Directory hierarchies: documents having a tree structure, based on a path or URI</p>
</li>
</ul>
<h3 id="api-–-query-language">API – Query language</h3>
<p><em>Document-oriented</em>  often come with an <em>API</em> or <em>Query language</em> that allows users to retrieve documents based on the metadata they contain.</p>
<h3 id="applications-1">Applications</h3>
<ul>
<li>
<p>Applications that need to manage a large variety of objects that differ in structure</p>
</li>
<li>
<p>Large product catalogs in e-commerce, customer profiles, content management applications</p>
</li>
</ul>
<h3 id="limitations-1">Limitations</h3>
<ul>
<li>
<p>No standard query syntax</p>
</li>
<li>
<p>Query performance not linearly  scalable</p>
</li>
<li>
<p>Join queries across collections not efficient</p>
</li>
</ul>
<h3 id="popular-open-source-document-oriented-databases">Popular open-source document-oriented databases</h3>

<table>
<thead>
<tr>
<th>Database</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="https://www.mongodb.com/">MongoDB</a></td>
<td>A general purpose, distirbuted document store, MongoDB is <a href="https://db-engines.com/en/ranking/document+store">the world’s most widely used document-oriented database</a>.</td>
</tr>
<tr>
<td><a href="https://www.couchbase.com/">Couchbase</a></td>
<td>Originally known as Membase, a JSON-based, Memcached-compatible document-based store. A multi-model database, Couchbase can also function as a key-value store.</td>
</tr>
<tr>
<td><a href="https://couchdb.apache.org/">Apache CouchDB</a></td>
<td>A project of the Apache Software Foundation, CouchDB stores data as JSON documents and uses JavaScript as its query language.</td>
</tr>
</tbody>
</table><h3 id="comparison-matrix-between-document-oriented-databases">Comparison matrix between document-oriented databases</h3>

<table>
<thead>
<tr>
<th>Name</th>
<th>ArangoDB</th>
<th>CouchDB</th>
<th>DocumentDB</th>
<th>MongoDB</th>
<th>Cosmos DB</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Description</strong></td>
<td>The database system supports document store as well as key/value and graph  data models with one database core and a unified query language AQL (ArangoDB Query Language).</td>
<td>JSON over REST/HTTP with Multi-Version Concurrency Control and limited ACID properties. Uses map and reduce for views and queries.</td>
<td>Fully managed MongoDB v3.6-compatible database service</td>
<td>Document database with replication and sharding, BSON store (binary format JSON).</td>
<td>Platform-as-a-Service offering, part of the Microsoft Azure platform. Builds upon and extends the earlier Azure DocumentDB.</td>
</tr>
<tr>
<td><strong>Main focus</strong></td>
<td>Natively store data for graph, document and search needs.</td>
<td>For accumulating, occasionally changing data, on which pre-defined queries are to be run. Places where versioning is important.</td>
<td>MongoDB compatible, content and catalog management,  mobile and web applications</td>
<td>Retains some friendly properties of SQL. (Query, index)</td>
<td>for modern app development with guaranteed single-digit millisecond response times and 99.999-percent availability backed by SLAs, automatic and instant scalability, and open source APIs for MongoDB and Cassandra.</td>
</tr>
<tr>
<td><strong>Publisher</strong></td>
<td>ArangoDB</td>
<td>Apache Software Foundation</td>
<td>Amazon Web Services</td>
<td>MongoDB, Inc</td>
<td>Microsoft</td>
</tr>
<tr>
<td><strong>License</strong></td>
<td>Apache License 2.0</td>
<td>Apache License</td>
<td>Proprietary online service</td>
<td>Server Side Public License for the DBMS, Apache 2 License for the client drivers</td>
<td>Proprietary</td>
</tr>
<tr>
<td><strong>Query language</strong></td>
<td>AQL (ArangoDB Query Language) is the SQL-like query language</td>
<td>HTTP</td>
<td>SQL (Structured Query Language) over hierarchical JSON documents.</td>
<td>MongoDB supports a rich query language to support read and write operations (CRUD)</td>
<td>Azure Cosmos DB SQL API accounts support querying items using Structured Query Language (SQL) as a JSON query language.</td>
</tr>
<tr>
<td><strong>Languages supported</strong></td>
<td>C, .NET, Java, Python, Node.js, PHP, Scala, Go, Ruby, Elixir</td>
<td>Any language that can make HTTP requests</td>
<td>various, REST</td>
<td>C, C++, C#, Java, Perl, PHP, Python, Go, Node.js, Ruby, Rust,[15] Scala</td>
<td>.NET, Java, Python, Node.js, JavaScript, SQL</td>
</tr>
<tr>
<td><strong>RESTful API</strong></td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
</tr>
<tr>
<td><strong>Release date</strong></td>
<td>2011</td>
<td>2005</td>
<td>2019</td>
<td>2009</td>
<td>2010</td>
</tr>
<tr>
<td><strong>Pricing</strong></td>
<td>Open-source</td>
<td>Open-source</td>
<td>Pay for what you use, there are no up-front costs, and there is no minimum fee.</td>
<td>Free download or Pay per instance + Service (MongoLab)</td>
<td>Azure Cosmos DB bills for provisioned throughput and consumed storage by the hour.</td>
</tr>
<tr>
<td><strong>Protocol</strong></td>
<td>HTTP</td>
<td>HTTP/REST</td>
<td>DocumentDB emulates a subset of the MongoDB 3.6 protocol</td>
<td>BSON (Binary)</td>
<td>Cassandra, MongoDB, Gremlin, and Azure Tables Storage.</td>
</tr>
<tr>
<td><strong>Projects using it</strong></td>
<td>Cisco, Opentext, Kabbage, Mentor, Barclays</td>
<td>Ubuntu, Meebo, BBC</td>
<td>Finra, Freshop, CapitalOne</td>
<td>Ebay, Adobe, SEGA, Google</td>
<td>Coca-Cola, Symantec, and Citrix.</td>
</tr>
<tr>
<td><strong>Website</strong></td>
<td><a href="https://www.arangodb.com/">https://www.arangodb.com/</a></td>
<td><a href="https://couchdb.apache.org/">https://couchdb.apache.org/</a></td>
<td><a href="https://aws.amazon.com/en/documentdb/">https://aws.amazon.com/en/documentdb/</a></td>
<td><a href="https://www.mongodb.com/">https://www.mongodb.com/</a></td>
<td><a href="https://azure.microsoft.com/es-mx/services/cosmos-db/">https://azure.microsoft.com/es-mx/services/cosmos-db/</a></td>
</tr>
</tbody>
</table><h2 id="references">References</h2>
<ul>
<li>1&amp;1 IONOS Inc. (2020, 4 mayo). <a href="https://www.ionos.com/digitalguide/hosting/technical-matters/in-memory-databases/">In-memory databases</a>. Retrieved June 9, 2020.</li>
<li>Raima. (November 19, 2020). <a href="https://raima.com/in-memory-database/">In-Memory Database</a>. Retrieved June 8, 2020.</li>
<li>OmniSci. (2019). <a href="https://www.omnisci.com/technical-glossary/in-memory-database">What is an In-Memory Database? Definition and FAQs | OmniSci</a>. Retrieved June 8, 2020.</li>
<li>Amazon Web Services. (2020). <a href="https://aws.amazon.com/nosql/in-memory/">What Is an In-Memory Database?</a>. Retrieved June 8, 2020.</li>
<li>Rouse, M. (August 3, 2012). <a href="https://whatis.techtarget.com/definition/in-memory-database">In-memory database</a>. Retrieved June 8, 2020.</li>
<li>Bjoor, A. (n.d.) <a href="https://www.accionlabs.com/articles/2018/4/9/choosing-a-nosql-database-technology-comparison-matrix">choosing-a-nosql-database</a>. Retrieved June 8, 2020.</li>
<li>Merkl, B. (July 12th, 2018) <a href="https://neo4j.com/blog/why-graph-databases-are-the-future/">Graph Databases for Begi treeue</a>. Retrieved June 8, 2020.</li>
<li>Amazon Web Service (n.d.)<a href="https://aws.amazon.com/nosql/graph/">What Is a Graph Database?</a>.  Retrieved June 8, 2020.</li>
<li>Wikipedia (n.d.) <a href="https://en.m.wikipedia.org/wiki/Graph_database">Graph Databases</a>. Retrieved June 13, 2020.</li>
<li>ArangoDB (n.d.) <a href="https://www.arangodb.com/docs/stable/aql/examples-create-test-data.html">Query Example</a>. Retrieved June 13, 2020.</li>
<li>ArangoDB (n.d.) <a href="https://www.arangodb.com/subscriptions/">Susbscriptions</a>. Retrieved June 13, 2020.</li>
<li>ArangoDB (n.d.) <a href="https://www.arangodb.com/why-arangodb/case-studies/">Case studies</a>. Retrieved June 13, 2020.</li>
<li>Neo4j (n.d.) <a href="https://neo4j.com/graphgist/advanced-query-tuning-example">Query Example</a>. Retrieved June 13, 2020.</li>
<li>Neo4j (n.d.) <a href="https://neo4j.com/blog/global-graphhack-projects-help-us-pick-winners/">Projects</a>. Retrieved June 13, 2020.</li>
<li>OrientDB (n.d) <a href="https://orientdb.com/docs/last/SQL-Query.html">Query Example</a>. Retrieved June 14, 2020.</li>
<li>G2 (n.d) <a href="https://www.g2.com/products/orientdb/pricing">OrientDB Pricing</a>. Retrieved June 14, 2020.</li>
<li>OrientDB (n.d.) <a href="https://orientdb.com/releases/page/9/">Releases</a>. Retrieved June 14, 2020.</li>
<li>OrientDB (n.d.) <a href="https://orientdb.org/docs//2.0/orientdb.wiki/SQL-Insert.html">Formats</a>. Retrieved June 14, 2020.</li>
<li>Amazon (n.d.) <a href="https://docs.aws.amazon.com/neptune/latest/userguide/get-started-graph-gremlin.html">Gremlin query example of amazon neptune</a>. Retrieved June 14, 2020.</li>
<li>Amazon (n.d.) <a href="https://aws.amazon.com/neptune/pricing/">Pricing</a>. Retrieved June 14, 2020.</li>
<li>Amazon (n.d.) <a href="https://aws.amazon.com/neptune/">Collaborations</a>. Retrieved June 14, 2020.</li>
<li>Amazon (n.d.) <a href="https://docs.aws.amazon.com/neptune/latest/userguide/feature-overview-data-model.html">Format</a>. Retrieved June 14, 2020.</li>
<li>AllegroDB (n.d.) <a href="https://allegrograph.com/allegrograph-editions/">Editions/Pricing</a>. Retrieved June 14, 2020.</li>
<li>Franz (n.d.) <a href="https://franz.com/agraph/support/documentation/current/http-protocol.html">Allegro DB Protocol</a>. Retrieved June 14, 2020.</li>
<li>AllegroDB (n.d.) <a href="https://allegrograph.com/press_room/allegrograph-6-5-marks-first-multi-model-semantic-graph-and-document-database-via-json-and-json-ld/">Format</a>. Retrieved June 14, 2020.</li>
<li>Drake, M. (August 9, 2019). <a href="%5Bhttps://www.digitalocean.com/community/tutorials/a-comparison-of-nosql-database-management-systems-and-models#key-value-databases%5D(https://www.digitalocean.com/community/tutorials/a-comparison-of-nosql-database-management-systems-and-models#key-value-databases)">A Comparison of NoSQL Database Management Systems and Models</a> at <a href="https://www.digitalocean.com/">DigitalOcean</a> . Retrieved June 8, 2020.</li>
<li>Wikipedia: <a href="%5Bhttps://en.wikipedia.org/wiki/NoSQL#Document_store%5D(https://en.wikipedia.org/wiki/NoSQL#Document_store)">Document-oriented database</a>. Retrieved June 8, 2020.</li>
<li>Wikipedia: <a href="https://en.wikipedia.org/wiki/Document-oriented_database#Implementations">Document-oriented implementations</a>.  Retrieved June 14, 2020.</li>
<li>ArangoDB (n.d.) <a href="https://www.arangodb.com/">ArangoDB features</a>. Retrieved June 14, 2020.</li>
<li>Apache (n.d.) <a href="https://couchdb.apache.org/">CouchDB</a>. Retrieved June 14, 2020</li>
<li>Amazon Web Services (n.d.) <a href="https://aws.amazon.com/en/documentdb/">DocumentDB</a>. Retrieved June 14, 2020.</li>
<li>MongoDB Inc. (n.d.) <a href="https://www.mongodb.com/">MongoDB</a>. Retrieved June 14, 2020.</li>
<li>Microsoft (n.d.) <a href="https://azure.microsoft.com/es-mx/services/cosmos-db/">Azure CosmosDB</a>. Retrieved June 14, 2020.</li>
</ul>

    </div>
  </div>
</body>

</html>
