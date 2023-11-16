Error Report Library
===================

https://github.com/theonetruenerd/VenusPackages/blob/main/ErrorReportLibrary.pkg

The error report library generates concise reports on both general errors and pipetting errors that occur during a run, extracting the information from the trace file. It adds the following functions:

- :ven:func:`CopyActiveTraceFile`
- :ven:func:`GenerateGeneralErrorsReport`
- :ven:func:`GeneratePipettingErrorsReport`

.. ven:function:: CopyActiveTraceFile(variable o_strTraceCopyFilePath)

  Finds the trace file that is currently active (i.e. associated with the current run) and makes a copy of it, which it saves in the location specified.

  :params o_strTraceCopyFilePath: The location that the copy of the trace file will be created in
  :type o_strTraceCopyFilePath: Variable
  :return: None 
  :rtype: N/A

.. ven:function:: GenerateGeneralErrorsReport(variable i_strTraceFilePath, variable o_strPDF_FilePath)

  Reads the active trace file, locates errors found within it and generates an error report on errors found in non-pipetting steps

  :params i_strTraceFilePath: The path to the current trace file 
  :params o_strPDF_FilePath: The file path for the exported PDF of the error report
  :type i_strTraceFilePath: Variable
  :type o_strPDF_FilePath: Variable
  :return: None
  :rtype: N/A

.. ven:function:: GeneratePipettingErrorsReport(variable i_strTraceFilePath, variable i_strTemplateFilePath, variable i_intWriteRowStart, o_strPDF_FilePath)

  Reads the active trace file, locates errors in the pipetting steps within it and generates an error report for the pipetting steps only

  :params i_strTraceFilePath: The path to the current trace file
  :params i_strTemplateFilePath: The path to the excel file used as a template for generating the report; should be installed when the library is unpacked
  :params i_intWriteRowStart: Which row of the excel file to begin the report on; usually two, can be more than two
  :params o_strPDF_FilePath: The file path for the exported PDF of the error report
  :type i_strTraceFilePath: Variable
  :type i_strTemplateFilePath: Variable
  :type i_intWriteRowStart: Variable
  :type o_strPDF_FilePath: Variable
  :return: None
  :rtype: N/A
