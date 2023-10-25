TraceLevel
=================================

The TraceLevel library adds a variety of functions related to the trace file. The functions it adds are:

- :py:func:`GetTraceLevel`
- :py:func:`SetTraceLevel`
- :py:func:`SetStringIndicator`
- :py:func:`Trace_02`
- :py:func:`Trace_04`
- :py:func:`Trace_06`
- :py:func:`Trace_08`
- :py:func:`Trace_10`
- :py:func:`TraceArray`
- :py:func:`TraceArrayHorizontally`
- :py:func:`TraceArraysFaceToFace`
- :py:func:`TraceSequence`
- :py:func:`TraceSequenceParameter`
- :py:func:`TraceSequencePositions`
- :py:func:`TraceAction`
- :py:func:`SetActionIndicator`

.. py:function:: GetTraceLevel()

  This function returns the current trace level.

  :return: This function returns one of the following predefined constants; TRACE_LEVEL_NONE (0), which corresponds to no traces at all. TRACE_LEVEL_RELEASE (1), which corresponds to only items with release trace level being traced. TRACE_LEVEL_DEBUG (2), which corresponds to everything being traced.
  :rtype: Variable

.. py:function:: SetTraceLevel(variable i_intTraceLevel)

  This function is used to set the trace level for the method or library.

  :params i_intTraceLevel: The trace level for the library. Set to one of the following constants; TRACE_LEVEL_NONE (0), which corresponds to no traces at all. TRACE_LEVEL_RELEASE (1), which corresponds to only items with release trace level being traced. TRACE_LEVEL_DEBUG (2), which corresponds to everything being traced.
  :type i_intTraceLevel: Variable (integer)
  :return: None
  :rtype: N/A

.. py:function:: SetStringIndicator(variable i_strStringIndicatorCharacter)

  This function is used to set one or more characters to indicate strings (by flanking them) in all traces. It can be useful to identify leading or trailing spaces in strings. You can do this by setting i_strStringIndicatorCharacter to \' or \*.

  :params i_strStringIndicatorCharacter: Characters that are being added at the beginning and the end of each string trace.
  :type i_strStringIndicatorCharacter: Variable
  :return: None
  :rtype: N/A

.. py:function:: Trace_02(variable i_intTraceLevel, variable i_varToTrace_01, variable i_varToTrace_02)

  This function is used to trace the value of 2 variables in one line. Will not automatically insert a space between the two variables.

  :params i_intTraceLevel: The trace level for the entry. Can be set to either TRACE_LEVEL_RELEASE (1) or TRACE_LEVEL_DEBUG (2). If set to 1, the function will show up in the trace when the trace level is set to either TRACE_LEVEL_RELEASE or TRACE_LEVEL_DEBUG, if set to 2, the function will only show up when the trace level is TRACE_LEVEL_DEBUG.
  :params i_varToTrace_01: The first variable to trace.
  :params i_varToTrace_02: The second variable to trace.
  :type i_intTraceLevel: Variable
  :type i_varToTrace_01: Variable
  :type i_varToTrace_02: Variable
  :return: None
  :rtype: N/A

.. py:function:: Trace_04(variable i_intTraceLevel, variable i_varToTrace_01, variable i_varToTrace_02, variable i_varToTrace_03, variable i_varToTrace_04)

  This function is used to trace the value of 4 variables in one line. Will not automatically insert a space between the variables.

  :params i_intTraceLevel: The trace level for the entry. Can be set to either TRACE_LEVEL_RELEASE (1) or TRACE_LEVEL_DEBUG (2). If set to 1, the function will show up in the trace when the trace level is set to either TRACE_LEVEL_RELEASE or TRACE_LEVEL_DEBUG, if set to 2, the function will only show up when the trace level is TRACE_LEVEL_DEBUG.
  :params i_varToTrace_01: The first variable to trace.
  :params i_varToTrace_02: The second variable to trace.
  :params i_varToTrace_03: The third variable to trace.
  :params i_varToTrace_04: The fourth variable to trace.
  :type i_intTraceLevel: Variable
  :type i_varToTrace_01: Variable
  :type i_varToTrace_02: Variable
  :type i_varToTrace_03: Variable
  :type i_varToTrace_04: Variable
  :return: None
  :rtype: N/A

.. py:function:: Trace_06(variable i_intTraceLevel, variable i_varToTrace_01, variable i_varToTrace_02, variable i_varToTrace_03, variable i_varToTrace_04, variable i_varToTrace_05, variable i_varToTrace_06)

  This function is used to trace the value of 6 variables in one line. Will not automatically insert a space between the variables.

  :params i_intTraceLevel: The trace level for the entry. Can be set to either TRACE_LEVEL_RELEASE (1) or TRACE_LEVEL_DEBUG (2). If set to 1, the function will show up in the trace when the trace level is set to either TRACE_LEVEL_RELEASE or TRACE_LEVEL_DEBUG, if set to 2, the function will only show up when the trace level is TRACE_LEVEL_DEBUG.
  :params i_varToTrace_01: The first variable to trace.
  :params i_varToTrace_02: The second variable to trace.
  :params i_varToTrace_03: The third variable to trace.
  :params i_varToTrace_04: The fourth variable to trace.
  :params i_varToTrace_05: The fifth variable to trace.
  :params i_varToTrace_06: The sixth variable to trace.
  :type i_intTraceLevel: Variable
  :type i_varToTrace_01: Variable
  :type i_varToTrace_02: Variable
  :type i_varToTrace_03: Variable
  :type i_varToTrace_04: Variable
  :type i_varToTrace_05: Variable
  :type i_varToTrace_06: Variable
  :return: None
  :rtype: N/A

.. py:function:: Trace_08(variable i_intTraceLevel, variable i_varToTrace_01, variable i_varToTrace_02, variable i_varToTrace_03, variable i_varToTrace_04, variable i_varToTrace_05, variable i_varToTrace_06, variable i_varToTrace_07, variable i_varToTrace_08)

  This function is used to trace the value of 8 variables in one line. Will not automatically insert a space between the variables.

  :params i_intTraceLevel: The trace level for the entry. Can be set to either TRACE_LEVEL_RELEASE (1) or TRACE_LEVEL_DEBUG (2). If set to 1, the function will show up in the trace when the trace level is set to either TRACE_LEVEL_RELEASE or TRACE_LEVEL_DEBUG, if set to 2, the function will only show up when the trace level is TRACE_LEVEL_DEBUG.
  :params i_varToTrace_01: The first variable to trace.
  :params i_varToTrace_02: The second variable to trace.
  :params i_varToTrace_03: The third variable to trace.
  :params i_varToTrace_04: The fourth variable to trace.
  :params i_varToTrace_05: The fifth variable to trace.
  :params i_varToTrace_06: The sixth variable to trace.
  :params i_varToTrace_07: The seventh variable to trace.
  :params i_varToTrace_08: The eighth variable to trace.
  :type i_intTraceLevel: Variable
  :type i_varToTrace_01: Variable
  :type i_varToTrace_02: Variable
  :type i_varToTrace_03: Variable
  :type i_varToTrace_04: Variable
  :type i_varToTrace_05: Variable
  :type i_varToTrace_06: Variable
  :type i_varToTrace_07: Variable
  :type i_varToTrace_08: Variable
  :return: None
  :rtype: N/A

.. py:function:: Trace_10(variable i_intTraceLevel, variable i_varToTrace_01, variable i_varToTrace_02, variable i_varToTrace_03, variable i_varToTrace_04, variable i_varToTrace_05, variable i_varToTrace_06, variable i_varToTrace_07, variable i_varToTrace_08, variable i_varToTrace_09, variable i_varToTrace_10)

  This function is used to trace the value of 10 variables in one line. Will not automatically insert a space between the variables.

  :params i_intTraceLevel: The trace level for the entry. Can be set to either TRACE_LEVEL_RELEASE (1) or TRACE_LEVEL_DEBUG (2). If set to 1, the function will show up in the trace when the trace level is set to either TRACE_LEVEL_RELEASE or TRACE_LEVEL_DEBUG, if set to 2, the function will only show up when the trace level is TRACE_LEVEL_DEBUG.
  :params i_varToTrace_01: The first variable to trace.
  :params i_varToTrace_02: The second variable to trace.
  :params i_varToTrace_03: The third variable to trace.
  :params i_varToTrace_04: The fourth variable to trace.
  :params i_varToTrace_05: The fifth variable to trace.
  :params i_varToTrace_06: The sixth variable to trace.
  :params i_varToTrace_07: The seventh variable to trace.
  :params i_varToTrace_08: The eighth variable to trace.
  :params i_varToTrace_09: The ninth variable to trace.
  :params i_varToTrace_10: The tenth variable to trace.
  :type i_intTraceLevel: Variable
  :type i_varToTrace_01: Variable
  :type i_varToTrace_02: Variable
  :type i_varToTrace_03: Variable
  :type i_varToTrace_04: Variable
  :type i_varToTrace_05: Variable
  :type i_varToTrace_06: Variable
  :type i_varToTrace_07: Variable
  :type i_varToTrace_08: Variable  
  :type i_varToTrace_09: Variable
  :type i_varToTrace_10: Variable
  :return: None
  :rtype: N/A

.. py:function:: TraceArray(variable i_intTraceLevel, variable i_strDescription, array i_arrvarToTrace)

  This function is used to trace an array of variables. It will trace each value of the array in its own line, along with the array description and the index of the value.

  :params i_intTraceLevel: The trace level for the entry. Can be set to either TRACE_LEVEL_RELEASE (1) or TRACE_LEVEL_DEBUG (2). If set to 1, the function will show up in the trace when the trace level is set to either TRACE_LEVEL_RELEASE or TRACE_LEVEL_DEBUG, if set to 2, the function will only show up when the trace level is TRACE_LEVEL_DEBUG.
  :params i_strDescription: A description of the array, which will be at the start of each line of the array trace.
  :params i_arrvarToTrace: The array to be traced.
  :type i_intTraceLevel: Variable
  :type i_strDescription: Variable
  :type i_arrvarToTrace: Array (of variables)
  :return: None
  :rtype: N/A

.. py:function:: TraceArrayHorizontally(variable i_intTraceLevel, variable i_strDescription, array i_arrvarToTrace)

  This function is used to trace an array of variables. It will trace the array description, followed by each array index and value pair, all on one line.

  :params i_intTraceLevel: The trace level for the entry. Can be set to either TRACE_LEVEL_RELEASE (1) or TRACE_LEVEL_DEBUG (2). If set to 1, the function will show up in the trace when the trace level is set to either TRACE_LEVEL_RELEASE or TRACE_LEVEL_DEBUG, if set to 2, the function will only show up when the trace level is TRACE_LEVEL_DEBUG.
  :params i_strDescription: A description of the array, which will be at the start of the array trace.
  :params i_arrvarToTrace: The array to be traced.
  :type i_intTraceLevel: Variable
  :type i_strDescription: Variable
  :type i_arrvarToTrace: Array (of variables)
  :return: None
  :rtype: N/A

.. py:function:: TraceArraysFaceToFace(variable i_intTraceLevel, variable i_strDescription_1, variable i_strDescription_2, array i_arrvarToTrace_1, array i_arrvarToTrace_2)

  This function is used to trace two arrays of variables at the same time, with values at the same index being shown on the same line as one another.

  :params i_intTraceLevel: The trace level for the entry. Can be set to either TRACE_LEVEL_RELEASE (1) or TRACE_LEVEL_DEBUG (2). If set to 1, the function will show up in the trace when the trace level is set to either TRACE_LEVEL_RELEASE or TRACE_LEVEL_DEBUG, if set to 2, the function will only show up when the trace level is TRACE_LEVEL_DEBUG.
  :params i_strDescription_1: A description of the first array, which will be at the start of the array trace.
  :params i_strDescription_2: A description of the second array, which will be at the start of the array trace.
  :params i_arrvarToTrace_1: The first array to be traced.
  :params i_arrvarToTrace_2: The second array to be traced.
  :type i_intTraceLevel: Variable
  :type i_strDescription_1: Variable
  :type i_strDescription_2: Variable
  :type i_arrvarToTrace_1: Array (of variables)
  :type i_arrvarToTrace_2: Array (of variables)
  :return: None
  :rtype: N/A

.. py:function:: TraceSequence(variable i_intTraceLevel, sequence i_seqToTrace)

  This function is used to trace a sequence. It will list the sequence name, current position, the count and total positions in the sequence, the max number of positions available, and the number of used positions. It will then list the labware ID and position ID for each value of the sequence.

  :params i_intTraceLevel: The trace level for the entry. Can be set to either TRACE_LEVEL_RELEASE (1) or TRACE_LEVEL_DEBUG (2). If set to 1, the function will show up in the trace when the trace level is set to either TRACE_LEVEL_RELEASE or TRACE_LEVEL_DEBUG, if set to 2, the function will only show up when the trace level is TRACE_LEVEL_DEBUG.
  :params i_seqToTrace: The sequence to be traced
  :type i_intTraceLevel: Variable
  :type i_seqToTrace: Sequence
  :return: None
  :rtype: N/A

.. py:function:: TraceSequenceParameter(variable i_intTraceLevel, sequence i_seqToTrace)

  This function is used to trace the parameters of a sequence. It will list the sequence name, current position, the count and total positions in the sequence, the max number of positions available, and the number of used positions.

  :params i_intTraceLevel: The trace level for the entry. Can be set to either TRACE_LEVEL_RELEASE (1) or TRACE_LEVEL_DEBUG (2). If set to 1, the function will show up in the trace when the trace level is set to either TRACE_LEVEL_RELEASE or TRACE_LEVEL_DEBUG, if set to 2, the function will only show up when the trace level is TRACE_LEVEL_DEBUG.
  :params i_seqToTrace: The sequence to be traced
  :type i_intTraceLevel: Variable
  :type i_seqToTrace: Sequence
  :return: None
  :rtype: N/A

.. py:function:: TraceSequencePositions(device ML_STAR, variable i_intTraceLevel, sequence i_seqToTrace, variable i_blnCurrentPositionOnly)

  This function is used to trace the deck positions of a sequence. It will trace the sequence name, then for each part of the sequence it will trace the position ID and the x, y, z, and r coordinates of the position.

  :params ML_STAR: The STAR device.
  :params i_intTraceLevel: The trace level for the entry. Can be set to either TRACE_LEVEL_RELEASE (1) or TRACE_LEVEL_DEBUG (2). If set to 1, the function will show up in the trace when the trace level is set to either TRACE_LEVEL_RELEASE or TRACE_LEVEL_DEBUG, if set to 2, the function will only show up when the trace level is TRACE_LEVEL_DEBUG.
  :params i_seqToTrace: The sequence to be traced
  :params i_blnCurrentPositionOnly: A boolean determining whether the function will trace positions for all sequence positions (0) or just the current sequence position (1).  
  :type ML_STAR: Device
  :type i_intTraceLevel: Variable
  :type i_seqToTrace: Sequence
  :type i_blnCurrentPositionOnly: Boolean
  :return: None
  :rtype: N/A

.. py:function:: TraceAction(variable i_intTraceLevel, variable i_intAction, variable i_strFunctionName, variable i_strMethodName, variable i_strComment)

  This function is used to trace different action states for a module. :py:func:`SetActionIndicator` can be used to help identify actions in log files more easily.

  :params i_intTraceLevel: The trace level for the entry. Can be set to either TRACE_LEVEL_RELEASE (1) or TRACE_LEVEL_DEBUG (2). If set to 1, the function will show up in the trace when the trace level is set to either TRACE_LEVEL_RELEASE or TRACE_LEVEL_DEBUG, if set to 2, the function will only show up when the trace level is TRACE_LEVEL_DEBUG.
  :params i_intAction: The action to be traced. Set to one of the following constants. START (1) corresponds to the entry being traced as starting. COMPLETE (2) corresponds to the entry being traced as finished successfully. ERROR (3) corresponds to the entry being traced as error occurred. PROGRESS (4) corresponds to the entry being traced as progressing. COMPLETE_WITH_ERROR (5) corresponds to the entry being traced as finished unsuccessfully.
  :params i_strFunctionName: The function name for the action trace. Can be set to the return value of the HSL function *GetFunctionName*, which will automatically be formatted correctly.
  :params i_strMethodName: The method name for the action trace. Can be set to the return value of the HSL function *GetMethodFileName*, which will automatically be formatted correctly.
  :params i_strComment: A comment to be traced with the action trace.
  :type i_intTraceLevel: Variable
  :type i_intAction: Variable
  :type i_strFunctionName: Variable
  :type i_strMethodName: Variable
  :type i_strComment: Variable
  :return: None
  :rtype: N/A

.. py:function:: SetActionIndicator(variable i_intAction, variable i_strIndicator)

  This function is used to set one or more characters to indicate actions. By setting *i_strIndicator* to different characters you can make it easy to identify different actions in the trace.

  :params i_intAction: The action to be traced. Set to one of the following constants. START (1) corresponds to the entry being traced as starting. COMPLETE (2) corresponds to the entry being traced as finished successfully. ERROR (3) corresponds to the entry being traced as error occurred. PROGRESS (4) corresponds to the entry being traced as progressing. COMPLETE_WITH_ERROR (5) corresponds to the entry being traced as finished unsuccessfully.
  :params i_strIndicator: Character(s) that are being repeated at a total length of up to 100 and traced before and after the action trace.
  :type: i_intAction: Variable
  :type i_strIndicator: Variable
  :return: None
  :rtype: N/A

