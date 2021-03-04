---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
ms.openlocfilehash: 24a74380fe6930c730357476792cea81ebaf7b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911705"
---
# Update-AzFunctionAppSetting

## 簡介
新增或更新功能應用程式中的應用程式設定。

## 語法

### ByName (預設) 
```
Update-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSetting <Hashtable>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionAppSetting -AppSetting <Hashtable> -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 描述
新增或更新功能應用程式中的應用程式設定。

## 例子

### 範例 1：在函數應用程式中新增應用程式設定。
```powershell
PS C:\> Update-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSetting @{"Name1" = "Value1"}
```

此命令在功能應用程式中新增應用程式設定。

## 參數

### -AppSetting
包含按鍵和值的雜湊表描述函數應用程式中要新增或更新的應用程式設定。
例如：@{"myappsetting"="123"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -強制
強制 Cmdlet 更新功能應用程式設定，而不會提示確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
函數應用程式的名稱。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源所屬的資源組名。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Azure 訂閱識別碼。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，提示您確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite

## 輸出

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary

## 筆記

別名

複雜的參數屬性

若要建立下列描述的參數，請建構包含適當屬性的雜湊表。 有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。


INPUTOBJECT： <ISite> 
  - `Location <String>`：資源位置。
  - `CloningInfoSourceWebAppId <String>`：來源應用程式的 ARM 資源識別碼。 應用程式資源識別碼為適用于其他插槽的表單//訂閱/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}，適用于其他插槽和/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}。
  - `[Kind <String>]`：資源類型。
  - `[Tag <IResourceTags>]`：資源標記。
    - `[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。
  - `[ClientAffinityEnabled <Boolean?>]`： <code>true</code> 啟用用戶端關聯 <code>false</code> 性;停止傳送會話關聯 Cookie，此 Cookie 會在同一個會話中將用戶端要求路由至相同的實例。 預設值 <code>true</code> 為 。
  - `[ClientCertEnabled <Boolean?>]`： <code>true</code> 若要啟用用戶端憑證驗證 (TLS 相互驗證) ;否則 <code>false</code> ，。 預設值 <code>false</code> 為 。
  - `[ClientCertExclusionPath <String>]`：用戶端憑證驗證逗號分隔排除路徑
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`：複製的應用程式會優先于應用程式設定。 如果指定，這些設定會優先于從來源應用程式複製的設定。 否則，會保留來源應用程式的應用程式設定。
    - `[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。
  - `[CloningInfoCloneCustomHostName <Boolean?>]`： <code>true</code> 從來源應用程式複製自訂主機名稱;否則 <code>false</code> ，.
  - `[CloningInfoCloneSourceControl <Boolean?>]`： <code>true</code> 從來源應用程式複製原始程式碼管理;否則 <code>false</code> ，.
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`： <code>true</code> 設定來源和目的地應用程式的負載平衡。
  - `[CloningInfoCorrelationId <String>]`：複製作業的相關識別碼。 此識別碼將多個複製作業系在一起，以使用相同的快照。
  - `[CloningInfoHostingEnvironment <String>]`：應用程式服務環境。
  - `[CloningInfoOverwrite <Boolean?>]`： <code>true</code> 以覆寫目的地應用程式;否則 <code>false</code> ，.
  - `[CloningInfoSourceWebAppLocation <String>]`：來源應用程式的位置，例如：美國西部或北歐洲
  - `[CloningInfoTrafficManagerProfileId <String>]`：要使用流量管理員設定檔的 ARM 資源識別碼 ，如果有。 Traffic Manager 資源識別碼是表單 /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}。
  - `[CloningInfoTrafficManagerProfileName <String>]`：要建立的流量管理員設定檔名稱。 只有在流量管理員設定檔不存在時，才需要這項功能。
  - `[Config <ISiteConfig>]`：應用程式的組配置。
    - `IsPushEnabled <Boolean>`：套用或設定旗標，指出推入端點是否已啟用。
    - `[ActionMinProcessExecutionTime <String>]`：執行動作前必須執行程式的最小時間
    - `[ActionType <AutoHealActionType?>]`：預先定義要採取的動作。
    - `[AlwaysOn <Boolean?>]`： <code>true</code> 如果已啟用 Always On;否則 <code>false</code> ，.
    - `[ApiDefinitionUrl <String>]`：API 定義的 URL。
    - `[ApiManagementConfigId <String>]`：APIM-Api識別碼。
    - `[AppCommandLine <String>]`：啟動 App 命令列。
    - `[AppSetting <INameValuePair[]>]`：應用程式設定。
      - `[Name <String>]`：配對名稱。
      - `[Value <String>]`：配對值。
    - `[AutoHealEnabled <Boolean?>]`： <code>true</code> 如果已啟用自動自動修復;否則 <code>false</code> ，.
    - `[AutoSwapSlotName <String>]`：自動交換插槽名稱。
    - `[ConnectionString <IConnStringInfo[]>]`：連接字串。
      - `[ConnectionString <String>]`：連接字串值。
      - `[Name <String>]`：連接字串的名稱。
      - `[Type <ConnectionStringType?>]`：資料庫類型。
    - `[CorAllowedOrigin <String[]>]`：獲取或設定應允許撥打跨來源電話的來源 (例如 http://example.com:12345) ： 使用 "*" 允許所有專案。
    - `[CorSupportCredentials <Boolean?>]`：獲取或設定是否允許具有認證之 CORS 要求。 請參閱         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         更多詳細資料。
    - `[CustomActionExe <String>]`：執行可執行檔。
    - `[CustomActionParameter <String>]`：可執行檔的參數。
    - `[DefaultDocument <String[]>]`：預設檔。
    - `[DetailedErrorLoggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用詳細的錯誤記錄，否則 <code>false</code> ，.
    - `[DocumentRoot <String>]`：檔根目錄。
    - `[DynamicTagsJson <String>]`：獲取或設定包含動態標記清單的 JSON 字串，該清單會從推入註冊端點中的使用者聲明進行評估。
    - `[ExperimentRampUpRule <IRampUpRule[]>]`：快速上線規則清單。
      - `[ActionHostName <String>]`：位置的主機名稱，如果決定將流量重新導向到該位置。 例如， myapp-stage.azurewebsites.net。
      - `[ChangeDecisionCallbackUrl <String>]`：您可以在 TiPCallback 網站擴充功能中提供自訂決策演算法，以指定 URL。 請參閱基架和合約的 TiPCallback 網站擴充功能。         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`：指定以分鐘為單位的間隔，以重新計算 ReroutePercentage。
      - `[ChangeStep <Double?>]`：在自動上手情況下，這是要新增/移除的步驟，直到到達 \n 或 <code>ReroutePercentage</code> <code>MinReroutePercentage</code>         <code>MaxReroutePercentage</code> 。 您可以在 TiPCallback 網站擴充功能中，以 .\nCustom 決策演算法指定的每 N 分鐘檢查網站 <code>ChangeIntervalInMinutes</code> 度量，URL 可以在其中指定 <code>ChangeDecisionCallbackUrl</code> 。
      - `[MaxReroutePercentage <Double?>]`：指定 ReroutePercentage 會維持在下方的上限。
      - `[MinReroutePercentage <Double?>]`：指定 ReroutePercentage 會維持在下限上方。
      - `[Name <String>]`：路由規則的名稱。 建議的名稱會指向在實驗中接收流量的插槽。
      - `[ReroutePercentage <Double?>]`：將會重新導向至的流量百分比 <code>ActionHostName</code> 。
    - `[FtpsState <FtpsState?>]`：FTP /FTPS 服務的狀態
    - `[HandlerMapping <IHandlerMapping[]>]`：處理常式的映射。
      - `[Argument <String>]`：要傳遞到腳本處理器的命令列引數。
      - `[Extension <String>]`：具有此副檔名的要求將會使用指定的 FastCGI 應用程式處理。
      - `[ScriptProcessor <String>]`：FastCGI 應用程式的絕對路徑。
    - `[HealthCheckPath <String>]`：健康狀態檢查路徑
    - `[Http20Enabled <Boolean?>]`：HTTP20Enabled：設定網站以允許用戶端以 HTTP2.0 進行連結
    - `[HttpLoggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用 HTTP 記錄，否則 <code>false</code> ，.
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`：主要 IP 安全性限制。
      - `[Action <String>]`：允許或拒絕此 IP 範圍的存取。
      - `[Description <String>]`：IP 限制規則描述。
      - `[IPAddress <String>]`：安全性限制的 IP 位址有效。         它可以是純粹 ipv4 位址 (子網路遮罩屬性) 或 CIDR 標記法 ，例如 ipv4/mask (前位比對) 。 對於 CIDR，不得指定子網路遮罩屬性。
      - `[Name <String>]`：IP 限制規則名稱。
      - `[Priority <Int32?>]`：IP 限制規則的優先順序。
      - `[SubnetMask <String>]`：限制有效之 IP 位址範圍的子網屏蔽。
      - `[SubnetTrafficTag <Int32?>]`： (子網) 標記
      - `[Tag <IPFilterTag?>]`：定義此 IP 篩選會用於什麼。 這是為了支援對代理程式進行 IP 篩選。
      - `[VnetSubnetResourceId <String>]`：虛擬網路資源識別碼
      - `[VnetTrafficTag <Int32?>]`： (內部) Vnet 流量標記
    - `[JavaContainer <String>]`：JAVA 容器。
    - `[JavaContainerVersion <String>]`：JAVA 容器版本。
    - `[JavaVersion <String>]`：JAVA 版本。
    - `[LimitMaxDiskSizeInMb <Int64?>]`：允許的磁片大小使用量上限 ，以 MB 為單位。
    - `[LimitMaxMemoryInMb <Int64?>]`：允許記憶體使用量上限 ，以 MB 為單位。
    - `[LimitMaxPercentageCpu <Double?>]`：允許的 CPU 使用量百分比上限。
    - `[LinuxFxVersion <String>]`：Linux App 架構及版本
    - `[LoadBalancing <SiteLoadBalancing?>]`：網站負載平衡。
    - `[LocalMySqlEnabled <Boolean?>]`： <code>true</code> 啟用本地 MySQL;否則 <code>false</code> ，.
    - `[LogsDirectorySizeLimit <Int32?>]`：HTTP 記錄目錄大小限制。
    - `[MachineKeyDecryption <String>]`：用於解密的演算法。
    - `[MachineKeyDecryptionKey <String>]`：解密金鑰。
    - `[MachineKeyValidation <String>]`：MachineKey 驗證。
    - `[MachineKeyValidationKey <String>]`：驗證鍵。
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`：受管理的管線模式。
    - `[ManagedServiceIdentityId <Int32?>]`：Managed Service Identity Id
    - `[MinTlsVersion <SupportedTlsVersions?>]`：MinTlsVersion：設定 SSL 要求所需的 TLS 最低版本
    - `[NetFrameworkVersion <String>]`：.NET Framework 版本。
    - `[NodeVersion <String>]`：版本Node.js。
    - `[NumberOfWorker <Int32?>]`：員工人數。
    - `[PhpVersion <String>]`：PHP 版本。
    - `[PowerShellVersion <String>]`：PowerShell 版本。
    - `[PreWarmedInstanceCount <Int32?>]`：預先警告的實例數目。         此設定僅適用于消費和消費計畫
    - `[PublishingUsername <String>]`：發佈使用者名稱。
    - `[PushKind <String>]`：資源類型。
    - `[PythonVersion <String>]`：版本為Python。
    - `[RemoteDebuggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用遠端問題，否則為 <code>false</code> 。
    - `[RemoteDebuggingVersion <String>]`：遠端測試版本。
    - `[RequestCount <Int32?>]`：要求計數。
    - `[RequestTimeInterval <String>]`：時間間隔。
    - `[RequestTracingEnabled <Boolean?>]`： <code>true</code> 如果已啟用要求追蹤;否則 <code>false</code> ，。
    - `[RequestTracingExpirationTime <DateTime?>]`：要求追蹤到期日。
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`：scm 的 IP 安全性限制。
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`：scm 使用主要之 IP 安全性限制。
    - `[ScmType <ScmType?>]`：SCM 類型。
    - `[SlowRequestCount <Int32?>]`：要求計數。
    - `[SlowRequestTimeInterval <String>]`：時間間隔。
    - `[SlowRequestTimeTaken <String>]`：所花時間。
    - `[TagWhitelistJson <String>]`：獲取或設定 JSON 字串，其中包含由推入註冊端點使用之白名單的標記清單。
    - `[TagsRequiringAuth <String>]`：獲取或設定 JSON 字串，其中包含要求在推入註冊端點使用使用者驗證的標記清單。         標記可以包含字母數位字元，而下列字元：'_'、'@'、'#'、'.'、'：'、'-'。         驗證應在 PushRequestHandler 執行。
    - `[TracingOption <String>]`：追蹤選項。
    - `[TriggerPrivateBytesInKb <Int32?>]`：以私人位元組為基礎的規則。
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`：以狀態碼為基礎的規則。
      - `[Count <Int32?>]`：要求計數。
      - `[Status <Int32?>]`：HTTP 狀態碼。
      - `[SubStatus <Int32?>]`：要求子狀態。
      - `[TimeInterval <String>]`：時間間隔。
      - `[Win32Status <Int32?>]`：Win32 錯誤碼。
    - `[Use32BitWorkerProcess <Boolean?>]`： <code>true</code> 使用 32 位的工作者程式;否則 <code>false</code> ，。
    - `[VirtualApplication <IVirtualApplication[]>]`：虛擬應用程式。
      - `[PhysicalPath <String>]`：實體路徑。
      - `[PreloadEnabled <Boolean?>]`： <code>true</code> 如果已啟用預先載入;否則 <code>false</code> ，.
      - `[VirtualDirectory <IVirtualDirectory[]>]`：虛擬應用程式的虛擬目錄。
        - `[PhysicalPath <String>]`：實體路徑。
        - `[VirtualPath <String>]`：虛擬應用程式的路徑。
      - `[VirtualPath <String>]`：虛擬路徑。
    - `[VnetName <String>]`：虛擬網路名稱。
    - `[WebSocketsEnabled <Boolean?>]`： <code>true</code> 如果啟用 WebSocket;否則 <code>false</code> ，.
    - `[WindowsFxVersion <String>]`：Xenon App Framework 與版本
    - `[XManagedServiceIdentityId <Int32?>]`：明確 Managed Service 身分識別識別碼
  - `[ContainerSize <Int32?>]`：函數容器的大小。
  - `[DailyMemoryTimeQuota <Int32?>]`：僅適用于動態應用程式 (允許的最大每日記憶體配額) 。
  - `[Enabled <Boolean?>]`： <code>true</code> 如果應用程式已啟用;否則 <code>false</code> ，. 將此值設定為 False 會停用應用程式 (應用程式離線) 。
  - `[HostNameSslState <IHostNameSslState[]>]`：Hostname SSL 狀態用來管理應用程式主機名稱的 SSL 綁定。
    - `[HostType <HostType?>]`：表示 hostname 是標準或存放庫主機名稱。
    - `[Name <String>]`：Hostname。
    - `[SslState <SslState?>]`：SSL 類型。
    - `[Thumbprint <String>]`：SSL 憑證指紋。
    - `[ToUpdate <Boolean?>]`：設定 <code>true</code> 為更新現有的主機名稱。
    - `[VirtualIP <String>]`：如果已啟用 IP 型 SSL，則指派給主機名稱的虛擬 IP 位址。
  - `[HostNamesDisabled <Boolean?>]`： <code>true</code> 停用應用程式的公用主機名稱;否則 <code>false</code> ，。          如果 <code>true</code> ，應用程式只能透過 API 管理程式進行。
  - `[HostingEnvironmentProfileId <String>]`：應用程式服務環境的資源識別碼。
  - `[HttpsOnly <Boolean?>]`：HTTPsOnly：將網站設定為僅接受 HTTPs 要求。 Http 要求重新導向的問題
  - `[HyperV <Boolean?>]`：Hyper-V 沙箱。
  - `[IdentityType <ManagedServiceIdentityType?>]`：受管理服務身分識別的類型。
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`：已指派與資源關聯的使用者身分清單。 使用者身分識別字典金鑰參照為表單中的 ARM 資源識別碼：'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`：這表示任何屬性都可以新增到這個物件。
  - `[IsXenon <Boolean?>]`：過時：Hyper-V 沙箱。
  - `[RedundancyMode <RedundancyMode?>]`：網站冗余模式
  - `[Reserved <Boolean?>]`： <code>true</code> 如果保留，否則為 <code>false</code> 。
  - `[ScmSiteAlsoStopped <Boolean?>]`： <code>true</code> 在應用程式停止 (時) KUDU 或網站中停止 SCM;否則， <code>false</code> 預設值為 <code>false</code> 。
  - `[ServerFarmId <String>]`：相關應用程式服務方案的資源識別碼，格式為：「/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}"。

## 相關連結

