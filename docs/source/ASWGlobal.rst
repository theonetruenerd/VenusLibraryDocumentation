ASWGlobal
============================================================

The ASWGlobal library doesn't add any functions, but instead declares common HSL constants  used in other libraries, SMTs, and methods. These are often used as the return values for functions. The constants it declares are:

  - False, No, and Off are all assigned as being hslFalse
  - True, Yes, and On are all assigned as being hslTrue
  - For dialogue buttons, each one is assigned a specific number: 
    - Ok = 1
    - Cancel = 2
    - Abort = 3
    - Retry = 4
    - Ignore = 5
    - Yes = 6
    - No = 7
  - Clicking STOP on a timer is assigned as being 3
