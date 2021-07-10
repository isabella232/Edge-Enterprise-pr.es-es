---
title: Asignación de directivas de Google Chrome a Microsoft Edge
ms.author: brianalt
author: brianalt
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Asignación de directivas de Google Chrome a Microsoft Edge
ms.openlocfilehash: 9c422c66df9f2892e54ad9d935f4d6de6f88eae3
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642846"
---
# <a name="google-chrome-to-microsoft-edge-policy-mapping"></a>Asignación de directivas de Google Chrome a Microsoft Edge

Este artículo asigna las directivas de Google Chrome a las directivas de Microsoft Edge relevantes compatibles con la versión 80. En el caso de las directivas de Microsoft Edge (versión heredada), vea el artículo [Asignación de directiva de Microsoft Edge (versión heredada) a Microsoft Edge](/deployedge/microsoft-edge-policy-map-chrome-to-newedge?branch=master).

> [!NOTE]
> La siguiente asignación está pensada para ayudarle con la implementación inicial de la versión 80 de Microsoft Edge. Para obtener una lista definitiva de las últimas directivas, consulte:
> - [Referencia de directiva de explorador](/deployedge/microsoft-edge-policies)
> - [Actualizar referencia de directiva](/deployedge/microsoft-edge-update-policies)

## <a name="google-chrome-to-microsoft-edge-policy-map"></a>Asignación de directivas de Google Chrome a Microsoft Edge

|Directiva de Google Chrome|Directiva de Microsoft Edge|
|-|-|
|[AbusiveExperienceInterventionEnforce](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AbusiveExperienceInterventionEnforce)|No disponible|
|[AdsSettingForIntrusiveAdsSites](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AdsSettingForIntrusiveAdsSites)|[AdsSettingForIntrusiveAdsSites](./microsoft-edge-policies.md#adssettingforintrusiveadssites)|
|[AllowCrossOriginAuthPrompt](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowCrossOriginAuthPrompt)|[AllowCrossOriginAuthPrompt](./microsoft-edge-policies.md#allowcrossoriginauthprompt)|
|[AllowDeletingBrowserHistory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowDeletingBrowserHistory)|[AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory)|
|[AllowDinosaurEasterEgg](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowDinosaurEasterEgg)|No disponible|
|[AllowedDomainsForApps](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowedDomainsForApps)|No disponible|
|[AllowFileSelectionDialogs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowFileSelectionDialogs)|[AllowFileSelectionDialogs](./microsoft-edge-policies.md#allowfileselectiondialogs)|
|[AllowOutdatedPlugins](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowOutdatedPlugins)|No disponible|
|[AllowPasswordProtectedFiles](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowPasswordProtectedFiles)|No disponible|
|[AllowPopupsDuringPageUnload](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowPopupsDuringPageUnload)|[AllowPopupsDuringPageUnload](./microsoft-edge-policies.md#allowpopupsduringpageunload)|
|[AllowSyncXHRInPageDismissal](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowSyncXHRInPageDismissal)|[AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal)|
|[AlternateErrorPagesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AlternateErrorPagesEnabled)|[AlternateErrorPagesEnabled](./microsoft-edge-policies.md#alternateerrorpagesenabled)|
|[AlternativeBrowserParameters](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AlternativeBrowserParameters)|Ver Microsoft Edge con modo IE|
|[AlternativeBrowserPath](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AlternativeBrowserPath)|Ver Microsoft Edge con modo IE|
|[AlwaysOpenPdfExternally](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AlwaysOpenPdfExternally)|[AlwaysOpenPdfExternally](./microsoft-edge-policies.md#alwaysopenpdfexternally)|
|[AmbientAuthenticationInPrivateModesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AmbientAuthenticationInPrivateModesEnabled)|No disponible|
|[ApplicationLocaleValue](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ApplicationLocaleValue)|[ApplicationLocaleValue](./microsoft-edge-policies.md#applicationlocalevalue)|
|[AudioCaptureAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AudioCaptureAllowed)|[AudioCaptureAllowed](./microsoft-edge-policies.md#audiocaptureallowed)|
|[AudioCaptureAllowedUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AudioCaptureAllowedUrls)|[AudioCaptureAllowedUrls](./microsoft-edge-policies.md#audiocaptureallowedurls)|
|[AudioSandboxEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AudioSandboxEnabled)|No disponible|
|[AuthNegotiateDelegateByKdcPolicy](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AuthNegotiateDelegateByKdcPolicy)|No disponible|
|[AuthNegotiateDelegateWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AuthNegotiateDelegateWhitelist)|[AuthNegotiateDelegateAllowlist](./microsoft-edge-policies.md#authnegotiatedelegateallowlist)|
|[AuthSchemes](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AuthSchemes)|[AuthSchemes](./microsoft-edge-policies.md#authschemes)|
|[AuthServerWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AuthServerWhitelist)|[AuthServerAllowlist](./microsoft-edge-policies.md#authserverallowlist)|
|[AutofillAddressEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutofillAddressEnabled)|[AutofillAddressEnabled](./microsoft-edge-policies.md#autofilladdressenabled)|
|[AutofillCreditCardEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutofillCreditCardEnabled)|[AutofillCreditCardEnabled](./microsoft-edge-policies.md#autofillcreditcardenabled)|
|[AutoplayAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutoplayAllowed)|[AutoplayAllowed](./microsoft-edge-policies.md#autoplayallowed)|
|[AutoplayWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutoplayWhitelist)|No disponible|
|[AutoSelectCertificateForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutoSelectCertificateForUrls)|[AutoSelectCertificateForUrls](./microsoft-edge-policies.md#autoselectcertificateforurls)|
|[BackgroundModeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BackgroundModeEnabled)|[BackgroundModeEnabled](./microsoft-edge-policies.md#backgroundmodeenabled)|
|[BlockExternalExtensions](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BlockExternalExtensions)|No disponible|
|[BlockLargeFileTransfer](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BlockLargeFileTransfer)|No disponible|
|[BlockThirdPartyCookies](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BlockThirdPartyCookies)|[BlockThirdPartyCookies](./microsoft-edge-policies.md#blockthirdpartycookies)|
|[BookmarkBarEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BookmarkBarEnabled)|[FavoritesBarEnabled](./microsoft-edge-policies.md#favoritesbarenabled)|
|[BrowserAddPersonEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserAddPersonEnabled)|[BrowserAddProfileEnabled](./microsoft-edge-policies.md#browseraddprofileenabled)|
|[BrowserGuestModeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserGuestModeEnabled)|[BrowserGuestModeEnabled](./microsoft-edge-policies.md#browserguestmodeenabled)|
|[BrowserGuestModeEnforced](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserGuestModeEnforced)|No disponible|
|[BrowserNetworkTimeQueriesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserNetworkTimeQueriesEnabled)|[BrowserNetworkTimeQueriesEnabled](./microsoft-edge-policies.md#browsernetworktimequeriesenabled)|
|[BrowserSignin](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSignin)|[BrowserSignin](./microsoft-edge-policies.md#browsersignin)|
|[BrowserSwitcherChromeParameters](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherChromeParameters)|Ver Microsoft Edge con modo IE|
|[BrowserSwitcherChromePath](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherChromePath)|Ver Microsoft Edge con modo IE|
|[BrowserSwitcherDelay](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherDelay)|Ver Microsoft Edge con modo IE|
|[BrowserSwitcherEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherEnabled)|Ver Microsoft Edge con modo IE|
|[BrowserSwitcherExternalGreylistUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherExternalGreylistUrl)|Ver Microsoft Edge con modo IE|
|[BrowserSwitcherExternalSitelistUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherExternalSitelistUrl)|Ver Microsoft Edge con modo IE|
|[BrowserSwitcherKeepLastChromeTab](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherKeepLastChromeTab)|Ver Microsoft Edge con modo IE|
|[BrowserSwitcherUrlGreylist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherUrlGreylist)|Ver Microsoft Edge con modo IE|
|[BrowserSwitcherUrlList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherUrlList)|Ver Microsoft Edge con modo IE|
|[BrowserSwitcherUseIeSitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherUseIeSitelist)|Ver Microsoft Edge con modo IE|
|[BuiltInDnsClientEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BuiltInDnsClientEnabled)|[BuiltInDnsClientEnabled](./microsoft-edge-policies.md#builtindnsclientenabled)|
|[CertificateTransparencyEnforcementDisabledForCas](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CertificateTransparencyEnforcementDisabledForCas)|[CertificateTransparencyEnforcementDisabledForCas](./microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforcas)|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CertificateTransparencyEnforcementDisabledForLegacyCas)|[CertificateTransparencyEnforcementDisabledForLegacyCas](./microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforlegacycas)|
|[CertificateTransparencyEnforcementDisabledForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CertificateTransparencyEnforcementDisabledForUrls)|[CertificateTransparencyEnforcementDisabledForUrls](./microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls)|
|[CheckContentCompliance](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CheckContentCompliance)|No disponible|
|[ChromeCleanupEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ChromeCleanupEnabled)|No disponible|
|[ChromeCleanupReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ChromeCleanupReportingEnabled)|No disponible|
|[ClickToCallEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ClickToCallEnabled)|No disponible|
|[CloudExtensionRequestEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudExtensionRequestEnabled)|No disponible|
|[CloudManagementEnrollmentMandatory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudManagementEnrollmentMandatory)|No disponible|
|[CloudManagementEnrollmentToken](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudManagementEnrollmentToken)|No disponible|
|[CloudPolicyOverridesPlatformPolicy](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudPolicyOverridesPlatformPolicy)|No disponible|
|[CloudPrintProxyEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudPrintProxyEnabled)|No disponible|
|[CloudPrintSubmitEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudPrintSubmitEnabled)|No disponible|
|[CloudReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudReportingEnabled)|No disponible|
|[CoalesceH2ConnectionsWithClientCertificatesForHosts](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CoalesceH2ConnectionsWithClientCertificatesForHosts)
|[CommandLineFlagSecurityWarningsEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CommandLineFlagSecurityWarningsEnabled)
|[ComponentUpdatesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ComponentUpdatesEnabled)|[ComponentUpdatesEnabled](./microsoft-edge-policies.md#componentupdatesenabled)|
|[CookiesAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CookiesAllowedForUrls)|[CookiesAllowedForUrls](./microsoft-edge-policies.md#cookiesallowedforurls)|
|[CookiesBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CookiesBlockedForUrls)|[CookiesBlockedForUrls](./microsoft-edge-policies.md#cookiesblockedforurls)|
|[CookiesSessionOnlyForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CookiesSessionOnlyForUrls)|[CookiesSessionOnlyForUrls](./microsoft-edge-policies.md#cookiessessiononlyforurls)|
|[CorsLegacyModeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CorsLegacyModeEnabled)|No disponible|
|[CorsMitigationList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CorsMitigationList)|No disponible|
|[DefaultBrowserSettingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultBrowserSettingEnabled)|[DefaultBrowserSettingEnabled](./microsoft-edge-policies.md#defaultbrowsersettingenabled)|
|[DefaultCookiesSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultCookiesSetting)|[DefaultCookiesSetting](./microsoft-edge-policies.md#defaultcookiessetting)|
|[DefaultDownloadDirectory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultDownloadDirectory)|No disponible|
|[DefaultGeolocationSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultGeolocationSetting)|[DefaultGeolocationSetting](./microsoft-edge-policies.md#defaultgeolocationsetting)|
|[DefaultImagesSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultImagesSetting)|[DefaultImagesSetting](./microsoft-edge-policies.md#defaultimagessetting)|
|[DefaultInsecureContentSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultInsecureContentSetting)|[DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting)|
|[DefaultJavaScriptSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultJavaScriptSetting)|[DefaultJavaScriptSetting](./microsoft-edge-policies.md#defaultjavascriptsetting)|
|[DefaultNotificationsSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultNotificationsSetting)|[DefaultNotificationsSetting](./microsoft-edge-policies.md#defaultnotificationssetting)|
|[DefaultPluginsSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultPluginsSetting)|[DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting)|
|[DefaultPopupsSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultPopupsSetting)|[DefaultPopupsSetting](./microsoft-edge-policies.md#defaultpopupssetting)|
|[DefaultPrinterSelection](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultPrinterSelection)|[DefaultPrinterSelection](./microsoft-edge-policies.md#defaultprinterselection)|
|[DefaultSearchProviderAlternateURLs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderAlternateURLs)|No disponible|
|[DefaultSearchProviderEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderEnabled)|[DefaultSearchProviderEnabled](./microsoft-edge-policies.md#defaultsearchproviderenabled)|
|[DefaultSearchProviderEncodings](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderEncodings)|[DefaultSearchProviderEncodings](./microsoft-edge-policies.md#defaultsearchproviderencodings)|
|[DefaultSearchProviderIconURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderIconURL)|No disponible|
|[DefaultSearchProviderImageURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderImageURL)|[DefaultSearchProviderImageURL](./microsoft-edge-policies.md#defaultsearchproviderimageurl)|
|[DefaultSearchProviderImageURLPostParams](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderImageURLPostParams)|[DefaultSearchProviderImageURLPostParams](./microsoft-edge-policies.md#defaultsearchproviderimageurlpostparams)|
|[DefaultSearchProviderKeyword](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderKeyword)|[DefaultSearchProviderKeyword](./microsoft-edge-policies.md#defaultsearchproviderkeyword)|
|[DefaultSearchProviderName](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderName)|[DefaultSearchProviderName](./microsoft-edge-policies.md#defaultsearchprovidername)|
|[DefaultSearchProviderNewTabURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderNewTabURL)|No disponible|
|[DefaultSearchProviderSearchURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderSearchURL)|[DefaultSearchProviderSearchURL](./microsoft-edge-policies.md#defaultsearchprovidersearchurl)|
|[DefaultSearchProviderSearchURLPostParams](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderSearchURLPostParams)|No disponible|
|[DefaultSearchProviderSuggestURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderSuggestURL)|[DefaultSearchProviderSuggestURL](./microsoft-edge-policies.md#defaultsearchprovidersuggesturl)|
|[DefaultSearchProviderSuggestURLPostParams](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderSuggestURLPostParams)|No disponible|
|[DefaultWebBluetoothGuardSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultWebBluetoothGuardSetting)|[DefaultWebBluetoothGuardSetting](./microsoft-edge-policies.md#defaultwebbluetoothguardsetting)|
|[DefaultWebUsbGuardSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultWebUsbGuardSetting)|[DefaultWebUsbGuardSetting](./microsoft-edge-policies.md#defaultwebusbguardsetting)|
|[DelayDeliveryUntilVerdict](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DelayDeliveryUntilVerdict)|No disponible|
|[DeveloperToolsAvailability](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DeveloperToolsAvailability)|[DeveloperToolsAvailability](./microsoft-edge-policies.md#developertoolsavailability)|
|[Disable3DAPIs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=Disable3DAPIs)|[Disable3DAPIs](./microsoft-edge-policies.md#disable3dapis)|
|[DisableAuthNegotiateCnameLookup](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DisableAuthNegotiateCnameLookup)|[DisableAuthNegotiateCnameLookup](./microsoft-edge-policies.md#disableauthnegotiatecnamelookup)|
|[DisablePrintPreview](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DisablePrintPreview)|[UseSystemPrintDialog](./microsoft-edge-policies.md#usesystemprintdialog)|
|[DisableSafeBrowsingProceedAnyway](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DisableSafeBrowsingProceedAnyway)|[PreventSmartScreenPromptOverride](./microsoft-edge-policies.md#preventsmartscreenpromptoverride)|
|[DisableScreenshots](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DisableScreenshots)|[DisableScreenshots](./microsoft-edge-policies.md#disablescreenshots)|
|[DiskCacheDir](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DiskCacheDir)|[DiskCacheDir](./microsoft-edge-policies.md#diskcachedir)|
|[DiskCacheSize](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DiskCacheSize)|[DiskCacheSize](./microsoft-edge-policies.md#diskcachesize)|
|[DNSInterceptionChecksEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DNSInterceptionChecksEnabled)|[DNSInterceptionChecksEnabled](./microsoft-edge-policies.md#dnsinterceptionchecksenabled)|
|[DnsOverHttpsMode](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DnsOverHttpsMode)|No disponible|
|[DnsOverHttpsTemplates](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DnsOverHttpsTemplates)|No disponible|
|[DownloadDirectory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DownloadDirectory)|[DownloadDirectory](./microsoft-edge-policies.md#downloaddirectory)|
|[DownloadRestrictions](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DownloadRestrictions)|[DownloadRestrictions](./microsoft-edge-policies.md#downloadrestrictions)|
|[EditBookmarksEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EditBookmarksEnabled)|[EditFavoritesEnabled](./microsoft-edge-policies.md#editfavoritesenabled)|
|[EnableAuthNegotiatePort](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnableAuthNegotiatePort)|[EnableAuthNegotiatePort](./microsoft-edge-policies.md#enableauthnegotiateport)|
|[EnableDeprecatedWebPlatformFeatures](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnableDeprecatedWebPlatformFeatures)|[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures)|
|[EnableMediaRouter](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnableMediaRouter)|[EnableMediaRouter](./microsoft-edge-policies.md#enablemediarouter)|
|[EnableOnlineRevocationChecks](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnableOnlineRevocationChecks)|[EnableOnlineRevocationChecks](./microsoft-edge-policies.md#enableonlinerevocationchecks)|
|[EnterpriseHardwarePlatformAPIEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnterpriseHardwarePlatformAPIEnabled)|[EnterpriseHardwarePlatformAPIEnabled](./microsoft-edge-policies.md#enterprisehardwareplatformapienabled)|
|[ExtensionAllowedTypes](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionAllowedTypes)|[ExtensionAllowedTypes](./microsoft-edge-policies.md#extensionallowedtypes)|
|[ExtensionInstallBlacklist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallBlacklist)|[ExtensionInstallBlocklist](./microsoft-edge-policies.md#extensioninstallblocklist)|
|[ExtensionInstallForcelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallForcelist)|[ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist)|
|[ExtensionInstallListsMergeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallListsMergeEnabled)|No disponible|
|[ExtensionInstallSources](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallSources)|[ExtensionInstallSources](./microsoft-edge-policies.md#extensioninstallsources)|
|[ExtensionInstallWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallWhitelist)|[ExtensionInstallAllowlist](./microsoft-edge-policies.md#extensioninstallallowlist)|
|[ExtensionSettings](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionSettings)|[ExtensionSettings](./microsoft-edge-policies.md#extensionsettings)|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExternalProtocolDialogShowAlwaysOpenCheckbox)|[ExternalProtocolDialogShowAlwaysOpenCheckbox](./microsoft-edge-policies.md#externalprotocoldialogshowalwaysopencheckbox)|
|[ForceEphemeralProfiles](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ForceEphemeralProfiles)|[ForceEphemeralProfiles](./microsoft-edge-policies.md#forceephemeralprofiles)|
|[ForceGoogleSafeSearch](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ForceGoogleSafeSearch)|[ForceGoogleSafeSearch](./microsoft-edge-policies.md#forcegooglesafesearch)|
|[ForceNetworkInProcess](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ForceNetworkInProcess)|[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess)|
|[ForceYouTubeRestrict](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ForceYouTubeRestrict)|[ForceYouTubeRestrict](./microsoft-edge-policies.md#forceyoutuberestrict)|
|[FullscreenAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=FullscreenAllowed)|[FullscreenAllowed](./microsoft-edge-policies.md#fullscreenallowed)|
|[GloballyScopeHTTPAuthCacheEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=GloballyScopeHTTPAuthCacheEnabled)|No disponible|
|[HardwareAccelerationModeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HardwareAccelerationModeEnabled)|[HardwareAccelerationModeEnabled](./microsoft-edge-policies.md#hardwareaccelerationmodeenabled)|
|[HideWebStoreIcon](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HideWebStoreIcon)|No disponible|
|[HomepageIsNewTabPage](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HomepageIsNewTabPage)|[HomepageIsNewTabPage](./microsoft-edge-policies.md#homepageisnewtabpage)|
|[HomepageLocation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HomepageLocation)|[HomepageLocation](./microsoft-edge-policies.md#homepagelocation)|
|[HSTSPolicyBypassList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HSTSPolicyBypassList)|[HSTSPolicyBypassList](./microsoft-edge-policies.md#hstspolicybypasslist)|
|[ImagesAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImagesAllowedForUrls)|[ImagesAllowedForUrls](./microsoft-edge-policies.md#imagesallowedforurls)|
|[ImagesBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImagesBlockedForUrls)|[ImagesBlockedForUrls](./microsoft-edge-policies.md#imagesblockedforurls)|
|[ImportAutofillFormData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportAutofillFormData)|[ImportAutofillFormData](./microsoft-edge-policies.md#importautofillformdata)|
|[ImportBookmarks](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportBookmarks)|[ImportFavorites](./microsoft-edge-policies.md#importfavorites)|
|[ImportHistory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportHistory)|[ImportHistory](./microsoft-edge-policies.md#importhistory)|
|[ImportHomepage](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportHomepage)|[ImportHomepage](./microsoft-edge-policies.md#importhomepage)|
|[ImportSavedPasswords](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportSavedPasswords)|[ImportSavedPasswords](./microsoft-edge-policies.md#importsavedpasswords)|
|[ImportSearchEngine](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportSearchEngine)|[ImportSearchEngine](./microsoft-edge-policies.md#importsearchengine)|
|[IncognitoModeAvailability](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=IncognitoModeAvailability)|[InPrivateModeAvailability](./microsoft-edge-policies.md#inprivatemodeavailability)|
|[InsecureContentAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=InsecureContentAllowedForUrls)|[InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls)|
|[InsecureContentBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=InsecureContentBlockedForUrls)|[InsecureContentBlockedForUrls](./microsoft-edge-policies.md#insecurecontentblockedforurls)|
|[IsolateOrigins](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=IsolateOrigins)|[IsolateOrigins](./microsoft-edge-policies.md#isolateorigins)|
|[JavaScriptAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=JavaScriptAllowedForUrls)|[JavaScriptAllowedForUrls](./microsoft-edge-policies.md#javascriptallowedforurls)|
|[JavaScriptBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=JavaScriptBlockedForUrls)|[JavaScriptBlockedForUrls](./microsoft-edge-policies.md#javascriptblockedforurls)|
|[LegacySameSiteCookieBehaviorEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=LegacySameSiteCookieBehaviorEnabled)|[LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled)|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=LegacySameSiteCookieBehaviorEnabledForDomainList)|[LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist)|
|[LocalDiscoveryEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=LocalDiscoveryEnabled)|No disponible|
|[ManagedBookmarks](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ManagedBookmarks)|[ManagedFavorites](./microsoft-edge-policies.md#managedfavorites)|
|[MaxConnectionsPerProxy](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=MaxConnectionsPerProxy)|[MaxConnectionsPerProxy](./microsoft-edge-policies.md#maxconnectionsperproxy)|
|[MaxInvalidationFetchDelay](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=MaxInvalidationFetchDelay)|No disponible|
|[MediaRouterCastAllowAllIPs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=MediaRouterCastAllowAllIPs)|[MediaRouterCastAllowAllIPs](./microsoft-edge-policies.md#mediaroutercastallowallips)|
|[MetricsReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=MetricsReportingEnabled)|[MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled)|
|[NativeMessagingBlacklist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NativeMessagingBlacklist)|[NativeMessagingBlocklist](./microsoft-edge-policies.md#nativemessagingblocklist)|
|[NativeMessagingUserLevelHosts](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NativeMessagingUserLevelHosts)|[NativeMessagingUserLevelHosts](./microsoft-edge-policies.md#nativemessaginguserlevelhosts)|
|[NativeMessagingWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NativeMessagingWhitelist)|[NativeMessagingAllowlist](./microsoft-edge-policies.md#nativemessagingallowlist)|
|[NetworkPredictionOptions](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NetworkPredictionOptions)|[NetworkPredictionOptions](./microsoft-edge-policies.md#networkpredictionoptions)|
|[NewTabPageLocation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NewTabPageLocation)|[NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation)|
|[NotificationsAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NotificationsAllowedForUrls)|[NotificationsAllowedForUrls](./microsoft-edge-policies.md#notificationsallowedforurls)|
|[NotificationsBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NotificationsBlockedForUrls)|[NotificationsBlockedForUrls](./microsoft-edge-policies.md#notificationsblockedforurls)|
|[NtlmV2Enabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NtlmV2Enabled)|[NtlmV2Enabled](./microsoft-edge-policies.md#ntlmv2enabled)|
|[NTPCustomBackgroundEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NTPCustomBackgroundEnabled)|No disponible|
|[OverrideSecurityRestrictionsOnInsecureOrigin](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=OverrideSecurityRestrictionsOnInsecureOrigin)|[OverrideSecurityRestrictionsOnInsecureOrigin](./microsoft-edge-policies.md#overridesecurityrestrictionsoninsecureorigin)|
|[PasswordLeakDetectionEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordLeakDetectionEnabled)|No disponible|
|[PasswordManagerEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordManagerEnabled)|[PasswordManagerEnabled](./microsoft-edge-policies.md#passwordmanagerenabled)|
|[PasswordProtectionChangePasswordURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordProtectionChangePasswordURL)|[PasswordProtectionChangePasswordURL](./microsoft-edge-policies.md#passwordprotectionchangepasswordurl)|
|[PasswordProtectionLoginURLs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordProtectionLoginURLs)|[PasswordProtectionLoginURLs](./microsoft-edge-policies.md#passwordprotectionloginurls)|
|[PasswordProtectionWarningTrigger](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordProtectionWarningTrigger)|[PasswordProtectionWarningTrigger](./microsoft-edge-policies.md#passwordprotectionwarningtrigger)|
|[PaymentMethodQueryEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PaymentMethodQueryEnabled)|[PaymentMethodQueryEnabled](./microsoft-edge-policies.md#paymentmethodqueryenabled)|
|[PluginsAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PluginsAllowedForUrls)|[PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls)|
|[PluginsBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PluginsBlockedForUrls)|[PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls)|
|[PolicyAtomicGroupsEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PolicyAtomicGroupsEnabled)|No disponible|
|[PolicyDictionaryMultipleSourceMergeList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PolicyDictionaryMultipleSourceMergeList)|No disponible|
|[PolicyListMultipleSourceMergeList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PolicyListMultipleSourceMergeList)|No disponible|
|[PolicyRefreshRate](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PolicyRefreshRate)|No disponible|
|[PopupsAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PopupsAllowedForUrls)|[PopupsAllowedForUrls](./microsoft-edge-policies.md#popupsallowedforurls)|
|[PopupsBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PopupsBlockedForUrls)|[PopupsBlockedForUrls](./microsoft-edge-policies.md#popupsblockedforurls)|
|[PrinterTypeDenyList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrinterTypeDenyList)|No disponible|
|[PrintHeaderFooter](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintHeaderFooter)|[PrintHeaderFooter](./microsoft-edge-policies.md#printheaderfooter)|
|[PrintingAllowedBackgroundGraphicsModes](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintingAllowedBackgroundGraphicsModes)|No disponible|
|[PrintingBackgroundGraphicsDefault](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintingBackgroundGraphicsDefault)|No disponible|
|[PrintingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintingEnabled)|[PrintingEnabled](./microsoft-edge-policies.md#printingenabled)|
|[PrintPreviewUseSystemDefaultPrinter](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintPreviewUseSystemDefaultPrinter)|[PrintPreviewUseSystemDefaultPrinter](./microsoft-edge-policies.md#printpreviewusesystemdefaultprinter)|
|[PromotionalTabsEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PromotionalTabsEnabled)|[PromotionalTabsEnabled](./microsoft-edge-policies.md#promotionaltabsenabled)|
|[PromptForDownloadLocation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PromptForDownloadLocation)|[PromptForDownloadLocation](./microsoft-edge-policies.md#promptfordownloadlocation)|
|[ProxyBypassList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxyBypassList)|[ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist)|
|[ProxyMode](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxyMode)|[ProxyMode](./microsoft-edge-policies.md#proxymode)|
|[ProxyPacUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxyPacUrl)|[ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl)|
|[ProxyServer](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxyServer)|[ProxyServer](./microsoft-edge-policies.md#proxyserver)|
|[ProxySettings](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxySettings)|[ProxySettings](./microsoft-edge-policies.md#proxysettings)|
|[QuicAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=QuicAllowed)|[QuicAllowed](./microsoft-edge-policies.md#quicallowed)|
|[RegisteredProtocolHandlers](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RegisteredProtocolHandlers)|[RegisteredProtocolHandlers](./microsoft-edge-policies.md#registeredprotocolhandlers)|
|[RelaunchNotification](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RelaunchNotification)|[RelaunchNotification](./microsoft-edge-policies.md#relaunchnotification)|
|[RelaunchNotificationPeriod](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RelaunchNotificationPeriod)|[RelaunchNotificationPeriod](./microsoft-edge-policies.md#relaunchnotificationperiod)|
|[RemoteAccessHostAllowClientPairing](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowClientPairing)|No disponible|
|[RemoteAccessHostAllowFileTransfer](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowFileTransfer)|No disponible|
|[RemoteAccessHostAllowGnubbyAuth](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowGnubbyAuth)|No disponible|
|[RemoteAccessHostAllowRelayedConnection](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowRelayedConnection)|No disponible|
|[RemoteAccessHostAllowUiAccessForRemoteAssistance](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowUiAccessForRemoteAssistance)|No disponible|
|[RemoteAccessHostClientDomainList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostClientDomainList)|No disponible|
|[RemoteAccessHostDomainList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostDomainList)|No disponible|
|[RemoteAccessHostFirewallTraversal](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostFirewallTraversal)|No disponible|
|[RemoteAccessHostMatchUsername](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostMatchUsername)|No disponible|
|[RemoteAccessHostRequireCurtain](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostRequireCurtain)|No disponible|
|[RemoteAccessHostTalkGadgetPrefix](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostTalkGadgetPrefix)|No disponible|
|[RemoteAccessHostTokenUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostTokenUrl)|No disponible|
|[RemoteAccessHostTokenValidationCertificateIssuer](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostTokenValidationCertificateIssuer)|No disponible|
|[RemoteAccessHostTokenValidationUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostTokenValidationUrl)|No disponible|
|[RemoteAccessHostUdpPortRange](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostUdpPortRange)|No disponible|
|[RendererCodeIntegrityEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RendererCodeIntegrityEnabled)|[RendererCodeIntegrityEnabled](./microsoft-edge-policies.md#renderercodeintegrityenabled)|
|[ReportExtensionsAndPluginsData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportExtensionsAndPluginsData)|No disponible|
|[ReportMachineIDData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportMachineIDData)|No disponible|
|[ReportPolicyData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportPolicyData)|No disponible|
|[ReportSafeBrowsingData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportSafeBrowsingData)|No disponible|
|[ReportUserIDData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportUserIDData)|No disponible|
|[ReportVersionData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportVersionData)|No disponible|
|[RequireOnlineRevocationChecksForLocalAnchors](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RequireOnlineRevocationChecksForLocalAnchors)|[RequireOnlineRevocationChecksForLocalAnchors](./microsoft-edge-policies.md#requireonlinerevocationchecksforlocalanchors)|
|[RestoreOnStartup](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RestoreOnStartup)|[RestoreOnStartup](./microsoft-edge-policies.md#restoreonstartup)|
|[RestoreOnStartupURLs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RestoreOnStartupURLs)|[RestoreOnStartupURLs](./microsoft-edge-policies.md#restoreonstartupurls)|
|[RestrictSigninToPattern](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RestrictSigninToPattern)|[RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern)|
|[RoamingProfileLocation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RoamingProfileLocation)|No disponible|
|[RoamingProfileSupportEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RoamingProfileSupportEnabled)|No disponible|
|[RunAllFlashInAllowMode](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RunAllFlashInAllowMode)|[RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode)|
|[SafeBrowsingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeBrowsingEnabled)|[SmartScreenEnabled](./microsoft-edge-policies.md#smartscreenenabled)|
|[SafeBrowsingExtendedReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeBrowsingExtendedReportingEnabled)|No disponible|
|[SafeBrowsingForTrustedSourcesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeBrowsingForTrustedSourcesEnabled)|[SmartScreenForTrustedDownloadsEnabled](./microsoft-edge-policies.md#smartscreenfortrusteddownloadsenabled)|
|[SafeBrowsingWhitelistDomains](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeBrowsingWhitelistDomains)|[SmartScreenAllowListDomains](./microsoft-edge-policies.md#smartscreenallowlistdomains)|
|[SafeSitesFilterBehavior](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeSitesFilterBehavior)|No disponible|
|[SavingBrowserHistoryDisabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SavingBrowserHistoryDisabled)|[SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled)|
|[SearchSuggestEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SearchSuggestEnabled)|[SearchSuggestEnabled](./microsoft-edge-policies.md#searchsuggestenabled)|
|[SecurityKeyPermitAttestation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SecurityKeyPermitAttestation)|[SecurityKeyPermitAttestation](./microsoft-edge-policies.md#securitykeypermitattestation)|
|[SendFilesForMalwareCheck](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SendFilesForMalwareCheck)|No disponible|
|[SharedClipboardEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SharedClipboardEnabled)|No disponible|
|[ShowAppsShortcutInBookmarkBar](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ShowAppsShortcutInBookmarkBar)|[ShowOfficeShortcutInFavoritesBar](./microsoft-edge-policies.md#showofficeshortcutinfavoritesbar)|
|[ShowCastIconInToolbar](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ShowCastIconInToolbar)|[ShowCastIconInToolbar](./microsoft-edge-policies.md#showcasticonintoolbar)|
|[ShowHomeButton](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ShowHomeButton)|[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton)|
|[SignedHTTPExchangeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SignedHTTPExchangeEnabled)|[SignedHTTPExchangeEnabled](./microsoft-edge-policies.md#signedhttpexchangeenabled)|
|[SitePerProcess](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SitePerProcess)|[SitePerProcess](./microsoft-edge-policies.md#siteperprocess)|
|[SpellcheckEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SpellcheckEnabled)|[SpellcheckEnabled](./microsoft-edge-policies.md#spellcheckenabled)|
|[SpellcheckLanguage](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SpellcheckLanguage)|[SpellcheckLanguage](./microsoft-edge-policies.md#spellchecklanguage)|
|[SpellcheckLanguageBlacklist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SpellcheckLanguageBlacklist)|[SpellcheckLanguageBlocklist](./microsoft-edge-policies.md#spellchecklanguageblocklist)|
|[SpellCheckServiceEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SpellCheckServiceEnabled)|No disponible|
|[SSLErrorOverrideAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SSLErrorOverrideAllowed)|[SSLErrorOverrideAllowed](./microsoft-edge-policies.md#sslerroroverrideallowed)|
|[SSLVersionMin](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SSLVersionMin)|[SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)|
|[StricterMixedContentTreatmentEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=StricterMixedContentTreatmentEnabled)|No disponible|
|[SuppressUnsupportedOSWarning](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SuppressUnsupportedOSWarning)|[SuppressUnsupportedOSWarning](./microsoft-edge-policies.md#suppressunsupportedoswarning)|
|[SyncDisabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SyncDisabled)|[SyncDisabled](./microsoft-edge-policies.md#syncdisabled)|
|[SyncTypesListDisabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SyncTypesListDisabled)|No disponible|
|[TabFreezingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TabFreezingEnabled)|[TabFreezingEnabled](./microsoft-edge-policies.md#tabfreezingenabled)|
|[TaskManagerEndProcessEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TaskManagerEndProcessEnabled)|[TaskManagerEndProcessEnabled](./microsoft-edge-policies.md#taskmanagerendprocessenabled)|
|[ThirdPartyBlockingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ThirdPartyBlockingEnabled)|No disponible|
|[TLS13HardeningForLocalAnchorsEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TLS13HardeningForLocalAnchorsEnabled)|No disponible|
|[TotalMemoryLimitMb](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TotalMemoryLimitMb)|[TotalMemoryLimitMb](./microsoft-edge-policies.md#totalmemorylimitmb)|
|[TranslateEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TranslateEnabled)|[TranslateEnabled](./microsoft-edge-policies.md#translateenabled)|
|[UnsafeEventsReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=UnsafeEventsReportingEnabled)|No disponible|
|[URLBlacklist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLBlacklist)|[URLBlocklist](./microsoft-edge-policies.md#urlblocklist)|
|[UrlKeyedAnonymizedDataCollectionEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=UrlKeyedAnonymizedDataCollectionEnabled)|No disponible|
|[URLsToCheckComplianceOfDownloadedContent](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLsToCheckComplianceOfDownloadedContent)|No disponible|
|[URLsToCheckForMalwareOfUploadedContent](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLsToCheckForMalwareOfUploadedContent)|No disponible|
|[URLsToNotCheckComplianceOfUploadedContent](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLsToNotCheckComplianceOfUploadedContent)|No disponible|
|[URLWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLWhitelist)|[URLAllowlist](./microsoft-edge-policies.md#urlallowlist)|
|[UserDataDir](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=UserDataDir)|[UserDataDir](./microsoft-edge-policies.md#userdatadir)|
|[UserFeedbackAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=UserFeedbackAllowed)|[UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)|
|[VariationsRestrictParameter](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=VariationsRestrictParameter)|No disponible|
|[VideoCaptureAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=VideoCaptureAllowed)|[VideoCaptureAllowed](./microsoft-edge-policies.md#videocaptureallowed)|
|[VideoCaptureAllowedUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=VideoCaptureAllowedUrls)|[VideoCaptureAllowedUrls](./microsoft-edge-policies.md#videocaptureallowedurls)|
|[WebAppInstallForceList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebAppInstallForceList)|[WebAppInstallForceList](./microsoft-edge-policies.md#webappinstallforcelist)|
|[WebComponentsV0Enabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebComponentsV0Enabled)|[WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled)|
|[WebRtcEventLogCollectionAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebRtcEventLogCollectionAllowed)|No disponible|
|[WebRtcLocalIpsAllowedUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebRtcLocalIpsAllowedUrls)|[WebRtcLocalIpsAllowedUrls](./microsoft-edge-policies.md#webrtclocalipsallowedurls)|
|[WebRtcUdpPortRange](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebRtcUdpPortRange)|[WebRtcUdpPortRange](./microsoft-edge-policies.md#webrtcudpportrange)|
|[WebUsbAllowDevicesForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebUsbAllowDevicesForUrls)|[WebUsbAllowDevicesForUrls](./microsoft-edge-policies.md#webusballowdevicesforurls)|
|[WebUsbAskForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebUsbAskForUrls)|[WebUsbAskForUrls](./microsoft-edge-policies.md#webusbaskforurls)|
|[WebUsbBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebUsbBlockedForUrls)|[WebUsbBlockedForUrls](./microsoft-edge-policies.md#webusbblockedforurls)|
|[WPADQuickCheckEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WPADQuickCheckEnabled)|[WPADQuickCheckEnabled](./microsoft-edge-policies.md#wpadquickcheckenabled)|

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Configuración de Microsoft Edge](configure-microsoft-edge.md)
- [Referencia de directiva de explorador](microsoft-edge-policies.md)