---


---

<h2 id="designing-data-intensive-applications-7">Designing Data-Intensive Applications 7</h2>
<h3 id="what-is-a-transaction">1.- What is a transaction?</h3>
<p>Transaction is a way for an application to group several reads and writes together into a logical unit. Transactions are not a law of nature; they were created with a purpose, namely to simplify the programming model for applications accessing a database.</p>
<h3 id="why-transactions-are-useful">2.- Why transactions are useful?</h3>
<p>By using transactions, the application is free to ignore certain potential error scenarios and concurrency issues, because the database takes care ofthem instead (we call these safety guarantees).</p>
<h3 id="what-does-acid-stands-for-and-describe-each-concept.">3.- What does ACID stands for and describe each concept.</h3>
<ul>
<li><strong>Atomicity:</strong> Transactions are all or nothing</li>
<li><strong>Consistency:</strong> Only valid data is saved</li>
<li><strong>Isolation:</strong> Transactions do not affect each other</li>
<li><strong>Durability:</strong> Written data will no be lost</li>
</ul>
<h3 id="what-is-the-main-idea-behind-applying-acid">4.- What is the main idea behind applying ACID?</h3>
<p>The idea of ACID consistency is that you have certain statements about your data(invariants) that must always be true</p>
<h3 id="the-contrary-of-acid-is...">5.- The contrary of ACID is…</h3>
<p>BASE, which stands for Basically Available, Soft state and Eventual consistency.</p>
<h3 id="what-is-atomicity">6.- What is atomicity?</h3>
<p>Atomic refers to something that cannot be broken down into smaller parts.The word means similar but subtly different things in different branches of computing. For example, in multi-threaded programming, if one thread executes an atomicoperation, that means there is no way that another thread could see the half-finishedresult of the operation.</p>
<h3 id="whats-the-most-basic-level-of-transaction-isolation">7.- What’s the most basic level of transaction isolation?</h3>
<p>Read committed</p>
<h3 id="what-is-isolation">8.- What is isolation?</h3>
<p>The idea is that each transaction reads from a consistent snapshot of the database—that is, the trans‐ action sees all the data that was committed in the database at the start of the transaction. Even if the data is subsequently changed by another transaction, each transaction sees only the old data from that particular point in time.</p>
<h3 id="describe-what-is-hinted-handoff">9.- Describe what is hinted handoff</h3>
<p>Once the network interruption is fixed, any writes that one node temporarily accepted on behalf of another node are sent to the appropriate “home” nodes.</p>
<h3 id="how-can-we-prevent-concurrency-problems">10.- How can we prevent concurrency problems?</h3>
<p>By removing the concurrency entirely: to execute only one transaction at a time, in serial order, on a single thread. By doing so, we completely sidestep the problem of detecting and preventing conflicts between transactions: the resulting isolation is by definition serializable.</p>

