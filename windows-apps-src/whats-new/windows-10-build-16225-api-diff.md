---
author: QuinnRadich
title: Windows 10 build 16225 API changes
description: Developers can use the following list to identify new or changed namespaces in Windows 10 SDK Preview Build 16190
keywords: what's new, whats new, update, flighted, flights, API, 16225
ms.author: quradic
ms.date: 7/6/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
---

# New APIs in the Windows 10 SDK Preview Build 16225

New and updated API namespaces have been made available to [Windows Insiders](https://insider.windows.com/) in the Windows 10 SDK Preview Build 16335.

Below is a full list of prelease documentation published for namespaces added or modified since the last public Windows 10 release, [Version 1703](windows-10-version-1703-api-diff.md). **Please note that prerelease documentation may be incomplete and subject to change, and these APIs may be renamed or removed in subsequent builds.**

## windows.applicationmodel

### [windows.applicationmodel.activation](https://docs.microsoft.com/uwp/api/windows.applicationmodel.activation)

#### [commandlineactivatedeventargs](https://docs.microsoft.com/uwp/api/windows.applicationmodel.activation.commandlineactivatedeventargs)

commandlineactivatedeventargs <br> commandlineactivatedeventargs.kind <br> commandlineactivatedeventargs.operation <br> commandlineactivatedeventargs.previousexecutionstate <br> commandlineactivatedeventargs.splashscreen <br> commandlineactivatedeventargs.user

#### [commandlineactivationoperation](https://docs.microsoft.com/uwp/api/windows.applicationmodel.activation.commandlineactivationoperation)

commandlineactivationoperation <br> commandlineactivationoperation.arguments <br> commandlineactivationoperation.currentdirectorypath <br> commandlineactivationoperation.exitcode <br> commandlineactivationoperation.getdeferral

#### [icommandlineactivatedeventargs](https://docs.microsoft.com/uwp/api/windows.applicationmodel.activation.icommandlineactivatedeventargs)

icommandlineactivatedeventargs <br> icommandlineactivatedeventargs.operation

#### [istartuptaskactivatedeventargs](https://docs.microsoft.com/uwp/api/windows.applicationmodel.activation.istartuptaskactivatedeventargs)

istartuptaskactivatedeventargs <br> istartuptaskactivatedeventargs.taskid

#### [startuptaskactivatedeventargs](https://docs.microsoft.com/uwp/api/windows.applicationmodel.activation.startuptaskactivatedeventargs)

startuptaskactivatedeventargs <br> startuptaskactivatedeventargs.kind <br> startuptaskactivatedeventargs.previousexecutionstate <br> startuptaskactivatedeventargs.splashscreen <br> startuptaskactivatedeventargs.taskid <br> startuptaskactivatedeventargs.user

### [windows.applicationmodel.appointments](https://docs.microsoft.com/uwp/api/windows.applicationmodel.appointments)

#### [appointmentstore](https://docs.microsoft.com/uwp/api/windows.applicationmodel.appointments.appointmentstore)

appointmentstore.getchangetracker

#### [appointmentstorechangetracker](https://docs.microsoft.com/uwp/api/windows.applicationmodel.appointments.appointmentstorechangetracker)

appointmentstorechangetracker.istracking

### [windows.applicationmodel.appservice](https://docs.microsoft.com/uwp/api/windows.applicationmodel.appservice)

#### [appservicetriggerdetails](https://docs.microsoft.com/uwp/api/windows.applicationmodel.appservice.appservicetriggerdetails)

appservicetriggerdetails.checkcallerforcapabilityasync

### [windows.applicationmodel.background](https://docs.microsoft.com/uwp/api/windows.applicationmodel.background)

#### [geovisittrigger](https://docs.microsoft.com/uwp/api/windows.applicationmodel.background.geovisittrigger)

geovisittrigger <br> geovisittrigger.geovisittrigger <br> geovisittrigger.monitoringscope

#### [paymentappcanmakepaymenttrigger](https://docs.microsoft.com/uwp/api/windows.applicationmodel.background.paymentappcanmakepaymenttrigger)

paymentappcanmakepaymenttrigger <br> paymentappcanmakepaymenttrigger.paymentappcanmakepaymenttrigger

### [windows.applicationmodel.calls](https://docs.microsoft.com/uwp/api/windows.applicationmodel.calls)

#### [voipcallcoordinator](https://docs.microsoft.com/uwp/api/windows.applicationmodel.calls.voipcallcoordinator)

voipcallcoordinator.setupnewacceptedcall

#### [voipphonecall](https://docs.microsoft.com/uwp/api/windows.applicationmodel.calls.voipphonecall)

voipphonecall.tryshowappui

### [windows.applicationmodel.contacts.dataprovider](https://docs.microsoft.com/uwp/api/windows.applicationmodel.contacts.dataprovider)

#### [contactdataproviderconnection](https://docs.microsoft.com/uwp/api/windows.applicationmodel.contacts.dataprovider.contactdataproviderconnection)

contactdataproviderconnection.createorupdatecontactrequested <br> contactdataproviderconnection.deletecontactrequested

#### [contactlistcreateorupdatecontactrequest](https://docs.microsoft.com/uwp/api/windows.applicationmodel.contacts.dataprovider.contactlistcreateorupdatecontactrequest)

contactlistcreateorupdatecontactrequest <br> contactlistcreateorupdatecontactrequest.contact <br> contactlistcreateorupdatecontactrequest.contactlistid <br> contactlistcreateorupdatecontactrequest.reportcompletedasync <br> contactlistcreateorupdatecontactrequest.reportfailedasync

#### [contactlistcreateorupdatecontactrequesteventargs](https://docs.microsoft.com/uwp/api/windows.applicationmodel.contacts.dataprovider.contactlistcreateorupdatecontactrequesteventargs)

contactlistcreateorupdatecontactrequesteventargs <br> contactlistcreateorupdatecontactrequesteventargs.getdeferral <br> contactlistcreateorupdatecontactrequesteventargs.request

#### [contactlistdeletecontactrequest](https://docs.microsoft.com/uwp/api/windows.applicationmodel.contacts.dataprovider.contactlistdeletecontactrequest)

contactlistdeletecontactrequest <br> contactlistdeletecontactrequest.contactid <br> contactlistdeletecontactrequest.contactlistid <br> contactlistdeletecontactrequest.reportcompletedasync <br> contactlistdeletecontactrequest.reportfailedasync

#### [contactlistdeletecontactrequesteventargs](https://docs.microsoft.com/uwp/api/windows.applicationmodel.contacts.dataprovider.contactlistdeletecontactrequesteventargs)

contactlistdeletecontactrequesteventargs <br> contactlistdeletecontactrequesteventargs.getdeferral <br> contactlistdeletecontactrequesteventargs.request

### [windows.applicationmodel.contacts](https://docs.microsoft.com/uwp/api/windows.applicationmodel.contacts)

#### [contactchangetracker](https://docs.microsoft.com/uwp/api/windows.applicationmodel.contacts.contactchangetracker)

contactchangetracker.istracking

#### [contactlist](https://docs.microsoft.com/uwp/api/windows.applicationmodel.contacts.contactlist)

contactlist.getchangetracker <br> contactlist.limitedwriteoperations

#### [contactlistlimitedwriteoperations](https://docs.microsoft.com/uwp/api/windows.applicationmodel.contacts.contactlistlimitedwriteoperations)

contactlistlimitedwriteoperations <br> contactlistlimitedwriteoperations.trycreateorupdatecontactasync <br> contactlistlimitedwriteoperations.trydeletecontactasync

#### [contactstore](https://docs.microsoft.com/uwp/api/windows.applicationmodel.contacts.contactstore)

contactstore.getchangetracker

### [windows.applicationmodel.core](https://docs.microsoft.com/uwp/api/windows.applicationmodel.core)

#### [applistentry](https://docs.microsoft.com/uwp/api/windows.applicationmodel.core.applistentry)

applistentry.appusermodelid

#### [apprestartfailurereason](https://docs.microsoft.com/uwp/api/windows.applicationmodel.core.apprestartfailurereason)

apprestartfailurereason

### [windows.applicationmodel.datatransfer](https://docs.microsoft.com/uwp/api/windows.applicationmodel.datatransfer)

#### [shareuioptions](https://docs.microsoft.com/uwp/api/windows.applicationmodel.datatransfer.shareuioptions)

shareuioptions.selectionrect <br> shareuioptions.theme

### [windows.applicationmodel.email](https://docs.microsoft.com/uwp/api/windows.applicationmodel.email)

#### [emailmailbox](https://docs.microsoft.com/uwp/api/windows.applicationmodel.email.emailmailbox)

emailmailbox.getchangetracker

### [windows.applicationmodel.payments.provider](https://docs.microsoft.com/uwp/api/windows.applicationmodel.payments.provider)

#### [paymentappcanmakepaymenttriggerdetails](https://docs.microsoft.com/uwp/api/windows.applicationmodel.payments.provider.paymentappcanmakepaymenttriggerdetails)

paymentappcanmakepaymenttriggerdetails <br> paymentappcanmakepaymenttriggerdetails.reportcanmakepaymentresult <br> paymentappcanmakepaymenttriggerdetails.request

### [windows.applicationmodel.payments](https://docs.microsoft.com/uwp/api/windows.applicationmodel.payments)

#### [paymentcanmakepaymentresult](https://docs.microsoft.com/uwp/api/windows.applicationmodel.payments.paymentcanmakepaymentresult)

paymentcanmakepaymentresult <br> paymentcanmakepaymentresult.paymentcanmakepaymentresult <br> paymentcanmakepaymentresult.status

#### [paymentcanmakepaymentresultstatus](https://docs.microsoft.com/uwp/api/windows.applicationmodel.payments.paymentcanmakepaymentresultstatus)

paymentcanmakepaymentresultstatus

#### [paymentrequest](https://docs.microsoft.com/uwp/api/windows.applicationmodel.payments.paymentrequest)

paymentrequest.id <br> paymentrequest.paymentrequest

### [windows.applicationmodel.useractivities.core](https://docs.microsoft.com/uwp/api/windows.applicationmodel.useractivities.core)

#### [coreuseractivitymanager](https://docs.microsoft.com/uwp/api/windows.applicationmodel.useractivities.core.coreuseractivitymanager)

coreuseractivitymanager.deleteuseractivitysessionsintimerangeasync

### [windows.applicationmodel.useractivities](https://docs.microsoft.com/uwp/api/windows.applicationmodel.useractivities)

#### [iuseractivitycontentinfo](https://docs.microsoft.com/uwp/api/windows.applicationmodel.useractivities.iuseractivitycontentinfo)

iuseractivitycontentinfo <br> iuseractivitycontentinfo.tojson

#### [useractivity](https://docs.microsoft.com/uwp/api/windows.applicationmodel.useractivities.useractivity)

useractivity.contentinfo

#### [useractivityattribution](https://docs.microsoft.com/uwp/api/windows.applicationmodel.useractivities.useractivityattribution)

useractivityattribution <br> useractivityattribution.addimagequery <br> useractivityattribution.alternatetext <br> useractivityattribution.iconuri <br> useractivityattribution.useractivityattribution <br> useractivityattribution.useractivityattribution

#### [useractivitychannel](https://docs.microsoft.com/uwp/api/windows.applicationmodel.useractivities.useractivitychannel)

useractivitychannel.deleteactivityasync <br> useractivitychannel.deleteallactivitiesasync

#### [useractivitycontentinfo](https://docs.microsoft.com/uwp/api/windows.applicationmodel.useractivities.useractivitycontentinfo)

useractivitycontentinfo <br> useractivitycontentinfo.fromjson <br> useractivitycontentinfo.tojson

#### [useractivityvisualelements](https://docs.microsoft.com/uwp/api/windows.applicationmodel.useractivities.useractivityvisualelements)

useractivityvisualelements.attribution

### [windows.applicationmodel](https://docs.microsoft.com/uwp/api/windows.applicationmodel)

#### [designmode](https://docs.microsoft.com/uwp/api/windows.applicationmodel.designmode)

designmode.designmode2enabled

#### [packagecatalog](https://docs.microsoft.com/uwp/api/windows.applicationmodel.packagecatalog)

packagecatalog.removeoptionalpackagesasync

#### [packagecatalogremoveoptionalpackagesresult](https://docs.microsoft.com/uwp/api/windows.applicationmodel.packagecatalogremoveoptionalpackagesresult)

packagecatalogremoveoptionalpackagesresult <br> packagecatalogremoveoptionalpackagesresult.extendederror <br> packagecatalogremoveoptionalpackagesresult.packagesremoved

## windows.devices

### [windows.devices.geolocation](https://docs.microsoft.com/uwp/api/windows.devices.geolocation)

#### [geovisit](https://docs.microsoft.com/uwp/api/windows.devices.geolocation.geovisit)

geovisit <br> geovisit.position <br> geovisit.statechange <br> geovisit.timestamp

#### [geovisitmonitor](https://docs.microsoft.com/uwp/api/windows.devices.geolocation.geovisitmonitor)

geovisitmonitor <br> geovisitmonitor.geovisitmonitor <br> geovisitmonitor.getlastreportasync <br> geovisitmonitor.monitoringscope <br> geovisitmonitor.start <br> geovisitmonitor.stop <br> geovisitmonitor.visitstatechanged

#### [geovisitstatechangedeventargs](https://docs.microsoft.com/uwp/api/windows.devices.geolocation.geovisitstatechangedeventargs)

geovisitstatechangedeventargs <br> geovisitstatechangedeventargs.visit

#### [geovisittriggerdetails](https://docs.microsoft.com/uwp/api/windows.devices.geolocation.geovisittriggerdetails)

geovisittriggerdetails <br> geovisittriggerdetails.readreports

#### [visitmonitoringscope](https://docs.microsoft.com/uwp/api/windows.devices.geolocation.visitmonitoringscope)

visitmonitoringscope

#### [visitstatechange](https://docs.microsoft.com/uwp/api/windows.devices.geolocation.visitstatechange)

visitstatechange

### [windows.devices.pointofservice](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice)

#### [claimedlinedisplay](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.claimedlinedisplay)

claimedlinedisplay.checkhealthasync <br> claimedlinedisplay.checkpowerstatusasync <br> claimedlinedisplay.customglyphs <br> claimedlinedisplay.getattributes <br> claimedlinedisplay.getstatisticsasync <br> claimedlinedisplay.maxbitmapsizeinpixels <br> claimedlinedisplay.statusupdated <br> claimedlinedisplay.supportedcharactersets <br> claimedlinedisplay.supportedscreensizesincharacters <br> claimedlinedisplay.trycleardescriptorsasync <br> claimedlinedisplay.trycreatewindowasync <br> claimedlinedisplay.trysetdescriptorasync <br> claimedlinedisplay.trystorestoragefilebitmapasync <br> claimedlinedisplay.trystorestoragefilebitmapasync <br> claimedlinedisplay.trystorestoragefilebitmapasync <br> claimedlinedisplay.tryupdateattributesasync

#### [linedisplay](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplay)

linedisplay.checkpowerstatusasync <br> linedisplay.statisticscategoryselector

#### [linedisplayattributes](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplayattributes)

linedisplayattributes <br> linedisplayattributes.blinkrate <br> linedisplayattributes.brightness <br> linedisplayattributes.characterset <br> linedisplayattributes.currentwindow <br> linedisplayattributes.ischaractersetmappingenabled <br> linedisplayattributes.ispowernotifyenabled <br> linedisplayattributes.screensizeincharacters

#### [linedisplaycursor](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplaycursor)

linedisplaycursor <br> linedisplaycursor.cancustomize <br> linedisplaycursor.getattributes <br> linedisplaycursor.isblinksupported <br> linedisplaycursor.isblocksupported <br> linedisplaycursor.ishalfblocksupported <br> linedisplaycursor.isothersupported <br> linedisplaycursor.isreversesupported <br> linedisplaycursor.isunderlinesupported <br> linedisplaycursor.tryupdateattributesasync

#### [linedisplaycursorattributes](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplaycursorattributes)

linedisplaycursorattributes <br> linedisplaycursorattributes.cursortype <br> linedisplaycursorattributes.isautoadvanceenabled <br> linedisplaycursorattributes.isblinkenabled <br> linedisplaycursorattributes.position

#### [linedisplaycursortype](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplaycursortype)

linedisplaycursortype

#### [linedisplaycustomglyphs](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplaycustomglyphs)

linedisplaycustomglyphs <br> linedisplaycustomglyphs.sizeinpixels <br> linedisplaycustomglyphs.supportedglyphcodes <br> linedisplaycustomglyphs.tryredefineasync

#### [linedisplaydescriptorstate](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplaydescriptorstate)

linedisplaydescriptorstate

#### [linedisplayhorizontalalignment](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplayhorizontalalignment)

linedisplayhorizontalalignment

#### [linedisplaymarquee](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplaymarquee)

linedisplaymarquee <br> linedisplaymarquee.format <br> linedisplaymarquee.repeatwaitinterval <br> linedisplaymarquee.scrollwaitinterval <br> linedisplaymarquee.trystartscrollingasync <br> linedisplaymarquee.trystopscrollingasync

#### [linedisplaymarqueeformat](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplaymarqueeformat)

linedisplaymarqueeformat

#### [linedisplaypowerstatus](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplaypowerstatus)

linedisplaypowerstatus

#### [linedisplaystatisticscategoryselector](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplaystatisticscategoryselector)

linedisplaystatisticscategoryselector <br> linedisplaystatisticscategoryselector.allstatistics <br> linedisplaystatisticscategoryselector.manufacturerstatistics <br> linedisplaystatisticscategoryselector.unifiedposstatistics

#### [linedisplaystatusupdatedeventargs](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplaystatusupdatedeventargs)

linedisplaystatusupdatedeventargs <br> linedisplaystatusupdatedeventargs.status

#### [linedisplaystoredbitmap](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplaystoredbitmap)

linedisplaystoredbitmap <br> linedisplaystoredbitmap.escapesequence <br> linedisplaystoredbitmap.trydeleteasync

#### [linedisplayverticalalignment](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplayverticalalignment)

linedisplayverticalalignment

#### [linedisplaywindow](https://docs.microsoft.com/uwp/api/windows.devices.pointofservice.linedisplaywindow)

linedisplaywindow.cursor <br> linedisplaywindow.marquee <br> linedisplaywindow.readcharacteratcursorasync <br> linedisplaywindow.trydisplaystoragefilebitmapatcursorasync <br> linedisplaywindow.trydisplaystoragefilebitmapatcursorasync <br> linedisplaywindow.trydisplaystoragefilebitmapatcursorasync <br> linedisplaywindow.trydisplaystoragefilebitmapatpointasync <br> linedisplaywindow.trydisplaystoragefilebitmapatpointasync <br> linedisplaywindow.trydisplaystoredbitmapatcursorasync

### [windows.devices.sensors.custom](https://docs.microsoft.com/uwp/api/windows.devices.sensors.custom)

#### [customsensor](https://docs.microsoft.com/uwp/api/windows.devices.sensors.custom.customsensor)

customsensor.maxbatchsize <br> customsensor.reportlatency

#### [customsensorreading](https://docs.microsoft.com/uwp/api/windows.devices.sensors.custom.customsensorreading)

customsensorreading.performancecount

### [windows.devices.sensors](https://docs.microsoft.com/uwp/api/windows.devices.sensors)

#### [accelerometer](https://docs.microsoft.com/uwp/api/windows.devices.sensors.accelerometer)

accelerometer.fromidasync <br> accelerometer.getdeviceselector

#### [accelerometerreading](https://docs.microsoft.com/uwp/api/windows.devices.sensors.accelerometerreading)

accelerometerreading.performancecount <br> accelerometerreading.properties

#### [altimeter](https://docs.microsoft.com/uwp/api/windows.devices.sensors.altimeter)

altimeter.maxbatchsize <br> altimeter.reportlatency

#### [altimeterreading](https://docs.microsoft.com/uwp/api/windows.devices.sensors.altimeterreading)

altimeterreading.performancecount <br> altimeterreading.properties

#### [barometer](https://docs.microsoft.com/uwp/api/windows.devices.sensors.barometer)

barometer.fromidasync <br> barometer.getdeviceselector <br> barometer.maxbatchsize <br> barometer.reportlatency

#### [barometerreading](https://docs.microsoft.com/uwp/api/windows.devices.sensors.barometerreading)

barometerreading.performancecount <br> barometerreading.properties

#### [compass](https://docs.microsoft.com/uwp/api/windows.devices.sensors.compass)

compass.fromidasync <br> compass.getdeviceselector <br> compass.maxbatchsize <br> compass.reportlatency

#### [compassreading](https://docs.microsoft.com/uwp/api/windows.devices.sensors.compassreading)

compassreading.performancecount <br> compassreading.properties

#### [gyrometer](https://docs.microsoft.com/uwp/api/windows.devices.sensors.gyrometer)

gyrometer.fromidasync <br> gyrometer.getdeviceselector <br> gyrometer.maxbatchsize <br> gyrometer.reportlatency

#### [gyrometerreading](https://docs.microsoft.com/uwp/api/windows.devices.sensors.gyrometerreading)

gyrometerreading.performancecount <br> gyrometerreading.properties

#### [inclinometer](https://docs.microsoft.com/uwp/api/windows.devices.sensors.inclinometer)

inclinometer.fromidasync <br> inclinometer.getdeviceselector <br> inclinometer.maxbatchsize <br> inclinometer.reportlatency

#### [inclinometerreading](https://docs.microsoft.com/uwp/api/windows.devices.sensors.inclinometerreading)

inclinometerreading.performancecount <br> inclinometerreading.properties

#### [lightsensor](https://docs.microsoft.com/uwp/api/windows.devices.sensors.lightsensor)

lightsensor.fromidasync <br> lightsensor.getdeviceselector <br> lightsensor.maxbatchsize <br> lightsensor.reportlatency

#### [lightsensorreading](https://docs.microsoft.com/uwp/api/windows.devices.sensors.lightsensorreading)

lightsensorreading.performancecount <br> lightsensorreading.properties

#### [magnetometer](https://docs.microsoft.com/uwp/api/windows.devices.sensors.magnetometer)

magnetometer.fromidasync <br> magnetometer.getdeviceselector <br> magnetometer.maxbatchsize <br> magnetometer.reportlatency

#### [magnetometerreading](https://docs.microsoft.com/uwp/api/windows.devices.sensors.magnetometerreading)

magnetometerreading.performancecount <br> magnetometerreading.properties

#### [orientationsensor](https://docs.microsoft.com/uwp/api/windows.devices.sensors.orientationsensor)

orientationsensor.fromidasync <br> orientationsensor.getdeviceselector <br> orientationsensor.getdeviceselector <br> orientationsensor.maxbatchsize <br> orientationsensor.reportlatency

#### [orientationsensorreading](https://docs.microsoft.com/uwp/api/windows.devices.sensors.orientationsensorreading)

orientationsensorreading.performancecount <br> orientationsensorreading.properties

### [windows.devices.smartcards](https://docs.microsoft.com/uwp/api/windows.devices.smartcards)

#### [smartcardcryptogramgenerator](https://docs.microsoft.com/uwp/api/windows.devices.smartcards.smartcardcryptogramgenerator)

smartcardcryptogramgenerator.issupported

#### [smartcardemulator](https://docs.microsoft.com/uwp/api/windows.devices.smartcards.smartcardemulator)

smartcardemulator.issupported

### [windows.devices.wifi](https://docs.microsoft.com/uwp/api/windows.devices.wifi)

#### [wifiadapter](https://docs.microsoft.com/uwp/api/windows.devices.wifi.wifiadapter)

wifiadapter.connectasync <br> wifiadapter.getwpsconfigurationasync

#### [wificonnectionmethod](https://docs.microsoft.com/uwp/api/windows.devices.wifi.wificonnectionmethod)

wificonnectionmethod

#### [wifiwpsconfigurationresult](https://docs.microsoft.com/uwp/api/windows.devices.wifi.wifiwpsconfigurationresult)

wifiwpsconfigurationresult <br> wifiwpsconfigurationresult.status <br> wifiwpsconfigurationresult.supportedwpskinds

#### [wifiwpsconfigurationstatus](https://docs.microsoft.com/uwp/api/windows.devices.wifi.wifiwpsconfigurationstatus)

wifiwpsconfigurationstatus

#### [wifiwpskind](https://docs.microsoft.com/uwp/api/windows.devices.wifi.wifiwpskind)

wifiwpskind

## windows.gaming

### [windows.gaming.input](https://docs.microsoft.com/uwp/api/windows.gaming.input)

#### [rawgamecontroller](https://docs.microsoft.com/uwp/api/windows.gaming.input.rawgamecontroller)

rawgamecontroller.displayname <br> rawgamecontroller.nonroamableid <br> rawgamecontroller.simplehapticscontrollers

### [windows.gaming.preview.gamesenumeration](https://docs.microsoft.com/uwp/api/windows.gaming.preview.gamesenumeration)

#### [gamelist](https://docs.microsoft.com/uwp/api/windows.gaming.preview.gamesenumeration.gamelist)

gamelist.mergeentriesasync <br> gamelist.unmergeentryasync

#### [gamelistentry](https://docs.microsoft.com/uwp/api/windows.gaming.preview.gamesenumeration.gamelistentry)

gamelistentry.gamemodeconfiguration <br> gamelistentry.launchablestate <br> gamelistentry.launcherexecutable <br> gamelistentry.launchparameters <br> gamelistentry.setlauncherexecutablefileasync <br> gamelistentry.setlauncherexecutablefileasync <br> gamelistentry.settitleidasync <br> gamelistentry.titleid

#### [gamelistentrylaunchablestate](https://docs.microsoft.com/uwp/api/windows.gaming.preview.gamesenumeration.gamelistentrylaunchablestate)

gamelistentrylaunchablestate

#### [gamemodeconfiguration](https://docs.microsoft.com/uwp/api/windows.gaming.preview.gamesenumeration.gamemodeconfiguration)

gamemodeconfiguration <br> gamemodeconfiguration.affinitizetoexclusivecpus <br> gamemodeconfiguration.cpuexclusivitymaskhigh <br> gamemodeconfiguration.cpuexclusivitymasklow <br> gamemodeconfiguration.isenabled <br> gamemodeconfiguration.maxcpucount <br> gamemodeconfiguration.percentgpumemoryallocatedtogame <br> gamemodeconfiguration.percentgpumemoryallocatedtosystemcompositor <br> gamemodeconfiguration.percentgputimeallocatedtogame <br> gamemodeconfiguration.relatedprocessnames <br> gamemodeconfiguration.saveasync

#### [gamemodeuserconfiguration](https://docs.microsoft.com/uwp/api/windows.gaming.preview.gamesenumeration.gamemodeuserconfiguration)

gamemodeuserconfiguration <br> gamemodeuserconfiguration.gamingrelatedprocessnames <br> gamemodeuserconfiguration.getdefault <br> gamemodeuserconfiguration.saveasync

### [windows.gaming.preview](https://docs.microsoft.com/uwp/api/windows.gaming.preview)

#### [windows](https://docs.microsoft.com/uwp/api/windows.gaming.preview.windows)

windows.gaming.preview

### [windows.gaming.ui](https://docs.microsoft.com/uwp/api/windows.gaming.ui)

#### [gamemonitor](https://docs.microsoft.com/uwp/api/windows.gaming.ui.gamemonitor)

gamemonitor <br> gamemonitor.getdefault <br> gamemonitor.requestpermissionasync

#### [gamemonitoringpermission](https://docs.microsoft.com/uwp/api/windows.gaming.ui.gamemonitoringpermission)

gamemonitoringpermission

#### [gameuiprovideractivatedeventargs](https://docs.microsoft.com/uwp/api/windows.gaming.ui.gameuiprovideractivatedeventargs)

gameuiprovideractivatedeventargs <br> gameuiprovideractivatedeventargs.gameuiargs <br> gameuiprovideractivatedeventargs.kind <br> gameuiprovideractivatedeventargs.previousexecutionstate <br> gameuiprovideractivatedeventargs.reportcompleted <br> gameuiprovideractivatedeventargs.splashscreen

## windows.graphics

### [windows.graphics.holographic](https://docs.microsoft.com/uwp/api/windows.graphics.holographic)

#### [holographiccamera](https://docs.microsoft.com/uwp/api/windows.graphics.holographic.holographiccamera)

holographiccamera.createlayerconfig <br> holographiccamera.drmmode <br> holographiccamera.getpresentationlayers <br> holographiccamera.setlayerconfig

#### [holographiccamerarenderingparameters](https://docs.microsoft.com/uwp/api/windows.graphics.holographic.holographiccamerarenderingparameters)

holographiccamerarenderingparameters.getpresentationlayerrenderingparameters

#### [holographicdisplay](https://docs.microsoft.com/uwp/api/windows.graphics.holographic.holographicdisplay)

holographicdisplay.refreshrate

#### [holographicspace](https://docs.microsoft.com/uwp/api/windows.graphics.holographic.holographicspace)

holographicspace.isconfigured

#### [presentationlayerconfig](https://docs.microsoft.com/uwp/api/windows.graphics.holographic.presentationlayerconfig)

presentationlayerconfig <br> presentationlayerconfig.presentationlayersettings

#### [presentationlayerdrmmode](https://docs.microsoft.com/uwp/api/windows.graphics.holographic.presentationlayerdrmmode)

presentationlayerdrmmode

#### [presentationlayerquad](https://docs.microsoft.com/uwp/api/windows.graphics.holographic.presentationlayerquad)

presentationlayerquad <br> presentationlayerquad.drmmode <br> presentationlayerquad.reprojectionmode <br> presentationlayerquad.texturedesc

#### [presentationlayerreference](https://docs.microsoft.com/uwp/api/windows.graphics.holographic.presentationlayerreference)

presentationlayerreference <br> presentationlayerreference.quad <br> presentationlayerreference.type

#### [presentationlayerrenderingparametersquad](https://docs.microsoft.com/uwp/api/windows.graphics.holographic.presentationlayerrenderingparametersquad)

presentationlayerrenderingparametersquad <br> presentationlayerrenderingparametersquad.direct3d11contentbuffer <br> presentationlayerrenderingparametersquad.drmmode <br> presentationlayerrenderingparametersquad.setquadplaneparameters

#### [presentationlayers](https://docs.microsoft.com/uwp/api/windows.graphics.holographic.presentationlayers)

presentationlayers <br> presentationlayers.layers

#### [presentationlayersettings](https://docs.microsoft.com/uwp/api/windows.graphics.holographic.presentationlayersettings)

presentationlayersettings <br> presentationlayersettings.enabled <br> presentationlayersettings.type

#### [presentationlayertype](https://docs.microsoft.com/uwp/api/windows.graphics.holographic.presentationlayertype)

presentationlayertype

### [windows.graphics.printing.workflow](https://docs.microsoft.com/uwp/api/windows.graphics.printing.workflow)

#### [printworkflowconfiguration](https://docs.microsoft.com/uwp/api/windows.graphics.printing.workflow.printworkflowconfiguration)

printworkflowconfiguration.sessionid <br> printworkflowconfiguration.sourceappdisplayname

## windows.management

### [windows.management.deployment](https://docs.microsoft.com/uwp/api/windows.management.deployment)

#### [addpackagebyappinstalleroptions](https://docs.microsoft.com/uwp/api/windows.management.deployment.addpackagebyappinstalleroptions)

addpackagebyappinstalleroptions

#### [packagemanager](https://docs.microsoft.com/uwp/api/windows.management.deployment.packagemanager)

packagemanager.addpackageasync <br> packagemanager.addpackagebyappinstallerfileasync <br> packagemanager.provisionpackageforallusersasync <br> packagemanager.requestaddpackageasync <br> packagemanager.requestaddpackagebyappinstallerfileasync <br> packagemanager.stagepackageasync

## windows.media

### [windows.media.appbroadcasting](https://docs.microsoft.com/uwp/api/windows.media.appbroadcasting)

#### [appbroadcastingmonitor](https://docs.microsoft.com/uwp/api/windows.media.appbroadcasting.appbroadcastingmonitor)

appbroadcastingmonitor <br> appbroadcastingmonitor.appbroadcastingmonitor <br> appbroadcastingmonitor.iscurrentappbroadcasting <br> appbroadcastingmonitor.iscurrentappbroadcastingchanged

#### [appbroadcastingstatus](https://docs.microsoft.com/uwp/api/windows.media.appbroadcasting.appbroadcastingstatus)

appbroadcastingstatus <br> appbroadcastingstatus.canstartbroadcast <br> appbroadcastingstatus.details

#### [appbroadcastingstatusdetails](https://docs.microsoft.com/uwp/api/windows.media.appbroadcasting.appbroadcastingstatusdetails)

appbroadcastingstatusdetails <br> appbroadcastingstatusdetails.isanyappbroadcasting <br> appbroadcastingstatusdetails.isappinactive <br> appbroadcastingstatusdetails.isblockedforapp <br> appbroadcastingstatusdetails.iscaptureresourceunavailable <br> appbroadcastingstatusdetails.isdisabledbysystem <br> appbroadcastingstatusdetails.isdisabledbyuser <br> appbroadcastingstatusdetails.isgamestreaminprogress <br> appbroadcastingstatusdetails.isgpuconstrained

#### [appbroadcastingui](https://docs.microsoft.com/uwp/api/windows.media.appbroadcasting.appbroadcastingui)

appbroadcastingui <br> appbroadcastingui.getdefault <br> appbroadcastingui.getforuser <br> appbroadcastingui.getstatus <br> appbroadcastingui.showbroadcastui

#### [windows](https://docs.microsoft.com/uwp/api/windows.media.appbroadcasting.windows)

windows.media.appbroadcasting

### [windows.media.apprecording](https://docs.microsoft.com/uwp/api/windows.media.apprecording)

#### [apprecordingmanager](https://docs.microsoft.com/uwp/api/windows.media.apprecording.apprecordingmanager)

apprecordingmanager <br> apprecordingmanager.getdefault <br> apprecordingmanager.getstatus <br> apprecordingmanager.recordtimespantofileasync <br> apprecordingmanager.savescreenshottofilesasync <br> apprecordingmanager.startrecordingtofileasync <br> apprecordingmanager.supportedscreenshotmediaencodingsubtypes

#### [apprecordingresult](https://docs.microsoft.com/uwp/api/windows.media.apprecording.apprecordingresult)

apprecordingresult <br> apprecordingresult.duration <br> apprecordingresult.extendederror <br> apprecordingresult.isfiletruncated <br> apprecordingresult.succeeded

#### [apprecordingsavedscreenshotinfo](https://docs.microsoft.com/uwp/api/windows.media.apprecording.apprecordingsavedscreenshotinfo)

apprecordingsavedscreenshotinfo <br> apprecordingsavedscreenshotinfo.file <br> apprecordingsavedscreenshotinfo.mediaencodingsubtype

#### [apprecordingsavescreenshotoption](https://docs.microsoft.com/uwp/api/windows.media.apprecording.apprecordingsavescreenshotoption)

apprecordingsavescreenshotoption

#### [apprecordingsavescreenshotresult](https://docs.microsoft.com/uwp/api/windows.media.apprecording.apprecordingsavescreenshotresult)

apprecordingsavescreenshotresult <br> apprecordingsavescreenshotresult.extendederror <br> apprecordingsavescreenshotresult.savedscreenshotinfos <br> apprecordingsavescreenshotresult.succeeded

#### [apprecordingstatus](https://docs.microsoft.com/uwp/api/windows.media.apprecording.apprecordingstatus)

apprecordingstatus <br> apprecordingstatus.canrecord <br> apprecordingstatus.canrecordtimespan <br> apprecordingstatus.details <br> apprecordingstatus.historicalbufferduration

#### [apprecordingstatusdetails](https://docs.microsoft.com/uwp/api/windows.media.apprecording.apprecordingstatusdetails)

apprecordingstatusdetails <br> apprecordingstatusdetails.isanyappbroadcasting <br> apprecordingstatusdetails.isappinactive <br> apprecordingstatusdetails.isblockedforapp <br> apprecordingstatusdetails.iscaptureresourceunavailable <br> apprecordingstatusdetails.isdisabledbysystem <br> apprecordingstatusdetails.isdisabledbyuser <br> apprecordingstatusdetails.isgamestreaminprogress <br> apprecordingstatusdetails.isgpuconstrained <br> apprecordingstatusdetails.istimespanrecordingdisabled

#### [windows](https://docs.microsoft.com/uwp/api/windows.media.apprecording.windows)

windows.media.apprecording

### [windows.media.capture.frames](https://docs.microsoft.com/uwp/api/windows.media.capture.frames)

#### [mediaframereader](https://docs.microsoft.com/uwp/api/windows.media.capture.frames.mediaframereader)

mediaframereader.acquisitionmode

#### [mediaframereaderacquisitionmode](https://docs.microsoft.com/uwp/api/windows.media.capture.frames.mediaframereaderacquisitionmode)

mediaframereaderacquisitionmode

#### [multisourcemediaframereader](https://docs.microsoft.com/uwp/api/windows.media.capture.frames.multisourcemediaframereader)

multisourcemediaframereader.acquisitionmode

### [windows.media.capture](https://docs.microsoft.com/uwp/api/windows.media.capture)

#### [appbroadcastbackgroundservice](https://docs.microsoft.com/uwp/api/windows.media.capture.appbroadcastbackgroundservice)

appbroadcastbackgroundservice.broadcastchannel <br> appbroadcastbackgroundservice.broadcastchannelchanged <br> appbroadcastbackgroundservice.broadcastlanguage <br> appbroadcastbackgroundservice.broadcastlanguagechanged <br> appbroadcastbackgroundservice.broadcasttitlechanged

#### [appbroadcastbackgroundservicesignininfo](https://docs.microsoft.com/uwp/api/windows.media.capture.appbroadcastbackgroundservicesignininfo)

appbroadcastbackgroundservicesignininfo.usernamechanged

#### [appbroadcastbackgroundservicestreaminfo](https://docs.microsoft.com/uwp/api/windows.media.capture.appbroadcastbackgroundservicestreaminfo)

appbroadcastbackgroundservicestreaminfo.reportproblemwithstream

#### [appcapture](https://docs.microsoft.com/uwp/api/windows.media.capture.appcapture)

appcapture.setallowedasync

#### [appcapturemetadatapriority](https://docs.microsoft.com/uwp/api/windows.media.capture.appcapturemetadatapriority)

appcapturemetadatapriority

#### [appcapturemetadatawriter](https://docs.microsoft.com/uwp/api/windows.media.capture.appcapturemetadatawriter)

appcapturemetadatawriter <br> appcapturemetadatawriter.adddoubleevent <br> appcapturemetadatawriter.addint32event <br> appcapturemetadatawriter.addstringevent <br> appcapturemetadatawriter.appcapturemetadatawriter <br> appcapturemetadatawriter.close <br> appcapturemetadatawriter.metadatapurged <br> appcapturemetadatawriter.remainingstoragebytesavailable <br> appcapturemetadatawriter.startdoublestate <br> appcapturemetadatawriter.startint32state <br> appcapturemetadatawriter.startstringstate <br> appcapturemetadatawriter.stopallstates <br> appcapturemetadatawriter.stopstate

### [windows.media.core](https://docs.microsoft.com/uwp/api/windows.media.core)

#### [audiostreamdescriptor](https://docs.microsoft.com/uwp/api/windows.media.core.audiostreamdescriptor)

audiostreamdescriptor.label

#### [imediastreamdescriptor2](https://docs.microsoft.com/uwp/api/windows.media.core.imediastreamdescriptor2)

imediastreamdescriptor2 <br> imediastreamdescriptor2.label

#### [initializemediastreamsourcerequestedeventargs](https://docs.microsoft.com/uwp/api/windows.media.core.initializemediastreamsourcerequestedeventargs)

initializemediastreamsourcerequestedeventargs <br> initializemediastreamsourcerequestedeventargs.getdeferral <br> initializemediastreamsourcerequestedeventargs.randomaccessstream <br> initializemediastreamsourcerequestedeventargs.source

#### [lowlightfusion](https://docs.microsoft.com/uwp/api/windows.media.core.lowlightfusion)

lowlightfusion <br> lowlightfusion.fuseasync <br> lowlightfusion.maxsupportedframecount <br> lowlightfusion.supportedbitmappixelformats

#### [lowlightfusionresult](https://docs.microsoft.com/uwp/api/windows.media.core.lowlightfusionresult)

lowlightfusionresult <br> lowlightfusionresult.close <br> lowlightfusionresult.frame

#### [mediasource](https://docs.microsoft.com/uwp/api/windows.media.core.mediasource)

mediasource.createfrommediaframesource

#### [mediasourceappserviceconnection](https://docs.microsoft.com/uwp/api/windows.media.core.mediasourceappserviceconnection)

mediasourceappserviceconnection <br> mediasourceappserviceconnection.initializemediastreamsourcerequested <br> mediasourceappserviceconnection.mediasourceappserviceconnection <br> mediasourceappserviceconnection.start

#### [sceneanalysiseffectframe](https://docs.microsoft.com/uwp/api/windows.media.core.sceneanalysiseffectframe)

sceneanalysiseffectframe.analysisrecommendation

#### [sceneanalysisrecommendation](https://docs.microsoft.com/uwp/api/windows.media.core.sceneanalysisrecommendation)

sceneanalysisrecommendation

#### [videostreamdescriptor](https://docs.microsoft.com/uwp/api/windows.media.core.videostreamdescriptor)

videostreamdescriptor.label

### [windows.media.dialprotocol](https://docs.microsoft.com/uwp/api/windows.media.dialprotocol)

#### [dialreceiverapp](https://docs.microsoft.com/uwp/api/windows.media.dialprotocol.dialreceiverapp)

dialreceiverapp <br> dialreceiverapp.current <br> dialreceiverapp.getadditionaldataasync <br> dialreceiverapp.setadditionaldataasync

### [windows.media.mediaproperties](https://docs.microsoft.com/uwp/api/windows.media.mediaproperties)

#### [mediaencodingprofile](https://docs.microsoft.com/uwp/api/windows.media.mediaproperties.mediaencodingprofile)

mediaencodingprofile.getaudiotracks <br> mediaencodingprofile.getvideotracks <br> mediaencodingprofile.setaudiotracks <br> mediaencodingprofile.setvideotracks

### [windows.media.speechsynthesis](https://docs.microsoft.com/uwp/api/windows.media.speechsynthesis)

#### [speechsynthesizer](https://docs.microsoft.com/uwp/api/windows.media.speechsynthesis.speechsynthesizer)

speechsynthesizer.trysetdefaultvoiceasync

#### [speechsynthesizeroptions](https://docs.microsoft.com/uwp/api/windows.media.speechsynthesis.speechsynthesizeroptions)

speechsynthesizeroptions.audiopitch <br> speechsynthesizeroptions.audiovolume <br> speechsynthesizeroptions.speakingrate

## windows.networking

### [windows.networking.backgroundtransfer](https://docs.microsoft.com/uwp/api/windows.networking.backgroundtransfer)

#### [backgroundtransferfilerange](https://docs.microsoft.com/uwp/api/windows.networking.backgroundtransfer.backgroundtransferfilerange)

backgroundtransferfilerange

#### [backgroundtransferrangesdownloadedeventargs](https://docs.microsoft.com/uwp/api/windows.networking.backgroundtransfer.backgroundtransferrangesdownloadedeventargs)

backgroundtransferrangesdownloadedeventargs <br> backgroundtransferrangesdownloadedeventargs.addedranges <br> backgroundtransferrangesdownloadedeventargs.getdeferral <br> backgroundtransferrangesdownloadedeventargs.wasdownloadrestarted

#### [downloadoperation](https://docs.microsoft.com/uwp/api/windows.networking.backgroundtransfer.downloadoperation)

downloadoperation.currentweberrorstatus <br> downloadoperation.getdownloadedranges <br> downloadoperation.getresultrandomaccessstreamreference <br> downloadoperation.israndomaccessrequired <br> downloadoperation.rangesdownloaded <br> downloadoperation.recoverableweberrorstatuses

### [windows.networking.connectivity](https://docs.microsoft.com/uwp/api/windows.networking.connectivity)

#### [connectionprofile](https://docs.microsoft.com/uwp/api/windows.networking.connectivity.connectionprofile)

connectionprofile.getprovidernetworkusageasync

#### [providernetworkusage](https://docs.microsoft.com/uwp/api/windows.networking.connectivity.providernetworkusage)

providernetworkusage <br> providernetworkusage.bytesreceived <br> providernetworkusage.bytessent <br> providernetworkusage.providerid

### [windows.networking.networkoperators](https://docs.microsoft.com/uwp/api/windows.networking.networkoperators)

#### [mobilebroadbandantennasar](https://docs.microsoft.com/uwp/api/windows.networking.networkoperators.mobilebroadbandantennasar)

mobilebroadbandantennasar <br> mobilebroadbandantennasar.antennaindex <br> mobilebroadbandantennasar.sarbackoffindex

#### [mobilebroadbandcellcdma](https://docs.microsoft.com/uwp/api/windows.networking.networkoperators.mobilebroadbandcellcdma)

mobilebroadbandcellcdma <br> mobilebroadbandcellcdma.basestationid <br> mobilebroadbandcellcdma.basestationlastbroadcastgpstime <br> mobilebroadbandcellcdma.basestationlatitude <br> mobilebroadbandcellcdma.basestationlongitude <br> mobilebroadbandcellcdma.basestationpncode <br> mobilebroadbandcellcdma.networkid <br> mobilebroadbandcellcdma.pilotsignalstrengthindb <br> mobilebroadbandcellcdma.systemid

#### [mobilebroadbandcellgsm](https://docs.microsoft.com/uwp/api/windows.networking.networkoperators.mobilebroadbandcellgsm)

mobilebroadbandcellgsm <br> mobilebroadbandcellgsm.basestationid <br> mobilebroadbandcellgsm.cellid <br> mobilebroadbandcellgsm.channelnumber <br> mobilebroadbandcellgsm.locationareacode <br> mobilebroadbandcellgsm.providerid <br> mobilebroadbandcellgsm.receivedsignalstrengthindbm <br> mobilebroadbandcellgsm.timingadvanceinbitperiods

#### [mobilebroadbandcelllte](https://docs.microsoft.com/uwp/api/windows.networking.networkoperators.mobilebroadbandcelllte)

mobilebroadbandcelllte <br> mobilebroadbandcelllte.cellid <br> mobilebroadbandcelllte.channelnumber <br> mobilebroadbandcelllte.physicalcellid <br> mobilebroadbandcelllte.providerid <br> mobilebroadbandcelllte.referencesignalreceivedpowerindbm <br> mobilebroadbandcelllte.referencesignalreceivedqualityindbm <br> mobilebroadbandcelllte.timingadvanceinbitperiods <br> mobilebroadbandcelllte.trackingareacode

#### [mobilebroadbandcellsinfo](https://docs.microsoft.com/uwp/api/windows.networking.networkoperators.mobilebroadbandcellsinfo)

mobilebroadbandcellsinfo <br> mobilebroadbandcellsinfo.neighboringcellscdma <br> mobilebroadbandcellsinfo.neighboringcellsgsm <br> mobilebroadbandcellsinfo.neighboringcellslte <br> mobilebroadbandcellsinfo.neighboringcellstdscdma <br> mobilebroadbandcellsinfo.neighboringcellsumts <br> mobilebroadbandcellsinfo.servingcellscdma <br> mobilebroadbandcellsinfo.servingcellsgsm <br> mobilebroadbandcellsinfo.servingcellslte <br> mobilebroadbandcellsinfo.servingcellstdscdma <br> mobilebroadbandcellsinfo.servingcellsumts

#### [mobilebroadbandcelltdscdma](https://docs.microsoft.com/uwp/api/windows.networking.networkoperators.mobilebroadbandcelltdscdma)

mobilebroadbandcelltdscdma <br> mobilebroadbandcelltdscdma.cellid <br> mobilebroadbandcelltdscdma.cellparameterid <br> mobilebroadbandcelltdscdma.channelnumber <br> mobilebroadbandcelltdscdma.locationareacode <br> mobilebroadbandcelltdscdma.pathlossindb <br> mobilebroadbandcelltdscdma.providerid <br> mobilebroadbandcelltdscdma.receivedsignalcodepowerindbm <br> mobilebroadbandcelltdscdma.timingadvanceinbitperiods

#### [mobilebroadbandcellumts](https://docs.microsoft.com/uwp/api/windows.networking.networkoperators.mobilebroadbandcellumts)

mobilebroadbandcellumts <br> mobilebroadbandcellumts.cellid <br> mobilebroadbandcellumts.channelnumber <br> mobilebroadbandcellumts.locationareacode <br> mobilebroadbandcellumts.pathlossindb <br> mobilebroadbandcellumts.primaryscramblingcode <br> mobilebroadbandcellumts.providerid <br> mobilebroadbandcellumts.receivedsignalcodepowerindbm <br> mobilebroadbandcellumts.signaltonoiseratioindb

#### [mobilebroadbandmodem](https://docs.microsoft.com/uwp/api/windows.networking.networkoperators.mobilebroadbandmodem)

mobilebroadbandmodem.getispassthroughenabledasync <br> mobilebroadbandmodem.setispassthroughenabledasync

#### [mobilebroadbandmodemconfiguration](https://docs.microsoft.com/uwp/api/windows.networking.networkoperators.mobilebroadbandmodemconfiguration)

mobilebroadbandmodemconfiguration.sarmanager

#### [mobilebroadbandmodemstatus](https://docs.microsoft.com/uwp/api/windows.networking.networkoperators.mobilebroadbandmodemstatus)

mobilebroadbandmodemstatus

#### [mobilebroadbandnetwork](https://docs.microsoft.com/uwp/api/windows.networking.networkoperators.mobilebroadbandnetwork)

mobilebroadbandnetwork.getcellsinfoasync

#### [mobilebroadbandsarmanager](https://docs.microsoft.com/uwp/api/windows.networking.networkoperators.mobilebroadbandsarmanager)

mobilebroadbandsarmanager <br> mobilebroadbandsarmanager.antennas <br> mobilebroadbandsarmanager.disablebackoffasync <br> mobilebroadbandsarmanager.enablebackoffasync <br> mobilebroadbandsarmanager.getistransmittingasync <br> mobilebroadbandsarmanager.hysteresistimerperiod <br> mobilebroadbandsarmanager.isbackoffenabled <br> mobilebroadbandsarmanager.issarcontrolledbyhardware <br> mobilebroadbandsarmanager.iswifihardwareintegrated <br> mobilebroadbandsarmanager.revertsartohardwarecontrolasync <br> mobilebroadbandsarmanager.setconfigurationasync <br> mobilebroadbandsarmanager.settransmissionstatechangedhysteresisasync <br> mobilebroadbandsarmanager.starttransmissionstatemonitoring <br> mobilebroadbandsarmanager.stoptransmissionstatemonitoring <br> mobilebroadbandsarmanager.transmissionstatechanged

#### [mobilebroadbandtransmissionstatechangedeventargs](https://docs.microsoft.com/uwp/api/windows.networking.networkoperators.mobilebroadbandtransmissionstatechangedeventargs)

mobilebroadbandtransmissionstatechangedeventargs <br> mobilebroadbandtransmissionstatechangedeventargs.istransmitting

### [windows.networking.sockets](https://docs.microsoft.com/uwp/api/windows.networking.sockets)

#### [messagewebsocketcontrol](https://docs.microsoft.com/uwp/api/windows.networking.sockets.messagewebsocketcontrol)

messagewebsocketcontrol.actualunsolicitedponginterval <br> messagewebsocketcontrol.clientcertificate <br> messagewebsocketcontrol.desiredunsolicitedponginterval <br> messagewebsocketcontrol.receivemode

#### [messagewebsocketmessagereceivedeventargs](https://docs.microsoft.com/uwp/api/windows.networking.sockets.messagewebsocketmessagereceivedeventargs)

messagewebsocketmessagereceivedeventargs.ismessagecomplete

#### [messagewebsocketreceivemode](https://docs.microsoft.com/uwp/api/windows.networking.sockets.messagewebsocketreceivemode)

messagewebsocketreceivemode

#### [streamsocketcontrol](https://docs.microsoft.com/uwp/api/windows.networking.sockets.streamsocketcontrol)

streamsocketcontrol.minprotectionlevel

#### [streamwebsocketcontrol](https://docs.microsoft.com/uwp/api/windows.networking.sockets.streamwebsocketcontrol)

streamwebsocketcontrol.actualunsolicitedponginterval <br> streamwebsocketcontrol.clientcertificate <br> streamwebsocketcontrol.desiredunsolicitedponginterval

## windows.phone

### [windows.phone.networking.voip](https://docs.microsoft.com/uwp/api/windows.phone.networking.voip)

#### [voipcallcoordinator](https://docs.microsoft.com/uwp/api/windows.phone.networking.voip.voipcallcoordinator)

voipcallcoordinator.setupnewacceptedcall

#### [voipphonecall](https://docs.microsoft.com/uwp/api/windows.phone.networking.voip.voipphonecall)

voipphonecall.tryshowappui

## windows.security

### [windows.security.authentication.web.provider](https://docs.microsoft.com/uwp/api/windows.security.authentication.web.provider)

#### [webaccountmanager](https://docs.microsoft.com/uwp/api/windows.security.authentication.web.provider.webaccountmanager)

webaccountmanager.invalidateappcacheforaccountasync <br> webaccountmanager.invalidateappcacheforallaccountsasync

### [windows.security.enterprisedata](https://docs.microsoft.com/uwp/api/windows.security.enterprisedata)

#### [fileprotectioninfo](https://docs.microsoft.com/uwp/api/windows.security.enterprisedata.fileprotectioninfo)

fileprotectioninfo.isprotectwhileopensupported

## windows.services

### [windows.services.maps.guidance](https://docs.microsoft.com/uwp/api/windows.services.maps.guidance)

#### [guidanceroadsegment](https://docs.microsoft.com/uwp/api/windows.services.maps.guidance.guidanceroadsegment)

guidanceroadsegment.isscenic

### [windows.services.maps.localsearch](https://docs.microsoft.com/uwp/api/windows.services.maps.localsearch)

#### [placeinfohelper](https://docs.microsoft.com/uwp/api/windows.services.maps.localsearch.placeinfohelper)

placeinfohelper <br> placeinfohelper.createfromlocallocation

### [windows.services.maps](https://docs.microsoft.com/uwp/api/windows.services.maps)

#### [maproute](https://docs.microsoft.com/uwp/api/windows.services.maps.maproute)

maproute.isscenic

#### [placeinfo](https://docs.microsoft.com/uwp/api/windows.services.maps.placeinfo)

placeinfo <br> placeinfo.create <br> placeinfo.create <br> placeinfo.createfromidentifier <br> placeinfo.createfromidentifier <br> placeinfo.createfrommaplocation <br> placeinfo.displayaddress <br> placeinfo.displayname <br> placeinfo.geoshape <br> placeinfo.identifier <br> placeinfo.isshowsupported <br> placeinfo.show <br> placeinfo.show

#### [placeinfocreateoptions](https://docs.microsoft.com/uwp/api/windows.services.maps.placeinfocreateoptions)

placeinfocreateoptions <br> placeinfocreateoptions.displayaddress <br> placeinfocreateoptions.displayname <br> placeinfocreateoptions.placeinfocreateoptions

## windows.storage

### [windows.storage.provider](https://docs.microsoft.com/uwp/api/windows.storage.provider)

#### [hydrationpolicymodifier](https://docs.microsoft.com/uwp/api/windows.storage.provider.hydrationpolicymodifier)

hydrationpolicymodifier

#### [insyncpolicy](https://docs.microsoft.com/uwp/api/windows.storage.provider.insyncpolicy)

insyncpolicy

#### [istorageprovideritempropertysource](https://docs.microsoft.com/uwp/api/windows.storage.provider.istorageprovideritempropertysource)

istorageprovideritempropertysource <br> istorageprovideritempropertysource.getitemproperties

#### [istorageproviderpropertycapabilities](https://docs.microsoft.com/uwp/api/windows.storage.provider.istorageproviderpropertycapabilities)

istorageproviderpropertycapabilities <br> istorageproviderpropertycapabilities.ispropertysupported

#### [storageprovideritemproperties](https://docs.microsoft.com/uwp/api/windows.storage.provider.storageprovideritemproperties)

storageprovideritemproperties <br> storageprovideritemproperties.setasync

#### [storageprovideritemproperty](https://docs.microsoft.com/uwp/api/windows.storage.provider.storageprovideritemproperty)

storageprovideritemproperty <br> storageprovideritemproperty.iconresource <br> storageprovideritemproperty.id <br> storageprovideritemproperty.storageprovideritemproperty <br> storageprovideritemproperty.value

#### [storageprovideritempropertydefinition](https://docs.microsoft.com/uwp/api/windows.storage.provider.storageprovideritempropertydefinition)

storageprovideritempropertydefinition <br> storageprovideritempropertydefinition.displaynameresource <br> storageprovideritempropertydefinition.id <br> storageprovideritempropertydefinition.storageprovideritempropertydefinition

#### [storageprovidersyncrootinfo](https://docs.microsoft.com/uwp/api/windows.storage.provider.storageprovidersyncrootinfo)

storageprovidersyncrootinfo <br> storageprovidersyncrootinfo.allowpinning <br> storageprovidersyncrootinfo.context <br> storageprovidersyncrootinfo.displaynameresource <br> storageprovidersyncrootinfo.hydrationpolicy <br> storageprovidersyncrootinfo.hydrationpolicymodifier <br> storageprovidersyncrootinfo.iconresource <br> storageprovidersyncrootinfo.id <br> storageprovidersyncrootinfo.insyncpolicy <br> storageprovidersyncrootinfo.path <br> storageprovidersyncrootinfo.populationpolicy <br> storageprovidersyncrootinfo.protectionmode <br> storageprovidersyncrootinfo.recyclebinuri <br> storageprovidersyncrootinfo.showsiblingsasgroup <br> storageprovidersyncrootinfo.storageprovideritempropertydefinitions <br> storageprovidersyncrootinfo.storageprovidersyncrootinfo <br> storageprovidersyncrootinfo.version

#### [storageprovidersyncrootmanager](https://docs.microsoft.com/uwp/api/windows.storage.provider.storageprovidersyncrootmanager)

storageprovidersyncrootmanager <br> storageprovidersyncrootmanager.getcurrentsyncroots <br> storageprovidersyncrootmanager.getsyncrootinformationforfolder <br> storageprovidersyncrootmanager.getsyncrootinformationforid <br> storageprovidersyncrootmanager.register <br> storageprovidersyncrootmanager.unregister

### [windows.storage.streams](https://docs.microsoft.com/uwp/api/windows.storage.streams)

#### [fileopendisposition](https://docs.microsoft.com/uwp/api/windows.storage.streams.fileopendisposition)

fileopendisposition

#### [filerandomaccessstream](https://docs.microsoft.com/uwp/api/windows.storage.streams.filerandomaccessstream)

filerandomaccessstream.openasync <br> filerandomaccessstream.openasync <br> filerandomaccessstream.openforuserasync <br> filerandomaccessstream.openforuserasync <br> filerandomaccessstream.opentransactedwriteasync <br> filerandomaccessstream.opentransactedwriteasync <br> filerandomaccessstream.opentransactedwriteforuserasync <br> filerandomaccessstream.opentransactedwriteforuserasync

### [windows.storage](https://docs.microsoft.com/uwp/api/windows.storage)

#### [storageprovider](https://docs.microsoft.com/uwp/api/windows.storage.storageprovider)

storageprovider.ispropertysupportedforpartialfileasync

## windows.system

### [windows.system.diagnostics](https://docs.microsoft.com/uwp/api/windows.system.diagnostics)

#### [diagnosticactionresult](https://docs.microsoft.com/uwp/api/windows.system.diagnostics.diagnosticactionresult)

diagnosticactionresult <br> diagnosticactionresult.extendederror <br> diagnosticactionresult.results

#### [diagnosticactionstate](https://docs.microsoft.com/uwp/api/windows.system.diagnostics.diagnosticactionstate)

diagnosticactionstate

#### [diagnosticinvoker](https://docs.microsoft.com/uwp/api/windows.system.diagnostics.diagnosticinvoker)

diagnosticinvoker <br> diagnosticinvoker.getdefault <br> diagnosticinvoker.getforuser <br> diagnosticinvoker.issupported <br> diagnosticinvoker.rundiagnosticactionasync

#### [processdiagnosticinfo](https://docs.microsoft.com/uwp/api/windows.system.diagnostics.processdiagnosticinfo)

processdiagnosticinfo.getappdiagnosticinfos

### [windows.system.profile.systemmanufacturers](https://docs.microsoft.com/uwp/api/windows.system.profile.systemmanufacturers)

#### [oemsupportinfo](https://docs.microsoft.com/uwp/api/windows.system.profile.systemmanufacturers.oemsupportinfo)

oemsupportinfo <br> oemsupportinfo.supportapplink <br> oemsupportinfo.supportlink <br> oemsupportinfo.supportprovider

#### [systemsupportinfo](https://docs.microsoft.com/uwp/api/windows.system.profile.systemmanufacturers.systemsupportinfo)

systemsupportinfo <br> systemsupportinfo.localsystemedition <br> systemsupportinfo.oemsupportinfo

### [windows.system.remotesystems](https://docs.microsoft.com/uwp/api/windows.system.remotesystems)

#### [remotesystem](https://docs.microsoft.com/uwp/api/windows.system.remotesystems.remotesystem)

remotesystem.manufacturerdisplayname <br> remotesystem.modeldisplayname

#### [remotesystemkinds](https://docs.microsoft.com/uwp/api/windows.system.remotesystems.remotesystemkinds)

remotesystemkinds.iot <br> remotesystemkinds.laptop <br> remotesystemkinds.tablet

### [windows.system](https://docs.microsoft.com/uwp/api/windows.system)

#### [appdiagnosticinfo](https://docs.microsoft.com/uwp/api/windows.system.appdiagnosticinfo)

appdiagnosticinfo.requestaccessasync <br> appdiagnosticinfo.requestinfoforappasync

#### [appmemoryreport](https://docs.microsoft.com/uwp/api/windows.system.appmemoryreport)

appmemoryreport.expectedtotalcommitlimit

#### [appresourcegroupbackgroundtaskreport](https://docs.microsoft.com/uwp/api/windows.system.appresourcegroupbackgroundtaskreport)

appresourcegroupbackgroundtaskreport <br> appresourcegroupbackgroundtaskreport.entrypoint <br> appresourcegroupbackgroundtaskreport.name <br> appresourcegroupbackgroundtaskreport.taskid <br> appresourcegroupbackgroundtaskreport.trigger

#### [appresourcegroupenergyquotastate](https://docs.microsoft.com/uwp/api/windows.system.appresourcegroupenergyquotastate)

appresourcegroupenergyquotastate

#### [appresourcegroupexecutionstate](https://docs.microsoft.com/uwp/api/windows.system.appresourcegroupexecutionstate)

appresourcegroupexecutionstate

#### [appresourcegroupinfo](https://docs.microsoft.com/uwp/api/windows.system.appresourcegroupinfo)

appresourcegroupinfo <br> appresourcegroupinfo.getbackgroundtaskreports <br> appresourcegroupinfo.getmemoryreport <br> appresourcegroupinfo.getprocessdiagnosticinfos <br> appresourcegroupinfo.getstatereport <br> appresourcegroupinfo.instanceid <br> appresourcegroupinfo.isshared

#### [appresourcegroupinfowatcher](https://docs.microsoft.com/uwp/api/windows.system.appresourcegroupinfowatcher)

appresourcegroupinfowatcher <br> appresourcegroupinfowatcher.added <br> appresourcegroupinfowatcher.enumerationcompleted <br> appresourcegroupinfowatcher.executionstatechanged <br> appresourcegroupinfowatcher.removed <br> appresourcegroupinfowatcher.start <br> appresourcegroupinfowatcher.status <br> appresourcegroupinfowatcher.stop <br> appresourcegroupinfowatcher.stopped

#### [appresourcegroupinfowatchereventargs](https://docs.microsoft.com/uwp/api/windows.system.appresourcegroupinfowatchereventargs)

appresourcegroupinfowatchereventargs <br> appresourcegroupinfowatchereventargs.appdiagnosticinfos <br> appresourcegroupinfowatchereventargs.appresourcegroupinfo

#### [appresourcegroupinfowatcherexecutionstatechangedeventargs](https://docs.microsoft.com/uwp/api/windows.system.appresourcegroupinfowatcherexecutionstatechangedeventargs)

appresourcegroupinfowatcherexecutionstatechangedeventargs <br> appresourcegroupinfowatcherexecutionstatechangedeventargs.appdiagnosticinfos <br> appresourcegroupinfowatcherexecutionstatechangedeventargs.appresourcegroupinfo

#### [appresourcegroupinfowatcherstatus](https://docs.microsoft.com/uwp/api/windows.system.appresourcegroupinfowatcherstatus)

appresourcegroupinfowatcherstatus

#### [appresourcegroupmemoryreport](https://docs.microsoft.com/uwp/api/windows.system.appresourcegroupmemoryreport)

appresourcegroupmemoryreport <br> appresourcegroupmemoryreport.commitusagelevel <br> appresourcegroupmemoryreport.commitusagelimit <br> appresourcegroupmemoryreport.privatecommitusage <br> appresourcegroupmemoryreport.totalcommitusage

#### [appresourcegroupstatereport](https://docs.microsoft.com/uwp/api/windows.system.appresourcegroupstatereport)

appresourcegroupstatereport <br> appresourcegroupstatereport.energyquotastate <br> appresourcegroupstatereport.executionstate

#### [datetimesettings](https://docs.microsoft.com/uwp/api/windows.system.datetimesettings)

datetimesettings <br> datetimesettings.setsystemdatetime

#### [diagnosticaccessstatus](https://docs.microsoft.com/uwp/api/windows.system.diagnosticaccessstatus)

diagnosticaccessstatus

#### [dispatcherqueue](https://docs.microsoft.com/uwp/api/windows.system.dispatcherqueue)

dispatcherqueue.shutdowncompleted <br> dispatcherqueue.shutdownstarting

#### [dispatcherqueuecontroller](https://docs.microsoft.com/uwp/api/windows.system.dispatcherqueuecontroller)

dispatcherqueuecontroller.createondedicatedthread

#### [dispatcherqueueshutdownstartingeventargs](https://docs.microsoft.com/uwp/api/windows.system.dispatcherqueueshutdownstartingeventargs)

dispatcherqueueshutdownstartingeventargs <br> dispatcherqueueshutdownstartingeventargs.getdeferral

#### [dispatcherqueuetimer](https://docs.microsoft.com/uwp/api/windows.system.dispatcherqueuetimer)

dispatcherqueuetimer.isrunning

#### [memorymanager](https://docs.microsoft.com/uwp/api/windows.system.memorymanager)

memorymanager.expectedappmemoryusagelimit

## windows.ui

### [windows.ui.composition.effects](https://docs.microsoft.com/uwp/api/windows.ui.composition.effects)

#### [scenelightingeffect](https://docs.microsoft.com/uwp/api/windows.ui.composition.effects.scenelightingeffect)

scenelightingeffect.reflectancemodel

#### [scenelightingeffectreflectancemodel](https://docs.microsoft.com/uwp/api/windows.ui.composition.effects.scenelightingeffectreflectancemodel)

scenelightingeffectreflectancemodel

### [windows.ui.composition.interactions](https://docs.microsoft.com/uwp/api/windows.ui.composition.interactions)

#### [interactiontracker](https://docs.microsoft.com/uwp/api/windows.ui.composition.interactions.interactiontracker)

interactiontracker.configurevector2positioninertiamodifiers

#### [interactiontrackerinertianaturalmotion](https://docs.microsoft.com/uwp/api/windows.ui.composition.interactions.interactiontrackerinertianaturalmotion)

interactiontrackerinertianaturalmotion <br> interactiontrackerinertianaturalmotion.condition <br> interactiontrackerinertianaturalmotion.create <br> interactiontrackerinertianaturalmotion.naturalmotion

#### [interactiontrackervector2inertiamodifier](https://docs.microsoft.com/uwp/api/windows.ui.composition.interactions.interactiontrackervector2inertiamodifier)

interactiontrackervector2inertiamodifier

#### [interactiontrackervector2inertianaturalmotion](https://docs.microsoft.com/uwp/api/windows.ui.composition.interactions.interactiontrackervector2inertianaturalmotion)

interactiontrackervector2inertianaturalmotion <br> interactiontrackervector2inertianaturalmotion.condition <br> interactiontrackervector2inertianaturalmotion.create <br> interactiontrackervector2inertianaturalmotion.naturalmotion

### [windows.ui.composition](https://docs.microsoft.com/uwp/api/windows.ui.composition)

#### [compositionanimation](https://docs.microsoft.com/uwp/api/windows.ui.composition.compositionanimation)

compositionanimation.initialvalueexpressions

#### [compositioncolorgradientstop](https://docs.microsoft.com/uwp/api/windows.ui.composition.compositioncolorgradientstop)

compositioncolorgradientstop <br> compositioncolorgradientstop.color <br> compositioncolorgradientstop.offset

#### [compositioncolorgradientstopcollection](https://docs.microsoft.com/uwp/api/windows.ui.composition.compositioncolorgradientstopcollection)

compositioncolorgradientstopcollection <br> compositioncolorgradientstopcollection.append <br> compositioncolorgradientstopcollection.clear <br> compositioncolorgradientstopcollection.first <br> compositioncolorgradientstopcollection.getat <br> compositioncolorgradientstopcollection.getmany <br> compositioncolorgradientstopcollection.getview <br> compositioncolorgradientstopcollection.indexof <br> compositioncolorgradientstopcollection.insertat <br> compositioncolorgradientstopcollection.removeat <br> compositioncolorgradientstopcollection.removeatend <br> compositioncolorgradientstopcollection.replaceall <br> compositioncolorgradientstopcollection.setat <br> compositioncolorgradientstopcollection.size

#### [compositiongradientbrush](https://docs.microsoft.com/uwp/api/windows.ui.composition.compositiongradientbrush)

compositiongradientbrush <br> compositiongradientbrush.anchorpoint <br> compositiongradientbrush.centerpoint <br> compositiongradientbrush.colorstops <br> compositiongradientbrush.extendmode <br> compositiongradientbrush.interpolationspace <br> compositiongradientbrush.offset <br> compositiongradientbrush.rotationangle <br> compositiongradientbrush.rotationangleindegrees <br> compositiongradientbrush.scale <br> compositiongradientbrush.transformmatrix

#### [compositiongradientextendmode](https://docs.microsoft.com/uwp/api/windows.ui.composition.compositiongradientextendmode)

compositiongradientextendmode

#### [compositionlight](https://docs.microsoft.com/uwp/api/windows.ui.composition.compositionlight)

compositionlight.exclusionsfromtargets

#### [compositionlineargradientbrush](https://docs.microsoft.com/uwp/api/windows.ui.composition.compositionlineargradientbrush)

compositionlineargradientbrush <br> compositionlineargradientbrush.endpoint <br> compositionlineargradientbrush.startpoint

#### [compositionobject](https://docs.microsoft.com/uwp/api/windows.ui.composition.compositionobject)

compositionobject.dispatcherqueue

#### [compositor](https://docs.microsoft.com/uwp/api/windows.ui.composition.compositor)

compositor.createcolorgradientstop <br> compositor.createcolorgradientstop <br> compositor.createlineargradientbrush <br> compositor.createspringscalaranimation <br> compositor.createspringvector2animation <br> compositor.createspringvector3animation

#### [initialvalueexpressioncollection](https://docs.microsoft.com/uwp/api/windows.ui.composition.initialvalueexpressioncollection)

initialvalueexpressioncollection <br> initialvalueexpressioncollection.clear <br> initialvalueexpressioncollection.first <br> initialvalueexpressioncollection.getview <br> initialvalueexpressioncollection.haskey <br> initialvalueexpressioncollection.insert <br> initialvalueexpressioncollection.lookup <br> initialvalueexpressioncollection.remove <br> initialvalueexpressioncollection.size

#### [layervisual](https://docs.microsoft.com/uwp/api/windows.ui.composition.layervisual)

layervisual.shadow

#### [naturalmotionanimation](https://docs.microsoft.com/uwp/api/windows.ui.composition.naturalmotionanimation)

naturalmotionanimation <br> naturalmotionanimation.delaybehavior <br> naturalmotionanimation.delaytime <br> naturalmotionanimation.stopbehavior

#### [scalarnaturalmotionanimation](https://docs.microsoft.com/uwp/api/windows.ui.composition.scalarnaturalmotionanimation)

scalarnaturalmotionanimation <br> scalarnaturalmotionanimation.finalvalue <br> scalarnaturalmotionanimation.initialvalue <br> scalarnaturalmotionanimation.initialvelocity

#### [springscalarnaturalmotionanimation](https://docs.microsoft.com/uwp/api/windows.ui.composition.springscalarnaturalmotionanimation)

springscalarnaturalmotionanimation <br> springscalarnaturalmotionanimation.dampingratio <br> springscalarnaturalmotionanimation.period

#### [springvector2naturalmotionanimation](https://docs.microsoft.com/uwp/api/windows.ui.composition.springvector2naturalmotionanimation)

springvector2naturalmotionanimation <br> springvector2naturalmotionanimation.dampingratio <br> springvector2naturalmotionanimation.period

#### [springvector3naturalmotionanimation](https://docs.microsoft.com/uwp/api/windows.ui.composition.springvector3naturalmotionanimation)

springvector3naturalmotionanimation <br> springvector3naturalmotionanimation.dampingratio <br> springvector3naturalmotionanimation.period

#### [vector2naturalmotionanimation](https://docs.microsoft.com/uwp/api/windows.ui.composition.vector2naturalmotionanimation)

vector2naturalmotionanimation <br> vector2naturalmotionanimation.finalvalue <br> vector2naturalmotionanimation.initialvalue <br> vector2naturalmotionanimation.initialvelocity

#### [vector3naturalmotionanimation](https://docs.microsoft.com/uwp/api/windows.ui.composition.vector3naturalmotionanimation)

vector3naturalmotionanimation <br> vector3naturalmotionanimation.finalvalue <br> vector3naturalmotionanimation.initialvalue <br> vector3naturalmotionanimation.initialvelocity

### [windows.ui.core](https://docs.microsoft.com/uwp/api/windows.ui.core)

#### [corewindow](https://docs.microsoft.com/uwp/api/windows.ui.core.corewindow)

corewindow.activationmode

#### [corewindowactivationmode](https://docs.microsoft.com/uwp/api/windows.ui.core.corewindowactivationmode)

corewindowactivationmode

### [windows.ui.input.inking.core](https://docs.microsoft.com/uwp/api/windows.ui.input.inking.core)

#### [coreincrementalinkstroke](https://docs.microsoft.com/uwp/api/windows.ui.input.inking.core.coreincrementalinkstroke)

coreincrementalinkstroke <br> coreincrementalinkstroke.appendinkpoints <br> coreincrementalinkstroke.boundingrect <br> coreincrementalinkstroke.coreincrementalinkstroke <br> coreincrementalinkstroke.createinkstroke <br> coreincrementalinkstroke.drawingattributes <br> coreincrementalinkstroke.pointtransform

#### [coreinkpresenterhost](https://docs.microsoft.com/uwp/api/windows.ui.input.inking.core.coreinkpresenterhost)

coreinkpresenterhost <br> coreinkpresenterhost.coreinkpresenterhost <br> coreinkpresenterhost.inkpresenter <br> coreinkpresenterhost.rootvisual

### [windows.ui.input.preview.injection](https://docs.microsoft.com/uwp/api/windows.ui.input.preview.injection)

#### [injectedinputgamepadinfo](https://docs.microsoft.com/uwp/api/windows.ui.input.preview.injection.injectedinputgamepadinfo)

injectedinputgamepadinfo <br> injectedinputgamepadinfo.buttons <br> injectedinputgamepadinfo.injectedinputgamepadinfo <br> injectedinputgamepadinfo.injectedinputgamepadinfo <br> injectedinputgamepadinfo.leftthumbstickx <br> injectedinputgamepadinfo.leftthumbsticky <br> injectedinputgamepadinfo.lefttrigger <br> injectedinputgamepadinfo.rightthumbstickx <br> injectedinputgamepadinfo.rightthumbsticky <br> injectedinputgamepadinfo.righttrigger

#### [inputinjector](https://docs.microsoft.com/uwp/api/windows.ui.input.preview.injection.inputinjector)

inputinjector.initializegamepadinjection <br> inputinjector.injectgamepadinput <br> inputinjector.trycreateforappbroadcastonly <br> inputinjector.uninitializegamepadinjection

### [windows.ui.input.spatial](https://docs.microsoft.com/uwp/api/windows.ui.input.spatial)

#### [spatialinteractioncontroller](https://docs.microsoft.com/uwp/api/windows.ui.input.spatial.spatialinteractioncontroller)

spatialinteractioncontroller.trygetrenderablemodelasync

#### [spatialinteractionsourcelocation](https://docs.microsoft.com/uwp/api/windows.ui.input.spatial.spatialinteractionsourcelocation)

spatialinteractionsourcelocation.angularvelocity <br> spatialinteractionsourcelocation.positionquality <br> spatialinteractionsourcelocation.sourcepointerpose

#### [spatialinteractionsourcepositionquality](https://docs.microsoft.com/uwp/api/windows.ui.input.spatial.spatialinteractionsourcepositionquality)

spatialinteractionsourcepositionquality

#### [spatialpointerinteractionsourcepose](https://docs.microsoft.com/uwp/api/windows.ui.input.spatial.spatialpointerinteractionsourcepose)

spatialpointerinteractionsourcepose.orientation <br> spatialpointerinteractionsourcepose.positionquality

### [windows.ui.input](https://docs.microsoft.com/uwp/api/windows.ui.input)

#### [radialcontrollerconfiguration](https://docs.microsoft.com/uwp/api/windows.ui.input.radialcontrollerconfiguration)

radialcontrollerconfiguration.appcontroller <br> radialcontrollerconfiguration.isappcontrollerenabled

### [windows.ui.shell](https://docs.microsoft.com/uwp/api/windows.ui.shell)

#### [adaptivecardbuilder](https://docs.microsoft.com/uwp/api/windows.ui.shell.adaptivecardbuilder)

adaptivecardbuilder <br> adaptivecardbuilder.createadaptivecardfromjson

#### [iadaptivecard](https://docs.microsoft.com/uwp/api/windows.ui.shell.iadaptivecard)

iadaptivecard <br> iadaptivecard.tojson

#### [iadaptivecardbuilderstatics](https://docs.microsoft.com/uwp/api/windows.ui.shell.iadaptivecardbuilderstatics)

iadaptivecardbuilderstatics <br> iadaptivecardbuilderstatics.createadaptivecardfromjson

#### [taskbarmanager](https://docs.microsoft.com/uwp/api/windows.ui.shell.taskbarmanager)

taskbarmanager <br> taskbarmanager.getdefault <br> taskbarmanager.isapplistentrypinnedasync <br> taskbarmanager.iscurrentapppinnedasync <br> taskbarmanager.ispinningallowed <br> taskbarmanager.issupported <br> taskbarmanager.requestpinapplistentryasync <br> taskbarmanager.requestpincurrentappasync

#### [windows](https://docs.microsoft.com/uwp/api/windows.ui.shell.windows)

windows.ui.shell

### [windows.ui.startscreen](https://docs.microsoft.com/uwp/api/windows.ui.startscreen)

#### [secondarytilevisualelements](https://docs.microsoft.com/uwp/api/windows.ui.startscreen.secondarytilevisualelements)

secondarytilevisualelements.mixedrealitymodel

#### [tilemixedrealitymodel](https://docs.microsoft.com/uwp/api/windows.ui.startscreen.tilemixedrealitymodel)

tilemixedrealitymodel <br> tilemixedrealitymodel.boundingbox <br> tilemixedrealitymodel.uri

### [windows.ui.viewmanagement.core](https://docs.microsoft.com/uwp/api/windows.ui.viewmanagement.core)

#### [coreinputview](https://docs.microsoft.com/uwp/api/windows.ui.viewmanagement.core.coreinputview)

coreinputview <br> coreinputview.getcoreinputviewocclusions <br> coreinputview.getforcurrentview <br> coreinputview.occlusionschanged <br> coreinputview.tryhideprimaryview <br> coreinputview.tryshowprimaryview

#### [coreinputviewocclusion](https://docs.microsoft.com/uwp/api/windows.ui.viewmanagement.core.coreinputviewocclusion)

coreinputviewocclusion <br> coreinputviewocclusion.occludingrect <br> coreinputviewocclusion.occlusionkind

#### [coreinputviewocclusionkind](https://docs.microsoft.com/uwp/api/windows.ui.viewmanagement.core.coreinputviewocclusionkind)

coreinputviewocclusionkind

#### [coreinputviewocclusionschangedeventargs](https://docs.microsoft.com/uwp/api/windows.ui.viewmanagement.core.coreinputviewocclusionschangedeventargs)

coreinputviewocclusionschangedeventargs <br> coreinputviewocclusionschangedeventargs.handled <br> coreinputviewocclusionschangedeventargs.occlusions

#### [windows](https://docs.microsoft.com/uwp/api/windows.ui.viewmanagement.core.windows)

windows.ui.viewmanagement.core

### [windows.ui.webui](https://docs.microsoft.com/uwp/api/windows.ui.webui)

#### [webuiapplication](https://docs.microsoft.com/uwp/api/windows.ui.webui.webuiapplication)

webuiapplication.requestrestartasync <br> webuiapplication.requestrestartforuserasync

#### [webuicommandlineactivatedeventargs](https://docs.microsoft.com/uwp/api/windows.ui.webui.webuicommandlineactivatedeventargs)

webuicommandlineactivatedeventargs <br> webuicommandlineactivatedeventargs.activatedoperation <br> webuicommandlineactivatedeventargs.kind <br> webuicommandlineactivatedeventargs.operation <br> webuicommandlineactivatedeventargs.previousexecutionstate <br> webuicommandlineactivatedeventargs.splashscreen <br> webuicommandlineactivatedeventargs.user

#### [webuistartuptaskactivatedeventargs](https://docs.microsoft.com/uwp/api/windows.ui.webui.webuistartuptaskactivatedeventargs)

webuistartuptaskactivatedeventargs <br> webuistartuptaskactivatedeventargs.kind <br> webuistartuptaskactivatedeventargs.previousexecutionstate <br> webuistartuptaskactivatedeventargs.splashscreen <br> webuistartuptaskactivatedeventargs.taskid <br> webuistartuptaskactivatedeventargs.user

### [windows.ui.xaml.automation.peers](https://docs.microsoft.com/uwp/api/windows.ui.xaml.automation.peers)

#### [automationnotificationkind](https://docs.microsoft.com/uwp/api/windows.ui.xaml.automation.peers.automationnotificationkind)

automationnotificationkind

#### [automationnotificationprocessing](https://docs.microsoft.com/uwp/api/windows.ui.xaml.automation.peers.automationnotificationprocessing)

automationnotificationprocessing

#### [automationpeer](https://docs.microsoft.com/uwp/api/windows.ui.xaml.automation.peers.automationpeer)

automationpeer.raisenotificationevent

#### [colorpickersliderautomationpeer](https://docs.microsoft.com/uwp/api/windows.ui.xaml.automation.peers.colorpickersliderautomationpeer)

colorpickersliderautomationpeer <br> colorpickersliderautomationpeer.colorpickersliderautomationpeer

#### [colorspectrumautomationpeer](https://docs.microsoft.com/uwp/api/windows.ui.xaml.automation.peers.colorspectrumautomationpeer)

colorspectrumautomationpeer <br> colorspectrumautomationpeer.colorspectrumautomationpeer

#### [navigationviewitemautomationpeer](https://docs.microsoft.com/uwp/api/windows.ui.xaml.automation.peers.navigationviewitemautomationpeer)

navigationviewitemautomationpeer <br> navigationviewitemautomationpeer.navigationviewitemautomationpeer

#### [personpictureautomationpeer](https://docs.microsoft.com/uwp/api/windows.ui.xaml.automation.peers.personpictureautomationpeer)

personpictureautomationpeer <br> personpictureautomationpeer.personpictureautomationpeer

#### [ratingcontrolautomationpeer](https://docs.microsoft.com/uwp/api/windows.ui.xaml.automation.peers.ratingcontrolautomationpeer)

ratingcontrolautomationpeer <br> ratingcontrolautomationpeer.ratingcontrolautomationpeer

#### [treeviewitemautomationpeer](https://docs.microsoft.com/uwp/api/windows.ui.xaml.automation.peers.treeviewitemautomationpeer)

treeviewitemautomationpeer <br> treeviewitemautomationpeer.treeviewitemautomationpeer

#### [treeviewlistautomationpeer](https://docs.microsoft.com/uwp/api/windows.ui.xaml.automation.peers.treeviewlistautomationpeer)

treeviewlistautomationpeer <br> treeviewlistautomationpeer.treeviewlistautomationpeer

### [windows.ui.xaml.controls.maps](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps)

#### [mapcontrol](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps.mapcontrol)

mapcontrol.layers <br> mapcontrol.layersproperty <br> mapcontrol.trygetlocationfromoffset <br> mapcontrol.trygetlocationfromoffset

#### [mapcontroldatahelper](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps.mapcontroldatahelper)

mapcontroldatahelper.createmapcontrol

#### [mapelement](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps.mapelement)

mapelement.mapstylesheetentry <br> mapelement.mapstylesheetentryproperty <br> mapelement.mapstylesheetentrystate <br> mapelement.mapstylesheetentrystateproperty <br> mapelement.tag <br> mapelement.tagproperty

#### [mapelement3d](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps.mapelement3d)

mapelement3d <br> mapelement3d.heading <br> mapelement3d.headingproperty <br> mapelement3d.location <br> mapelement3d.locationproperty <br> mapelement3d.mapelement3d <br> mapelement3d.model <br> mapelement3d.pitch <br> mapelement3d.pitchproperty <br> mapelement3d.roll <br> mapelement3d.rollproperty <br> mapelement3d.scale <br> mapelement3d.scaleproperty

#### [mapelementslayer](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps.mapelementslayer)

mapelementslayer <br> mapelementslayer.mapcontextrequested <br> mapelementslayer.mapelementclick <br> mapelementslayer.mapelementpointerentered <br> mapelementslayer.mapelementpointerexited <br> mapelementslayer.mapelements <br> mapelementslayer.mapelementslayer <br> mapelementslayer.mapelementsproperty

#### [mapelementslayerclickeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps.mapelementslayerclickeventargs)

mapelementslayerclickeventargs <br> mapelementslayerclickeventargs.location <br> mapelementslayerclickeventargs.mapelements <br> mapelementslayerclickeventargs.mapelementslayerclickeventargs <br> mapelementslayerclickeventargs.position

#### [mapelementslayercontextrequestedeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps.mapelementslayercontextrequestedeventargs)

mapelementslayercontextrequestedeventargs <br> mapelementslayercontextrequestedeventargs.location <br> mapelementslayercontextrequestedeventargs.mapelements <br> mapelementslayercontextrequestedeventargs.mapelementslayercontextrequestedeventargs <br> mapelementslayercontextrequestedeventargs.position

#### [mapelementslayerpointerenteredeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps.mapelementslayerpointerenteredeventargs)

mapelementslayerpointerenteredeventargs <br> mapelementslayerpointerenteredeventargs.location <br> mapelementslayerpointerenteredeventargs.mapelement <br> mapelementslayerpointerenteredeventargs.mapelementslayerpointerenteredeventargs <br> mapelementslayerpointerenteredeventargs.position

#### [mapelementslayerpointerexitedeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps.mapelementslayerpointerexitedeventargs)

mapelementslayerpointerexitedeventargs <br> mapelementslayerpointerexitedeventargs.location <br> mapelementslayerpointerexitedeventargs.mapelement <br> mapelementslayerpointerexitedeventargs.mapelementslayerpointerexitedeventargs <br> mapelementslayerpointerexitedeventargs.position

#### [maplayer](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps.maplayer)

maplayer <br> maplayer.maplayer <br> maplayer.maptabindex <br> maplayer.maptabindexproperty <br> maplayer.visible <br> maplayer.visibleproperty <br> maplayer.zindex <br> maplayer.zindexproperty

#### [mapmodel3d](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps.mapmodel3d)

mapmodel3d <br> mapmodel3d.createfrom3mfasync <br> mapmodel3d.createfrom3mfasync <br> mapmodel3d.mapmodel3d

#### [mapmodel3dshadingoption](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps.mapmodel3dshadingoption)

mapmodel3dshadingoption

#### [mapstylesheetentries](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps.mapstylesheetentries)

mapstylesheetentries <br> mapstylesheetentries.admindistrict <br> mapstylesheetentries.admindistrictcapital <br> mapstylesheetentries.airport <br> mapstylesheetentries.area <br> mapstylesheetentries.arterialroad <br> mapstylesheetentries.building <br> mapstylesheetentries.business <br> mapstylesheetentries.capital <br> mapstylesheetentries.cemetery <br> mapstylesheetentries.continent <br> mapstylesheetentries.controlledaccesshighway <br> mapstylesheetentries.countryregion <br> mapstylesheetentries.countryregioncapital <br> mapstylesheetentries.district <br> mapstylesheetentries.drivingroute <br> mapstylesheetentries.education <br> mapstylesheetentries.educationbuilding <br> mapstylesheetentries.foodpoint <br> mapstylesheetentries.forest <br> mapstylesheetentries.golfcourse <br> mapstylesheetentries.highspeedramp <br> mapstylesheetentries.highway <br> mapstylesheetentries.indigenouspeoplesreserve <br> mapstylesheetentries.island <br> mapstylesheetentries.majorroad <br> mapstylesheetentries.medical <br> mapstylesheetentries.medicalbuilding <br> mapstylesheetentries.military <br> mapstylesheetentries.naturalpoint <br> mapstylesheetentries.nautical <br> mapstylesheetentries.neighborhood <br> mapstylesheetentries.park <br> mapstylesheetentries.peak <br> mapstylesheetentries.playingfield <br> mapstylesheetentries.point <br> mapstylesheetentries.pointofinterest <br> mapstylesheetentries.political <br> mapstylesheetentries.populatedplace <br> mapstylesheetentries.railway <br> mapstylesheetentries.ramp <br> mapstylesheetentries.reserve <br> mapstylesheetentries.river <br> mapstylesheetentries.road <br> mapstylesheetentries.roadexit <br> mapstylesheetentries.roadshield <br> mapstylesheetentries.routeline <br> mapstylesheetentries.runway <br> mapstylesheetentries.sand <br> mapstylesheetentries.shoppingcenter <br> mapstylesheetentries.stadium <br> mapstylesheetentries.street <br> mapstylesheetentries.structure <br> mapstylesheetentries.tollroad <br> mapstylesheetentries.trail <br> mapstylesheetentries.transit <br> mapstylesheetentries.transitbuilding <br> mapstylesheetentries.transportation <br> mapstylesheetentries.unpavedstreet <br> mapstylesheetentries.vegetation <br> mapstylesheetentries.volcanicpeak <br> mapstylesheetentries.walkingroute <br> mapstylesheetentries.water <br> mapstylesheetentries.waterpoint <br> mapstylesheetentries.waterroute

#### [mapstylesheetentrystates](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.maps.mapstylesheetentrystates)

mapstylesheetentrystates <br> mapstylesheetentrystates.disabled <br> mapstylesheetentrystates.hover <br> mapstylesheetentrystates.selected

### [windows.ui.xaml.controls.primitives](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.primitives)

#### [colorpickerslider](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.primitives.colorpickerslider)

colorpickerslider <br> colorpickerslider.colorchannel <br> colorpickerslider.colorchannelproperty <br> colorpickerslider.colorpickerslider

#### [colorspectrum](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.primitives.colorspectrum)

colorspectrum <br> colorspectrum.color <br> colorspectrum.colorchanged <br> colorspectrum.colorproperty <br> colorspectrum.colorspectrum <br> colorspectrum.components <br> colorspectrum.componentsproperty <br> colorspectrum.hsvcolor <br> colorspectrum.hsvcolorproperty <br> colorspectrum.maxhue <br> colorspectrum.maxhueproperty <br> colorspectrum.maxsaturation <br> colorspectrum.maxsaturationproperty <br> colorspectrum.maxvalue <br> colorspectrum.maxvalueproperty <br> colorspectrum.minhue <br> colorspectrum.minhueproperty <br> colorspectrum.minsaturation <br> colorspectrum.minsaturationproperty <br> colorspectrum.minvalue <br> colorspectrum.minvalueproperty <br> colorspectrum.shape <br> colorspectrum.shapeproperty

#### [flyoutbase](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.primitives.flyoutbase)

flyoutbase.onprocesskeyboardaccelerators <br> flyoutbase.tryinvokekeyboardaccelerator

#### [layoutinformation](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.primitives.layoutinformation)

layoutinformation.getavailablesize

#### [listviewitempresenter](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.primitives.listviewitempresenter)

listviewitempresenter.revealbackground <br> listviewitempresenter.revealbackgroundproperty <br> listviewitempresenter.revealbackgroundshowsabovecontent <br> listviewitempresenter.revealbackgroundshowsabovecontentproperty <br> listviewitempresenter.revealborderbrush <br> listviewitempresenter.revealborderbrushproperty <br> listviewitempresenter.revealborderthickness <br> listviewitempresenter.revealborderthicknessproperty

### [windows.ui.xaml.controls](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls)

#### [bitmapiconsource](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.bitmapiconsource)

bitmapiconsource <br> bitmapiconsource.bitmapiconsource <br> bitmapiconsource.showasmonochrome <br> bitmapiconsource.showasmonochromeproperty <br> bitmapiconsource.urisource <br> bitmapiconsource.urisourceproperty

#### [charactercasing](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.charactercasing)

charactercasing

#### [colorpickerhsvchannel](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.colorpickerhsvchannel)

colorpickerhsvchannel

#### [combobox](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.combobox)

combobox.placeholderforeground <br> combobox.placeholderforegroundproperty

#### [contentdialog](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.contentdialog)

contentdialog.showasync

#### [contentdialogplacement](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.contentdialogplacement)

contentdialogplacement

#### [control](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.control)

control.oncharacterreceived

#### [disabledformattingaccelerators](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.disabledformattingaccelerators)

disabledformattingaccelerators

#### [fonticonsource](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.fonticonsource)

fonticonsource <br> fonticonsource.fontfamily <br> fonticonsource.fontfamilyproperty <br> fonticonsource.fonticonsource <br> fonticonsource.fontsize <br> fonticonsource.fontsizeproperty <br> fonticonsource.fontstyle <br> fonticonsource.fontstyleproperty <br> fonticonsource.fontweight <br> fonticonsource.fontweightproperty <br> fonticonsource.glyph <br> fonticonsource.glyphproperty <br> fonticonsource.istextscalefactorenabled <br> fonticonsource.istextscalefactorenabledproperty <br> fonticonsource.mirroredwhenrighttoleft <br> fonticonsource.mirroredwhenrighttoleftproperty

#### [grid](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.grid)

grid.columnspacing <br> grid.columnspacingproperty <br> grid.rowspacing <br> grid.rowspacingproperty

#### [iconsource](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.iconsource)

iconsource <br> iconsource.foreground <br> iconsource.foregroundproperty

#### [istexttrimmedchangedeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.istexttrimmedchangedeventargs)

istexttrimmedchangedeventargs

#### [mediatransportcontrols](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.mediatransportcontrols)

mediatransportcontrols.hide <br> mediatransportcontrols.isrepeatbuttonvisible <br> mediatransportcontrols.isrepeatbuttonvisibleproperty <br> mediatransportcontrols.isrepeatenabled <br> mediatransportcontrols.isrepeatenabledproperty <br> mediatransportcontrols.show <br> mediatransportcontrols.showandhideautomatically <br> mediatransportcontrols.showandhideautomaticallyproperty

#### [navigationview](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.navigationview)

navigationview.autosuggestbox <br> navigationview.autosuggestboxproperty <br> navigationview.containerfrommenuitem <br> navigationview.iteminvoked <br> navigationview.menuitemcontainerstyle <br> navigationview.menuitemcontainerstyleproperty <br> navigationview.menuitemcontainerstyleselector <br> navigationview.menuitemcontainerstyleselectorproperty <br> navigationview.menuitemfromcontainer <br> navigationview.menuitemssource <br> navigationview.menuitemssourceproperty <br> navigationview.menuitemtemplate <br> navigationview.menuitemtemplateproperty <br> navigationview.menuitemtemplateselector <br> navigationview.menuitemtemplateselectorproperty <br> navigationview.selecteditem <br> navigationview.selecteditemproperty <br> navigationview.selectionchanged <br> navigationview.settingsitem <br> navigationview.settingsitemproperty

#### [navigationviewdisplaymodechangedeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.navigationviewdisplaymodechangedeventargs)

navigationviewdisplaymodechangedeventargs <br> navigationviewdisplaymodechangedeventargs.displaymode

#### [navigationviewitem](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.navigationviewitem)

navigationviewitem <br> navigationviewitem.compactpanelength <br> navigationviewitem.compactpanelengthproperty <br> navigationviewitem.icon <br> navigationviewitem.iconproperty <br> navigationviewitem.navigationviewitem

#### [navigationviewitembase](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.navigationviewitembase)

navigationviewitembase

#### [navigationviewitemheader](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.navigationviewitemheader)

navigationviewitemheader <br> navigationviewitemheader.navigationviewitemheader

#### [navigationviewiteminvokedeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.navigationviewiteminvokedeventargs)

navigationviewiteminvokedeventargs <br> navigationviewiteminvokedeventargs.invokeditem <br> navigationviewiteminvokedeventargs.issettingsinvoked <br> navigationviewiteminvokedeventargs.navigationviewiteminvokedeventargs

#### [navigationviewitemseparator](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.navigationviewitemseparator)

navigationviewitemseparator <br> navigationviewitemseparator.navigationviewitemseparator

#### [navigationviewlist](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.navigationviewlist)

navigationviewlist <br> navigationviewlist.navigationviewlist

#### [navigationviewselectionchangedeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.navigationviewselectionchangedeventargs)

navigationviewselectionchangedeventargs <br> navigationviewselectionchangedeventargs.issettingsselected <br> navigationviewselectionchangedeventargs.selecteditem

#### [passwordbox](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.passwordbox)

passwordbox.passwordchanging

#### [passwordboxpasswordchangingeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.passwordboxpasswordchangingeventargs)

passwordboxpasswordchangingeventargs <br> passwordboxpasswordchangingeventargs.iscontentchanging

#### [pathiconsource](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.pathiconsource)

pathiconsource <br> pathiconsource.data <br> pathiconsource.dataproperty <br> pathiconsource.pathiconsource

#### [ratingcontrol](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.ratingcontrol)

ratingcontrol <br> ratingcontrol.caption <br> ratingcontrol.captionproperty <br> ratingcontrol.initialsetvalue <br> ratingcontrol.initialsetvalueproperty <br> ratingcontrol.isclearenabled <br> ratingcontrol.isclearenabledproperty <br> ratingcontrol.isreadonly <br> ratingcontrol.isreadonlyproperty <br> ratingcontrol.iteminfo <br> ratingcontrol.iteminfoproperty <br> ratingcontrol.maxrating <br> ratingcontrol.maxratingproperty <br> ratingcontrol.placeholdervalue <br> ratingcontrol.placeholdervalueproperty <br> ratingcontrol.ratingcontrol <br> ratingcontrol.value <br> ratingcontrol.valuechanged <br> ratingcontrol.valueproperty

#### [ratingitemfontinfo](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.ratingitemfontinfo)

ratingitemfontinfo <br> ratingitemfontinfo.disabledglyph <br> ratingitemfontinfo.disabledglyphproperty <br> ratingitemfontinfo.glyph <br> ratingitemfontinfo.glyphproperty <br> ratingitemfontinfo.placeholderglyph <br> ratingitemfontinfo.placeholderglyphproperty <br> ratingitemfontinfo.pointeroverglyph <br> ratingitemfontinfo.pointeroverglyphproperty <br> ratingitemfontinfo.pointeroverplaceholderglyph <br> ratingitemfontinfo.pointeroverplaceholderglyphproperty <br> ratingitemfontinfo.ratingitemfontinfo <br> ratingitemfontinfo.unsetglyph <br> ratingitemfontinfo.unsetglyphproperty

#### [ratingitemimageinfo](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.ratingitemimageinfo)

ratingitemimageinfo <br> ratingitemimageinfo.disabledimage <br> ratingitemimageinfo.disabledimageproperty <br> ratingitemimageinfo.image <br> ratingitemimageinfo.imageproperty <br> ratingitemimageinfo.placeholderimage <br> ratingitemimageinfo.placeholderimageproperty <br> ratingitemimageinfo.pointeroverimage <br> ratingitemimageinfo.pointeroverimageproperty <br> ratingitemimageinfo.pointeroverplaceholderimage <br> ratingitemimageinfo.pointeroverplaceholderimageproperty <br> ratingitemimageinfo.ratingitemimageinfo <br> ratingitemimageinfo.unsetimage <br> ratingitemimageinfo.unsetimageproperty

#### [ratingiteminfo](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.ratingiteminfo)

ratingiteminfo <br> ratingiteminfo.ratingiteminfo

#### [richeditbox](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.richeditbox)

richeditbox.charactercasing <br> richeditbox.charactercasingproperty <br> richeditbox.copyingtoclipboard <br> richeditbox.cuttingtoclipboard <br> richeditbox.disabledformattingaccelerators <br> richeditbox.disabledformattingacceleratorsproperty <br> richeditbox.horizontaltextalignment <br> richeditbox.horizontaltextalignmentproperty

#### [richtextblock](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.richtextblock)

richtextblock.horizontaltextalignment <br> richtextblock.horizontaltextalignmentproperty <br> richtextblock.istexttrimmed <br> richtextblock.istexttrimmedchanged <br> richtextblock.istexttrimmedproperty <br> richtextblock.texthighlighters

#### [richtextblockoverflow](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.richtextblockoverflow)

richtextblockoverflow.istexttrimmed <br> richtextblockoverflow.istexttrimmedchanged <br> richtextblockoverflow.istexttrimmedproperty

#### [splitview](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.splitview)

splitview.paneopened <br> splitview.paneopening

#### [stackpanel](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.stackpanel)

stackpanel.spacing <br> stackpanel.spacingproperty

#### [swipebehavioroninvoked](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.swipebehavioroninvoked)

swipebehavioroninvoked

#### [swipecontrol](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.swipecontrol)

swipecontrol <br> swipecontrol.bottomitems <br> swipecontrol.bottomitemsproperty <br> swipecontrol.close <br> swipecontrol.leftitems <br> swipecontrol.leftitemsproperty <br> swipecontrol.rightitems <br> swipecontrol.rightitemsproperty <br> swipecontrol.swipecontrol <br> swipecontrol.topitems <br> swipecontrol.topitemsproperty

#### [swipeitem](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.swipeitem)

swipeitem <br> swipeitem.background <br> swipeitem.backgroundproperty <br> swipeitem.behavioroninvoked <br> swipeitem.behavioroninvokedproperty <br> swipeitem.command <br> swipeitem.commandparameter <br> swipeitem.commandparameterproperty <br> swipeitem.commandproperty <br> swipeitem.foreground <br> swipeitem.foregroundproperty <br> swipeitem.iconsource <br> swipeitem.iconsourceproperty <br> swipeitem.invoked <br> swipeitem.swipeitem <br> swipeitem.text <br> swipeitem.textproperty

#### [swipeiteminvokedeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.swipeiteminvokedeventargs)

swipeiteminvokedeventargs <br> swipeiteminvokedeventargs.swipecontrol

#### [swipeitems](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.swipeitems)

swipeitems <br> swipeitems.append <br> swipeitems.clear <br> swipeitems.first <br> swipeitems.getat <br> swipeitems.getmany <br> swipeitems.getview <br> swipeitems.indexof <br> swipeitems.insertat <br> swipeitems.mode <br> swipeitems.modeproperty <br> swipeitems.removeat <br> swipeitems.removeatend <br> swipeitems.replaceall <br> swipeitems.setat <br> swipeitems.size <br> swipeitems.swipeitems

#### [swipemode](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.swipemode)

swipemode

#### [symboliconsource](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.symboliconsource)

symboliconsource <br> symboliconsource.symbol <br> symboliconsource.symboliconsource <br> symboliconsource.symbolproperty

#### [textblock](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.textblock)

textblock.horizontaltextalignment <br> textblock.horizontaltextalignmentproperty <br> textblock.istexttrimmed <br> textblock.istexttrimmedchanged <br> textblock.istexttrimmedproperty <br> textblock.texthighlighters

#### [textbox](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.textbox)

textbox.beforetextchanging <br> textbox.charactercasing <br> textbox.charactercasingproperty <br> textbox.copyingtoclipboard <br> textbox.cuttingtoclipboard <br> textbox.horizontaltextalignment <br> textbox.horizontaltextalignmentproperty <br> textbox.placeholderforeground <br> textbox.placeholderforegroundproperty

#### [textboxbeforetextchangingeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.textboxbeforetextchangingeventargs)

textboxbeforetextchangingeventargs <br> textboxbeforetextchangingeventargs.cancel <br> textboxbeforetextchangingeventargs.newtext

#### [textcontrolcopyingtoclipboardeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.textcontrolcopyingtoclipboardeventargs)

textcontrolcopyingtoclipboardeventargs <br> textcontrolcopyingtoclipboardeventargs.handled

#### [textcontrolcuttingtoclipboardeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.textcontrolcuttingtoclipboardeventargs)

textcontrolcuttingtoclipboardeventargs <br> textcontrolcuttingtoclipboardeventargs.handled

#### [treeview](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.treeview)

treeview.selectall <br> treeview.selecteditems <br> treeview.selectionmode <br> treeview.selectionmodeproperty

#### [treeviewselectionmode](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.treeviewselectionmode)

treeviewselectionmode

### [windows.ui.xaml.documents](https://docs.microsoft.com/uwp/api/windows.ui.xaml.documents)

#### [block](https://docs.microsoft.com/uwp/api/windows.ui.xaml.documents.block)

block.horizontaltextalignment <br> block.horizontaltextalignmentproperty

#### [texthighlighter](https://docs.microsoft.com/uwp/api/windows.ui.xaml.documents.texthighlighter)

texthighlighter <br> texthighlighter.background <br> texthighlighter.backgroundproperty <br> texthighlighter.foreground <br> texthighlighter.foregroundproperty <br> texthighlighter.ranges <br> texthighlighter.texthighlighter

#### [texthighlighterbase](https://docs.microsoft.com/uwp/api/windows.ui.xaml.documents.texthighlighterbase)

texthighlighterbase

#### [textrange](https://docs.microsoft.com/uwp/api/windows.ui.xaml.documents.textrange)

textrange

### [windows.ui.xaml.hosting](https://docs.microsoft.com/uwp/api/windows.ui.xaml.hosting)

#### [designerappmanager](https://docs.microsoft.com/uwp/api/windows.ui.xaml.hosting.designerappmanager)

designerappmanager <br> designerappmanager.appusermodelid <br> designerappmanager.close <br> designerappmanager.createnewviewasync <br> designerappmanager.designerappmanager <br> designerappmanager.duplicatehandleintoapp <br> designerappmanager.loadobjectintoappasync <br> designerappmanager.processexited

#### [designerappview](https://docs.microsoft.com/uwp/api/windows.ui.xaml.hosting.designerappview)

designerappview <br> designerappview.applicationviewid <br> designerappview.appusermodelid <br> designerappview.close <br> designerappview.updateviewasync <br> designerappview.viewsize <br> designerappview.viewstate

#### [designerappviewstate](https://docs.microsoft.com/uwp/api/windows.ui.xaml.hosting.designerappviewstate)

designerappviewstate

#### [processexitedeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.hosting.processexitedeventargs)

processexitedeventargs <br> processexitedeventargs.exitcode

### [windows.ui.xaml.input](https://docs.microsoft.com/uwp/api/windows.ui.xaml.input)

#### [characterreceivedroutedeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.input.characterreceivedroutedeventargs)

characterreceivedroutedeventargs <br> characterreceivedroutedeventargs.character <br> characterreceivedroutedeventargs.handled <br> characterreceivedroutedeventargs.keystatus

#### [keyboardaccelerator](https://docs.microsoft.com/uwp/api/windows.ui.xaml.input.keyboardaccelerator)

keyboardaccelerator <br> keyboardaccelerator.invoked <br> keyboardaccelerator.isenabled <br> keyboardaccelerator.isenabledproperty <br> keyboardaccelerator.key <br> keyboardaccelerator.keyboardaccelerator <br> keyboardaccelerator.keyproperty <br> keyboardaccelerator.modifiers <br> keyboardaccelerator.modifiersproperty <br> keyboardaccelerator.scopeowner <br> keyboardaccelerator.scopeownerproperty

#### [keyboardacceleratorinvokedeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.input.keyboardacceleratorinvokedeventargs)

keyboardacceleratorinvokedeventargs <br> keyboardacceleratorinvokedeventargs.element <br> keyboardacceleratorinvokedeventargs.handled

#### [pointerroutedeventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.input.pointerroutedeventargs)

pointerroutedeventargs.isgenerated

#### [processkeyboardacceleratoreventargs](https://docs.microsoft.com/uwp/api/windows.ui.xaml.input.processkeyboardacceleratoreventargs)

processkeyboardacceleratoreventargs <br> processkeyboardacceleratoreventargs.handled <br> processkeyboardacceleratoreventargs.key <br> processkeyboardacceleratoreventargs.modifiers

### [windows.ui.xaml.markup](https://docs.microsoft.com/uwp/api/windows.ui.xaml.markup)

#### [markupextension](https://docs.microsoft.com/uwp/api/windows.ui.xaml.markup.markupextension)

markupextension <br> markupextension.markupextension <br> markupextension.providevalue

#### [markupextensionreturntypeattribute](https://docs.microsoft.com/uwp/api/windows.ui.xaml.markup.markupextensionreturntypeattribute)

markupextensionreturntypeattribute <br> markupextensionreturntypeattribute.markupextensionreturntypeattribute

### [windows.ui.xaml.media](https://docs.microsoft.com/uwp/api/windows.ui.xaml.media)

#### [acrylicbrush](https://docs.microsoft.com/uwp/api/windows.ui.xaml.media.acrylicbrush)

acrylicbrush.alwaysusefallback <br> acrylicbrush.alwaysusefallbackproperty <br> acrylicbrush.tinttransitionduration <br> acrylicbrush.tinttransitiondurationproperty

#### [revealbrush](https://docs.microsoft.com/uwp/api/windows.ui.xaml.media.revealbrush)

revealbrush.alwaysusefallback <br> revealbrush.alwaysusefallbackproperty <br> revealbrush.getstate <br> revealbrush.setstate <br> revealbrush.stateproperty

#### [revealbrushstate](https://docs.microsoft.com/uwp/api/windows.ui.xaml.media.revealbrushstate)

revealbrushstate

### [windows.ui.xaml](https://docs.microsoft.com/uwp/api/windows.ui.xaml)

#### [frameworkelement](https://docs.microsoft.com/uwp/api/windows.ui.xaml.frameworkelement)

frameworkelement.actualtheme <br> frameworkelement.actualthemechanged <br> frameworkelement.actualthemeproperty

#### [uielement](https://docs.microsoft.com/uwp/api/windows.ui.xaml.uielement)

uielement.characterreceived <br> uielement.characterreceivedevent <br> uielement.getchildrenintabfocusorder <br> uielement.keyboardaccelerators <br> uielement.onprocesskeyboardaccelerators <br> uielement.processkeyboardaccelerators <br> uielement.tryinvokekeyboardaccelerator