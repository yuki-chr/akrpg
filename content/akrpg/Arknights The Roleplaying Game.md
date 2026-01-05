# Introduction
Arknights The Roleplaying Game (AKRPG) is a fan-made roleplaying game set in the world of the mobile game [Arknights](https://arknights.global), using the Nd6 *(link)* roleplaying system.
# Core System Mechanics
The following are core Nd6 mechanics as they are implemented in this game.
### Roll Types
Depending on the situation, different types of dice rolls can be used in AKRPG. Those are Checks, Tests and Flat Rolls.
#### Checks
Checks are by far the most common roll type, and are generally used to determine whether an action with uncertain results will succeed or fail. To perform a Check you first build a dice pool according to what the rules for the specific roll state (depending on the implementation, this might be a combination of character attributes, skill and situational modifiers). Once the pool is ready you can roll the dice and check the result: any die that rolled 4+ is a success, and additionally any die that rolled 6 also counts as a "Perfect", which can be used to determine additional effects depending on the check. The number of Perfects rolled for a given check is referred to as `P`. The success of a Check can be determined in two ways:
- **Difficulty**: If the rules (or the GM) set a specified Difficulty value for the Check, then it will succeed if the amount of successes is greater than or equal to the Difficulty, and fail otherwise.
- **Open Check**: Some Checks do not have a fixed threshold for success, and instead can have varying effects based on the number of successes rolled. These are called Open Checks and are best suited to be used in situations where there isn't a clear-cut separation between success and failure, but rather degrees of success to the action.
Depending on the implementation, the player attempting the Check might always know its type/difficulty, or it might sometimes be hidden to them.
#### Tests
Tests are an alternative roll type, suited to determine the strength of an effect when there is something that can absorb or reduce it. The most common application is damage rolls against a defense/armor value. Like with Checks, you begin by building your dice pool according to the rules of the roll, then you roll the dice. Unlike Checks however, Tests always have a Difficulty value between 1 and 5, and each die succeeds if it beats (**not** equals) this value. The result of the Test is the number of dice that succeeded the roll.
If the Difficulty of a Test is brought below 1 then there is no need to roll the dice as every die rolled will succeed regardless, and likewise if it is brought above 5 every die will fail.
#### Flat Rolls
Flat Roll is an umbrella term to cover any type of roll not belonging to the previous two. When the rules call for a Flat Roll, they will define how to build the dice pool, and how to interpret the results. One example of this would be a simple coinflip, where a single die is rolled with no modifiers and a result of 4+ is a success while otherwise a failure.
### Resource Pools
Resources in AKRPG are tracked in various ways, however particular attention is given to those that can be expressed as dice pools. Those can consist in two main forms: Reserves and Trackers.
#### Reserves
A reserve consists in a number of dice that can be spent or consumed for various purposes. Each reserve will have its way(s) to add dice to it, and may or may not have a maximum value. Dice from a reserve also needs to specify how and when its dice can be spent or consumed. Generally, (part of) it can be used to contribute to or build a dice pool.
#### Trackers
A tracker is similar to a reserve, but the value of each die is recorded. On top of adding and removing dice from the pool, it is also possible to change the value of one or more dice in it. Optionally, a die could be removed if it's value would go below 1 or above 6. Sometimes, it might be useful to keep track of how many dice in a tracker have a value of 6, those can be referred to as "full" dice.
In general, trackers are used to keep record of resources with numerical values, and not to build dice pools, but exceptions can of course exist.
# Setting
[Arknights Wiki](https://arknights.wiki.gg/wiki/Terra)
# Characters
Characters are at the core of an AKRPG game. This section details how to build your character, as well as how to progress them as the game continues.

Full page: [[Characters]]
# Interactions
As the game plays out, there will be many times when the characters want to interact with the world around them in ways that have uncertain outcomes, this section covers the mechanics to handle such situations.

Full page: [[Interactions]]
# Combat
Terra is not a land at peace, and combat is sometimes unavoidable (or other times the characters might be the ones to cause it in the first place). This section explains the rules to run a combat encounter in AKRPG.

Full page: [[Combat]]