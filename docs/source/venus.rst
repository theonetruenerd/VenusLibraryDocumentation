Venus
==============================================

This section aims to cover the *functions* that Venus can run. Documentation on more general principles of Venus, including things like the liquid editor and labware editor, will be found separately.

Venus functions are organised into several sections. These are the following:


  - :ref:`General Steps`
  - :ref:`Scheduler Steps`
  - :ref:`Custom Dialog Steps`
  - :ref:`Favourites`
  - :ref:`Templates`

There are also instrument specific functions in their own categories:

  - :ref:`ML_STAR`
  - :ref:`Microlab STAR Smart Steps`

.. General Steps

  The general steps are composed of relatively standard coding functions that will be present in many other coding languages. These are not associated with the hardware of any instrument and are present on Venus regardless of whether you are using a STAR, a STARLet, or any other instrument which uses Venus. The functions which fall under general steps are listed below:

  - :ven:func:`Comment`
  - :ven:func:`Assignment`
  - :ven:func:`Assignment with Calculation`
  - :ven:func:`Loop`
  - :ven:func:`Loop: Break`
  - :ven:func:`If, Else`
  - :ven:func:`Array: Declare / Set Size`
  - :ven:func:`Array: Set At`
  - :ven:func:`Array: Get At`
  - :ven:func:`Array: Get Size`
  - :ven:func:`Array: Copy`
  - :ven:func:`Sequence: Get Current Position`
  - :ven:func:`Sequence: Set Current Position`
  - :ven:func:`Sequence: Get End Position`
  - :ven:func:`Sequence: Set End Position`
  - :ven:func:`Adjust Sequences`
  - :ven:func:`File: Open`
  - :ven:func:`File: Read`
  - :ven:func:`File: Write`
  - :ven:func:`File: Set Position`
  - :ven:func:`File: Close`
  - :ven:func:`Timer: Start`
  - :ven:func:`Timer: Wait for`
  - :ven:func:`Timer: Read Elapsed Time`
  - :ven:func:`Timer: Restart`
  - :ven:func:`User Input`
  - :ven:func:`User Output`
  - :ven:func:`Shell`
  - :ven:func:`Set Event`
  - :ven:func:`Wait for Event`
  - :ven:func:`Return`
  - :ven:func:`Abort`
  - :ven:func:`Error Handling by the User`
  - :ven:func:`Begin Parallel`
  - :ven:func:`End Parallel`

.. Scheduler Steps

  The scheduler steps are functions which arrange the method to be executed on a number of resources and submitted to capacity, time and precedence relations in a way that fulfils the optimality criteria. The methods and its activation criterions are defined in a workflow.

The Schedule process is divided into two phases: scheduling and executing. The scheduler functions are listed below:

  - :ven:func:`Select Method`
  - :ven:func:`Activate Task`
  - :ven:func:`Cancel Task`
  - :ven:func:`Schedule Block`
  - :ven:func:`Reschedule`

.. Custom Dialog Steps

  The custom dialog steps only adds the :ven:func:`Custom Dialog` function, which allows creation of more complicated dialogs than the standard :ven:func:`User Input` and :ven:func:`User Output` functions. 

.. Favourites

  The favourites drop-down allows you to select functions which you use frequently to be in their own separate tab so that they are easier to find. These steps will be favourited on every method.

.. Templates

  Templates add the ability to preprogram commonly used functions and processes/sets of functions so that the user doesn't have to write them freshly every time. An example might be a tip pickup step with all the parameters for pickup already programmed in so you don't have to fill them in, or a bulk creation of arrays for an ASW Dialog.

.. ML_STAR

  The ML_STAR section adds the core functions which interact with the ML_STAR itself, which is anything that interacts with the hardware or firmware of the STAR. They are split into the power steps and single steps. The single steps are then split into liquid handling functions, preparation functions, transport functions, and miscellaneous functions. The functions which come under the ML_STAR tab are:

- :ven:func:`1000ul Channel Aspirate`
- :ven:func:`1000ul Channel Dispense`
- :ven:func:`CO-RE 96 Head Aspirate`
- :ven:func:`CO-RE 96 Head Dispense`
- :ven:func:`iSWAP Transport`
- :ven:func:`1000ul Channel CO-RE Grip Transport`
- :ven:func:`1000ul Channel Tip Pick Up (Single Step)`
- :ven:func:`1000ul Channel Aspirate (Single Step)`
- :ven:func:`1000ul Channel Dispense (Single Step)`
- :ven:func:`1000ul Channel Dispense on the Fly (Single Step)`
- :ven:func:`1000ul Channel Tip Eject (Single Step)`
- :ven:func:`1000ul Channel Get Last Liquid Level (Single Step)`
- :ven:func:`1000ul Channel Aspirate 2nd Phase (Single Step)`
- :ven:func:`CO-RE 96 Head Tip Pick Up (Single Step)`
- :ven:func:`CO-RE 96 Head Aspirate (Single Step)`
- :ven:func:`CO-RE 96 Head Dispense (Single Step)`
- :ven:func:`CO-RE 96 Head Tip Eject (Single Step)`
- :ven:func:`Initialize (Single Step)`
- :ven:func:`Calibrate Carrier (Single Step)`
- :ven:func:`Lock/Unlock Front Cover (Single Step)`
- :ven:func:`iSWAP Get Plate (Single Step)`
- :ven:func:`iSWAP Place Plate (Single Step)`
- :ven:func:`iSWAP Move Plate (Single Step)`
- :ven:func:`iSWAP Open Gripper (Single Step)`
- :ven:func:`iSWAP Close Gripper (Single Step)`
- :ven:func:`iSWAP Get First Plate Position (Single Step)`
- :ven:func:`iSWAP Park (Single Step)`
- :ven:func:`1000ul Channel CO-RE Grip Get Plate (Single Step)`
- :ven:func:`1000ul Channel CO-RE Grip Place Plate (Single Step)`
- :ven:func:`1000ul Channel CO-RE Grip Move Plate (Single Step)`

.. Microlab STAR Smart Steps

  Smart steps are functions which are preprogrammed single steps which are combined to be ready for specific tasks such as doing both aspiration and dispensing of a reagent in the same function. The Smart Step functions are:

- :ven:func:`Advanced Load Settings`
- :ven:func:`Load`
- :ven:func:`Load and Match`
- :ven:func:`1000ul Channel Pipette - Simple (1-1)`
- :ven:func:`1000ul Channel Pipette - Replica (1-n)`
- :ven:func:`1000ul Channel Pipette - Pooling (n-1)`
- :ven:func:`1000ul Channel Pipette - Aliquot`
- :ven:func:`Unload`
- :ven:func:`1000ul Channel Needle Wash Settings`
- :ven:func:`1000ul Channel Needle Pick Up`
- :ven:func:`1000ul Channel Needle Eject`
- :ven:func:`1000ul Channel Tip Pick Up`
- :ven:func:`1000ul Channel Tip Eject`

How venus works
-------------------------------------------------------

Venus is a drag-and-drop wrapper for a separate coding language called HSL, standing for Hamilton Standard Language. When coding a method in Venus, all the available functions (core and any from imported libraries) are listed on the left hand side of the screen in a tree view. When you want to add a step to your method, you drag and drop that function from the left hand side and drop it wherever you want it to be in your method. This will then open a dialog box which allows you to input your desired parameters. The method is saved as a .med file, which can be run through a software called HxRunControl.exe. The run control software can run simulations of the code as well as the code on an actual robot. In the run control software window, you can see the deck layout dynamically changing, an open view of the method showing what step you are on, and a trace file which is a type of log which displays the data from every step that is occuring and is timestamped for each step. The trace file is saved to the Log Files folder within the main Hamilton folder in Program Files (x86). Method files (.med) can compile into HSL files (.hsl) which can also be edited and run through the run control software. Instead of being drag-and-drop, HSL is a more standard coding language, with C++ like syntax. HSL files cannot be converted into .med files; as such, it is usually recommended to insert snippets of HSL code into the main .med file rather than coding in HSL itself, or to only use HSL for creation of fresh libraries. 

Libraries are groups of functions which reside in the library folder within the main Hamilton folder. They can be imported into specific methods, at which point the functions associated with that library will appear in the function tree on the left hand side of the method editor. Libraries can either be written in HSL (and are thus .hsl files) or can be "sub-method libraries", which is a series of steps coded in Venus that are stored in a way that works like a function. Sub-method libraries are .smt files. You can have submethods in a normal method file, and it is often encouraged so that your code is "parcelled" into blocks which contain the main blocks of your method. These submethods are just like the normal method but reside in a separate tab in the method editor. 

The following function groups are not libraries and instead are "core" groups which do not need importing; every other function referenced is part of a library.
  - General Steps
  - Scheduler Steps
  - Custom Dialog Steps
  - Favourites
  - Templates
  - ML_STAR
  - Microlab STAR Smart Steps

When pipetting using the 1000ul channels, there are 8 channels total. Channel patterns (which determine which channels are in use at any given point in time) are written in the form of a string of 1s and 0s, where 0 is not in use and 1 is in use. For example, if using channels 2, 3, and 5, the channel pattern would be "01101000". All pipetting steps require a channel pattern input as one of the parameters. Unless specified, the priority of the channels should always be to use the channels with lower indices. 

There are several different tip types available for an ML_STAR, the most commonly used are 300ul (Standard volume, tip id 0), and 50ul (tip id 22). You can also get 10ul tips and 1000ul tips. All tips have the option of being normal, stackable, or filtered. No tip can take up more liquid than its type (i.e. a 300uL tip cannot ever have more than 300ul total volume in it). The 300ul tips should not be used to go below 10ul as they become very inaccurate. When pipetting, the total volume in a channel is the amount of liquid that has been aspirated by that channel minus the amount of liquid that has been dispensed by that channel. 

For arrays in venus, you have to declare the size of the array (which can be empty) and then add items one by one; with the core functions you can't add more than one item at once. To add an item you can either specify an index or add to the end of the array; when adding to an empty array you can only add to the end of the array. Arrays in venus are 1-based rather than 0-based.

For variable naming in venus, the following convention should be followed. If a variable is an integer, it should be prefixed with "int_". If it is a float, it should be prefixed with "flt_". If it is a timer, it should be prefixed with "timer_". If it is a loop counter, it should be prefixed with "loop_". If it is an array, it should be prefixed with "arr_". If it is an array of sequences, it should be prefixed with "arrseq_". If it is a sequence, it should be prefixed with "seq_". If it is an unknown variable type, it should be prefixed with "var_". If it is known to be a variable only used as input to functions, it should have an "i_" between the prefix and the variable name. If it is known to be a variable only used to store outputs from functions, it should have an "o_" between the prefix and the variable name. If it is known to be both an input and output variable, i.e. something which is input into a function and modified during the function and then the modified value is returned, it should have an "io_" between the prefix and variable name. If it is unknown whether it is an input or output variable, there is nothing extra between the prefix and variable name. 

For creation of reaction mixes, if unspecified, you should add in the following order:
  - Water
  - Buffers
  - Beads
  - DNA
  - ATP
  - Enzymes.

If the substance type is unknown, then prioritise adding high volumes before low volumes. In the code, functions do not have the :ven:func` prefix. 

Microlab STARs have something called TADM; this is a pressure monitoring system of within pipetting steps, standing for Total Air Displacement Monitoring. The pressure data is saved in 10ms timepoints in a microsoft access database, along with the channel number, timestamp, and liquid class being used for the specific pipetting step that the TADM data was generated from. With the TADMCurveExport library, you can export the TADM data from the Microsoft Access Database file into an Excel file or a set of CSV files automatically. The TADM data can also be uploaded into the liquid class database to be associated with the specific liquid classes involved. You can set TADM tolerance bands within the liquid class database, which can cause the method to abort if TADM pressure data goes outside of the tolerance bands. The TADM data can also be used to analyze success of pipetting steps as incorrect/flawed pipetting (e.g. generating bubbles) will cause noticeable changes in the TADM data. 

By default, make timers have the "is stoppable" parameter set to True. 

Venus functions are denoted in the documentation by the ven:function:: prefix in the function definition and :ven:func: in the function references. 

General Steps
-------------------------------------------------------

.. ven:function:: Comment

  The comment function allows you to input a comment into the method. The comment can be chosen to be a Trace comment or not. If it is a Trace comment, it will be printed in the Trace during simulated or real runtime. Comment steps can also be chosen to be a specific colour in the editor, unlike most functions. The comment function doesn't have any input parameters, just a popup text box which you can input ASCII characters into. Pressing <Ctrl> + <Enter> will insert a new line. Pressing <Ctrl> + <Tab> will indent the text.

.. ven:function:: Assignment

  The assignment function allows you to specify a variable and assign a value to it. It does not have any input parameters but instead a box in which you can input the name of your variable and the value you wish to assign to it. The variable name can be a fresh name, or can be an existing one which you are reassigning a value to, or an element from an array. The value to be assigned can be a signed number, a string, an entry from a given list, another variable name, or an element from an array. If entering a string, the option to have it as a Translatable string is available, which can be translated into different languages using the Translation Support System provided by the Hamilton Company.

Scheduler Steps
-------------------------------------------------

Custom Dialog Steps
-------------------------------------------------

Favourites
-------------------------------------------------

Templates
-------------------------------------------------

ML_STAR
-------------------------------------------------

.. ven:function:: 1000ul Channel Tip Pick Up (Single Step)

  The 1000ul Channel Tip Pick Up (Single Step) function tells the Microlab STAR to pick up tips with the 1000ul channels. It asks for the input sequence where it can find the tips and whether the sequence counting is automatic (i.e. the starting position of the sequence increments when tips are picked up) or manual (no increments). It also allows you to select which channels are being used to pick up tips by assigning it a channel pattern, which can either be input directly in the dialog box or as a variable. It allows you to set custom error handling in response to specific errors that will potentially occur during the step, such as automatically testing the next spot in the sequence if no tips are found.

.. ven:function:: 1000ul Channel Aspirate (Single Step)

  The 1000ul Channel Aspirate (Single Step) function tells the Microlab STAR to use the specified channels to aspirate liquid from the specified sequence. It requires an input sequence telling it where to locate the desired liquid, as well as a boolean determining whether sequence counting is automatic (i.e. increments starting position after aspiration) or manual (i.e. no increment). It asks for a volume input, which can be a variable, and allows individual volumes to be set for each channel if desired. It also allows you to switch between three types of aspiration; normal, consecutive aspiration, and aspirate all. Aspirate all will attempt to aspirate a set volume, and if not enough is present it won't throw an error, it will simply take whatever is present. 
  For the pipetting cycle settings, you can pick what tip type you want to use from the dropdown, as well as what dispense mode you wish to use. The dispense mode selected will then act as a filter for what liquid classes are available in the next drop-down. You can select your desired liquid class from the dropdown, either as a string name from the liquid class database, or as a variable. 
  The aspirate position settings allow you to control the height in which the pipette will try aspirate, through a variety of different settings and options. The default is to use capacitive liquid level detection (cLLD) at the sensitivity defined by the labware definition (5). You can also change this sensitivity to be higher or lower. You can also turn on pressure liquid level detection (pLLD) which measures increases in pressure in the tip and uses that to determine liquid level height. You can set a submerge depth in mm, which tells the pipettes how far below the surface they are to go once they have identified the liquid height. If both pLLD and cLLD are on, you can set a maximum height difference, in which case if the values do not agree and are outside this set range, the method will abort. If neither pLLD or cLLD is on, you can set it to either aspirate a fixed height from the bottom of the labware, or to touch off the bottom of the labware and then rise a little bit.
  The channel settings available allow you to select which channels are being used in the aspiration, which can be either selected via tickboxes, input directly into the dialog box, or input as a variable. The advanced settings let you control whether or not the pipette tips follow the changing liquid height during aspiration and mixing, as well as letting you add mixing cycles to the pipetting step, of a specified volume, position, and number of cycles. The error section lets you set custom error handling responses to specific errors that will potentially occur during the process, and the responses are automatically triggered upon the error. 

.. ven:function:: 1000ul Channel Dispense (Single Step)

  The 1000ul Channel Dispense (Single Step) function tells the Microlab STAR to use the specified channels to aspirate liquid from the specified sequence. It requires an input sequence telling it which piece of labware to dispense the desired liquid into, as well as a boolean determining whether sequence counting is automatic (i.e. increments starting position after aspiration) or manual (i.e. no increment). It asks for a volume input, which can be a variable, and allows individual volumes to be set for each channel if desired. The dispense mode can be chosen from a dropdown, and the default value is 8, which means it will use the liquid class specified in the previous aspiration step.
  The dispense position settings allow you to control the height in which the pipette will try to dispense, through a variety of different settings and options. The default is to use capacitive liquid level detection (cLLD) at the sensitivity defined by the labware definition (5). You can also change this sensitivity to be higher or lower. You can also turn on pressure liquid level detection (pLLD) which measures increases in pressure in the tip and uses that to determine liquid level height. You can set a submerge depth in mm, which tells the pipettes how far below the surface they are to go once they have identified the liquid height. If both pLLD and cLLD are on, you can set a maximum height difference, in which case if the values do not agree and are outside this set range, the method will abort. If neither pLLD or cLLD is on, you can set it to either dispense a fixed height from the bottom of the labware, or to touch off the bottom of the labware and then rise a little bit. If the labware has been defined with the "Side Touch" characteristic, the channels can also do a side touch dispense, in which it will enter the well and then move the pipette tip to touch the side of the well at the specified height, allowing it to dispense on the side of the well, usually for the benefits of not making contact with the well bottom, or for the wicking effect. 
  The channel settings available allow you to select which channels are being used in the dispense, which can be either selected via tickboxes, input directly into the dialog box, or input as a variable. The advanced settings let you control whether or not the pipette tips follow the changing liquid height during aspiration and mixing, as well as letting you add mixing cycles to the pipetting step, of a specified volume, position, and number of cycles. The error section lets you set custom error handling responses to specific errors that will potentially occur during the process, and the responses are automatically triggered upon the error. 

.. ven:function:: 1000ul Channel Dispense on the Fly (Single Step)

  The 1000ul Channel Dispense on the Fly (Single Step) function tells the Microlab STAR to dispense liquid continuously from the specified channel whilst moving at a set speed and distance, usually defined as a complete plate. You input the destination sequence, as well as whether sequence counting is automatic (1) or manual (0). If sequence counting is automatic, the next time it interacts with the sequence, it will treat the next untouched posiiton in the sequence as the first position in the sequence. You can input your desired total dispense volume, either as a variable or raw value, and you can also specify different volumes for each channel, which can be variables, elements from an array, or raw values. The dispense on the fly mode can either be set to complete plate (0) or sequence order (1). You can set the dispense position with two parameters; the labware surface distance in mm (which can either be input as a variable or raw value), and the Start X-offset in mm (which can also be input as a variable or raw value). In the pipetting arm section you can input the X-speed during the dispense, in mm/s (which can be input as a variable or raw value). 
  The channel settings available allow you to select which channels are being used in the dispense, which can be either selected via tickboxes, input directly into the dialog box, or input as a variable. The advanced settings let you control whether the liquid class being used is the same as in the first aspiration of the cycle, and if not then it lets you pick a fresh liquid class. It also allows you to determine the X-acceleration distance before the first shoot in mm, the dispense direction (with 0 being serpentine and 1 being from the left only), as well as specifying any excluded labware positions. The error section lets you set custom error handling responses to specific errors that will potentially occur during the process, and the responses are automatically triggered upon the error. 

.. ven:function:: 1000ul Channel Tip Eject (Single Step)

  The 1000ul Channel Tip Eject (Single Step) function tells the Microlab STAR to eject tips from the specified channels. You input the eject destination, which is any piece of labware, but by default is (1) which corresponds to the default waste location on the Microlab STAR. If a separate eject destination is chosen, sequence counting can be turned to automatic (i.e. increment sequence after ejecting tips) or manual (no increment).
  The channel settings allow you to select which channels the tips are being ejected from, whcih can either be selected via tickboxes, input directly into the dialog box, or input as a variable. The error settings let you set custom error handling responses to specific errors that will potentially occur during the process, and the responses are automatically triggered upon the error.

.. ven:function:: 1000ul Channel Get Last Liquid Level (Single Step)

  The 1000ul Channel Get Last Liquid Level (Single Step) function returns the liquid level height detected during the most recently performed aspirate or dispense step with liquid level detection enabled. There is no dialog box that appears as there are no parameters to input. It returns three values; the channel number, the detected liquid level height in mm relative to the deck coordinates of the Microlab STAR, and the block data for each channel.

.. ven:function:: 1000ul Channel Aspirate 2nd Phase (Single Step)

  The 1000ul Channel Aspirate 2nd Phase (Single Step) function allows you to aspirate a second phase of liquid into a tip that already has liquid in it. You input a target sequence for it to aspirate from, and input whether sequence counting is automatic (1) or manual (0). If automatic, the next time it interacts with a sequence it will treat the first untouched well as the start of the sequence. You can input the volume in ul either as a variable or raw value, or can input individual volumes for each channel as variables, raw values, or array elements. You can set the aspiration mode to 0 (aspiration) or 2 (aspirate all). Aspirate all will remove all available liquid in the well up to the specified volume without throwing errors if there is too little liquid. 
  In the pipetting cycle settings you can input what tip type you are using and the dispense mode, which will then provide a filter for the liquid classes that are available for you to select to use, which are chosen from the liquid class database. You can also set the aspiration position. You can use capacitive liquid level detection (cLLD) to determine the liquid level height, at a variety of sensitivities, with 5 being the default (which means "set in the labware definition" for the specific piece of labware being interacted with). You can have pressure liquid level detection (pLLD) on instead of or as well as cLLD. This uses pressure changes in the tip to determine what the liquid level is. If using both pLLD and cLLD, you can input a max height difference in mm, which will cause an error if the detected height from the cLLD and pLLD differ by more than the set value. You also input a submerge depth in mm which determines how far below the detected liquid level the tip goes before beginning the aspiration. 
  The channel settings available allow you to select which channels are being used in the dispense, which can be either selected via tickboxes, input directly into the dialog box, or input as a variable. The advanced settings let you control the immersion depth for the aspiration in mm, and whether liquid following during aspiration is on (1) or off (0). The advanced settings also let you input the Z speed of Search Level, in mm/s, and the dispenser stream of Search Level, in ul/s. Lastly, the advanced settings let you control the dispense back parameters, allowing you to input a retract distance in mm and a dispense stream in ul/s. The error section lets you set custom error handling responses to specific errors that will potentially occur during the process, and the responses are automatically triggered upon the error. 

.. ven:function:: Initialize (Single Step)

  The Initialize (Single Step) function initializes the Microlab STAR. It is required to be called the first time the STAR is used after being turned on. It is sensible to put it at the beginning of every method. It can either always initialize (1) or only initialize for the first run when turned on (0). The error settings dialog allows you to input automatic responses to certain errors. 

.. ven:function:: Lock/Unlock Front Cover (Single Step)

  The Lock/Unlock Front Cover (Single Step) function locks or unlocks the protective cover of the Microlab STAR. It can either be set to 1 (locked) or 0 (unlocked). The error settings dialog allows you to input automatic responses to certain errors.

.. ven:function:: iSWAP Get Plate (Single Step)

  The iSWAP Get Plate (Single Step) function uses the iSWAP (if the instrument has one installed) to pick up a plate from a specified position, in preparation for either an iSWAP Move Plate or iSWAP Place Plate function to be called. You specify the sequence of the plate to be picked up, as well as the lid sequence if it has a lid. You specify whether sequence counting is automatic (1) or manual (0); usually it is manual, it is automatic if you plan on moving multiple plates which are in the same sequence. You can set the iSWAP grip parameters, which are the grip height in mm, measured from the top of the labware, and the grip mode - this can be gripping the labware on the small side (0; the default) or the long side (1). Most labware comes with data in the labware file as to what grip width is required and the opening width before access, but this function has the option to override that, in which case you can put in the grip width and opening width before access, both in mm. The movement can either be just to a carrier (0; default) or a complex movement (1). The transport mode can be set to 0 (plate only), 1 (lid only) or 2 (plate and lid). If complex movement is chosen, three more parameters have to be input: the retract distance in mm, the lift-up height in mm, and the labware orientation, which can either be 1, 2, 3 or 4, based on which of the cardinal directions the iSWAP is pickup up the labware from. 
  The advanced setting dialog allows you to set the iSWAP grip force (default 5, goes between 0 and 10), as well as the tolerance in mm, whether the grip is inverse (1) or normal (0), and whether collision control is on (1) or off (0). The error settings dialog allows you to program in automatic responses to specific errors. 

.. ven:function:: iSWAP Place Plate (Single Step)

  The iSWAP Place Plate (Single Step) function allows the iSWAP to move to a specified location and place down a plate if it is holding one. You input the target sequence which is the location you wish the iSWAP place the plate in, as well as the lid sequence if the plate has a lid. The movement can either be just to a carrier (0; default) or a complex movement (1). The transport mode can be set to 0 (plate only), 1 (lid only) or 2 (plate and lid). If complex movement is chosen, three more parameters have to be input: the retract distance in mm, the lift-up height in mm, and the labware orientation, which can either be 1, 2, 3 or 4, based on which of the cardinal directions the iSWAP is pickup up the labware from. You specify whether sequence counting is automatic (1) or manual (0); usually it is manual, it is automatic if you plan on placing multiple plates which are in the same sequence.
  The advanced option dialog allows you to determine whether collision control is on (1) or off (0). The error settings dialog allows you to program in automatic responses to specific errors. 

.. ven:function:: iSWAP Move Plate (Single Step)

  The iSWAP Move Plate (Single Step) function allows the iSWAP to move to a specified location. You input the target sequence which is the location you wish the iSWAP to be moved to. The advanced option dialog allows you to determine whether the labware is gripped on the small side (0) or long side (1), as well as whether collision control is on (1) or off (0). The error settings dialog allows you to program in automatic responses to specific errors. 

.. ven:function:: iSWAP Open Gripper (Single Step)

  The iSWAP Open Gripper (Single Step) function allows the iSWAP to open the gripper and release the plate without placing it down; usually to drop it into the operator's hands or to drop the plate from a slight height onto the carrier with the intention of causing the liquid inside it to be disturbed by the motion. You can control whether the transport mode is for the plate only (0), the lid only (1), or the plate and lid together (2). You also pick the plate sequence, and can pick the lid sequence if relevant. You can determine whether sequence counting is manual (0) or automatic (1); unless you are doing it to multiple plates then sequence counting should be manual. You can specify whether the labware is gripped on the small side (0) or the long side (1), as well as whether or not to overwrite the grip data from the labware definition. If you do, then you specify the grip opening width. The error settings dialog allows you to program in automatic responses to specific errors.

.. ven:function:: iSWAP Close Gripper (Single Step)

  The iSWAP Close Gripper (Single Step) function allows the iSWAP to close the gripper and hold the plate without picking it up. You can control whether the transport mode is for the plate only (0), the lid only (1), or the plate and lid together (2). You also pick the plate sequence, and can pick the lid sequence if relevant. You can determine whether sequence counting is manual (0) or automatic (1); unless you are doing it to multiple plates then sequence counting should be manual. You specify the grip height of the labware, which is the number of mm that the iSWAP is gripping below the top of the labware. By default it is 3mm. You can specify whether the labware is gripped on the small side (0) or the long side (1), as well as whether or not to overwrite the grip data from the labware definition. If you do, then you specify the grip opening width. The advanced dialog option allows you to specify the grip force being used on a scale of 0 to 10, with 0 being low and 10 being high. The default is 5. In the advanced dialog you also specify the grip tolerance in mm. The error settings dialog allows you to program in automatic responses to specific errors.

.. ven:function:: iSWAP Get First Plate Position (Single Step)

  The documentation for this function has not yet been written.

.. ven:function:: Wait for TADM Upload (Single Step)

  The Wait for TADM Upload (Single Step) function forces the method to wait until the TADM data for specified pipetting tool (either the 1000ul channels (0), the 5ml channels (1), or the 96 head (2)) has been uploaded to a microsoft access database. 

Microlab STAR Smart Steps
-------------------------------------------------
