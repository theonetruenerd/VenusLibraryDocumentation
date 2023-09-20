HSLFilLib - unfinished
================================

This library allows interaction with and manipulation of files present on the host computer. It adds the following functions: 

- :py:func:`FilEof`
- :py:func:`FilFindFile`
- :py:func:`FilFindNextFile`
- :py:func:`FilFormatBarcodeFile`
- :py:func:`FilGetBinPath`
- :py:func:`FilGetCommState`
- :py:func:`FilGetCommTimeouts`
- :py:func:`FilGetConfigPath`
- :py:func:`FilGetLabwarePath`
- :py:func:`FilGetLibraryPath`
- :py:func:`FilGetLogFilesPath`
- :py:func:`FilGetMethodsPath`
- :py:func:`FilGetSystemPath`
- :py:func:`FilIsNull`
- :py:func:`FilReadString`
- :py:func:`FilRemoveFields`
- :py:func:`FilSearchPath`
- :py:func:`FilSetCommState`
- :py:func:`FilSetCommTimeouts`
- :py:func:`FilUpdateRecord`
- :py:func:`FilWriteString`

.. py:function:: FilEof(variable filObj)

  This function checks whether the current position in the specified file is the final line

  :params filObj: The opened file to be checked
  :type filObj: Variable (file)
  :return: Boolean as to whether the position is the end of the file or not
  :rtype: Boolean
