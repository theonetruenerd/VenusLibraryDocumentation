Error Codes & Debugging
===========================

I will try compile as many different error codes and their explanations here, as well as potential causes and solutions to deal with them as and when they pop up. If there are any you wish to add, please message me on my discord "theonetruenerd" or email me at "tarunchapman@hotmail.com". Notably, the error codes that show up in the trace look slightly different to the ones presented here. If the trace error code looks like this: (0x12 - 0x3 - 0x45) [which corresponds to (MinorID - MajorID - SpecificErrorID)], then the translated error code will look like this: 0xa3120045. The error code should always be 10 digits long, with zeroes padding the bit between the 2 and 45. 

The Major ID is usually assigned in the library which is causing the error; for example in HSLUtilLib2 there is a function called "Error" in which there is a static const variable called MajorID. The minor ID corresponds to the general type of error; in HSLUtilLib2 "0x01" is used to refer to a general runtime error.

  - :ref:`Runtime Errors <RuntimeErrors>`
  - :ref:`Syntax Errors <SyntaxErrors>`
