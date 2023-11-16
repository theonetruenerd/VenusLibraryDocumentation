Aliquot with Easy Steps
==========================================

https://github.com/theonetruenerd/VenusPackages/blob/main/Aliquot_for_EasySteps.pkg

The Aliquot with Easy Steps library adds one function aimed at making aliquoting with Easy- or Single steps easier. This library is outdated, the Aliquot_for_EasySteps_v2 library should be used instead. The function it adds is:

- :ven:func:`CalcAliquote`

.. ven:function:: CalcAliquote(sequence DispenseSequence, variable VolumePerWell, variable VolumePreAliquote, variable VolumePostAliquote, variable MaxVolumeTip, variable VolumeToAspirate, variable NumberOfDispense, variable FullTrace, variable NumberOfChannels)

  This function calculates the important variables for performing aliquoting with Easy- or Single steps.

  :params DispenseSequence: The sequence for the aliquots to be dispensed into
  :params VolumePerWell: The volume of the aliquots per well
  :params VolumePreAliquote: The volume of the pre-aliquot
  :params VolumePostAliquote: The volume of the post-aliquot
  :params MaxVolumeTip: The maximum volume of the selected CO-RE Tip
  :params VolumeToAspirate: The volume which has to be aspirated
  :params NumberOfDispense: The number of dispense steps per aspiration
  :params FullTrace: The detail level of the trace (1 is full, 0 is normal)
  :params NumberOfChannels: The number of channels installed on the system
  :type DispenseSequence: Sequence
  :type VolumePerWell: Variable
  :type VolumePreAliquote: Variable
  :type VolumePostAliquote: Variable
  :type MaxVolumeTip: Variable
  :type VolumeToAspirate: Variable
  :type NumberOfDispenses: Variable
  :type FullTrace: Boolean
  :type NumberOfChannels: Variable
  :return: None
  :rtype: N/A
