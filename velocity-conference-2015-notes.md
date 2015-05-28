# Velocity Conference 2015

## DAY 1

### Keynote

#### Housekeeping
- leave feedback to speakers; rate

#### Laura Bell [@lady_nerd](https://twitter.com/lady_nerd) - SafeStack

*Securing organizations through bad behavior*

- security
- #betteroffbad for questions or comments
- self responsibility for security on apps

3 steps to help security of your app
- think of attacks in the mind of a villian
- create a safe place (to play with attacks)
- don't be afraid to play (be creative and throw out the rule book)
  - rules influence behavior and expectations, so you must throw those out

*Feedback for speaker: Good awareness session on securing your app or system. She was entertaining and the metaphors (artisan box with a cat in it) she used in the beginning were carried successfully throughout her talk. *


#### Dana Quinn [@dquinn_devops](https://twitter.com/dquinn_devops) - Intuit
*Lessons learned for large-scale apps running in a hybrid cloud environment – Intuit’s journey*

Intuit moved workloads to the cloud for the usual reasons of cheaper processing and more flexibility and he's explaining his lessons learned.

- Workload choice requirements
  - build environments
  - load test generation
  - decoupled systems

- Choice of toolset
  - Hybrid was attractive, but went with cloud-native
  - Cloud vendor lockin was a risk, but they feel comfortable with the choice

- Cloud shouldn't feel like fog
  - legacy mgmt patters into clouds shouldn't be brought in
  - insist on right patterns

- Track your costs
  - Empower teams to manage own spending

*Feedback for speaker: Decent content of the migration of workloads at Intuit. Could have used more key takeaways. *


#### Dave McCrory - Basho Technologies 
*Addressing operational challenges: Building a faster, highly available data tier for active workloads*

- scale or fail!
- data problem are arising due to massive amounts
- data consitency challenge
  - CAP Theorem; tradeoffs in distibuted systems
- data gravity
  - growth effect through apps/services funneling all data somewhere


#### Rob Peters [@rjpcal](https://twitter.com/rjpcal) - Verizon Digital Media Services
*Maintaining performance and reliability on the edge Robert Peters*

Verizon's Global Delivery Network
- Delivery on promises
  - pefromance at the edge
  - secure by design
  - verizon-size network

Conway's law to influence organization on technology
- Conway's law alternate interpretation
  - Standard
  - Alternate

Example #1: canary/coalmine tools for release management
- Showing metrics on changes they can make in continuous releasing

Key Takeaways
- Tools need clearly defined team 
- be strategic
- use/fine tune existing tools

*Feedback for speaker: He spoke pretty fast so it was hard to keep up with and not sure he made his point across, but this could be that he only had 5 minutes to present.*


#### Astrid Atkinson [@shinynew_oz](https://twitter.com/shinynew_oz) - Google
*Engineering for the long game: Managing complexity in distributed systems*

Managing distributed systems over a really long time
What is the "long game"?

Rules of the long game
- imagine you'll be very successful
- complexity increases over time

Scale systems not teams
- good teams/people are previous
- teams outlast any piece of code

Diversification of growing systems
- they get too complex
- inevitable vertical/horizontal scaling
- high costs, many resources

Enable Growth
- manage software, not machines
- standarize your env
  - consistency is key
  - Google has splash status pages for each system to show all details about it
    - also, shows who are the owners of the pages

Engineer for maintainability
- identify cost of maintaining
- use shared infrastructure

Be responsible and considerate when encountering issues such as timeouts or bad responses

Insights on consolidation of systems
- pick the right moment
- be ... 

Engineering for flexibility
- shared systems have drawbacks though; requires coordination with cross teams
- moving workloads is challenging

Second systems

Iterate early and often (insights on moving to new systems)
- get changes in production early
- if new systems don't add better capabilities, then don't do it
- big changes require long lead times
  - huge endeavor at Google with all of their systems
- move biggest customer first

Rules of the long game
"Don't let the weeds get higher than the garden"
- question what's taking the longest time, what's costing the most
- no finish line, no end game, quickly evolving
- pay attention to what you're really trying to achieve and keep eyes on the outcomes

*Feedback for speaker: Informative speaker and good content about scaling challenges. She'd be a good contact for advice or someone to follow.*


#### Jessica DeVita [@ubergeekgirl](https://twitter.com/ubergeekgirl) & Jennelle Crothers [@jkc137](https://twitter.com/jkc137) - Microsoft
*Not your parents' Microsoft*

Sponsored keynote just talking about how Microsoft is evolving -- not much content


#### Jason Ding [@jding](https://twitter.com/jding) - Salesforce
*Prevent, rather than fix: How to scale to enable your customers*

Scalable Prevention

Customers of different sizes - how to address scaling
- scope, plan, test, optimize (iterative)

Expose lots of limitations with the iterative process
- Feedback is super valuable
- metrics of a/b testing of new features/changes also good to know

Scaling issues can be found through testing
- Simulations are key to find potential scaling problems

*Feedback for speakers: Not so much valuble content, since it was a sponsored keynote. Lots of energy and some humorous slides/memes. I didn't need my coffee during this presentation.*


#### Indy Young

Empathy

Solving issues
- brainstorm with as many people as you can; this will increase your creativity
- subconsious will syntehsize all the ideas floating around when your brain is relaxed

Empathy
- be more sensitive
- emotionally aware

How do you apply this to operations or development?

Types of empathy (8 but only listing 4)
- mirrored empathy
  - smiling at another, and receiving a smile back
- personal distress
  - empathy for someone who "cuts their finger in the kitchen"
- effective empathy
  - feeling same emotion another person feeling
- emotional empathy

Most of this content is about empthy and consideration for outside factors. Pretty abstract talk and somewhat philosophical. Somewhat of a snoozer.

*Feedback for speaker: Pretty serious tone, could use a joke or two to lighten the mood. Most content designers would know about.*


#### Zach Leatherman [@zachleat](https://twitter.com/zachleat) - Filament Group
*The performance and usability of font loading*

@font-face

- default behavior is harmful for the web

@font-face usage
- 47% on top of 1000 websites
- avg 97kb payload per site
- impact of fonts aren't as bad as images

Not all requests are created equal

Web fonts have non trivial performance on web pages

1) Trigger a font download
- showing font-face syntax/declaration in css
- formats
  - WOFF/WOFF2 (30% smaller than woff - use this instead)
  - TTF
  - don't use SVG, lots of bugs

If font isn't used, then it isn't downloaded
Browsers will download the font differently
- Some will download when content is in element, some won't 

Unicode Range only allows a font to be downloaded (request) if a character matches the unicode range

`font-family`, `font-weight`, `font-style` are declarations that become 

"faux bold" or "faux italic" are terms to describe a font synthesis that happens when the browser programmatically figures out how much weight or style to give the font
- Font Synthesis only support by Firefox

Instagram uses the `<i>` element for a login button which forced the page to download a font. Could have saved ~13k if set the `i` element to font-style: normal;


2) Behavior of page while downloading

While font-face is downloading
- see invisible text
- font loads, rerender text using webfont (flash of invisible text)

Showing examples of slow performance on Apple, Instagram, Facebook

Flash of Unstyled Text (FOUT)

Not just a performance problem, but it also affects the integrity of the content
Showing example of Mitt Romney headline where 'not' text wasn't loading due to the slow font loading. Changed the full meaning of headline.

Anti-patterns
- CSS onload
  - Overreliance on it
- Async CSS
  - Same problem of blocking as CSS onload technique
  - Filament group has discussion on this https://github.com/filamentgroup/loadCSS

Embrace more FOUT instead of FOIT
- font-rendering css property (not supported yet)
- css font loading api (js lib)

Takeaways
- Lots of tools to ease transition to web fonts to fallback fonts
- Default browser rendering of fonts is harmful to web font loading
- Thoughts about Flash of Faux Text http://www.zachleat.com/web/foft/
- Can use the css font loading polyfill for the time being [https://github.com/bramstein/fontloader](https://github.com/bramstein/fontloader) [http://dev.w3.org/csswg/css-font-loading/](http://dev.w3.org/csswg/css-font-loading/)

#### Steve Souders [@souders](https://twitter.com/souders) - SpeedCurve
*Design+Performance*

Design / Devs are complementary forces to achieve same goal

Some designers have lack of awareness about performance
- This should be a goal for developers to create this awareness


- create small interdisciplinary teams
- set some guiding principles
  - "speed is more important than design embellishment"
- prototype early in code, not photoshop
  - use photoshop for assets
- measure the performance
  - set up "performance budgets"
  - Etsy has a bar of performance metrics at top of page for staff members to see
    - "in-page reminders"
  - SpeedCurve has a bookmarklet that shows all the data being gathered during the page visit

Page load time doesn't equate to good user experience

webpagetest tool
- Speed Index is basically a median for the render time of pixels (when 50% of pixels have been rendered)

Comparison video of gmail and amazon that shows finish loading time

Hero image delay
- took only 500ms to download, but took 2.5s-3s to show on the page
- turns out that js/css blocking images

Preloading scripts
- putting js at bottom of page before body isn't a good practice anymore
- on bottom, it gives them higher priority to download

Custom Metrics
- define most important elements 
- measure user User Timing api
- track with RUM (real-user monitoring) and synthetic (web browsing emulation)

Takeaways
- figure out what matters most to users
- forcus on UX exp/perf
- define custom metrics


#### Ian Malpass [@indec](https://twitter.com/indec) - Etsy

*Failure is an option*

How to learn from failure

3 truths 
- we'll create bugs
- we'll build the wrong thing
- you'll not forsee the unexpected

Consequences to failure
- money, time, data, credibility loss

Failure is inevitible, expensive failure isn't

Speed & Trust == flexibility

Etsy has their own deploy tool that is open to *everyone*
- can deploy any time, but try not to do it during off-hours

Build in small chunks and do code reviews
- Good learning experience for everyone

When something breaks, roll forward, not roll backward
- I think he means instead of rolling back to revert changes, they try to fix the bugs to move forward

Mixture of automated/manual testing

`try` program that compares the changes against automation tests
`princess` program that emulates changes in pre-production before they push to production

"Dark code" - code that isn't executed

"Feature flags" to throttle how many users get the new feature
- Ability for partial failures by usage of feature flags

Reducing the risk of building the wrong things by doing continous delivery on products
Continous deployment permits adding/changing/fixing things quicker
Unlike deployment at every 3-6 months where things need to be just right

Prototypes of new features by asking merchants to be "beta testers"

You can't avoid failure, but you can learn from mistakes

Blameless culture at Etsy
- post-mortems about what happened
- learn from mistakes
- share what they've learned
- celebrate failure by having annual awards

Push the envelope or else there's no progress
Don't be timid to make changes

Speed makes us safe

## DAY 2