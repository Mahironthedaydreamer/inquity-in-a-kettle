---
publish: true
created: 2026-09-07T04:23:37.727Z
modified: 2026-09-07T06:04:46.180Z
---

## Level 3:

### Divination Savant

Choose two Wizard spells from the Divination school, each of which must be no higher than level 2, and add them to your spellbook for free.
In addition, whenever you gain access to a new level of spell slots in this class, you can add one Wizard spell from the Divination school to your spellbook for free. The chosen spell must be of a level for which you have spell slots. ^DivLv3-1

### Portent

Glimpses of the future begin to press on your awareness. Whenever you finish a Long Rest, roll 2D20 and record the numbers rolled. You can replace any D20 Test made by you or a creature that you can see with one of these foretelling rolls. You must choose to do so before the roll, and you can replace a roll in this way only once per turn.
Each foretelling roll can be used only once. When you finish a Long Rest, you lose any unused foretelling rolls. ^DivLv3-2

## Level 6:

### Expert Divination

Casting Divination spells comes so easily to you that it expends only a fraction of your spellcasting efforts. When you cast a Divination spell using a level 2+ spell slot, you regain one expended spell slot. The slot you regain must be of a level lower than the slot you expended and can’t be higher than level 5. ^DivinerLv6

## Level 10:

### The Third Eye

You can increase your powers of perception. As a Bonus Action, choose one of the following benefits, which lasts until you start a Short or Long Rest. You can’t use this feature again until you finish a Short or Long Rest.
**Darkvision.** You gain Darkvision with a range of 120 feet.
**Greater Comprehension.** You can read any language.
**See Invisibility.** You can cast See Invisibility without expending a spell slot. ^DivinerLv10

## Level 14:

### Greater Portent

The visions in your dreams intensify and paint a more accurate picture in your mind of what is to come. Roll 3D20 for your Portent feature rather than two. ^DivinerLv14

## Features

```meta-bind-js-view
{Wizard#Level} as progression
---
const WizLevel = context.bound.progression;

// conditional checks to output custom text
if (WizLevel < 6) {
    return engine.markdown.create('## [Divination Savant](Diviner#^DivLv3-1)<br>[Portent](Diviner#^DivLv3-2) ^Diviner');
} else if(WizLevel < 10){
	return engine.markdown.create('## [Divination Savant](Diviner#^DivLv3-1)<br>[Portent](Diviner#^DivLv3-2)<br>[Expert Divination](Diviner#^DivinerLv6) ^Diviner');
} else if (WizLevel < 14) {
    return engine.markdown.create('## [Divination Savant](Diviner#^DivLv3-1)<br>[Portent](Diviner#^DivLv3-2)<br>[Expert Divination](Diviner#^DivinerLv6)<br>[The Third Eye](Diviner#^DivinerLv10) ^Diviner');
} else {
    return engine.markdown.create('## [Divination Savant](Diviner#^DivLv3-1)<br>[Portent](Diviner#^DivLv3-2)<br>[Expert Divination](Diviner#^DivinerLv6)<br>[The Third Eye](Diviner#^DivinerLv10)<br>[Greater Portent](Diviner#^DivinerLv14) ^Diviner');
}
```

#Wizard
#Wizard-Subclasses
#Character-Data
