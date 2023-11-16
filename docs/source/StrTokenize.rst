StrTokenize
=====================

https://github.com/theonetruenerd/VenusPackages/blob/main/StrTokenize.pkg

The string tokenize library allows you to split a string into an array based on delimiters. It adds one function:

- :ven:func:`StrTokenize`

.. ven:function:: StrTokenize(variable strIn, variable strDelimiter, array arrTokens, boolean bAttendEmptyTokens)

	This function takes the input string and splits it at any point where it finds the specified delimiter, returning the substrings as members of an array. Can be told to add empty strings or not (occurs when the delimiter appears twice in a row).

	:params strIn: The input string to be split
	:params strDelimiter: The character to be used as the delimiter
	:params arrTokens: The output array of split-substrings
	:params bAttendEmptyTokens: Boolean determining whether to include empty substrings or not in the array
	:type strIn: Variable
	:type strDelimiter: Variable
	:type arrTokens: Array
	:type bAttendEmptyTokens: Variable
	:return: None
	:rtype: N/A
