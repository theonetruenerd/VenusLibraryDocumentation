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

Venus is a drag-and-drop wrapper for a separate coding language called HSL. When coding a method in venus, all the available functions (core and any from imported libraries) are listed on the left hand side of the screen in a tree view. When you want to add a step to your method, you drag and drop that function from the left hand side and drop it wherever you want it to be in your method. This will then open a dialog box which allows you to input your desired parameters. The method is saved as a .med file, which can be run through a software called HxRunControl.exe. The run control software can run simulations of the code as well as the code on an actual robot. In the run control software window, you can see the deck layout dynamically changing, an open view of the method showing what step you are on, and a trace file which is a type of log which displays the data from every step that is occuring and is timestamped for each step. The trace file is saved to the Log Files folder within the main Hamilton folder in Program Files (x86). Method files (.med) can compile into HSL files (.hsl) which can also be edited and run through the run control software. Instead of being drag-and-drop, HSL is a more standard coding language, with C++ like syntax. HSL files cannot be converted into .med files; as such, it is usually recommended to insert snippets of HSL code into the main .med file rather than coding in HSL itself, or to only use HSL for creation of fresh libraries. 

Libraries are groups of functions which reside in the library folder within the main Hamilton folder. They can be imported into specific methods, at which point the functions associated with that library will appear in the function tree on the left hand side of the method editor. Libraries can either be written in HSL (and are thus .hsl files) or can be "sub-method libraries", which is a series of steps coded in Venus that are stored in a way that works like a function. Sub-method libraries are .smt files. You can have submethods in a normal method file, and it is often encouraged so that your code is "parcelled" into blocks which contain the main blocks of your method. These submethods are just like the normal method but reside in a separate tab in the method editor. 

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

  This function's documentation has not yet been written

.. ven:function:: 1000ul Channel Tip Eject (Single Step)

  The 1000ul Channel Tip Eject (Single Step) function tells the Microlab STAR to eject tips from the specified channels. You input the eject destination, which is any piece of labware, but by default is (1) which corresponds to the default waste location on the Microlab STAR. If a separate eject destination is chosen, sequence counting can be turned to automatic (i.e. increment sequence after ejecting tips) or manual (no increment).
  The channel settings allow you to select which channels the tips are being ejected from, whcih can either be selected via tickboxes, input directly into the dialog box, or input as a variable. The error settings let you set custom error handling responses to specific errors that will potentially occur during the process, and the responses are automatically triggered upon the error.

Microlab STAR Smart Steps
-------------------------------------------------
