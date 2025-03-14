Error Codes & Debugging
===========================

I will try compile as many different error codes and their explanations here, as well as potential causes and solutions to deal with them as and when they pop up. If there are any you wish to add, please message me on my discord "theonetruenerd" or email me at "tarunchapman@hotmail.com". Notably, the error codes that show up in the trace look slightly different to the ones presented here. If the trace error code looks like this: (0x12 - 0x3 - 0x45) [which corresponds to (MajorID - MinorID - SpecificErrorID)], then the translated error code will look like this: 0xa3120045. The error code should always be 10 digits long, with zeroes padding the bit between the 2 and 45. 

The Major ID is usually assigned in the library which is causing the error; for example in HSLUtilLib2 there is a function called "Error" in which there is a static const variable called MajorID. The minor ID corresponds to the general type of error; in HSLUtilLib2 "0x01" is used to refer to a general runtime error.

At least I think? I've found a bit of inconsistency so will keep digging.

- :ref:`Runtime Errors <RuntimeErrors>`
- :ref:`Syntax Errors <SyntaxErrors>`
- :ref:`Unsorted Errors <FirmwareErrors>`

Major IDs that have been identified
------------------------------
NB: The codes are in hexadecimal so (for example) 31 = 1F

- 0: None
- 2: HxCfgFil
- 3: HxTrcFil
- 4: HxParams
- 5: HxLabwr
- 6: HxPlumb
- 7: HxM4Comm
- 8: HxM4Inst
- 9: HxM4PPtr
- 10: HxPm4Met
- 11: HxPm4Cfg
- 12: HxPm4Run
- 13: HxPhnx
- 14: HxMovPrb
- 15: HxSsInst
- 16: HxDeckEd
- 17: HxRun
- 18: HxReg
- 19: HxM4MetsDat
- 20: HxM4MetsCfg
- 21: HxP96P4Wz
- 22: HxP96M4MetsRun
- 23: HxM4PPtrCfg
- 25: HxM4LoadCfg
- 26: HxM4PrbInLabwr
- 27: HxCfgEd
- 28: HxPm4Wz
- 29: HxWrkFil
- 30: HxM4PPtrCfg2
- 31: HxM4CComm
- 32: HxM4PPtrPars
- 33: HxM4Transfer
- 34: HxHslParser
- 35: HxHslExecutor
- 36: HxHslRctl
- 37: HxFdxProtocol
- 38: HxSerial
- 39: HxTextMet
- 40: HxGruCommand
- 41: HxGruInst
- 42: HxCommand
- 43: HxSwapCommand
- 44: HxProSim
- 45: HxCompCommand
- 46: HxMetEdCompCmd
- 47: HxPrbInLw
- 48: HxMetEd
- 49: HxCommunication
- 50: HxProtocol
- 51: HxUsbComm
- 52: HxGruCompCmd
- 53: HxSampleTracker
- 54: HxGruLiquid
- 55: HxSecurity
- 56: HxGruLiquidEditor
- 57: HxStarMaintAndVer
- 58: HxSoftMaxPro
- 59: HxCytomat
- 60: HxM4Command
- 61: HxCarousel
- 62: HxMetChaining
- 63: HxAuditTrail
- 64: HxTrace
- 65: HxTraceView
- 66: HxView
- 67: HxWatchView
- 68: HxPowerWaveHt
- 69: HxInstrumentData
- 70: HxMethodCopy
- 71: HxBtiElx405AutoWasher
- 72: HxSecurityCom
- 73: HxStarBvsCommand
- 74: HxStarBvsConfig
- 75: HxReportConfig
- 76: HxServices
- 77: HxScheduleView
- 78: HxStCompCmd
- 79: HxStarData
- 80: HxUserManager
- 81: HxSchedCompCmd
- 82: HxFan
- 83: HxSysDeck
- 84: HxVSpin
- 85: HxElementCounter
- 86: HxStarConfig
- 87: HxConfigEditor
- 88: HxStarDevices
- 89: HxVSpinAccess2
- 90: HxEditSequenceDlg
- 91: HxStarBiotechMaintMet
- 92: HxLabwrcat
- 93: HxLabwrCatComponents
- 94: HxStarDynDilLib
- 95: HxMosquito
- 96: HxDatabase
- 97: HxVectorDatabase
- 98: HxTranslationSupport
- 99: HxUtilLib
- 100: HxReagentDisp
- 101: HxSpeVacuum
- 102: HxM384
- 103: HxGen5
- 104: HxBigBearShaker
- 105: HxSys3DView
- 106: HxImpactCmd
- 107: HxXRPLiteMC
- 108: NimbusFourProbe
- 109: TrackGripper
- 110: HxCoreDevices
- 111: HxCoreLiquid
- 112: HxCoreLiquidEditor
- 113: HxXRPLiteConfigurator
- 114: HxTcpIpBdzComm
- 115: MiroIncubatorCmd
- 116: GuavaLinkCmd
- 117: PowerSocket
- 118: HxCustomDialog
- 119: GlasColMixerCmd
- 120: EntryExit
- 121: ForteOctetCmd
- 122: NexusXPeelCmd
- 123: PHERAstar_module
- 124: HXETRACKCMD

Minor IDs that have been identified 
------------------------------

NB: Codes are once again in hexadecimal. I'm slightly unsure on some of these

HxVectorDB:

- 0: UnexpectedError
- 1: InterfaceNotInitialized
- 2: CannotInitializedInterface
- 3: CannotGetTableSchema
- 4: CannotGetElementCounter
- 5: ErrorInWorkerThread
- 6: CannotGetProperty
- 7: CannotSetProperty
- 8: CannotGetTranslationTable
- 9: CannotAddAdditionalData
- 10: CannotGetAdditionalData
- 11: CannotDeleteAdditionalData
- 16: Worklist_CannotAddJobs
- 17: Worklist_CannotGetJobs
- 18: Worklist_CannotGetJobAdditionalData
- 19: Worklist_CannotRemoveJob
- 20: Worklist_CannotGetJobState
- 21: Worklist_CannotAddJobAdditionalData
- 22: Worklist_CannotDeleteJobAdditionalData
- 23: Worklist_CannotGetJob
- 24: Worklist_CannotSetJobState
- 48: Tracking_CannotStartRun
- 49: Tracking_CannotPauseRun
- 50: Tracking_CannotResumeRun
- 51: Tracking_CannotEndRun
- 52: Tracking_CannotAbortRun
- 53: Tracking_CannotInterruptRun
- 54: Tracking_CannotCreateDeck
- 55: Tracking_CannotGetDeckID
- 56: Tracking_CannotGetAllLabwareOnDeck
- 57: Tracking_CannotGetLoadStateOfLabware
- 58: Tracking_CannotGetElementID
- 59: Tracking_CannotGetLabware
- 60: Tracking_CannotGetLabwareLoadingTime
- 61: Tracking_CannotAssignLabwareToJob
- 62: Tracking_CannotAssignLabwareToJobs
- 63: Tracking_CannotGetLabwareBarcode
- 64: Tracking_CannotGetLabwareVolume
- 65: Tracking_CannotGetLabwareState
- 66: Tracking_CannotUpdateTADMCurveIDForVolumeMove
- 67: Tracking_CannotGetLabwareLastSourceBarcode
- 68: Tracking_CannotGetLabwareSourceBarcodeList
- 69: Tracking_CannotGetLabwareInitialValues
- 70: Tracking_CannotGetRunID
- 71: Tracking_CannotGetRun
- 72: Tracking_CannotGetRunState
- 73: Tracking_CannotGetUserRunState
- 74: Tracking_CannotSetUserRunState
- 75: Tracking_CannotGetRunActions
- 76: Tracking_CannotGetRunAction
- 77: Tracking_CannotAddRunAction
- 78: Tracking_CannotGetElementIDs
- 79: Tracking_CannotGetLabwareHierarchy
- 80: Tracking_CannotTrackActionLoad
- 81: Tracking_CannotTrackActionUnload
- 82: Tracking_CannotTrackActionMoveVolume
- 83: Tracking_CannotTrackActionMove
- 84: Tracking_CannotTrackActionWash
- 85: Tracking_CannotTrackActionIncubate
- 86: Tracking_CannotTrackActionSetBarcode
- 87: Tracking_CannotTrackActionSetLabwareState
- 88: Tracking_CannotTrackActionCustomAction


HxDatabase:

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

Internal Error Codes which have been identified (presumably is the same as SpecificErrorId?)
-----------------------------------------------------
NB: Once again, these are in Hexadecimal and four digits - error code 10 is 000A

HxVectorDatabase:

- 0: UnexpectedError
- 1: InterfaceAlreadyInitialized
- 2: CannotDetermineAdditionalValueType
- 3: UnknownEnumValue
- 4: UnsupportedEnumValue
- 5: UnsupportedValueFromDB
- 6: InconsistentDB
- 7: NotImplemented
- 8: CannotConnectToDb
- 9: CannotDetermineOS
- 10: ValueOutOfRange
- 11: ExternalDatabaseServerNotSupportedInStandardVersion
- 12: FunctionNotSupportedInStandardVersion
- 13: FunctionNotSupportedOnRemoteDatabaseServer
- 14: CannotFindConfigFile
- 15: CannotFindSqlScript
- 16: CannotConvertValueToByte
- 17: CannotConvertValueToShort
- 18: CannotConvertValueToInt
- 19: CannotConvertValueToLong
- 20: CannotConvertValueToBool
- 21: CannotConvertValueToDouble
- 22: CannotConvertValueToString
- 23: CannotConvertValueToDateTime
- 32: CannotConvertValueToHxVectorDbJobState
- 33: CannotConvertValueToHxVectorDbValueType
- 34: CannotConvertValueToHxVectorDbActionState
- 35: CannotConvertValueToHxPars
- 36: CannotConvertValueToHxVectorDbLabwareHandling
- 37: CannotConvertValueToHxVectorDbLabwareLevel
- 38: CannotConvertValueToHxVectorDbLabwareState
- 39: CannotConvertValueToHxVectorDbStepType
- 40: BadParameterSupplied
- 41: CannotConvertValueToHxVectorDbRunState
- 42: CannotSetValueInConfigFile
- 43: CannotGetValueInConfigFile
- 44: CannotFindStringInStringTable
- 45: CannotConvertValueToHxVectorDbActionType
- 46: CannotConvertValueToHxVectorDbLabwareUsageType
- 47: CannotConvertValueToHxVectorDbRunAction
- 48: CannotDetachDatabase
- 49: CannotConvertValueToHxVectorDbSortingAlgorithm
- 50: CannotRenameExistingDatabaseFiles
- 51: CannotConvertValueToHxVectorDbActionType
- 52: SqlScriptChecksumVerificationFailed
- 4097: CannotFindJob
- 4098: CannotDeterminePhoenixVersion
- 4099: CannotDetermineCurrentUsername
- 4100: RunAlreadyStarted
- 4101: RunNotRunning
- 4102: RunNotPaused
- 4103: MultipleRunsWithSameGUIDDetected
- 4104: CannotUpdateInternalRunID
- 4105: CannotDetermineInstrumentIDForConfiguration
- 4106: InstrumentDuplicatesInDatabse
- 4107: InstrumentConfigurationDuplicatesInDatabase
- 4108: DeckAlreadyExistsForInstrument
- 4109: LabwareAlreadyExists
- 4110: LabwareDoesNotExist
- 4111: OnlySingleLabwareAccessAllowed
- 4112: UnknownDeckID
- 4113: IllegalLabwareHandlingCombination
- 4114: CannotExtractLabwareName
- 4115: CannotMixActionsOfDifferentActionTypes
- 4116: IfNotExistsCreateNotAllowed
- 4117: IfExistsRemoveNotAllowed
- 4118: IfNotExists_ErrorNotAllowed
- 4119: CannotExtractBaseName
- 4120: CannotNormalizeLabwareAccessName
- 4121: CannotLinkLabware
- 4122: CannotExtractInstrumentName
- 4123: CannotSplitLabwareAccessName
- 4124: CannotDetermineLabwareStatePriority
- 4125: CannotConvertActionStateToLabwareState
- 4126: WrongNumberOfLabwareForAction
- 4127: CannotFindRun
- 4128: CannotFindAction
- 4129: CannotFinishPreWork
- 4130: CannotCreateAction
- 4131: CannotLinkLabware
- 4132: CannotAddDetail
- 4133: CannotAddAdditionalData
- 4134: CannotUpdateLabwareData
- 4135: IfNotExistsIgnoreActionNotAllowed
- 4136: DeckDoesNotExistForInstrument
- 4137: SequenceNotValidAtIndex
- 4138: CannotAddAdditionalData
- 4139: CannotGetAdditionalData
- 4140: CannotDeleteAdditionalData
- 4141: CannotFindRunAction
- 4142: CannotFindInstrument
- 4143: SequenceNotValid
- 4144: ConnectedContainerNotAllowed
- 4145: LabwareOrLabwareTypeNotValid
- 4146: LabwareTypeDoesNotExist
- 4147: LabwareMainTypeDoesNotExist
- 4148: ExperimentDoesNotExist
- 4149: LabwareOrExperimentDoesNotExist
- 4150: CannotAddErrorInfo
- 4151: CurrentLabwareDoesNotMatchPreviousLabware
- 4152: CurrentLabwareAlreadyUsed
- 4153: LabwareIsAlreadyPartOfExperiment
- 4154: ExperimentAlreadyExists
- 4155: DatabaseAlreadyExists
- 4156: DatabaseFileAlreadyAttached
- 4157: CannotFindAValueForAdditionalDataKey
- 4158: IfExistsErrorNotAllowed
- 4159: BadLabwareAccessName
- 4160: CannotFindDeck
- 4161: FileDoesNotExist
- 4162: CannotRemoveExperimentSourceLabware
- 4163: LabwareIsCurrentlyLoadedAndMustBeUnloadedBeforeReloading
- 4164: CannotLookupAdditionalData
- 4165: BarcodeAlreadyUsedAsUniqueBarcode
- 4166: BarcodeNotUnique
- 4167: CannotClearUniqueBarcodeList
- 8193: CannotFindReportDirectory
- 40961: AdditionalDataForeignNotExistsAction
- 40962: AdditionalDataForeignNotExistsInstrument
- 40963: AdditionalDataForeignNotExistsInstrumentConfiguration
- 40964: AdditionalDataForeignNotExistsJob
- 40965: AdditionalDataForeignNotExistsLabware
- 40966: AdditionalDataForeignNotExistsRunAction
- 40967: AdditionalDataForeignNotExistsRun
- 65535: CannotCreateErrorInfo

HxDatabase:

- 0: Unexpected
- 1: CreateTableNotSupported
- 2: CreateProcedureNotSupported
- 3: UnknownEnumValue
- 4: UnsupportedEnumValue
- 5: CannotSynchronizeInternalParameterCollection
- 6: InternalParameterCollectionOutOfSync
- 7: UnknownDBMSIdentifier
- 8: CannotLoadConfigFile
- 9: CannotConvertParameter
- 10: CannotCompareCultureAware
- 11: CannotInferValueFromValue
- 12: BadParameterSupplied
- 13: CannotUseSuppliedConfigFile
- 14: ConfigFileContainsErrors
- 15: ParametersMissing
- 16: SQLScriptCommandTextNotSet
- 17: SQLScriptDoesNotExist
- 18: ExecuteSQLScriptRequiresCommandTypeText
- 19: CannotReadSQLScript
- 20: CannotExecuteSQLScript
- 21: NotImplemented
- 22: CouldNotParseConnectionString
- 65535: CannotCreateErrorInfo
