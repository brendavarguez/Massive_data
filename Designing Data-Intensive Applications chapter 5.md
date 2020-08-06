---


---

<h2 id="designing-data-intensive-applications-chapter-5">Designing Data-Intensive Applications chapter 5</h2>
<h3 id="what-is-replication">1.- What is replication?</h3>
<p>Replication allows to keep a copy of your data on multiple machines that are connected via a network.</p>
<h3 id="what-is-the-difference-between-replication-and-partitioning">2.- What is the difference between <em>replication</em> and <em>partitioning</em>?</h3>
<p>Replication allow us to keep an exact copy of the same data in different locations while partitioning will split a whole dataset into smaller subsets (partitions).</p>
<h3 id="why-to-replicate-your-data-instead-of-doing-partitions">3.- Why to replicate your data instead of doing partitions?</h3>
<p>Because an important advantage of replication is that if a certain location is unavailable, our entire data can still be accessed from different locations.</p>
<h3 id="what-is-the-difference-between-synchronous-and-asynchronous-replication">4.- What is the difference between synchronous and asynchronous replication?</h3>
<p>The difference between synchronous and asynchronous replication is that in synchronous replication the leader waits until a follower has confirmed that it has received the write before reporting success to the user and before making the write visible to other clients; while in asynchronous replication the leader does not wait for a response from the follower after sending a message.</p>
<h3 id="mention-an-scenario-where-multi-leader-replication-can-be-implemented">5.- Mention an scenario where multi-leader replication can be implemented?</h3>
<p>Imagine you are working in a document with your colleges. Each person who has permissions the correct permission (such as read and write) can perform changes in the document. However, these changes are only applied to their local replica, but asynchronously replicated to the server and any other users who are editing the same document.</p>
<h3 id="what-is-failover">6.- What is failover?</h3>
<p>After the failure of a leader, one of the followers needs to be promoted to be the new leader, clients need to be reconfigured to send their writes to the new leader, and the other followers need to start consuming data changes from the new leader.</p>

