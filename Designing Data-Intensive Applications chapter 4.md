---


---

<h2 id="designing-data-intensive-applications-chapter-4">Designing Data-Intensive Applications chapter 4</h2>
<h4 id="what-are-some-problems-while-encoding-and-decoding-data-from-one-language-to-another">1.- What are some problems while encoding and decoding data from one language to another?</h4>
<p>The first problem is that when you encode your data in a specific language, for another language it may result difficult to read it. Second, if the decoding process is not  able to instantiate arbitrary classes, then it will be hard to restore data in the same object type.</p>
<h4 id="mention-the-standardized-data-presentation-formats.">2.- Mention the standardized data presentation formats.</h4>
<ul>
<li>JSON</li>
<li>XML</li>
<li>CSV</li>
</ul>
<h4 id="what-are-some-disadvantages-of-these-data-presentation-formats">3.- What are some disadvantages of these data presentation formats?</h4>
<p>CSV and XML are not able to distinguish between numbers and strings of numbers. On the other hand, JSON it is able to make this difference, unfortunately, it doesn’t distinguish integers and floating-point numbers. Another point is that both JSON and XML can easily work with Unicode characters, however, they don’t support binary strings.</p>
<h4 id="mention-some-advantages-of-binary-encodings-based-on-schemas.">4.- Mention some advantages of binary encodings based on schemas.</h4>
<ul>
<li>
<p>They can be much more compact than the various “binary JSON” variants, since they can omit field names from the encoded data.</p>
</li>
<li>
<p>The schema is a valuable form of documentation, and because the schema is required for decoding, you can be sure that it is up to date.</p>
</li>
<li>
<p>Keeping a database of schemas allows you to check forward and backward compatibility of schema changes, before anything is deployed.</p>
</li>
</ul>
<h4 id="give-an-example-where-http-works-as-a-web-service-instead-of-a-transfer-protocol.">5.-Give an example where HTTP works as a web service instead of a transfer protocol.</h4>
<p>A client application running on a user’s device such as a native app on a mobile device, making requests to a service over HTTP which typically go over the public internet.</p>
<h4 id="mention-some-advantages-of-using-a-message-broker-instead-of-rpc-remote-procedure-calls-for-message-passing.">6.- Mention some advantages of using a message broker instead of RPC (remote procedure calls) for message passing.</h4>
<ul>
<li>A message broker is able to act as a buffer if the recipient is unavailable, which will improve system reliability.</li>
<li>It can automatically redeliver messages to a process that has crashed, which will prevent the system of loosing messages.</li>
<li>Message brokers avoids the sender needing to know the IP address and port number of the recipient. This is useful in a cloud deployment where virtual machines often come and go.</li>
<li>Is is possible to send the same message to several recipients.</li>
<li>The communication is one-way, which means that a sender neither expect to receive a reply to its messages nor cares  who consumes them. A good example is <strong>Apache Kafka</strong>.</li>
</ul>
<h4 id="provide-a-brief-explanation-of-how-message-brokers-works.">7.- Provide a brief explanation of how message brokers works.</h4>
<p>A sender shares data to a named topic or a queue, however, it is the broker which makes sure that this data is delivered to one or more consumers of or subscribers to that queue or topic.</p>
<p>A feature of a topic is that it only provides one-way communication. Nevertheless, the good thing about consumers is that they are able to publish messages to another topic or to a reply queue that is consumed by the sender of the original message. However, if consumer republishes messages to another topic, then you may need to be careful to preserve unknown fields.</p>
<h4 id="give-an-example-of-how-message-brokers-are-used.">8.- Give an example of how message brokers are used.</h4>
<p>Let’s talk about a fleet of trucks.</p>
<p><a href="data/fleet.png"></a></p>
<p>Imagine we have a fleet of trucks and each truck reports its GPS position a topic named trucks_gps that contains the position of all trucks (<strong>one</strong> topic for all my trucks).</p>
<p>Each truck will send a message to this topic every 20 seconds and each message will contain truck ID and the truck position (latitude and longitude).</p>
<p><a href="data/fleet.png"></a></p>
<p>Why do we need a broker message for this process? Maybe I want to have consumers of my data such as:</p>
<ul>
<li>Location dashboard for my employees so they can look at the trucking data.</li>
<li>Notification service, when a truck is running out of fuel or a truck has been driving for too long and it seems like the driver should take a break.</li>
</ul>

