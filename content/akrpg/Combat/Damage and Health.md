# Health
A character's health represents their ability to withstand damage and injuries before falling in battle. Health is measured by two strictly related values, *Health Dice* (HD) and *Hit Points* (HP). Each health die has 6 HP, and as such a creature's maximum amount of health points is $Max HP = HD*6$, representing their vitality in perfect conditions. When a character receives healing, they cannot go above their Max HP value.
## Barrier
Barrier is a form of temporary HP that a creature can gain from various sources. Barrier is measured in HD like health, but unlike health it is unaffected by healing and can only be recovered by receiving additional barrier dice. When a creature loses any amount of HP, it is first taken from its barrier and only after the barrier is depleted any leftover amount of damage is dealt to its health.
## Shield
Shield is a [[Arknights The Roleplaying Game#Reserves|reserve]] that can absorb some incoming damage and can be gained from various sources. Whenever a creature takes any amount of damage, if it has at least one die of shield, remove 1d from its shield and roll it:
- **6**: reduce the damage taken by *5* (can become 0), then put the die back in the shield reserve.
- **1-5**: reduce the damage taken by the rolled amount (can become 0).

*A single instance of damage can only be affected by a maximum of 1d of shield, regardless of how much shield a creature has.*
# Damage
When characters are hit by attacks or other dangers, they may take damage, which reduces a character's HP — or barrier if present — by its amount. Different types of damage exist in AKRPG, and each follows slightly different rules.
## Physical and Arts Damage
By far the most common types of damage, Physical and Arts damage share the same rules but interact with different defensive attributes. When taking any amount of damage of one of those two types, the player controlling the creature that dealt the damage rolls an amount of dice equal to the damage value. This is called a Damage Roll, and is a [[Arknights The Roleplaying Game#Tests|test]] with the target's DEF (in case of physical damage) or RES (in case of arts damage) as its Difficulty. The number of successes obtained from the test represents the damage that managed to pierce through the target's defenses and is dealt as damage.
## True Damage
True damage differs in that it does not have a damage roll, instead it is directly applied as damage ignoring the target's defenses. True damage also ignores conditions that modify damage taken *including those which increase it* — such as sanctuary *(link)* or fragility *(link)*.
## Damage Over Time
Certain effects or attacks can cause a creature to take damage over multiple rounds. Each creature has a *Damage Over Time (DOT)* [[Arknights The Roleplaying Game#Trackers|tracker]] that represents this damage. At the start of its turn, a creature loses HP equal to the amount of dice in their DOT tracker, then decreases each die by one, removing any that would go below 1. Since this damage is directly applied on a creature's HP, it ignores any condition or effect that alters damage taken, as well as any shield. Dice can be added to the DOT tracker by various sources, but regardless of its origin, it is always applied as either a *full DOT* or as an *half DOT*. The former adds the specified amount of dice — in most cases one, but it could be more — to the tracker each showing the number 6, while the latter adds the dice showing the number 3, thus halving the duration and overall damage dealt.
## Elemental Damage
Elemental Damage is a special kind of damage which can only be applied to creatures under the effect of [[Conditions#Elemental Injury|elemental injury]]. Like true damage, elemental damage does not have a damage roll, and ignores the target's DEF and RES, but unlike true damage it is affected by conditions and effects that alter damage taken — such as sanctuary *(link)* or fragility *(link)*.
# Down and Dying
When a character's HP falls to 0 or lower, they immediately gain the [[Conditions#Downed|downed]] condition. A downed character cannot take any action, and will slowly bleed out and die if they don't receive assistance in a short time. When a character is downed, they immediately gain a [[Arknights The Roleplaying Game#Reserves|reserve]] with a starting amount of dice equal to their current number of HD. At the start of each of their turns, the player controlling a downed character rolls one die from the reserve, then depending on the result:
- **6**: The player puts the die back in the reserve.
- **2-5**: The player discards the die.
- **1**: The player discards the die and removes another die from the reserve (without rolling it).

If a character runs out of dice in their dying reserve completely, they immediately die. A downed character can be restored to combat state with the [[Combat#Stabilize|Stabilize]] action. When a character loses the downed condition, their [[Conditions#Wounded|wounded]] condition's value increases by 1 *(a character without the wounded condition is considered to have a value of 0)*.