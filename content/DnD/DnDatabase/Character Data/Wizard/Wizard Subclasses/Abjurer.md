---
publish: true
created: 2026-09-07T04:23:37.727Z
modified: 2026-09-07T06:04:46.177Z
---

## Level 3:

### Abjuration Savant

Choose two Wizard spells from the Abjuration school, each of which must be no higher than level 2, and add them to your spellbook for free.
In addition, whenever you gain access to a new level of spell slots in this class, you can add one Wizard spell from the Abjuration school to your spellbook for free. The chosen spell must be of a level for which you have spell slots. ^AbjurerLv3-1

### Arcane Ward

You can weave magic around yourself for protection. When you cast an Abjuration spell with a spell slot, you can simultaneously use a strand of the spell’s magic to create a magical ward on yourself that lasts until you finish a Long Rest. The ward has a Hit Point maximum equal to twice your Wizard level plus your Intelligence modifier. Whenever you take damage, the ward takes the damage instead, and if you have any Resistances or Vulnerabilities, apply them before reducing the ward’s Hit Points. If the damage reduces the ward to 0 Hit Points, you take any remaining damage. While the ward has 0 Hit Points, it can’t absorb damage, but its magic remains.
Whenever you cast an Abjuration spell with a spell slot, the ward regains a number of Hit Points equal to twice the level of the spell slot. Alternatively, as a Bonus Action, you can expend a spell slot, and the ward regains a number of Hit Points equal to twice the level of the spell slot expended.
Once you create the ward, you can’t create it again until you finish a Long Rest. ^AbjurerLv3-2

## Level 6:

### Projected Ward

When a creature that you can see within 30 feet of yourself takes damage, you can take a Reaction to cause your Arcane Ward to absorb that damage. If this damage reduces the ward to 0 Hit Points, the warded creature takes any remaining damage. If that creature has any Resistances or Vulnerabilities, apply them before reducing the ward’s Hit Points. ^AbjurerLv6

## Level 10:

### Spell Breaker

You always have the Counterspell and Dispel Magic spells prepared. In addition, you can cast Dispel Magic as a Bonus Action, and you can add your Proficiency Bonus to its ability check.
When you cast either spell with a spell slot, that slot isn’t expended if the spell fails to stop a spell. ^AbjurerLv10

## Level 14: Spell Resistance

You have Advantage on saving throws against spells, and you have Resistance to the damage of spells. ^AbjurerLv14

## Features

```meta-bind-js-view
{Wizard#Level} as progression
---
const WizLevel = context.bound.progression;

// conditional checks to output custom text
if (WizLevel < 6) {
    return engine.markdown.create('## [Abjuration Savant](Abjurer#^AbjurerLv3-1)<br>[Arcane Ward](Abjurer#^AbjurerLv3-2) ^Abjurer');
} else if(WizLevel < 10){
	return engine.markdown.create('## [Abjuration Savant](Abjurer#^AbjurerLv3-1)<br>[Arcane Ward](Abjurer#^AbjurerLv3-2)<br>[Projected Ward](Abjurer#^AbjurerLv6) ^Abjurer');
} else if (WizLevel < 14) {
    return engine.markdown.create('## [Abjuration Savant](Abjurer#^AbjurerLv3-1)<br>[Arcane Ward](Abjurer#^AbjurerLv3-2)<br>[Projected Ward](Abjurer#^AbjurerLv6)<br>[Spell Breaker](Abjurer#^AbjurerLv10) ^Abjurer');
} else {
    return engine.markdown.create('## [Abjuration Savant](Abjurer#^AbjurerLv3-1)<br>[Arcane Ward](Abjurer#^AbjurerLv3-2)<br>[Projected Ward](Abjurer#^AbjurerLv6)<br>[Spell Breaker](Abjurer#^AbjurerLv10)<br>[Spell Resistance](Abjurer#^AbjurerLv14) ^Abjurer');
}
```

#Wizard
#Wizard-Subclasses
#Character-Data
