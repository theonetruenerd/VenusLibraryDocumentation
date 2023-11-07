Alpha Numeric Conversion
=============================================================

https://github.com/theonetruenerd/VenusPackages/blob/main/AlphaNumericConversion.pkg

This library adds four functions related to converting plate positions to their integer equivalents and vice versa. The functions it adds are:

- :py:func:`Alpha_Num_Add_0_to_Position`
- :py:func:`Alpha_Num_Remove_0_from_Position`
- :py:func:`Convert_Alpha_Numeric_to_Numbers`
- :py:func:`Convert_Numbers_to_Alpha_Numeric`

.. py:function:: Alpha_Num_Add_0_to_Position(variable io_Str_Position_ID)

  This function takes a single position and adds the 0 between the letter and number if it needs one. Example would be A1 -> A01, B1 -> B01. Position variable must be a string.

  :params io_Str_Position_ID: The alphanumeric position that the 0 needs to be added to.
  :type io_Str_Position_ID: Variable
  :return: None
  :rtype: N/A

.. py:function:: Alpha_Num_Remove_0_from_Position(variable io_Str_Position_ID)

  This function takes a single position and removes the 0 if there is one. Example would be A01 -> A1, B01 -> B1. Position variable must be a string.

  :params io_Str_Position_ID: The alphanumeric position that the 0 needs to be removed from.
  :type io_Str_Position_ID: Variable
  :return: None
  :rtype: N/A

.. py:function:: Convert_Alpha_Numeric_to_Numbers(variable i_Sort_by_Column, variable i_Alpha_Numeric_Value, variable i_Total_Rows, variable i_Total_Columns, variable o_Numeric_Value)

  This function takes an alpha numeric value and returns the integer that corresponds to that position number. If a 1 is entered for "i_Sort_by_Column", the submethod will sort by columns, i.e. A1 -> 1, B1 -> 2, etc. If a 0 is entered, it will sort by rows, i.e. A1 -> 1, A2 -> 2.

  :params i_Sort_by_Column: Whether the positions will be sorted by row (0) or by column (1)
  :params i_Alpha_Numeric_Value: The alpha numeric value to be converted
  :params i_Total_Rows: The total number of rows in the target labware, between 1 and 26.
  :params i_Total_Columns: The total number of columns in the target labware, betweem 1 and 99.
  :params o_Numeric_Value: The output converted position
  :type i_Sort_by_Column: Boolean
  :type i_Alpha_Numeric_Value: Variable  
  :type i_Total_Rows: Variable
  :type i_Total_Columns: Variable
  :type o_Numeric_Value: Variable
  :return: None
  :rtype: N/A

.. py:function:: Convert_Numbers_to_Alpha_Numeric(variable i_Sort_by_Column, variable i_Numeric_Value, variable i_Total_Rows, variable i_Total_Columns, variable o_Alpha_Numeric_Value)

  This function takes an integer value and returns the corresponding alpha numeric position. If a 1 is entered for "i_Sort_by_Column", the submethod will sort by columns, i.e. 1 -> A1, 2 -> B1, etc. If a 0 is entered, it will sort by rows, i.e. 1 -> A1, 2 -> A2.

  :params i_Sort_by_Column: Whether the positions will be sorted by row (0) or by column (1)
  :params i_Numeric_Value: The numeric value to be converted
  :params i_Total_Rows: The total number of rows in the target labware, between 1 and 26.
  :params i_Total_Columns: The total number of columns in the target labware, between 1 and 99.
  :params o_Alpha_Numeric_Value: The output converted position
  :type i_Sort_by_Column: Boolean
  :type i_Numeric_Value: Variable
  :type i_Total_Rows: Variable
  :type i_Total_Columns: Variable
  :type o_Alpha_Numeric_Value: Variable
  :return: None
  :rtype: N/A
