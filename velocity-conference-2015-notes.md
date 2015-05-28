# Velocity Conference 2015

## DAY 1

### Keynote

#### Housekeeping
- leave feedback to speakers; rate

#### Laura Bell - SafeStack
@lady_nerd

- security
- #betteroffbad for questions or comments
- self responsibility for security on apps

3 steps to help security of your app
- think of attacks in the mind of a villian
- create a safe place (to play with attacks)
- don't be afraid to play (be creative and throw out the rule book)
  - rules influence behavior and expectations, so you must throw those out

*Feedback for speaker: Good awareness session on securing your app or system. She was entertaining and the metaphors (artisan box with a cat in it) she used in the beginning were carried successfully throughout her talk. *


#### Dana Quinn - Intuit
@dquinn_devops

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


#### Dave McCrory - Basho Technologies - CTO 

- scale or fail!
- data problem are arising due to massive amounts
- data consitency challenge
  - CAP Theorem; tradeoffs in distibuted systems
- data gravity
  - growth effect through apps/services funneling all data somewhere

#### Rob Peters - Verizon - Chief Architect
@rjpcal

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

#### Astrid Atkinson - Google
@shinynew_oz

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


#### Jessica DeVita & Jennelle Crothers - Microsoft
@jkc137
@ubergeekgirl

Sponsored keynote just talking about how Microsoft is evolving -- not much content


#### Jason Ding - Salesforce - Sr. Performance Engineer 
@jding

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


## DAY 2