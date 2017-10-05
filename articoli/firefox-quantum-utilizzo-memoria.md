Questa è la traduzione dell’articolo <a href="http://www.erahm.org/2017/09/25/firefox-memory-usage-in-the-quantum-era/" target="_blank">Firefox Memory Usage in the Quantum Era</a> pubblicato sul blog di Eric Rahm.
Traduttore: <a href="https://www.mozillaitalia.org">Nome e cognome/nick/a scelta</a>


<h1>Firefox Memory Usage in the Quantum Era</h1>

	
		This is a continuation of my <em>Are They Slim Yet</em> series. For background see my <a href="firefox-memory-usage-with-multiple-content-processes">previous installment</a>.
Firefox’s upcoming release 57 has a huge focus on performance. We’ve <a href="https://wiki.mozilla.org/Quantum">quantum-ed all the things</a> but we haven’t really talked about memory usage, which is something that often falls by the wayside in the pursuit of performance. Luckily since we brought <a href="are-we-slim-yet-is-dead-all-hail-are-we-slim-yet">AWSY in tree</a> it’s been pretty easy to track memory usage and regressions even <a href="https://bugzilla.mozilla.org/show_bug.cgi?id=1378526">on separate development branches</a>. The Stylo team was a big user of this and it shows, we flipped the switch to enable Stylo by default around the 7th and you can see a fairly large regression, but by the 16th it was mostly gone:

<img src="https://i1.wp.com/www.erahm.org/wp-content/uploads/2017/09/Screenshot-2017-9-26-Explicit-Memory-summary-opt-stylo-disabled-linux64-stylo-disabled-mozilla-central-and-others.png?resize=660%2C451" alt="" class="aligncenter size-full wp-image-187" srcset="https://i1.wp.com/www.erahm.org/wp-content/uploads/2017/09/Screenshot-2017-9-26-Explicit-Memory-summary-opt-stylo-disabled-linux64-stylo-disabled-mozilla-central-and-others.png?w=857 857w, https://i1.wp.com/www.erahm.org/wp-content/uploads/2017/09/Screenshot-2017-9-26-Explicit-Memory-summary-opt-stylo-disabled-linux64-stylo-disabled-mozilla-central-and-others.png?resize=300%2C205 300w, https://i1.wp.com/www.erahm.org/wp-content/uploads/2017/09/Screenshot-2017-9-26-Explicit-Memory-summary-opt-stylo-disabled-linux64-stylo-disabled-mozilla-central-and-others.png?resize=768%2C524 768w" sizes="(max-width: 660px) 100vw, 660px" data-recalc-dims="1" />


https://twitter.com/nnethercote/status/908838175891611648

Hopefully I’ve convinced you we’ve put a lot of work into performance, now let’s see how we’re doing memory-wise compared to other browsers.
The <a href="are-they-slim-yet-round-2">methodology for the test</a> is the same as previous runs: I used the <a href="https://github.com/EricRahm/atsy">ATSY project</a> to load 30 pages and measure memory usage of the various processes that each browser spawns during that time.
<h3>The results</h3>

<figure id="attachment_181" style="width: 600px" class="wp-caption aligncenter"><img src="https://i2.wp.com/www.erahm.org/wp-content/uploads/2017/09/chart1.png?resize=600%2C371" alt="Browser Memory Usage." class="size-full wp-image-181" srcset="https://i2.wp.com/www.erahm.org/wp-content/uploads/2017/09/chart1.png?w=600 600w, https://i2.wp.com/www.erahm.org/wp-content/uploads/2017/09/chart1.png?resize=300%2C186 300w" sizes="(max-width: 600px) 100vw, 600px" data-recalc-dims="1" /><figcaption class="wp-caption-text">Memory usage of browsers across operating systems.</figcaption></figure>

Edge has the highest memory usage on Windows, Chrome comes in with 1.4X the memory usage of Firefox 64-bit on Windows, about 2X Firefox on Linux. On macOS Safari is now by far the worst offender in memory usage, Chrome and Firefox are about even with Firefox memory usage having gone up a fair amount since the last time I measured.
Overall I’m pretty happy with where we’re at, but now that our big performance push is over I’d like to see us focus more on dropping memory usage so we can start pushing up the number of content processes. I’d also like to take a closer look into what’s going on on macOS as that’s been our biggest regression.
Browsers included are Edge 38 on Windows 10, <a href="https://www.google.com/chrome/browser/beta.html">Chrome Beta 62</a> on all platforms, <a href="https://www.mozilla.org/firefox/channel/desktop/">Firefox Beta 57</a> on all platforms, and <a href="https://developer.apple.com/safari/technology-preview/">Safari Technology Preview 40</a> on macOS 10.12.6.
<em>Note: I had to run the test for Safari manually again, they seem to have made some changes that cause all of the pages from my test to be loaded in the same content process.</em>
