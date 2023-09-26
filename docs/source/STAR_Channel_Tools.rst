STAR_Channel_Tools - unfinished

==================================

https://github.com/theonetruenerd/VenusPackages/blob/main/STAR_Channel_Tools.pkg

The STAR_Channel_Tools submethod library adds a variety of functions which are related to the use of the 8 channels. The following functions are added:

  - :py:func:`CHAN_ACCESS_Sort1Sequence`
  - :py:func:`CHAN_ACCESS_Sort1Sequence1Array`
  - :py:func:`CHAN_ACCESS_Sort1Sequence2Arrays`
  - :py:func:`CHAN_ACCESS_Sort2Sequences`
  - :py:func:`CHAN_ACCESS_Sort2Sequences1Array`
  - :py:func:`CHAN_ACCESS_Sort2Sequences2Arrays`
  - :py:func:`LIQUID_LEVEL_GetLiquidLevelHeight`
  - :py:func:`LIQUID_LEVEL_MeasureLiquidMulti`
  - :py:func:`LIQUID_LEVEL_MeasureLiquidSingle`
  - :py:func:`LIQUID_LEVEL_ReturnVolumesFromLiquidLevel`
  - :py:func:`MOVE_ChannelsToSequencePosition`
  - :py:func:`MOVE_ChannelsToSequencePosition_5mL`
  - :py:func:`MOVE_CheckPlateWithTwoChannels`
  - :py:func:`MOVE_InitDispenseDrive`
  - :py:func:`MOVE_InitDispenseDrive_5mL`
  - :py:func:`PLATE_STACK_CountPlateStacks`
  - :py:func:`QUERY_GetChannelPosition`
  - :py:func:`QUERY_GetChannelPosition_5mL`
  - :py:func:`QUERY_GetTipPresentState`
  - :py:func:`QUERY_GetTipPresentState_5mL`
  - :py:func:`QUERY_GetTipVolume`
  - :py:func:`QUERY_GetTIpVolume_5mL`
  - :py:func:`SPLIT_WELLS_AddContainersToWell`
  - :py:func:`SPLIT_WELLS_RemoveContainers`
  - :py:func:`TRAVEL_LANES_MoveChannelsToTravelLanes`
  - :py:func:`TRAVEL_LANES_MoveChannelsToTravelLanes_5mL`
  - :py:func:`TRAVEL_LANES_MoveChannelsToYPosition`
  - :py:func:`TRAVEL_LANES_MoveChannelsToYPosition_5mL`
  - :py:func:`TRAVEL_LANES_MoveChannelsWithTravelLanes`
  - :py:func:`TRAVEL_LANES_MoveChannelsWithTravelLanes_5mL`
  - :py:func:`TRAVEL_LANES_SingleSource_ChannelDisplacement`
  - :py:func:`TRAVEL_LANES_SingleSource_ChannelDisplacement_5mL`

..  py:function:: CHAN_ACCESS_Sort1Sequence(device ML_STAR, sequence io_Sequence_to_Sort, variable i_Channel_Type, boolean i_Sort_by_Labware, boolean i_Sort_by_XY, boolean i_Sort_for_Channel_Raster, variable i_Max_Channel, sequence o_Sorted_Sequence, variable o_Channel_Pattern)

  This submethod takes an input sequence and sorts it based on the input parameters of labware, position, and raster. Once sorted, the submethod will choose a position that the current channel can access up to the maximum. If the current channel cannot access the position, it will skip it and move to the next available position. If the current cannot access any more positions, that channel will be skipped. Make sure the channel use setting is set to "All Sequence Positions" in the pipettting step, otherwise the sequence and channel pattern will not line up.

  :params ML_STAR: The ML_STAR itself, which will be the only option in the dropdown. 
  :params io_Sequence_to_Sort: The input sequence to be sorted.
  :params i_Channel_Type: The channel type associated with the pipetting step (1mL, 5mL, labware handler). 0 = 1mL, 1 = 5mL, 2 = Labware handler.
  :params i_Sort_by_Labware: A boolean determining whether the sequence is to be sorted by labware in ascending order
  :params i_Sort_by_XY: A boolean determining whether the sequence is to be sorted by position (X ascending, Y descending)
  :params i_Sort_for_Channel_Raster: A boolean determining whether the next position will be at least the raster distance unless no other positions are available
  :params i_Max_Channel: The maximum channel that you want to be used from 1 to 16. 0 turns this option off and the maximum number of channels will be used. 
  :params o_Sorted_Sequence: The outputted sorted sequence for the pipetting step
  :params o_Channel_Pattern: The outputted channel pattern for the pipetting step
  :type ML_STAR: Device
  :type io_Sequence_to_Sort: Sequence
  :type i_Channel_Type: Variable
  :type i_Sort_by_Labware: Boolean
  :type i_Sort_by_XY: Boolean
  :type i_Sort_for_Channel_Raster: Boolean
  :type i_Max_Channel: Variable
  :type o_Sorted_Sequence: Sequence
  :type o_Channel_Pattern: Variable
  :return: The number of sequence positions remaining in the sequence
  :rtype: Variable

.. py:function:: CHAN_ACCESS_Sort1Sequence1Array(device ML_STAR, sequence io_Sequence_to_Sort, array io_Array_of_Variables, variable i_Channel_Type, boolean i_Sort_by_Labware, boolean i_Sort_by_XY, boolean i_Sort_for_Channel_Raster, variable i_Max_Channel, sequence o_Sorted_Sequence, array o_Sorted_Array, variable o_Channel_Pattern)

  This submethod takes in input sequence and sorts it by the conditions given below.  After sorting, the submethod will choose a position that the current channel can access up to the maximum.  If the current channel cannot access the position, it wil skip it and move to the next available position.  If the current channel cannot access any more positions, that channel will be skipped.  The array will be sorted with the sequence.  The array and the sequence must be the same size. Make sure the channel use setting is set to "All sequence positions" otherwise the sequence and channel pattern will not line up.

  :params ML_STAR: The ML_STAR itself, which will be the only option in the dropdown.
  :params io_Sequence_to_Sort: The input sequence to be sorted.
  :params io_Array_of_Variables: The array to be sorted with the sequence.
  :params i_Channel_Type: The channel type associated with the pipetting step (1mL, 5mL, labware handler). 0 = 1mL, 1 = 5mL, 2 = Labware handler.
  :params i_Sort_by_Labware: A boolean determining whether the sequence is to be sorted by labware in ascending order
  :params i_Sort_by_XY: A boolean determining whether the sequence is to be sorted by position (X ascending, Y descending)
  :params i_Sort_for_Channel_Raster: A boolean determining whether the next position will be at least the raster distance unless no other positions are available
  :params i_Max_Channel: The maximum channel that you want to be used from 1 to 16. 0 turns this option off and the maximum number of channels will be used. 
  :params o_Sorted_Sequence: The outputted sorted sequence for the pipetting step
  :params o_Sorted_Array: The outputted sorted array which matches the sequence
  :params o_Channel_Pattern: The outputted channel pattern for the pipetting step
  :type ML_STAR: Device
  :type io_Sequence_to_Sort: Sequence
  :params io_Array_of_Variables: Array
  :type i_Channel_Type: Variable
  :type i_Sort_by_Labware: Boolean
  :type i_Sort_by_XY: Boolean
  :type i_Sort_for_Channel_Raster: Boolean
  :type i_Max_Channel: Variable
  :type o_Sorted_Sequence: Sequence
  :type o_Sorted_Array: Array
  :type o_Channel_Pattern: Variable
  :return: The number of sequence positions remaining in the sequence
  :rtype: Variable

.. py:function: LIQUID_LEVEL_GetLiquidLevelHeight(device ML_STAR, variable i_str_LiquidLevelReturn, sequence i_seq_Labware, variable i_int_Channel, variable o_flt_LiquidHeight)

  This function will return the liquid level height relative to the container bottem.

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown.
  :params i_str_LiquidLevelReturn: The return value of the liquid level detect from the pipetting step. 
  :params i_seq_Labware: The input sequence from which the height is to be determined
  :params i_int_Channel: The channel which will be used to determine the liquid level height
  :params o_flt_LiquidHeight: The detected liquid level height
  :type ML_STAR: Device
  :type i_str_LiquidLevelReturn: Variable
  :type i_seq_Labware: Sequence
  :type i_int_Channel: Integer
  :type o_flt_LiquidHeight: Float
  :return: None
  :rtype: N/A
