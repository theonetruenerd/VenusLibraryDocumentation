Check Carrier Presence v2
=======================================

https://github.com/theonetruenerd/VenusPackages/blob/main/CheckCarrierPresence.pkg

This library adds functions which allow you to check whether one or more carriers are loaded on the deck. It requires the sensor at each carrier position to be present and functional. The functions it adds are:

  - :ven:func:`CheckCarrierPresenceByArrOfLabIDs`
  - :ven:func:`CheckCarrierPresenceByLabID`

.. ven:function:: CheckCarrierPresenceByArrOfLabIDs(variable iInstrument, array iArrLabIDs, array oArrLabIDsNotLoaded)

  This function checks whether several carriers are loaded on the deck. This is done by checking if the sensor at each carrier is giving a signal. It will output an array of all the not-loaded carriers, as well as returning a boolean to say whether all carriers are loaded (0) or at least one carrier is not loaded properly (1)

  :params iInstrument: The instrument present, must be ML_STAR
  :params iArrLabIDs: The input array of the Lab IDs for the carriers being checked
  :params oArrLabIDsNotLoaded: The output array of the Lab IDs of any carriers which are not loaded. Empty if every Lab ID is loaded.
  :type iInstrument: Variable
  :type iArrLabIDs: Array
  :type oArrLabIDsNotLoaded: Array
  :return: Boolean of whether all carriers are loaded correctly (0) or at least one carrier is not loaded correctly (1)
  :rtype: Boolean

.. ven:function:: CheckCarrierPresenceByLabID(variable iInstrument, variable iLabIDOfCarrier)

  This function checks whether a carrier is loaded on the deck. This is done by checking if the sensor at the carrier is giving a signal. It will return a boolean to say whether the carrier is not loaded (0) or loaded (1). 

  :params iInstrument: The instrument present, must be ML_STAR
  :params iLabIDOfCarrier: The labware ID of the carrier being checked
  :type iInstrument: Variable
  :type iLabIDOfCarrier: variable  
  :return: A boolean determining whether the carrier is loaded (0) or not loaded (1)
  :rtype: Boolean

