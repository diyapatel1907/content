---
title: Web accessibility for seizures and physical reactions
slug: Web/Accessibility/Seizure_disorders
tags:
  - Media Queries
  - PEAT
  - Photosensitive Epilepsy Analysis Tool
  - The Harding Test
  - color
  - epilepsy
  - musicogenic seizures
  - photosensitivity
  - prefers-reduced-motion
  - reflex epilepsy
  - saturation
  - seizure disorders
  - seizures
  - web animation
---
<p>This article introduces concepts behind making web content accessible for those with vestibular disorders, and how to measure and prevent content leading to seizures and / or other physical reactions.</p>

<h2 id="Overview">Overview</h2>

<h3 id="Seizures">Seizures</h3>

<p>Seizures caused by light are known as photosensitive epilepsy. Content that flickers, flashes, or blinks can trigger photosensitive epilepsy. Web technologies that use video, animated gifs, animated pngs, animated SVGs, Canvas, and CSS or JavaScript animations are all capable of content that can induce seizures or other incapacitating physical reactions. Certain visual patterns, especially stripes, can also cause physical reactions even though they are not animated. Photosensitive epilepsy is actually a kind of "reflex epilepsy"—seizures occurring in response to a trigger. In the case of photosensitive epilepsy, seizures are triggered specifically by flashing lights, but other types of reflex epilepsies may be triggered by the act of reading, or by noises. Patterns and images can also trigger epilepsy.</p>

<p>The fact that static images may cause seizures and other disorders is documented in such articles as “<strong><a href="https://doi.org/10.1016/j.cub.2017.03.076">Gamma Oscillations and photosensitive epilepsy</a></strong>”, where it is noted “<em>Certain visual images, even in the absence of motion or flicker, can trigger seizures in patients with photosensitive epilepsy</em>” The Epilepsy Foundation, in its article,<a href="https://www.epilepsy.com/article/2014/3/shedding-light-photosensitivity-one-epilepsys-most-complex-conditions-0"> "<strong>Shedding Light on Photosensitivity, One of Epilepsy's Most Complex Conditions</strong>" </a>talks about static images and patterns. "<em>Static or moving patterns of discernable light and dark stripes have the same effect as flashing lights because of the alternation of dark and bright areas."</em> The Epilepsy Foundation of America Working Group is able to "quantify" the problem a little.<em> "A pattern with the potential for provoking seizures contains clearly discernible stripes, numbering more than five light-dark pairs of stripes in any orientation</em>" In addition to stripes, checkered patterns have also been known to cause photosensitive seizures, according to <strong><a href="https://www.cedars-sinai.edu/Patients/Health-Conditions/Photosensitive-Seizures.aspx">Cedars-Sinai.</a></strong></p>

<p>Although static images are possible as triggers, they are less consistent. The trigger that is well established and strong is flashing/strobe lights. Dr. Selim Benbadis of USF's Comprehensive Epilepsy Program notes, "The only thing that is really documented is flashing lights, which can trigger seizures in patients with photosensitive epilepsy. Only a few types of epilepsies are photosensitive though, and the vast majority of epilepsies are not." In addition to seizures brought about by photosensitivity, listening to certain pieces of music can also trigger what are called musicogenic seizures, although these types of seizures seem to be much more rare. For a great introduction on the topic of musicogenic seizures, visit Epilepsy Ontario's web page on <strong><a href="https://epilepsyontario.org/musicogenic-seizures/">Musicogenic Seizures</a></strong>.</p>

<p>Seizures and epilepsy are not the same. In its article,<a href="https://www.epilepsy.com/article/2014/4/revised-definition-epilepsy"> <strong>"A Revised Definition of Epilepsy"</strong></a> the Epilepsy Foundation notes that…"<em>a seizure is an event and epilepsy is the disease involving recurrent unprovoked seizures</em>." According to the Epilepsy Foundation's page "<strong><a href="https://www.epilepsy.com/start-here/about-epilepsy-basics/how-serious-are-seizures">How Serious Are Seizures?</a></strong>" , "<em>Sudden unexpected death in epilepsy (SUDEP) is likely the most common disease-related cause of death in with epilepsy. It is not frequent but it is a very real problem and people need to be aware of its risk</em>".</p>

<p>The point is, seizures most definitely can be and are fatal, and developers and designers are incredibly important to making the web a safer place for those with sensitivities to photosensitive or musicogenic triggers.</p>

<p>Seizures can be fatal, but even the ones that are "only" debilitating can be of such severity, that they render the user incapacitated. Other disorders, such as disorientation, nausea, vomiting, and more can also be so severe that the user is unable to function. The Epilepsy Foundation's article, <strong><a href="https://www.epilepsy.com/learn/triggers-seizures/photosensitivity-and-seizures">Photosensitivity and Seizures</a></strong>, provides a list of triggers that may cause seizures in photosensitive people; here's an excerpt from that list:</p>

<ul>
	<li>Television screens or computer monitors due to the flicker or rolling images.</li>
	<li>Certain video games or TV broadcasts containing rapid flashes or alternating patterns of different colors.</li>
	<li>Intense strobe lights like visual fire alarms.</li>
	<li>Natural light, such as sunlight, especially when shimmering off water, flickering through trees or through the slats of Venetian blinds.</li>
	<li>Certain visual patterns, especially stripes of contrasting colors.</li>
</ul>

<p>That same article continues that many factors must combine to trigger the photosensitive reaction. Of note is that it includes the wavelength of light as a possible factor; wavelengths in the red part of the spectrum seem to be especially problematic. In the article, "<strong><a href="https://www.w3.org/TR/UNDERSTANDING-WCAG20/seizure-does-not-violate.html">Understanding WCAG 2.0 Three Flashes or Below Threshold</a></strong>" notes generally that: “<em>Individuals who have photosensitive seizure disorders can have a seizure triggered by content that flashes at certain frequencies for more than a few flashes</em>” and goes on to note, very specifically that: “<em><strong>People are even more sensitive to red flashing than to other colors, so a special test is provided for saturated red flashing</strong></em>”.</p>

<p>You don't even need an image or video to cause harm. A <code>&lt;div&gt;</code> element set to change color and luminosity at high frequency, easily done via JavaScript, can cause real harm. And, flickering can occur everywhere. For example, "spinners" commonly used to display while pages load, can easily "flicker" while spinning.</p>

<p>Additional concerns exist for individuals with motor-skills problems. For example, the page for Trace Research &amp; Development Center’s <strong><a href="https://trace.umd.edu/peat">Photosensitive Epilepsy Analysis Tool</a></strong> notes that “<em>Photosensitive seizures can be provoked by certain types of flashing in web or computer content, including mouse-overs that cause large areas of the screen to rapidly flash on and off repeatedly</em>.”</p>

<h3 id="Other_physical_reactions">Other physical reactions</h3>

<p>Nausea, vertigo (or dizziness), and disorientation are very nonspecific symptoms associated with all kinds of diseases and not particularly suggestive of seizures (except maybe disorientation, which is seen in seizures). However, seizures are not the only adverse physical response possible from flashing, flickering, blinking, and other such stimuli. In 1997, a Japanese cartoon featured an animated "virus bomb". Some of the children watching the cartoon reacted by having seizures, others by suffering nausea, shaking, and vomiting blood. The reactions from the children were so severe, they had to be rushed to the emergency room. The physical disorders listed below are all possible consequences: each of these physical reactions may be so severe as to be incapacitating.</p>

<ul>
	<li>Seizures</li>
	<li>Vestibuler Disordera</li>
	<li>Migraines</li>
	<li>Nausea</li>
	<li>Vomiting</li>
</ul>

<h2 id="Flashing_blinking_flickering">Flashing, blinking, &amp; flickering</h2>

<p>Although "flashing" and "blinking" are sometimes used interchangeably, they are not the same. According to the W3C, blinking is a distraction problem, whereas flashing refers to content that occurs more than 3 times per second, is large enough, and bright enough. <strong><a href="https://www.section508.gov/content/guide-accessible-web-design-development#flashing">Section 508</a></strong> prohibits flickering effects with a frequency greater than 3 Hz (flickers per second) and lower than 55 Hz. The Epilepsy Foundation's article "<strong><a href="https://www.epilepsy.com/article/2014/3/shedding-light-photosensitivity-one-epilepsys-most-complex-conditions-0">Shedding Light on Photosensitivity, One of Epilepsy's Most Complex Conditions</a></strong>" notes "<em>Generally, flashing lights between the frequencies of five to 30 flashes per second (Hertz) are most likely to trigger seizures. In order to be safe, the consensus recommends that photosensitive individuals should not be exposed to flashes greater than three per second.</em>" For some people, however, flashing/blinking can cause symptoms at less than 3 Hz.</p>

<p>It's important to note that not all flashing and blinking is bad. NASA, in its document titled, "<strong><a href="https://colorusage.arc.nasa.gov/flashing.php">Blinking, Flashing, and Temporal Response</a></strong>" notes that blinking and flashing can be powerful tools for drawing attention—as is necessary for warning buttons— (This assumes that users can still see the screen while elements are flashing. This is not always true.) For some users, blinking but also cautions that they must be used sparingly, and with care. As it applies to web design, systems that alert company employees to danger by "hijacking" the screen to provide a flashing warning of emergency need to take into consideration the rate, size, and luminosity changes in the screen as these warnings are flashed.</p>

<h3 id="Flashing_and_Flickering—How_is_danger_quantified">Flashing and Flickering—How is danger quantified?</h3>

<p>According to the article, <strong><a href="https://www.epilepsy.com/sites/core/files/atoms/files/Epilepsia%20vol%2046%20issue%209%20Photosensitivity.pdf">Photic- and pattern-induced seizures: expert consensus of the Epilepsy Foundation of America Working Group,</a></strong> "<em>A flash is a potential hazard if it has luminance &gt;or=20 cd/m2, occurs at a frequency of &gt;or=3 Hz, and occupies a solid visual angle of &gt;or=0.006 steradians (approximately 10% of the central visual field or 25% of screen area at typical viewing distances)</em>."</p>

<p>How far is a typical viewing distance? The recommendation considered for a typical viewing distance at the time of the writing was "<em>the area can be taken as applying to an area &gt;25% of the area of a television screen, assuming standard viewing distances of ≥2 m (∼9 feet</em>)". Much has changed since that time, and we are now much closer to our screen.</p>

<p>Certain colors, and/or combinations of colors, also matter. <strong><a href="https://www.sciencedaily.com/releases/2009/09/090925092858.htm">Certain Colors More Likely To Cause Epileptic Fits, Researchers Find,</a></strong> notes that "<em>…complexities underlying brain dynamics could be modulated by certain color combinations more than the others, for example, red-blue flickering stimulus causes larger cortical excitation than red-green or blue-green stimulus."</em></p>

<h3 id="Flashing_flashing_red">Flashing &amp; flashing red</h3>

<p><strong><a href="https://www.w3.org/WAI/WCAG21/Understanding/three-flashes-or-below-threshold.html">WCAG 2.3.1 general flash and red flash thresholds</a> are defined as follows:</strong></p>

<ul>
	<li>A <strong>general flash</strong> is defined as a pair of opposing changes in <strong><a href="https://www.w3.org/TR/WCAG21/#dfn-relative-luminance">relative luminance</a></strong> of 10% or more of the maximum relative luminance where the relative luminance of the darker image is below 0.80; and where "a pair of opposing changes" is an increase followed by a decrease, or a decrease followed by an increase, and</li>
	<li>A <strong>red flash</strong> is defined as any pair of opposing transitions involving a saturated red</li>
</ul>

<p>These standards are based on earlier research. In 2004, The Epilepsy Foundation of America convened a workshop developed a<strong><a href="https://www.ncbi.nlm.nih.gov/pubmed/16146438"> consensus</a></strong> on photosensitive seizures, stating "<em>A flash is a potential hazard if it has luminance at least 20 cd/m2 , occurs at a frequency of least 3 Hz, and occupies a solid visual angle of at least 0.006 steradians (about 10% of the central visual field or 25% of screen area at typical viewing distances)."</em> The transition to or from a saturated red is important; the transition to or from a saturated red is a risk on its own: "<strong><em>Irrespective of luminance, a transition to or from a saturated red is also considered a risk.</em>"</strong></p>

<h3 id="Size_and_distance">Size and distance</h3>

<h4 id="How_big_It_depends.">How big? It depends.</h4>

<p>"Relative" size and distance both matter. According to <strong><a href="https://trace.umd.edu/peat">PEAT</a></strong>, "<em>The combined area of flashes occurring concurrently occupies no more than a total of one quarter of any 341 x 256 pixel rectangle anywhere on the displayed screen area when the content is viewed at 1024 by 768 pixels</em>."</p>

<p>The point that the field of vision is an important consideration arises in the article addressing WCAG 2.3.1 continues: "<em>The 1024 x 768 screen is used as the reference screen resolution for the evaluation. The 341 x 256 pixel block represents a 10 degree viewport at a typical viewing distance. (The 10 degree field is taken from the original specifications and represents the central vision portion of the eye, where people are most susceptible to photo stimuli.)</em>"</p>

<p>This pixel area ratio calculates for relative size, but distance also matters.</p>

<p>Distance matters because it affects the total field of vision. When viewers wear ocular masks for gaming, the field of vision is likely enveloped in its entirety by the screen. <strong><a href="https://webvr.info/">WebVR</a></strong> is an open specification that makes it possible to experience VR in your browser, which can be experienced on phone, computer or headset. The concern about flashing images in an ocular mask is a growing one, since the mask is so close to the eyes.</p>

<p><strong><a href="https://www.epilepsysociety.org.uk">The Epilepsy Society (UK)</a></strong>, in their article, "<strong><a href="https://www.epilepsysociety.org.uk/3d-films-and-virtual-reality#.XQlC5ohKiUk">3d Films and Virtual Reality</a></strong>", noted: "<em>With VR the images flash very quickly and generally this is too quickly to trigger a seizure in people with photosensitive epilepsy. However, the field of view is large and so more of the eye is stimulated. This means that more of the brain may be affected and this may trigger a photosensitive seizure</em>."</p>

<p>(Note that some users will not be able to see with blinking cursors, and may get migraines, motion sickness, and disorientation, although blinking cursors occupy a much smaller area of the screen.)</p>

<h3 id="Patterns_and_parallax">Patterns, and parallax</h3>

<p>Contrasting dark and light geometric patterns are a known culprit; stripes and checks are the best known examples. The Epilepsy Foundation of America Working Group lists how many light-dark pairs of stripes are likely to provoke seizures, and, in what conditions. If a pattern is unchanging and straight, eight lines is the maximum allowable, but if it undulates, no more than five lines.</p>

<p>Parallax effects can cause disorientation. Use parallax effects with caution; if you must use them, ensure the user has a control to turn them off.</p>

<p>"A pattern with the potential for provoking seizures contains clearly discernible stripes, numbering more than five light-dark pairs of stripes in any orientation. When the light-dark stripes of any pattern collectively subtend at the eye from the minimal-expected viewing distance a solid angle of &gt;0.006 steradians, the luminance of the lightest stripe is &gt;50 cd/m2, and the pattern is presented for &gt;or=0.5 s, then the pattern should display no more than five light-dark pairs of stripes, if the stripes change direction, oscillate, flash, or reverse in contrast; if the pattern is unchanging or smoothly drifting in one direction, no more than eight stripes."</p>

<p>Not all is known, and even with the metrics listed above, additional factors come into play. For example, going from a smaller area to a larger one increases the likelihood that the brain responds, as well as increasing contrast, and increasing spatial frequency from a low to middle. It's also known, although the reasoning is not understood behind it, that going from simple orientations (for example, stripes) to a multiple one (for example, the checkered pattern that emerges when laying one set of stripes on top of, but perpendicular to, the original set) affects the brain.</p>

<h3 id="Colors">Colors</h3>

<p>Understanding color is important for accessibility. See <a href="/en-US/docs/Web/Accessibility/Understanding_Colors_and_Luminance">understanding colors and luminance</a> as it relates to web accessibility and accessibility in general.</p>

<p>How the color relates to its background—usually framed in terms of contrast—and how drastically the color changes frame to frame in animation is important. For more on this, see <strong><a href="https://www.w3.org/TR/UNDERSTANDING-WCAG20/seizure-does-not-violate.html">Three Flashes or Below Threshold Understanding SC 2.3.1</a></strong></p>

<h4 id="The_Special_Case_of_Red"><strong>The Special Case of Red </strong></h4>

<p>It has been demonstrated that <strong><a href="https://www.sciencedaily.com/releases/2009/09/090925092858.htm">some colors are more likely to cause epileptic fits than others</a></strong>; Human physiology and psychology is affected by the color red in general.  Its power to influence behavior has even been noted in animals. </p>

<ul>
	<li><strong>Red Desaturation tests</strong> The human eye is so sensitively tuned to red that ophthalmologists set up a test using it. The Red desaturation test assesses the integrity of the optic nerve. For more information as to how an ophthalmologist uses this test, see <strong><a href="https://www.smart-optometry.com/red-desaturation/">Red Desaturation</a></strong></li>
	<li><strong>Red Environment:</strong> Studies have shown that for those who suffer Traumatic Brain Injury, <strong><a href="https://www.ncbi.nlm.nih.gov/pubmed/20649469">cognitive function is reduced in a red environment</a></strong>.</li>
</ul>

<p><strong><a href="/en-US/docs/Web/Accessibility/Understanding_Colors_and_Luminance">Saturated Red </a></strong>is a special, dangerous case, and there are special tests for it. In addition to a red environment affecting the cognitive function of those with Traumatic Brain Injury, color in the red spectrum wavelength seems to require special concern and special tests. Dr. Gregg Vanderheiden, when testing the Photosensitive Epilepsy Analysis Tool, noted that the seizure rates were much higher than expected. They found that we are much more sensitive to saturated red flashing. (See the video,<strong><a href="https://www.pbs.org/video/university-place-the-photosensitive-epilepsy-analysis-tool-ep-429/"> The Photosensitive Epilepsy Analysis Tool</a></strong><a href="https://www.pbs.org/video/university-place-the-photosensitive-epilepsy-analysis-tool-ep-429/">)</a></p>

<h4 id="Websafe_does_not_mean_seizure-safe">Websafe does not mean seizure-safe</h4>

<p>Note that the color <strong>#990000</strong> is considered "<strong>websafe</strong>". That does <em>not</em> mean it is safe as "safe for not causing seizures", it only means that the color may be "safely" reproduced accurately by the technology used to generate color on screens.</p>

<h2 id="Measuring_to_prevent_harm">Measuring to prevent harm</h2>

<p>Measuring the potential for harm is a good starting point. Factors considered within tests include color, luminosity, size, contrast, and in cases of animation, frequency. WCAG 2.1 provides guidance for evaluating content.</p>

<p>In August, 2004, the Epilepsy Foundation of America convened a workshop to begin to develop an expert consensus on photosensitive seizures. The following, expert, and authoritative information is from: <strong><a href="https://www.ncbi.nlm.nih.gov/pubmed/16146438">Photic- and pattern-induced seizures: expert consensus of the Epilepsy Foundation of America Working Group.</a></strong></p>

<p>"<em>A flash is a potential hazard if it has luminance &gt;or=20 cd/m2, occurs at a frequency of &gt;or=3 Hz, and occupies a solid visual angle of &gt;or=0.006 steradians (approximately 10% of the central visual field or 25% of screen area at typical viewing distances). A transition to or from saturated red also is considered a risk. A pattern with the potential for provoking seizures contains clearly discernible stripes, numbering more than five light-dark pairs of stripes in any orientation. When the light-dark stripes of any pattern collectively subtend at the eye from the minimal-expected viewing distance a solid angle of &gt;0.006 steradians, the luminance of the lightest stripe is &gt;50 cd/m2, and the pattern is presented for &gt;or=0.5 s, then the pattern should display no more than five light-dark pairs of stripes, if the stripes change direction, oscillate, flash, or reverse in contrast; if the pattern is unchanging or smoothly drifting in one direction, no more than eight stripes. These principles are easier to apply in the case of fixed media, for example, a prerecorded TV show, which can be analyzed frame-by-frame, as compared with interactive media.</em>"</p>

<p>The "cd/m2" refers to candela per square meter. So for the web developer, how does this relate to measurements for color, luminance, and saturation?</p>

<p>The candela is a SI unit (International System of units) of luminous intensity. It's a photometric term, and photometry deals with the measurement of visible light as perceived by human eyes. Wikipedia's article on "<strong><a href="https://en.wikipedia.org/wiki/Candela_per_square_metre">Candela per square metre</a></strong>" puts it in terms of what we are familiar with as developers: on a display device, and in the RGB space. This is helpful, because there's a specific standard assumed to be used on monitors, printers, and the Internet, and it is the <strong>sRGB</strong> (standard Red Green Blue).</p>

<p>"<em>As a measure of light emitted per unit area, this unit is frequently used to specify the brightness of a display device. The <strong><a href="https://en.wikipedia.org/wiki/SRGB">sRGB</a></strong> spec for monitors targets 80 cd/m<sup>2</sup>.<sup><a href="https://en.wikipedia.org/wiki/Candela_per_square_metre#cite_note-3">[3]</a></sup> Typically, calibrated monitors should have a brightness of 120 cd/m<sup>2</sup>. Most consumer desktop <strong><a href="https://en.wikipedia.org/wiki/Liquid_crystal_display">liquid crystal displays</a></strong> have luminances of 200 to 300 cd/m<sup>2</sup>.<sup><a href="https://en.wikipedia.org/wiki/Candela_per_square_metre#cite_note-4">[4]</a></sup> <strong><a href="https://en.wikipedia.org/wiki/High-definition_television">High-definition televisions</a></strong> range from 450 to about 1500 cd/m<sup>2</sup></em>."</p>

<p>The takeaway is that the <strong>sRGB</strong> color space is a common touch point between research, assessment tools, and developers, since it is easily converted from the commonly used Hex code.</p>

<h3 id="Human_physiology_and_psychology_as_a_consideration">Human physiology and psychology as a consideration</h3>

<p>Many experts work to quantify and measure to the greatest extent possible the kinds of web content that can serve as triggers for seizures. That said, it can't be forgotten that color is as much about human perception in the brain as it is the measurement of light coming from a computer screen.</p>

<p>In addition to the psychological variances, there are also physiological differences among us. There will be variances and nuances as to how a real human being perceives, and responds to, color and light. For example, Tom Jewett, Lecturer Emeritus of Computer Sciences at Cal State University Long Beach, notes the following concerning <strong><a href="https://colortutorial.design/hsb.html">lightness in the HSL color scale</a></strong> "…<em>The distinction between levels of lightness is not actually linear as the HSL scale would imply; we are much more sensitive to changes in lighter values than to darker ones</em>."</p>

<p>It's important to understand that light and its measurements are linear, but human vision and human perception are not. Investigation and discussion is ongoing as to how to relate the machine measurement of light as it passes from a computer screen, through the distance to the human eye, filtered by human vision, and then manipulated through the human brain.</p>

<p>Even age and sex can play a role. According to the Epilepsy Foundation's article, <strong><a href="https://www.epilepsy.com/article/2014/3/shedding-light-photosensitivity-one-epilepsys-most-complex-conditions-0">Shedding Light on Photosensitivity, One of Epilepsy's Most Complex Conditions</a></strong><em>, "Children and adolescents are more prone than adults to have an abnormal response to light stimulation, and the first light-induced seizure almost always occurs before age 20".</em> The article follows with this statistic: <em>"Girls (60 percent) are more often affected than boys (40 percent), although seizures are more frequent in boys because they are more likely to be playing video games. Video games often contain potentially provocative light stimulation".</em></p>

<p><strong>User testing is very problematic</strong>. Naturally, no one wants to subject a seizure-prone individual to user testing. It's dangerous. To that point, one of the most ethical thing that developers and designers can do is use tools that have been developed by experts in the field who have worked hand-in-hand with physicians to develop the tool. As of this writing, there are two commonly available tools that have been ethically and professionally developed by researchers and physicians for film/videos: <strong>PEAT</strong>, and the <strong>Harding Test</strong>.</p>

<h3 id="Photosensitive_Epilepsy_Analysis_Tool_PEAT">Photosensitive Epilepsy Analysis Tool (PEAT)</h3>

<p>The <a href="https://trace.umd.edu/"><strong>Trace Research and Development Center</strong></a> has set a gold standard for a <strong><a href="https://trace.umd.edu/peat">Photosensitive Epilepsy Analysis Tool</a></strong>, and they've made a point to make it <em><strong>free</strong></em> to download. PEAT can help authors determine whether animations or video in their content are likely to cause seizures. Please note the restriction on its use: <em><strong>Use of PEAT to assess material commercially produced for television broadcast, film, home entertainment, or gaming industries is prohibited. Use the Harding Test or other tools for commercial purposes.</strong></em></p>

<p>To get a free copy of the University of Maryland's Photosensitive Epilepsy Analysis Tool, visit the <strong><a href="https://trace.umd.edu/">Trace Research &amp; Development Center</a></strong></p>

<p><img alt="University of Maryland College of Information Studies Photosensitive Epilepsy Analysis Tool." src="peatversion1pt6.png"></p>

<h3 id="The_Harding_Test">The Harding Test</h3>

<p>As use of the PEAT tool is prohibited for commercial use, television programmers can use the Harding Test at <strong><a href="https://www.hardingtest.com/">HardingTest.com</a></strong>. The Harding Test is another gold standard. Television programmers in various countries must pass this test before being able to broadcast, so the group at <strong><a href="https://www.hardingtest.com/">HardingTest.com</a></strong> provide both analysis and certification of video content.</p>

<p><img alt="Harding Flash and Pattern Analyzer." src="screen_shot_2019-06-20_at_11.16.17_am.png"></p>

<h2 id="Accessibility_Solutions_for_Developers">Accessibility Solutions for Developers</h2>

<p>All animations are potentially dangerous. As designers and developers our responsibility is to ensure we do no harm either intentionally or unintentionally. If we must include something that has the potential to cause harm, it is vital to prevent users from accidentally encountering the harmful content, and to provide ways for users to prevent and control animations mitigating potential harm:</p>

<h3 id="What_the_web_developer_can_do">What the web developer can do</h3>

<h4 id="Do_no_harm">Do no harm</h4>

<p><strong><a href="https://www.w3.org/WAI/standards-guidelines/wcag/new-in-21/">WCAG Guideline 2.3 Seizures and Physical Reactions</a></strong> provides an overview: “Do not design content in a way that is known to cause seizures or physical reactions”. Don't include animation that a user cannot control. Don't design with patterns known to cause problems. If you must include a gif or png with flashing in it, record it in a video format instead so that controls are available to the user. Give the user the ability to avoid it, turn it off, or render it less harmful.</p>

<h4 id="Understand_malice">Understand malice</h4>

<p>As a developer or designer, ask yourself if strobing content really needs to be on your webpage. Even if handled properly, there are those who may download offending content from your site and weaponize it. It is believed the first documented attempt at using computers to effect physical harm via animation began Saturday, March 22, 2008: The Epilepsy Foundation's website was hacked via posts with flashing images and links falsely claiming to be helpful. Users with vestibular disorders who were seeking help from the site were affected.</p>

<p>A series of legal considerations are underway after journalist Kurt Eichenwald, a known epileptic, suffered a seizure after being sent an animated gif in December 2016: the flashing gif carried the message, "You deserve a seizure for your posts".</p>

<h4 id="Control_exposure_control_access">Control exposure, control access</h4>

<p>Controlling exposure to the page is key to ensuring that someone susceptible to seizures is not exposed to it accidentally. WCAG notes that a single object can make the entire page unusable.</p>

<p>If you believe you may have an image or animation that may cause seizures, control access to it by first displaying a warning about the content, and then putting it in a location where the user must opt in to it, such as clicking a button, or ensuring that the link to the page has a distinct and obvious warning.</p>

<p>Consider using metadata such as <code><strong>&lt;meta name="robots" content="noindex, nofollow"&gt;</strong></code> so that the page is not indexed by search engines.</p>

<h4 id="Do_Not_Index_Do_Not_Follow">Do Not Index, Do Not Follow</h4>

<p>By not indexing the page, the likelihood that users will stumble upon it via search will be reduced.</p>

<pre class="brush: html">&lt;html&gt;
&lt;head&gt;
&lt;title&gt;…&lt;/title&gt;
<strong>&lt;meta name="robots" content="noindex, nofollow"&gt;</strong>
&lt;/head&gt; </pre>

<h3 id="Animated_GIFs">Animated GIFs</h3>

<p>All image types are potentially dangerous, however, animated gifs deserve special mention because of their ubiquity, and the fact that the animation speed is actually controlled within the GIF file itself.</p>

<h4 id="Detect_if_a_GIF_is_animated">Detect if a GIF is animated</h4>

<ul>
	<li><strong><a href="https://www.npmjs.com/package/animated-gif-detector">NPM's animated-gif-detector</a></strong> allows for the ability to determine animate <em>as early as possible</em> in a given HTTP request.</li>
	<li>Zakirt provides a gist for <strong><a href="https://gist.github.com/zakirt/faa4a58cec5a7505b10e3686a226f285">animated-gif-detect.js</a></strong></li>
</ul>

<p>With animated GIFs, ensure animation is inactive until the user chooses to activate it. For example, the user must push a button or check a box in order to start the animation.</p>

<p><strong>Resources for detecting and controlling animated GIFs include</strong></p>

<ul>
	<li><strong><a href="https://npm.runkit.com/animated-gif-detector">RunKit Animated GIF Detector.</a></strong></li>
	<li><strong><a href="https://rubentd.com/gifplayer/">rubentd.com/gifplayer/</a></strong> is a jQuery plugin that will help you play and stop animated gifs on your website</li>
</ul>

<h3 id="Videos">Videos</h3>

<p>As in the case of animated GIFs, the user must push a button or check a box in order to start the animation. There are many ways to do this, such as NOT adding the <code><a href="/en-US/docs/Web/API/HTMLMediaElement/autoplay">autoplay</a></code> attribute to <strong><code>&lt;video controls&gt;</code></strong>, or setting {{CSSxRef('animation-play-state')}} to <code>paused</code> as an initial state. To see a powerful example of how this can actually work see the article by <strong><a href="https://www.kirupa.com/html5/toggling_animations_on_off.htm">Kirupa, Toggling Animations On and Off.</a></strong><a href="https://www.kirupa.com/html5/toggling_animations_on_off.htm"> </a> Kirupa uses the <strong><code>animation-play-state</code></strong> in concert with {{CSSxRef('transition')}}, {{CSSxRef('transform')}}, and {{CSSxRef('prefers-reduced-motion')}} to create a very accessible experience under the user's control.</p>

<p><strong><a href="https://www.w3.org/TR/css-animations-1/#animation-play-state">animation-play-state</a></strong> This is a css property that sets whether an animation is running or paused.</p>

<pre class="brush: css">div {
  animation-play-state: paused;
}</pre>

<p><strong><a href="https://www.w3.org/TR/css-transitions-1/">transitions</a></strong> Set the duration to zero for the initial stage of animation.</p>

<pre class="brush: html">div {
  transition-duration: 0s;
}</pre>

<h3 id="Ensure_the_user_can_also_stop_animations_as_well_as_start_them">Ensure the user can also stop animations as well as start them</h3>

<p><code><strong>&lt;video&gt;</strong></code> with no attributes will not play automatically, but also will have no controls. Ensure that you add the <strong><code>controls</code></strong> attribute to the video element so that the user can stop the video as well as start it.</p>

<pre class="brush: html">&lt;video controls&gt;
  &lt;source src="video.mp4" type="video/mp4"&gt;
  &lt;source src="video.ogg" type="video/ogg"&gt;
  Your browser does not support the video tag.
&lt;/video&gt;
</pre>

<h4 id="Programmatically_ensure_controls_are_available">Programmatically ensure controls are available</h4>

<p>The <strong><code>HTMLMediaElement.controls</code></strong> property reflects the <strong><code>controls</code></strong> HTML attribute, which controls whether user interface controls for playing the media item will be displayed.</p>

<h5 id="Video">Video</h5>

<p>To ensure that a video has controls that a user can access, ensure that you add the word "controls" to HTML5 video and audio elements.</p>

<p><strong><code>&lt;video controls&gt;</code></strong></p>

<pre class="brush: html">&lt;video controls&gt;
  &lt;source src="myVideo.mp4" type="video/mp4"&gt;
  &lt;source src="myVideo.webm" type="video/webm"&gt;
  &lt;p&gt;Your browser doesn't support HTML5 video. Here is
     a &lt;a href="myVideo.mp4"&gt;link to the video&lt;/a&gt; instead.&lt;/p&gt;
&lt;/video&gt;</pre>

<h5 id="Audio">Audio</h5>

<p>Taking that same example and applying it to audio,</p>

<p><strong><code>&lt;audio controls&gt;</code></strong></p>

<pre class="brush: html">&lt;audio controls&gt;
  &lt;source src=&quot;myAudio.ogg&quot; type=&quot;audio/ogg&quot;&gt;
  &lt;source src=&quot;myAudio.mp3&quot; type=&quot;audio/mpeg&quot;&gt;
  &lt;p&gt;Your browser does not support the audio element. Here is a &lt;a href=&quot;myAudio.mp3&quot;&gt;link to the audio&lt;/a&gt; instead.&lt;/p&gt;
&lt;/audio&gt;</pre>

<h5 id="Audio_as_part_of_Video">Audio as part of Video</h5>

<p>Note that the audio in videos can be controlled by the muted content attribute, even though the content is within the <strong><code>&lt;video&gt;</code></strong> element rather than the <strong><code>&lt;audio&gt;</code></strong> element. This example is from the section on <strong><a href="https://html.spec.whatwg.org/multipage/media.html#concept-media-muted">muted media attribute</a></strong> description from the HTML Living Standard. It explains that the video will autoplay quietly in the background until the user takes action to unmute the audio.</p>

<pre class="brush: html">&lt;video src="adverts.cgi?kind=video" controls autoplay loop muted&gt;&lt;/video&gt;</pre>

<h3 id="Control_speed">Control speed</h3>

<p>This seems obvious, but because there are so many MIME types, the mechanisms for handling them varies greatly, and for that reason there's not a one-size-fits-all solution to the problem. This is further complicated by the fact that even how files are classified complicates how they should be handled. For example, the .gif file format is usually understood to be an image, but is also considered a video file format in some circles because of its ability to be animated. For a comprehensive listing of media types, please visit<strong><a href="https://www.iana.org/assignments/media-types/media-types.xhtml"> IANA.org's page for Media Types.</a></strong><a href="https://www.iana.org/assignments/media-types/media-types.xhtml">.</a></p>

<p>The methods for sniffing them out is not a casual exercise. You may be interested in following the <strong><a href="https://mimesniff.spec.whatwg.org/">MIME Sniffing</a></strong> standard at whatwg.org. Just about every kind of image can be animated; how they are animated varies, and therefore, the control of the animation varies.</p>

<h4 id="Commonly_animated_file_types">Commonly animated file types</h4>

<ul>
	<li><strong>Bitmap</strong> animation</li>
	<li><strong>Canvas</strong> MDN's tutorial on Canvas has a great section on <strong><a href="/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_animations">Basic Animations</a></strong> <code><strong>setInterval()</strong></code> is a mainstay in Canvas animation, but it is also interesting to see how it interacts with screen refresh. See the article, <strong><a href="https://stackoverflow.com/questions/19764018/controlling-fps-with-requestanimationframe">Controlling fps with requestAnimationFrame?</a></strong> in which they discuss the nuts and bolts of implementing <strong><code>requestAnimationFrame</code></strong> against the backdrop of screen refresh.</li>
	<li><strong>GIFs (Raster)</strong> are tough to crack because control for their animation resides within the gif files themselves. For information about controlling the speed of gifs see <strong>W3C's</strong> <strong>G152: Setting animated gif images to stop blinking after n cycles (within 5 seconds)</strong> <strong><a href="https://www.w3.org/TR/WCAG20-TECHS/G152.html">https://www.w3.org/TR/WCAG20-TECHS/G152.html</a></strong> A great <strong>stackoverflow</strong> article on the subject is, "<strong><a href="https://stackoverflow.com/questions/2385203/can-you-control-gif-animation-with-javascript">Can you control GIF animation with Javascript?</a></strong>"</li>
	<li><strong>GIFV (Raster)</strong> considered a variant, video version of GIF. The format is not standardized, and must reference a "real" video file (e.g. a .webm file) which must exist elsewhere.</li>
	<li><strong>JPG (Raster)</strong></li>
	<li><strong>MNG (Raster)</strong> Multiple-image Network Graphics is a graphics file format for animated images. Also considered by some to be a video format.</li>
	<li><strong>PNG, APNG (Raster)</strong> Portable Network Graphics and Animated Portable Network Graphics may both be animated.</li>
	<li><strong>SVGs (Vector)</strong> The MDN document, "<strong><a href="/en-US/docs/Web/SVG">SVG: Scalable Vector Graphics</a></strong>", notes that "<em>SVG is a text-based open Web standard. It is explicitly designed to work with other web standards such as <strong><a href="/en-US/docs/Web/CSS">CSS</a></strong>, <strong><a href="/en-US/docs/Web/API/Document_Object_Model">DOM</a></strong>, and <strong><a href="/en-US/docs/Web/SVG/SVG_animation_with_SMIL">SMIL</a></strong>.</em>" SVGs can be used as an image, for example, <strong><code>&lt;img src="example.svg" alt="This is an image using a svg as a source"&gt;</code></strong> This means that SVG appearance and animation can be controlled through CSS keyframes and animations. For interaction with JavaScript, see the MDN documents on <strong><a href="/en-US/docs/Web/API/Document_Object_Model#svg_interfaces">SVG Interfaces</a></strong> and <strong><a href="/en-US/docs/Web/SVG/Applying_SVG_effects_to_HTML_content">Applying SVG effects to HTML content</a></strong>.</li>
	<li><strong>Voxel</strong> <strong>(Raster)</strong> Three-dimensional <strong><a href="https://en.wikipedia.org/wiki/Voxel">voxel</a></strong> raster graphics are employed in video games and are also used in medical imaging.</li>
</ul>

<h4 id="Text_can_also_be_animated">Text can also be animated</h4>

<p>Translations and transformations can animate text in a div, and do harm. Although it is experimental technology, <code><strong><a href="/en-US/docs/Web/API/CSSKeyframe/keyText" rel="nofollow">CSSKeyframe.keyText</a></strong></code> is being developed. Moving text can induce seizures for the same reasons that moving images do, so avoid animating your text. It's a good idea to avoid using moving text anyhow, as many screenreaders cannot read moving text and it's bad user experience even for those with no vision or vestibular issues.</p>

<h3 id="CSS_for_animation">CSS for animation</h3>

<p>In the style sheet or within the <strong><code>&lt;style&gt;</code></strong> element, many options can combine together to create a powerful experience for the user. We've already mentioned the <code><strong>animation</strong></code> property earlier in this document. It's actually shorthand for all animation properties, including:</p>

<ul>
	<li><strong><code>animation-play-state</code> </strong></li>
	<li><strong><code>animation-duration</code></strong> has a value of <strong><code>&lt;time&gt;;</code></strong> this is the duration an animation takes to complete one cycle. This may be specified in either seconds <strong><code>(s)</code></strong> or milliseconds <strong><code>(ms)</code>.</strong> A default value of 0s indicates no animation should occur.</li>
	<li><strong><code>animation-timing-function</code></strong></li>
</ul>

<p>The animation property is powerful on its own, of course, but combined with other properties and queries, such as <strong><code>prefers-reduced-motion</code></strong>, a powerful set of options can be set up for the user. Setting <strong><code>animation-duration</code></strong> and <strong><code>transition-duration</code></strong> properties to a short duration rather than setting them to <strong><code>animation: none</code></strong> and <strong><code>transition: none</code></strong>, enables a safeguard to prevent issues in any case there is a dependency on the animation to run</p>

<h3 id="JavaScript_animation">JavaScript animation</h3>

<p>JavaScript is often used to control &lt;canvas&gt; elements and SVGs. Most JavaScript code that applies to HTML5 video also applies to audio. <strong><code>HTMLMediaElement.playbackRate</code></strong> is used to implement user controls for the playback rate for both video and audio. A value of 1.0 is default and considered normal speed; a value of 0.5 is half the speed, a value of 2.0 is twice the speed. A negative number plays the video or audio backwards. Set the playback rate property: <strong><code>HTMLMediaElement.playbackRate = playbackspeed</code></strong></p>

<p><strong><a href="/en-US/docs/Web/API/Document/getAnimations">document.getAnimations()</a></strong> is an experimental technology, and includes <strong><a href="/en-US/docs/Web/CSS/CSS_Animations">CSS Animations</a></strong>, <strong><a href="/en-US/docs/Web/CSS/CSS_Transitions">CSS Transitions</a></strong>, and <strong><a href="/en-US/docs/Web/API/Web_Animations_API">Web Animations</a></strong>. The MDN document, <strong><a href="/en-US/docs/Web/API/Document/getAnimations">Document.getAnimations()</a></strong> provides the following code sample of how to slow down all animations on a page to half speed.</p>

<pre class="brush: js">document.getAnimations().forEach(
  function (animation) {
    animation.playbackRate *= .5;
  }
);
</pre>

<p><strong>Image sources for animation</strong></p>

<p>One of the easiest ways is to start with an image that is already in existence, using it as an image source, and then animating it. Remember, you can use GIFs, JPGs, PNGs, SVGs and other file types here as an image source, as long as they are allowed file types—and sizes—in your environment. SVGs are often not allowed, due to security concerns. The MDN document, <strong><a href="/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_animations">Basic animations</a></strong>, provides outstanding examples of this, using multiple image sources for the sun, earth, and moon, and using several canvas methods to control the speed and animation of the earth as it orbits around the sun, and the moon as it orbits around the earth. Use the codepen available with this tutorial to adjust <code>ctx.rotate</code> in the code to see how the animation is affected when changes are made.</p>

<h4 id="If_you_absolutely_positively_must_use_flashing_animation…">If you absolutely, positively <em>must</em> use flashing animation…</h4>

<p>Make sure it has a control on it. Make sure it is turned off when the viewer first encounters it, and that a user must opt-in to see the animation.</p>

<p>An example of a format that has no controls available to the user is a gif file. Animation speed is controlled within the gif image itself. Converting an animated gif to video enables controls to be put on the animation, and gives the user agency. There are many free online converters available for use, such as <a href="https://ezgif.com/">EZGif</a> and <a href="https://gif-2-mp4.com/">GIF to MP4</a>.</p>

<h4 id="Set_user_expectations"><strong>Set user expectations</strong></h4>

<p>Give users a heads-up as to what will happen <strong>before</strong> they click on that link. Describe the animation that is to follow. See <strong><a href="https://www.w3.org/TR/WCAG21/#change-on-request">WCAG 2.1 Success Criterion 3.2.5 Change on Request</a></strong>.</p>

<h4 id="Keep_it_small">Keep it small</h4>

<p>If you absolutely positively must have flashing, keep it small. Generally speaking, limit the size of the flash to an area approximately 341 by 256 pixels or less. This pixel size assumes that a viewer is at a typical distance from the screen. As mentioned earlier, this size may be too big if the image is to be viewed at close range, such as in a VR headset. WebVR is an open specification that makes it possible to experience VR in your browser. WebVR can be experienced on phone, computer or headset.</p>

<p>If you are designing for a game or VR that uses an ocular mask, <strong>or CAN be used by an ocular mask</strong>, such as in Firefox Reality (a browser for virtual reality), ensure that the size of the rectangle is much smaller than 341 by 256 pixels, because the image is much closer to a user's eyes.</p>

<h4 id="Reduce_contrast">Reduce contrast</h4>

<p>Normally, higher contrast is a good thing when it comes to accessibility. The greater the contrast of a text color to its background (technically called <em>luminosity contrast ratio,</em> according to W3.org's page on <strong><a href="https://www.w3.org/WAI/perspective-videos/contrast/">Colors with Good Contrast</a></strong><em>),</em> the easier such content is to read. Users with low vision are especially appreciative of efforts to ensure high contrast of text against its background. When the content is animated, however, <strong><em>reducing</em></strong> contrast is actually a way to reduce the likelihood that the animated content will cause seizures. Drop the contrast ratio if three flashes within one second are detected.</p>

<p>The contrast ratio is defined in <strong><a href="https://www.w3.org/TR/WCAG21/">WCAG 2.1</a></strong> as follows:</p>

<dl>
	<dt><dfn>contrast ratio</dfn></dt>
	<dd>
	<p>(L1 + 0.05) / (L2 + 0.05), where</p>

	<ul>
		<li>L1 is the <strong><a href="https://www.w3.org/TR/WCAG21/#dfn-relative-luminance">relative luminance</a></strong> of the lighter of the colors, and</li>
		<li>L2 is the <strong><a href="https://www.w3.org/TR/WCAG21/#dfn-relative-luminance">relative luminance</a></strong> of the darker of the colors.</li>
	</ul>
	</dd>
</dl>

<p>It's best if you can adjust the contrast before it is uploaded or published to the web. For videos and animated GIFS, the Adobe Suite of products is a phenomenal resource for traditional images. Also for images, an online tool available is pinetools.com's <strong><a href="https://pinetools.com/brightness-contrast-image">Brightness and contrast online</a></strong>. If you intend to make animated gifs, for example, start with one that has a lower contrast ratio.</p>

<p>JavaScript is also an option for reducing contrast dynamically. Here's a code example from the section titled, "<strong><a href="/en-US/docs/Web/API/Document_Object_Model/Traversing_an_HTML_table_with_JavaScript_and_DOM_Interfaces#setting_background_of_a_paragraph">Example: Setting the background color of a paragraph</a></strong>" from the MDN document, <strong><a href="/en-US/docs/Web/API/Document_Object_Model/Traversing_an_HTML_table_with_JavaScript_and_DOM_Interfaces">Traversing an HTML table with JavaScript and DOM Interfaces</a></strong>. Notice that the color in the example is described in the <strong>RGB</strong> color space.</p>

<p><strong>HTML Content <a href="/en-US/docs/Web/API/Document_Object_Model/Traversing_an_HTML_table_with_JavaScript_and_DOM_Interfaces#html_content_2">(link to source page)</a></strong></p>

<pre class="brush: html">&lt;body&gt;
  &lt;input type="button" value="Set paragraph background color" onclick="set_background()"&gt;
  &lt;p&gt;hi&lt;/p&gt;
  &lt;p&gt;hello&lt;/p&gt;
&lt;/body&gt;</pre>

<p><strong>JavaScript Content <a href="/en-US/docs/Web/API/Document_Object_Model/Traversing_an_HTML_table_with_JavaScript_and_DOM_Interfaces#javascript_content_2">(link to source page)</a></strong></p>

<pre class="brush: js">function set_background() {
  // get a list of all the body elements (there will only be one),
  // and then select the zeroth (or first) such element
  myBody = document.getElementsByTagName(&quot;body&quot;)[0];

  // now, get all the p elements that are descendants of the body
  myBodyElements = myBody.getElementsByTagName(&quot;p&quot;);

  // get the second item of the list of p elements
  myP = myBodyElements[1];
  myP.style.background = &quot;rgb(255,0,0)&quot;;
}
</pre>

<h4 id="Avoid_fully_Saturated_Reds_for_flashing_content">Avoid fully Saturated Reds for flashing content</h4>

<p>As mentioned earlier in this document, the Epilepsy Foundation of America convened a workshop in August 2004 to begin to develop an expert consensus on photosensitive seizures. Among their results was the understanding that "<em>A flash is a potential hazard if it has luminance at least 20 cd/m2 , occurs at a frequency of least 3 Hz, and occupies a solid visual angle of at least 0.006 steradians (about 10% of the central visual field or 25% of screen area at typical viewing distances). A transition to or from saturated red also is considered a risk.</em>" They also note in that same consensus: "<strong>Irrespective of luminance, a transition to or from a saturated red is also considered a risk.</strong>"</p>

<h3 id="Provide_alternative_CSS_styles">Provide alternative CSS styles</h3>

<p>With the understanding that much of animation and flashing can be controlled via CSS methods, it's important to explore ways to make alternative options available to users, and to make the control of these options convenient and visible.</p>

<p><strong>Alternative Style Sheets</strong></p>

<p>Modern browsers will display the alternate CSS available in alternate style sheets if the users know where to look for them. In some cases, the alternate styles are revealed when the users go through the View menu, in other cases they are manifested in the settings, sometimes both. Not all users know to look for these options via the browser or settings, so it's worth considering doing things the old-fashioned way, with obvious buttons or links to change the style so that users can see them. Doing so won't conflict with, or override, the browser's ability to read the alternate style sheets, or the ability of the user to set preferences in the settings.</p>

<p>It's important to know that certain users, such as those who rely on speech-recognition systems, often depend on legacy buttons and links because their disability prevents them from using a mouse, or to be able to take advantage of touch events on mobile tablets.</p>

<p>Common ways to include the alternative stylesheets into your HTML documents are to use the <code><strong>&lt;link&gt;</strong></code> element, and <strong><code>@import</code>.</strong></p>

<p><strong>The <code>&lt;link&gt;</code> element</strong></p>

<p>Use the <strong><code>&lt;link&gt;</code></strong> element, alongside with and together with the attributes of <strong><code>rel="alternate stylesheet"</code></strong> and for title,<strong> <code>title="…"</code></strong> in the <strong><code>&lt;HEAD&gt;</code></strong> section of the webpage.</p>

<pre class="brush: html">&lt;head&gt;
  &lt;title&gt;Home Page&lt;/title&gt;
  &lt;link href="main.css" rel="stylesheet" type="text/css" title="Default Style"&gt;
  &lt;link href="alternate1.css" rel="alternate stylesheet" type="text/css" title="Alternate One"&gt;
  &lt;link href="alternate2.css" rel="alternate stylesheet" type="text/css" title="Alternate Two"&gt;
&lt;/head&gt;</pre>

<p id="sect3">@import</p>

<p><strong><code>@import </code></strong>is also a way to incorporate style sheets, but it is not quite as well supported as the <strong><code>&lt;link&gt;</code></strong> element.</p>

<pre class="brush: html">&lt;STYLE type="text/css"&gt;
  @import url(alternate1.css);
  @import url(alternate2.css);
&lt;/STYLE&gt;</pre>

<p>By using alternate style sheets (remember to add the titles) you are setting it up for users to be able to use their browsers to choose alternate styles.</p>

<h3 id="Dynamic_Style_Switching">Dynamic Style Switching</h3>

<p>One problem with relying on the browser to reveal alternative styles is that not all users are technically savvy enough to discover the alternate styles. Or, because of their disability, are not able to. Buttons or links make it obvious that options are available to many grateful users. There's a multitude of ways to add toggle buttons to allow the user to switch to the different style sheets. That said, the use of alternative style sheets are not the only option. Another option is to manipulate the style of the page itself. According to the MDN document, <strong><a href="/en-US/docs/Web/API/CSS_Object_Model/Using_dynamic_styling_information">Using dynamic styling information</a></strong>, "<em>where possible, it really is best practice to dynamically manipulate classes via the <strong><a href="/en-US/docs/Web/API/Element/className"><code>className</code></a></strong> property since the ultimate appearance of all of the styling hooks can be controlled in a single stylesheet".</em> One of the best examples around as to how to do this is from the W3C's page, <strong><a href="https://www.w3.org/TR/WCAG20-TECHS/C29.html">C29: Using a style switcher to provide a conforming alternate version</a></strong>.</p>

<h3 id="Extreme_Cases_Text-Only_Alternatives">Extreme Cases: Text-Only Alternatives</h3>

<p>A separate, alternative stylesheet that prevents images from being displayed is easy to make. It's a draconian solution; but it is one that is sometimes necessary for school teachers and other public servants who must serve those with extreme sensitivities. These public servants can ask their developers to develop a special alternative style sheet using <strong><code>display:none</code>.</strong> Here's how to do it via CSS:</p>

<pre class="brush: css">img { display:none;}
</pre>

<h4 id="Take_advantage_of_media_queries_with_&lt;style&gt;">Take advantage of media queries with <code>&lt;style&gt;</code></h4>

<p>In setting up media queries, you are enabling controls by the user; these controls are made available in the browser or in the OS. See the MDN document, "<strong><a href="/en-US/docs/Web/Accessibility/Accessibility:_What_users_can_to_to_browse_safely">Accessibility: What users can do to browse more safely</a></strong>" to see more details of how a user accesses the controls.</p>

<h4 id="prefers-reduced-motion"><code>prefers-reduced-motion</code></h4>

<p>Support for prefers-reduced-motion in modern browsers is growing.</p>

<pre class="brush: css">@media screen and (prefers-reduced-motion: reduce) { }
@media screen and (prefers-reduced-motion) { }</pre>

<p>To see a great example of how to use the code <code>prefers-reduced-motion</code>, visit the MDN document, <strong><a href="/en-US/docs/Web/CSS/@media/prefers-reduced-motion">prefers-reduced-motion</a></strong>, or see the example below from the section on <strong><a href="https://developers.google.com/web/updates/2019/04/nic74">New in Chrome 74</a></strong>.</p>

<pre class="brush: css">button {
  animation: vibrate 0.3s linear infinite both;
}

@media (prefers-reduced-motion: reduce) {
  button {
    animation: none;
  }
}
</pre>

<h4 id="prefers-color-scheme"><code>prefers-color-scheme</code></h4>

<p>This can be useful if the ambient light API is not available. Support is emerging.</p>

<pre class="brush: css">@media (prefers-color-scheme: dark) {
    /* adust styles for dark mode */
}</pre>

<h4 id="Window.matchMedia">Window.matchMedia()</h4>

<p>There is a powerful tool available to developers via Window.matchMedia(). A great resource is MDN's document on <strong><a href="/en-US/docs/Web/API/Window/matchMedia">Window.matchMedia()</a></strong></p>

<h4 id="media_update_feature">media update feature</h4>

<p>The more often the screen is refreshed, the more stable it appears to the human eye, and the less it "flickers". The vast majority of modern technology refreshes at a rate that does not cause problems with photosensitivity. However, not everybody is wealthy enough to be able to afford the most recent technology: older or underpowered computers can have low refresh rates. <strong><a href="https://www.abilitynet.org.uk/sites/abilitynet.org.uk/files/Epilepsy%20and%20Computing%20Nov%202015.pdf">AbilityNet's Factsheet (November 2015) Computers and Epilepsy (pdf) </a></strong>describes more of the details on refresh rates.</p>

<p>A very old article, Tech Republic's <strong><a href="https://www.techrepublic.com/forums/discussions/epilepsy-and-crt-lcd-screen-flicker/">Epilepsy and CRT/LCD screen flicker</a></strong>, had an interesting response concerning the refresh rates in Hz.</p>

<ul>
	<li>"This effect is noticeable, and documented, up to 70 Hz."</li>
	<li>"These studies would seem to indicate that you should stay away from refresh rates under 70 Hz, and use a rate not divisible by 10."</li>
</ul>

<p>Eric Bailey, of CSS-Tricks, found an innovative use the update feature which, used in combination with animation-duration or transition-duration, to conclude at a rate that is imperceptible to the human eye. In other words, Eric's techniques address the refresh-rate problem. The CSS below is from the article, <strong><a href="https://css-tricks.com/revisiting-prefers-reduced-motion-the-reduced-motion-media-query/">CSS-TRICKS Revisiting prefers-reduced-motion, the reduced motion media query</a></strong>.</p>

<pre class="brush: css">@media screen and (prefers-reduced-motion: reduce),
(update: slow) {
* { animation-duration: 0.001ms !important;
    animation-iteration-count: 1 !important; /* Hat tip Nick/cssremedy (https://css-tricks.com/revisiting-prefers-reduced-motion-the-reduced-motion-media-query/#comment-1700170) */
    transition-duration: 0.001ms !important;
 }
}</pre>

<p>From W3.org's page on <strong><a href="https://www.w3.org/TR/mediaqueries-4/">Media Queries 4</a></strong>:</p>

<p>The <code><strong><a href="https://www.w3.org/TR/mediaqueries-4/#descdef-media-update" id="ref-for-descdef-media-update②">update</a></strong> </code>media feature is used to query the ability of the output device to modify the appearance of content once it has been rendered. It has the values of "none", "slow", and "fast".</p>

<h2 id="Developmental_Experimental_Features">Developmental &amp; Experimental Features</h2>

<h4 id="MDN_Navigator.doNotTrack"><strong>MDN Navigator.doNotTrack</strong></h4>

<p><strong><a href="/en-US/docs/Web/API/Navigator/doNotTrack">From the documentation</a>: "</strong>Returns the user's do-not-track setting. This is "1" if the user has requested not to be tracked by web sites, content, or advertising"</p>

<h4 id="Media_Queries_Level_5">Media Queries Level 5</h4>

<p>EnvironmentMQ (Planned in Media Queries Level 5)</p>

<dl>
  <dt>light-level</dt>
  <dd>
    <p><a href="https://drafts.csswg.org/mediaqueries-5/#light-level">light-level</a> has three valid values: dim, normal, and washed. Interestingly, the specification refrains from actually defining the three levels in terms of a measurement of lux, because devices with a light sensor usually adjust the brightness of the screen automatically. The specifications also note the difference in technology, such as e-ink, which remains readable in bright daylight, versus liquid crystals, which do not.</p>
  </dd>

  <dt>environment-blending</dt>
  <dd>
    <p>From W3C's Draft document, Media Queries Level 5: "<em>The <strong><a href="https://drafts.csswg.org/mediaqueries-5/#descdef-media-environment-blending">environment-blending</a></strong> media feature is used to query the characteristics of the user’s display so the author can adjust the style of the document. An author might choose to adjust the visuals and/or layout of the page depending on the display technology to increase the appeal or improve legibility</em>."</p>
  </dd>
</dl>

<h5 id="User_Preference_Media_Features_Planned_in_Media_Queries_Level_5">User Preference Media Features (Planned in Media Queries Level 5)</h5>

<p><strong><a href="https://drafts.csswg.org/mediaqueries-5/#mf-user-preferences">User Preference Media Features</a></strong> in <strong><a href="https://drafts.csswg.org/mediaqueries-5/">W3C Editor's Draft Media Queries Level 5</a></strong> are especially promising in providing user control over media. Here are some highlights:</p>
  
  <dl>
    <dt>inverted-colors</dt>
    <dd>
      <p>According to the section, <strong><a href="https://drafts.csswg.org/mediaqueries-5/#mf-user-preferences">User Preference Media Features</a></strong> , "The <strong><a href="https://drafts.csswg.org/mediaqueries-5/#descdef-media-inverted-colors" id="ref-for-descdef-media-inverted-colors①">inverted-colors</a></strong> media feature indicates whether the content is displayed normally, or whether colors have been inverted."</p>
    </dd>

    <dt>forced-colors</dt>
    <dd>
      <p><a href="https://drafts4.csswg.org/mediaqueries-5/#forced-colors">forced-colors</a></p>
      
      <p>In <strong><a href="https://drafts.csswg.org/css-color-adjust-1/#forced-colors-mode">forced-colors-mode</a>,</strong> the user agent enforces the user's preferred color palette on the page, overriding the author's chosen colors.  From W3C's Draft document, Media Queries Level 5 section on forced-colors: "<em>The forced-colors media feature is used to detect if the user agent has enabled a<strong><a href="https://drafts.csswg.org/css-color-adjust-1/#forced-colors-mode"> forced colors mode</a></strong> where it enforces a user-chosen limited color palette on the page</em>". The user will need to be made aware of this ability, and it will need to play nice with the appropriate value for the prefers-color-scheme media query.</p>
    </dd>

    <dt>light-level</dt>
    <dd>
      <p>From W3C's Draft document, Media Queries Level 5 section on light-level: "<em>The <code><strong><a href="https://drafts.csswg.org/mediaqueries-5/#descdef-media-light-level" id="ref-for-descdef-media-light-level①">light-level</a></strong></code> media feature is used to query about the ambient light-level in which the device is used, to allow the author to adjust style of the document in response</em>." This will be a godsend to those who have motor-skills problems, or for some with cognitive difficulties, who cannot find the right "button" to change their screen settings.</p>

      <dt>prefers-contrast</dt>
      <dd>
        <p>From W3C's Draft document, Media Queries Level 5 section on <a href="https://drafts4.csswg.org/mediaqueries-5/#prefers-contrast"><code><strong>prefers-contrast</strong></code></a>: "<em>The <strong><code>prefers-contrast</code></strong> media feature is used to detect if the user has requested the system increase or decrease the amount of contrast between adjacent colors. For example, many users have difficulty reading text that has a small difference in contrast to the text background and would prefer a larger contrast.</em>" Sometimes there can be such a thing as too much contrast; a halo effect around text can occur in such situations and actually reduce legibility. Putting the amount of contrast in the user's control is a definite gift for accessibility.</p>
      </dd>
  </dl>

<h4 id="MediaQueryList_Interface"><code>MediaQueryList</code> Interface</h4>

<p>Section 4.2 from the CSSWG.org drafts integrates with the <strong><a href="https://html.spec.whatwg.org/multipage/webappapis.html#event-loop" id="ref-for-event-loop">event loop</a></strong> defined in HTML. <strong><a href="https://drafts.csswg.org/cssom-view/#biblio-html">[HTML]</a></strong> for the <strong><code><a href="https://drafts.csswg.org/cssom-view/#mediaquerylist" id="ref-for-mediaquerylist③">MediaQueryList</a></code></strong> object. See the MDN document, <strong><a href="/en-US/docs/Web/API/MediaQueryList">MediaQueryList</a></strong> for more information.</p>

<h4 id="Personalization_Help_and_Support">Personalization Help and Support</h4>

<p>The requirement for the <code>literal </code>property is taken from <strong><a href="https://www.w3.org/TR/personalization-semantics-help-1.0/">section 23 Non-literal Text and Images</a></strong></p>

<p><strong>Requirement:</strong> Some users cannot understand non-literal text and icons such as metaphors, idioms etc. The <code>literal</code> property is intended to identify text or images as non-literal and allows the author to explain non-literal text and images to users.</p>

<h4 id="Transitions_for_CSS_and_SVG">Transitions (for CSS and SVG)</h4>

<p>The following is from the <strong><a href="https://www.w3.org/TR/web-animations-1/">Web Animations model</a></strong> CSSWG.org drafts</p>

<p>The Web Animations model is intended to provide the features necessary for expressing CSS Transitions <strong><a href="https://drafts.csswg.org/web-animations/#biblio-css-transitions-1">[CSS-TRANSITIONS-1]</a></strong>, CSS Animations <strong><a href="https://drafts.csswg.org/web-animations/#biblio-css-animations-1">[CSS-ANIMATIONS-1]</a></strong>, and SVG <strong><a href="https://drafts.csswg.org/web-animations/#biblio-svg11">[SVG11]</a></strong>.</p>

<h2 id="See_also">See also</h2>

<h4 id="MDN">MDN</h4>

<ul>
	<li><a href="/en-US/docs/Web/Accessibility/Accessibility:_What_users_can_to_to_browse_safely">Accessibility: What users can do to browse more safely</a></li>
	<li><a href="/en-US/docs/Web/Accessibility/Understanding_Colors_and_Luminance">Accessibility: Understanding color and luminance</a></li>
	<li><a href="/en-US/docs/Web/SVG/Applying_SVG_effects_to_HTML_content">Applying SVG effects to HTML Content</a></li>
	<li><a href="/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_animations">Basic Animations</a> (Canvas Tutorial)</li>
	<li><a href="/en-US/docs/Web/API/Canvas_API">Canvas API</a></li>
	<li><a href="/en-US/docs/Web/API/CanvasRenderingContext2D/drawImage">CanvasRenderingContext2D.drawImage()</a></li>
	<li><a href="/en-US/docs/Web/CSS/color_value">&lt;color&gt;</a></li>
	<li><a href="/en-US/docs/Web/API/Document_Object_Model">Document Object Model</a></li>
	<li><a href="/en-US/docs/Web/API/MediaQueryList">MediaQueryList</a></li>
	<li><a href="/en-US/docs/Web/API/CSS_Object_Model/Using_dynamic_styling_information">Using dynamic styling information</a></li>
	<li><a href="/en-US/docs/Web/API/WebGL_API">WebGL: 2D and 3D graphics for the web</a></li>
	<li><a href="/en-US/docs/Web/API/WebVR_API">WebVR API</a></li>
</ul>

<h4 id="Color">Color</h4>

<ul>
	<li><a href="https://colortutorial.design/">Color Tutorial: describing color</a> Tom Jewett.</li>
	<li><a href="https://stackoverflow.com/questions/596216/formula-to-determine-brightness-of-rgb-color">Formula to Determine Brightness of RGB color</a> Stack Exchange Discussion Thread</li>
	<li><a href="https://www.scientificamerican.com/article/how-the-color-red-influences-our-behavior/">How the Color Red Influences Our Behavior</a> Scientific American By Susana Martinez-Conde, Stephen L. Macknik on <time datetime="2014-11-01">November 1, 2014</time></li>
</ul>

<h4 id="Discussions">Discussions</h4>

<ul>
	<li><a href="https://github.com/w3c/wcag/issues/553">Problems with WCAG 2.0 Flash Definition #553</a></li>
	<li><a href="https://github.com/w3c/wcag/issues/585">WCAG 2.1 Understanding 2.3.1 - missing/vague dimension definitions #585</a></li>
	<li>
	<h4 id="Epilepsy_and_Seizures">Epilepsy and Seizures</h4>
	</li>
	<li><a href="https://www.epilepsy.com/article/2014/3/shedding-light-photosensitivity-one-epilepsys-most-complex-conditions-0">Shedding Light on Photosensitivity, One of Epilepsy's Most Complex Conditions</a> Epilepsy Foundation <em>Certain individuals are born with special sensitivity to flashing lights or contrasting visual patterns, such as stripes, grids and checkerboards. Because of this condition, their brain will produce seizure-like discharges when exposed to this type of visual stimulation</em></li>
	<li><a href="https://www.sciencedirect.com/science/article/pii/S0960982217304062?via%3Dihub">Gamma oscillations and photosensitive epilepsy</a> Current Biology <a href="https://www.sciencedirect.com/science/journal/09609822/27/9">Volume 27, Issue 9</a>, 8 May 2017, Pages R336-R338 <em>Certain <a href="https://www.sciencedirect.com/topics/biochemistry-genetics-and-molecular-biology/retina-image">visual images</a>, even in the absence of <a href="https://www.sciencedirect.com/topics/biochemistry-genetics-and-molecular-biology/motion">motion</a> or flicker, can trigger seizures in patients with photosensitive epilepsy.</em></li>
	<li><a href="https://www.cedars-sinai.edu/Patients/Health-Conditions/Photosensitive-Seizures.aspx">Photosensitive Seizures. Cedars-Sinai</a> "<em>Photosensitive seizures are triggered by flashing or flickering lights. These seizures can also be triggered by certain patterns such as stripes.</em>"</li>
	<li><a href="https://www.ncbi.nlm.nih.gov/pubmed/16146438">Photic-and pattern-induced seizures: expert consensus of the Epilepsy Foundation of America Working Group</a>. Eplepsia 2005 Sept, 46(9):1423-5 PubMed.gov NCBI <a href="https://www.ncbi.nlm.nih.gov/pubmed/?term=Harding%20G%5BAuthor%5D&amp;cauthor=true&amp;cauthor_uid=16146438">Harding G</a><sup>1</sup>, <a href="https://www.ncbi.nlm.nih.gov/pubmed/?term=Wilkins%20AJ%5BAuthor%5D&amp;cauthor=true&amp;cauthor_uid=16146438">Wilkins AJ</a>, <a href="https://www.ncbi.nlm.nih.gov/pubmed/?term=Erba%20G%5BAuthor%5D&amp;cauthor=true&amp;cauthor_uid=16146438">Erba G</a>, <a href="https://www.ncbi.nlm.nih.gov/pubmed/?term=Barkley%20GL%5BAuthor%5D&amp;cauthor=true&amp;cauthor_uid=16146438">Barkley GL</a>, <a href="https://www.ncbi.nlm.nih.gov/pubmed/?term=Fisher%20RS%5BAuthor%5D&amp;cauthor=true&amp;cauthor_uid=16146438">Fisher RS</a>; <a href="https://www.ncbi.nlm.nih.gov/pubmed/?term=Epilepsy%20Foundation%20of%20America%20Working%20Group%5BCorporate%20Author%5D">Epilepsy Foundation of America Working Group</a>.</li>
</ul>

<h4 id="GPII">GPII</h4>

<ul>
	<li><a href="https://ds.gpii.net/learn/accessibility-masterlist">Accessibility Master List</a> Gregg Vanderheiden Ph.D. Editor</li>
</ul>

<h4 id="Harding">Harding</h4>

<p>Along with the PEAT tool, is generally recognized to be one of the two "gold standards" for analyzing flashes</p>

<ul>
	<li><a href="https://www.hardingfpa.com">Harding Flash and Pattern Analyzer</a></li>
</ul>

<h4 id="ISO">ISO</h4>

<ul>
	<li><a href="https://www.iso.org/obp/ui/#iso:std:iec:61966:-2-2:ed-1:v1:en">IEC 61966-2-2:2003(en)</a> Multimedia systems and equipment — Colour measurement and management — Part 2-2: Colour management — Extended RGB color space — scRGB</li>
</ul>

<h4 id="Photosensitive_Epilepsy_Analysis_Tool">Photosensitive Epilepsy Analysis Tool</h4>

<p>Along with the Harding tool, is generally recognized to be one of the two "gold standards" for analyzing flashes</p>

<ul>
	<li><a href="https://trace.umd.edu/peat">Trace Research and Development Center</a></li>
	<li><a href="https://www.useragentman.com/blog/2017/04/02/using-peat-to-create-seizureless-web-animations/">Using PEAT To Create Seizureless Web Animations</a></li>
</ul>

<h4 id="W3C">W3C</h4>

<ul>
	<li><a href="https://www.w3.org/TR/css-color-3/">CSS Color Module Level 3</a></li>
	<li><a href="https://www.w3.org/TR/personalization-semantics-1.0/">Personalization Semantics Explainer 1.0</a>. Working Draft</li>
	<li><a href="https://www.w3.org/TR/2019/WD-personalization-semantics-tools-1.0-20190711/">Personalization Tools 1.0</a> Working Draft</li>
	<li><a href="https://www.w3.org/TR/UNDERSTANDING-WCAG20/seizure-does-not-violate.html">Three Flashes or Below Threshold Understanding SC 2.3.1</a> Understanding WCAG 2.0 (Older, but contains some explanations of references made in the WCAG 2.1 criteria)</li>
	<li><a href="https://www.w3.org/WAI/WCAG21/Understanding/three-flashes-or-below-threshold.html">Three Flashes or Below Threshold Understanding Success Criterion 2.3.1</a> Understanding WCAG 2.1</li>
	<li><a href="https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum.html">Understanding Success Criteria 1.4.3: Contrast (Minimum)</a></li>
	<li><a href="https://www.w3.org/WAI/">Web Accessibility Initiative (WAI)</a></li>
	<li><a href="https://www.w3.org/TR/web-animations-1/">Web Animations Mode</a>l W3C Working Draft</li>
	<li><a href="https://www.w3.org/TR/WCAG20/#relativeluminancedef">Web Content Accessibility Guidelines (WCAG) 2.0</a> definition of relative luminance</li>
	<li><a href="https://www.w3.org/TR/WCAG21/">Web Content Accessibility Guidelines (WCAG) 2.1</a></li>
</ul>

<h2 id="Contributors">Contributors:</h2>

<p>Heartfelt thanks to Teal; Wayne Dick of the <a href="https://www.w3.org/WAI/GL/low-vision-a11y-tf/">Low Vision Task Force of the W3C</a>; Tom Jewett and Eric Eggert from <a href="https://knowbility.org/">Knowbility;</a> Jim Allan of the <a href="https://diagramcenter.org/">Diagram Center;</a> and Dr. Selim R. Benbadis, Director, <a href="https://health.usf.edu/medicine/neurology/epilepsy">Comprehensive Epilepsy Program and Clinical Neurophysiology Laboratory at USF and TGH in Tampa, Florida</a> for their great, great assistance and discussions on this topic.</p>

<p>We are <em>all</em> in tremendous gratitude to the Trace Research &amp; Development Center for making their amazing tool, the <a href="https://trace.umd.edu/peat">Photosensitive Epilepsy Analysis Tool (PEAT)</a> for free.</p>