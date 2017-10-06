Questa è la traduzione dell’articolo <a href="https://blog.mozilla.org/blog/2017/09/26/firefox-quantum-beta-developer-edition/" target="_blank">Start Your Engines – Firefox Quantum Lands in Beta, Developer Edition</a> pubblicato da <a href="https://blog.mozilla.org/blog/author/nnguyenmozillacom/">Nick Nguyen</a> per il blog Mozilla.
Traduttore: <a href="https://www.mozillaitalia.org">Nome e cognome/nick/a scelta</a>


<h1>Start Your Engines – Firefox Quantum Lands in Beta, Developer Edition</h1>


Engines are important, both in cars and in browsers. That’s why we’re so revved up this morning – we’re releasing the Beta of a whole new Firefox, one that’s powered by a completely reinvented, modernized engine. Since the version number – 57 – can’t really convey the magnitude of the changes we’ve made, and how much faster this new Firefox is, we’re calling this upcoming release <a href="https://www.mozilla.org/firefox/quantum">Firefox Quantum</a>.

<h4>The journey to Firefox Quantum</h4>

Last October we announced <a href="https://medium.com/mozilla-tech/a-quantum-leap-for-the-web-a3b7174b3c12">Project Quantum</a>, our effort to create a next-generation engine for modern computers, by leveraging technology from our <a href="http://www.servo.org">Servo research project</a>. Since then, our engineering team has been relentless in their focus on making Firefox incredibly fast. 
Already this year we’ve launched several major improvements to Firefox that have it made it better than ever. For example, we’ve transformed Firefox to run using multiple processes, <a href="https://medium.com/mozilla-tech/the-search-for-the-goldilocks-browser-and-why-firefox-may-be-just-right-for-you-1f520506aa35">striking the “just right” balance between speed and memory usage</a>. In addition, we’ve launched game-changing features like <a href="https://medium.com/mozilla-tech/why-webassembly-is-a-game-changer-for-the-web-and-a-source-of-pride-for-mozilla-and-firefox-dda80e4c43cb">WebAssembly</a> and <a href="https://medium.com/mozilla-tech/webvr-shipping-today-in-firefox-d54d490a2072">WebVR</a>, enabling super fast, near-native performance for web apps on the desktop and on VR headsets. 
We’ve shipped a lot already, but we’ve been planning for many more projects to come together in Firefox Quantum. 


<h4>Noticeably faster on many of the top websites</h4>

Firefox Quantum is such a big leap forward that you’ll feel it instantly, just browsing your favorite websites. 
Turns out you can measure Firefox Quantum’s speed, too – our pit crew is kind of <a href="https://hacks.mozilla.org/2017/06/designing-for-performance-a-data-informed-approach-for-quantum-development/">obsessed with a data-driven approach</a>. One simple way of estimating browser performance is with <a href="https://mozilla.github.io/arewefastyet-speedometer/2.0//">Speedometer 2.0</a>, a (still-in-development) benchmark that simulates modern web applications. Results vary based on the computer and apps you’re actively using, but one thing that’s relatively consistent is that <a href="https://blog.mozilla.org/firefox/quantum-performance-test/">Firefox Quantum is about 2X faster</a> than Firefox was a year ago. 

<img class="size-large wp-image-10855 alignnone" src="https://ffp4g1ylyit3jdyti1hqcvtb-wpengine.netdna-ssl.com/wp-content/uploads/2017/09/Firefox-Quantum-is-2x-faster-600x321.png" alt="" width="600" height="321" srcset="https://blog.mozilla.org/wp-content/uploads/2017/09/Firefox-Quantum-is-2x-faster-600x321.png 600w, https://blog.mozilla.org/wp-content/uploads/2017/09/Firefox-Quantum-is-2x-faster-300x160.png 300w, https://blog.mozilla.org/wp-content/uploads/2017/09/Firefox-Quantum-is-2x-faster-768x411.png 768w, https://blog.mozilla.org/wp-content/uploads/2017/09/Firefox-Quantum-is-2x-faster-1000x535.png 1000w" sizes="(max-width: 600px) 100vw, 600px" /> 
We encourage you to make your own comparisons, but here’s a short video that captures our observations when comparing Firefox Quantum and Chrome on various websites. Firefox Quantum is often perceivably faster. 

https://www.youtube.com/embed/YIywpvHewc0

<em>Webpagetest running on Acer Aspire E15. Performance varies based on several factors.</em> 



<h4>So how we did we make Firefox Quantum so fast?</h4>
Firefox has historically run mostly on just one CPU core, but Firefox Quantum takes advantage of multiple CPU cores in today’s desktop and mobile devices much more effectively. This improved utilization of your computer’s hardware makes Firefox Quantum dramatically faster. One example: we’ve developed a breakthrough approach to laying out pages: a<a href="https://hacks.mozilla.org/2017/08/inside-a-super-fast-css-engine-quantum-css-aka-stylo/"> super fast CSS engine</a> written in <a href="http://www.rust-lang.org">Rust</a>, a systems programming language that Mozilla pioneered. Firefox’s new CSS engine runs quickly, in parallel across multiple CPU cores, instead of running in one slower sequence on a single core. No other browser can do this. 
We’ve also improved Firefox so that the tab you’re actively using downloads and runs before other tabs you have open in the background. This prioritization of your active tab, along with<a href="https://medium.com/mozilla-tech/the-search-for-the-goldilocks-browser-and-why-firefox-may-be-just-right-for-you-1f520506aa35"> Firefox&#8217;s “just right” multi-process architecture</a>, results in Firefox Quantum often being faster than Chrome, while consuming roughly 30% less RAM. 
In addition, for the past several months we’ve run a browser-wide initiative to zap any instances of slowness you might encounter while using Firefox. So far our pit crew has fixed 468 of these issues, both small papercuts and big bottlenecks. 

&nbsp; 

<h4>Introducing the fast and fluid Photon design</h4>

It’s not enough to perform well on benchmarks, it’s also important that our users feel like they’re using a well thought out and high performance product.  To reflect all these under-the-hood improvements, we’ve refined and rebuilt Firefox’s user interface through our<a href="https://www.youtube.com/watch?v=tJG278nX6dM"> Photon project</a>. Our talented team of designers and user researchers spent time understanding how users perceive web browsers, and in particular where they felt they were waiting on their browsers. 
With the new design, Firefox leaps ahead with a new interface that reflects today’s reality of High DPI displays and users who are more task focused than they’ve ever been. We’re confident that with Photon, Firefox Quantum users will be impressed by the modern new design that puts their needs first. Photon doesn’t just look good, it’s also smarter. If you’re using Photon on a Windows PC with a touch display, the menus change size based on whether you click with a mouse or touch with a finger. 
The new, minimalist design introduces square tabs, smooth animations, and a Library, which provides quick access to your saved stuff: bookmarks, Pocket, history, downloads, tabs, and screenshots. Firefox Quantum feels right at home with today’s mouse and touch-driven operating systems: Windows 10, macOS High Sierra, Android Oreo, and iOS 11. 

<div style="width: 940px;" class="wp-video"><!--[if lt IE 9]><script>document.createElement('video');</script><![endif]-->
<video class="wp-video-shortcode" id="video-10833-1" width="940" height="510" loop="1" autoplay="1" preload="metadata" controls="controls"><source type="video/webm" src="https://ffp4g1ylyit3jdyti1hqcvtb-wpengine.netdna-ssl.com/wp-content/uploads/2017/09/Firefox-Quantum-Photon-UI-2.webm?_=1" /><a href="https://ffp4g1ylyit3jdyti1hqcvtb-wpengine.netdna-ssl.com/wp-content/uploads/2017/09/Firefox-Quantum-Photon-UI-2.webm">https://blog.mozilla.org/wp-content/uploads/2017/09/Firefox-Quantum-Photon-UI-2.webm</a></video>
</div>




<h4>Pocket built-in</h4>

Firefox Quantum enhances Firefox’s integration with<a href="https://getpocket.com/"> Pocket</a>, the read-it-later app that Mozilla acquired last year. When you open a new tab, you’ll see currently trending web pages recommended by Pocket users so you won’t miss out on what’s hot online, as well as your top sites. With the<a href="https://itunes.apple.com/us/app/pocket-save-articles-and-videos-to-view-later/id309601447?mt=8"> Pocket app for iOS</a> and<a href="https://play.google.com/store/apps/details?id=com.ideashower.readitlater.pro"> Android</a>, you’ll have offline access to your saved stories wherever you go. 
&nbsp; 

<div style="width: 940px;" class="wp-video"><video class="wp-video-shortcode" id="video-10833-2" width="940" height="510" loop="1" autoplay="1" preload="metadata" controls="controls"><source type="video/webm" src="https://ffp4g1ylyit3jdyti1hqcvtb-wpengine.netdna-ssl.com/wp-content/uploads/2017/09/Firefox-Quantum-integrates-Pocket.webm?_=2" /><a href="https://ffp4g1ylyit3jdyti1hqcvtb-wpengine.netdna-ssl.com/wp-content/uploads/2017/09/Firefox-Quantum-integrates-Pocket.webm">https://blog.mozilla.org/wp-content/uploads/2017/09/Firefox-Quantum-integrates-Pocket.webm</a></video></div>

&nbsp; 

<h4>Upgrade to Firefox Quantum soon, or download the Beta today</h4>

If you’re already among the Firefox faithful, you’ll automatically upgrade to Firefox Quantum on November 14. But, if you enjoy the cutting edge, you can<a href="https://www.mozilla.org/en-US/firefox/channel/desktop/#beta"> try it in Beta on desktop</a>,<a href="https://play.google.com/store/apps/details?id=org.mozilla.firefox_beta"> Android</a>, and<a href="https://www.mozilla.org/en-US/firefox/channel/ios/"> iOS</a>. Or, if you’re a web developer,<a href="https://www.mozilla.org/en-US/firefox/developer/"> download Developer Edition</a>, which includes brand new, cutting-edge tools for those who build the web. 
So much has changed about Firefox these past few years, and even more is in store. To learn more about Firefox Quantum in November, visit our <a href="https://www.mozilla.org/firefox/quantum">page</a> and we’ll keep you up to date on the latest news. 
We’re super excited to get Firefox Quantum to our beta users and hope you’ll give it a try. 

