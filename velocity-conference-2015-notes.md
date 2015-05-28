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

#### Dana Quinn
Intuit
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

#### Dave McCrory - CTO
Basho Technologies

- scale or fail!
- data problem are arising due to massive amounts
- data consitency challenge
  - CAP Theorem; tradeoffs in distibuted systems
- data gravity
  - growth effect through apps/services funneling all data somewhere

#### Rob Peters - Chief Architect
@rjpcal
Verizon

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

## DAY 2