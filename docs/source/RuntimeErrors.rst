Runtime Errors
========================

.. _RuntimeErrors:

Venus errors
--------------------

- :ref:`0xa0220001 : No memory <0xa0220001>`
- :ref:`0xa1230002 : Inserting identifier failed <0xa1230002>`
- :ref:`0xa1230003 : Identifier not found <0xa1230003>`
- :ref:`0xa2230004 : L-value not a number <0xa2230004>`
- :ref:`0xa2230005 : R-value not a number <0xa2230005>`
- :ref:`0xa1230006 : Not an identifier <0xa1230006>`
- :ref:`0xa1220007 : Unrecognized token <0xa1220007>`
- :ref:`0xa1230008 : R-value not bound <0xa1230008>`
- :ref:`0xa2230009 : Bad number <0xa2230009>`
- :ref:`0xa123000a : Bad tree <0xa123000a>`
- :ref:`0xa123000b : Invalid entry <0xa123000b>`
- :ref:`0xa122000c : Function identifier is protected <0xa122000c>`
- :ref:`0xa223000d : Underspecified <0xa223000d>`
- :ref:`0xa2230037 : Overspecified <0xa2230037>`
- :ref:`0xa123000e : Setting value failed <0xa123000e>`
- :ref:`0xa123000f : Function identifier not found <0xa123000f>`
- :ref:`0xa1230010 : Bindings not found <0xa1230010>`
- :ref:`0xa1230011 : Temporary variable not found <0xa1230011>`
- :ref:`0xa1230012 : Unknown function type <0xa1230012>`
- :ref:`0xa2230013 : Unable to find file <0xa2230013>`
- :ref:`0xa1230014 : Type mismatch <0xa1230014>`
- :ref:`0xa2230015 : Bad L-value <0xa2230015>`
- :ref:`0xa2230016 : Bad R-value <0xa2230016>`
- :ref:`0xa2220017 : Unrecognised type <0xa2220017>`
- :ref:`0xa1230018 : Bad memory type <0xa1230018>`
- :ref:`0xa1230019 : Array reference out of bound <0xa1230019>`
- :ref:`0xa123001a : Bad array identifier type <0xa123001a>`
- :ref:`0xa123001b : Tag insert failed <0xa123001b>`
- :ref:`0xa123001c : Dynamic memory identifier not bound <0xa123001c>`
- :ref:`0xa123001d : Tag identifier not bound <0xa123001d>`
- :ref:`0xa123001e : Structure reference out of bound <0xa123001e>`
- :ref:`0xa123001f : Bad tag identifier type <0xa123001f>`
- :ref:`0xa1230020 : L-value is not a structure identifier <0xa1230020>`
- :ref:`0xa1230021 : L-value is not an array identifier <0xa1230021>`
- :ref:`0xa1230022 : Failed to lookup tag identifier in tag table <0xa1230022>`
- :ref:`0xa1230023 : Signal break <0xa1230023>`
- :ref:`0xa1230024 : Copy out of bound <0xa1230024>`
- :ref:`0xa1230025 : Signal return <0xa1230025>`
- :ref:`0xa2230026 : Array size is not an integer <0xa2230026>`
- :ref:`0xa1230027 : Failed to copy tag table <0xa1230027>`
- :ref:`0xa1230029 : Function has not been defined <0xa1230029>`
- :ref:`0xa123002a : Unable to enter nesting level <0xa123002a>`
- :ref:`0xa123002b : Unable to exit nesting level <0xa123002b>`
- :ref:`0xa122002c : No context <0xa122002c>`
- :ref:`0xa123002d : Failed to read file <0xa123002d>`
- :ref:`0xa123002e : Failed to create timer <0xa123002e>`
- :ref:`0xa123002f : Failed to set timer <0xa123002f>`
- :ref:`0xa1230030 : Failed to wait timer <0xa1230030>`
- :ref:`0xa1230031 : Failed to create event <0xa1230031>`
- :ref:`0xa1230032 : Failed to set event <0xa1230032>`
- :ref:`0xa1230033 : Failed to wait event <0xa1230033>`
- :ref:`0xa1230034 : Bad argument <0xa1230034>`
- :ref:`0xa2230035 : Syntax error <0xa2230035>`
- :ref:`0xa2230036 : Integer divide by zero <0xa2230036>`
- :ref:`0xa2230038 : Returning address of local variable or temporary <0xa2230038>`
- :ref:`0xa2230039 <0xa2230039>`
- :ref:`0xa223003a : Unable to find file <0xa223003a>`
- :ref:`0xa223003b : File not updatable <0xa223003b>`
- :ref:`0xa223003c : Recursive call <0xa223003c>`
- :ref:`0xa223003d : Failed to wait for threads <0xa223003d>`
- :ref:`0xa223003e : Time-out interval elapsed <0xa223003e>`
- :ref:`0xa2220044 : Automation type not supported <0xa2220044>`
- :ref:`0xa1230046 : Bad argument parameter <0xa1230046>`
- :ref:`0xa123004d : Sequence property not found <0xa123004d>`
- :ref:`0xa123004e : int64 not supported <0xa123004e>`

HSLUtilLib Errors
-----------------------------

- :ref:`0xa0000001 : The parameter is incorrect <0x00000001>`

HSLUtilLib2 Errors
-----------------------------

- :ref:`0xa1630001 : Unexpected error <0xa1630001>`
- :ref:`0xa1630002 : Create object failed/Invalid parameter <0xa1630002>`
- :ref:`0xa1630003 : Value check failed: Invalid type <0xa1630003>`
- :ref:`0xa1630004 : Value check failed: Invalid range <0xa1630004>`
- :ref:`0xa1630005 : Labware error <0xa1630005>`
- :ref:`0xa1630006 : Array index not a number <0xa1630006>`
- :ref:`0xa1630007 : Array index not an integer <0xa1630007>`
- :ref:`0xa1630008 : Array index must not be negative <0xa1630008>`
- :ref:`0xa1630009 : Array index must not be greater than array size <0xa1630009>`

Error explanations and advice
-----------------------------

.. _0xa0220001: 

  **0xa0220001: No memory**

  This error means that the system cannot allocate or access enough memory or disk space for whatever operation causes the error to arise. To fix this, try:

  - Opening task manager and closing down other programs that are using a lot of RAM
  - Modify the operation to optimise for less memory usage
  - Increase the amount of RAM that Venus has been allocated
  - In task manager, go to details, right click the hamilton software and assign priority high

.. _0xa1230002: 

  **0xa1230002: Inserting identifier failed**

  This error means that the parser or executer could not insert the specified identifier into the symbol table. Some examples of how this error can arise are: if the table is corrupted, if the identifier being read causes issues for the parser, or similar. To fix this, try:

  - Replace the identifier with something else temporarily, to determine whether it is the identifier causing the issue or something else
  - Check to make sure the identifier has all the data associated with it that the symbol table needs. Typically this includes name, type and attributes
  - Check to make sure the identifier doesn't include any symbols that might interfere with the parser. These can include anything outside of standard ASCII characters from range 0xa0 - 0x7F.

.. _0xa1230003:

  **0xa1230003: Identifier not found**

  This error means that the parser or executer could not find the specified identifier in the symbol table. This usually means something like a sequence or variable has either not been added or has been added but misspelt. To fix this, try:

  - Check what the error says. It should be an error which tells you the name of what it fails to lookup, which is useful for debugging purposes.
  - Check whether the name given in the error is spelt correctly; if not then that needs correcting
  - Check whether the name given in the error has been initialised/defined. It may be there, it may be there but misspelt, it may not be there at all. If it isn't there, add it and try again. If it is there but misspelt, rename it to the correct item. 
  - If the name is there and spelt correctly, make sure that the correct symbol table is being called during the method

.. _0xa2230004: 

  **0xa2230004: L-value not a number**

  This error means that the executor has detected that the left hand side of the expression at the specified line is not a number. The error thrown will usually include the line number from which the error arose; this will be the line number in the HSL code. Look up the error to find whereabouts in the Venus code it corresponds to, but don't fix it in the HSL method editor; otherwise you can only use HSL method editor from that point onwards as Venus only compiles one way med --> hsl. This usually occurs when two values are being added and one of them is not a number but instead a string. To fix this, try:

  - Checking whether you are trying to add two numbers or concatenate two strings, both have similar syntax. 
  - If trying to add two numbers, check which one is on the left e.g. s in the equation v = s + 1
  - Make sure the selected number is a number and not a string or similar. You can either convert it to a number manually, or you can input a step into the method which automatically converts strings to their float/int equivalents. This can be performed by the StrFVal function from HSLStrLib.
  - If trying to concatenate two strings, then the leftmost value is still being stored as a number rather than a string
  - Use the StrFStr function from HSLStrLib to convert a floating point number into the correpsponding character string before concatenating.

.. _0xa2230005: 

  **0xa2230005: R-value not a number**

  This error means that the executor has detected that the right hand side of the expression at the specified line is not a number. The error thrown will usually include the line number from which the error arose; this will be the line number in the HSL code. Look up the error to find whereabouts in the Venus code it corresponds to, but don't fix it in the HSL method editor; otherwise you can only use HSL method editor from that point onwards as Venus only compiles one way med --> hsl. This usually occurs when two values are being added and one of them is not a number but instead a string. To fix this, try:

  - Checking whether you are trying to add two numbers or concatenate two strings, both have similar syntax. 
  - If trying to add two numbers, check which one is on the right e.g. 1 in the equation v = s + 1
  - Make sure the selected number is a number and not a string or similar. You can either convert it to a number manually, or you can input a step into the method which automatically converts strings to their float/int equivalents. This can be performed by the StrFVal function from HSLStrLib.
  - If trying to concatenate two strings, then the leftmost value is still being stored as a number rather than a string
  - Use the StrFStr function from HSLStrLib to convert a floating point number into the correpsponding character string before concatenating.

.. _0xa1230006:

  **0xa1230006: Not an identifier**

  This error means that the symbol table entry of the identifier at the specified line is not an identifier. To fix this, try: 

  - Changing the name of the identifier being used. You can also look through the method to confirm that the identifier is being used and that you are not misspelling anything

.. _0xa1220007:

  **0xa1220007: Unrecognized token**

  This error means that the executor detected an unrecognized token. This usually means that what it is trying to parse contains characters that are not allowed. A typical example of this is when a JSON Parser tries to parse HTML, and encounters the \"<\" character. To fix this, try:

  - Identify what code line the error comes from via the HSL code, and then look at that code in Venus. 
  - Look through the code that the executor is trying to manage and try identify any characters that might not be standard. This includes anything outside of the normal ASCII range of 0xa0 - 0x7F. Remove or replace those characters
  - Check that any special characters that are part of strings have backslashes in front of them.

.. _0xa1230008:

  **0xa1230008: R-value not bound**

  This error occurs when the R-value in a line is not bound to a valid value. An example would be v = a + b, where b has not been assigned to any value, or has been assigned to a sequence rather than a variable and thus cannot take part in this operation. To fix this, try:

  - Identify what code line the error comes from via the HSL code, and identify what variable is on the right hand side of that line
  - Check to see what the type of that variable is. If not obvious from reading the code, you can use the StrGetType function from HSLStrLib, or CheckValueType from HSLUtilLib2, or go through and try specific ones such as IsBoolean from HSLUtilLib.
  - If the variable is the correct type, check to see that it has been assigned to the right value. An easy way to do this is just to add in a step which traces the variable value immediately before the error.
  - If the variable is the right type and the correct value, check to see what value the line is expecting --> could it be mistakenly expecting a string concatenation instead of a summation.

.. _0xa2230009:

  **0xa2230009: Bad number**

  This error means that the executor detected an error in a number at the specific line. This often occurs if a number is of the wrong format e.g. int rather than flt. To fix this, try:

  - Check what number is causing the error to occur by looking at the line given in the error code. 
  - Work out what type the line is expecting the number to be --> for example, a loop counter will be expecting an integer rather than a float
  - Check what type the number causing the error is. This can be done using the CheckValueType from HSLUtilLib2, or the IsFloat/IsInteger functions from HSLUtilLib. 
  - If unsure, just toggle the number type and see if swapping it from int to flt or vice versa helps. 

.. _0xa123000a: 

  **0xa123000a: Bad tree**

  This error means that the executor detected an error in the structure of the syntax tree.

.. _0xa123000b:

  **0xa123000b: Invalid entry**

  This error means that the executor has detected an invalid symbol table entry. This error usually occurs if there is a non-ASCII character present in the symbol table, and the executor was not the one who inserted the value into the symbol table in the first place. To fix this, try:

  - Work out which characters in the symbol table are invalid
  - Try to replace those characters with their ASCII equivalents, as well as work out where/why they were added in teh first place

.. _0xa122000c:

  **0xa122000c: Function identifier is protected**

  This error means that the parser or executor detected a protected function identifier in the symbol table at the specified line. This happens if a device is declared in the local scope, for example. To fix this, try:

  - Checking to make sure nothing is in the local scope which shouldn't be

.. _0xa223000d:

  **0xa223000d: Underspecified**

  This error means that the executor detected underspecified formal parameters of a function at the specific line. To fix this, try:

  - Check what line the error gives as the function going wrong, look at that line in HSL and work out the correct location in Venus code
  - Look at whatever functions are present on that line and check how many input parameters the functions are meant to have vs how many they actually have
  - Make sure all input parameters exist and are not just empty variables/arrays/sequences.

.. _0xa2230037:

  **0xa2230037: Overspecified**

  This error means that the executor detected overspecified formal parameters ofa  function at the specific line. To fix this, try:

  - Check what line the error gives as the function going wrong, look at that line in HSL and work out the correct location in Venus code
  - Look at whatever functions are present on that line and check how many input parameters the functions are meant to have vs how many they actually have
  - Make sure all input parameters exist and are not just empty variables/arrays/sequences.

.. _0xa123000e:

  **0xa123000e: Setting value failed**

  This error means that the executor failed to set the value of a symbol table entry at the specified line. To fix this, try:

  - Check what line the error gives as the function going wrong, look at that line in HSL and work out the correct location in Venus code
  - See what value is trying to be set within the symbol table; make sure it has no special characters, the correct type and attributes

.. _0xa123000f:

  **0xa123000f: Function identifier not found**

  This error occurs when the executor failed to lookup a function identifier in the symbol table at the specified line. This usually means the function has not been defined properly or has failed to import into the symbol table properly. It can also be the result of a misspelt name at any steps involving it. To fix this, try:

  - See what the name of the function is that isn't being found
  - Check to see if the function name is spelt correctly
  - Check to see earlier in the method that the function has been defined and imported successfully into the symbol table
  - Check to see if this happens everytime this function is called or just this one step. If it happens every time then it is likely a definition/import issue, if only once then it is likely a naming/exporting issue.

.. _0xa1230010:

  **0xa1230010: Bindings not found**

  This error occurs when the executor failed to lookup the value bound to a formal parameter in the symbol table at the line specified. 

.. _0xa1230011:

  **0xa1230011: Temporary variable not found**

  This error occurs when the executor failed to delete the identifier of a temporary variable in the symbol table at the line specified.

.. _0xa1230012:

  **0xa1230012: Unknown function type**

  This error occurs when the executor detects a function which hasn't been defined at the specific line. To fix this, try:

  - Work out which function hasn't been defined based on the line of code which throws the error
  - Check whether function name is misspelt
  - Check whether function is defined post calling rather than pre calling
  - Check whether function has been defined at all

.. _0xa2230013:

  **0xa2230013: Unable to find file**

  This error occurs when the executor can't find the file specified. To fix this, try:

  - Check the line of code to determine what the path of the file is that is nonexistent
  - Determine whether the path was computer specific and the method has been ported across computers e.g. was the file in C:\\Users\\tchapman and should be in C:\\Users\\Hamilton. To avoid this in the first place, save things in the Hamilton folder of the C:\\Program Files x86 instead. 
  - Check whether the file has been moved since the path was created
  - Check whether the file name has been misspelt
  - If file name is a variable, check to see it has been defined correctly

.. _0xa1230014: 

  **0xa1230014: Type mismatch**

  This error occurs when the executor detects a mismatch between the types of variable fed into a function compared to the defined parameter that the function is meant to have an as input. To fix this, try:

  - Check which function is causing the error
  - Check what type of input the function is expecting; will hopefully be in the documentation, if not you can delve into the HSL code for that function and see directly
  - Check what type of variable you are feeding in to the function and confirm it matches the type the function is expecting

.. _0xa2230015:

  **0xa2230015: Bad L-value**

  This error occurs when the left hand side value for an operation is incorrect for the operation. To fix this, try:

  - Check what type of variable the operator is expecting
  - Check what type of variable you are feeding into the operator equation
  - This error could be using the wrong operator e.g. & rather than +, or by using the wrong variable type e.g. float rather than int

.. _0xa2230016:

  **0xa2230016: Bad R-value**

    This error occurs when the right hand side value for an operation is incorrect for the operation. To fix this, try:

  - Check what type of variable the operator is expecting
  - Check what type of variable you are feeding into the operator equation
  - This error could be using the wrong operator e.g. & rather than +, or by using the wrong variable type e.g. float rather than int

.. _0xa2220017:

  **0xa2220017: Unrecognized type**

  This error occurs when the executor detects an unrecognized storage type at the specified line.

.. _0xa1230018: 

  **0xa1230018: Bad memory type**

  This error occurs when the executor detects a bad memory type for an array at the specified line.

.. _0xa1230019:

  **0xa1230019: Array reference out of bound**

  This error occurs when the executor detects an invalid index for an array at a specified line. To fix this, try:

  - Check the size of the array that is being queried
  - Check which value from the array you are expecting to call and check what index that value has
  - Potentially add a step into the method to find that index on a dynamic basis so that you can change the array earlier in the method without messing up that step

.. _0xa123001a:

  **0xa123001a: Bad array identifier type**

  This error occurs when the executor detects an unrecognized storage type for an array identifier at the specified line.

.. _0xa123001b: 

  **0xa123001b: Tag insert failed**

  This error occurs when the executor fails to insert an identifier into the tag table of a structure definition at the specified line.

.. _0xa123001c:

  **0xa123001c: Dynamic memory identifier not bound**

  This error occurs when the executor detected at the specified line an identifier of a dynamic memory object that was not bound to a valid value. This is when a variable or data structures has been allocated at runtime, and has been assigned an incorrect value, such as binding an identifier that is meant to be a variable to a submethod instead. As far as I'm aware, this is only possible to do by editing the HSL code, I don't think the method editor has any functions that allow you to bind identifiers incorrectly, I'm not 100% certain on that though. To fix this, try: 

  - Locate the identifier that is causing the error (should be possible in either the method editor or the hsl method editor)
  - Confirm what kind of object the identifier is meant to be
  - Work out what method editor step corresponds to the incorrect HSL code, which is likely to be a block of HSL code inserted directly into the method editor
  - Correct that code (if you have knowledge of HSL) or replace it with method editor steps that have the same functionality. If you're really attached to the HSL block of code but aren't proficient with HSL, try to make the same function with method editor steps in a separate method, look at the HSL code that generates, and copy that HSL code into the original method as an inserted block of HSL. 

.. _0xa123001d:

  **0xa123001d: Tag identifier not bound**

  This error occurs when the executor detected at the specified line an identifier of a structure tag object that was not bound to a valid value. A structure tag object is a piece of metadata associated with a variable. In this error, a variable is expected to have some sort of tag, but the tag doesn't exist. To fix this, try:

  - Determine which variable the tag is meant to be associated with based on the specified line
  - From that, work out what kind of tag is meant to be present. This is doable by looking at the HSL code. In the HSL Method Editor Help section, you can go to HSL Reference \> Declaration of Objects \> Declaration of Structure Objects to see what the format of tag declaration is meant to be, and therefore can compare this to the code in the method associated with the object declaration
  - Add the assignment of the tag in the method editor code, confirming via the HSL that the tag has been assigned correctly. You can also assign the tag via an HSL code insert step.

.. _0xa123001e:

  **0xa123001e: Structure reference out of bound**

  This error occurs when the executor detects a reference to an element of a structure which is outside the allowed range. A few examples of this are integers which are too large or too small, or strings which are too long. To fix this, try:

  - Determine which reference is out of bounds. This should be doable by looking at the HSL code; the error message in the trace file should show you which line is the one causing the problems. 
  - Locate in the HSL code where the bounds of the identifier have been set; this can usually be done by searching the HSL file for "struct" functions, and then seeing what character(s) follow the "}" character. 
  - Depending on the requirements of the reference, either adjust the reference bounds assignment to include the target value, or adjust the function which is causing the error to ensure the reference is always within the specified bounds (e.g. splitting/truncating strings, editing loops to only contain correct integers)

.. _0xa123001f:

  **0xa123001f: Bad tag identifier type**

  This error occurs when the identifier of a structure tag object has been assigned to an incorrect type, such as a being assigned a string rather than an integer. To fix this, try:

  - Determine what tag is causing the problem by looking at the HSL code associated with the line specified in the trace file
  - Identify what type of data the tag is expecting
  - If the tag is expecting a string rather than an int, locate the assignment and add quotation marks around the assignment
  - If the tag is expecting an int rather than a string, locate the assignment and either use a function to convert the string to an int or remove the quotation marks around the assignment
  - If the tag is expecting an int rather than a float or vice versa, locate the assignment and use a function to convert one to the other. 
  - Functions to convert the variable type are present in the HSLExtensions:Core library

.. _0xa1230020:

  **0xa1230020: L-value is not a structure identifier**

 This error occurs when the executor detects a data reference which is not a structure at the specified line, in the left hand side of the assignment.

.. _0xa1230021:

  **0xa1230021: L-value is not an array identifier**

  This error occurs when the executor detects a data reference which is not an array at the specified line, in the left hand side of the assignment.

.. _0xa1230022: 

  **0xa1230022: Failed to lookup tag identifier in the tag table**

  This error occurs when the executor detects a tag identifier which is not a member of the tag table. To fix this, try:

 - Checking whether your tag is correctly spelled
 - Attempt to add your tag to the tag table
 - Change your tag to be one which is present in the tag table already

.. _0xa1230023:

  **0xa1230023: Signal break**

  This error occurs when the executor detects an invalid break statement at the specified line.

.. _0xa1230024:

  **0xa1230024: Copy out of bound**

  This error occurs when the executor detects a structure copy which is out of bound.

.. _0xa1230025:

  **0xa1230025: Signal return**

  This error occurs when the executor detects an invalid return-statement.

.. _0xa2230026:

  **0xa2230026: Array size is not an integer**

  This error occurs when the executer detects an error in the size of an array at the specified line. This is usually if an array is assigned to a float or string by accident. To fix this, try:

  - Check where the size of the array was assigned. If it was done via a calculation (especially a division), it is often assigned a float even when the numbers divide exactly.
  - If the assignment of size was done via a variable, check to ensure the variable was written as an integer and not as a string
  - If you can't identify where the mistake is in assignment type, you can try use one of the convert-to-integer functions and see whether that works or whether it throws up a fresh error.
  - Make sure the array size is positive
  - Try assigning the array size dynamically, i.e. when declaring the array make it empty, and then add items to it at the end of the array rather than at specific locations

.. _0xa1230027: 

  **0xa1230027: Failed to copy tag table**

  This error occurs when the executor fails to copy the tag table.

.. _0xa1230029:

  **0xa1230029: Function has not been defined**

  This error occurs when a function has not been defined in the library it is being called from. To fix this, try:

  - If you are the author of the target library, open the code in HSL and check whether the function has been defined at all, or if it is only defined in one namespace, or if it has been misspelled, or if it has been incorrectly commented out
  - If you are not the author of the library but are proficient in HSL, you can do as above, but would be worth making a copy of the library and editing that instead
  - Otherwise, remove the function from your method and find an alternative way of doing whatever you were aiming to do

.. _0xa123002a: 

  **0xa123002a: Unable to enter nesting level**

  This error occurs when the executor failed to enter the nesting level at the specified line.

.. _0xa123002b:

  **0xa123002b: Unable to exit nesting level**

  This error occurs when the executor failed to exit the nesting level at the specified line.

.. _0xa122002c: 

  **0xa122002c: No context**

  This error occurs when the executor fails to create a new symbol table at the specified line.

.. _0xa123002d:

  **0xa123002d: Failed to read file**

  This error occurs when the executor fails to read a specific file. To fix this, try:

  - Ensure the file path specified is a correct and valid path
  - Ensure the file you are trying to read exists
  - Check whether the file has the hidden attribute. If so, you can use the File Handling library to remove that property dynamically during the run, or do it manually in file explorer
  - Ensure that the file is in a location that Venus has access to

.. _0xa123002e:

  **0xa123002e: Failed to create timer**

  This error occurs when the executor or parser fails to create a timer at the specified line

.. _0xa123002f:

  **0xa123002f: Failed to set timer**

  This error occurs when the executor fails to set a timer at the specified line

.. _0xa1230030:

  **0xa1230030: Failed to wait timer**

  This error occurs when the executor fails to wait for at timer to be signaled at the specified line

.. _0xa1230031:

  **0xa1230031: Failed to create event**

  This error occurs when the parser or executor fails to create an event at the specified line

.. _0xa1230032:

  **0xa1230032: Failed to set event**

  This error occurs when the executor fails to set an event at the specified line

.. _0xa1230033:

  **0xa1230033: Failed to wait event**

  This error occurs when the executor fails to wait for an event to be signaled

.. _0xa1230034:

  **0xa1230034: Bad argument**

  This error occurs when the executor detects an error in the function argument at the specified line. An example of this would be having a File:Set Position command with a non-integer value as the input; as positions can only take integer values. To fix this, try: 

  - Determine from the trace file which line and function are causing these errors
  - Determine the type of input the function is expecting (e.g. int, str, var)
  - Determine any bounds the function input has (e.g. max 300uL volume for 300uL tips)
  - Check your input and see which of the above it doesn't meet
  - If your input is the right value but the wrong type, there are various functions that can convert variables from one type to another - for example in HSLMthLib you can convert floats to ints, ints to strings, etc.

.. _0xa2230035:

  **0xa2230035: Syntax error**

  This error occurs when the parser detects syntax errors in the method

.. _0xa2230036:

  **0xa2230036: Integer divide by zero**

  This error occurs when the executor detects an integer divide by zero at a specified line. To fix this, try:

  - Determine which variable/integer is being treated as a zero in the calculation
  - Check that that variable/integer has an assignment step associated with it; without one it will default to zero
  - Check that the variable is correctly spelled; if incorrectly spelled (compared to its assignment) it will default to zero

.. _0xa2230038:

  **0xa2230038: Returning address of local variable or temporary**

  This error occurs when the executor detects a function returning the address of a local or temporary variable. This causes problems as local variables and temporary variables are destroyed upon function return, so the address returned becomes invalid. To fix this, try:

  - Converting the variable that is being returned to global or task local
  - Removing the function return value if it isn't essentially

.. _0xa2230039:

  **0xa2230039**

  This error occurs when a library requires an installer to be run before use and the installer hasn't yet been run. An example of this would be the Dynamic Liquid Classes library. To fix this, try:

  - Contact me directly as there is a reasonable chance I have the installer and can send it over
  - Contact your Hamilton apps specialist
  - Go into the hsl file for the library, find the author (usually in the final line or at the top commented out) and contact them directly

.. _0xa223003a:

  **0xa223003a: Unable to find file**

  This error occurs when the executor couldn't find the file at the specified line. To fix this, try:

  - Checking that the file isn't a hidden file
  - Checking that the file exists
  - Checking that the file is in the location specified in the path
  - Checking that the path is correct with no spelling mistakes and has double backslashes instead of single
  - Check that the file is in a location that Venus has access to

.. _0xa223003b:

  **0xa223003b: File not updatable**

  This error occurs when the executor is asked to update a non-updatable file. To fix this, try:

  - Removing the read-only tag of the file, which can either be done manually in file explorer or using the File Handling library
  - Moving the file to a location that Venus has edit access in (such as to documents instead of Program Files section)
  - Giving venus the appropriate permissions to edit files in that area
  - Making sure the file isn't in use by another program or open separately

.. _0xa223003c:

  **0xa223003c: Recursive call**

  This error occurs when the executor detects a recursive or concurrent funtion call. To fix this, try:

  - If the function is one from an HSL library, remove the function from your method and find an alternative way of doing whatever you were trying to do, or edit the HSL file to fix it if you are proficient in HSL
  - If the recursion is caused by function parameter input, change the parameters to be not that function. If need be you can create two copies of a function and call one from within the other.
  - If the concurrency is caused by a method fork in which both call the same function, you can either stop the fork or add in a "wait for event" clause to ensure that they trigger sequentially rather than concurrently

.. _0xa223003d:

  **0xa223003d: Failed to wait for thread(s)**

  This error occurs when the executor fails to wait for one or more threads to be signaled. 

.. _0xa223003e:

  **0xa223003e: Time-out interval elapsed**

  This error occurs when the time-out window for a specific function or error elapses without user response. To fix this, try:

  - Ensure that the user is present at the STAR or that there is a way of notifying the user when a time-out dialog pops up
  - If the dialog is one caused by a function, increase the time-out period of the dialog, or set it to an infinite timeout (usually by setting the timeout to 0)

.. _0xa2220044: 

  **0xa2220044: Automation type not supported**

  This error occurs when there is a reference to an automation function which has a parameter that is not supported.

.. _0xa1230046:

  **80xa1230046: Bad argument parameter**

  This error occurs when the executor detects an error in a function argument at the specified line. To fix this, try:

  - Determine which argument within the function is causing the error
  - Confirm that the argument is the correct type (e.g. a string of 0 vs an int of 0)
  - Check that the argument has not been misspelled if it is a variable
  - Check that the function being called is the correct one

.. _0xa123004d: 

  **0xa123004d: Sequence property not found**

  This error occurs when the sequence property being referenced is not found. To fix this, try:

  - If the sequence is one which is defined in the layout file, go into the layout file and view/edit the sequence properties there
  - If the sequence is one which is defined during the method, confirm that the step defining the referenced property exists
  - Confirm that the step defining the referenced property is not commented out, is called in advance of the sequence property being referenced, and is not misspelled

.. _0xa123004e:

  **0xa123004e: Int64 not supported**

  This error occurs when a 64 bit integer is used on certain platforms. To fix this, try:

  - Moving off a windows 2000 platform
  - Changing the integer to a 32 bit integer

.. _0x00000001:

  **0x00000001: The parameter is incorrect**

 This error occurs when the parameter input into a function is incorrect. To fix this, try:

  - Check that the variable type inputted into a function is correct, for example not an integer instead of a string/float.
  - Check that the parameter value is within the acceptable range; either length for string or upper and lower limits for int or float or bool

.. _0xa1630001: 

  **0xa1630001: Unexpected error**

  This error occurs when there is an error in an HSLUtilLib2 step which is not covered by any of the other error messages.

.. _0xa1630002: 

  **0xa1630002: Create object failed/Invalid parameter**

  This error is listed as Create Object Failed in the index of HSLUtilLib2, but described as invalid parameter. I'm assuming that the latter is correct, in which case the error occurs when one or more parameters for an HSLUtilLib2 step is invalid. To fix this, try: 

  - Check what parameters the function called is expecting and compare to the ones you're feeding in
  - Check whether you are feeding in the correct number of parameters

.. _0xa1630003:

  **0xa1630003: Value Check Failed Invalid Type**

  This error occurs when the executor finds a function parameter or read from file that is not of the expected type. To fix this, try:

  - Check what type of parameter you're feeding in to the function or file and make sure it is the expected type. The expected type should be findable in the documentation, if not then it should be findable in the raw HSL code. 
  - Check that the parameter is actually being fed into the function and that it hasn't been misspelt
  - Check that the file is present in the right location and hasn't been corrupted or moved to the incorrect place

.. _0xa1630004:

  **0xa1630004: Value Check Failed Invalid Range**

  This error occurs when the executor finds a function parameter or read from file that is not within the expected range. To fix this, try:

  - Check what the expected range of the function or file read. This should be findable in the documentation, but will be in the raw HSL code if not.
  - Check what the value of the parameter being fed in is.
  - Check whether the range is due to the parameter being mistakenly high or the function range being mistakenly low.

.. _0xa1630005: 

  **0xa1630005: Labware Error**

  This error occurs when the access of labware based on LabwareID and PositionID causes an error. To fix this, try:

  - Check that the labware/position IDs have been spelt correctly
  - Check that the layout file for the method is the correct one
  - Check that the labware still exists on the system deck and hasn't been deleted
  - Check that the labware file still exists in the system database and hasn't been moved or deleted

.. _0xa1630006:

  **0xa006: Array Index Not A Number**

  This error occurs when the index of the specified array is not a positive integer. To fix this, try:

  - Identify what the index of the array is e.g. is it a float, a negative integer, a string
  - If the identifier is a numeric string or a float that ends in .0, use a convert to int function
  - If the array index is something other than that, try to assign it to a positive integer as a key code or unique identifier

.. _0xa1630007:

  **0xa1630007: Array Index Not An Integer**

  This error occurs when the index of the specified array is a float rather than an integer. To fix this, try:

  - If the index is at a .0, use a convert to int function
  - If the index is at a non .0, either use a floor or ceiling function, or assign a positive integer as a key code or unique identifier

.. _0xa1630008:

  **0xa1630008: Array Index Must Not Be Negative**

    This error occurs when the index of the specified array is less than 1. To fix this, try:

  - If the index is less than 0, perhaps take the absolute value of the index, provided that doesn't clash with another identifier.
  - If the index is between 0 and 1, or the abs value of the index would clash, work out where you want the value to be within the array. If it needs inserting, use an insert function from one of the array libraries. If it doesn't need inserting, get the length of the array and append the value and assign it that as the index.

.. _0xa1630009:

  **0xa1630009: Array Index Must Not Be Greater Than Array Size**

  This error occurs when the index of the specified array is greater than the size of the array. To fix this, try:

  - Check what the index of the value in the array that you are intending to call is and assign it to that
  - If the value is not within the array correctly, adjust the size of the array to be one larger and append the value at the end of the array or use an insert function from an array library. 
