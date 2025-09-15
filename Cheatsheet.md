Links / Choices

## Simple link:
[[Go to "Passage"]]

Link + set variable + jump:
(link: "Option")[(set: $variable to "Value")(goto: "Passage")]

Clickable text, sets a variable, moves to another passage.

## Variables

Create / set variable:
(set: $variable to "text")

(set: $score to 0)

(set: $flag to true)

Modify numeric variable:
(set: $score to $score + 1)

Variables store numbers, text, booleans, or lists.
Conditional display:

(if: $variable is "Value")[Text if true](else:)[Text if false]

## Conditional Logic

If / Else-if / Else:

(if: $score > 10)[Win!]

(else-if: $score > 5)[Almost!]

(else:)[Try again!]

Multiple conditions (AND / OR):

(if: $flag and $score > 5)[You can enter]

(if: $flag or $variable is "Value")[One condition is true]


## Lists / Loops

(set: $inventory to (a: "Sword", "Shield"))

Add / remove items:

(push: $inventory, "Potion")

(remove: $inventory, "Sword")

Loop through list:

(for: each _item, ...$inventory)[I have _item.]

## Styling

Bold / Italics:

Bold ''Italic''

Text color: (text-color: red)["Danger!"]

Size and font:

(font: "Courier New")[Monospaced text]

(font-size: 20pt)[Big text]

### Mini Example – Choice + Variable

(link: "Tall")[(set: $height to "Tall")(goto: "Summary")]

(link: "Short")[(set: $height to "Short")(goto: "Summary")]

(if: $height is "Tall")[You reach the top shelf.]

(else:)[You cannot reach it.]

# Common Macros

(set:) – Assign or change variable – (set: $score to 1)

(if:) – Conditional display – (if: $flag)[Text]

(else-if:) – Alternate condition – (else-if: $score > 5)[Almost]

(else:) – Default if conditions fail – (else:)[Try again]

(link:) – Clickable text – (link: "Go")[...]

(goto:) – Jump to another passage – (goto: "Passage")

(display:) – Show another passage inline – (display: "Stats")

(for:) – Loop through list or repeat content – (for: each _item, ...$inventory)[_item]

(replace:) – Replace content of a passage or variable – (replace: ?box)[New text]

(append:) – Add text to existing element – (append: ?box)[More text]

(prepend:) – Add text to start of element – (prepend: ?box)[Intro text]

(mouseover:) – Text appears on hover – (mouseover: "Hover me")[Surprise!]

(toggle:) – Show/hide content on click – (toggle: "More info")[Extra details]

(event:) – Run code when event happens – (event: "click")[ (set: $flag to true) ]

(print:) – Display variable or value – (print: $score)
