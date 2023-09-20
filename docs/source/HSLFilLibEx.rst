HSLFileLibEx
=============================

HSLFilLibEx allows you to manipulate files. It adds the following functions:

- :py:func:`FilCopyFileEx`
- :py:func:`FilDeleteFileEx`
- :py:func:`FilFormatReportFileEx`

.. py:function:: FilCopyFileEx(variable SourceFilePathName, variable DestinationFilePathName)

  This function creates a copy of the specified file, which will be placed in the specified new location

  :params SourceFilePathName: The path to the file which you wish to copy, including the file name and extension
  :params DestinationFilePathName: The path to which you would like to copy the file, including the file name and extension
  :type SourceFilePathName: Variable
  :type DestinationFilePathName: Variable 
  :return: None
  :rtype: N/A

.. py:function:: FilDeleteFileEx(variable FilePathName)

  This function deletes the file at the specified location

  :params FilePathName: The path to the file which you wish to delete, including file name and extension
  :type FilePathName: Variable
  :return: None
  :rtype: N/A

.. py:function:: FilFormatReportFileEx(variable SourceFilePathName, variable DestinationFilePathName)

  This function creates a formatted/filtered copy of the specified report file. It searches the file for the string "Element Name" and copies any subsequent lines to the new file.

  :params SourceFilePathName: The path to the file which you wish to format, including file name and extension
  :params DestinationFilePathName: The path to the file you would like to create the formatted report in, including file name and extension.
  :type SourceFilePathName: Variable
  :type DestinationFilePathName: Variable
  :return: None
  :rtype: N/A
