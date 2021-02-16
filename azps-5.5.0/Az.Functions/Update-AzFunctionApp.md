---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
ms.openlocfilehash: 08485ab1686b87c6421f456b53caa5d1deaf0c7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133215"
---
# Update-AzFunctionApp

## 摘要
更新函數 app。

## 句法

### ByName (預設) 
```
Update-AzFunctionApp -Name <String> -ResourceGroupName <String> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionApp -InputObject <ISite> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## 說明
更新函數 app。

## 示例

### 範例1：更新函數 app 託管方案。
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -PlanName NewPlanName 
```

這個命令會更新函數 app 託管方案。

### 範例2：針對函數 app 設定 SystemAssigned managed 身分識別。
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType SystemAssigned 
```

這個命令會為函數 app 設定 SystemAssigned managed 身分識別。

### 範例3：更新函數 app Application Insights。
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -ApplicationInsightsName ApplicationInsightsProjectName 
```

這個命令會更新函數 app Application Insights。

### 範例3：從函數 app 移除受管理的身分識別。
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType None 
```

這個命令會從函數 app 移除受管理的身分識別。

## 參數

### -ApplicationInsightsKey
要新增之 App Insights 的檢測鍵。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationInsightsName
要新增至函數 App 之現有 App Insights 專案的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
將 Cmdlet 作為背景作業執行。

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

### -IdentityID
指定與函數 app 相關聯的使用者識別碼清單。
使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
指定用於函數 app 的身分識別類型。
類型 "None" 將移除函數 app 中的任何身分識別。
此參數可接受的值為：-SystemAssigned-UserAssigned-None

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。

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

### -NoWait
在作業完成之前，立即開始作業並立即返回。
若要判斷該作業是否已順利完成，請使用一些其他的機制。

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

### -PlanName
服務方案的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。

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
Azure 訂閱 ID。

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

### -Tag
資源標記。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

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
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### ISite 中的 Api20190801，然後再

## 輸出

### ISite 中的 Api20190801，然後再

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


INPUTOBJECT <ISite> ： 
  - `Location <String>`：資源位置。
  - `CloningInfoSourceWebAppId <String>`：源 app 的 ARM 資源識別碼。 App 資源識別碼的形式是生產槽的表單/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}，而其他槽的/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} 則是。
  - `[Kind <String>]`：資源類型。
  - `[Tag <IResourceTags>]`：資源標記。
    - `[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。
  - `[ClientAffinityEnabled <Boolean?>]`： <code>true</code> 若要啟用客戶關係 <code>false</code> ，請停止傳送會話相關性 cookie，該 cookie 會將同一個會話中的用戶端要求路由至同一個實例。 預設值為 <code>true</code> 。
  - `[ClientCertEnabled <Boolean?>]`： <code>true</code> 若要啟用用戶端憑證驗證 (TLS 相互驗證) ; 否則， <code>false</code> 。 預設值為 <code>false</code> 。
  - `[ClientCertExclusionPath <String>]`：用戶端憑證驗證以逗號分隔的排除路徑
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`：適用于克隆之 app 的應用程式設定覆寫。 如果已指定，這些設定會覆寫從源 app 克隆的設定。 否則，來源應用程式的應用程式設定會保留下來。
    - `[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。
  - `[CloningInfoCloneCustomHostName <Boolean?>]`： <code>true</code> 若要從來源 app 克隆自訂主機名稱，否則， <code>false</code> 。
  - `[CloningInfoCloneSourceControl <Boolean?>]`： <code>true</code> 若要從來源應用程式克隆來源控制，否則， <code>false</code> 。
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`： <code>true</code> 為來源和目的地 app 設定負載平衡。
  - `[CloningInfoCorrelationId <String>]`：克隆作業的相關 ID。 這個識別碼將多個克隆作業結合在一起，以使用相同的快照。
  - `[CloningInfoHostingEnvironment <String>]`： App 服務環境。
  - `[CloningInfoOverwrite <Boolean?>]`： <code>true</code> 要覆寫目的地 app; 否則， <code>false</code> 。
  - `[CloningInfoSourceWebAppLocation <String>]`：來源應用程式的位置（例如：西美國或北歐）
  - `[CloningInfoTrafficManagerProfileId <String>]`：要使用之流量管理器設定檔的 ARM 資源識別碼（如果存在的話）。 流量管理員資源識別碼的形式為/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}。
  - `[CloningInfoTrafficManagerProfileName <String>]`：要建立之流量管理器設定檔的名稱。 只有流量管理器設定檔尚不存在時，才需要這麼做。
  - `[Config <ISiteConfig>]`：應用程式的配置。
    - `IsPushEnabled <Boolean>`：取得或設定指示是否已啟用推播端點的標誌。
    - `[ActionMinProcessExecutionTime <String>]`：在採取動作前必須執行的最短時間。
    - `[ActionType <AutoHealActionType?>]`：預先定義的要採取的動作。
    - `[AlwaysOn <Boolean?>]`： <code>true</code> 如果啟用 [永不開啟]，則為（否則，） <code>false</code> 。
    - `[ApiDefinitionUrl <String>]`： API 定義的 URL。
    - `[ApiManagementConfigId <String>]`： APIM-Api 識別碼。
    - `[AppCommandLine <String>]`：啟動 App 命令列。
    - `[AppSetting <INameValuePair[]>]`：應用程式設定。
      - `[Name <String>]`：配對名。
      - `[Value <String>]`： [配對] 值。
    - `[AutoHealEnabled <Boolean?>]`： <code>true</code> 如果已啟用自動修復，則為（否則，） <code>false</code> 。
    - `[AutoSwapSlotName <String>]`：自動交換槽名稱。
    - `[ConnectionString <IConnStringInfo[]>]`：連接字串。
      - `[ConnectionString <String>]`：連接字串值。
      - `[Name <String>]`：連接字串的名稱。
      - `[Type <ConnectionStringType?>]`：資料庫的類型。
    - `[CorAllowedOrigin <String[]>]`：取得或設定允許進行交叉起源撥打電話的來源清單 (例如： http://example.com:12345) 。 使用 "*" 全部允許。
    - `[CorSupportCredentials <Boolean?>]`：取得或設定是否允許含身分驗證的 CORS 要求。 如需詳細         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         資訊，請參閱。
    - `[CustomActionExe <String>]`：要執行的可執行檔。
    - `[CustomActionParameter <String>]`：可執行檔的參數。
    - `[DefaultDocument <String[]>]`：預設檔。
    - `[DetailedErrorLoggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用詳細的錯誤記錄，則為（否則，） <code>false</code> 。
    - `[DocumentRoot <String>]`：檔根。
    - `[DynamicTagsJson <String>]`：取得或設定一個 JSON 字串，其中包含將從推入註冊端點中的使用者宣告評估的動態標記清單。
    - `[ExperimentRampUpRule <IRampUpRule[]>]`：提升式規則清單。
      - `[ActionHostName <String>]`：如果決定要將流量重新導向到的槽主機名稱。 例如. myapp-stage.azurewebsites.net。
      - `[ChangeDecisionCallbackUrl <String>]`：您可以在 TiPCallback 網站副檔名中提供自訂決策演算法，您可以指定此 URL。 請參閱架設與合約的 TiPCallback 網站延伸。         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`：指定要重新評估 ReroutePercentage 的間隔時間（以分鐘為單位）。
      - `[ChangeStep <Double?>]`：在自動向上斜坡案例中，這是要新增/移除的步驟， <code>ReroutePercentage</code> 直到到達 \n <code>MinReroutePercentage</code> 或         <code>MaxReroutePercentage</code> 。 在 .\NCustom 決策演算法中指定的每 N 分鐘數，都 <code>ChangeIntervalInMinutes</code> 可以在 TiPCallback 網站副檔名中提供，您可以在其中指定 URL <code>ChangeDecisionCallbackUrl</code> 。
      - `[MaxReroutePercentage <Double?>]`：指定 ReroutePercentage 將持續的上限。
      - `[MinReroutePercentage <Double?>]`：指定 ReroutePercentage 將持續的較低邊界。
      - `[Name <String>]`：路由規則的名稱。 建議的名稱是指向將在實驗中接收流量的槽。
      - `[ReroutePercentage <Double?>]`：將會重新導向之流量的百分比 <code>ActionHostName</code> 。
    - `[FtpsState <FtpsState?>]`： FTP/FTPS 服務的狀態
    - `[HandlerMapping <IHandlerMapping[]>]`：處理常式對應。
      - `[Argument <String>]`：要傳送至腳本處理器的命令列引數。
      - `[Extension <String>]`：具有此延伸的要求將會使用指定的 FastCGI 應用程式來處理。
      - `[ScriptProcessor <String>]`： FastCGI 應用程式的絕對路徑。
    - `[HealthCheckPath <String>]`：健康情況檢查路徑
    - `[Http20Enabled <Boolean?>]`： Http20Enabled：將網站設定為允許用戶端經由 HTTP 2.0 連線
    - `[HttpLoggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用 HTTP 記錄，則為，否則為 <code>false</code> 。
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`：主要的 IP 安全性限制。
      - `[Action <String>]`：允許或拒絕此 IP 範圍的存取權。
      - `[Description <String>]`： IP 限制規則描述。
      - `[IPAddress <String>]`： [安全性限制] 適用的 IP 位址。         它可以是純 ipv4 位址的形式 (必要的 SubnetMask 屬性) 或 CIDR 符號（例如 ipv4/遮罩 (前導位相符）) 。 若是 CIDR，則不得指定 SubnetMask 屬性。
      - `[Name <String>]`： IP 限制規則名稱。
      - `[Priority <Int32?>]`： IP 限制規則的優先順序。
      - `[SubnetMask <String>]`：限制有效的 IP 位址範圍的子網路遮罩。
      - `[SubnetTrafficTag <Int32?>]`： (內部) 子網流量標記
      - `[Tag <IPFilterTag?>]`：定義此 IP 篩選將用於何種用途。 這是為了支援在 proxy 上進行 IP 篩選。
      - `[VnetSubnetResourceId <String>]`：虛擬網路資源識別碼
      - `[VnetTrafficTag <Int32?>]`： (內部) Vnet 流量標記
    - `[JavaContainer <String>]`： JAVA 容器。
    - `[JavaContainerVersion <String>]`： JAVA 容器版本。
    - `[JavaVersion <String>]`： JAVA 版本。
    - `[LimitMaxDiskSizeInMb <Int64?>]`：允許的磁片大小上限，以 MB 為單位。
    - `[LimitMaxMemoryInMb <Int64?>]`：允許的最大記憶體使用量（MB）。
    - `[LimitMaxPercentageCpu <Double?>]`：允許的 CPU 使用量上限百分比。
    - `[LinuxFxVersion <String>]`： Linux App 架構與版本
    - `[LoadBalancing <SiteLoadBalancing?>]`：網站負載平衡。
    - `[LocalMySqlEnabled <Boolean?>]`： <code>true</code> 若要啟用本機 MySQL，否則， <code>false</code> 。
    - `[LogsDirectorySizeLimit <Int32?>]`： HTTP 記錄目錄大小限制。
    - `[MachineKeyDecryption <String>]`：用於解密的演算法。
    - `[MachineKeyDecryptionKey <String>]`：解密金鑰。
    - `[MachineKeyValidation <String>]`： MachineKey 驗證。
    - `[MachineKeyValidationKey <String>]`：驗證金鑰。
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`：受管理的管線模式。
    - `[ManagedServiceIdentityId <Int32?>]`：受管理的服務身分識別識別碼
    - `[MinTlsVersion <SupportedTlsVersions?>]`： MinTlsVersion：設定 SSL 要求所需的最小 TLS 版本
    - `[NetFrameworkVersion <String>]`： .NET Framework 版本。
    - `[NodeVersion <String>]`： Node.js 版本。
    - `[NumberOfWorker <Int32?>]`：工人的人數。
    - `[PhpVersion <String>]`： PHP 版本。
    - `[PowerShellVersion <String>]`： PowerShell 版本。
    - `[PreWarmedInstanceCount <Int32?>]`： PreWarmed 實例數。         此設定僅適用于消耗量與彈性方案
    - `[PublishingUsername <String>]`：發佈使用者名稱。
    - `[PushKind <String>]`：資源類型。
    - `[PythonVersion <String>]`： Python 版本。
    - `[RemoteDebuggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用遠端偵錯，則為，否則為 <code>false</code> 。
    - `[RemoteDebuggingVersion <String>]`：遠端偵錯版本。
    - `[RequestCount <Int32?>]`： [要求計數]。
    - `[RequestTimeInterval <String>]`：時間間隔。
    - `[RequestTracingEnabled <Boolean?>]`： <code>true</code> 如果已啟用要求追蹤，則為（否則，） <code>false</code> 。
    - `[RequestTracingExpirationTime <DateTime?>]`：要求追蹤到期時間。
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`：適用于 scm 的 IP 安全性限制。
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`：適用于 scm 的 IP 安全性限制使用 main。
    - `[ScmType <ScmType?>]`： SCM 類型。
    - `[SlowRequestCount <Int32?>]`： [要求計數]。
    - `[SlowRequestTimeInterval <String>]`：時間間隔。
    - `[SlowRequestTimeTaken <String>]`：拍攝的時間。
    - `[TagWhitelistJson <String>]`：取得或設定一個 JSON 字串，其中包含由推入註冊端點所使用的白板標記清單。
    - `[TagsRequiringAuth <String>]`：取得或設定一個 JSON 字串，其中包含需要使用者驗證才能用於推入註冊端點的標記清單。         標記可以由字母數位字元及下列專案所組成：「_ '、' @ '、' # '、'. '、'： '、'-」。         驗證應該在 PushRequestHandler 進行。
    - `[TracingOption <String>]`：追蹤選項。
    - `[TriggerPrivateBytesInKb <Int32?>]`：以私人位元組為基礎的規則。
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`：以狀態碼為基礎的規則。
      - `[Count <Int32?>]`： [要求計數]。
      - `[Status <Int32?>]`： HTTP 狀態碼。
      - `[SubStatus <Int32?>]`：要求子狀態。
      - `[TimeInterval <String>]`：時間間隔。
      - `[Win32Status <Int32?>]`： Win32 錯誤碼。
    - `[Use32BitWorkerProcess <Boolean?>]`： <code>true</code> 若要使用32位的輔助進程，請按相反的方式 <code>false</code> 。
    - `[VirtualApplication <IVirtualApplication[]>]`：虛擬應用程式。
      - `[PhysicalPath <String>]`：實體路徑。
      - `[PreloadEnabled <Boolean?>]`： <code>true</code> 如果已啟用預載入，則為，否則為 <code>false</code> 。
      - `[VirtualDirectory <IVirtualDirectory[]>]`：虛擬應用程式的虛擬目錄。
        - `[PhysicalPath <String>]`：實體路徑。
        - `[VirtualPath <String>]`：虛擬應用程式的路徑。
      - `[VirtualPath <String>]`：虛擬路徑。
    - `[VnetName <String>]`：虛擬網路名稱。
    - `[WebSocketsEnabled <Boolean?>]`： <code>true</code> 如果已啟用 WebSocket，則為，否則為 <code>false</code> 。
    - `[WindowsFxVersion <String>]`： Xenon 應用程式架構與版本
    - `[XManagedServiceIdentityId <Int32?>]`：顯式管理的服務身分識別識別碼
  - `[ContainerSize <Int32?>]`：函數容器的大小。
  - `[DailyMemoryTimeQuota <Int32?>]`： (僅適用于動態 app 的 [允許的每日記憶體時間配額限制]) 。
  - `[Enabled <Boolean?>]`： <code>true</code> 如果已啟用應用程式，否則為 <code>false</code> 。 將此值設定為 false 會停用 app (將 app 離線) 。
  - `[HostNameSslState <IHostNameSslState[]>]`：主機名稱 SSL 狀態是用來管理 app 主機名稱的 SSL 系結。
    - `[HostType <HostType?>]`：表示主機名稱是標準版還是知識庫主機名稱。
    - `[Name <String>]`主機.
    - `[SslState <SslState?>]`： SSL 類型。
    - `[Thumbprint <String>]`： SSL 憑證指紋。
    - `[ToUpdate <Boolean?>]`：設定為 <code>true</code> 以更新現有的主機名稱。
    - `[VirtualIP <String>]`：如果啟用 IP SSL，則會指派給主機名稱的虛擬 IP 位址。
  - `[HostNamesDisabled <Boolean?>]`： <code>true</code> 若要停用應用程式的公用主機名稱，否則， <code>false</code> 。          如果 <code>true</code> 是，只能透過 API 管理程式存取 app。
  - `[HostingEnvironmentProfileId <String>]`：應用程式服務環境的資源識別碼。
  - `[HttpsOnly <Boolean?>]`： HttpsOnly：將網站配置為只接受 HTTPs 要求。 Http 要求的重新導向問題
  - `[HyperV <Boolean?>]`： Hyper-v 沙箱。
  - `[IdentityType <ManagedServiceIdentityType?>]`：受管理的服務身分識別類型。
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`：指派與資源相關聯之身分識別的使用者清單。 使用者身分識別字典金鑰參照會是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`：這表示您可以將任何屬性新增至此物件。
  - `[IsXenon <Boolean?>]`：已過時： Hyper-v 沙箱。
  - `[RedundancyMode <RedundancyMode?>]`：網站冗余模式
  - `[Reserved <Boolean?>]`： <code>true</code> 如果保留，則為，否則， <code>false</code> 。
  - `[ScmSiteAlsoStopped <Boolean?>]`： <code>true</code> 若要在應用程式停止時停止 SCM (KUDU) 網站，請按相反步驟操作 <code>false</code> 。 預設值為 <code>false</code> 。
  - `[ServerFarmId <String>]`：相關應用程式服務方案的資源識別碼，格式為： "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}"。

## 相關連結

