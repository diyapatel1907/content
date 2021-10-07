---
title: Pseudo-classes and pseudo-elements
slug: Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements
tags:
  - Beginner
  - CSS
  - Learn
  - Pseudo
  - Pseudo-class
  - Pseudo-element
  - Selectors
---
<p>{{LearnSidebar}}{{PreviousMenuNext("Learn/CSS/Building_blocks/Selectors/Attribute_selectors", "Learn/CSS/Building_blocks/Selectors/Combinators", "Learn/CSS/Building_blocks")}}</p>

<p>The next set of selectors we will look at are referred to as <strong>pseudo-classes</strong> and <strong>pseudo-elements</strong>. There are a large number of these, and they often serve quite specific purposes. Once you know how to use them, you can look at the list to see if there is something which works for the task you are trying to achieve. Once again the relevant MDN page for each selector is helpful in explaining browser support.</p>

<table>
 <tbody>
  <tr>
   <th scope="row">Prerequisites:</th>
   <td>Basic computer literacy, <a href="/en-US/docs/Learn/Getting_started_with_the_web/Installing_basic_software">basic software installed</a>, basic knowledge of <a href="/en-US/docs/Learn/Getting_started_with_the_web/Dealing_with_files">working with files</a>, HTML basics (study <a href="/en-US/docs/Learn/HTML/Introduction_to_HTML">Introduction to HTML</a>), and an idea of how CSS works (study <a href="/en-US/docs/Learn/CSS/First_steps">CSS first steps</a>.)</td>
  </tr>
  <tr>
   <th scope="row">Objective:</th>
   <td>To learn about the pseudo-class and pseudo-element selectors.</td>
  </tr>
 </tbody>
</table>

<h2 id="What_is_a_pseudo-class">What is a pseudo-class?</h2>

<p>A pseudo-class is a selector that selects elements that are in a specific state, e.g. they are the first element of their type, or they are being hovered over by the mouse pointer. They tend to act as if you had applied a class to some part of your document, often helping you cut down on excess classes in your markup, and giving you more flexible, maintainable code.</p>

<p>Pseudo-classes are keywords that start with a colon:</p>

<pre>:<em>pseudo-class-name</em></pre>

<h3 id="Simple_pseudo-class_example">Simple pseudo-class example</h3>

<p>Let's look at a simple example. If we wanted to make the first paragraph in an article larger and bold, we could add a class to that paragraph and then add CSS to that class, as shown in the first example below:</p>

<p>{{EmbedGHLiveSample("css-examples/learn/selectors/first-child.html", '100%', 800)}}</p>

<p>However, this could be annoying to maintain — what if a new paragraph got added to the top of the document? We'd need to move the class over to the new paragraph. Instead of adding the class, we could use the {{cssxref(":first-child")}} pseudo-class selector — this will <em>always</em> target the first child element in the article, and we will no longer need to edit the HTML (this may not always be possible anyway, maybe due to it being generated by a CMS.)</p>

<p>{{EmbedGHLiveSample("css-examples/learn/selectors/first-child2.html", '100%', 700)}}</p>

<p>All pseudo-classes behave in this same kind of way. They target some bit of your document that is in a certain state, behaving as if you had added a class into your HTML. Take a look at some other examples on MDN:</p>

<ul>
 <li><code><a href="/en-US/docs/Web/CSS/:last-child">:last-child</a></code></li>
 <li><code><a href="/en-US/docs/Web/CSS/:only-child">:only-child</a></code></li>
 <li><code><a href="/en-US/docs/Web/CSS/:invalid">:invalid</a></code></li>
</ul>

<div class="notecard note">
<p><strong>Note:</strong> It is valid to write pseudo-classes and elements without any element selector preceding them. In the example above, you could write <code>:first-child</code> and the rule would apply to <em>any</em> element that is the first child of an <code>&lt;article&gt;</code> element, not just a paragraph first child — <code>:first-child</code> is equivalent to <code>*:first-child</code>. However, usually you want more control than that, so you need to be more specific.</p>
</div>

<h3 id="User-action_pseudo_classes">User-action pseudo classes</h3>

<p>Some pseudo-classes only apply when the user interacts with the document in some way. These <strong>user-action</strong> pseudo-classes, sometimes referred to as <strong>dynamic pseudo-classes</strong>, act as if a class had been added to the element when the user interacts with it. Examples include:</p>

<ul>
 <li><code><a href="/en-US/docs/Web/CSS/:hover">:hover</a></code> — mentioned above; this only applies if the user moves their pointer over an element, typically a link.</li>
 <li><code><a href="/en-US/docs/Web/CSS/:focus">:focus</a></code> — only applies if the user focuses the element using keyboard controls.</li>
</ul>

<p>{{EmbedGHLiveSample("css-examples/learn/selectors/hover.html", '100%', 500)}}</p>

<h2 id="What_is_a_pseudo-element">What is a pseudo-element?</h2>

<p>Pseudo-elements behave in a similar way. However, they act as if you had added a whole new HTML element into the markup, rather than applying a class to existing elements. Pseudo-elements start with a double colon <code>::</code>.</p>

<pre><em>::pseudo-element-name</em></pre>

<div class="notecard note">
<p><strong>Note:</strong> Some early pseudo-elements used the single colon syntax, so you may sometimes see this in code or examples. Modern browsers support the early pseudo-elements with single- or double-colon syntax for backwards compatibility.</p>
</div>

<p>For example, if you wanted to select the first line of a paragraph you could wrap it in a <code>&lt;span&gt;</code> element and use an element selector; however, that would fail if the number of words you had wrapped were longer or shorter than the parent element's width. As we tend not to know how many words will fit on a line — as that will change if the screen width or font-size changes — it is impossible to robustly do this by adding HTML.</p>

<p>The <code>::first-line</code> pseudo-element selector will do this for you reliably — if the number of words increases or decreases it will still only select the first line.</p>

<p>{{EmbedGHLiveSample("css-examples/learn/selectors/first-line.html", '100%', 800)}}</p>

<p>It acts as if a <code>&lt;span&gt;</code> was magically wrapped around that first formatted line, and updated each time the line length changed.</p>

<p>You can see that this selects the first line of both paragraphs.</p>

<h2 id="Combining_pseudo-classes_and_pseudo-elements">Combining pseudo-classes and pseudo-elements</h2>

<p>If you wanted to make the first line of the first paragraph bold you could chain the <code>:first-child</code> and <code>::first-line</code> selectors together. Try editing the previous live example so it uses the following CSS. We are saying that we want to select the first line, of the first <code>&lt;p&gt;</code> element, which is inside an <code>&lt;article&gt;</code> element.</p>

<pre class="brush: css">article p:first-child::first-line {
  font-size: 120%;
  font-weight: bold;
}</pre>

<h2 id="Generating_content_with_before_and_after">Generating content with ::before and ::after</h2>

<p>There are a couple of special pseudo-elements, which are used along with the <code><a href="/en-US/docs/Web/CSS/content">content</a></code> property to insert content into your document using CSS.</p>

<p>You could use these to insert a string of text, such as in the live example below. Try changing the text value of the {{cssxref("content")}} property and see it change in the output. You could also change the <code>::before</code> pseudo-element to <code>::after</code> and see the text inserted at the end of the element instead of the beginning.</p>

<p>{{EmbedGHLiveSample("css-examples/learn/selectors/before.html", '100%', 400)}}</p>

<p>Inserting strings of text from CSS isn't really something we do very often on the web however, as that text is inaccessible to some screen readers and might be hard for someone to find and edit in the future.</p>

<p>A more valid use of these pseudo-elements is to insert an icon, for example the little arrow added in the example below, which is a visual indicator that we wouldn't want read out by a screenreader:</p>

<p>{{EmbedGHLiveSample("css-examples/learn/selectors/after-icon.html", '100%', 400)}}</p>

<p>These pseudo-elements are also frequently used to insert an empty string, which can then be styled just like any element on the page.</p>

<p>In this next example, we have added an empty string using the <code>::before</code> pseudo-element. We have set this to <code>display: block</code> in order that we can style it with a width and height. We then use CSS to style it just like any element. You can play around with the CSS and change how it looks and behaves.</p>

<p>{{EmbedGHLiveSample("css-examples/learn/selectors/before-styled.html", '100%', 500)}}</p>

<p>The use of the <code>::before</code> and <code>::after</code> pseudo-elements along with the <code>content</code> property is referred to as "Generated Content" in CSS, and you will often see this technique being used for various tasks. A great example is the site <a href="https://www.cssarrowplease.com/">CSS Arrow Please</a>, which helps you to generate an arrow with CSS. Look at the CSS as you create your arrow and you will see the {{cssxref("::before")}} and {{cssxref("::after")}} pseudo-elements in use. Whenever you see these selectors, look at the {{cssxref("content")}} property to see what is being added to the document.</p>

<h2 id="Reference_section">Reference section</h2>

<p>There are a large number of pseudo-classes and pseudo-elements, and it is useful to have a list to refer to. Below are tables listing them, with links to their reference pages on MDN. Use this as a reference to see the kinds of things that are available for you to target.</p>

<h3 id="Pseudo-classes">Pseudo-classes</h3>

<table class="standard-table no-markdown">
 <thead>
  <tr>
   <th scope="col">Selector</th>
   <th scope="col">Description</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{ Cssxref(":active") }}</td>
   <td>Matches when the user activates (for example clicks on) an element.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":any-link") }}</td>
   <td>Matches both the <code>:link</code> and <code>:visited</code> states of a link.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":blank") }}</td>
   <td>Matches an <a href="/en-US/docs/Web/HTML/Element/input"><code>&lt;input&gt;</code> element</a> whose input value is empty.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":checked") }}</td>
   <td>Matches a radio button or checkbox in the selected state.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":current") }}</td>
   <td>Matches the element, or an ancestor of the element, that is currently being displayed.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":default") }}</td>
   <td>Matches the one or more UI elements that are the default among a set of similar elements.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":dir") }}</td>
   <td>Select an element based on its directionality (value of the HTML <code><a href="/en-US/docs/Web/HTML/Global_attributes/dir">dir</a></code> attribute or CSS <code><a href="/en-US/docs/Web/CSS/direction">direction</a></code> property).</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":disabled") }}</td>
   <td>Matches user interface elements that are in an disabled state.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":empty") }}</td>
   <td>Matches an element that has no children except optionally white space.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":enabled") }}</td>
   <td>Matches user interface elements that are in an enabled state.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":first") }}</td>
   <td>In <a href="/en-US/docs/Web/CSS/Paged_Media">Paged Media</a>, matches the first page.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":first-child") }}</td>
   <td>Matches an element that is first among its siblings.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":first-of-type") }}</td>
   <td>Matches an element which is first of a certain type among its siblings.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":focus") }}</td>
   <td>Matches when an element has focus.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":focus-visible")}}</td>
   <td>Matches when an element has focus and the focus should be visible to the user.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":focus-within") }}</td>
   <td>Matches an element with focus plus an element with a descendent that has focus.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":future") }}</td>
   <td>Matches the elements after the current element.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":hover") }}</td>
   <td>Matches when the user hovers over an element.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":indeterminate") }}</td>
   <td>Matches UI elements whose value is in an indeterminate state, usually <a href="/en-US/docs/Web/HTML/Element/input/checkbox">checkboxes</a>.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":in-range") }}</td>
   <td>Matches an element with a range when its value is in-range.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":invalid") }}</td>
   <td>Matches an element, such as an <code>&lt;input&gt;</code>, in an invalid state.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":lang") }}</td>
   <td>Matches an element based on language (value of the HTML <a href="/en-US/docs/Web/HTML/Global_attributes/lang">lang</a> attribute).</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":last-child") }}</td>
   <td>Matches an element which is last among its siblings.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":last-of-type") }}</td>
   <td>Matches an element of a certain type that is last among its siblings.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":left") }}</td>
   <td>In <a href="/en-US/docs/Web/CSS/CSS_Pages">Paged Media</a>, matches left-hand pages.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":link")}}</td>
   <td>Matches unvisited links.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":local-link")}}</td>
   <td>Matches links pointing to pages that are in the same site as the current document.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":is", ":is()")}}</td>
   <td>Matches any of the selectors in the selector list that is passed in.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":not") }}</td>
   <td>Matches things not matched by selectors that are passed in as a value to this selector.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":nth-child") }}</td>
   <td>Matches elements from a list of siblings — the siblings are matched by a formula of the form <var>an+b</var> (e.g. 2n + 1 would match elements 1, 3, 5, 7, etc. All the odd ones.)</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":nth-of-type") }}</td>
   <td>Matches elements from a list of siblings that are of a certain type (e.g. <code>&lt;p&gt;</code> elements) — the siblings are matched by a formula of the form <var>an+b</var> (e.g. 2n + 1 would match that type of element, numbers 1, 3, 5, 7, etc. All the odd ones.)</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":nth-last-child") }}</td>
   <td>Matches elements from a list of siblings, counting backwards from the end. The siblings are matched by a formula of the form <var>an+b</var> (e.g. 2n + 1 would match the last element in the sequence, then two elements before that, then two elements before that, etc. All the odd ones, counting from the end.)</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":nth-last-of-type") }}</td>
   <td>Matches elements from a list of siblings that are of a certain type (e.g. <code>&lt;p&gt;</code> elements), counting backwards from the end. The siblings are matched by a formula of the form <var>an+b</var> (e.g. 2n + 1 would match the last element of that type in the sequence, then two elements before that, then two elements before that, etc. All the odd ones, counting from the end.)</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":only-child") }}</td>
   <td>Matches an element that has no siblings.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":only-of-type") }}</td>
   <td>Matches an element that is the only one of its type among its siblings.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":optional") }}</td>
   <td>Matches form elements that are not required.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":out-of-range") }}</td>
   <td>Matches an element with a range when its value is out of range.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":past") }}</td>
   <td>Matches the elements before the current element.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":placeholder-shown") }}</td>
   <td>Matches an input element that is showing placeholder text.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":playing") }}</td>
   <td>Matches an element representing an audio, video, or similar resource that is capable of being “played” or “paused”, when that element is “playing”.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":paused") }}</td>
   <td>Matches an element representing an audio, video, or similar resource that is capable of being “played” or “paused”, when that element is “paused”.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":read-only") }}</td>
   <td>Matches an element if it is not user-alterable.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":read-write") }}</td>
   <td>Matches an element if it is user-alterable.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":required") }}</td>
   <td>Matches form elements that are required.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":right") }}</td>
   <td>In <a href="/en-US/docs/Web/CSS/CSS_Pages">Paged Media</a>, matches right-hand pages.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":root") }}</td>
   <td>Matches an element that is the root of the document.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":scope") }}</td>
   <td>Matches any element that is a scope element.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":valid") }}</td>
   <td>Matches an element such as an <code>&lt;input&gt;</code> element, in a valid state.</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":target") }}</td>
   <td>Matches an element if it is the target of the current URL (i.e. if it has an ID matching the current <a href="https://en.wikipedia.org/wiki/Fragment_identifier">URL fragment</a>).</td>
  </tr>
  <tr>
   <td>{{ Cssxref(":visited") }}</td>
   <td>Matches visited links.</td>
  </tr>
 </tbody>
</table>

<h3 id="Pseudo-elements">Pseudo-elements</h3>

<table class="standard-table no-markdown">
 <thead>
  <tr>
   <th scope="col">Selector</th>
   <th scope="col">Description</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{ Cssxref("::after") }}</td>
   <td>Inserts a stylable element appearing after the originating element's actual content, if used with the {{cssxref("content")}} property with a value other than <code>none</code>.</td>
  </tr>
  <tr>
   <td>{{ Cssxref("::before") }}</td>
   <td>Inserts a stylable element appearing before the originating element's actual content, if used with the {{cssxref("content")}} property with a value other than <code>none</code>.</td>
  </tr>
  <tr>
   <td>{{ Cssxref("::first-letter") }}</td>
   <td>Matches the first letter of the element.</td>
  </tr>
  <tr>
   <td>{{ Cssxref("::first-line") }}</td>
   <td>Matches the first line of the containing element.</td>
  </tr>
  <tr>
   <td>{{ Cssxref("::grammar-error") }}</td>
   <td>Matches a portion of the document containing a grammar error as flagged by the browser.</td>
  </tr>
  <tr>
   <td>{{ Cssxref("::marker") }}</td>
   <td>Matches the marker box of a list item, which typically contains a bullet or number.</td>
  </tr>
  <tr>
   <td>{{ Cssxref("::selection") }}</td>
   <td>Matches the portion of the document that has been selected.</td>
  </tr>
  <tr>
   <td>{{ Cssxref("::spelling-error") }}</td>
   <td>Matches a portion of the document containing a spelling error as flagged by the browser.</td>
  </tr>
 </tbody>
</table>

<p>{{PreviousMenuNext("Learn/CSS/Building_blocks/Selectors/Attribute_selectors", "Learn/CSS/Building_blocks/Selectors/Combinators", "Learn/CSS/Building_blocks")}}</p>

<h2 id="In_this_module">In this module</h2>

<ol>
 <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance">Cascade and inheritance</a></li>
 <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Selectors">CSS selectors</a>
  <ul>
   <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Selectors/Type_Class_and_ID_Selectors">Type, class, and ID selectors</a></li>
   <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Selectors/Attribute_selectors">Attribute selectors</a></li>
   <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements">Pseudo-classes and pseudo-elements</a></li>
   <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Selectors/Combinators">Combinators</a></li>
  </ul>
 </li>
 <li><a href="/en-US/docs/Learn/CSS/Building_blocks/The_box_model">The box model</a></li>
 <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Backgrounds_and_borders">Backgrounds and borders</a></li>
 <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Handling_different_text_directions">Handling different text directions</a></li>
 <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Overflowing_content">Overflowing content</a></li>
 <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Values_and_units">Values and units</a></li>
 <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Sizing_items_in_CSS">Sizing items in CSS</a></li>
 <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Images_media_form_elements">Images, media, and form elements</a></li>
 <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Styling_tables">Styling tables</a></li>
 <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Debugging_CSS">Debugging CSS</a></li>
 <li><a href="/en-US/docs/Learn/CSS/Building_blocks/Organizing">Organizing your CSS</a></li>
</ol>