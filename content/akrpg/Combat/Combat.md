Combat happens on a grid of squares, each representing the space taken up by a single combatant.

A combat encounter is divided in rounds, during which each combatant generally takes one turn. The order of turns within a round depends on each combatant's initiative value, with higher values acting first.
# Initiative
At the start of combat, all combatants roll an open check using their INI. The turn order is determined by the resulting number of successes in descending order (the combatant with the highest number of successes acts first). In case of tie, the number of Perfects determines who acts first. In case of tie on the number of Perfects, the highest INI value goes first. Combatants belonging to the same faction who are adjacent in the turn order can freely choose who acts first each turn.
# Actions in Combat
In each round you can:
**During your turn**
- Use a single movement action
- Use a number of actions up to your ASPD
- Use any number of quick actions
**Outside of your turn**
- Use up to one reaction when it's trigger requirements are met
## Movement Actions
Movement Actions represent the way a combatant moves around the battlefield. All characters get access to the following two movement actions by default:
- Move a number of squares equals to the character's MOV.
- Shift 1 square?
## Actions
Standard Actions (simply actions for short) are the most common for of action in AKRPG. From weapon attacks to powerful arts, *most* effects that damage, heal or influence creatures other than their user will require an action. The number of actions a combatant can take each turn is not fixed, rather it depends on their ASPD attribute.
## Quick Actions
Quick Actions represent faster activities that require less concentration to perform, like speaking a few words or dropping an item you are holding. You can do as many quick actions per turn as you want, but only once each.
## Reactions
Reactions are a special type of action that can be performed outside of a combatant's turn. Every reaction has a `trigger` attribute which defines when it can be used. Depending on their `priority` attributes, reactions are divided into two categories:
- **Interrupts** happen before the triggering event resolves, and if upon resolving the interrupt the conditions for the triggering event are no longer met, the triggering event does not happen.
- **Follow-Ups** happen immediately after the triggering event resolves.
# Movement
Movement is done one square at a time. Entering a new square costs 1sq of movement by default, but if terrain has a different movement cost then it is applied whenever entering a square of that type of terrain (the cost needs to be paid in full, if the movement left is not enough to pay the terrain cost then it is not possible to move to that square). Diagonal movement follows the same rules, but moving around corners cannot be done via the diagonal and require the additional square to move around.

## Shift?
Shift is a special kind of movement that doesn't trigger reactions triggered by characters moving.
*(does movement need to be done consecutively? is it possible to split or change action order?)*
# Morale
Morale is a shared [[Arknights The Roleplaying Game#Reserves|reserve]] used by the players. At the start of each round the party gains 1d of morale, and [[Classes#Vanguard|vanguard]] characters can generate more in multiple ways. Any player can spend morale to gain various benefits during their turn.

Full Page: [[Morale]].
# Skill Points
Skill points are a resource used by characters to access more powerful skills in combat. Unlike Morale, each character has their own SP pool that cannot be shared. Characters begin combat with their SP at its maximum value, but SP cannot be recovered during battle outside of specific skill or talents. Even in that case, a character cannot have more SP than their maximum and any additional SP gained while at max is lost. *(need to properly define how max sp works but maybe just 3 flat, or 1/2/3 scaling with Elite level idk)*
# Attacks
Most skills that inflict damage (with the notable exception of save-based effects) require their user to first make an attack against the target. Attacks are resolved by a check, called an *Attack Roll*, with the target's current EVA score as difficulty. The pool for this check - referred to as **ATK** - is defined by each skill or trait that calls for an attack, and is affected by any ATK modifier applied to the creature rolling it.

If the check is successful, the attack is considered successful as well, and its hit effects are applied. Otherwise, the attack missed or its target managed to deflect it, and its miss effects will be applied if present, otherwise nothing happens. There is no default behaviour for Perfects in an attack roll, and each attack can define them if needed.
## Multiple Attack Penalty
Attacking an enemy is a task that requires concentration, and doing it multiple times in a short timespan is bound to have diminishing returns. This is represented by the Multiple Attack Penalty (**MAP**) mechanic. During your turn, for any attack roll you make you have `ATK -Xd` where X is your current MAP value. MAP starts at 0 at the start of each of your turns, and increases by one for each attack action you take during your turn. Reactions and other actions take outside your turn are unaffected by MAP. *MAP only increases after an attack action is completely resolved, and multiple attack rolls within the same action only increase it once.*
# Damage and Health
A character's health represents their ability to withstand damage and injuries before falling in battle.

Full Page: [[Damage and Health]].
# Conditions
Conditions are statuses that can be applied to a character. They can be either negative or positive, and can be applied by various sources. Conditions can be divided into three main broad categories: *Positive Status Effects*, *Negative Status Effects* and *Elemental Injury*.

Full Page: [[Conditions]].
# Blocking
When a character engages their enemies in melee combat, it prevents them from moving freely around the battlefield and forces them to keep their guard up. In game, this is covered by the block mechanic.

Full Page: [[Blocking]].
# Attribute Checks in Combat
Certain rules, skills or other effects may call for an [[Attribute Checks|attribute check]] in combat. When that happens, resolve the check using their rules as described in the Interactions section.
## Saves in Combat
Just like regular attribute checks, [[Attribute Checks#Saves|save rolls]] in combat follow their regular rules, but they have more strictly defined use cases. Some effects that target unwilling creatures might allow the target to resist the effect with a save. In this case, the creature rolls the save immediately, then the effects continues resolving. Other effects might apply lasting conditions that are terminated by successfully saving against them. In this case the creature rolls the save at the end of each of its turns until it succeeds, or until the effect ends via other means. The notation for this type of save is `<effect> (<attribute> save ends)` and it affects any statement within the same effect *before* the brackets. That means, every statement after the brackets will not be affected by the save result. If multiple save ends clauses are defined within the same effect, than each only affects statements following the previous one, meaning no statement is affected by more than one save ends clause.
# Zones
A zone is a set of squares on which an effect is applied. Zones can be created by a character's skills, other creatures' skills, devices, terrain types and other sources, and can either have a fixed duration or depend on other conditions to last. Each zone defines the when to apply its effects, and every creature within the zone that meets the conditions will receive the effect of the zone (common triggers are entering a square of the zone, starting or ending your turn in a square of the zone, performing actions while in the zone...).
# Summons
Certain skills and traits allow a creature to summon allies to fight alongside them. Summoned creatures gain the [summon] tag, and are subject to a few specific rules. Summons generally have their own stats, but in some cases might inherit part of or all of them from their summoner. Summons don't possess an initiative value, and rather act during the turn of their summoner. Unless otherwise specified, Summons don't have actions of their own and are controlled by their summoner's action, as defined by the summoning skill or trait.
# General Actions
The following actions are available to all characters.
## Stabilize
(INT/SEN check, diff 1/2? remove the downed condition and heal the character to HP equal to their HD + P)