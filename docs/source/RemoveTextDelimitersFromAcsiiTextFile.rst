RemoveTextDelimitersFromAsciiTextFile
===============================

https://github.com/theonetruenerd/VenusPackages/blob/main/RemoveTextDelimitersFromAsciiTextFile.pkg

The RemoveTextDelimitersFromAsciiFile library adds a single function which edits a file to remove all delimiters from the Ascii file at the given file path. 

- :py:func:`RemoveTextDelimitersFromAsciiTextFile`

.. py:function:: RemoveTextDelimitersFromAsciiTextFile(variable fileName)

  This function removes any text delimiters from the Ascii text file at the specified file path. It edits the file rather than outputting a copy.

  :params fileName: The file path of the text file to be edited
  :type fileName: Variable
  :return: Boolean of whether the text file was found (hslTrue) or not found (hslFalse)
  :rtype: Boolean

