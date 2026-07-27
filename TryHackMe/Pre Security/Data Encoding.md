**Learning Objectives**


* ASCII
* Unicode
* UTF-8, UTF-16, and UTF-32
* How emoji is encoded
* what causes weird gibberish characters

**ASCII**

* ASCII stands for American Standard Code for Information Interchange, and it is an early character encoding from 1963 that uses numbers 0-127 to represent English letters, digits, punctuation, and some control characters.
* The original ASCII was limited to seven bits. 
* ASCII acts as a small bilingual dictionary between text and numeric codes. Consider the following samples from the original ASCII table. Since the table has 128 entries, we only made a brief selection to give you an idea of how things are represented in ASCII.

## ASCII Character Reference Table

| Decimal | Hexadecimal | Binary | Symbol | Description |
|---------:|:-----------:|:------:|:------:|-------------|
| ... | ... | ... | ... | ... |
| 48 | 30 | 00110000 | 0 | Zero |
| ... | ... | ... | ... | ... |
| 57 | 39 | 00111001 | 9 | Nine |
| ... | ... | ... | ... | ... |
| 65 | 41 | 01000001 | A | Uppercase A |
| ... | ... | ... | ... | ... |
| 88 | 58 | 01011000 | X | Uppercase X |
| 89 | 59 | 01011001 | Y | Uppercase Y |
| 90 | 5A | 01011010 | Z | Uppercase Z |
| 91 | 5B | 01011011 | [ | Opening bracket |
| 92 | 5C | 01011100 | \ | Backslash |
| 93 | 5D | 01011101 | ] | Closing bracket |
| 94 | 5E | 01011110 | ^ | Caret (Circumflex) |
| 95 | 5F | 01011111 | _ | Underscore |
| 96 | 60 | 01100000 | ` | Grave accent |
| 97 | 61 | 01100001 | a | Lowercase a |
| 98 | 62 | 01100010 | b | Lowercase b |
| 99 | 63 | 01100011 | c | Lowercase c |
| ... | ... | ... | ... | ... |
| 122 | 7A | 01111010 | z | Lowercase z |
| ... | ... | ... | ... | ... |
| 127 | 7F | 01111111 | DEL | Delete |


**Unicode**

* Unicode is a universal character encoding standard. It assigns unique code points to characters from all modern and historical writing systems worldwide. Unicode supports the interchange, processing, and display of text in diverse languages. 
* This makes it easy to use different languages in a single file or message.

**UTF-8, UTF-16, and UTF-32**

* It encodes Unicode points into 1 to 4 bytes dynamically. In other words, it decides on the number of bytes based on the character complexity. ASCII characters (U+0000 to U+007F) use exactly 1 byte, identical to the original ASCII, ensuring seamless backward compatibility. 
*  Non-ASCII characters like Ω (U+03A9) use 2 bytes, while complex scripts or emoji like 🔥 (U+1F525) require 4 bytes.

conclusion - 

we learned about ASCII and its limitations, and about Unicode and three encoding standards: UTF-8, UTF-16, and UTF-32. We explored how Unicode enables us to cover not only the world’s languages but also symbols such as chess pieces and emojis.


