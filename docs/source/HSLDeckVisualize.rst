HSLDeckVisualize
======================================

https://github.com/theonetruenerd/VenusPackages/blob/main/HSLDeckVisualize.pkg

The HSLDeckVisualize library adds functions which will update the layout shown in the run control to account for manually performed actions or cause specific effects to occur. The functions it adds are:

- :ven:func:`UpdateUsedPositions`
- :ven:func:`UpdateUsedLabware`
- :ven:func:`UpdateLoadedLabware`

.. ven:function:: UpdateUsedPositions(device dev, sequence positions, variable action, variable description)

  This function updates the list of used positions and updates the view.

  :params dev: The instrument for which the associated deck view will be updated. ML_STAR should be the only option visible in the dropdown.
  :params positions: The sequence of labware and positions IDs to be updated.
  :params action: The action to be performed on the specified positions. The same action will be performed for all positions. Action can be an integer from 0-6, with the values each representing a different event. 0 = Position is selected, 1 = Processing, 2 = Reserved, 3 = Error, 4 = Processed, 5 = Reset action state to none, 6 = Position selected and flashing.
  :params description: The description displayed in the first section of the status bar in the deck view. 
  :type dev: Device
  :type positions: Sequence
  :type action: Variable
  :type description: Variable
  :return: None
  :rtype: N/A

.. ven:function:: UpdateUsedLabware(device dev, array labware, array action, variable description)

  This function updates the list of used labware and updates the view accordingly. The labware and action arrays must be the same size.

  :params dev: The instrument for which the associated deck view will be updated. ML_STAR should be the only option visible in the dropdown.
  :params labware: The array of labware IDs for updating
  :params action: The array of actions which will be applied to the associated labware at the same index in the labware array. Action can be an integer from 0-6, with the values each representing a different event. 0 = Position is seleccted, 1 = Processing, 2 = Reserved, 3 = Error, 4 = Processed, 5 = Reset action state to none, 6 = Position selected and flashing.
  :params description: The description displayed in the first section of the status bar in the deck view. 
  :type dev: Device
  :type labware: Array
  :type action: Array
  :type description: Variable
  :return: None
  :rtype: N/A

.. ven:function:: UpdateLoadedLabware(device dev, array labware, array state, variable description)

  This function updates the list of loaded labware and updates the view accordingly. The labware and action arrays must be the same size.

  :params dev: The instrument for which the associated deck view will be updated. ML_STAR should be the only option visible in the dropdown.
  :params labware: The array of labware IDs for updating
  :params state: The array of load state which will be applied to the associated labware at the same index in the labware array. State can be an integer from 0-5, with the values each representing a different state. 0 = unload the labware and make not visible, 1 = load the labware, 2 = preparing to unload, 3 = preparing to load, 4 = labware will flash, 5 = labware will flash
  :params description: The description displayed in the first section of the status bar in the deck view. 
  :type dev: Device
  :type labware: Array
  :type state: Array
  :type description: Variable
  :return: None
  :rtype: N/A
