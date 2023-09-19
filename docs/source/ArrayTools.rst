ArrayTools
====================================

The ArrayTools library provides the following functions:
- :py:func:`ArraySeqVLookup`
- :py:func:`ArrayVLookup`
- :py:func:`ConvertArrayOfNumericIntegersIntoString`
- :py:func:`ConvertArrayOfNumericStringsIntoInteger`
- :py:func:`Lookup`
- :py:func:`Sort3ArraysByNumericAscendingOrder`
- :py:func:`Update_Value_in_Array`
- :py:func:`get_distinct_from_array`
- :py:func:`mergeArrays`
- :py:func:`removeValueFromArray_basedOnIndex`

.. py:function:: ArraySeqVLookup(array i_arraySequencesA, array i_arrayValuesB, variable i_varCondition, array o_arraySequencesC)
  Given 2 arrays  A (Sequences) and B (Values) with same size
  Retrieve all the sequences in A where B = input value
  A(seq1, seq2, seq3,seq4,seq5, seq6, ...)
  B(1, 2, 3, 1, 2, 3, ...)

  Get from A all elements where B = 1
  C(seq1, seq4, ...)

  :param i_arraySequencesA: The input array of sequences to filter
  :param i_arrayValuesB: The input array of variables to act as a filter
  :param i_varCondition: The input value of the variable which is to be selected
  :param o_arraySequencesC: The output array of the sequences whose index matches the indices in which the the value of the variable is equal to the filter
  :type i_arraySequencesA: Array of sequences
  :type i_arrayValuesB: Array of variables
  :type i_varCondition: Variable
  :type o_arraySequencesC: Array of sequences
  :return: None
  :rtype: N/A

.. py:function::ArrayVLookup(array i_arrayValuesA, array i_arrayValuesB, variable i_varCondition, array o_arrayValuesC)
  Given 2 arrays of values A and B with same size
  Retrieve all the elements in B where A = input value

  A(100, 20, 15, 45, 42, 1, ...)
  B(1, 2, 3, 1, 2, 3, ...)

  Get from A all elements where B = 1
  C(100, 15, ...)

  :param i_arrayValuesA: The input array of variables to filter
  :param i_arrayValuesB: The input array of variables to act as a filter
  :param i_varCondition: The input value of the variable which is to be selected
  :param o_arrayValuesC: The output array of the variables whose index matches the indices in which the value of the variable is equal to the filter
  :type i_arrayValuesA: Array of variables
  :type i_arrayValuesB: Array of variables
  :type i_varCondition: Variable
  :type o_arrayValuesC: Array of variables
  :return: None
  :rtype: N/A
