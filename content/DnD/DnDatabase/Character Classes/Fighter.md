---
publish: true
created: 2026-09-07T04:23:37.722Z
modified: 2026-09-07T06:04:46.068Z
---

## Level: `INPUT[slider(minValue(1), maxValue(20), addLabels(true)):Level]` | Second Wind (D10) charges: `VIEW[ ({Level} < 3) ? "2" : ({Level} < 10) ? "3" : "4" ]`

## Subclass `INPUT[inlineSelect(option(Select a subclass), option(BattleMaster), option(Champion), option(EldritchKnight), option(PsiWarrior)):FighterSubclass]`

```meta-bind-js-view
{FighterSubclass} as chosenOption
---
const selection = context.bound.chosenOption;
if (!selection) return engine.markdown.create("*Please select an option.*");

// Dynamically construct a standard Obsidian file link or heading embed
// Example target: ![[DataFile#Option A]]
const embedString = `![[${selection}#Tracker]]`;

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
	1: "Fighter Level1",
	2: "Fighter Level2",
	3: "Fighter Level3",
	4: "Fighter Level4",
	5: "Fighter Level5",
	6: "Fighter Level6",
	7: "Fighter Level7",
	8: "Fighter Level8",
	9: "Fighter Level9",
	10: "Fighter Level10",
	11: "Fighter Level11",
	12: "Fighter Level12",
	13: "Fighter Level13",
	14: "Fighter Level14",
	15: "Fighter Level15",
	16: "Fighter Level16",
	17: "Fighter Level17",
	18: "Fighter Level18",
	19: "Fighter Level19",
	20: "Fighter Level20",
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

## Subclass Description

```meta-bind-js-view
{FighterSubclass} as selected
---
if (!context.bound.selected) { return engine.markdown.create("*Please select a file from the dropdown above.*"); } // Creates an internal markdown embed link based on the frontmatter selection
const embedString = `![[${context.bound.selected}]]`;
return engine.markdown.create(embedString);
```

#Character-Classes
#Fighter
