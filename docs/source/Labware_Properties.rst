Labware Properties
=========================================

https://github.com/theonetruenerd/VenusPackages/blob/main/Labware_Properties.pkg

The labware properties library adds a variety of functions which assist with obtaining the physical data of the labware, as well as things like its ID. The functions it adds are:

  - :py:func:`GetCarrierIDandSiteID_FromLabID`
  - :py:func:`Get_ContainerBaseOffset`
  - :py:func:`Get_ContainerBaseThickness`
  - :py:func:`Get_Height`
  - :py:func:`Get_NameAndFileName`
  - :py:func:`Get_NumberOfColumns`
  - :py:func:`Get_NumberOfRows`
  - :py:func:`Get_RackBaseToCoverBase`
  - :py:func:`Get_StackHeight`
  - :py:func:`Get_XYZ_deckPosition`
  - :py:func:`Get_XY_dimensions`

.. py:function:: GetCarrierIDandSiteID_FromLabID(device io_instrument, variable i_labware_ID, variable o_carrier_ID, variable o_site_ID)

  This function takes outputs the carrier ID and site ID which are associated with the given labware ID. It works on both the Nimbus and the STAR.

  :params io_instrument: The instrument being used. Will either be ML_STAR or Nimbus.
  :params i_labware_ID: The labware ID from which the other IDs are being pulled.
  :params o_carrier_ID: The carrier ID associated with the given labware ID.
  :params o_site_ID: The site ID associated with the given labware ID.
  :type io_instrument: Device
  :type i_labware_ID: Variable
  :type o_carrier_ID: Variable
  :type o_site_ID: Variable
  :return: A boolean determining whether the labware ID exists (1) or not (0)
  :rtype: Boolean

.. py:function:: Get_ContainerBaseOFfset(device io_instrument, sequence i_sequenceLabware, variable i_sequencePosition, variable o_ContainerBaseOffset)

  This function outputs the distance from the rack base to the container base for the labware at the given sequence position.

  :params io_instrument: The instrument being used. Will either be ML_STAR or Nimbus.
  :params i_sequenceLabware: The sequence associated with the labware being checked.
  :params i_sequencePosition: The position ID or index of the sequence being checked. Can be either int or str. An input of 0 will auto-select the first position.
  :params o_ContainerBaseOFfset: The distance from the rack base to the container base at the specified position
  :type io_instrument: Device
  :type i_sequenceLabware: Sequence
  :type i_sequencePosition: Variable
  :type o_ContainerBaseOFfset: Variable
  :return: None
  :rtype: N/A

.. py:function:: Get_ContainerBaseThickness(device io_instrument, sequence i_sequenceLabware, variable o_containerBaseThickness)

  This function outputs the base thickness of the container at the first position of a given sequence.

  :params io_instrument: The instrument being used. Will be either ML_STAR or Nimbus.
  :params i_sequenceLabware: The sequence asspciated with the labware being checked.
  :params o_containerBaseThickness: The thickness of the base of the container being checked.
  :type io_instrument: Device
  :type i_sequenceLabware: Sequence
  :type o_containerBaseThickness: Variable
  :return: None
  :rtype: N/A

.. py:function:: Get_Height(device io_instrument, sequence i_sequenceLabware, variable o_labwareHeight)

  This function outputs the height of the labware at the first position of a given sequence. This value is only the labware height, not the absolute Z position.

  :params io_instrument: The instrument being used. Will be either ML_STAR or Nimbus.
  :params i_sequenceLabware: The sequence associated with the labware being checked.
  :params o_labwareHeight: The height of the labware being checked.
  :type io_instrument: Device
  :type i_sequenceLabware: Sequence
  :type o_labwareHeight: Variable
  :return: None  
  :rtype: N/A

.. py:function:: Get_NameAndFileName(device io_instrument, sequence i_sequenceLabware, variable o_viewName, variable o_fileName)

  This function outputs the labware view name and the file name associated with it (with path)

  :params io_instrument: The instrument being used. Will be either ML_STAR or Nimbus.
  :params i_sequenceLabware: The sequence associated with the labware of interest.
  :params o_viewName: The view name of the labware being checked.
  :params o_fileName: The file name (with path) of the labware being checked.
  :return: None
  :rtype: N/A

.. py:function:: Get_NumberOfColumns(device io_instrument, sequence i_sequenceLabware, variable o_labwareColumns)

  This function outputs the number of columns defined in the labware from the first position of a given sequence.

  :params io_instrument: The instrument being used. Will be either ML_STAR or Nimbus.
  :params i_sequenceLabware: The sequence associated with the labware of interest.
  :params o_labwareColumns: The number of columns defined in the labware being checked.
  :type io_instrument: Device
  :type i_sequenceLabware: Sequence
  :type o_labwareColumns: Variable  
  :return: None
  :rtype: N/A

.. py:function:: Get_NumberOfRows(device io_instrument, sequence i_sequenceLabware, variable o_labwareColumns)

  This function outputs the number of rows defined in the labware at the first position of a given sequence. The variable and function description both say columns; this is incorrect.

  :params io_instrument: The instrument being used. Will be either ML_STAR or Nimbus.
  :params i_sequenceLabware: The sequence associated with the labware being checked.
  :params o_labwareColumns: The number of rows defined in the labware being checked.
  :type io_instrument: Device
  :type i_sequenceLabware: Sequence
  :type o_labwareColumns: Variable
  :return: None
  :rtype: N/A

.. py:function:: Get_RackBaseToCoverBase(device io_instrument, sequence i_sequenceLabware, variable o_RackBaseToCoverBase_Height)

  This function outputs the height from the base of the rack to the base of the cover/lid of the labware at the first position of a given sequence.

  :params io_instrument: The instrument being used. Will be either ML_STAR or Nimbus.
  :params i_sequenceLabware: The sequence associated with the labware being checked.
  :params o_RackBaseToCoverBase_Height: The distance from the rack base to the cover base.
  :type io_instrument: Device
  :type i_sequenceLabware: Sequence
  :type o_RackBaseToCoverBase_Height: Variable
  :return: None
  :rtype: N/A

.. py:function:: Get_StackHeight(device io_instrument, sequence i_sequenceLabware, variable o_labwareStackHeight)

  This function outputs the stack height of the specified labware at the first position of a given sequence.

  :params io_instrument: The instrument being used. Will be either ML_STAR or Nimbus.
  :params i_sequenceLabware: The sequence associated with the labware being checked.
  :params o_labwareStackHeight: The stack height of the labware being checked, or the covered stack height if the labware is lidded.
  :type io_instrument: Device
  :type i_sequenceLabware: Sequence
  :type o_labwareStackHeight: Variable
  :return: None
  :rtype: N/A

.. py:function:: Get_XYZ_deckPosition(device io_instrument, sequence i_sequenceLabware, variable o_labware_deckPosition_X, variable o_labware_deckPosition_Y, variable o_labware_deckPosition_Z)

  This function returns the X, Y and Z coordinates of the upper left well of the specified labware at the first position of a given sequence. The description of this function says it only does the X and Y coordinates, this is incorrect.

  :params io_instrument: The instrument being used. Will be either ML_STAR or Nimbus.
  :params i_sequenceLabware: The sequence associated with the labware being checked.
  :params o_labware_deckPosition_X: The X coordinate of the labware on the deck.
  :params o_labware_deckPosition_Y: The Y coordinate of the labware on the deck.
  :params o_labware_deckPosition_Z: The Z coordinate of the labware on the deck.
  :type io_instrument: Device
  :type i_sequenceLabware: Sequence
  :type o_labware_deckPosition_X: Variable
  :type o_labware_deckPosition_Y: Variable
  :type o_labware_deckPosition_Z: Variable
  :return: None
  :rtype: N/A

.. py:function:: Get_XY_dimensions(device io_instrument, sequence i_sequenceLabware, variable o_X_width, variable o_Y_depth)

  This function outputs the X (width) and Y (depth) dimensions of the specified labware at the first position of a given sequence.

  :params io_instrument: The instrument being used. Will be either ML_STAR or Nimbus.
  :params i_sequenceLabware: The sequence associated with the labware being checked.
  :params o_X_width: The width of the labware being checked.
  :params o_Y_depth: The depth of the labware being checked.
  :type io_instrument: Device
  :type i_sequenceLabware: Sequence
  :type o_X_width: Variable
  :type o_Y_depth: Variable
  :return: None
  :rtype: N/A
