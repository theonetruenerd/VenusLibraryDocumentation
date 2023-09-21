Zero uL Scanner
=========================

https://github.com/theonetruenerd/VenusPackages/blob/main/ZerouLScanner.pkg

The zero uL scanner library adds a single function which is designed to be added at the end of a method. It scans the trace file for any steps in which 0uL was pipetted and returns the number of times that happened. This is to check for steps where (for example) it is pipetting a volume based on a variable, and there is a spelling mistake in the variable, or the variable isn't defined correctly. It will work in both simulation mode and normal mode.

- :py:func:`CheckFor0s`

.. py:function:: CheckFor0s()

  This function checks for any steps in which 0uL has been pipetted and returns the number of times that has happened.

  :return: Number of times 0uL has been pipetted
  :rtype: Variable
