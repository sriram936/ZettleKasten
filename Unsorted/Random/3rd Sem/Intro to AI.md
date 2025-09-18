PEAS
- Performance
- Environment
- Action
- Sensors

Rational thinking: following specific rules and regulations , the action should be performed to succeed a task,  to achieve an expected outcome.

Turing test :  Interaggator is unable to find if a task is done by ai agent or human, then the ai agent succeded the test.

1) Fully obs vs Partially obs

2) Static(chess, env dont change as user plays or course of action) vs Dynamic(env changes)

3) Discrete(Finite set of percepts n actions) vs Continuous

4) Episodic(Series of one shot action, only current percept is required) vs Sequential(Work happened in the past is needed to achieve)

5) Single-Agent vs Multiple-Agent

6) Accessible and Inaccessible

7) Stochastic(env will be randomly changing and env change on current action, cant predict future env state)  vs Deterministic

Tables are important

TYPES OF AGENTS

1) Simple reflex agent
	 - Take decision on current percept , no past history knowledge
	 - Not adaptive to environment changes
	- state = percept
	- rule = rule-match(state, rules)
	- action = rule-action (rule)
	- return action

2) Model based reflex agent
	- Current state is based on the past percept history.
	- static: model, current world state(description)
	- rules, set of condition action rules Kev, rules about how worlds evolves Kacct, description of rules
	- Eg: Cleaning robots, student study plan
	- Partially observable environment