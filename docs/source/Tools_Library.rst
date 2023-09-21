Tools Library
============================================

https://github.com/theonetruenerd/VenusPackages/blob/main/Tools_Library.pkg

The tools library is designed to add some QoL functions to Venus. It adds the following functions.

- :py:func:`CalculateNumberOfTubesAndVolumePerTube`
- :py:func:`Reformat_Sequence`
- :py:func:`Reformat_ValuesForDialog`

.. py:function:: CalculateNumberOfTubesAndVolumePerTube(variable i_str_ReagentName, variable i_int_NumberOfSamples, variable i_flt_VolumePerSample, variable i_flt_MaximumContainerVolume, variable i_flt_DeadLabwareVolume, variable i_flt_DeadVolumeReagent, variable o_int_NumberOfContainersNeeded, array o_arr_VolumesPerContainer, array o_arr_DescriptionForDialog)

	This function calculates the number of containers needed for a reagent and the volume per container.

	:params i_str_ReagentName: The name of the reagent being calculated
	:params i_int_NumberOfSamples: The number of samples requiring the reagent
	:params i_flt_VolumePerSample: The volume of reagent required for each sample
	:params i_flt_MaximumContainerVolume: The maximum volume a single container can hold
	:params i_flt_DeadVolumeLabware: The dead volume in the labware
	:params i_flt_DeadVolumeReagent: The percentage dead volume of the reagent
	:params o_int_NumberOfContainersNeeded: The calculated number of containers needed
	:params o_arr_VolumesPerContainer: An array of the volumes required for each tube
	:params o_arr_DescriptionForDialog: An array of the descriptions for the dialog
  :type i_str_ReagentName: Variable
  :type i_int_NumberOfSamples: Variable
  :type i_flt_VolumePerSample: Variable
  :type i_flt_MaximumContainerVolume: Variable
  :type i_flt_DeadVolumeLabware: Variable
  :type i_flt_DeadVolumeReagent: Variable
  :type o_int_NumberOfContainersNeeded: Variable
  :type o_arr_VolumesPerContainer: Array of variables
  :type o_arr_DescriptionForDialog: Array of variables
  :return: None
  :rtype: N/A

.. py:function:: Reformat_Sequence(sequence io_sequenceInput, variable i_intNumberOfPositions)

  This function reformats a sequence to have as many positions as needed:
  Source Sequence:
  A1, B1

  Total Number of positions needed = 4

  Output Sequence:
  A1, B1, A1, B1

  :params io_sequenceInput: The sequence of interest
  :params i_intNumberOfPositions: The number of positions required
  :type io_sequenceInput: Sequence
  :type i_intNumberOfPositions: Variable
  :return: None
  :rtype: N/A

.. py:function:: Reformat_ValuesForDialog(variable i_flt_valueToReformat, variable o_str_valueFormatted)

  This function translates floats into strings and gets rid of any trailing 0s. Use the output value to display volumes in dialogs only.

  :params i_flt_valueToReformat: The float to turn into a string
  :params o_str_valueFormatted: The output string after it has been converted from a float
  :type i_flt_valueToReformat: Variable
  :type o_str_valueFormatted: Variable
  :return: None
  :rtype: N/A
