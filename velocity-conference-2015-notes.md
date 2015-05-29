# Velocity Conference 2015

## DAY 1

### Housekeeping
- leave feedback to speakers; rate

### Securing organizations through bad behavior
*Laura Bell [@lady_nerd](https://twitter.com/lady_nerd) - SafeStack*

- security
- #betteroffbad for questions or comments
- self responsibility for security on apps

3 steps to help security of your app
- think of attacks in the mind of a villian
- create a safe place (to play with attacks)
- don't be afraid to play (be creative and throw out the rule book)
  - rules influence behavior and expectations, so you must throw those out

Feedback for speaker: Good awareness session on securing your app or system. She was entertaining and the metaphors (artisan box with a cat in it) she used in the beginning were carried successfully throughout her talk.


### Lessons learned for large-scale apps running in a hybrid cloud environment – Intuit’s journey
*Dana Quinn [@dquinn_devops](https://twitter.com/dquinn_devops) - Intuit*

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

Feedback for speaker: Decent content of the migration of workloads at Intuit. Could have used more key takeaways.


### Addressing operational challenges: Building a faster, highly available data tier for active workloads
*Dave McCrory - Basho Technologies*

- scale or fail!
- data problem are arising due to massive amounts
- data consitency challenge
  - CAP Theorem; tradeoffs in distibuted systems
- data gravity
  - growth effect through apps/services funneling all data somewhere


### Maintaining performance and reliability on the edge
*Rob Peters [@rjpcal](https://twitter.com/rjpcal) - Verizon Digital Media Services*

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

Feedback for speaker: He spoke pretty fast so it was hard to keep up with and not sure he made his point across, but this could be that he only had 5 minutes to present.


### Engineering for the long game: Managing complexity in distributed systems
*Astrid Atkinson [@shinynew_oz](https://twitter.com/shinynew_oz) - Google*

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


### Not your parents' Microsoft
*Jessica DeVita [@ubergeekgirl](https://twitter.com/ubergeekgirl) & Jennelle Crothers [@jkc137](https://twitter.com/jkc137) - Microsoft*

Sponsored keynote just talking about how Microsoft is evolving -- not much content


### Prevent, rather than fix: How to scale to enable your customers
*Jason Ding [@jding](https://twitter.com/jding) - Salesforce*

Scalable Prevention

Customers of different sizes - how to address scaling
- scope, plan, test, optimize (iterative)

Expose lots of limitations with the iterative process
- Feedback is super valuable
- metrics of a/b testing of new features/changes also good to know

Scaling issues can be found through testing
- Simulations are key to find potential scaling problems

Feedback for speakers: Not so much valuble content, since it was a sponsored keynote. Lots of energy and some humorous slides/memes. I didn't need my coffee during this presentation.


### A practical type of empathy
*Indy Young [@indiyoung](https://twitter.com/indiyoung)*

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


### The performance and usability of font loading
*Zach Leatherman [@zachleat](https://twitter.com/zachleat) - Filament Group*

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

### Design+Performance
*Steve Souders [@souders](https://twitter.com/souders) - SpeedCurve*

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


### Failure is an option

*Ian Malpass [@indec](https://twitter.com/indec) - Etsy*

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


### Learn how to build your own cognitive applications with the IBM Watson Developer Cloud
*Salil Ahuja [@salilahuja](https://twitter.com/salilahuja) - IBM*

Watson creating APIs and used in the cloud
Asked who's heard of Bluemix (only a few people raised their hands)

Acquisition of Alchemy Language API

Bluemix is down so live demos can't be shown

AlchemyData News
Concept Insights


### Maintaining the biggest machine in the world with mobile apps
*Lucasz Pater [lukasz.pater@cern.ch](lukasz.pater@cern.ch) - CERN*

CERN
- Tries to answer deep questions about the universe by simulating atomic big bangs
- Composed of millions of components

Asset Management Challenge at CERN
- millions of physical assets
- site infrastructure over 700 buildings, tunnes, caverns roads
- accelerator complex: supra-conducting magnets, cryogenics, electronics

Mobile Strategy & Architecture
- developed a native one-size-fits-all app for field engineers
  - was a disaster due to many outside factors such as expensive devices, training contractors, etc..
- native app for specific user tasks and HTML5 web apps were a success

Current architecture
- Infor EAM
  - Native web interface, SOAP, various auth methods

- Web services hub (JAX-WS/RS + Tomcat)
  - SOAP, REST, compression, checksumming, caching, extensive logging, web sockets, asynchronous communication

APIs made possible through REST/SOAP

Web Apps possible thanks to HTML5, JS/jQuery

CERN web/mobile apps using localStorage for offline usage

Native-based apps are a challenge because supporting multiple platforms is resource heavy

Availability of high-speed networks and web standards make HTML5 web apps

No mention of hybrid -- perhaps a plug for MF? :)


## DAY 2

### Ensuring a performant web for the next billion people
*Bruce Lawson [@brucel](https://twitter.com/brucel) - Opera*

4 billion people in asia
Estimated to explode in growth even further

What do all the nations named in asia have in common
- people worldwide want to consume same goods/service
- they visit the similar sites, but majority of visits are on low-end phones

New manifest file developed with light metadata and icon

Responsive images
- `<picture>`
- scrset
...

Proxy Browsers
- QQ, UC Browser, Puffin, Microsoft Express

Opera mini can render content on their servers, then send compressed binary blob to client

Reduction in features of content during process
- no web fonts
- no custom animations
- no border-radius
- use svg icons

Opera Mini focuses on compression and compatibility


### Great, you're now a software company. Now what?
*Patrick Lightbody [@plightbo](https://twitter.com/plightbo) - New Relic*

- All businesses are becoming a software companies
- Social has transformed companies 


### Twenty thousands leagues inside the optical fiber 
*Ariya Hidayat [@AriyaHidayat](https://twitter.com/AriyaHidayat) - Shape Security*

Distance of communications can be a problem

History of communications
- Photophone from Alexander Bell
- Free space communication
- Telephone dominance (electricity over light communications)


Talking about fiber optics and lasers -- very technical in physics I can't follow lol

Improving new fiber type can get 255 Tb/s over 1km (50 channels x 5.1 Tb/s)



### Beyond the hype cycle; bleeding edge for the enterprise 
*Shane Evans - Hewlett-Packard*

QA & Testing has seen a growth spurt in enterprise

Inability to adopt agile is due to a failure to implement a testing process

Technology adoption curve looks like a chart from marketing (innovators - laggards)

5 billion connected devices by 2015, 

DevOps is a prerequisite for IoT

- Build smarter automation
- address the legacy, simulate through virtualization 
- think about the process scalability

Agile wasn't meant for enterprise, but can be


### Overcoming the challenges of image delivery 
*Mohammed Aboul-Magd [@mohammedam](https://twitter.com/mohammedam) - Akamai Technologies*

Users demand rich experiences

over course of day akamai deliver 750,000,000 jpgs a day

Operational challenges delivering images
- delivering to different densities, formats, compression rates, composition, etc..


Ideal scenario
- have original asset
- all delivery will be automatic
- best size, quality, format chosen

Akamai Image Manager
- upload raw images > automatic policy/rules -> delivery?


### Reflections on mountain moving, from the first year of USDS 
*Mikey Dickerson - Federal Government | United States Digital Services Team*

Healthcare.gov funding for 20m in 2015

Congress passed bill in 2016 for 100+m

Processes such as green card replacements or VA claims had vast improvement by placing necessary materials and applications online

Not interested in being Bunjee bosses, not interested in making app for agency, then disappearing


### Measurement is not enough: The rise of performance analytics 
*Buddy Brewer [@bbrewer](https://twitter.com/bbrewer) - SOASTA*

Relationships between data and people

Performance has a specific set of meanings to different people

User's definition of performance is unique

People's "languages" are different so it's important to create relationships of different meanings on performance


### Recruiting for diversity in tech 
*Laine Campbell [@LaineVCampbell](https://twitter.com/LaineVCampbell) - Pythian*

All employees are recruiting for a company (actively/passively), your actions, your language

Reduce skepticism in recruiting

create a culture of forgiveness, don't be afraid to speak out

Diversity is 2-dimensional

STEM will be the next middle class
- could bring us back to balance

meritocracy is broken
- governing group makes up teams
- group would rather hire for comfort than diversity

businesses should have codes of conduct


### New ways to deploy and manage applications at scale
*Kelsey Hightower [@kelseyhightower](https://twitter.com/kelseyhightower) - CoreOS*

**How can the design team gain any takeways from this heavy operations presentation**
- Engineers love using the terminal and are very efficient
- Managing some apps with APIs

Using Ansible to automate apps/IT infrastructure
- great for automating starting instances of apps with variables
- Not great scaling down because instances will not be shut down when change made to config

Using scheduling (automatic/manual - actual people)
- must move past shell scripting

Decouple applications from the machines
- use configs to manage machines not apps
- better abstraction for apps (containers)
- use of app centric tools (Kubernetes)

Containers
- building containers has been problem
- payload size is really big for others to download
- ship build artifacts NOT build environments
- dockerfile can be called a "specification"

Managing containers
- kubernetes
- nodes, node manifest (specification)
- pods, representation of an application (also has a manifest)

Cluster of nodes on a system that Kubernetes works with
- Relication feature: anytime a pod goes down, kubernetes will find another pod with nodes that match the specification to start up

Real world demo time
- showing how powerful kubernetes can be with container management
- impressive example of rolling out new app deployment using rolling upgrade with Canary(?) pattern


### Making continuous delivery a reality at a large enterprise 
*Adam Auerbach [@bugman31](https://twitter.com/bugman31) - Capital One*

Advanced Testing 
Agile transformation of testing group
drive towards continuous delivery

Capital One more than bank company, they have retail, digital apps, etc.

CO Tech structure
- Shared Tech services
- LOB Tech org

DevOps & Agile

Agile Tranformation
- in the past, waterfall we got really good at
  - everyone had a role/task

Leveraged Scaled Agile Framework (SAFe) http://www.scaledagileframework.com/
- could get teams get up and running quickly
- ten teams in a few months
- release planning party every 3 months

Over 700 agile teams at CO

Agile training saw success
- devliery from 6 months to 3 months
- release planning much better
- align people on trains?

Opportunities
- dev sprints
- testing sprints
- integration / hardening

Challenge
- Couldn't get anything out the door under 12 months

Creation of something called a System Team
- teams composed of release management, config mgmt, continuous builds/deployments, etc..
- aligned to 10 teams, 10-12 people on team
- represent release mgmnt
- ci (continuous integration)
- problem of not having enough bandwidth for each team to complete goals

Created standards for the teams to refer to
- place for source, templates, builds cycles

Lessons learned from System Teams
- treat as a new agile team
  - team members are properly training
  - team members are fully dedicated
  - ensure acccess to all tools and systems need (stand)
- leverage a sprint 0 to focus on grooming backlog
- focus on early outcomes to develop creditbility
- scrum works well early but kanban is more sustaining
- teams will be large initially and reduce as maturity is achieved

System Teams in place, still needed more to address more issues

Continuous testing
- Implementation of BDD and TDD has permitted faster integration
- adoption 6-9 months for existing teams, shorter for new teams

Manual testers need to do automated testing
- they don't have the skills to do this, so training must be involved

Continous Toolsets
SVN, Git, AWS, Chef, Hudson, uDeploy

New Dashboard
- Hygieia; OSS coming out soon - realtime view of all their platforms

Service virtualization
- enables robust testing if env has limitations
- meaning if front end is ready to test, but API isn't, you can virtualize the service

Test data
- tool built to support System Teams

Many processes for automated and continuous integration/deployment
Many checks and balances through tools to maintain  

Key Metrics
- output (will be replaced by cycle time)
- speed
- quality

Key outcomes
- drive adoption across the company, teams working together to advocate, showing results
- enterprise support groups help minimize upgront costs to getting started

Value Stream Analysis
- tool to communicate ROI for leadership hesitant to invest
- 6 person team, single person dedicated to builds, deployment, 
- 1 week increments (pic on phone)

Other lessons learned
- reuse proven frameworks
- evangelists at every level/discipline
- education for everyone
- leverage dedicated resources who support/nurture the community
- be prepared


### Engineering transformation: Everyone owns quality 
*Huseyin Dursun - VMware*

Some background
- VMWare release cadence 6/9/12 mo, quarterly service relesaes
- transition to quarterly cadence for regular on-premise releases

Goal is to increase the cadence

Had traditional organization up until last year
- vertical and overhead, working in silos

Engineering Transformation
What are we doing
- quality is everyone's responsibility
- system centric rather than feature/func-centric
- moving func validation responsibility to developer
- forming engineering services/opertaions layers/teams to validation coverage and production support

Why are we doing it?
- achieving enterprise grade quality
- right level of coverage
- predictability
- transform to prepare for cloud

Transition from traditional model
- many checks and balances (pic on phone) 

Specialized engineers for various components of development

Before transformation, need a baseline template in place first

Delivery pipeline: desktop to cloud
- vmware is using almost all their products for this process
- Code Stream, Orchestrator, Automation, Operations, Log Insight, etc.

Exploratory Testing
- new model has no room for manual testing

Cultural Transformation stages
- denial > resistance > commitment > exploration

Takeaways
- no perfet time for transformation
- piloting helps, not a panacea
- identify potential candidates for specialized roles early
- no over communication; keep evangelizing
- have backup plan dealing with backlog issue
- metrics, necessary but not sufficient


### PARKING LOT
- Lots of mentions of automated testing in relation with continuous cycle: Should designers give requirements early to dev team before wireframes come out? Does this already happen?

