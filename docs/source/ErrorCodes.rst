Error Codes & Debugging
===========================

I will try compile as many different error codes and their explanations here, as well as potential causes and solutions to deal with them as and when they pop up. If there are any you wish to add, please message me on my discord "theonetruenerd" or email me at "tarunchapman@hotmail.com". Notably, the error codes that show up in the trace look slightly different to the ones presented here. If the trace error code looks like this: (0x12 - 0x3 - 0x45) [which corresponds to (MinorID - MajorID - SpecificErrorID)], then the translated error code will look like this: 0xa3120045. The error code should always be 10 digits long, with zeroes padding the bit between the 2 and 45. 

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
