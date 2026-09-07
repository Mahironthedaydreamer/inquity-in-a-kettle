---
publish: true
created: 2026-09-07T04:23:37.727Z
modified: 2026-09-07T06:04:46.126Z
---

## Level 3

### Spellcasting

You have learned to cast spells. The information below details how you use those rules as an Eldritch Knight.

_**Cantrips.**_ You know two cantrips of your choice from the Wizard spell list (see that class’s section for its list). Ray of Frost and Shocking Grasp are recommended. Whenever you gain a Fighter level, you can replace one of these cantrips with another cantrip of your choice from the Wizard spell list.

When you reach Fighter level 10, you learn another Wizard cantrip of your choice.

_**Spell Slots.**_ The Eldritch Knight Spellcasting table shows how many spell slots you have to cast your level 1+ spells. You regain all expended slots when you finish a Long Rest.

_**Prepared Spells of Level 1+.**_ You prepare the list of level 1+ spells that are available for you to cast with this feature. To start, choose three level 1 spells from the Wizard spell list. Burning Hands, Jump, and Shield are recommended.

The number of spells on your list increases as you gain Fighter levels, as shown in the Prepared Spells column of the Eldritch Knight Spellcasting table. Whenever that number increases, choose additional spells from the Wizard spell list until the number of spells on your list matches the number on the table. The chosen spells must be of a level for which you have spell slots. For example, if you’re a level 7 Fighter, your list of prepared spells can include five Wizard spells of levels 1 and 2 in any combination.

_**Changing Your Prepared Spells.**_ Whenever you gain a Fighter level, you can replace one spell on your list with another Wizard spell for which you have spell slots.

_**Spellcasting Ability.**_ Intelligence is your spellcasting ability for your Wizard spells.

_**Spellcasting Focus.**_ You can use an Arcane Focus as a Spellcasting Focus for your Wizard spells.

### War Bond

You learn a ritual that creates a magical bond between yourself and one weapon. You perform the ritual over the course of 1 hour, which can be done during a Short Rest. The weapon must be within your reach throughout the ritual, at the conclusion of which you touch the weapon and forge the bond. The bond fails if another Fighter is bonded to the weapon or if the weapon is a magic item to which someone else is attuned.

Once you have bonded a weapon to yourself, you can’t be disarmed of that weapon unless you have the Incapacitated condition. If it is on the same plane of existence, you can summon that weapon as a Bonus Action, causing it to teleport instantly to your hand.

You can have up to two bonded weapons, but you can summon only one at a time with a Bonus Action. If you attempt to bond with a third weapon, you must break the bond with one of the other two.

## Level 7

### War Magic

When you take the Attack action on your turn, you can replace one of the attacks with a casting of one of your Wizard cantrips that has a casting time of an action. ^EldritchKnightLv7

## Level 10

### Eldritch Strike

You learn how to make your weapon strikes undercut a creature’s ability to withstand your spells. When you hit a creature with an attack using a weapon, that creature has Disadvantage on the next saving throw it makes against a spell you cast before the end of your next turn. ^EldritchKnightLv10

## Level 15

### Arcane Charge

When you use your Action Surge, you can teleport up to 30 feet to an unoccupied space you can see. You can teleport before or after the additional action. ^EldritchKnightLv15

## Level 18

### Improved War Magic

You can replace 2 of the attacks with a casting of one of your level 1 or level 2 Wizard spells that has a casting time of action. ^EldritchKnightLv18

#Character-Data
#Fighter
#Fighter-Subclasses
#Spell-User

## Tracker

```meta-bind-js-view
{Fighter#Level} as progression
---
const spellsPrepped = context.bound.progression;

// JavaScript conditional checks to output custom text
if (spellsPrepped < 3) {
    return engine.markdown.create('## Spells Prepared: 0');
} else if (spellsPrepped < 4) {
    return engine.markdown.create('## Spells Prepared: 3 | Level 1: 2');
} else if (spellsPrepped < 7){
	return engine.markdown.create('## Spells Prepared: 4 | Level 1: 3');
} else if (spellsPrepped < 8){
	return engine.markdown.create('## Spells Prepared: 5 | Level 1: 4 | Level 2: 2');
} else if (spellsPrepped < 10){
	return engine.markdown.create('## Spells Prepared: 6 | Level 1: 4 | Level 2: 2');
} else if(spellsPrepped < 11){
	return engine.markdown.create('## Spells Prepared: 7 | Level 1: 4 | Level 2: 3');
} else if(spellsPrepped < 13){
	return engine.markdown.create('## Spells Prepared: 8 | Level 1: 4 | Level 2: 3');
} else if(spellsPrepped < 14){
	return engine.markdown.create('## Spells Prepared: 9 | Level 1: 4 | Level 2: 3 | Level 3: 2');
} else if(spellsPrepped < 16){
	return engine.markdown.create('## Spells Prepared: 10 | Level 1: 4 | Level 2: 3 | Level 3: 3');
} else if(spellsPrepped < 19){
	return engine.markdown.create('## Spells Prepared: 11 | Level 1: 4 | Level 2: 3 | Level 3: 3');
} else if(spellsPrepped < 20){
	return engine.markdown.create('## Spells Prepared: 12 | Level 1: 4 | Level 2: 3 | Level 3: 3 | Level 4: 1');
} else {
    return engine.markdown.create('## Spells Prepared: 13 | Level 1: 4 | Level 2: 3 | Level 3: 3 | Level 4: 1');
}
```
