---
layout: default-layout
title: iDLRLTSConnectionParameters - Dynamsoft Label Recognition iOS Class
description: This page shows the iDMLTSConnectionParameters class of Dynamsoft Label Recognition for iOS SDK.
keywords: iDMLTSConnectionParameters, class, objective-c, oc, swift
needAutoGenerateSidebar: true
permalink: /programming/objectivec-swift/api-reference/class/dlr-lts-connection-parameters.html
---


# iDLRLTSConnectionParameters
Defines a class to configure the parameters to connect to license tracking server.  


## Attributes
    
| Attribute | Type |
|---------- | ---- |
| [`mainServerURL`](#mainserverurl) | *NSString\** |
| [`standbyServerURL`](#standbyserverurl) | *NSString\** |
| [`handshakeCode`](#handshakecode) | *NSString\** |
| [`sessionPassword`](#sessionpassword) | *NSString\** |
| [`chargeWay`](#chargeway) | *EnumDMChargeWay* |
| [`UUIDGenerationMethod`](#uuidgenerationmethod) | *EnumDMUUIDGenerationMethod* |
| [`maxBufferDays`](#maxbufferdays) | *NSInteger* |
| [`limitedLicenseModules`](#limitedlicensemodules) | *NSArray\** |
| [`organizationID`](#organizationid) | *NSString\** |
| [`products`](#products) | *NSInteger* |


### mainServerURL
The URL of the license tracking server.
```objc
NSString*  mainServerURL
```

**Value Range**

Any string value   

**Default value**

""

**Remarks**

If you choose "Dynamsoft-hosting", then no need to change the value of MainServerURL and StandbyServerURL. When both are set to null (default value), it will connect to Dynamsoft's license tracking servers for online verification.   


### standbyServerURL
The URL of the standby license tracking server.
```objc
NSString*  standbyServerURL
```

**Value Range**

Any string value   

**Default value**

""

**Remarks**

If you choose "Dynamsoft-hosting", then no need to change the value of MainServerURL and StandbyServerURL. When both are set to null (default value), it will connect to Dynamsoft's license tracking servers for online verification.   


### handshakeCode
The handshake code.
```objc
NSString*  handshakeCode
```

**Value Range**

Any string value   

**Default value**

""

### sessionPassword
The session password of the handshake code set in license tracking server.
```objc
NSString*  sessionPassword
```

**Value Range**

Any string value   

**Default value**

""

### chargeWay
Sets the charge way.
```objc
EnumDMChargeWay chargeWay
```

**Value Range**

A value of [`EnumDMChargeWay`]({{ site.enumerations }}other-enums.html#dm_chargeway) Enumeration items.

**Default value**

`EnumDMChargeWayAuto`

**See also**

[`EnumDMChargeWay`]({{ site.enumerations }}other-enums.html#dm_chargeway)
      

### UUIDGenerationMethod
Sets the method to generate UUID.
```objc
EnumDMUUIDGenerationMethod UUIDGenerationMethod
```

**Value Range**

A value of [`EnumDMUUIDGenerationMethod`]({{ site.enumerations }}other-enums.html#dm_uuidgenerationmethod) Enumeration items.

**Default value**

`EnumDMUUIDGenerationMethodRandom`

**See also**

[`EnumDMUUIDGenerationMethod`]({{ site.enumerations }}other-enums.html#dm_uuidgenerationmethod)
      

### maxBufferDays
Sets the max days to buffer the license info.
```objc
NSInteger maxBufferDays
```

**Value Range**

[0,0x7fffffff]   

**Default value**

7

### limitedLicenseModules
Sets the license modules to use.
```objc
NSArray*  limitedLicenseModules
```

**Value Range**

Each array item can be any one of the [`EnumDMLicenseModule`]({{ site.enumerations }}other-enums.html#dm_licensemodule) Enumeration items.   

**Default value**

nil

**See also**

[`EnumDMLicenseModule`]({{ site.enumerations }}other-enums.html#dm_licensemodule)    
      
### organizationID
The organization ID got from Dynamsoft.
```objc
NSString* organizationID
```

**Value Range**

Any string value   

**Default value**

""

### products
Sets the products to get the license for. Product values can be combined.
```objc
NSInteger products
```

**Value Range**

A combine value of [`EnumProduct`]({{ site.enumerations }}other-enums.html#product) Enumeration items.

**Default value**

`EnumProductALL`

**See also**

[`EnumProduct`]({{ site.enumerations }}other-enums.html#product)
  