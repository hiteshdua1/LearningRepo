# BDD
> BDD is an approach that collaboratively specifies the system's desired behaviour. Each time a piece of behaviour is agreed, we use that specification to "drive" the development of the code that will implement that behaviour.

## How ?
> ### Discovery -> Formulation -> Automation
1. We start by collaboratively **discovering** the scope of the behaviour required by the story. 
2. Once we have agreed on that behaviour, we **formulate** the specification in business-readable language.
3. Finally, we **automate** the formulated specification to verify that the system actually behaves as expected.



**"Living documentation"** automatically tells us when the system and the documentation are out of sync. This may be for one of several reasons:
- the behaviour specified has not yet been implemented
- the implementation contains a defect
- the documentation is out of date


## BDD and Agile
> BDD is a collaborative activity. Living documentation is a secondary, valuable, output of applying BDD practices.


## When to do BDD ?
User stories were created to be "placeholders for a conversation."
They allow us to defer detailed analysis until we're confident that the behaviour they describe actually needs to be developed.

## Discovery Workshop.
> [![Discover Video](https://i.ibb.co/QJ2gFZ1/image.png)](https://platform.thinkific.com/videoproxy/v1/play/bnf65mcp59r8a2tjqsug?&autoplay=true&crosstime=135)


### The Three Amigos
- Developer
- Tester
- Product Owner

The goal of a three amigos meeting is to ensure that the team fully understand the scope of the story being discussed. For this to be effective, we need to have at least three different perspectives represented at the meeting.

More than three people might attend a three amigos meeting, because:

some stories are broad enough to require the input of more than three perspectives
more than one representative of each perspective may attend

## Formulation
Gherkin language 

```
Feature: Google Searching
  As a web surfer, I want to search Google, so that I can learn new things.
  
  Scenario: Simple Google search
    Given a web browser is on the Google page
    When the search phrase "panda" is entered
    Then results for "panda" are shown
```

Some Examples :
- http://tfs:8080/tfs/DefaultCollection/SaxoTrader/_workitems/edit/1078049
- http://tfs:8080/tfs/DefaultCollection/SaxoTrader/_workitems/edit/1078277

