MN-CSS

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

Goals: 
In the past many UI libraries and FE styling tools and tool chains have treated CSS as a problem to be solved, and fair enough, in the past CSS had many rough edges, but modern CSS has addressed many of those pain points, and by-in-large the ecosystem has failed to move past the entrenched thinking. css-modules, emotion/css-in-js, etc.

Projects exist to help educate developers, but a library that unifies the concepts of modern CSS, the simplicity of classless CSS, and the composibility and ergonomics of atomic-css seems to be somewhat of a gap at the moment.

Beyond direct tooling, conventions like BEM aimed to bring sanity, but at scale (wether project size or team size) such solutions had their own challenges. Atomic CSS was another one of these conventions. Though Tailwind takes that to an unhealthy extreme, inheriting all the problems of inline styles, the atomic-css convention works, and can scale well in my experience.

MN.css aims to be a more modern approach than Pico.css - to [Un-Sass-ify](https://css-tricks.com/is-it-time-to-un-sass/) it with a more modern CSS syntax approach, in some ways like water.css but including more and deeper styles than water. MN.css also aims to be less complex, and for now much less ambitious, than DaisyUI, importantly without a reliance on a heavy and CSS hostile dependency like Tailwind. Maybe closer to Bootstrap or Bulma, but more classless, more lightweight and no build tools required. I think we could get to something beyond the ambition of many classless CSS libs without getting bloated and if we setting it so that extended and customizing can be acheived simply by removing or modifiying some component parts such that a no tooling at all is needed or even encouraged maybe it encourages using CSS itself rather than outsourcing styles to a framework/library that folks are reluctant to 'eject' from.  

Un-tooling. not just Sass, but Tailwind, UnoCSS etc are all so complicated,  a bit of atomic css utilities on top of some classless CSS, some basic CSS componentization, NO BUILD tool, no distribution stack, just text files that can be copied, and then modified.
