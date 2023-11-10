PlateEditor96
==========================================

https://github.com/theonetruenerd/VenusPackages/blob/main/PlateEditor96.pkg

This library adds functions which help edit the sequences on a plate dynamically during a method, either with a dialogue or from a csv file. The functions it adds are:

  - :py:func:`EditPlate96_Custom`
  - :py:func:`EditPlate96`
  - :py:func:`EditPlate96_with_BarcodesFromCsv`
  - :py:func:`EditPlate96_with_BarcodesFromExcelAccess`

.. py:function:: EditPlate96_Custom(sequence o_SeqEdit, sequence i_OriginalPlateSeq, variable i_message, variable fixed_number, sequence i_forbiddenWellsSeq, sequence i_preSelectionSeq, variable i_Editable)

  This function shows a GUI to select wells in a 96 plate, and returns a sequence sorted A1,B1,C1... with the selection  with addtional options.

  :params o_SeqEdit: The returned plate sequence with the newly selected wells
  :params i_OriginalPlateSeq: The original input plate sequence which isn't modified
  :params i_message: Message to be shown in the GUI
  :params fixed_number: Set this to 0 if you want a free choice of the number of wells, or to >0 if you want a set value of wells to be chosen
  :params i_forbiddenWellsSeq: Any wells which are unable to be selected
  :params i_preSelectionSeq: Any wells which are automatically selected
  :params i_Editable: A boolean determining whether the user is able to (1) select or deselect wells or not (0). With this at 0, the plate editor effectively becomes a GUI displaying updates of which wells are selected. 
  :type o_SeqEdit: Sequence
  :type i_OriginalPlateSeq: Sequence
  :type i_message: Variable
  :type fixed_number: Variable
  :type i_forbiddenWellsSeq: Sequence
  :type i_preSelectionSeq: Sequence
  :type i_Editable: Boolean
  :return: None
  :rtype: N/A
