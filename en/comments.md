# Comments

Comments serve as a sort of in-code documentation.
When inserted into a code, they are effectively ignored by the implementation;
they are solely intended to be used as notes by the humans that read source code.

## Syntax

`/: comment :/` (1)

`/:/` (2)

 1) "multi-line" comment also known as "C-style" comment.
 2) "triplet" comment also known as "stupid" comment.

All comments are removed from the code by the lexer before the preprocessor.

## Multi-line

Multi-line comments are usually used to comment large blocks of text
or small fragments of code; however, they can be used to comment single lines.
To insert text as a comment, simply surround the text with `/:` and `:/`.
Multi-line comments tell the implementation to ignore all content between `/:` and `:/`.

Except within a character constant, a string literal, or a comment, the characters `/:` introduce a comment.
Multi-line comments cannot be nested.

## Triplet

Triplet comments are usually used to comment nothing.
To insert a triplet comment, simply write `/:/`.
The triplet comment is a shorter version of the empty multi-line comment `/::/`.

Except within a character constant, a string literal, or a comment, the characters `/:/` is a comment.
Triplet comments cannot be nested.

## Example

```
/:
Multi-line comments can contain
multiple lines.
:/
 
/: Or, just one line. :/

/:----------------------------------------------------------------:/

/::/

/:/
```
