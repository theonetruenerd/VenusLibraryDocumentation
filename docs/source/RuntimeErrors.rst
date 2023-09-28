Runtime Errors
========================

Venus errors
--------------------

- :py:func:`0xa0220001` : No memory
- :py:func:`0xa1230002` : Inserting identifier failed
- :py:func:`0xa1230003` : Identifier not found
- :py:func:`0xa2230004` : L-value not a number
- :py:func:`0xa2230005` : R-value not a number
- :py:func:`0xa1230006` : Not an identifier
- :py:func:`0xa1220007` : Unrecognized token
- :py:func:`0xa2230008` : R-value not bound
- :py:func:`0xa2230009` : Bad number
- :py:func:`0xa123000a` : Bad tree
- :py:func:`0xa123000b` : Invalid entry
- :py:func:`0xa122000c` : Function identifier is protected
- :py:func:`0xa223000d` : Underspecified
- :py:func:`0xa2230037` : Overspecified
- :py:func:`0xa123000e` : Setting value failed
- :py:func:`0xa123000f` : Function identifier not found
- :py:func:`0xa1230010` : Bindings not found
- :py:func:`0xa1230011` : Temporary variable not found
- :py:func:`0xa1230012` : Unknown function type
- :py:func:`0xa2230013` : Unable to find file
- :py:func:`0xa1230014` : Type mismatch
- :py:func:`0xa2230015` : Bad L-value
- :py:func:`0xa2230016` : Bad R-value
- :py:func:`0xa2220017` : Unrecognised type
- :py:func:`0xa1230018` : Bad memory type
- :py:func:`0xa1230019` : Array reference out of bound
- :py:func:`0xa123001a` : Bad array identifier type
- :py:func:`0xa123001b` : Tag insert failed
- :py:func:`0xa123001c` : Dynamic memory identifier not bound
- :py:func:`0xa123001d` : Tag identifier not bound
- :py:func:`0xa123001e` : Structure reference out of bound
- :py:func:`0xa123001f` : Bad tag identifier type
- :py:func:`0xa1230020` : L-value is not a structure identifier
- :py:func:`0xa1230021` : L-value is not an array identifier
- :py:func:`0xa1230022` : Failed to lookup tag identifier in tag table
- :py:func:`0xa1230023` : Signal break
- :py:func:`0xa1230024` : Copy out of bound
- :py:func:`0xa1230025` : Signal return
- :py:func:`0xa2230026` : Array size is not an integer
- :py:func:`0xa1230027` : Failed to copy tag table
- :py:func:`0xa1230029` : Function has not been defined
- :py:func:`0xa123002a` : Unable to enter nesting level
- :py:func:`0xa123002b` : Unable to exit nesting level
- :py:func:`0xa122002c` : No context
- :py:func:`0xa123002d` : Failed to read file
- :py:func:`0xa123002e` : Failed to create timer
- :py:func:`0xa123002f` : Failed to set timer
- :py:func:`0xa1230030` : Failed to wait timer
- :py:func:`0xa1230031` : Failed to create event
- :py:func:`0xa1230032` : Failed to set event
- :py:func:`0xa1230033` : Failed to wait event
- :py:func:`0xa1230034` : Bad argument
- :py:func:`0xa2230035` : Syntax error
- :py:func:`0xa2230036` : Integer divide by zero
- :py:func:`0xa2230038` : Returning address of local variable or temporary
- :py:func:`0xa223003a` : Unable to find file
- :py:func:`0xa223003b` : File not updatable
- :py:func:`0xa223003c` : Recursive call
- :py:func:`0xa223003d` : Failed to wait for thread(s)
- :py:func:`0xa223003e` : Time-out interval elapsed
- :py:func:`0xa2220044` : Automation type not supported
- :py:func:`0xa1230046` : Bad argument parameter
- :py:func:`0xa123004d` : Sequence property not found
- :py:func:`0xa123004e` : int64 not supported

HSLUtilLib2 Errors
-----------------------------

- :py:func:`0x0001` : Unexpected error
- :py:func:`0x0002` : Create object failed
- :py:func:`0x0003` : Value check failed: Invalid type
- :py:func:`0x0004` : Value check failed: Invalid range
- :py:func:`0x0005` : Labware error
- :py:func:`0x0006` : Array index not a number
- :py:func:`0x0007` : Array index not an integer
- :py:func:`0x0008` : Array index must not be negative
- :py:func:`0x0009` : Array index must not be greater than array size

Error explanations and advice
-----------------------------

.. py:function:: 0xa0220001 (No memory)

  This error means that the system cannot allocate or access enough memory or disk space for whatever operation causes the error to arise. To fix this, try:

  - Opening task manager and closing down other programs that are using a lot of RAM
  - Modify the operation to optimise for less memory usage
  - Increase the amount of RAM that Venus has been allocated
  - In task manager, go to details, right click the hamilton software and assign priority high

.. py:function:: 0xa1230002 (Inserting identifier failed)

  This error means that the parser or executer could not insert the specified identifier into the symbol table. Some examples of how this error can arise are: if the table is corrupted, if the identifier being read causes issues for the parser, or similar. To fix this, try:

  - Replace the identifier with something else temporarily, to determine whether it is the identifier causing the issue or something else
  - Check to make sure the identifier has all the data associated with it that the symbol table needs. Typically this includes name, type and attributes
  - Check to make sure the identifier doesn't include any symbols that might interfere with the parser. These can include anything outside of standard ASCII characters from range 0x00 - 0x7F.

.. py:function:: 0xa1230003 (Identifier not found)

  This error means that the parser or executer could not find the specified identifier in the symbol table. This usually means something like a sequence or variable has either not been added or has been added but misspelt. To fix this, try:

  - Check what the error says. It should be an error which tells you the name of what it fails to lookup, which is useful for debugging purposes.
  - Check whether the name given in the error is spelt correctly; if not then that needs correcting
  - Check whether the name given in the error has been initialised/defined. It may be there, it may be there but misspelt, it may not be there at all. If it isn't there, add it and try again. If it is there but misspelt, rename it to the correct item. 
  - If the name is there and spelt correctly, make sure that the correct symbol table is being called during the method

.. py:function:: 0xa2230004 (L-value not a number)

  This error means that the executor has detected that the left hand side of the expression at the specified line is not a number. The error thrown will usually include the line number from which the error arose; this will be the line number in the HSL code. Look up the error to find whereabouts in the Venus code it corresponds to, but don't fix it in the HSL method editor; otherwise you can only use HSL method editor from that point onwards as Venus only compiles one way (med --> hsl). This usually occurs when two values are being added and one of them is not a number but instead a string. To fix this, try:

  - Checking whether you are trying to add two numbers or concatenate two strings, both have similar syntax. 
  - If trying to add two numbers, check which one is on the left (e.g. s in the equation v = s + 1)
  - Make sure the selected number is a number and not a string or similar. You can either convert it to a number manually, or you can input a step into the method which automatically converts strings to their float/int equivalents. This can be performed by the StrFVal function from HSLStrLib.
  - If trying to concatenate two strings, then the leftmost value is still being stored as a number rather than a string
  - Use the StrFStr function from HSLStrLib to convert a floating point number into the correpsponding character string before concatenating.

.. py:function:: 0xa2230005 (R-value not a number)

  This error means that the executor has detected that the right hand side of the expression at the specified line is not a number. The error thrown will usually include the line number from which the error arose; this will be the line number in the HSL code. Look up the error to find whereabouts in the Venus code it corresponds to, but don't fix it in the HSL method editor; otherwise you can only use HSL method editor from that point onwards as Venus only compiles one way (med --> hsl). This usually occurs when two values are being added and one of them is not a number but instead a string. To fix this, try:

  - Checking whether you are trying to add two numbers or concatenate two strings, both have similar syntax. 
  - If trying to add two numbers, check which one is on the right (e.g. 1 in the equation v = s + 1)
  - Make sure the selected number is a number and not a string or similar. You can either convert it to a number manually, or you can input a step into the method which automatically converts strings to their float/int equivalents. This can be performed by the StrFVal function from HSLStrLib.
  - If trying to concatenate two strings, then the leftmost value is still being stored as a number rather than a string
  - Use the StrFStr function from HSLStrLib to convert a floating point number into the correpsponding character string before concatenating.

.. py:function:: 0xa1230006 (Not an identifier)

  This error means that the symbol table entry of the identifier at the specified line is not an identifier. To fix this, try: 

  - Changing the name of the identifier being used. You can also look through the method to confirm that the identifier is being used and that you are not misspelling anything

.. py:function:: 0xa1220007 (Unrecognized token)

  This error means that the executor detected an unrecognized token. This usually means that what it is trying to parse contains characters that are not allowed. A typical example of this is when a JSON Parser tries to parse HTML, and encounters the \"<\" character. To fix this, try:

  - Identify what code line the error comes from via the HSL code, and then look at that code in Venus. 
  - Look through the code that the executor is trying to manage and try identify any characters that might not be standard. This includes anything outside of the normal ASCII range of 0x00 - 0x7F. Remove or replace those characters
  - Check that any special characters that are part of strings have backslashes in front of them.

.. py:function:: 0xa1230008 (R-value not bound)

  This error occurs when the R-value in a line is not bound to a valid value. An example would be v = a + b, where b has not been assigned to any value, or has been assigned to a sequence rather than a variable and thus cannot take part in this operation. To fix this, try:

  - Identify what code line the error comes from via the HSL code, and identify what variable is on the right hand side of that line
  - Check to see what the type of that variable is. If not obvious from reading the code, you can use the StrGetType function from HSLStrLib, or CheckValueType from HSLUtilLib2, or go through and try specific ones such as IsBoolean from HSLUtilLib.
  - If the variable is the correct type, check to see that it has been assigned to the right value. An easy way to do this is just to add in a step which traces the variable value immediately before the error.
  - If the variable is the right type and the correct value, check to see what value the line is expecting --> could it be mistakenly expecting a string concatenation instead of a summation.

.. py:function:: 0xa2230009 (Bad number)

  This error means that the executor detected an error in a number at the specific line. This often occurs if a number is of the wrong format (e.g. int rather than flt). To fix this, try:

  - Check what number is causing the error to occur by looking at the line given in the error code. 
  - Work out what type the line is expecting the number to be --> for example, a loop counter will be expecting an integer rather than a float
  - Check what type the number causing the error is. This can be done using the CheckValueType from HSLUtilLib2, or the IsFloat/IsInteger functions from HSLUtilLib. 
  - If unsure, just toggle the number type and see if swapping it from int to flt or vice versa helps. 

.. py:function:: 0xa123000a (Bad tree)

  This error means that the executor detected an error in the structure of the syntax tree.

.. py:function:: 0xa123000b (Invalid entry)

  This error means that the executor has detected an invalid symbol table entry. This error usually occurs if there is a non-ASCII character present in the symbol table, and the executor was not the one who inserted the value into the symbol table in the first place. To fix this, try:

  - Work out which character(s) in the symbol table are invalid
  - Try to replace those characters with their ASCII equivalents, as well as work out where/why they were added in teh first place

.. py:function:: 0xa122000c (Function identifier is protected)

  This error means that the parser or executor detected a protected function identifier in the symbol table at the specified line. This happens if a device is declared in the local scope, for example. To fix this, try:

  - Checking to make sure nothing is in the local scope which shouldn't be

.. py:function:: 0xa223000d (Underspecified)

  This error means that the executor detected underspecified formal parameters of a function at the specific line. To fix this, try:

  - Check what line the error gives as the function going wrong, look at that line in HSL and work out the correct location in Venus code
  - Look at whatever functions are present on that line and check how many input parameters the functions are meant to have vs how many they actually have
  - Make sure all input parameters exist and are not just empty variables/arrays/sequences.

.. py:function:: 0xa2230037 (Overspecified)

  This error means that the executor detected overspecified formal parameters ofa  function at the specific line. To fix this, try:

  - Check what line the error gives as the function going wrong, look at that line in HSL and work out the correct location in Venus code
  - Look at whatever functions are present on that line and check how many input parameters the functions are meant to have vs how many they actually have
  - Make sure all input parameters exist and are not just empty variables/arrays/sequences.

.. py:function:: 0xa123000e (Setting value failed)

  This error means that the executor failed to set the value of a symbol table entry at the specified line. To fix this, try:

  - Check what line the error gives as the function going wrong, look at that line in HSL and work out the correct location in Venus code
  - See what value is trying to be set within the symbol table; make sure it has no special characters, the correct type and attributes

.. py:function:: 0xa123000f (Function identifier not found)

  This error occurs when the executor failed to lookup a function identifier in the symbol table at the specified line. This usually means the function has not been defined properly or has failed to import into the symbol table properly. It can also be the result of a misspelt name at any steps involving it. To fix this, try:

  - See what the name of the function is that isn't being found
  - Check to see if the function name is spelt correctly
  - Check to see earlier in the method that the function has been defined and imported successfully into the symbol table
  - Check to see if this happens everytime this function is called or just this one step. If it happens every time then it is likely a definition/import issue, if only once then it is likely a naming/exporting issue.
