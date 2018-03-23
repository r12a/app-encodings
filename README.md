# Encoding converter

To use it, go to: https://r12a.github.io/app-encodings/index.html

This app allows you to see what bytes are used by legacy encodings to represent a particular character, or to convert a sequence of bytes into characters for a range of encodings. You can customise the encodings you want to experiment with by clicking on `change encodings shown`. The default selection excludes most of the single-byte encodings.

The algorithms used are based on those described in the [Encoding specification](https://encoding.spec.whatwg.org/), and thus describe the behaviour you can expect from web browsers. The transforms may not be the same as for other conversion tools. (In some cases the browsers may also produce a different result than shown here. See [the tests](http://www.w3.org/International/tests/repo/results/encoding-dbl-byte).)

*Encoding* algorithms convert Unicode characters to sequences of double-digit hex numbers that represent the bytes found in the target character encoding. A character that cannot be handled by an encoder will be represented as a decimal HTML character escape.

*Decoding* algorithms take the byte codes just mentioned and convert them to Unicode characters. The algorithm returns replacement characters where it is unable to map a given byte to the encoding.

For the decoder input you can provide a string of two-digit hex numbers separated by space or by percent signs.

Green backgrounds appear behind sequences where all characters or bytes were successfully mapped to a character in the given encoding. Beware, however, that the character mapped to may not be the one you expect – especially in the single byte encodings.

To identify characters and look up information about them you will find [UniView](http://r12a.github.io/uniview/) extremely useful. You can paste Unicode characters into the UniView `text area` and click on the down-arrow icon below to find out what they are. (Click on the name that appears for more detailed information.) It is particularly useful for identifying escaped characters. Copy the escape(s) to the `Find` input area on UniView and click on `Dec` just below.

This app also provides a couple of extra tools below the main area. One converts between hex codepoint numbers, decimal codepoint numbers and characters. Just add one of the above and remove the focus, and the other fields will be updated. The other tool allows you to create a list of all characters in various legacy encodings.
