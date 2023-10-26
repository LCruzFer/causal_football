# Causal Football 
Little private project to understand causal effects in football. Main idea right now: What is the causal effect of wingback moving closer to attacking winger on probability of next shot scoring a goal?

## Idea
What is the causal effect of a defender moving close to attacking winger in likelihood of run of winger (carrying ball maybe as condition) resulting in goal (or say shot with xG larger than some value V)? Interact this with dummy signaling defense sitting deep vs standing high (need to define what sitting deep and high are, e.g. deep: at least X players of defending team in own first third) 

Conditions:
- look at effect of closest player that is between attacker and goal moving closer
- look at runs in last third only, maybe even only runs when winger is already carrying the ball
- Need to define when shot still counting to Same attack (e.g. no more than x passes between run and shot or less than x backward passes or maybe there is some convention I can use)
- How is this related to distance to ground line?

Control for: 
- position of other defenders relative to other attackers or space around them (increases when one defender is moving out) 
- General stats of player (top speed, successful passes/crosses/shots, etc)
- Strength of team (league position of both)
- Past xG of attack (my Y) created by run in last third
- 

Panel data approach: multiple runs by same player available across 90 minutes (time FE to account for general fatigue etc and individual level FE to account for general skill) 