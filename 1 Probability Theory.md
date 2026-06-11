# Probability
- discovered to make sense of uncertainties

Definition:  
A number between 0 to 1 (inclusive) that is assigned to a random outcome of uncertainties
- 0 be impossible
- 1 be certain

## 2 interpretations of probability
- Classical (theoretical) probability
- Relative frequency (Empirical) probability

# Classical probability
In this version, all random outcomes are considered to be **equally likely**.
- can only use classical probability formula when all events are equally likely

Formula:  
for the probability of a <font color="#00b0f0">random event A</font> occurring  

$$
P(A) = \frac{\text{Number of different outcomes for A}}{\text{Total number of possible outcomes}}
$$

Example:  
Deck of:
- 6 of hearts
- 7 of spades
- 8 of diamonds
- 9 of clubs
- 10 of hearts
What is the probability of picking 6 of hearts?
- 1/5
What is the probability of picking a card with hearts?
- 2/5
What is the probability of picking a value >= 7?
- 4/5

# Relative frequency (Empirical) Probability
The probability assigned to an outcome is the proportion of times it would occur over the long run.
- used with data that has been collected over the years or existing past data

Concerns in relative frequency probability:
1. How many times are considered a long run?
2. What if the outcome cannot be repeated?
	- Events cannot repeated exactly
3. There is no past data as it is an utterly new situation?
	- different variables affecting the event

Formula:  
for the probability of A  

$$
P(A) = \frac{f}{n}
$$

where  
f: number of times the outcomes occur  
n: total number of observations

# Probability Venn Diagram
Example: Dice  
Possible Sample space: {1,2,3,4,5,6}  
S = {1,2,3,4,5,6}
- ![[attachments/{03F311DC-9077-47E2-97C4-17174E4B472B}.png]]
What is the probability of getting a 6? (Event A)  
A = {6}
- ![[attachments/{B58E1C40-0FA3-4CB6-98D3-542BC3FF2940}.png]]

## Probability of a complementary event
Probability of a complementary event is the probability that it doesn't happen

$$
P(A^C) = 1-P(A)
$$

Continued Example:  
![[attachments/{0771EC20-0822-4DE4-8BCB-554B024C1AB6}.png]]  
Probability of NOT getting a '6':   
Classical interpretation: $P(A^C)=1-P(A)=1-\frac{1}{6}=\frac{5}{6}$  
Empirical interpretation: $P(A^C)=1-P(A)=1-\frac{30}{100}=\frac{70}{100}$
- from data

## Another example:
Dice sample size: {1,2,3,4,5,6}  
Probability of getting an even number: {2,4,6}  
Probability of getting a number bigger than 3: {4,5,6}  
Venn Diagram:  
![[attachments/{6A042A22-0114-4692-8A9A-B26BA1ACD519}.png]]  
What is the probability of getting an even number OR a number > 3?  
Look at the diagram. The probability will be $\frac{4}{6}$

This is an example of the following formula for the <font color="#00b0f0">probability of union of events A and B</font>:

$$
P(A\cup B)=P(A)+P(B)-P(A\cap B)
$$

used for OR statements  
If we use formula for the example:  
$\frac{3}{6}+\frac{3}{6}-\frac{1}{3}=\frac{2}{3}$


Probability of getting an odd number OR a number 6?  
Event A getting an odd number: {1,3,5}  
Event B getting "6": {6}
- Event A and B are <font color="#00b0f0">mutually exclusive events</font>.
	- Probability of A and B occurring is 0
![[attachments/{79A963B5-B7E3-4738-9FEA-AE0418048A8B}.png]]  
Use the formula:  
$P(A\cup B)=P(A)+P(B)-P(A\cap B)$   
$\frac{3}{6}+\frac{1}{6}-0=\frac{4}{6}=\frac{2}{3}$
- 0 because they don't intersect

# Union & Intersection Events
1. Probability of **intersection** of events A and B is the probability that **both A and B occur**.
2. Probability of **Union** of events A and B is the probability **of either A or B or both occur.**

$$
\begin{gathered}
P(A\cup B)=P(A)+P(B)-P(A\cap B)\\
\text{Mutually Exclusive Events}: P(A\cup B)=P(A)+P(B)
\end{gathered}
$$

Example:  
A company has made a policy that in the next 5 years, 40% of their new employees will be male and 30% of their new employees will be Singapore-born. There will also be 35% overseas-born, female new employees.
- What percentage of new employees will be overseas-born?
	- Event SB= {Singaporean-born employee} = 30
	- Event O = {Overseas employee}{Complement of SB} = 70
	- Answer: 70%
- What percentage of new employees will be Singaporean-born men?
	- Event SB= {Singaporean-born employee} = 30
	- Event O = {Overseas employee} = 70
	
	- Event M = {Male employee} = 40
	- Event F = {Female Employee} = $P(M^C)$ = 60
	
	- Event $P(O\cap F)$ = {Overseas and Female} = 35/100
	- ![[attachments/{B0AE0E14-4498-4BF9-B57A-DDB47FDC46E5}.png]]
	- Event $P(M\cup SB) = P(O\cap F)^C = 1-\frac{35}{100}=\frac{65}{100}$ 
	- 65/100 ~ Singaporean born or Male
	- Use union formula: $P(A\cup B)=P(A)+P(B)-P(A\cap B)$ to sub in known values
	- 65 = 40 + 30 - $P(M\cap SB)$
	- $P(M\cap SB)$ = 40+30-65	= 5
	- Answer: 5% of the new employees will be Singaporean-born men
	
	- Alternative approach using cross-tabulation:
	- ![[attachments/{7796A425-2D0D-4F57-BE6D-A119BF04B0B5}.png]]

# Conditional Probability
- Probability of an event can be changed if additional information is available

$$
\begin{gathered}
P(A|B)=\frac{\text{Probability that both events A and B occur simultaneously}}{\text{Probability of B occuring}} \\
= \text{Probability of event A occuring given that event B has occured}
\end{gathered}
$$

- $P(A|B) \neq P(B|A)$

Example:  
Dice sample space S = {1,2,3,4,5,6}  
Event A is getting a '6' = 1/6  
Event B is getting an even number B = {2,4,6} = 3/6
- What is the probability of Event A, given that event B has occurred? $P(A|B)?$
	- $P(A|B)=\frac{P(A\cap B)}{P(B)} =\frac{1\div 6}{3\div 6} = \frac{1}{3}$
- What is the probability of Event B, given that event A has occurred? $P(B|A)?$
	- $P(B|A) = \frac{P(A\cap B)}{P(A)} = \frac{1 \div 6}{1 \div 6} = 1$
	- Remember: $P(A\cap B)$ can be found by using $P(B\cap A)=P(B)+P(A)-P(B\cup A)$


The table below shows the probabilities of males, females, employed or unemployed in a population.  
![[attachments/{42A4130E-966B-490C-8EED-3EB6ADAEC1E5}.png]]
- Find the probability of being employed, given that the person is male? $P(E|M)?$
	- $P(E|M)=\frac{P(E\cap M)}{P(M)}=\frac{0.52}{0.57}\approx 0.91228$
	- Conclusion: If you choose a random person (male) from the population, there is 91% of chance that they are employed!
- Find the probability of being male, given that the person is employed? $P(M|E)?$
	- $P(M|E)=\frac{P(M\cap E)}{P(E)}=\frac{0.52}{0.93}\approx 0.559$
	- Conclusion: 56% chance they are male

# Multiplicative Rules of Probability
A way to calculate the intersection of events A and B.

$$
P(A\cap B)=P(A|B)P(B)
$$

where we multiply $P(A|B)\text{ and }P(B)$
- Pretty similar to simple probability multiplication
- **Tree diagrams** are pretty good at visualising what to multiply

Example:  
2 blue and 3 red marbles are in a bag. A child is asked to randomly picked 2 marbles without replacement.
- What is the probability that the child picks a second blue marble, given that he/she has already picked a blue marble? $\text{Find }P(\text{2nd Blue}|\text{1st Blue})$
- What is the probability that the child picks **2 blue marbles?**
Tree Diagram:  
![[attachments/{BE2E148B-A4BC-4D75-9946-B4D28879C5E0}.png]]  
Answer for first part would be $\frac{1}{4}$  
Second Part:  

$$
\begin{gathered}
\text{Find P(1st Blue }\cap\text{ 2nd Blue)}\\
P(1st~Blue) = \frac{2}{5}\\
P(\text{2nd Blue}|\text{1st Blue}) = \frac{1}{4}\\
P(\text{1st Blue }\cap\text{ 2nd Blue}) = \frac{2}{5}\times \frac{1}{4} = \frac{1}{10}
\end{gathered}
$$

# Independent & Mutually Exclusive Events
## Independent Events
If the conditional probability of A given that B has occurred remains unchanged as the original probability of A, then A and B are said to be independent events.
- A is not affected by B. They are independent events.

$$
P(A|B)=P(A)~or~P(B|A)=P(B)
$$

Example: consider tossing 2 fair dice  
Event A: getting a '6' on the first dice: P(A) = 1/6  
Event B: getting a '6' on the second dice: P(B) = 1/6
- How to know if they are independent?
	- $Find~P(A|B)\text{ \& compare it with }P{(A)}$
	- $P(A\cap B)= \frac{1}{36};\text{ Visualise 36 different combinations, only 1 will have both die on 6s}$
	- $P(A|B)=\frac{P(A\cap B)}{P(B)}=\frac{1\div 36}{1\div 6}=\frac{1}{6}$
	- $P(A|B)=P(B)=\frac{1}{6}$

### How 'replacing' affects the events
![[attachments/{AAE7EDAD-EF2F-442A-8DFA-2C6AD6FE4EFC}.png]]
- With replacement of the marbles, the events between the first choice and the second choice are now independent from each other

#### A way to represent Independent events using tree diagrams
By <font color="#00b0f0">applying replacements to our tree diagrams</font>, we can visualise independent events

Example:  
Consider tossing 2 fair coins. What is the probability of getting at least 1 head?
- ![[attachments/{5C19449A-780C-4AD6-BDF8-EA8F9B56BA50}.png]]

### Intersection of Events on independent events
For independent events,

$$
\begin{gathered}
P(A| B)=P(A)\\
\color{white} \rule{4cm}{0.4pt}\\
\therefore  P(A\cap B)=P(B|A)P(A)=P(B)P(A)
\end{gathered}
$$

known as multiplication rule of independent events
- can be extended to as many independent events

## Mutually Exclusive Events
**WILL NOT** occur at the same time
- (e.g. event of being male or female)
- Mutually exclusive events **MUST** be dependent because occurrence of 1 event is affecting the other.

Example:  
Rolling a die and getting 2 OR 6
- Cannot happen simultaneously
- $P(2~or~6)=P(2)+P(6)=\frac{1}{6}+\frac{1}{6}=\frac{1}{3}$

## Formula Table
| When KNOWN Events are: | $P(A \cup B)$ is:      | $P(A\cap B)$ is: | $P(A\|B)$ is:             |
| ---------------------- | ---------------------- | ---------------- | ------------------------- |
| Mutually Exclusive     | $P(A)+P(B)$            | 0                | 0                         |
| Independent            | $P(A)+P(B)-P(A)P(B)$   | $P(A)P(B)$       | $P(A)$                    |
| Any (Unknown)          | $P(A)+P(B)-P(A\cap B)$ | $P(A)P(B\|A)$    | $\frac{P(A\cap B)}{P(B)}$ |

# Bayes' Theorem
## Exhaustive Events
2 events A and B are called exhaustive events if they together cover all possible outcomes.

$$
P(A\cup B)=P(S)=1
$$

Example:  
Tossing a dice, sample space $S=\left\{ 1,2,3,4,5,6 \right\}$
- Event A is getting an even number: $A=\left\{ 2,4,6 \right\}$
- Event B is getting an odd number: $B=\{ 1,3,5 \}$
- Probability of getting an even number or odd number: $P(A\cup B)=P(S)=1$

## Law of Total Probability
allows us to calculate the probability of an event by considering all possible ways it can occur across a set of mutually exclusive and exhaustive events

$$
P(A) = P(A|B₁)P(B₁) + P(A|B₂)P(B₂) + ... + P(A|Bₙ)P(Bₙ)
$$

$$
P(A)=P(A\cap B_{1})+P(A\cap B_{2})+\dots+P(A\cap Bn)
$$

Example:  
Imagine a medical test:
- Let A be "positive test result"
- Let B₁ be "patient has disease"
- Let B₂ be "patient does not have disease"
$P(A) = P(A|B₁)P(B₁) + P(A|B₂)P(B₂)$

## Bayes' Theorem
Bayes' Theorem provides a way to update the probability of a hypothesis given new evidence.  
<font color="#00b0f0">Not in formula sheet:</font>

$$
P(B|A) = \frac{P(A|B)P(B)}{P(A)}
$$

Rewrite with law of total probability:

$$
P(B|A)=\frac{P(A|B)P(B)}{P(A|B)P(B)+P(A|B^C)P(B^C)}
$$

we can get $B|A$ if we know $A|B ~\&~ B~ \&~ A|B^C$

"False Positive" ~ Detecting a condition that does not actually exist  
"False Negative" ~ Missing a condition that actually exists

Example:  
Assume 1% of human population are allergic to cats. Suppose there is a medical test for this allergy with a correct detection rate of 80% and a false positive of 10%.
- What is the probability that when a person tests positive, they really have an allergy?
	- Let having Allergy P(A) and not having P(A')
	- Test shows positive P(T) and showing negative P(T')
	- What we know:
	- $P(A) = 0.01$
	- $P(A')=0.99$
	- $P(T|A)=0.80$
	- $P(T|A')=0.10$
	- What we are trying to find: $P(A|T)$
	- We use Bayes' Theorem and plug in values
	- $P(A|T)=\frac{P(T|A)P(A)}{P(T|A)P(A)+P(T|A^C)P(A^C)}=\frac{0.8\times 0.01}{0.8\times 0.01 + 0.1 \times 0.99}=\frac{8}{107}\approx 0.075 \approx 7\%$

Example:  
Of the one million monkeys in Singapore most are good-natured. But 100 monkeys of the one million are pure evil! An aspiring student in our Course develops an "Evil Monkey Alarm" which he/she offers to sell to the government. The government decides to test the reliability of the alarm by conducting trials.
1. When presented with an evil monkey, the alarm goes off 99% of the time.
2. When presented with a nice monkey, the alarm goes off 1% of the time.
- If a monkey sets off the alarm, what is the probability that it is evil?
	- We have:
	- $P(evil)=0.0001$
	- $P(nice)=0.9999$
	- $P(A^+|evil)= 0.99$
	- $P(A^+|nice)=0.01$
	- Calculate $P(evil|A^+)$
	- $P(evil|A+)=\frac{P(A^+|evil)P(evil)}{P(A^+|evil)P(evil)+P(A^+|nice)P(nice)}=\frac{0.99\times 0.0001}{0.99\times 0.0001 + 0.01\times 0.9999}\approx 0.98\% \approx 1\%$
	- Because of huge population size and the chance of a false positive