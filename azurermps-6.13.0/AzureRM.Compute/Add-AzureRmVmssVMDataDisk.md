---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssVMDataDisk.md
ms.openlocfilehash: c4a4aa530f29de93458f618dbf45f639fe873f1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450249"
---
# Add-AzureRmVmssVMDataDisk

## 摘要
在 Vmss VM 中新增資料磁片。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Add-AzureRmVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**載入 AzureRmVmssVMDataDisk** Cmdlet 會將資料磁片新增到 Vmss VM。

## 示例

### 範例1：將受管理的資料磁片新增至 Vmss VM。
```powershell
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

第一個命令會取得現有的受管理磁片。
Next 命令會取得資源群組名稱所提供的現有 Vmss VM、Vmss 名稱和實例識別碼。
下一個命令會將受管理的磁片新增至儲存在本機 $VmssVM 的 Vmss VM 中。
Final 命令會使用已新增的資料磁片來更新 Vmss VM。

## 參數

### -快取
指定磁片的快取模式。
此參數可接受的值為：
- 唯讀
- 讀
- None 預設值為 ReadWrite。
變更此值會導致虛擬機器重新開機。
此設定會影響磁片的一致性和效能。

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CreateOption
指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。
此參數可接受的值為：
- 選用.
指定此選項以從專用磁片建立虛擬機器。
當您指定此選項時，請勿指定 *SourceImageUri* 參數。
您需要 *VhdUri* ，才能告知 Azure 平臺將虛擬硬碟的位置 (VHD) 附加成資料磁片至虛擬機器。
- 有空.
指定此程式以建立空白的資料磁片。
- FromImage.
指定此選項以從通用影像或磁片建立虛擬機器。
當您指定此選項時，您必須指定 *SourceImageUri* 參數，以告知 Azure 平臺要作為資料磁片附加的 VHD 位置。
*VhdUri* 參數是用來識別虛擬機器所使用的資料磁片 VHD 儲存位置。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSizeInGB
指定要附加至虛擬機器的空白磁片大小（以 gb 為位元組）。

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

### -Lun
指定資料磁片的邏輯單元號碼 (LUN) 。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
指定受管理磁片的 ID。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
指定受管理磁片的儲存帳戶類型。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSetVM
指定要新增資料磁片的本機虛擬機器縮放設定 VM 物件。
您可以使用 **AzureRmVmssVM** Cmdlet 來取得虛擬機器縮放設定 VM 物件。

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
指定是否應該在受管理的資料磁片上啟用或停用 WriteAccelerator。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSVirtualMachineScaleSetVM 中的 [計算] 命令。

### System.object

### System.object

### CachingTypes 中的 [Azure. 管理]

## 輸出

### PSVirtualMachineScaleSetVM 中的 [計算] 命令。

## 筆記

## 相關連結
