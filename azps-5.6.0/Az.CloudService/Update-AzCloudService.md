---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: bb67420e3fbb4479a79c7a837aad3b9a65635d88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916249"
---
# Update-AzCloudService

## 簡介
建立或更新雲端服務。
請注意，某些屬性只能在建立雲端服務期間設定。

## 語法

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 描述
建立或更新雲端服務。
請注意，某些屬性只能在建立雲端服務期間設定。

## 例子

### 範例 1：新增 RDP 擴充功能至現有的雲端服務
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

上述一組命令會將 RDP 擴充功能新增到現有的名為 ContosoCS 的雲端服務，該服務屬於名為 ContosOrg 的資源群組。

### 範例 2：從雲端服務移除所有延伸模組
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

上述一組命令會從名為 ContosoCS 的現有雲端服務移除所有屬於 ContosOrg 資源群組的擴充功能。

### 範例 3：從雲端服務移除 RDP 擴充功能
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

上述一組命令會從名為 ContosoCS 的現有雲端服務移除 RDP 副檔名，該服務屬於名為 ContosOrg 的資源群組。

### 範例 4：Scale-Out / Scale-In角色實例
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

上述命令集顯示如何針對屬於 ContosOrg 資源群組的名為 ContosoCS 的雲端服務，進行縮小和縮放角色實例計數。

## 參數

### -AsJob
以工作執行命令

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
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -InputObject
身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoWait
非同步執行命令

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

### -Parameter
說明雲端服務。
若要建構，請參閱 PARAMETER 屬性的 NOTES 區段，並建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.ICloudService

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.iCloudServiceIdentity

## 輸出

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.ICloudService

## 筆記

別名

複雜的參數屬性

若要建立下列描述的參數，請建構包含適當屬性的雜湊表。 有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。


INPUTOBJECT： <ICloudServiceIdentity> 身分識別參數
  - `[CloudServiceName <String>]`: 
  - `[Id <String>]`：資源識別路徑
  - `[ResourceGroupName <String>]`: 
  - `[RoleInstanceName <String>]`：角色實例的名稱。
  - `[RoleName <String>]`：角色名稱。
  - `[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。 訂閱識別碼會構成每個服務通話 URI 的一部分。
  - `[UpdateDomain <Int32?>]`：指定可識別更新網域的整數值。 更新網域會以零型索引識別：第一個更新網域的識別碼為 0，第二個更新網域的識別碼為 1，以此類比。

<ICloudService>PARAMETER：說明雲端服務。
  - `Location <String>`：資源位置。
  - `[Configuration <String>]`：指定雲端 (.csc) XML 服務組配置。
  - `[ConfigurationUrl <String>]`：指定一個 URL，該 URL 參照到 Blob 服務中的服務群組原則位置。 服務套件 URL 可以是來自任何儲存帳戶 (SAS) URI 的共用存取簽名。         這是只寫入的屬性，不會在 GET 通話中返回。
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`：說明雲端服務擴充功能設定檔。
    - `[Extension <IExtension[]>]`：雲端服務的擴充功能清單。
      - `[AutoUpgradeMinorVersion <Boolean?>]`：明確指定平臺是否可以在提供類型HandlerVersion時自動升級至較高的次要版本。
      - `[ForceUpdateTag <String>]`：標記以強制使用提供的公用和受保護的設定。         變更標記值可讓您重新經營擴充功能，而不需要變更任何公用或受保護的設定。         如果未變更 forceUpdateTag，處理常式仍然會使用公用或受保護的設定更新。         如果 forceUpdateTag 或任何公用或受保護的設定都沒有變更，延伸模組會流向具有相同序號的角色實例，而是否要重新執行，則由處理常式的執行方式決定
      - `[Name <String>]`：副檔名的名稱。
      - `[ProtectedSetting <String>]`：已加密的擴充功能之受保護的設定，在送往角色實例之前。
      - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
      - `[Publisher <String>]`：副檔名處理常式發行者的名稱。
      - `[RolesAppliedTo <String[]>]`：可申請此擴充功能的角色清單。 如果未指定屬性或指定 '*'，延伸模組會適用于雲端服務中的所有角色。
      - `[Setting <String>]`：擴充功能公用設定。 對於 JSON 擴充功能，這是該擴充功能 JSON 設定。 對於 XML 擴充 (如 RDP) ，這是該副檔名的 XML 設定。
      - `[SourceVaultId <String>]`：資源識別碼
      - `[Type <String>]`：指定擴充功能的類型。
      - `[TypeHandlerVersion <String>]`：指定擴充功能的版本。 指定擴充功能的版本。 如果未指定此元素，或是使用星號 (*) 做為值，則使用最新版本的擴充功能。 如果以主要版本號碼和星號指定值做為次要版本號碼 (X.) ，會選取指定主要版本的最新次要版本。 如果在 X.Y (指定主要版本號碼和次要版本號碼) ，會選取特定的擴充版本。 如果指定版本，系統即會對角色實例執行自動升級。
  - `[NetworkProfile <ICloudServiceNetworkProfile>]`：雲端服務的網路設定檔。
    - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`：雲端服務的負載平衡器組組清單。
      - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`：IP 清單
        - `[Name <String>]`: 
        - `[PrivateIPAddress <String>]`：雲端服務所參照的私人 IP 位址。
        - `[PublicIPAddressId <String>]`：資源識別碼
        - `[SubnetId <String>]`：資源識別碼
      - `[Name <String>]`：資源名稱
    - `[SwappableCloudService <ISubResource>]`: 
      - `[Id <String>]`：資源識別碼
  - `[OSProfile <ICloudServiceOSProfile>]`：說明雲端服務的 OS 設定檔。
    - `[Secret <ICloudServiceVaultSecretGroup[]>]`：指定應該要安裝在角色實例上的一組憑證。
      - `[SourceVaultId <String>]`：資源識別碼
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`：SourceVault 中包含憑證的重要庫參照清單。
        - `[CertificateUrl <String>]`：這是憑證的 URL，已上傳至金鑰庫作為機密。
  - `[PackageUrl <String>]`：指定參照 Blob 服務中服務套件位置的 URL。 服務套件 URL 可以是來自任何儲存帳戶 (SAS) URI 的共用存取簽名。         這是只寫入的屬性，不會在 GET 通話中返回。
  - `[RoleProfile <ICloudServiceRoleProfile>]`：說明雲端服務的角色設定檔。
    - `[Role <ICloudServiceRoleProfileProperties[]>]`：雲端服務的角色清單。
      - `[Name <String>]`：資源名稱。
      - `[SkuCapacity <Int64?>]`：指定雲端服務中的角色實例數目。
      - `[SkuName <String>]`：SKU 名稱。 注意：如果雲端服務目前使用的硬體不支援新的 SKU，您必須刪除並重建雲端服務，或移回舊的 SKU。
      - `[SkuTier <String>]`：指定雲端服務層級。 可能的值為 <br /><br /> **標準** <br /><br /> **基本**
  - `[StartCloudService <Boolean?>]`： (選擇性) 指出是否要在建立雲端服務後立即啟動。 預設值為 `true` 。         如果為 False，服務模型仍然會部署，但程式碼不會立即執行。 服務會改為 PoweredOff，直到您打電話給 Start，此時服務就會啟動。 即使已部署的服務為關閉電源，仍會產生費用。
  - `[Tag <ICloudServiceTags>]`：資源標記。
    - `[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`：雲端服務的更新模式。 角色實例會配置在部署服務時更新網域。 更新可以在每個更新網域中手動啟動，或在所有更新網域中自動啟動。         可能的值為 <br /><br />**自動**<br /><br />**手動** <br /><br />**同時**<br /><br />         如果未指定，預設值為自動。如果設定為手動，則必須要求 PUT UpdateDomain 以套用更新。 如果設定為自動，系統會自動將更新順序套用至每個更新網域。

## 相關連結

