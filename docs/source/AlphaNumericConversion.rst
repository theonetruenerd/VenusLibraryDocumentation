Alpha Numeric Conversion
=============================================================

https://github.com/theonetruenerd/VenusPackages/blob/main/AlphaNumericConversion.pkg

This library adds four functions related to converting plate positions to their integer equivalents and vice versa. The functions it adds are:

- :py:func:`Alpha_Num_Add_0_to_Position`
- :py:func:`Alpha_Num_Remove_0_from_Position`
- :py:func:`Convert_Alpha_Numeric_to_Numbers`
- :py:func:`Convert_Numbers_to_Alpha_Numeric`

.. py:function:: Alpha_Num_Add_0_to_Position(variable io_Str_Position_ID)

  This function takes a single position and adds the 0 between the letter and number if it needs one
