HSL_SeqDailyTools
=======================================================

https://github.com/theonetruenerd/VenusPackages/blob/main/HSL_SeqDailyTools.pkg 

The HSL_SeqDailyTools library adds four functions aimed at making some parts of sequence handling slightly easier. The four functions it adds are:

- :py:func:`CopyPlatePattern96ToTipRack`
- :py:func:`CopyPlatePatternToPlate`
- :py:func:`GetNumberOfPositionsLeft`
- :py:func:`SeqEasyEdit`

.. py:function:: CopyPlatePattern96ToTipRack(sequence plateSource, sequence tipRack)

  This function copies the sequence pattern on a 96 well plate and applies it to a tip rack. It is used to ensure that the 96 head only picks up tips in the wells that the plate is going to be interacting with.

  :params plateSource: The sequence pattern on the plate to be copied
  :params tipRack: The sequence of the tip rack which will have the template applied to it
  :type plateSource: Sequence
  :type tipRack: Sequence
  :return: None
  :rtype: N/A

.. py:function:: CopyPlatePatternToPlate(sequence plateSource, sequence plateTarget)

  This function copies the pattern of wells from one plate to another plate. It is useful when a plate is being moved around on deck, or when reagents are being pipetted from one plate into the same locations on another plate.

  :params plateSource: The sequence pattern from the plate to be copied
  :params plateTarget: The sequence of the second plate which is having the template applied to it
  :type plateSource: Sequence
  :type plateTarget: Sequence
  :return: None
  :rtype: N/A

.. py:function:: GetNumberOfPositionsLeft(sequence seq, variable numberOfPositionsLeft)

  This function calculates the number of positions left in a sequence

  :params seq: The sequence which is being checked
  :params numberOfPositionsLeft: The output value of how many positions are left in the sequence
  :type seq: Sequence
  :type numberOfPositionsLeft: Variable
  :return: None  
  :rtype: N/A

.. py:function:: SeqEasyEdit(sequence seq, variable timeout, variable dialog_title, variable dialog_msg, device ML_STAR)

  This function is a simplified version of SeqEdit, with only the parameters that are regularly used. It opens a dialog box from which the user can edit whichever sequence is specified in the input.

  :params seq: The sequence which is being edited
  :params timeout: How long the dialog window will stay open by itself before it closes and continues the method without editing the sequence
  :params dialog_title: The title of the dialog window which pops up
  :params dialog_message: The text within the dialog window which pops up
  :params ML_STAR: The device used. Should be ML_STAR from the dropdown
  :type seq: Sequence
  :type timeout: Variable
  :type dialog_title: Variable
  :type dialog_message: Variable
  :type ML_STAR: Device
  :return: None
  :rtype: N/A
