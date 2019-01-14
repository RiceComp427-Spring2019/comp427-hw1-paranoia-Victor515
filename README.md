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
- Scenario: Documents
- Assumptions:
  - I assume that this document management system is not intended for everyday use, which means it only stores documents that are viewed important and sensitive to the company.  This system can only be accessed within the company's intranet, and different people have different privileges when they use this document system.
- Assets:
  - The assets we want protect are some sensitive documents to the firm. We want to ensure that people could view/edit/delete documents in this system only if they have the privilege to do so. People who do not have this privilege can never access any document in the system, and people who have privileges to view/edit/delete one document cannot view/edit/delete other documents in the system.
  - These assets are viewed highly important to the law firm. Disclosure of documents to irrelevant inpeople will lead to leak of critical information and huge costs. Customers will think that their information are not secure with us and refuse to do business with us in the future. On the other hand, if documents are falsely modified, our law firm could potentially break the law and eventually go bankrupt.
- Threats:
  - There are several kinds of attackers based on their motives. Firstly, attackers may attack our document management system to obtain documents. They may sell these documents to make profits or they may take advantage of information stored in documents themselves. Secondly, attackers may attack because they want to undermine our firm or create trouble for us.
  - These attackers will pose different types of threats to us. First, they can break into our firm's intranet and hack into our system if the system is public to everyone in the company. Even if the system requires authentication to log in, they may still find ways to break into our authentication system. Second, if attackers are employees of our company, they may have some privileges to log into the document system. In some way, they may alter their privileges, like changing from "view only" to "edit/delete", or extend their privileges of one file to the other. Or, they actually have the privilege to view/edit/delete one document, and they maliciously intend to do something evil.
- Countermeasures:
  - For threats from outside attackers, we have some countermeasures to defend against them. First, we need to set up authentication system and constantly upgrade it for our document management system, so that only authorized person can log into the system. Second, we could narrow the range where this document management system can be accessed, for example, from the whole intranet in the company to some subnet. Thirdly, we could set up some monitoring system for our firm's intranet, so that malicious intent from the outside will be spotted in time. These three countermeasures are specially designed for attackers outside the company. The first and third countermeasures will generate costs like installation and maintenance fees of authentication and monitoring system. The second countermeasures, on the other hand, will add complexity and inconvenience for people who really want to access the document management system.
  - For threats posed by inside attackers, we also have design several countermeasures. First, we want to make sure that granting of privileges must be done by human and people cannot arbitrarily alter their privileges inside the system. Editing/Deleting document is more significant, so these actions can only be manually approved by those who are legally responsible for these documents. This method will create inconvenience for people in charge of documents, and probably slow down procedures to modify some documents. Second, we want to make sure every action within the system is well recorded. If any loss is generated, we could easily investigate into records to find out who is held responsible. And of course, rule and regulations must be established to prevent any unjustified and harmful actions. The second method will have costs like implementing a robust recording application within the document system.

## Problem 3
- Scenario: As one of security officers at Uber/Lyft, how do I design security mechanisms and policies to  guarantee the safety of passengers along their rides.
- Assumptions:
  - I assume that during a ride, drivers are more familiar with the surrounding environment--his/her car, and passengers are at a relative disadvantaged place.
- Assets:
  - The assets I want to protect is the safety of any passenger during his/her ride. As an online ride scheduling system, if we cannot provide safety of our passengers, there will be direct costs because we will be sued to pay large amount of compensation fees. Also, people will view rides provided by our company as unsafe, and refuse to use our products in the long run.
- Threats:
  - The major attackers of our passengers' safety are drivers, and there are two kinds of threats.  First, we may recruit some drivers without enough information about them and their cars (for example, their current address, car license number, credit score report, etc.).  At other times, people may forge their documents and register, while our registration system is not strong enough to detect these falsified proof. Thus, malicious people will have incentives to register in our system and threaten the security of our passengers. Second, even if a driver is a regular person, with valid personal and car information, he/she may still pose threats to our passengers. For example, the driver may drive after drinking, or he/she may happen to be in a low mood and drive in a dangerous fashion. This kind of threat is harder to protect than the first kind, because we cannot predict when such situations will take place.
- Countermeasures:
  - We need to have different countermeasures against these two kinds of threats. For the first kind, we need to devise strict and effective procedures to verify a driver's eligibility to enter the system. This procedure may require any applicant to submit more documents and may take more time to verify the provided information. This will create costs, because we need to hire more people to enforce such a procedure, and we may discourage some eligible drivers before they decide to apply for a driver. Therefore, we need to make sure that our procedures are short enough, but still valid to verify a driver. 
  - To deal with second threats, which happen more occasionally, we could set up our emergency center to cope with any threats happening in real time. For example, we could track drivers on the GPS through our app. And if the car stop at an abnormal place, or it drives toward a different direction other than the desired destination, we would contact the driver to verify or contact local police for help. Such an emergency center could somehow reduce the probability that some threats actually happen to our passengers, despite that we need to pay money to set it up. Also, we would set up feedback and rating system in our application. A passenger who feels that the driver could threat future passengers' safety could provide feedback to us, and any driver which is rated to a low enough points will be punished, or eliminated from our system. The cost is that we need to implement such a system, but it will help us in the long run to eliminate drivers that are not eligible.

