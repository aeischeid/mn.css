# MN-CSS

the name: MN because Minnesota is both a cool place and where the devs making this live - Also mn is short, and works as a shortened version of 'minimalist', which is a good descriptor of the philosophy this project intends to embrace.

## Status
Very Very much a work in progress!

The inspirations:
- https://www.youtube.com/watch?v=nhbYveaV0pk 
- https://sqvrltastic.art/guides/animating-details-element-with-css/
- https://moderncss.dev/
- https://modern-css.com/
- https://css-tricks.com/is-it-time-to-un-sass/
- https://una.im/contrast-color

The prior art:
- pico.css https://picocss.com/
- https://github.com/kevquirk/simple.css
- water.css https://watercss.kognise.dev/
- missing.style https://missing.style/
- milligram https://milligram.io/
- mini.css https://minicss.us/docs.htm
- bolt.css https://boltcss.com/
- dev.css https://tangled.org/devins.page/dev.css
- https://github.com/DigitallyTailored/Classless.css?tab=readme-ov-file
- https://andybrewer.github.io/mvp/mvp.html
- https://smolcss.dev/
- https://matcha.mizu.sh/

beyond mere classless libs
- DaisyUI https://daisyui.com/
- Shadcn-classless https://nandaleio.github.io/shadcn-classless/#introdution
- Materialize https://materializecss.com/typography.html
- WebAwesome with Native https://webawesome.com/docs/utilities/native/

Overwhelming meta list of others: 
- https://github.com/dbohdan/classless-css 
- https://dohliam.github.io/dropin-minimal-css/


### Goals: 
In the past many UI libraries and FE styling tools and tool chains have treated CSS as a problem to be solved, and fair enough, in the past CSS had many rough edges, but modern CSS has addressed many of those pain points, and by-in-large the ecosystem has failed to move past the entrenched thinking. CSS-modules, Emotion/css-in-js, and Tailwind are all opinionated [leaky abstractions](https://jakelazaroff.com/words/tailwind-is-a-leaky-abstraction/) that have a [real cost](https://glazkov.com/2022/02/23/the-cost-of-opinion/) associated with them.

Many projects exist to help educate developers, but a library that unifies the concepts of modern CSS, the simplicity of classless CSS, and the composability and ergonomics of atomic-css seems to be somewhat of a gap at the moment. Additionally, some of the accessibility and theme-ability available with modern CSS is not something many existing libraries are taking full advantage of, and to be fair a lot of it has only really landed or been polished enough through things like [the interop project](https://wpt.fyi/interop-2026) in the last couple years.

Beyond direct tooling, conventions like [BEM](https://getbem.com/introduction/) aimed to bring sanity, but at scale (wether project size or team size) such solutions had their own challenges. [Atomic CSS](https://css-tricks.com/lets-define-exactly-atomic-css/) was another one of these conventions. Though Tailwind takes that atomic utility classes idea to an unhealthy extreme, inheriting most of the problems that had developers move away from inline styles in the first place, I do think with some minor discipline and discretion the atomic-css convention works, and can scale well in my experience.

MN.css aims to be a more modern approach than Pico.css - to [Un-Sass-ify](https://css-tricks.com/is-it-time-to-un-sass/) it with a more modern CSS syntax approach, in some ways like Water.css but including more and deeper styles than water. MN.css also aims to be less complex, and quite a bit less ambitious, than for example DaisyUI, but importantly without any reliance on heavy and dare I say CSS hostile dependencies like Tailwind. Maybe closer to [Bootstrap](https://getbootstrap.com/) or [Bulma](https://bulma.io/), but more classless, more lightweight and no build tools required. I think we could get to something beyond the ambition of many classless CSS libs without getting bloated, and if we're setting it up so that extending and customizing can be achieved simply by removing or modifying some component parts, such that a no tooling at all is needed or even encouraged maybe it encourages using CSS itself rather than outsourcing styles to a framework/library that folks are reluctant to 'eject' from.  

### Un-tooling.

Not just Sass, but Tailwind, UnoCSS, and many such tools are all so complicated - often with a goal of shipping less CSS which is great in theory, but when most pages are shipping dozens of megabytes of JS, a few extra KB of CSS is hardly a top concern, all the more considering the opportunity CSS has with [modern dictionary compression](https://httptoolkit.com/blog/dictionary-compression-performance-zstd-brotli/). All things considered a slightly larger, but highly cachable core bundle of CSS might be preferable.

A thing I really appreciated about the Svelte project early on was how they were trying to revive jQuery's "write less; do more" approach. MN.css is maybe aiming to bring that to CSS in a way that also doesn't add a single dependency to your project. With a bit of atomic utilities, on top of some classless CSS, and some basic CSS componentization/compartimentalization, this can be achieved with NO BUILD tool, no distribution stack, just a small collection of text files that can be copied, and then modified without fear. 

One outcome I personally would hope for is that unlike the aesthetic flattening or homogenizing effects that Bootstrap or MaterialUI or other design systems have had on the web, where developers maybe changed a few theme colors but left almost everything else alone, this library would actually encourage a renewed diversity in design. Maybe that is overly optimistic, but in my experience the level of abstraction of these design system implementations brought a level of fear; where actual customization was avoided for multiple reasons, including having to learn and incorporate the whole build tool pipeline of the project to accomplish it, or how it would likely make it hard to upgrade to a future version or some-such. No build tool and no official distribution channel or even versioning/releases might seem like an odd choice for a modern library, but in that it encourages you to take it and make it your own - actually for real - I think it aligns with the projects goals, and follows the spirit of [html5 boilerplate project](https://html5boilerplate.com/)

To assist in developing mn.css itself, a config file for [Biome](https://biomejs.dev/) is in place, and `bunx serve .` works great as an alternative to just using the `file://` protocol in the browser - though that is a perfect valid approach as well. Tools like Playwright have some potential for adding a level of testing rigor that many CSS libraries often lack. But, so far nothing is in place for visual regression testing.

## A note on "AI"

In the era of LLM developer tools many training data sets are built around established or legacy approaches - with a risk of further entrenching them. And some web developers may ask why even bother learning CSS, much less modern CSS, when LLMs will happily pump out the unwieldy strings of class names, and Linters + Tailwind will clean a lot of it up for you after the fact, but before it ships. 

Are we solving a non-problem? 

Putting the capabilities or ethics of LLMs mostly aside, I can see the value in the avoidance of tedium or what some might call 'unnecessary complexity'. LLMs do seem to have potential in avoiding unnecessary complexity, and boilerplate, including CSS boilerplate, is often that! Still, there is a major difference between using tech to write gobs of boilerplate for you and building or choosing a better conceptual system which has much less boilerplate. Assuming the later is possible, settling for the former feels shortsighted or foolish in that it ends up being much more fragile in addition to being a death sentence for proper understanding, and proper understanding of our design primitives is crucial for good UX in the long run.

Another benefit generative AI advocates talk about is "lowering the floor" - and fair enough many web developers, and even more people who just want to use the web have little interest in becoming experts in CSS. But LLMs are hardly the only way to reduce the barriers to entry. Better, simpler, more approachable libraries do this too! Whats more, they can do it without relying on third party pay-to-play services, crazy energy use, or unethical model and training. Additionally better libraries that can accomplish this without requiring deep knowledge, but still promoting or enabling such understanding rather than obscuring or discouraging it. Better libraries fully embracing modern approaches therefor are a Win-Win-Win type of scenario worth pursuing.
