---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: fbdefd7e80e0054bbef8e12614316f7b23ff134a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917770"
---
# Update-AzVmss

## 簡介
更新 VMSS 的狀態。

## 語法

### DefaultParameter (預設) 
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
**Update-Az Vms Cmdlet** 會更新虛擬機器縮放集 (VMSS) 本機 VMSS 物件的狀態。

## 例子

### 範例 1：將 VMSS 的狀態更新為本地 VMSS 物件的狀態。
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

此命令會更新名為 VMSS001 的 VMSS 狀態，該狀態屬於名為 Group001 的資源群組，並更新為本地 VMSS 物件的狀態 ，$LocalVMSS。

## 參數

### -AsJob
在背景中執行 Cmdlet 並返回工作以追蹤進度。

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

### -AutomaticOSUpgrade
設定作業系統升級是否應該在較新版本的影像推出時自動套用至縮放集實例。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutomaticRepairGracePeriod
由於 VM 上的狀態變更，自動修復暫停的時間量。 狀態變更完成之後，寬限期即開始。 這有助於避免意外或意外維修。 時間長度應該以 ISO 8601 格式指定。 PT30M (允許的寬限期) 30 分鐘，這也是預設值。 PT90M 中允許的最大寬限期為 90 (分鐘) 。

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

### -BootDiagnosticsEnabled
是否應該在虛擬機器縮放比例集上啟用開機診斷。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootDiagnosticsStorageUri
儲存空間帳戶的 URI，用於放置主機輸出和螢幕擷取畫面。

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

### -CustomData
指定自訂資料的底數為 64 的編碼字串。
這會解碼為二進位陣列，該陣列會儲存為虛擬機器上的檔案。
二進位陣列的長度上限為 65535 位元組。 <br>
若要針對您的 VM 使用雲端 init，請參閱在建立期間使用[雲端 init 自訂 Linux VM。](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

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

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAutoRollback
停用自動作業系統升級策略的自動重回

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
表示此 Cmdlet 會停用 Linux OS 的密碼驗證。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticRepair
啟用或停用虛擬機器縮放比例集上的自動修復。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticUpdate
指出 VMSS 中的 Windows 虛擬機器是否已啟用自動更新。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionAtHost
使用者可以在要求中使用此參數，以啟用或停用虛擬機器縮放集的主機加密。 

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityId
指定與虛擬機器縮放比例集相關聯的使用者身分設定清單。
使用者身分識別參照為表單中的 ARM 資源識別碼：'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identityies/{identityName}'

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
指定用於虛擬機器縮放集的身分識別類型。
"SystemAssignedUserAssigned" 類型包括隱含建立身分識別，以及一組使用者指派的身分識別。
類型為 "None" 會從虛擬機器縮放集移除任何身分。
此參數可接受的值為：
- SystemAssigned
- UserAssigned
- SystemAssignedUserAssigned
- 沒有

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferenceId
指定影像參照識別碼。

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

### -ImageReferenceOffer
指定 VMImage 提供的虛擬機器 (類型) 類型。
若要取得影像優惠，請使用 Get-AzVMImageOffer Cmdlet。

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

### -ImageReferencePublisher
指定 VMImage 的發行者名稱。
若要取得發行者，請使用 Get-AzVMImagePublisher Cmdlet。

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

### -ImageReferenceSKU
指定 VMImage SKU。
若要取得 SKUS，請使用 Get-AzVMImageSku Cmdlet。

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

### -ImageReferenceVersion
指定 VMImage 的版本。
若要使用最新版本，請指定最新版本的值，而非特定版本。

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

### -ImageUri
指定使用者圖像的 Blob URI。
VMSS 會在同一個使用者映射容器內建立作業系統磁片。

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

### -LicenseType
指定授權類型，用於顯示您自己的授權案例。

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

### -Managed在 Managed的StorageAccountType
指定受管理磁片的儲存帳戶類型。
此參數可接受的值為：
- StandardLRS
- PremiumLRS

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

### -MaxBatchInstancePercent
在一個批次中以輪流升級同時升級的虛擬機器實例總數百分比上限。
由於這是上限，先前或未來批次中的不健康實例可能會導致批次中實例的百分比降低，以確保較高的可靠性。
如果未指定值，則值會設為 20。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
指定您願意為低優先順序 VM/VMSS 支付的最高價格。 此價格為美元。 此價格會與 VM 大小目前低優先順序價格進行比較。 此外，在建立/更新低優先順序 VM/VMSS 時，會比較價格，且只有在 maxPrice 大於目前低優先順序價格時，作業才能成功。 如果建立 VM/VMSS 之後，目前的低優先順序價格超出 maxPrice，maxPrice 也會用於評估低優先順序的 VM/VMSS。 可能的值為：任何大於零的十進位值。 範例：0.01538。  -1 表示基於價格考慮，不應將低優先順序的 VM/VMSS 從上而退出。 此外，如果您未提供，預設最高價格為 -1。

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxUnhealthyInstancePercent
縮放集內同時不健康之虛擬機器實例總數的最大百分比，可能是升級的結果，或是由虛擬機器健康情況檢查在輪流升級中止之前發現處於不健康狀態。
在開始任何批次之前，將會檢查此限制。
如果未指定值，則值會設為 20。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxUnhealthyUpgradedInstancePercent
可發現處於不健康狀態之升級虛擬機器實例的最大百分比。
此檢查將在每個批次升級之後執行。
如果超過此百分比，滾動更新會中止。
如果未指定值，則值會設為 20。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Os在Caching
指定作業系統磁片的緩存模式。 此參數可接受的值為：
- 沒有
- ReadOnly
- 朗讀預設值為 ReadWrite。
如果您變更緩存值，Cmdlet 會重新開機虛擬機器。
此設定會影響磁片的一致性與績效。

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OsRiteWriteAccelerator
指定作業系統磁片上是否應該啟用或停用 WriteAccelerator。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -過度配置
指出 Cmdlet 是否過度配置 VMSS。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PauseTimeBetweenBatches
在一個批次中完成所有虛擬機器的更新，到下一個批次開始之間的等待時間。
時間長度應該以 ISO 8601 格式指定。
預設值為 0 秒 (PT0S) 。

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

### -PlanName
指定計劃名稱。

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

### -PlanProduct
指定計劃產品。

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

### -PlanPromotionCode
指定方案促銷代碼。

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

### -PlanPublisher
指定計劃發行者。

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

### -ProvisionMSEVAgent
指出是否應該在 VMSS 的 Windows 虛擬機器上部署虛擬機器代理程式。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
要用於此縮放集的鄰近位置群組資源識別碼。

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
指定 VMSS 所屬的資源組名。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleInPolicy
縮放虛擬機器縮放比例集時要遵循的規則。  可能的值為：「Default」、'Oldest%。以及'Newest%。。」  當虛擬機器縮放集已調整為比例時，如果這是一個分區比例集，則縮放集會先跨區域進行平衡的預設值。  然後，它會盡可能跨錯誤網域進行平衡。  在每個錯誤網域中，選擇移除的虛擬機器都是不受縮放保護的虛擬機器。  當虛擬機器縮放集進行縮放時，會選擇最舊、不受縮放保護的虛擬機器進行移除。  對於分區虛擬機器縮放集，縮放集會先跨區域平衡。  在每個區域中，會選擇最舊的未受到保護的虛擬機器進行移除。  當虛擬機器縮放集進行縮放時，將會選擇不受縮放保護的最新的虛擬機器，以移除最新的虛擬機器。  對於分區虛擬機器縮放集，縮放集會先跨區域平衡。  在每個區域中，系統將會選擇最新的未受到保護的虛擬機器進行移除。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
指定單一位置群組。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVMS
指定擴充功能不會在額外過度配置之虛擬機器上執行。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sku以
指定 VMSS 中的實例數目。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKUName
指定 VMSS 所有實例的大小。

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

### -SkuTier
指定 VMSS 的層級。
此參數可接受的值為：
- 標準
- 基本

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

### -標記
以雜湊表格形式建立索引鍵值組。 例如：@{key0="value0";key1=$null;key2="value2"}

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

### -TerminateScheduledEventNotBeforeTimeoutInMinutes
刪除的虛擬機器 (分鐘數) 在事件自動核准之前 (終止已排程事件) 。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -終止ScheduledEvents
指定是否要啟用或停用終止已排程事件。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -時區
指定 Windows OS 的時區。 例如， \" 太平洋標準時間 \" 。 <br>
可以從[TimeZoneInfo.GetSystemTimeZones TimeZoneInfo.Id時區取得可能的值](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)。 [](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id)

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

### -UltraSSDEnabled
可啟用或停用一或多個受管理資料存放區的功能之標UltraSSD_LRS虛擬機器縮放比例集上的儲存空間帳戶類型。
只有啟用此屬性時，UltraSSD_LRS儲存帳戶類型的受管理磁片才能新增到 VMSS。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UpgradePolicyMode
指定縮放集的虛擬機器升級模式。
此參數可接受的值為：
- 自動
- 手動
- 滾動

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VhdContainer
指定用來儲存 VMSS 作業系統磁片的容器 URL。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
指定一個本地 VMSS 物件。
若要取得 VMSS 物件，請使用 Get-AzVmss Cmdlet。
此虛擬機器物件包含 VMSS 的更新狀態。

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMScaleSetName
指定此 Cmdlet 所建立之 VMSS 的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet

### System.Boolean

## 輸出

### Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet

## 筆記

## 相關連結

[Get-AzEvss](./Get-AzVmss.md)

[New-AzEvss](./New-AzVmss.md)

[Remove-AzEvss](./Remove-AzVmss.md)

[Restart-AzEvss](./Restart-AzVmss.md)

[Set-AzEvss](./Set-AzVmss.md)

[Start-AzEvss](./Start-AzVmss.md)

[Stop-AzEvss](./Stop-AzVmss.md)


