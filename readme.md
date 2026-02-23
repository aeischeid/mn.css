# MN-CSS

the name: MN because Minnesota is both a cool place and where the devs making this live - Also mn is short, and works as a shortened version of 'minimalist', which is a good descriptor of the philosophy this project intends to embrace.

The inspirations:
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
- https://moderncss.dev/
- https://modern-css.com/

beyond mere classless libs
- DaisyUI https://daisyui.com/
- Shadcn-classless https://nandaleio.github.io/shadcn-classless/#introdution
- Materialize https://materializecss.com/typography.html

... Overwhelming meta list of others: https://github.com/dbohdan/classless-css 

### Goals: 
In the past many UI libraries and FE styling tools and tool chains have treated CSS as a problem to be solved, and fair enough, in the past CSS had many rough edges, but modern CSS has addressed many of those pain points, and by-in-large the ecosystem has failed to move past the entrenched thinking. css-modules, emotion/css-in-js, etc.

Projects exist to help educate developers, but a library that unifies the concepts of modern CSS, the simplicity of classless CSS, and the composibility and ergonomics of atomic-css seems to be somewhat of a gap at the moment.

Beyond direct tooling, conventions like BEM aimed to bring sanity, but at scale (wether project size or team size) such solutions had their own challenges. Atomic CSS was another one of these conventions. Though Tailwind takes that to an unhealthy extreme, inheriting all the problems of inline styles, the atomic-css convention works, and can scale well in my experience.

MN.css aims to be a more modern approach than Pico.css - to [Un-Sass-ify](https://css-tricks.com/is-it-time-to-un-sass/) it with a more modern CSS syntax approach, in some ways like water.css but including more and deeper styles than water. MN.css also aims to be less complex, and quite a bit less ambitious, than DaisyUI, but importantly without any reliance on heavy and CSS hostile dependencies like Tailwind. Maybe closer to [Bootstrap](https://getbootstrap.com/) or [Bulma](https://bulma.io/), but more classless, more lightweight and no build tools required. I think we could get to something beyond the ambition of many classless CSS libs without getting bloated, and if we're setting it up so that extending and customizing can be acheived simply by removing or modifiying some component parts, such that a no tooling at all is needed or even encouraged maybe it encourages using CSS itself rather than outsourcing styles to a framework/library that folks are reluctant to 'eject' from.  

### Un-tooling.

Not just Sass, but Tailwind, UnoCSS etc are all so complicated. A thing I really appreaciated about the Svelte project early on was how they were trying to revive jQuery's "write less; do more" approach. MN.css is maybe aiming to bring that to CSS in a way that also doesn't add a single dependency to your project. With a bit of atomic css utilities, on top of some classless CSS, and some basic CSS componentization/compartimentalization, this can be acheived with NO BUILD tool, no distribution stack, just a small collection of text files that can be copied, and then modified without fear. One outcome I personally would hope for is that unlike the aesthetic flattening or homogonizing effects that Bootstrap or MaterialUI or other design systems have had on the web, where developers maybe changed theme colors but left everything else alone, this library would actually encourage a renewed diversity in design. Maybe that is overly optimistic, but in my experience the level of abstraction of these design system implementations brought a level of fear; where actual customization was avoided for multiple reasons, including having to learn and incorperate the whole build tool pipeline of the project to accomplish it, or how it would likely make it hard to upgrade to a future version or somesuch. No build tool and no offical distribution channel or even versioning/releases might seem like an odd choice for a modern library, but in that it encourages you to take it and make it your own - actually for real - I think it aligns with the projects goals, and follows the spirit of [html5 boilerplate project](https://html5boilerplate.com/)
