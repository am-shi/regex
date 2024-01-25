# regex
learning regex.

My notes:
All of the regex answers are formatted like this: / regex /g
-The period . allows selecting any character, including special characters and spaces

-Character Sets [abc]
If one of the characters in a word can be various characters, we write it in square brackets [] with all alternative characters. For example, to write an expression that can find all the words in the text, type the characters a, e, i, o, u adjacently within square brackets [].

text: bar ber bir bor bur
regex: b[aeiou]r

-Negated Character Sets [^abc]
To find all words in the text below, except for ber and bor, type e and o side by side after the caret ^ character inside square brackets [].

text: bar ber bir bor bur
regex :b[^eo]r
so the result was: bar,bir,bur (everything except e and o)

-Letter Range[a-z]
To find the letters in the specified range, the starting letter and the ending letter are written in square brackets [] with a dash between them -. It is case-sensitive. Type the expression that will select all lowercase letters between e and o, including themselves.

text: abcdefghijklmnopqrstuvwxyz
regex: [e-o]
result: everything from e to o

-Number Range[0-9]
To find the numbers in the specified range, the starting number and the ending number are written in square brackets [] with a dash - between them. Write an expression that will select all numbers between 3 and 6, including themselves.

text: 0123456789
regex:[3-6]

-Practice: Any Character
Type the expression to select individual letters, numbers, spaces, and special characters in the text. The expression you type must match any character.

text: az AZ 09 _- = !? ., :;
regex: /./g
selected all of them

-Practice: Character Sets
Write the phrase that matches each word in the text. The only characters that change are the initials of the words.

text: beer deer feer
regex: [bdf]eer

-Practice: Negated Character Sets
Write down the expression that will match anything other than the words beor and beur in the text. Do this using the negated character set.

text: bear beor beer beur
regex: be[^ou]r

