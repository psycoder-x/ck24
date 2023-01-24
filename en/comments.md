# Comments

Comments serve as a sort of in-code documentation.
When inserted into a code, they are effectively ignored by the implementation;
they are solely intended to be used as notes by the humans that read source code.

## Syntax

```
/: comment :/
```

All comments are removed from the code by the lexer before the preprocessor.

## Multi-line

Multi-line comments are usually used to comment large blocks of text
or small fragments of code; however, they can be used to comment single lines.
To insert text as a comment, simply surround the text with `/:` and `:/`.
Multi-line comments tell the implementation to ignore all content between `/:` and `:/`.

Except within a character constant, a string literal, or a comment, the characters `/:` introduce a comment.
Multi-line comments cannot be nested.

## Example

```
/:
Multi-line comments can contain
multiple lines.
:/
 
/: Or, just one line. :/
```
