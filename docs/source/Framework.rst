Framework (from HSLExtensions)
=========================

https://github.com/theonetruenerd/VenusPackages/blob/main/Framework.pkg

The framework library from HSLExtensions provides two visible functions, but is also required for a few of the other HSLExtension libraries. It uses the functionality of the ASW Standard TraceLevel library. The functions it adds are: 

- :ven:func:`GetVersion`
- :ven:func:`SetTraceLevel`

.. ven:function:: GetVersion()

  This function gets the framework version

  :return: The framework version
  :rtype: String

.. ven:function:: SetTraceLevel(variable i_intTraceLevel)

  This function sets the trace level of the framework.

  :params i_intTraceLevel: The trace level, for the ASWStandard::TraceLevel library. 0 = TRACE_LEVEL_NONE, 1 = TRACE_LEVEL_RELEASE, 2 = TRACE_LEVEL_DEBUG.
  :type i_intTraceLevel: Variable
  :return: None
  :rtype: N/A
