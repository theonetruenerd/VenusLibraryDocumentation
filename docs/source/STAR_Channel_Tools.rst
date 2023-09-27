STAR_Channel_Tools
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
  :params io_Array_of_Variables: The array to be sorted with the sequence. Used positions will be removed from the array.
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
  :type io_Array_of_Variables: Array
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

.. py:function:: CHAN_ACCESS_Sort1Sequence2Arrays(device ML_STAR, sequence io_Sequence_to_Sort, array io_Array_of_Variables, array io_Array_of_Variables2, variable i_Channel_Type, boolean i_Sort_by_Labware, boolean i_Sort_by_XY, boolean i_Sort_for_Channel_Raster, variable i_Max_Channel, sequence o_Sorted_Sequence, array o_Sorted_Array, array o_Sorted_Array2, variable o_Channel_Pattern)

  This submethod takes in input sequence and sorts it by the conditions given below.  After sorting, the submethod will choose a position that the current channel can access up to the maximum.  If the current channel cannot access the position, it wil skip it and move to the next available position.  If the current channel cannot access any more positions, that channel will be skipped.  The arrays will be sorted with the sequence.  The arrays and the sequence must be the same size. Make sure the channel use setting is set to "All sequence positions" otherwise the sequence and channel pattern will not line up.

  :params ML_STAR: The ML_STAR itself, which will be the only option in the dropdown.
  :params io_Sequence_to_Sort: The input sequence to be sorted.
  :params io_Array_of_Variables: The first array to be sorted with the sequence. Used positions will be removed from the array.
  :params io_Array_of_Variables2: The second array to be sorted with the sequence. Used positions will be removed from the array.
  :params i_Channel_Type: The channel type associated with the pipetting step (1mL, 5mL, labware handler). 0 = 1mL, 1 = 5mL, 2 = Labware handler.
  :params i_Sort_by_Labware: A boolean determining whether the sequence is to be sorted by labware in ascending order
  :params i_Sort_by_XY: A boolean determining whether the sequence is to be sorted by position (X ascending, Y descending)
  :params i_Sort_for_Channel_Raster: A boolean determining whether the next position will be at least the raster distance unless no other positions are available
  :params i_Max_Channel: The maximum channel that you want to be used from 1 to 16. 0 turns this option off and the maximum number of channels will be used. 
  :params o_Sorted_Sequence: The outputted sorted sequence for the pipetting step
  :params o_Sorted_Array: The outputted sorted first array which matches the sequence
  :params o_Sorted_Array2: The outputted sorted second array which matches the sequence
  :params o_Channel_Pattern: The outputted channel pattern for the pipetting step
  :type ML_STAR: Device
  :type io_Sequence_to_Sort: Sequence
  :type io_Array_of_Variables: Array
  :type io_Array_of_Variables2: Array
  :type i_Channel_Type: Variable
  :type i_Sort_by_Labware: Boolean
  :type i_Sort_by_XY: Boolean
  :type i_Sort_for_Channel_Raster: Boolean
  :type i_Max_Channel: Variable
  :type o_Sorted_Sequence: Sequence
  :type o_Sorted_Array: Array
  :type o_Sorted_Array2: Array
  :type o_Channel_Pattern: Variable
  :return: The number of sequence positions remaining in the sequence
  :rtype: Variable

..  py:function:: CHAN_ACCESS_Sort2Sequences(device ML_STAR, sequence io_Sequence_to_Sort, sequence io_Sequence_to_Sort2, variable i_Channel_Type, boolean i_Sort_by_Labware, boolean i_Sort_by_XY, boolean i_Sort_for_Channel_Raster, variable i_Max_Channel, sequence o_Sorted_Sequence, sequence o_Sorted_Sequence2, variable o_Channel_Pattern)

  This sub method takes the in input sequences and sorts them by the conditions given below.  After sorting, the sub will choose a position that the current channel can access in both sequence positions up to the maximum.  If the current channel cannot access the positions, it wil skip it and move to the next available position.  If the current channel cannot access any more positions, that channel will be skipped. Make sure the channel use setting is set to "All sequence positions" otherwise the sequence and channel pattern will not line up. The first sequence is the driving sequence and the second sequence will be adjusted by the first sort.
 
  :params ML_STAR: The ML_STAR itself, which will be the only option in the dropdown. 
  :params io_Sequence_to_Sort: The first input sequence to be sorted.
  :params io_Sequence_to_Sort2: The second input sequence to be sorted.
  :params i_Channel_Type: The channel type associated with the pipetting step (1mL, 5mL, labware handler). 0 = 1mL, 1 = 5mL, 2 = Labware handler.
  :params i_Sort_by_Labware: A boolean determining whether the sequence is to be sorted by labware in ascending order
  :params i_Sort_by_XY: A boolean determining whether the sequence is to be sorted by position (X ascending, Y descending)
  :params i_Sort_for_Channel_Raster: A boolean determining whether the next position will be at least the raster distance unless no other positions are available
  :params i_Max_Channel: The maximum channel that you want to be used from 1 to 16. 0 turns this option off and the maximum number of channels will be used. 
  :params o_Sorted_Sequence: The outputted second sorted sequence for the pipetting step
  :params o_Sorted_Sequence2: The outputted second sorted sequence for the pipetting step
  :params o_Channel_Pattern: The outputted channel pattern for the pipetting step
  :type ML_STAR: Device
  :type io_Sequence_to_Sort: Sequence
  :type io_Sequence_to_Sort2: Sequence
  :type i_Channel_Type: Variable
  :type i_Sort_by_Labware: Boolean
  :type i_Sort_by_XY: Boolean
  :type i_Sort_for_Channel_Raster: Boolean
  :type i_Max_Channel: Variable
  :type o_Sorted_Sequence: Sequence
  :type o_Sorted_Sequence2: Sequence  
  :type o_Channel_Pattern: Variable
  :return: The number of sequence positions remaining in the sequence
  :rtype: Variable

.. py:function:: CHAN_ACCESS_Sort2Sequences1Array(device ML_STAR, sequence io_Sequence_to_Sort, sequence io_Sequence_to_Sort2, array io_Array_of_Variables, variable i_Channel_Type, boolean i_Sort_by_Labware, boolean i_Sort_by_XY, boolean i_Sort_for_Channel_Raster, variable i_Max_Channel, sequence o_Sorted_Sequence, sequence o_Sorted_Sequence2, array o_Sorted_Array, variable o_Channel_Pattern)

  This sub method takes the in input sequences and sorts them by the conditions given below.  After sorting, the sub will choose a position that the current channel can access in both sequence positions up to the maximum.  If the current channel cannot access the positions, it wil skip it and move to the next available position.  If the current channel cannot access any more positions, that channel will be skipped. Make sure the channel use setting is set to "All sequence positions" otherwise the sequence and channel pattern will not line up. The first sequence is the driving sequence and the second sequence will be adjusted by the first sort.
 
  :params ML_STAR: The ML_STAR itself, which will be the only option in the dropdown. 
  :params io_Sequence_to_Sort: The first input sequence to be sorted.
  :params io_Sequence_to_Sort2: The second input sequence to be sorted.
  :params i_Channel_Type: The channel type associated with the pipetting step (1mL, 5mL, labware handler). 0 = 1mL, 1 = 5mL, 2 = Labware handler.
  :params i_Sort_by_Labware: A boolean determining whether the sequence is to be sorted by labware in ascending order
  :params i_Sort_by_XY: A boolean determining whether the sequence is to be sorted by position (X ascending, Y descending)
  :params i_Sort_for_Channel_Raster: A boolean determining whether the next position will be at least the raster distance unless no other positions are available
  :params i_Max_Channel: The maximum channel that you want to be used from 1 to 16. 0 turns this option off and the maximum number of channels will be used. 
  :params o_Sorted_Sequence: The outputted second sorted sequence for the pipetting step
  :params o_Sorted_Sequence2: The outputted second sorted sequence for the pipetting step
  :params o_Sorted_Array: The sorted array. The array will be the size of the maximum channel.
  :params o_Channel_Pattern: The outputted channel pattern for the pipetting step
  :type ML_STAR: Device
  :type io_Sequence_to_Sort: Sequence
  :type io_Sequence_to_Sort2: Sequence
  :type i_Channel_Type: Variable
  :type i_Sort_by_Labware: Boolean
  :type i_Sort_by_XY: Boolean
  :type i_Sort_for_Channel_Raster: Boolean
  :type i_Max_Channel: Variable
  :type o_Sorted_Sequence: Sequence
  :type o_Sorted_Sequence2: Sequence  
  :type o_Sorted_Array: Array
  :type o_Channel_Pattern: Variable
  :return: The number of sequence positions remaining in the sequence
  :rtype: Variable

.. py:function:: CHAN_ACCESS_Sort2Sequences2Arrays(device ML_STAR, sequence io_Sequence_to_Sort, sequence io_Sequence_to_Sort2, array io_Array_of_Variables, array io_Array_of_Variables2, variable i_Channel_Type, boolean i_Sort_by_Labware, boolean i_Sort_by_XY, boolean i_Sort_for_Channel_Raster, variable i_Max_Channel, sequence o_Sorted_Sequence, sequence o_Sorted_Sequence2, array o_Sorted_Array, array o_Sorted_Array2, variable o_Channel_Pattern)

  This sub method takes the in input sequences and sorts them by the conditions given below.  After sorting, the sub will choose a position that the current channel can access in both sequence positions up to the maximum.  If the current channel cannot access the positions, it wil skip it and move to the next available position.  If the current channel cannot access any more positions, that channel will be skipped. Make sure the channel use setting is set to "All sequence positions" otherwise the sequence and channel pattern will not line up. The first sequence is the driving sequence and the second sequence will be adjusted by the first sort.
 
  :params ML_STAR: The ML_STAR itself, which will be the only option in the dropdown. 
  :params io_Sequence_to_Sort: The first input sequence to be sorted. This positions removed will be removed from this sequence.
  :params io_Sequence_to_Sort2: The second input sequence to be sorted. The positions used will be removed from this sequence.
  :params io_Array_of_Variables: The input array of variables which will be sorted with the first sequence. The positions used will be removed from the array.
  :params io_Array_of_Variables2: The input array of variables which will be sorted with the second sequence. The positions used will be removed from the array.
  :params i_Channel_Type: The channel type associated with the pipetting step (1mL, 5mL, labware handler). 0 = 1mL, 1 = 5mL, 2 = Labware handler.
  :params i_Sort_by_Labware: A boolean determining whether the sequence is to be sorted by labware in ascending order
  :params i_Sort_by_XY: A boolean determining whether the sequence is to be sorted by position (X ascending, Y descending)
  :params i_Sort_for_Channel_Raster: A boolean determining whether the next position will be at least the raster distance unless no other positions are available
  :params i_Max_Channel: The maximum channel that you want to be used from 1 to 16. 0 turns this option off and the maximum number of channels will be used. 
  :params o_Sorted_Sequence: The outputted second sorted sequence for the pipetting step
  :params o_Sorted_Sequence2: The outputted second sorted sequence for the pipetting step
  :params o_Sorted_Array: The sorted array. The array will be the size of the maximum channel.
  :params o_Sorted_Array2: The second sorted array. The array will be the size of the maximum channel.
  :params o_Channel_Pattern: The outputted channel pattern for the pipetting step
  :type ML_STAR: Device
  :type io_Sequence_to_Sort: Sequence
  :type io_Sequence_to_Sort2: Sequence
  :type i_Channel_Type: Variable
  :type i_Sort_by_Labware: Boolean
  :type i_Sort_by_XY: Boolean
  :type i_Sort_for_Channel_Raster: Boolean
  :type i_Max_Channel: Variable
  :type o_Sorted_Sequence: Sequence
  :type o_Sorted_Sequence2: Sequence  
  :type o_Sorted_Array: Array
  :type o_Sorted_Array2: Array
  :type o_Channel_Pattern: Variable
  :return: The number of sequence positions remaining in the sequence
  :rtype: Variable

.. py:function:: LIQUID_LEVEL_GetLiquidLevelHeight(device ML_STAR, variable i_str_LiquidLevelReturn, sequence i_seq_Labware, variable i_int_Channel, variable o_flt_LiquidHeight)

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

.. py:function:: LIQUID_LEVEL_MeasureLiquidMulti(device ML_STAR, array i_arrseq_FullReservoirSequences, sequence i_seq_TipsToUse, sequence i_seq_TipWaste, variable i_str_TipCounter, variable i_int_LLD_Sensitivity, variable i_bool_ConvertTouL, array o_arr_VolumesMeasured)

  This function will pick up the desired tips and will measure the liquid level at the center most well of the desired reservoirs and will return the volumes in uL. Ensure the sequence used for the reservoir contains the FULL number of positions of the reservoir, otherwise volume estimation will be incomplete! The tip types supported are: 50uL Filter, 50uL, 300uL Filter, 300uL, 1000uL Filter, and 1000uL.

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown.
  :params i_arrseq_FullReservoirSequences: The array of full reservoir sequences to be checked.
  :params i_seq_TipsToUse: The sequence of the tips to be used to measure the liquid level.
  :params i_seq_TipWaste: The sequence of the waste used to eject the tips.
  :params i_str_TipCounter: The tip counter to be used for the tips on pickup. Place "" if no tip counter will be used.
  :params i_int_LLD_Sensitivity: Integer representing the liquid level sensitivity to be used. 1 is very high, 4 is low, 5 is from labware definition.
  :params i_bool_ConvertTouL: Boolean determining whether it converts to uL (hslTrue) or stays as mL (hslFalse).
  :params o_arr_VolumesMeasured: The array of volumes that were measured.
  :type ML_STAR: Device
  :type i_arrseq_FullReservoirSequences: Array
  :type i_seq_TipsToUse: Sequence
  :type i_seq_TipWaste: Sequence
  :type i_str_TipCounter: Variable
  :type i_int_LLD_Sensitivity: Variable
  :type i_bool_ConvertTouL: Boolean
  :type o_arr_VolumesMeasured: Array
  :return: Whether the measurement has been successful or not
  :rtype: Boolean

.. py:function:: LIQUID_LEVEL_MeasureLiquidSingle(device ML_STAR, sequence i_seq_FullReservoirSequence, sequence i_seq_TipsToUse, sequence i_seq_TipWaste, variable i_str_TipCounter, variable i_bool_IncrementTipSequence, variable i_int_LLD_Sensitivity, variable i_bool_ConvertTouL, variable o_flt_VolumeMeasured)

  This function will pick up the desired tip and will measure the liquid level at the center most well of the desired reservoir and will return the volume in uL. Ensure the sequence used for the reservoir contains the FULL number of positions of the reservoir, otherwise volume estimation will be incomplete! The tip types supported are: 50uL Filter, 50uL, 300uL Filter, 300uL, 1000uL Filter, and 1000uL.

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown.
  :params i_seq_FullReservoirSequences: The full reservoir sequence to be checked.
  :params i_seq_TipsToUse: The sequence of the tips to be used to measure the liquid level.
  :params i_seq_TipWaste: The sequence of the waste used to eject the tips.
  :params i_str_TipCounter: The tip counter to be used for the tips on pickup. Place "" if no tip counter will be used.
  :params i_bool_IncrementTipSequence: Boolean determining whether the tip sequence should be incremented after pickup or not.
  :params i_int_LLD_Sensitivity: Integer representing the liquid level sensitivity to be used. 1 is very high, 4 is low, 5 is from labware definition.
  :params i_bool_ConvertTouL: Boolean determining whether it converts to uL (hslTrue) or stays as mL (hslFalse).
  :params o_flt_VolumeMeasured: A float of the volume that was measured.
  :type ML_STAR: Device
  :type i_seq_FullReservoirSequences: Sequence
  :type i_seq_TipsToUse: Sequence
  :type i_seq_TipWaste: Sequence
  :type i_str_TipCounter: Variable
  :type i_bool_IncrementTipSequence: Boolean
  :type i_int_LLD_Sensitivity: Variable
  :type i_bool_ConvertTouL: Boolean
  :type o_flt_VolumeMeasured: Float
  :return: Whether the measurement has been successful or not
  :rtype: Boolean

.. py:function:: LIQUID_LEVEL_ReturnVolumesFromLiquidLevel(device ML_STAR, variable i_str_PipettingReturn, variable i_str_LiquidLevelReturn, variable i_bool_ConvertTouL, array o_arr_VolumesMeasured)

  This function will return the volumes that were measured from a previous aspiration step.

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_str_PipettingReturn: The return value of the pipetting step to measure liquid level
  :params i_str_LiquidLevelReturn: The return value of the liquid level detect
  :params i_bool_ConvertTouL: Boolean determining whether it converts to uL (hslTrue) or stays as mL (hslFalse)
  :params o_arr_VolumesMeasured: An array of the volumes which were measured for each channel
  :type ML_STAR: Device
  :type i_str_PipettingReturn: Variable
  :type i_str_LiquidLevelReturn: Variable
  :type i_bool_ConvertTouL: Boolean
  :type o_arr_VolumesMeasured: Array
  :return: None
  :rtype: N/A

.. py:function:: MOVE_ChannelsToSequencePosition(device ML_STAR, variable i_str_ChPattern, sequence i_seq_Positions, variable i_flt_ZHeight)

  This function moves the 1mL channels to set positions. This function will only move the channels that are activated by the channel pattern.  The positions in the sequence will skip over the positions where the channel is turned off.

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_str_ChPattern: The channel pattern of the pipettes to move  
  :params i_seq_Positions: The X Y positions to move the channels to
  :params i_flt_ZHeight: The Z positions to end the channels in
  :type ML_STAR: Device
  :type i_str_ChPattern: Variable
  :type i_seq_Positions: Sequence
  :type i_flt_ZHeight: Variable
  :return: None
  :rtype: N/A

.. py:function:: MOVE_ChannelsToSequencePosition_5mL(device ML_STAR, variable i_str_ChPattern, sequence i_seq_Positions, variable i_flt_ZHeight)

  This function moves the 5mL channels to set positions. This function will only move the channels that are activated by the channel pattern.  The positions in the sequence will skip over the positions where the channel is turned off.

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_str_ChPattern: The channel pattern of the pipettes to move  
  :params i_seq_Positions: The X Y positions to move the channels to
  :params i_flt_ZHeight: The Z positions to end the channels in
  :type ML_STAR: Device
  :type i_str_ChPattern: Variable
  :type i_seq_Positions: Sequence
  :type i_flt_ZHeight: Variable
  :return: None
  :rtype: N/A

.. py:function:: MOVE_CheckPlateWithTwoChannels(device ML_STAR, variable i_int_FrontMostChannel, sequence i_seq_PlateToCheck, variable i_flt_TapWidth)

  This function will take the front most channel and the channel behind it to tap the labware at the sequence position.  This function requires both channels to either have a tip or tool loaded on them before calling.  

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_int_FrontMostChannel: The front-most channel being used to check plates
  :params i_seq_PlateToCheck: The sequence position to perform a tap to check for plate existence
  :params i_flt_TapWidth: The distance in mm for the channels to be separated before tapping
  :type ML_STAR: Device
  :type i_int_FrontMostChannel: Variable
  :type i_seq_PlateToCheck: Sequence
  :type i_flt_TapWidth: Variable
  :return: Boolean determining whether plate was found (hslTrue) or not (hslFalse)
  :rtype: Boolean

.. py:function:: MOVE_InitDispenseDrive(device ML_STAR, variable i_int_ChannelNumber)

  This function moves the dispense drive for the specified 1mL channel to its home position

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_int_ChannelNumber: The channel to initialise the dispense drive
  :type ML_STAR: Device
  :type i_int_ChannelNumber: Variable
  :return: None
  :rtype: N/A

.. py:function:: MOVE_InitDispenseDrive_5mL(device ML_STAR, variable i_int_ChannelNumber)

  This function moves the dispense drive for the specified 5mL channel to its home position

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_int_ChannelNumber: The channel to initialise the dispense drive
  :type ML_STAR: Device
  :type i_int_ChannelNumber: Variable
  :return: None
  :rtype: N/A

.. py:function:: PLATE_STACK_CountPlateStacks(device ML_STAR, sequence i_seq_PlateStack_Full, sequence o_seq_PlateStack_Count, variable o_int_PlateCount)

  This function will use the channels to measure the number of plates in a plate stack

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_seq_PlateStack_Full: The full sequence of the plate stack to measure
  :params o_seq_PlateStack_Count: The sequence of the plate stack measured
  :params o_int_PlateCount: The total number of plates measured in the plate stack
  :type ML_STAR: Device
  :type i_seq_PlateStack_Full: Sequence
  :type o_seq_PlateStack_Count: Sequence
  :type o_int_PlateCount: Variable
  :return: None
  :rtype: N/A

.. py:function:: QUERY_GetChannelPosition(device ML_STAR, variable i_int_ChNumber, variable o_flt_XCoord, variable o_flt_YCoord, variable o_flt_ZCoord)

  This function will return the current coordinate of the specified 1mL channel

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_int_ChNumber: The number of the channel whose position is being checked
  :params o_flt_XCoord: The X coordinate of the channel
  :params o_flt_YCoord: The Y coordinate of the channel
  :params o_flt_ZCoord: The Z coordinate of the channel
  :type ML_STAR: Device
  :type i_int_ChNumber: Variable
  :type o_flt_XCoord: Variable
  :type o_flt_YCoord: Variable
  :type o_flt_ZCoord: Variable
  :return: None
  :rtype: N/A

.. py:function:: QUERY_GetChannelPosition_5mL(device ML_STAR, variable i_int_ChNumber, variable o_flt_XCoord, variable o_flt_YCoord, variable o_flt_ZCoord)

  This function will return the current coordinate of the specified 5mL channel

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_int_ChNumber: The number of the channel whose position is being checked
  :params o_flt_XCoord: The X coordinate of the channel
  :params o_flt_YCoord: The Y coordinate of the channel
  :params o_flt_ZCoord: The Z coordinate of the channel
  :type ML_STAR: Device
  :type i_int_ChNumber: Variable
  :type o_flt_XCoord: Variable
  :type o_flt_YCoord: Variable
  :type o_flt_ZCoord: Variable
  :return: None
  :rtype: N/A

.. py:function:: QUERY_GetTipPresentState(device ML_STAR, variable i_int_ChNumber, variable o_bln_TipPresent)

  This function outputs true if a tip is loaded and false if a tip is not loaded on the specified 1mL channel

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_int_ChNumber: The number of the channel which is being checked
  :params o_bln_TipPresent: A boolean output of whether the tip is present (hslTrue) or not (hslFalse)
  :type ML_STAR: Device
  :type i_int_ChNumber: Variable
  :type o_bln_TipPresent: Variable
  :return: None
  :rtype: N/A

.. py:function:: QUERY_GetTipPresentState_5mL(device ML_STAR, variable i_int_ChNumber, variable o_bln_TipPresent)

  This function outputs true if a tip is loaded and false if a tip is not loaded on the specified 5mL channel

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_int_ChNumber: The number of the channel which is being checked
  :params o_bln_TipPresent: A boolean output of whether the tip is present (hslTrue) or not (hslFalse)
  :type ML_STAR: Device
  :type i_int_ChNumber: Variable
  :type o_bln_TipPresent: Variable
  :return: None
  :rtype: N/A

.. py:function:: QUERY_GetTipVolume(device ML_STAR, variable i_int_ChNumber, variable o_flt_MaxVolume, variable o_flt_CurrentChannelVolume)

  This function queries the specified 1mL channel to get the max and the current channel volume.  This volume includes the air gap and the conversion made by the correction curve.

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_int_ChNumber: The number of the channel which is being checked
  :params o_flt_MaxVolume: The maximum volume of the channel
  :params o_flt_CurrentChannelVolume: The current volume in the channel
  :type ML_STAR: Device
  :type i_int_ChNumber: Variable
  :type o_flt_MaxVolume: Variable
  :type o_flt_CurrentChannelVolume: Variable
  :return: None
  :rtype: N/A

.. py:function:: QUERY_GetTipVolume(device ML_STAR, variable i_int_ChNumber, variable o_flt_MaxVolume, variable o_flt_CurrentChannelVolume)

  This function queries the specified 5mL channel to get the max and the current channel volume.  This volume includes the air gap and the conversion made by the correction curve.

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_int_ChNumber: The number of the channel which is being checked
  :params o_flt_MaxVolume: The maximum volume of the channel
  :params o_flt_CurrentChannelVolume: The current volume in the channel
  :type ML_STAR: Device
  :type i_int_ChNumber: Variable
  :type o_flt_MaxVolume: Variable
  :type o_flt_CurrentChannelVolume: Variable
  :return: None
  :rtype: N/A

.. py:function:: SPLIT_WELLS_AddContainersToWell(device ML_STAR, sequence i_seq_SequenceToSplit, variable i_int_SequenceIndex, variable i_int_MaxSplitNumber, sequence io_seq_SplitSequence)

  This function will split a well into a sequence of multiple containers, each of which can be aspirated from individually. 

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_seq_SequenceToSplit: The sequence that contains the well to be split into multiple containers
  :params i_int_SequenceIndex: The index of the sequence that is to be split into multiple containers
  :params i_int_MaxSplitNumber: The number of times that the selected container will be split. Won't exceed the width of the well
  :params io_seq_SplitSequence: The sequence containing the split wells. Will append to the end of the sequence. 
  :type ML_STAR: Device
  :type i_seq_SequenceToSplit: Sequence
  :type i_int_SequenceIndex: Variable
  :type i_int_MaxSplitNumber: Variable
  :type io_seq_SplitSequence: Sequence
  :return: None
  :rtype: N/A

.. py:function:: SPLIT_WELLS_Remove_Containers(device ML_STAR, variable i_bool_UpdateVolumes)

  This function will remove the containers added by the split wells function

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_bool_UpdateVolume: A boolean determining whether to update the split source volume with the volume set in sample tracking. 
  :type ML_STAR: Device
  :type i_bool_UpdateVolume: Boolean
  :return: None
  :rtype: N/A

.. py:function:: TRAVEL_LANES_MoveChannelsToTravelLanes(device ML_STAR)

  This function will move the 1mL channels to the travel lanes

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :type ML_STAR: Device
  :return: None
  :rtype: N/A

.. py:function:: TRAVEL_LANES_MoveChannelsToTravelLanes_5mL(device ML_STAR)

  This function will move the 5mL channels to the travel lanes

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :type ML_STAR: Device
  :return: None
  :rtype: N/A

.. py:function:: TRAVEL_LANES_MoveChannelsToYPosition(device ML_STAR, sequence i_seq_TargetSequence, variable i_flt_XOffsetFromOrigin)

  Parameters include the Instrument, a destination sequence, and whether or not a shift in the x-direction is wanted before moving the 1mL channels in y-direction (to doubly ensure no crossver of open wells).  Channels will be moved to their Y coordinates at the X origin of the next labware in the sequence plus the X offset. The channels will move to the current position of the input Sequence.

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_seq_TargetSequence: The sequence to move the channels to
  :params i_flt_XOffsetFromOrigin: The distance from the plate's origin to start the channel approach
  :type ML_STAR: Device
  :type i_seq_TargetSequence: Sequence
  :type i_flt_XOffsetFromOrigin: Variable
  :return: None
  :rtype: N/A

.. py:function:: TRAVEL_LANES_MoveChannelsToYPosition_5mL(device ML_STAR, sequence i_seq_TargetSequence, variable i_flt_XOffsetFromOrigin)

  Parameters include the Instrument, a destination sequence, and whether or not a shift in the x-direction is wanted before moving the 5mL channels in y-direction (to doubly ensure no crossver of open wells).  Channels will be moved to their Y coordinates at the X origin of the next labware in the sequence plus the X offset. The channels will move to the current position of the input Sequence.

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_seq_TargetSequence: The sequence to move the channels to
  :params i_flt_XOffsetFromOrigin: The distance from the plate's origin to start the channel approach
  :type ML_STAR: Device
  :type i_seq_TargetSequence: Sequence
  :type i_flt_XOffsetFromOrigin: Variable
  :return: None
  :rtype: N/A

.. py:function:: TRAVEL_LANES_MoveChannelsWithTravelLanes(device ML_STAR, sequence i_seq_TargetSequence, variable i_flt_XOffsetFromOrigin)

  This command is designed to shift all the 1mL channels on the instrument to either the front and/or the back of the instrument in a layout that ensures tips will not crossover any carriers. Parameters include the Instrument, a destination sequence, and whether or not a shift in the x-direction is wanted before moving the channels in y-direction (to doubly ensure no crossver of open wells).  Channels will be moved to their Y coordinates at the X origin of the next labware in the sequence plus the X offset. The channels will move to the current position of the input Sequence.

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_seq_TargetSequence: The sequence to move the channels to
  :params i_flt_XOffsetFromOrigin: The distance from the plate's origin to start the channel approach
  :type ML_STAR: Device
  :type i_seq_TargetSequence: Sequence
  :type i_flt_XOffsetFromOrigin: Variable
  :return: None
  :rtype: N/A

.. py:function:: TRAVEL_LANES_MoveChannelsWithTravelLanes_5mL(device ML_STAR, sequence i_seq_TargetSequence, variable i_flt_XOffsetFromOrigin)

  This command is designed to shift all the 5mL channels on the instrument to either the front and/or the back of the instrument in a layout that ensures tips will not crossover any carriers. Parameters include the Instrument, a destination sequence, and whether or not a shift in the x-direction is wanted before moving the channels in y-direction (to doubly ensure no crossver of open wells).  Channels will be moved to their Y coordinates at the X origin of the next labware in the sequence plus the X offset. The channels will move to the current position of the input Sequence.

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_seq_TargetSequence: The sequence to move the channels to
  :params i_flt_XOffsetFromOrigin: The distance from the plate's origin to start the channel approach
  :type ML_STAR: Device
  :type i_seq_TargetSequence: Sequence
  :type i_flt_XOffsetFromOrigin: Variable
  :return: None
  :rtype: N/A

.. py:function:: TRAVEL_LANES_SingleSource_ChannelDisplacement(device ML_STAR, variable i_strStepReturn)

  This command is designed to move unused 1mL channels to the back of the instrument when pipetting one well at a time while more than one channel has tips/liquid. It requires the Instrument type and Step Return variable from the Aspirate/Dispense step (this is used to determine which channel needs to be moved).

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_strStepReturn: The bound step return from given desired pipetting step
  :type ML_STAR: Device
  :type i_strStepReturn: Variable
  :return: None
  :rtype: N/A

.. py:function:: TRAVEL_LANES_SingleSource_ChannelDisplacement_5mL(device ML_STAR, variable i_strStepReturn)

  This command is designed to move unused 5mL channels to the back of the instrument when pipetting one well at a time while more than one channel has tips/liquid. It requires the Instrument type and Step Return variable from the Aspirate/Dispense step (this is used to determine which channel needs to be moved).

  :params ML_STAR: The ML_STAR itself, will be the only option in the dropdown
  :params i_strStepReturn: The bound step return from given desired pipetting step
  :type ML_STAR: Device
  :type i_strStepReturn: Variable
  :return: None
  :rtype: N/A
