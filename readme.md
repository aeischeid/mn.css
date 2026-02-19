MN-CSS

the name: MN because Minnesota is both a cool place and where the devs making this live - Also mn is short, and works as a shortened version of 'minimalist', which is a good descriptor of the philosophy this project intends to embrace.

The inspirations:
pico.css https://picocss.com/
water.css https://watercss.kognise.dev/
missing.style https://missing.style/
milligram https://milligram.io/
mini.css https://minicss.us/docs.htm
bolt.css https://boltcss.com/
dev.css https://tangled.org/devins.page/dev.css

DaisyUI https://daisyui.com/
Shadcn-classless https://nandaleio.github.io/shadcn-classless/#introdution
Materialize https://materializecss.com/typography.html

... Overwhelming meta list of others: https://github.com/dbohdan/classless-css 

Goals: 
In the past many UI libraries and FE styling tools and tool chains have treated CSS as a problem to be solved, and fair enough, in the past CSS had many rough edges, but modern CSS has addressed many of those pain points, and by-in-large the ecosystem has failed to move past the entrenched thinking. css-modules, emotion/css-in-js, etc.

Projects exist to help educate developers, but a library that unifies the concepts of modern CSS, the simplicity of classless CSS, and the composibility and ergonomics of atomic-css seems to be somewhat of a gap at the moment.

Beyond direct tooling, conventions like BEM aimed to bring sanity, but at scale (wether project or team) had their own challenges. Atomic CSS was another one of these conventions. Though tailwind takes that to an unhealthy extreme IMO that convention works can scale well in my experience.

More modern than Pico.css - Un-Sass-ify (css tricks link) it with a more modern CSS syntax approach, in some ways like water.css but including more and deeper styles than water. Less complex, and for now much less ambitious, than DaisyUI importantly without a reliance on a heavy and CSS hostile dependency like Tailwind. I think we could get to something beyond the ambition of many classless CSS libs without bloating it and setting it up to be extended and customized such that a project adopting  

Un-tooling. not just Sass, but Tailwind, UnoCSS etc are all so complicated,  a bit of atomic css utilities on top of some classless CSS, some basic CSS componentization, NO BUILD tool, no distribution stack, just text files that can be copied, and then modified.
