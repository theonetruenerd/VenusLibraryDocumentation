Inheco ODTC
==========================================

The Inheco ODTC library is used to operate up to 4 Inheco ODTC devices, adding both "Standard" and "Advanced" functions to manipulate them. The functions added are:

Standard Functions
-----------------------------------------

- :ven:func:`Connect`
- :ven:func:`GetStatus`
- :ven:func:`Reset`
- :ven:func:`Initialize`
- :ven:func:`SetTraceLevel`
- :ven:func:`OpenDoor`
- :ven:func:`CloseDoor`
- :ven:func:`DownloadProtocol`
- :ven:func:`ExecuteMethod`
- :ven:func:`WaitForEndOfExecuteMethod`
- :ven:func:`StopMethod`
- :ven:func:`Abort`
- :ven:func:`ReadActualTemperature`
- :ven:func:`Terminate`
- :ven:func:`EvaluateError`
- :ven:func:`AddAllowedReturnCode`

Advanced Functions
-----------------------------------------

- :ven:func:`LockDevice`
- :ven:func:`UnlockDevice`
- :ven:func:`SetCSVSeparator`
- :ven:func:`SetDateTime`
- :ven:func:`SetNetWorkConfig`
- :ven:func:`GetParameters`
- :ven:func:`GetDeviceIdentification`
- :ven:func:`GetConfiguration`
- :ven:func:`Pause`
- :ven:func:`DoContinue`
- :ven:func:`SetParameters`
- :ven:func:`SetLogLevel`
- :ven:func:`RegisterStatusEventURL`
- :ven:func:`UnregisterStatusEventURL`
- :ven:func:`GetLastData`
- :ven:func:`DisableTemperatureEvent`

.. ven:function:: Connect(variable i_strLocalIP, variable i_strDeviceIP, variable i_strDevicePort, variable i_blnSimulationMode, variable o_intDeviceID, variable o_strMessage)

  This function is used to connect to the Inheco ODTC device.

  :params i_strLocalIP: The IP address of the computer. If this parameter is set to an empty string, the library will try to retrieve the computer's IP address automatically. If automatic IP address configuration doesn't work (i.e. two or more network cards in the system have close IP addresses), configure the IP address to a fixed one and supply this address.
  :params i_strDeviceIP: The IP address of the ODTC device. This must be in the format of "xxx.xxx.xxx.xxx". The IP address of the device can be retrieved using the Inhecodevice finder tool located in the library directory. Start the application 'DeviceFinder (xxxxx).exe' where xxxxx represents a five-digit revision number, wait at least 20 seconds to see the retrieved ip address. If address is not found automatically, click button 'Find Device via Name/IP' and supply the string ODTC_XXXXXX where XXXXXX represents the last 6 characters of the device's MAC address. The string to provide may be found on the label SiLA Service Configuration located on the device controller. 
  :params i_strDevicePort: The port used by the ODTC device. Should be set to "". This parameter should only be set to a specific port on official request as the device has to be configured to use this special port.
  :params i_blnSimulationMode: Simulation mode for the library. Set to either 0 (device is not simulated) or 1 (device is simulated).
  :params o_intDeviceID: The unique identifier for this device. Use this number as input for all subsequent function calls.
  :params o_strMessage: Informational message
  :type i_strLocalIP: Variable
  :type i_strDeviceIP: Variable
  :type i_strDevicePort: Variable
  :type i_blnSimulationMode: Boolean
  :type o_intDeviceID: Variable
  :type o_strMessage: Variable
  :return: A boolean as to whether the function returned successfully (1) or not (0).
  :rtype: Boolean

.. ven:function:: GetStatus(variable i_intDeviceID, variable o_strDeviceID, variable o_strState, variable o_blnLocked, variable o_strPMSId, variable o_strCurrentTime, variable o_intSILAReturnValue, variable o_strSILAMessage)

  This function is used to retrieve the status of the device.

  :params i_intDeviceID: The unique identifier for the device as returned by the :ven:func:`Connect` function. 
  :params o_strDeviceID: Internal information of the device
  :params o_strState: State as reported by the device. One of the following values:'startup', 'resetting', 'standby', 'idle', 'busy', 'paused', 'errorhandling', 'inerror', 'asynchpaused', 'pauserequested', 'processing', 'responsewaiting'
  :params o_blnLocked: Lock state of the device
  :params o_strPMSId: Name of the PMS connected to the device
  :params o_strCurrentTime: Time as reported by the device
  :params o_intSILAReturnValue: The SILA return code of the device
  :params o_strSILAMessage: The SILA message returned by the device
  :type i_intDeviceID: Variable
  :type o_strDeviceID: Variable
  :type o_strState: Variable 
  :type o_blnLocked: Variable
  :type o_strPMSId: Variable
  :type o_strCurrentTime: Variable
  :type o_intSILAReturnValue: Variable
  :type o_strSILAMessage: Variable
  :return: A boolean as to whether the function returned succesfully (1) or not (0).
  :rtype: Boolean
