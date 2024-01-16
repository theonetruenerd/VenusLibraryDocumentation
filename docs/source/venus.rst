Venus
==============================================

This section aims to cover the *functions* that Venus can run. Documentation on more general principles of Venus, including things like the liquid editor and labware editor, will be found separately.

NB: This section is probably coming last as out of all of the Venus resources it has the best documentation.

The Venus functions are split into a few main categories:

- :ref:`General Steps`
- :ref:`ML_STAR`
- :ref:`Custom Dialog Steps`


General Steps
------------------------------------------------

The general steps are steps which are not instrument-specific (and thus not hardware-related), and aren't involved in custom dialog creation. They are the following:

- :py:func:`Comment`
- :py:func:`Assignment`
- :py:func:`Assignment with Calculation`
- :py:func:`Loop`
- :py:func:`Loop: Break`
- :py:func:`If, Else`
- :py:func:`Array: Declare / Set Size`
- :py:func:`Array: Set At`
- :py:func:`Array: Get At`
- :py:func:`Array: Get Size`
- :py:func:`Array: Copy`
- :py:func:`Sequence: Get Current Position`
- :py:func:`Sequence: Set Current Position`
- :py:func:`Sequence: Get End Position`
- :py:func:`Sequence: Set End Position`
- :py:func:`Adjust Sequences`
- :py:func:`File: Open`
- :py:func:`File: Read`
- :py:func:`File: Write`
- :py:func:`File: Set Position`
- :py:func:`File: Close`
- :py:func:`Timer: Start`
- :py:func:`Timer: Wait For`
- :py:func:`Timer: Read Elapsed Time`
- :py:func:`Timer: Restart`
- :py:func:`User Input`
- :py:func:`User Output`
- :py:func:`Shell`
- :py:func:`Set Event`
- :py:func:`Wait for Event`
- :py:func:`Return`
- :py:func:`Abort`
- :py:func:`Error Handling by the User`
- :py:func:`Begin Parallel`
- :py:func:`End Parallel`


ML_STAR
--------------------------------------

The ML_STAR steps are steps which relate to the ML_STAR and interact with its hardware specifically, doing things such as pipetting, moving channels, etc. They are split into two categories; the four Smart Steps and the remaining Single Steps. They are as follows:

- :py:func:`1000uL Channel Aspirate`
- :py:func:`1000uL Channel Dispense`
- :py:func:`iSWAP Transport`
- :py:func:`1000uL Channel CO-RE Grip Transport`
- :py:func:`1000uL Channel Tip Pick Up (Single Step)`
- :py:func:`1000uL Channel Aspirate (Single Step)`
- :py:func:`1000uL Channel Dispense (Single Step)`
- :py:func:`1000uL Channel Dispense on the Fly (Single Step)`
- :py:func:`1000uL Channel Tip Eject (Single Step)`
- :py:func:`1000uL Channel Get Last Liquid Level (Single Step)`
- :py:func:`1000uL Channel Aspirate 2nd Phase (Single Step)`
- :py:func:`Initialize (Single Step)`
- :py:func:`Lock/Unlock Front Cover (Single Step)`
- :py:func:`iSWAP Get Plate (Single Step)`
- :py:func:`iSWAP Place Plate (Single Step)`
- :py:func:`iSWAP Move Plate (Single Step)`
- :py:func:`iSWAP Open Gripper (Single Step)`
- :py:func:`iSWAP Close Gripper (Single Step)`
- :py:func:`iSWAP Get First Plate Position (Single Step)`
- :py:func:`iSWAP Park (Single Step)`
- :py:func:`1000uL Channel CO-RE Grip Get Plate (Single Step)`
- :py:func:`1000uL Channel CO-RE Grip Place Plate (Single Step)`
- :py:func:`1000uL Channel CO-RE Grip Move Plate (Single Step)`
- :py:func:`1000uL Channel Move To Position (Single Step)`
- :py:func:`Wait for TADM Upload (Single Step)`

Custom Dialog Steps
------------------------------------------

The custom dialog steps only has a single step called custom dialog, which helps in the creation of more personalised versions of the standard User Input and User Output dialogs. 

- :py:func:`Custom Dialog`


