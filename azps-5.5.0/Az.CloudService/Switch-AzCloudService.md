---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: f10d11dbbe98c098286a072d5882bf5d3a464d8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136571"
---
# Switch-AzCloudService

## 摘要
在兩個雲端服務 (延伸支援) 負載平衡器之間交換 Vip。

## 句法

### CloudServiceName (預設) 
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CloudService
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 說明
在兩個雲端服務 (延伸支援) 負載平衡器之間交換 Vip。

## 示例

### 範例1：使用名稱切換雲端服務
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

上述命令會在名為「BService」的雲端服務上執行 vipswap 作業，並會在使用者在確認提示字元上確認該動作之後，才會執行該作業。
[BService]，並以其可交換的雲端服務進行交換。

### 範例2：使用雲端服務物件切換雲端服務
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

上述命令會在名為「BService」的雲端服務上執行 vipswap 作業，並會在使用者在確認提示字元上確認該動作之後，才會執行該作業。
[BService]，並以其可交換的雲端服務進行交換。

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

### -Async


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

### -CloudService
若要建立，請參閱 CLOUDSERVICE 屬性和建立雜湊資料表的備忘稿區段。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudServiceName


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
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

### -ResourceGroupName


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
可唯一識別 Microsoft Azure 訂閱的訂閱認證。
[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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

## 輸出

### System.object

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


CLOUDSERVICE <CloudService> ： 
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

