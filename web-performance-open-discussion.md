# Web Performance - Open Discussion

### Date: 17.07.2018
### Venue: Garmin
### Description:
Join us for a final tech meetup before the summer social event!

This time we'll tackle multiple perspective in this open discussion about optimizations and trade-offs in web performance.

Make sure we'll cover things like:
* The critical rendering path
* Browser hints and optimization techniques
* JavaScript loading and execution times
* Image optimizations
* Reducing the size of your app
* Rendering at 60fps
* Tools and platforms

### Meeting notes:
#### Critical Rendering Path:
* Which are the critical resources
* How we can use [`async` and `defer`](http://www.growingwiththeweb.com/2014/02/async-vs-defer-attributes.html) to remove JS from the critical path
* Using [resource hints](https://developer.mozilla.org/en-US/docs/Web/HTML/Preloading_content) to preload critical resources
* Inline critical css if possible - https://jonassebastianohlsson.com/criticalpathcssgenerator/

#### Limit the size of the JS bundles
* Minify + Gzip + Code Split (using dynamic imports in webpack)
* For React try https://github.com/jamiebuilds/react-loadable
* Leverage tree-shaking

#### Image optimizations
* Use the [picture element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture) to load different modern encodings (webp, mozjpeg, etc.)
* Use srcset to specify [responsive images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)
* Try out [lazysizes](https://github.com/aFarkas/lazysizes) for lazy loading offscreen images
* A great ebook by Addy Osmani - https://images.guide/

#### Tools
* Chrome DevTools (including the Audit tab - [Lighthouse](https://developers.google.com/web/tools/lighthouse/)
* https://webpagetest.org/
* https://gtmetrix.com/
* https://github.com/webpack-contrib/webpack-bundle-analyzer
* https://github.com/wix/import-cost

#### The RAIL model and rendering at 60fps
* [More about Response, Animation, Idle, Load](https://developers.google.com/web/fundamentals/performance/rail)
* Favor css animations based on [opacity and transforms](https://developers.google.com/web/fundamentals/performance/rendering/) to enable fast GPU driven animations

#### Creating a Performance Culture at work
* Educate people
* Visualize performance costs
* Enforce performance metrics with tools

#### Literature
- [High Performance Browser Networking by ILYA GRIGORIK](https://hpbn.co/)
