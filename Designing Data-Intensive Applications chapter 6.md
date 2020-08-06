---


---

<h2 id="designing-data-intensive-applications-chapter-6">Designing Data-Intensive Applications chapter 6</h2>
<h3 id="what-is-partitioning">1.-   What is partitioning?</h3>
<p>Partitions are defined in such a way that each piece of data (each record, row, or document) belongs to exactly one partition. There are various ways of achieving this. In effect, each partition is a small database of its own, although the database may support operations that touch multiple partitions at the same time.</p>
<h3 id="what-are-the-two-ways-to-apply-a-partition">2.- What are the two ways to apply a partition?</h3>
<ul>
<li>Key range partitioning: where keys are sorted, and a partition owns all the keys from some minimum up to some maximum. Sorting has the advantage that efficient range queries are possible, but there is a risk of hot spots if the application often accesses keys that are close together in the sorted order.</li>
<li>Hash partitioning: where a hash function is applied to each key, and a partition owns a range of hashes. This method destroys the ordering of keys, making range queries inefficient, but may distribute load more evenly.</li>
</ul>
<h3 id="how-can-we-avoid-partition-with-disproportionately-high-load">3.- How can we avoid partition with disproportionately high load?</h3>
<p>Assign records to nodes randomly. That would distribute the data quite evenly across the nodes.But it’s not the best way, thus let’s assume for now that you have a simple key-value data model, in which you always access a record by its primary key. For example, in an old-fashioned paper encyclopedia, you look up an entry by its title; since all the entries are alphabetically sorted by title, you can quickly find the one you’re looking for.</p>
<h3 id="why-do-we-combine-partition-with-replication">4.- Why do we combine partition with replication?</h3>
<p>Because we can copy for each partition that is stored in multiple nodes. This means that, even though each record belongs to exactly one partition, it may still be stored on several different nodes for fault tolerance.</p>
<h3 id="what-is-skewness-in-partitioning">5.- What is skewness in partitioning?</h3>
<p>When the partitioning is unfair, so that some partitions have more data or queries than others, we call it skewed. The presence of skew makes partitioning much less effective.<br>
In an extreme case, all the load could end up on one partition, so 9 out of 10 nodes are idle and your bottleneck is the single busy node. A partition with disproportionately high load is called a <em>hot spot</em>.</p>
<h3 id="many-distributed-datastores-use-a-hash-function-to-determine-the-partition-for-a-given-key-why-does-this-happen">6.- Many distributed datastores use a hash function to determine the partition for a given key, why does this happen?</h3>
<p>Because of the risk of skew and hot spots.</p>
<h3 id="describe-consistent-hashing">7.- Describe consistent hashing</h3>
<p>It’s a way of evenly distributing load across an internet-wide system of caches such as a content delivery network (CDN). It uses randomly chosen partition boundaries to avoid the need for central control or distributed consensus.</p>
<h3 id="name-the-primary-problem-of-using-secondary-indexes">8.- Name the primary problem of using secondary indexes</h3>
<p>They don’t map neatly to partitions.  There are two main approaches to partitioning a database with secondary indexes: document-based partitioning and term-based partitioning.</p>
<h3 id="what-are-the-two-ways-of-partitioning-secondary-indexes">9.- What are the two ways of partitioning secondary indexes?</h3>
<p>Document-partitioned indexes (local indexes) and term-partitioned indexes (global indexes).</p>
<h3 id="what-is-rebalancing">10.- What is rebalancing?</h3>
<p>The process of moving load from one node in the cluster to another is called rebalancing.<br>
And is expected to meet some minimum requirements:</p>
<ul>
<li>For the load (data storage, read and write requests) to be shared fairly between the nodes in the cluster.</li>
<li>While rebalancing is happening, the database should continue accepting reads and writes.</li>
<li>No more data than necessary should be moved between nodes, to make rebalancing fast and to minimize the network and disk I/O load.</li>
</ul>

