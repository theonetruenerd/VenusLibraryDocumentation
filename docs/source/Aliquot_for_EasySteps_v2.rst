Aliquot for Easy Steps v2
=================================================

https://github.com/theonetruenerd/VenusPackages/blob/main/Aliquot_for_EasySteps_v2.pkg

This library adds two functions aimed at making aliquoting steps easier. The functions added are:

  - :ven:func:`CalcAliquot_v2_1`
  - :ven:func:`CalcChannelPattern`

.. ven:function:: CalcAliquot_v2_1(sequence DispenseSequence, variable VolumePerWell, variable VolumePreAliquote, variable VolumePostAliquote, variable MaxVolumeTip, variable NumberOfDispense, variable NumberOfChannels, variable intNumberOfChannelsInstalled, array arrVolumeToAspirateByChannel, array arrVolumeToMixBeforeAspiration, array arrChannelPatternDispense, variable strChannelPatternAspirate)

  This function calculates the important variables for performing an aliquote pipetting with Easy- or Single Steps

  :params DispenseSequence: The sequence for the aliquots to be dispensed into
  :params VolumePerWell: The volume of the aliquotes per well
  :params VolumePreAliquote: The volume of the pre-aliquote
  :params VolumePostAliquote: The volume of the post-aliquote
  :params MaxVolumeTip: The maximum volume of the selected CO-RE Tip
  :params NumberOfDispense: The number of dispense steps per aspiration
  :params NumberOfChannels: The number of the channels to use for the process
  :params intNumberOfChannelsInstalled: The number of channels installed in the system
  :params arrVolumeToAspirateByChannel: An output of the array of volumes to aspirate by channel
  :params arrVolumeToMixBeforeAspiration: An output of the array of volumes to mix before aspiration (typically used during the first aspiration only)
  :params arrChannelPatternDispense: The output array of channel patterns for the dispense
  :params strChannelPatternAspirate: An output string of the channel pattern to aspirate
  :type DispenseSequence: Sequence
  :type VolumePerWell: Variable 
  :type VolumePreAliquote: Variable
  :type VolumePostAliquote: Variable
  :type MaxVolumeTip: Variable
  :type NumberOfDispense: Variable
  :type NumberOfChannels: Variable
  :type intNumberOfChannelsInstalled: Variable
  :type arrVolumeToAspirateByChannel: Array
  :type arrVolumeToMixBeforeAspiration: Array
  :type arrChannelPatternDispense: Array
  :type strChannelPatternAspirate: String
  :return: None
  :rtype: N/A

.. ven:function:: CalcChannelPattern(variable i_int_NumberOfPositions, variable i_int_NumberOfInstalledChannels, variable o_str_ChannelPattern)

  This function creats a channel pattern based on the number of desired positions and the number of installed channels.

  :params i_int_NumberOfPositions: The number of positions to use, which must be less than or equal to the Number of Installed Channels
  :params i_int_NumberOfInstalledChannels: The number of channels installed on the instrument
  :params o_str_ChannelPattern: The output channel pattern as a string  
  :return: None
  :rtype: N/A
