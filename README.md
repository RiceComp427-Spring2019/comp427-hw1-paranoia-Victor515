# <img src="http://www.rice.edu/_images/rice-logo.jpg" width=180> Comp427, Spring 2018, Homework 1
## Rational Paranoia
The homework specifications, as well as the corresponding course slide decks,
can be found on the [Comp427 Piazza](https://piazza.com/class/jqifhp864b37ju).
This assignment is due **Thursday, January 17 at 6 p.m.**

You will do this homework by editing the _README.md_ file. It's in
[MarkDown format](https://guides.github.com/features/mastering-markdown/)
and will be rendered to beautiful HTML when you visit your GitHub repo.

## Student Information
Please also edit _README.md_ and replace your instructor's name and NetID with your own:

_Student name_: Yubo Ouyang

_Student NetID_: yo10

Your NetID is typically your initials and a numeric digit. That's
what we need here.

_If you contacted us in advance and we approved a late submission,
please cut-and-paste the text from that email here._

## Problem 1
- Stadium
- Assumptions:
  - Assume I am in charge of a football stadium in a university, whose ranking is among the best in this country. Because the stadium is not very large, for each game, tickets are sold out quite early, and there are a lot of people who want to see a game but do not have a ticket.
- Assets:
  - The asset we want protect here is the right of any ticket holder. We want to ensure that people who have a ticket can take the seat they are assigned to, and those who do not have a seat cannot get into the stadium. Also, we want to make sure everybody takes their own seats, instead of taking others'.
  - If we fail to protect the right of ticket holders, costs could be so huge. First,  those who cannot take their desired seats even though they buy the ticket could sue us for compensation. Second, if we continuously fail to protect, it will give people motivation to not buy tickets and just sneak into the stadium, which creates a vicious cycle.
- Threats:
  - There are outside and inside threats we need defend against. The outside threats come from people who do not have tickets but try to sneak in to see the game. They have several ways. First, there are many gates around the stadium, and they could carefully choose a gate with fewest guards and just sneak in; or they could find a gate with so many crowd that guards could barely keep an eye on everyone. Second, these people could forge their tickets and if they make their tickets so real, they could directly walk into the stadium without being stopped. Third, in some cases, those guards may falsely execute their power and let their friends get in through the back door.
  - The inside threats are from those who have a ticket but intentionally take other people's seats for some reasons (such as sit next to their friends, or have a nicer view of the game).
- Countermeasures:
  - The inside threats are easier to defend against, because they are easy to find out. One simple countermeasure could be that we set up some guards in each section, and ask them resolve any case that somebody takes someone else's seat. The cost is that we need to hire people, but the benefit is that most of inside threats would be resolved.
  - The outside threats are harder to protect against. We need to have countermeasures for each way of "attacks" stated above. For the first way of "attack", we could arrange each ticket holders to go to their destined entrance, so that each entrance will have almost equal volume. Also, if some entrances become too crowded at some periods, we could assign more guards and ticket checkers to those places, dynamically.  The cost is that we need to devise and implement a "load balancing" mechanism. The cost is worthy because this kind of attack tends to have high frequency. Also, in this way, we could avoid hiring more people, which will increase our costs of countermeasures.
  - For the second way of "attack" using forged tickets, we could upgrade our ticket authentication system so that only real tickets will be accepted. The cost is the upgrading costs and the cost to train people to use new system. But since ticket forging tend to have great harm and high frequency, we need to afford the costs of this countermeasure. Also, we need to make sure that the ticket authentication process is not too long so that each entrance is not crowded with people.
  - The third way of "attack" is hard to prevent using any technical measures. But we could set up rules that those who abuse their power will be fined heavily and fired. In this way, we set up a negative incentive for people to not use this kind of "attack".

## Problem 2
- Scenario: {Stadium|TSA|Documents|Grading|G20}
- Assumptions:
  - explain_your_assumptions
- Assets:
  - explanatory_paragraph
  - explanatory_paragraph ...
- Threats:
  - explanatory_paragraph 
  - explanatory_paragraph ...
- Countermeasures:
  - explanatory_paragraph
  - explanatory_paragraph ...

## Problem 3
- Scenario: Your choice (give a brief explanation)
- Assumptions:
  - explain_your_assumptions
- Assets:
  - explanatory_paragraph
  - explanatory_paragraph ...
- Threats:
  - explanatory_paragraph 
  - explanatory_paragraph ...
- Countermeasures:
  - explanatory_paragraph
  - explanatory_paragraph ...

