<div class="relative flex w-full min-w-[min(450px,80vw)] snap-center flex-col gap-1 rounded-2xl border border-token-main-surface-tertiary bg-white p-5 text-left dark:bg-gray-700"><div class="flex gap-4 items-center mb-1"><div><div class="pt-0"><div class="gizmo-bot-avatar flex h-8 w-8 items-center justify-center overflow-hidden rounded-full"><div class="relative p-1 rounded-sm flex items-center justify-center bg-token-main-surface-primary text-token-text-primary h-8 w-8"></div></div></div></div></div><div class="flex max-w-full flex-col"><div data-message-author-role="assistant" data-message-id="9d6449fa-416c-4189-a029-d522461a1005" dir="auto" class="min-h-8 text-message flex w-full flex-col items-end gap-2 whitespace-normal break-words [.text-message+&amp;]:mt-5"><div class="flex w-full flex-col gap-1 empty:hidden first:pt-[3px]"><div class="markdown prose w-full break-words dark:prose-invert dark"><h3>Test-Driven Development (TDD) vs Behavior-Driven Development (BDD)</h3><p>Both <strong>Test-Driven Development (TDD)</strong> and <strong>Behavior-Driven Development (BDD)</strong> are software development practices focused on writing tests before the actual code is written. However, they differ in terms of <strong>focus</strong>, <strong>process</strong>, and <strong>who writes the tests</strong>. Let’s break them down with an example.</p><hr><h3><strong>Test-Driven Development (TDD)</strong></h3><ul><li><strong>Focus</strong>: TDD focuses on <strong>unit testing</strong> and how the code is implemented. It ensures that the code works as expected, by writing tests for small units (functions or methods).</li><li><strong>Process</strong>:<ol><li>Write a failing test (Red)</li><li>Write just enough code to make the test pass (Green)</li><li>Refactor the code while ensuring tests pass (Refactor)</li></ol></li></ul><h4>TDD Example: Calculator</h4><p>Imagine we are building a calculator that can add two numbers. Here’s how TDD would approach it:</p><ol><li><p><strong>Write a failing test</strong>:</p><div class="overflow-y-auto p-4" dir="ltr"><code class="!whitespace-pre hljs language-python"><span class="hljs-keyword">def</span> <span class="hljs-title function_">test_add_two_numbers</span>():
    <span class="hljs-keyword">assert</span> add(<span class="hljs-number">2</span>, <span class="hljs-number">3</span>) == <span class="hljs-number">5</span>
</code></div></div></pre><p>Here, the <code>add()</code> function doesn’t exist yet, so this test will fail.</p></li><li><p><strong>Write code to pass the test</strong>:</p><pre class="!overflow-visible"><div class="dark bg-gray-950 contain-inline-size rounded-md border-[0.5px] border-token-border-medium relative"><div class="flex items-center text-token-text-secondary bg-token-main-surface-secondary px-4 py-2 text-xs font-sans justify-between rounded-t-md h-9">python</div><div class="sticky top-9 md:top-[5.75rem]"><div class="absolute bottom-0 right-2 flex h-9 items-center"><div class="flex items-center rounded bg-token-main-surface-secondary px-2 font-sans text-xs text-token-text-secondary"><span class="" data-state="closed"><button class="flex gap-1 items-center py-1">
</div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="!whitespace-pre hljs language-python"><span class="hljs-keyword">def</span> <span class="hljs-title function_">add</span>(<span class="hljs-params">a, b</span>):
    <span class="hljs-keyword">return</span> a + b
</code></div></div></pre><p>Now, the test will pass.</p></li><li><p><strong>Refactor</strong> (if necessary):
If the code is simple, no refactor is needed in this case, but in more complex scenarios, this is where you clean up the code.</p></li></ol><hr><h3><strong>Behavior-Driven Development (BDD)</strong></h3><ul><li><strong>Focus</strong>: BDD is more <strong>user-focused</strong> and describes the behavior of the system from the perspective of how the system should work for an end user. BDD uses a more natural language style (usually Gherkin syntax) to express the expected behavior.</li><li><strong>Process</strong>:<ol><li>Write a behavior specification or user story (Given-When-Then)</li><li>Automate the specification with tests</li><li>Implement code to make the tests pass</li></ol></li></ul><h4>BDD Example: Calculator (Adding Two Numbers)</h4><ol><li><p><strong>Write a behavior scenario (Given-When-Then)</strong>:</p><pre class="!overflow-visible">


<div class="dark bg-gray-950 contain-inline-size rounded-md border-[0.5px] border-token-border-medium relative"><div class="flex items-center text-token-text-secondary bg-token-main-surface-secondary px-4 py-2 text-xs font-sans justify-between rounded-t-md h-9">sql</div><div class="sticky top-9 md:top-[5.75rem]"><div class="absolute bottom-0 right-2 flex h-9 items-center"><div class="flex items-center rounded bg-token-main-surface-secondary px-2 font-sans text-xs text-token-text-secondary"><span class="" data-state="closed"><button class="flex gap-1 items-center py-1">
</span></div></div></div>



<div class="overflow-y-auto p-4" dir="ltr"><code class="!whitespace-pre hljs language-sql">Scenario: <span class="hljs-keyword">Add</span> two numbers
  Given I have a calculator
  <span class="hljs-keyword">When</span> I input <span class="hljs-number">2</span> <span class="hljs-keyword">and</span> <span class="hljs-number">3</span>
  <span class="hljs-keyword">Then</span> the <span class="hljs-keyword">result</span> should be <span class="hljs-number">5</span>
</code></div></div></pre></li><li><p><strong>Automate the behavior using BDD tools</strong> (e.g., with Python and <code>pytest-bdd</code> or Cucumber for Java):</p><pre class="!overflow-visible"><div class="dark bg-gray-950 contain-inline-size rounded-md border-[0.5px] border-token-border-medium relative"><div class="flex items-center text-token-text-secondary bg-token-main-surface-secondary px-4 py-2 text-xs font-sans justify-between rounded-t-md h-9">python</div><div class="sticky top-9 md:top-[5.75rem]"><div class="absolute bottom-0 right-2 flex h-9 items-center"><div class="flex items-center rounded bg-token-main-surface-secondary px-2 font-sans text-xs text-token-text-secondary"><span class="" data-state="closed"><button class="flex gap-1 items-center py-1"></span></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="!whitespace-pre hljs language-python"><span class="hljs-keyword">from</span> pytest_bdd <span class="hljs-keyword">import</span> scenario, given, when, then

<span class="hljs-meta">@scenario(<span class="hljs-params"><span class="hljs-string">'calculator.feature'</span>, <span class="hljs-string">'Add two numbers'</span></span>)</span>
<span class="hljs-keyword">def</span> <span class="hljs-title function_">test_add_two_numbers</span>():
    <span class="hljs-keyword">pass</span>

<span class="hljs-meta">@given(<span class="hljs-params"><span class="hljs-string">'I have a calculator'</span></span>)</span>
<span class="hljs-keyword">def</span> <span class="hljs-title function_">calculator</span>():
    <span class="hljs-keyword">return</span> Calculator()

<span class="hljs-meta">@when(<span class="hljs-params"><span class="hljs-string">'I input 2 and 3'</span></span>)</span>
<span class="hljs-keyword">def</span> <span class="hljs-title function_">input_numbers</span>(<span class="hljs-params">calculator</span>):
    calculator.add(<span class="hljs-number">2</span>, <span class="hljs-number">3</span>)

<span class="hljs-meta">@then(<span class="hljs-params"><span class="hljs-string">'the result should be 5'</span></span>)</span>
<span class="hljs-keyword">def</span> <span class="hljs-title function_">result_is_5</span>(<span class="hljs-params">calculator</span>):
    <span class="hljs-keyword">assert</span> calculator.result == <span class="hljs-number">5</span>
</code></div></div></pre></li><li><p><strong>Write the actual implementation</strong>:</p><pre class="!overflow-visible"><div class="dark bg-gray-950 contain-inline-size rounded-md border-[0.5px] border-token-border-medium relative"><div class="flex items-center text-token-text-secondary bg-token-main-surface-secondary px-4 py-2 text-xs font-sans justify-between rounded-t-md h-9">python</div><div class="sticky top-9 md:top-[5.75rem]"><div class="absolute bottom-0 right-2 flex h-9 items-center"><div class="flex items-center rounded bg-token-main-surface-secondary px-2 font-sans text-xs text-token-text-secondary"><span class="" data-state="closed">></span></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="!whitespace-pre hljs language-python"><span class="hljs-keyword">class</span> <span class="hljs-title class_">Calculator</span>:
    <span class="hljs-keyword">def</span> <span class="hljs-title function_">__init__</span>(<span class="hljs-params">self</span>):
        self.result = <span class="hljs-number">0</span>

    <span class="hljs-keyword">def</span> <span class="hljs-title function_">add</span>(<span class="hljs-params">self, a, b</span>):
        self.result = a + b
</code></div></div></pre></li></ol><hr><h3><strong>Key Differences</strong>:</h3><table><thead><tr><th>Aspect</th><th>TDD</th><th>BDD</th></tr></thead><tbody><tr><td><strong>Focus</strong></td><td>How code works (developer-centric)</td><td>How the system behaves (user-centric)</td></tr><tr><td><strong>Language</strong></td><td>Code-focused (e.g., unit tests)</td><td>Human-readable scenarios (Gherkin syntax)</td></tr><tr><td><strong>Process</strong></td><td>Red → Green → Refactor</td><td>Given → When → Then</td></tr><tr><td><strong>Audience</strong></td><td>Primarily developers</td><td>Developers, testers, and business analysts</td></tr><tr><td><strong>Tests Granularity</strong></td><td>Unit tests (small pieces of functionality)</td><td>Acceptance or behavior tests (full features)</td></tr><tr><td><strong>Documentation</strong></td><td>Tests double as technical documentation</td><td>Scenarios serve as requirements and tests</td></tr></tbody></table><hr><h3>Summary</h3><ul><li><strong>TDD</strong> is about writing tests for small units of code to verify the functionality, focusing on the <strong>developer's perspective</strong>.</li><li><strong>BDD</strong> is about describing the <strong>expected behavior</strong> of a system from a <strong>user's perspective</strong>, focusing on collaboration between developers, testers, and non-technical stakeholders.</li></ul></div></div></div></div></div>


Key Differences:
Purpose:

TDD ensures the code functions correctly at a low level (unit tests).
BDD focuses on the system’s behavior as seen by the end user (acceptance tests).
Language:

TDD tests are written by developers in the same language as the code.
BDD uses a more natural language (e.g., Gherkin) to describe tests, making them accessible to non-developers like business analysts.
Scope:

TDD works on the unit level.
BDD works at a higher level (integration or system tests) focusing on end-user behavior.
In short, TDD is about building the software right, whereas BDD is about building the right software.