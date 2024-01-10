Error Codes & Debugging
===========================

I will try compile as many different error codes and their explanations here, as well as potential causes and solutions to deal with them as and when they pop up. If there are any you wish to add, please message me on my discord "theonetruenerd" or email me at "tarunchapman@hotmail.com". Notably, the error codes that show up in the trace look slightly different to the ones presented here. If the trace error code looks like this: (0x12 - 0x3 - 0x45) [which corresponds to (MinorID - MajorID - SpecificErrorID)], then the translated error code will look like this: 0xa3120045. The error code should always be 10 digits long, with zeroes padding the bit between the 2 and 45. 

The Major ID is usually assigned in the library which is causing the error; for example in HSLUtilLib2 there is a function called "Error" in which there is a static const variable called MajorID. The minor ID corresponds to the general type of error; in HSLUtilLib2 "0x01" is used to refer to a general runtime error.

  - :ref:`Runtime Errors <RuntimeErrors>`
  - :ref:`Syntax Errors <SyntaxErrors>`
  - :ref:`Unsorted Errors <FirmwareErrors>`

Major IDs that have been identified (unsure if all associated with errors?)
------------------------------
  - 76: Hamilton.HxServicesBase
  - 85: Hamilton.HxElementCounter
  - 96: Hamilton.HxDatabase
  - 97: Hamilton.HxVectorDatabase

Minor IDs that have been identified (unsure if all associated with errors?)
------------------------------

Hamilton.HxVectorDB:

- 01: IHxVectorDbTracking
- 02: IHxVectorDbWorklistManagement
- 03: IHxVectorDbManagement
- 04: IHxVectorDbConfiguration
- 05: IHxVectorDbFilter
- 06: WorkerThread
- 07: ConnectionStringWizardTools
- 08: Singleton

Hamilton.HxDatabase:

- 00: Global
- 01: Singleton
- 02: ResourceManager
- 03: Error
- 05: IHxDbManagement
- 06: IHxDbConfiguration
- 07: Utilities
- 16: IHxDbCommand
- 17: IHxDbCommandCollection
- 18: IHxDbConnection
- 19: IHxDbCreateParameterCollection
- 20: IHxDbCreateProcedureCommand
- 21: IHxDbCreateTableCommand
- 22: IHxDbDataReader
- 23: IHxDbParameter
- 24: IHxDbParameterCollection
- 25: IHxDbTransaction

[Need sorting]

- 10: HxEmail
- 20: HxErrorEvent
- 21: SendAddress
- 22: SendFlag
- 23: ExecuteFlag
- 24: ExecuteName
- 26: startApplication
- 27: ExecuteArgument
- 40: HxGeneralSettings()
- 42: RequiredPasswordLength
- 43: SystemName
- 44: SimulationOn
- 45: GetSequenceRGB
- 46: AskForSequenceNameAfterDrop
- 47: GetSound
- 48: SetSound
- 49: GetTimeout
- 50: SetTimeout
- 60: HxInstallation
- 62: GetFeatureDescription
- 63: ActivateFeature
- 64: InstallFeature
- 65: GetFeatureExpiryISODate
- 66: GetFeatureStatusText
- 67: LegalizeInstallation
- 68: GetFeatureNameFromId
- 69: GetFeatureDescriptionById
- 70: GetFeatureExpiryISODateById
- 71: GetFeatureStatusTextById
- 72: UninstallFeature
