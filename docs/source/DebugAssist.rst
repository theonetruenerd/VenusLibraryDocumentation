DebugAssist
============================

https://github.com/theonetruenerd/VenusPackages/blob/main/DebugAssist.pkg 

The debug assist library adds one functions aimed at helping the user identify, understand, and fix runtime errors. The function it adds is:

- :py:func:`FullErrorAnalysis`

.. py:function:: FullErrorAnalysis(variable i_PathForErrorDataAnalysis)

  This function is designed to be called in the "OnAbort" submethod. It will look at the error that caused the abort to be triggered, convert the trace file error code into the more standard form, identify what that error corresponds with and hopefully suggest some initial things to check. In order for the dialogue to pop up, this function requires ASWStandardDialogues to be initialised.

  :params i_PathForErrorDataAnalysis: A file path for where the error data will be exported. Currently not very important as the main bonus of the library is the dialogue that pops up, although the intention is to add more detail to this exported file.
  :type i_PathForErrorDataAnalysis: Variable
  :return: None
  :rtype: N/A
