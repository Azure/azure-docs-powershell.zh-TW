---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: e0f9ad794f1631c5c8615480c6074f040f7fe749
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127919"
---
# Update-AzCloudService

## 摘要
建立或更新雲端服務。
請注意，有些屬性只能在建立雲端服務期間設定。

## 句法

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 說明
建立或更新雲端服務。
請注意，有些屬性只能在建立雲端服務期間設定。

## 示例

### 範例1：將 RDP 延伸新增至現有的雲端服務
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

上方的命令集會將 RDP 延伸新增至現有的名為 ContosoCS 的雲端服務，該名稱屬於名為 ContosOrg 的資源群組。

### 範例2：從雲端服務移除所有延伸
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

上方的一組命令會從屬於名為 ContosOrg 之資源群組的現有雲端服務中移除所有延伸。

### 範例3：從雲端服務移除 RDP 延伸
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

上方的一組命令會從屬於名為 ContosOrg 之資源群組的現有雲端服務，移除 RDP 延伸。

### 範例4： Scale-Out/Scale-In 角色實例
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

上方的命令集說明如何將屬於名為 ContosOrg 之資源群組之名為 ContosoCS 的雲端服務的「橫向」和「擴展」角色實例計數。

## 參數

### -AsJob
執行命令做為工作

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
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。

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
以非同步方式執行命令

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

### -參數
描述雲端服務。
若要建立，請參閱參數屬性的 [記事] 區段，然後建立雜湊資料表。

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

### ICloudService （CloudService）。 Api20201001Preview。

### ICloudServiceIdentity （CloudService）的

## 輸出

### ICloudService （CloudService）。 Api20201001Preview。

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


INPUTOBJECT <ICloudServiceIdentity> ：身分識別參數
  - `[CloudServiceName <String>]`: 
  - `[Id <String>]`：資源身分識別路徑
  - `[ResourceGroupName <String>]`: 
  - `[RoleInstanceName <String>]`：角色實例的名稱。
  - `[RoleName <String>]`：角色的名稱。
  - `[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。 [訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。
  - `[UpdateDomain <Int32?>]`：指定識別更新網域的整數值。 更新網域是以零為基礎的索引來標識：第一個更新網域的識別碼為0，第二個是 ID 為1，依此類推。

參數 <ICloudService> ：說明雲端服務。
  - `Location <String>`：資源位置。
  - `[Configuration <String>]`：指定雲端服務的 XML 服務配置 ( .cscfg) 。
  - `[ConfigurationUrl <String>]`：指定在 Blob 服務中參照服務配置位置的 URL。 您可以從任何儲存空間帳戶 (SAS) URI，以共用存取簽章的服務套件 URL。         這是只寫屬性，不會在 [取得呼叫] 中傳回。
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`：說明雲端服務延伸設定檔。
    - `[Extension <IExtension[]>]`：雲端服務的延伸清單。
      - `[AutoUpgradeMinorVersion <Boolean?>]`：明確指定平臺在可用時是否可自動將 typeHandlerVersion 升級至較高的次要版本。
      - `[ForceUpdateTag <String>]`：標記以強制套用提供的公用和受保護設定。         變更 tag 值可讓您重新執行延伸，而不需變更任何公用或受保護的設定。         如果 forceUpdateTag 未變更，則處理常式仍會套用對公眾或受保護設定的更新。         如果沒有 forceUpdateTag，也不會變更任何公開或受保護的設定，延伸將會以相同的序號碼流向角色實例，而不論是否重新執行，都可以使用處理程式的實現
      - `[Name <String>]`：延伸的名稱。
      - `[ProtectedSetting <String>]`：已在傳送至角色實例之前加密之副檔名的受保護設定。
      - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
      - `[Publisher <String>]`：延伸處理常式發行者的名稱。
      - `[RolesAppliedTo <String[]>]`：選用的角色清單來套用此延伸。 如果未指定屬性或指定了 ' *」，則會將延伸套用到雲端服務中的所有角色。
      - `[Setting <String>]`：延伸的公開設定。 對於 JSON 延伸，這是延伸的 JSON 設定。 針對 XML 延伸 (例如 RDP) ，這是延伸的 XML 設定。
      - `[SourceVaultId <String>]`：資源識別碼
      - `[Type <String>]`：指定延伸的類型。
      - `[TypeHandlerVersion <String>]`：指定延伸的版本。 指定副檔名的版本。 如果未指定此元素，或使用星號 ( * ) 作為值，就會使用最新的延伸版本。 如果將該值指定為主要版本號碼，並以星號做為次要版本號碼 (X. ) ，則會選取指定主要版本的最新次要版本。 如果 (X-y) 指定主要版本號碼和次要版本號碼，則會選取特定副檔名版本。 如果指定版本，則會在角色實例上執行自動升級。
  - `[NetworkProfile <ICloudServiceNetworkProfile>]`：雲端服務的網路設定檔。
    - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`：雲端服務的負載平衡器設定清單。
      - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`： IP 清單
        - `[Name <String>]`: 
        - `[PrivateIPAddress <String>]`：雲端服務所參照的私人 IP 位址。
        - `[PublicIPAddressId <String>]`：資源識別碼
        - `[SubnetId <String>]`：資源識別碼
      - `[Name <String>]`：資源名稱
    - `[SwappableCloudService <ISubResource>]`: 
      - `[Id <String>]`：資源識別碼
  - `[OSProfile <ICloudServiceOSProfile>]`：說明雲端服務的 OS 設定檔。
    - `[Secret <ICloudServiceVaultSecretGroup[]>]`：指定應該安裝在角色實例上的憑證集合。
      - `[SourceVaultId <String>]`：資源識別碼
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`： SourceVault 中包含憑證的主要保存庫參照清單。
        - `[CertificateUrl <String>]`：這是已上傳到金鑰保存庫的憑證 URL （密碼）。
  - `[PackageUrl <String>]`：指定要參照 Blob 服務中服務套件位置的 URL。 您可以從任何儲存空間帳戶 (SAS) URI，以共用存取簽章的服務套件 URL。         這是只寫屬性，不會在 [取得呼叫] 中傳回。
  - `[RoleProfile <ICloudServiceRoleProfile>]`：說明雲端服務的角色設定檔。
    - `[Role <ICloudServiceRoleProfileProperties[]>]`：雲端服務的角色清單。
      - `[Name <String>]`：資源名稱。
      - `[SkuCapacity <Int64?>]`：指定雲端服務中的角色實例數。
      - `[SkuName <String>]`： Sku 名稱。 注意：如果雲端服務目前所在的硬體不支援新版 SKU，您必須刪除並重新建立雲端服務，或移回舊版 SKU。
      - `[SkuTier <String>]`：指定雲端服務的層級。 可能的值為 <br /><br /> **標準** <br /><br /> **空白**
  - `[StartCloudService <Boolean?>]`： (選用) 指出是否要在建立雲端服務後立即啟動。 預設值為 `true` 。         如果是 false，則表示服務模型仍在部署，但程式碼不會立即執行。 相反地，服務會在您呼叫 Start 之前 PoweredOff，直到該服務開始時才會啟動。 即使是 poweredoff，部署的服務仍會產生費用。
  - `[Tag <ICloudServiceTags>]`：資源標記。
    - `[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`：雲端服務的更新模式。 部署服務時，系統會將角色實例指派給更新網域。 更新可以在每個更新網域中手動啟動，或是在所有更新網域中自動啟動。         可能的值為 <br /><br />**自動**<br /><br />**手動** <br /><br />**辦公**<br /><br />         如果沒有指定，則預設值為 Auto。如果設定為 [手動]，則必須呼叫 UpdateDomain，才能套用更新。 如果設為 Auto，更新會自動套用至每個更新網域。

## 相關連結

