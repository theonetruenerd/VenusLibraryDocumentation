Error Simulator
======================================

https://github.com/theonetruenerd/VenusPackages/blob/main/ErrorSimulator.pkg

This library adds the ability to simulate a variety of errors, to assist with debugging or custom error handling. The functions it adds are:

  - :py:func:`AA_Abstract`
  - :py:func:`STEP1_PrepareRegistryAndCfgFile`
  - :py:func:`STEP2a_SimulateError_Channels`
  - :py:func:`STEP2b_SimulateError_COREGripper`
  - :py:func:`STEP2c_SimulateError_iSWAP`
  - :py:func:`STEP2d_SimulateError_96Head`
  - :py:func:`STEP2e_SimulateError_384Head`
  - :py:func:`STEP2f_SimulateError_BarcodeReading`
  - :py:func:`STEP2g_SimulateError_Autoload`
  - :py:func:`STEP2h_SimulateError_CRWashstation`
  - :py:func:`STEP3_Restore_BackupCfgFile`
  - :py:func:`STEP4_Optional_SwitchChecksum_ON`

.. py:function:: AA_Abstract()

  This function does nothing. In the submethod library itself it simply lists the changelog.

.. py:function:: STEP1_PrepareRegistryAndCfgFile(device ML_STAR)

  This function prepares the system files and registry to perform the error simulation. You can put this step at the beginning of your method, and you can disable it after the 1st run, once all registry and configuration settings are done. It switches off the checksum in the registry, asking for confirmation to modify the registry during run. It converts the \Config\ML_STAR_Simulator.cfg file to ASCII. It creates a copy of ML_STAR_Simulator.cfg named ML_STAR_Simulator.cfg.bak for future restoration if needed. It replaces the string reload "0" with reload "1".

  :params ML_STAR: The instrument being used. Should be ML_STAR.
  :type ML_STAR: Device  
  :return: None
  :rtype: N/A

.. py:function:: STEP2a_SimulateError_Channels(variable ChannelNumber, variable WhenSimulateError, variable ErrorToSimulate, device ML_STAR)

  This function simulates an error in the channels. It can simulate an error of your choice (between errors 1 and 12) in a desired channel at any step of the pipetting process. The error codes are: 
  - 1....... Liquid Level not found  (error 06/70)
  - 2.......  Not enough liquid  (error 06/71)
  - 3....... Liquid level not found with Dual LLD ( error 06/73)
  - 4....... Clot error (error 04/81)
  - 5....... Liquid not correctly aspirated (error 06/80)
  - 6.......Tip already present (error 07/00)
  - 7....... No Tip (error 08/00)
  - 8....... Wrong tip type detected (error 08/78)
  - 9....... Syntax / parameter out of range (error 01/00)
  - 10....... Hardware (error 02/00)  
  - 11....... Not Executed (error 03/00)
  - 12....... Not Completed (error 10/00)

  :params ChannelNumber: A string of the channel(s) in which the error is to be simulated, e.g. "1,2,4,7"
  :params WhenSimulateError: The step of the process in which the error is desired to be simulated. 1 = Aspiration, 2 = Dispense, 3 = Tip pickup, 4 = Tip eject
  :params ErrorToSimulate: Integer corresponding to the desired simulated error, key listed in function description.
  :params ML_STAR: The instrument being used. Should be ML_STAR.
  :type ChannelNumber: Variable
  :type WhenSimulateError: Variable
  :type ErrorToSimulate: Variable
  :type ML_STAR: Device
  :return: None
  :rtype: N/A

.. py:function:: STEP2b_SimulateError_COREGripper(variable ChannelNumber, variable WhenSimulateError, variable ErrorToSimulate, device ML_STAR)

  This function simulates an error in the CO-RE gripper. It can simulate an error of your choice (between errors 1 and 4) in a desired channel at any step of the process. The error codes are:
  - 1....... Can´t get the CORE grippers  (error 08/75)
  - 2....... Step lost in Z drive, crash against something (error 02/62)
  - 3....... Hardware (error 02/00)
  - 4....... Read Barcode Error (05/00)

  :params ChannelNumber: A string of the channel(s) in which the error is to be simulated, e.g. "1,2,4,7"
  :params WhenSimulateError: The step of the process in which the error is desired to be simulated. 1 = Pickup CO-RE, 2 = Get Plate, 3 = Put Plate, 4 = Eject CO-RE gripper
  :params ErrorToSimulate: Integer corresponding to the desired simulated error, key listed in function description.
  :params ML_STAR: The instrument being used. Should be ML_STAR.
  :type ChannelNumber: Variable
  :type WhenSimulateError: Variable
  :type ErrorToSimulate: Variable
  :type ML_STAR: Device
  :return: None
  :rtype: N/A

.. py:function:: STEP2c_SimulateError_iSWAP(variable WhenSimulateError, variable ErrorToSimulate, device ML_STAR)

  This function simulates an error in the iSWAP. It can simulate an error of your choice (between errors 1 and 4) at any step of the process. The error codes are:
  - 1...... Expected object not found (error 21/94)
  - 2...... Step lost in Z drive, crash against something (error 02/62)
  - 3...... Hardware (error 02/00)
  - 4...... Object lost (error 23/96)

  :params WhenSimulateError: The step of the process in which the error is desired to be simulated. 1 = Get Plate, 2 = Put Plate
  :params ErrorToSimulate: Integer corresponding to the desired simulated error, key listed in function description.
  :params ML_STAR: The instrument being used. Should be ML_STAR.
  :type WhenSimulateError: Variable
  :type ErrorToSimulate: Variable
  :type ML_STAR: Device
  :return: None
  :rtype: N/A

.. py:function:: STEP2d_SimulateError_96Head(variable WhenSimulateError, variable ErrorToSimulate, device ML_STAR)

  This function simulates an error in the 96-head. It can simulate an error of your choice (between errors 1 and 12 - not all available) at any step of the process. The error codes are:
  - 1....... Liquid Level not found  (error 06/70)
  - 2....... Not enough liquid  (error 06/71)
  - 6....... Tip already present (error 07/00)
  - 7....... No Tip (error 08/00)
  - 8....... Wrong tip type detected (error 08/78)
  - 9....... Syntax / parameter out of range (error 01/00)
  - 10...... Hardware (error 02/00)  
  - 11...... Not Executed (error 03/00)
  - 12...... Not Completed (error 10/00)

  :params WhenSimulateError: The step of the process in which the error is desired to be simulated. 1 = Aspiration, 2 = Dispense, 3 = Tip Pickup, 4 = Tip eject, 5 = Wash
  :params ErrorToSimulate: Integer corresponding to the desired simulated error, key listed in function description.
  :params ML_STAR: The instrument being used. Should be ML_STAR.
  :type WhenSimulateError: Variable
  :type ErrorToSimulate: Variable
  :type ML_STAR: Device
  :return: None
  :rtype: N/A

.. py:function:: STEP2e_SimulateError_384head(variable WhenSimulateError, variable ErrorToSimulate, device ML_STAR)

  This function simulates an error in the 384-head. It can simulate an error of your choice (between errors 1 and 12 - not all available) at any step of the process. The error codes are:
  - 1....... Liquid Level not found  (error 06/70)
  - 2....... Not enough liquid  (error 06/71)
  - 6....... Tip already present (error 07/00)
  - 7....... No Tip (error 08/00)
  - 8....... Wrong tip type detected (error 08/78)
  - 9....... Syntax / parameter out of range (error 01/00)
  - 10...... Hardware (error 02/00)  
  - 11...... Not Executed (error 03/00)
  - 12...... Not Completed (error 10/00)

  :params WhenSimulateError: The step of the process in which desired error is to be simulated. 1 = Aspiration, 2 = Dispense, 3 = Tip Pickup, 4 = Tip eject, 5 = Wash.
  :params ErrorToSimulate: Integer corresponding to the desired simulated error, key listed in function definition.
  :params ML_STAR: The instrument being used. Should be ML_STAR
  :type WhenSimulatedError: Variable
  :type ErrorToSimulate: Variable
  :type ML_STAR: Device
  :return: None
  :rtype: N/A

.. py:function:: STEP2f_SimulateError_BarcodeReading(variable WhenSimulateError, device ML_STAR)

  This function simulates an error during the barcode reading step. It can simulate the error as though it was either the CO-RE grips or the iSWAP involved.

  :params WhenSimulateError: Poorly labelled variable, likely copied and pasted. This is not when the error is simulated; it is instead whether the barcode is being read with CO-RE grips (1) or the iSWAP (2)
  :param ML_STAR: The instrument being used. Should be ML_STAR
  :type WhenSimulateError: Variable
  :type ML_STAR: Device
  :return: None
  :rtype: N/A

.. py:function:: STEP2g_SimulateError_Autoload(variable notReadPosition_Str, variable notPresentPosition_Str, device ML_STAR)

  This submethod simulates the "Barcode not read"  and "Labware not Present Errors".you can enter positions with errors separated by a comma

  :params notReadPosition_Str: A string of comma separated values with the positions in which you want to simulate barcode errors
  :params notPresentPosition_Str: A string of comma separated values with the positions in which you want to simulate labware not present errors.
  :params ML_STAR: The instrument being used. Should be ML_STAR.
  :type notReadPosition_Str: Variable
  :type notPresentPosition_Str: Variable
  :type ML_STAR: Device
  :return: None  
  :rtype: N/A

.. py:function:: STEP2h_SimulateError_CRWashstation(variable errorToSimulate, device ML_STAR)

  This function simulates an error when starting the washing with the CR washstation

  :params errorToSimulate: The error being simulated. 1 = Not washing liquid error, 2 = hardware error.
  :params ML_STAR: The instrument being used. Should be ML_STAR.
  :type errorToSimulate: Variable
  :type ML_STAR: Device
  :return: None
  :rtype: N/A

.. py:function:: STEP3_Restore_BackupCfgFile(device ML_STAR)

  This function restores the backup configuration file created in function STEP1_PrepareRegistryAndCfgFile

  :params ML_STAR: The instrument being used. Should be ML_STAR.
  :type ML_STAR: Device
  :return: None
  :rtype: N/A

.. py:function:: STEP4_Optional_SwitchChecksum_ON()

  This function is optional.  Use it at the end of your method if you want to Switch the File Checksum ON in the registry

  :return: None
  :rtype: N/A
