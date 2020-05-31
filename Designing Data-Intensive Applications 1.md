---


---

<h2 id="designing-data-intensive-applications-1">Designing Data-Intensive Applications 1</h2>
<h4 id="chapter-1">Chapter 1</h4>
<h5 id="when-talking-about-database-systems-developers-when-is-it-correct-to-call-someone-a-data-system-designer-instead-of-just-application-developer">1. - When talking about database systems developers, when is it correct to call someone a data system designer instead of just application developer?</h5>
<p>When you combine several tools in order to provide a service such as the service’s interface or application programming interface (API), which usually hides those implementation details from clients.</p>
<h5 id="mention-some-factors-that-influence-the-design-of-a-data-system.">2. - Mention some factors that influence the design of a data system.</h5>
<ul>
<li>Skills and experience of the people involved.</li>
<li>Legacy system dependencies.</li>
<li>The timescale for delivery.</li>
<li>Your organization’s tolerance of different kinds of risk.</li>
</ul>
<h5 id="when-can-be-said-that-a-system-is-reliable">3. - When can be said that a system is reliable?</h5>
<p>If the system continue working correctly even if it faces some errors such as hardware or software faults, and even human error, then it can be said that the system is reliable.</p>
<h5 id="what-is-the-difference-between-fault-and-failure">4. - What is the difference between <em>fault</em> and <em>failure</em>?</h5>
<p>A <em>fault</em> is usually defined as one component of the system deviating from its purpose, whereas a <em>failure</em> is when the whole system stops providing the required service to the user.</p>
<h5 id="what-was-the-main-reason-because-more-applications-have-begun-using-larger-numbers-of-machines">5. - What was the main reason because more applications have begun using larger numbers of machines?</h5>
<p>Because data volumes and applications’ computing demands have increased.</p>
<h5 id="why-a-systematic-error-within-a-system-is-harder-to-anticipate">6. -Why a systematic error within a system is harder to anticipate?</h5>
<p>Due to they are correlated across nodes they tend to cause many more system failures than uncorrelated hardware faults.</p>
<h5 id="how-can-we-make-our-systems-to-be-reliable">7.- How can we make our systems to be reliable?</h5>
<ul>
<li>
<p>Design systems in a way that minimizes opportunities for error.</p>
</li>
<li>
<p>Test thoroughly at all levels, from unit tests to whole-system integration tests and manual tests.</p>
</li>
<li>
<p>Allow quick and easy recovery from human errors, to minimize the impact in the case of a failure.</p>
</li>
<li>
<p>Set up detailed and clear monitoring, such as performance metrics and error rates.</p>
</li>
<li>
<p>Implement good management practices and training.</p>
</li>
</ul>
<h5 id="why-reliable-systems-are-important">8.- Why reliable systems are important?</h5>
<p>Because not having a reliable system can cause a loss in productivity, which can lead to have huge costs in terms of lost revenue and damage to reputation.</p>
<h5 id="if-a-system-is-working-reliably-today-can-we-trust-that-it-will-work-reliably-in-the-future">9.- If a system is working reliably today, can we trust that it will work reliably in the future?</h5>
<p>No because users needs may change/increase over time, and one common reason for degradation is increased load.</p>
<h4 id="extra-questions">Extra questions</h4>
<h5 id="what-is-chaos-monkey">1.- What is Chaos Monkey?</h5>
<p>Is a tool invented in 2011 by Netflix to test the resilience of its IT infrastructure.</p>
<h5 id="how-does-chaos-monkey-works">2.- How does Chaos Monkey works?</h5>
<p>It works by intentionally disabling computers in Netflix’s production network to test how remaining systems respond to the outage.</p>

