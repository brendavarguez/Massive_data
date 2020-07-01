---


---

<h4 id="before-sql-which-were-the-other-popular-alternatives-for-data-storage">1.- Before SQL, which were the other popular alternatives for data storage?</h4>
<p>Network model and hierarchical model.</p>
<h4 id="mention-some-of-the-firsts-use-cases-of-relational-databases">2.- Mention some of the firsts use cases of relational databases:</h4>
<p>Among transaction processing some tasks included baking transactions, airline reservations and stock-kee ping in warehouses. In terms of batch processing customer invoicing, payroll and reporting were the main applications.</p>
<h4 id="lets-suppose-your-database-is-not-able-to-perform-join-operations.-how-would-you-solve-this">3.- Let’s suppose your database is not able to perform join operations. How would you solve this?</h4>
<p>Unfortunately, in this case it is necessary to emulate joins by making multiple queries to the database.</p>
<h4 id="what-were-the-main-reasons-that-led-to-the-creation-of-nosql-databases">4.- What were the main reasons that led to the creation of NoSql databases?</h4>
<ul>
<li>A need for greater scalability including very large datasets or very high write throughput.</li>
<li>Developers were not happy with restrictiveness of relational schemas.</li>
<li>Specialized query operations that are not well supported by the relational model.</li>
<li>The preference for free and open source software</li>
</ul>
<h4 id="in-the-document-model-it-is-said-that-the-data-presentation-leads-to-locality-advantage-in-comparison-with-relational-model-why">5.- In the document model it is said that the data presentation leads to locality advantage in comparison with relational model, why?</h4>
<p>Let’s imagine that your database stores information about users and different information is stored in different tables. If for some reason it is necessary to access to the entire document or entire information about users, then in a relational database you must perform multiple queries since the data is split across multiple table  which often leads to great time cost while in a document oriented database you only need to access to a single document to have all the information,</p>
<h4 id="does-locality-advantage-always-applies">6.- Does locality advantage always applies?</h4>
<p>No, it only works when large parts of the document at the same time are required because document oriented databases often needs to load the entire document, even tough you only need parts of it. This can be wasteful in term of time and memory on large documents.</p>
<h4 id="what-is-an-advantage-of-assigning-ids-to-each-table-in-a-database">7.- What is an advantage of assigning IDs to each table in a database?</h4>
<p>There are some data that is important to humans and, at the same time, may be subject to change however this is not the case for IDs. People doesn’t care that much about IDs and for that reason it is not likely to be changed.</p>
<h4 id="how-document-oriented-database-manage-to-handle-one-to-many--relationships">8.- How document oriented database manage to handle <em>one-to-many</em>  relationships?</h4>
<p>By nesting records instead of saving each one of them in different tables. As you may see in the example above, the field tags and ratings are an example of this. This is how a document in Mongodb, a document oriented database, looks like.</p>
<pre><code>{
    "name": "keyboard",
    "decription": "logitech keyboard",
    "tags": ["computers", "gaming"],
    "quantity": 3,
    "created_at": new Date(),
    "ratings" : {
            "quality" : 10,
            "strength" : 9
    }
}

</code></pre>

