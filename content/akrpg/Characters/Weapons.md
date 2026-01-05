Whether it's a guard's blade, a caster's staff or a defender's shield, characters use weapons to help them in combat. Each weapon provides a character with a basic attack *(link)*, and some grant additional skills as well. Many other skills also require a weapon to be used, and might make use of some of the weapon's attributes.
## How to read a weapon
Each weapon is described by a name, a series of attributes, and one or more skills.
### Name
The weapon's name. *Weapons here presented are to be treated as templates, a player might want to give their character's weapon a more specific name and description if it better matches their character's background, without affecting its attributes.*
### Class
Weapons are divided into classes, a character can only benefit from a weapon belonging to a class they are proficient with.
### Tags
Each weapon has a list of tags defining additional properties of the weapon.
### Handling
The handling attribute represents how easy a weapon is to use effectively in combat. Handling is expressed as a positive or negative number, and is added as an ATK bonus (or penalty if negative) to each attack roll made with the weapon.
### Range (optional)
Any weapon with the [ranged] tag will detail its range here, expressed as a number of squares. *(maybe minimum/optimal/long?)*
### Damage
The weapon's base damage, referred to as `W` and used by many [weapon] skills in their damage formula.
### AP (optional)
Weapons with the [armor piercing] tag can more easily penetrate their target's defenses. When these weapons inflict physical damage *(link)*, reduce the target's DEF by the weapon's **AP** attribute for the damage calculation only. *When reduced this way, DEF cannot go below 1 unless it was already 0 before applying AP.* 
### Reload (optional)
Certain weapons need an extended amount of time to be readied for attacking again after an amount of consecutive uses. When a weapon has the [reload] tag, this attribute will be present. Reload is expressed as `<actions>/<capacity>`, meaning that every `<capacity>` attacks done with the weapon, `<actions>` actions need to be spent reloading it. If a character's ASPD is less than the reload time for the weapon, multiple turns need to be spent reloading. *The reload actions are considered each a separate part of the process and don't necessarily need to be taken consecutively, nor they prevent the character from doing anything else in between. For example, a reload of 2 actions might consist in one action to remove the empty magazine and one other action to insert a new one.*
### Skills
A weapon can have one or more skills available to anyone wielding it, as long as they are proficient with the weapon's class. All weapons except for Auxiliary Arts Units *(link)* have a basic attack skill, and some weapons can have additional skills.
# Weapon Classes
## Swords?
## Spears?
## Hammers?
## Shields
## Hybrid Weapons?
## Crossbows?
## Siege Weapons?
## Firearms?
## Core Arts Units?
## Splash Arts Units?
## Healing Arts Units?
## Hybrid Arts Units?
## Auxiliary Arts Units
# Weapon Tags
The following tags can appear on weapons:
- **Melee**: the weapon has melee attacks and can be used for melee skills
- **Ranged**: the weapon has ranged attacks and can be used for ranged skills
- **Reload**: the weapon requires actions to reload
- **Armor Piercing**: the weapon can ignore part of the target's DEF
- **Integrated Arts Unit**:  The weapon has a built-in arts unit and can be used for [arts] skills in place of a standalone arts unit.