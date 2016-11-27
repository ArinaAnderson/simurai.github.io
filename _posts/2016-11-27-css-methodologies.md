# When to use which CSS methodology
Over the years more and more CSS methodologies started to appear and it can be quite hard to keep an overview and decide what to use. In this post we try to find the right CSS methodology for a certain situation, because unfortunately there just isn’t the perfect one.

Alright then, let’s dive right into this abyss.

> I just want to create a single page or a simple site. The content is mostly text and maybe a form or two. There aren’t any co-workers, just me (and my cat).  

👉 Keep it simple and style HTML elements directly without using classes. [Use the cascade and let things inherit](https://www.smashingmagazine.com/2016/11/css-inheritance-cascade-global-scope-new-old-worst-best-friends/).  As the site grows, you might wanna look into start using [OOOCSS](http://oocss.org/) , or use some utility classes here and there.

> We’re a medium sized team. Our project grew quite a bit in complexity. Multiple people work simultaneously on the same thing.   

👉 Use BEM, SUIT, SMACSS, ITCSS, Enduring etc. They are all different, but still share similarities and overlap in some areas. Discuss it with the team and maybe try out a few before settling on a final choice.


> We’re a large company with different teams. Our product is large and complex. It’s hard to keep up what’s going on. We constantly iterate and don’t want to break something in another corner.  

👉 Use [JSX](https://facebook.github.io/react/docs/jsx-in-depth.html) , [JSS](https://github.com/cssinjs/jss) (or a similar CSS-in-JS library). Also take a look at Atomic CSS with [ACSS](https://acss.io/)  which tries to solve the same problem with a different approach.

- - - -

That’s probably the 3 main uses cases, but there are lots more situations that have their own specific needs:

> I want to get started with a prototype .  

👉 Use a “single purpose class” library like [TACHYONS](http://tachyons.io/) or [BASSCSS](http://basscss.com/) . It can be liberating writing HTML and CSS at the same time in the same place. No switching files, no pondering what the class name should be called, just quickly build .


> Our project has lots of states, lots of things that need to be updated at runtime.  

👉 Use [JSX](https://facebook.github.io/react/docs/jsx-in-depth.html) , [JSS](https://github.com/cssinjs/jss) (or a similar CSS-in-JS library). 


> I want to release a CSS framework (yes, me too).  

👉 Use BEM with a namespace. So it has some protection but is still customizable. Also providing a way to easily theme the framework would be nice, maybe by changing variables.


> I want to create a 3rd party widget (that shouldn’t be customizable).  

👉 CSS Modules. The unique classes will guard against styles leaking out or in. Iframes or Web Components should also be considered.


> I want to create a [CodePen](https://codepen.io/) .  

👉 Use something new. This is your chance of actually trying out something you aren’t familiar yet.


> I hate my coworkers.  

👉 Use chained classes, like `.header > ul.nav li .button {}`. This will make your coworkers suffer and satisfy your schadenfreude.

ok, wait.. don’t do the last one. The only reason I can think of using chained selectors is if you have no access to the markup. Like when it gets dictated by the CMS and there is no way to change it. I guess then it’s the best (only) choice.


- - - -


As you can see, there are many different use cases and that’s why debating about CSS methodologies can be hard without knowing each other’s context. 

Some closing thoughts: You don’t have to settle on a single CSS methodology. It can also be mixed. Switching to a new methodology is also possible and sometimes a must. Like when a project starts out as a simple prototype but then later grows into a more complex project with many team members. But switching methodologies can be quite time consuming and brittle. So a little planing upfront can save lots of headaches later on. Happy choosing!


- - - -


> Disclaimer: I’m biased too, who isn’t? I also haven’t used every CSS methodology long enough to claim that I know what I’m talking about. But I still try to stay as neutral as possible. If you think this post got something wrong or is missing, [click this link](#) and edit away.  
