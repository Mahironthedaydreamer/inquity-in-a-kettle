---
publish: true
created: 2026-09-07T04:23:37.722Z
modified: 2026-09-07T06:04:46.072Z
---

## Level : `INPUT[slider(minValue(1), maxValue(20), addLabels(true)):Level ]`

## [Cantrips](SpellsBasics.md#^Cantrips): `VIEW[ ({Level} < 4) ? "3" : ({Level} < 10) ? "4" : "5"]`|  [Prepared Spells](SpellsBasics.md#^SpellPrep):`VIEW[({Level}<2)?"4":({Level}<3)?"5":({Level}<4)?"6":({Level}<5)?"7":({Level}<6)?"9":({Level}<7)?"10":({Level}<8)?"11":({Level}<9)?"12":({Level}<10)?"14":({Level}<11)?"15":({Level}<13)?"16":({Level}<14)?"17":({Level}<15)?"18":({Level}<16)?"19":({Level}<17)?"21":({Level}<18)?"22":({Level}<19)?"23":({Level}<20)?"24":"25"]`

## [Spell Slots](SpellsBasics.md#^SpellSlot):

### Lv1:`VIEW[ ({Level} < 2) ? "2," : ({Level} < 3) ? "3," : "4,"]`Lv2:`VIEW[ ({Level} < 3) ? "- ," : ({Level} < 4) ? "2," : "3,"]`Lv3:`VIEW[ ({Level} < 5) ? "- ," : ({Level} < 5) ? "2," : "3,"]`Lv4:`VIEW[ ({Level} < 7) ? "-" : ({Level} < 8) ? "1" : ({Level} < 9) ? "2" : "3"]`

### Lv5:`VIEW[ ({Level} < 9) ? "- ," : ({Level} < 10) ? "1," : "2,"]`Lv6:`VIEW[ ({Level} < 11) ? "- ," : ({Level} < 19) ? "1," : "2,"]`Lv7:`VIEW[ ({Level} < 13) ? "- ," : ({Level} < 20) ? "1," : "2,"]`Lv8:`VIEW[ ({Level} < 15) ? "- ," : "1,"]`Lv9:`VIEW[ ({Level} < 17) ? "-" : "1"]`

## Subclass `INPUT[inlineSelect(option(Select a subclass), option(Abjurer), option(Diviner), option(Evoker), option(Illusionist)):WizardSubclass]`

```meta-bind-js-view
{WizardSubclass} as chosenOption
---
const selection = context.bound.chosenOption;
if (!selection) return engine.markdown.create("*Please select an option.*");

// Dynamically construct a standard Obsidian file link or heading embed
// Example target: ![[DataFile#Option A]]
const embedString = `![[${selection}#Features]]`;

return engine.markdown.create(embedString);
```

---

## Class Description

```meta-bind-js-view
{Level} as statusNumber
---
const maxNum = context.bound.statusNumber;
if (!maxNum || maxNum < 1) return "Select a status number.";

const fileMap = {
	1: "Wizard Level 1",
	2: "Wizard Level 2",
	3: "Wizard Level 3",
	4: "Wizard Level 4",
	5: "Wizard Level 5",
	6: "Wizard Level 6",
	7: "Wizard Level 7",
	8: "Wizard Level 8",
	9: "Wizard Level 9",
	10: "Wizard Level 10",
	11: "Wizard Level 11",
	12: "Wizard Level 12",
	13: "Wizard Level 13",
	14: "Wizard Level 14",
	15: "Wizard Level 15",
	16: "Wizard Level 16",
	17: "Wizard Level 17",
	18: "Wizard Level 18",
	19: "Wizard Level 19",
	20: "Wizard Level 20",
};

let accumulatedMarkdown = "";

for (let i = maxNum; i >= 1; i--) {
    const fileName = fileMap[i];
    if (!fileName) continue;

    // This dynamically creates standard Obsidian embeds ![[FileName]] on the fly
    accumulatedMarkdown += `### ![[${fileName}]]\n\n`;
}

return engine.markdown.create(accumulatedMarkdown);
```

---

#Character-Classes
#Wizard
