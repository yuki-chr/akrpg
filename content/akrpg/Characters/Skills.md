Skills represent special types of actions and attacks that a character can use in combat. Each skill has a **Name**, an **Action Type**, a **Cost**, several **Tags**, and a **Description**.
# Name
The name of the skill.
# Action Type
Each skill uses a specific action type, which is one between the following:
- **Action**: using the skill requires an [[Combat#Actions|action]].
- **Quick**: using the skill counts as a [[Combat#Quick Actions|quick action]].
- **Reaction**: the skill is used as a [[Combat#Reactions|reaction]]. Can additionally have the [forced] tag to make its use mandatory.
# Cost
The [[Combat#Skill Points|SP]] cost of using the skill. Can be 0.
# Tags
Tags further define the skill's behavior and properties. There are many tags that a skill can have, but a few more commonly used and are described here, organized by what they describe.
## Activation
Activation tags tell whether the skill's effects resolve immediately, or if it remains active for an extended amount of time. The following tags are exclusive and mandatory, one and only one between them will be present for each skill.
- **Instant**: The skill resolves immediately when used.
- **Activated**: The skill stays active for a prolonged duration.
A character can only have one [activated] skill active at a given time, and can't activate one while another one is active. 

It is important to note that an instant skill that applies a long lasting condition on its target(s) and an activated skill that applies the same condition are *not* the same. The effect of an activated skill only persists while the skill is active, and as such if the user is incapacitated or the skill is interrupted by any other means - as well as if the target leaves its range, usually - the effect ceases. On the other hand, an instant skill resolves immediately, and any lasting effects it may have are considered conditions applied to its target(s), meaning that they are unaffected by the skill user's status or any range consideration.
## Skill Type
The following tags are exclusive but not mandatory, at most one of them will be present for each skill.
- **Stance**: Stance skills allow the user to enter a stance *(link)*
- **Ammo**: Activating the skill provides an amount of charges, and a way of spending them. The skill's effects ends when all the charges have been spent.
*(continue)*
## Weapon
This tag notes that the skill operates through a weapon. To use a skill with the [weapon] tag, you need to have one equipped (unless otherwise specified, any weapon works).
## Arts
This tag will be present to note that a skill uses Originium Arts *(link)*, requiring the caster to be equipped with an arts unit *(link)* or to be an infected *(link)*.
# Description
Explanation of the skill's effects, further divided in several entries. Throughout a skill description, the keyword `self` is used to reference the creature using the skill.
## Require
Some skills can only be used if certain conditions are met. Such prerequisites are listed in the **Require** entry. For example:
> **Require**: `self` is wielding a melee weapon.
## Trigger
Only applies to [reaction] skills. Describes the events or conditions that need to happen to allow the use of the skill. Note that by default, using a reaction when its trigger happens is not mandatory. The [forced] tag modifies this behaviour, forcing a character to use the skill when its trigger happens if possible.
## Priority
Only applies to [reaction] skills. Specifies whether the skill is an interrupt or a followup (see [[Combat#Reactions|Reactions]]).
## Target
The **Target** entry determines what the skill will affect. It can usually be creatures - including `self` if the skill affects the user - or squares. This entry can reference the **Range** entry using the `range` keyword if relevant, in which case the latter will be present as well. For example: 
> **Target**: 1 creature in `range`

*The expression 'an ally' does not include the skill's user. Expressions like 'a creature' or 'a friendly creature' instead do, unless otherwise specified.*
## Range
Some skills have their **Target** entry limited by a range. There are three types of range: **Melee**, **Ranged** and **Area-of-Effect (AoE)**.

Melee range covers the right squares adjacent to the user. Additionally, certain skills with the [weapon] tag might list their range as `melee weapon`. This means that the skill's range is equal to that of a melee weapon used to cast the skill.

Ranged ranges affect targets further away, and can be expressed as follows:
- `ranged <number>sq`: reaches up to the specified number of squares away, counting from the skill's user.
- `ranged weapon`: can only appear if the skill has the [weapon] tag, and means that the skill's range is equal of that of the ranged weapon used to cast the skill.
- `ranged sight`: reaches up to the user's line of sight.

Some skills are not just limited by distance for their targeting, but define a specific set of squares as their range. This kind of range is referred to as Area-of-Effect (AoE) and is described by three characteristics: **point of origin**, **shape** and **size**.
### Point of Origin
The square from which the shape is drawn. It is described in two main forms: When the origin is necessarily the square occupied by Self, then it is noted with the keyword `close`, and the syntax is as follows:
> **Range**: `close <shape> <size>`

If the point of origin can instead be placed elsewhere, the syntax is instead the following:
> **Range**: `<shape> <size> <condition>`

In this case, any square that fulfills `<condition>` can be designated as origin. One common form for this is `within Xsq`, which allows the origin to be placed in any square that is no further than X squares from Self.
### Shape and Size
Several shapes are possible for AoE skills, each with its own size parameters. The options are:
- `Burst X`: Square of radius X sq centered on origin. Burst 0 represents the origin square only.
- `Diamond X`: *(that thing yk)*
- `Line X`: Line X sq long, starting from one of the 8 squares adjacent to the origin.
- `Blast NxM`: Rectangular area N by M squares, with one square of the N-length side adjacent to the origin.
## Attack
If the skill has an attack it will be described by the **Attack** entry, which defines how to build the pool for the attack roll *(link)*. For example:
> **Attack**: STR+1d

The consequences of the attack will be then explained with two additional sub-entries: **Hit**, **Critical** and **Miss**.
### Hit
All skills with an `attack` entry will include a `hit` entry describing what happens if the attack roll is successful. This often includes damage, but also debuffs, crowd-controls or any additional consequence of the attack. *This entry defines an effect, and is equivalent to `effect: if the attack succeeded, then <hit>`.*

A single attack can have multiple hits, which will be stated in the **Attack** entry.  Hits can then be defined with multiple **Hit** entries or with a single one that is repeated multiple times. In the former case, each hit is executed sequentially in order as they are written. In the latter instead, the **Hit** entry is repeated one time per hit.
### Critical
Certain attacks gain additional effects with particularly good rolls. This is called a *Critical Hit*, and the effects of it are described in this entry. **Critical** is always followed by a value, and the attack is considered a critical hit if the number of Perfects rolled is greater than or equal to this value. *This entry defines an effect, and is equivalent to `effect: if the attack succeeded and P>=<value>, then <critical>`.*
### Miss
Optional entry, describes what happens if the attack roll fails. This is often used for skills powerful enough to still inflict some damage even on miss, or if other side effects apply - including potentially to Self. *This entry defines an effect, and is equivalent to `effect: if the attack failed, then <miss>`.*
## Effect
A skill's **Effect** entry describes effects that happen regardless of whether the attack roll succeeds, or even if the skills has no attack to begin with.
## Aftereffect
Certain skills have additional effects that happen once their primary effect ends. A skill's **Aftereffect** entry defines an effect which takes place immediately after the effect listed before it completely resolves (that includes any long-lasting effect ending). As such, **Aftereffect** entries can only appear if the skill has an **Effect** in the first place. *This entry defines an effect, and is equivalent to `effect: when the previous effect ends, <aftereffect>`. It follows that multiple aftereffect entries can be present one after the other, with each one triggering once the previous finishes resolving.*
## Boost
Certain skills allow spending morale to increase their effects, when that is the case, it is shown in the **Boost** entry. Sometimes, this entry can be written as `Boost X` where X is a positive number. In that case, you can spend X morale to obtain the additional effects listed afterwards.