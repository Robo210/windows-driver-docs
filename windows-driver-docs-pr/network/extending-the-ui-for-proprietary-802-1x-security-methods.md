---
title: Extending the UI for Proprietary 802.1X Security Methods
description: Extending the UI for Proprietary 802.1X Security Methods
ms.assetid: 3307179f-f30b-4234-a64d-4e771ac8673e
keywords:
- proprietary 802.1X security WDK IHV UI Extensions DLL
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
---

# Extending the UI for Proprietary 802.1X Security Methods


**Important**  The [Native 802.11 Wireless LAN](native-802-11-wireless-lan4.md) interface is deprecated in Windows 10 and later. Please use the WLAN Device Driver Interface (WDI) instead. For more information about WDI, see [WLAN Universal Windows driver model](wifi-universal-driver-model.md).

 

If the Native 802.11 IHV Extensions DLL supports proprietary 802.1X-based security extensions, the Native 802.11 IHV UI Extensions DLL can extend the Network Configuration user interface's (UI's) **Security** tab to allow user configuration of the these extensions. For more information about extending the Native 802.11 802.1X module, see [Interface to the Native 802.11 802.1X Module](interface-to-the-native-802-11-802-1x-module.md).

For more information about the Network Configuration UI and other Native 802.11 components, see [Native 802.11 Software Architecture](native-802-11-software-architecture.md).

Before it displays the **Security** tab, the operating system does the following:

1.  Queries the Native 802.11 IHV UI Extensions DLL for its security property extensions through a call to the [**IDot11ExtUI::GetDot11ExtUIProperties**](https://msdn.microsoft.com/library/windows/hardware/ff553776) method. The operating system passes a value of **DOT11\_EXT\_UI\_KEYEXTENSION** to the method's *ExtType* parameter.

    Property extensions of type **DOT11\_EXT\_UI\_KEYEXTENSION** do not provide security settings that are mutually exclusive to the standard Microsoft security settings. Instead, this type of security property extension provides IHV-defined 802.1X settings that are used together with the Microsoft 802.1X settings.

2.  Queries the friendly name of the 802.1X security extension by calling the extension's [**IDot11ExtUIProperty::GetDot11ExtUIPropertyFriendlyName**](https://msdn.microsoft.com/library/windows/hardware/ff553768) method.

3.  Queries the extension's [**IDot11ExtUIProperty::Dot11ExtUIPropertyIsStandardSecurity**](https://msdn.microsoft.com/library/windows/hardware/ff553760) method to determine whether the extension supports a security type extension. If the method sets the *fIsStandardSecurity* parameter to **FALSE**, the operating system will add the extension's friendly name to the **Security type** list on the **Security** tab.

4.  When the end user selects an item from the **Security type** list, the operating system responds by calling the [**IDot11ExtUIProperty::Dot11ExtUIPropertyGetSelected**](https://msdn.microsoft.com/library/windows/hardware/ff553753) method for each extension to match the selection of the end user. The first extension that returns a value of **TRUE** for the method's *pfIsSelected* parameter is determined to be the selected extension. After this is confirmed, the operating system highlights the selection made by the end user.

5.  Calls the selected property extension's [**IDot11ExtUIProperty::Dot11ExtUIPropertyHasConfigurationUI**](https://msdn.microsoft.com/library/windows/hardware/ff553756) method to determine whether it has a custom UI property page that can be displayed. If the method returns a value of **TRUE** for the method's *fHasConfigurationUI* parameter, the operating system will display a **Configure** button next to the **Security type** list.

    If the end user clicks the **Configure** button, the operating system will call the selected property extension's [**IDot11ExtUIProperty::DisplayDot11ExtUIProperty**](https://msdn.microsoft.com/library/windows/hardware/ff553749) method to display the custom configuration UI for the extension.

6.  Calls the selected property extension's [**IDot11ExtUIProperty::Dot11ExtUIPropertyGetDisplayInfo**](https://msdn.microsoft.com/library/windows/hardware/ff553752) method. Through this method, the Native 802.11 IHV UI Extensions DLL can return other property extensions to the **Security** tab of the Native 802.11 Network Configuration UI.

    The **IDot11ExtUIProperty::Dot11ExtUIPropertyGetDisplayInfo** method returns a list of the items that the selected property extension adds to the **Security** tab. Each entry in the list is formatted as a [**DOT11\_EXT\_UI\_PROPERTY\_DISPLAY\_INFO**](https://msdn.microsoft.com/library/windows/hardware/ff548637) structure.

    For Windows Vista, the Native 802.11 IHV UI Extensions DLL can only add items to the **Encryption** list on the **Security** tab. As a result, each item in the list of [**DOT11\_EXT\_UI\_PROPERTY\_DISPLAY\_INFO**](https://msdn.microsoft.com/library/windows/hardware/ff548637) structures must have a **DOT11\_EXT\_UI\_DISPLAY\_INFO\_TYPE** of **DOT11\_EXT\_UI\_DISPLAY\_INFO\_CIPHER** in order to be included in the **Encryption** list.

7.  When the end user selects from the **Encryption** list, the operating system will call the selected property extension's [**IDot11ExtUIProperty::Dot11ExtUIPropertySetDisplayInfo**](https://msdn.microsoft.com/library/windows/hardware/ff553763) method to process the profile data that is associated with the end user's selection.

 

 





