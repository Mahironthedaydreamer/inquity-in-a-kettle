---
publish: true
created: 2026-09-07T04:23:37.727Z
modified: 2026-09-07T06:04:46.189Z
---

## Level 3:

### Illusion Savant

Choose two Wizard spells from the Illusion school, each of which must be no higher than level 2, and add them to your spellbook for free.
In addition, whenever you gain access to a new level of spell slots in this class, you can add one Wizard spell from the Illusion school to your spellbook for free. The chosen spell must be of a level for which you have spell slots. ^IlluLv3-1

### Improved Illusions

You can cast Illusion spells without providing Verbal components, and if an Illusion spell you cast has a range of 10+ feet, the range increases by 60 feet.
You also know the Minor Illusion cantrip. If you already know it, you learn a different Wizard cantrip of your choice. The cantrip doesn’t count against your number of cantrips known. You can create both a sound and an image with a single casting of Minor Illusion, and you can cast it as a Bonus Action. ^IlluLv3-2

## Level 6:

### Phantasmal Creatures

You always have the Summon Beast and Summon Fey spells prepared. Whenever you cast either spell, you can change its school to Illusion, which causes the summoned creature to appear spectral. You can cast the Illusion version of each spell without expending a spell slot, but casting it without a slot halves the creature’s Hit Points. Once you cast either spell without a spell slot, you must finish a Long Rest before you can cast the spell in that way again. ^IllusionistLv6

## Level 10:

### Illusory Self

When a creature hits you with an attack roll, you can take a Reaction to interpose an illusory duplicate of yourself between the attacker and yourself. The attack automatically misses you, then the illusion dissipates.
Once you use this feature, you can’t use it again until you finish a Short or Long Rest. You can also restore your use of it by expending a level 2+ spell slot (no action required). ^IllusionistLv10

## Level 14:

### Illusory Reality

You have learned to weave shadow magic into your illusions to give them a semi-reality. When you cast an Illusion spell with a spell slot, you can choose one inanimate, nonmagical object that is part of the illusion and make that object real. You can do this on your turn as a Bonus Action while the spell is ongoing. The object remains real for 1 minute, during which it can’t deal damage or give any conditions. For example, you can create an illusion of a bridge over a chasm and then make it real and cross it. ^IllusionistLv14

## Features

```meta-bind-js-view
{Wizard#Level} as progression
---
const WizLevel = context.bound.progression;

// conditional checks to output custom text
if (WizLevel < 6) {
    return engine.markdown.create('## [Illusion Savant](Illusionistonist#^IlluLv3-1)<br>[Improved Illusions](Illusionist#IlluLvLv3-2) ^Illusionist');
} else if(WizLevel < 10){
	return engine.markdown.create('## [Illusion Savant](Illusionist#^IlluLv3-1)<br>[Improved Illusions](Illusionist#^IlluLv3-2)<br>[Phantasmal Creatures](Illusionist#^IllusionistLv6) ^Illusionist');
} else if (WizLevel < 14) {
    return engine.markdown.create('## [Illusion Savant](Illusionist#^IlluLv3-1)<br>[Improved Illusions](Illusionist#^IlluLv3-2)<br>[Phantasmal Creatures](Illusionist#^IllusionistLv6)<br>[Illusory Self](Illusionist#^IllusionistLv10) ^Illusionist');
} else {
    return engine.markdown.create('## [Illusion Savant](Illusionist#^IlluLv3-1)<br>[Improved Illusions](Illusionist#^IlluLv3-2)<br>[Phantasmal Creatures](Illusionist#^IllusionistLv6)<br>[Illusory Self](Illusionist#^IllusionistLv10)<br>[Illusory Reality](Illusionist#^IllusionistLv14) ^Illusionist');
}
```

#Wizard
#Wizard-Subclasses
#Character-Data
