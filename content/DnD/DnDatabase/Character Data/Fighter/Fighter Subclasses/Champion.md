---
publish: true
created: 2026-09-07T04:23:37.726Z
modified: 2026-09-07T06:04:46.123Z
---

## Level 3

### Improved Critical

Your attack rolls with weapons and Unarmed Strikes can score a Critical Hit on a roll of 19 or 20 on the D20.

### Remarkable Athlete

Thanks to your athleticism, you have Advantage on Initiative rolls and Strength (Athletics) checks.
In addition, immediately after you score a Critical Hit, you can move up to half your Speed without provoking Opportunity Attacks.

## Level 7

### Additional Fighting Style

You gain another Fighting Style feat of your choice. ^ChampionLv7

## Level 10

### Heroic Warrior

The thrill of battle drives you toward victory. During combat, you can give yourself Heroic Inspiration whenever you start your turn without it. ^ChampionLv10

## Level 15

### Superior Critical

Your attack rolls with weapons and Unarmed Strikes can now score a Critical Hit on a roll of 18–20 on the D20. ^ChampionLv15

## Level 18

### Survivor

You attain the pinnacle of resilience in battle, giving you these benefits.
_**Defy Death.**_ You have Advantage on Death Saving Throws. Moreover, when you roll 18–20 on a Death Saving Throw, you gain the benefit of rolling a 20 on it.
_**Heroic Rally.**_ At the start of each of your turns, you regain Hit Points equal to 5 plus your Constitution modifier if you are Bloodied and have at least 1 Hit Point. ^ChampionLv18

#Character-Data
#Fighter
#Fighter-Subclasses

## Tracker

```meta-bind-js-view
{Fighter#Level} as progression
---
const betterCrit = context.bound.progression;

// conditional checks to output custom text
if (betterCrit < 15) {
    return engine.markdown.create('## Critical Threshold: 19-20');
} else {
    return engine.markdown.create('## Critical Threshold: 18-20');
}
```
