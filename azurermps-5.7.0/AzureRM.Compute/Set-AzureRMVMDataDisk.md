---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 2f961f144bc322cb1b1b12001ed006bc783ed67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450679"
---
# Set-AzureRmVMDataDisk

## 摘要
修改虛擬機器資料磁片的屬性。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ChangeWithName
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

### ChangeWithLun
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

## 說明
**AzureRmVMDataDisk** Cmdlet 會修改虛擬機器資料磁片的屬性。

## 示例

### 範例1：修改資料磁片的快取模式
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

第一個命令會使用 **AzureRmVM** 來取得名為 ContosoVM07 的虛擬機器。
該命令會將它儲存在 $VM 變數中。

第二個命令會修改 $VM 虛擬機器上名為 DataDisk01 之資料磁片的快取模式。
命令會將結果傳遞給 Update-AzureRmVM Cmdlet，以執行您的變更。
對緩衝模式所做的變更會導致虛擬機器重新開機。

## 參數

### -快取
指定磁片的快取模式。
此參數可接受的值為：

- 唯讀
- 讀

預設值為 ReadWrite。
變更此值會導致虛擬機器重新開機。

此設定會影響磁片的一致性和效能。

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
指定資料磁片的大小（以 gb 為數）。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
指定此 Cmdlet 所修改之資料磁片的邏輯單元號碼 (LUN) 。

```yaml
Type: Int32
Parameter Sets: ChangeWithLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 所修改之資料磁片的名稱。

```yaml
Type: String
Parameter Sets: ChangeWithName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
指定此 Cmdlet 修改資料磁片的虛擬機器。
若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

## 筆記

## 相關連結

[AzureRmVM](./Get-AzureRmVM.md)

[更新-AzureRmVM](./Update-AzureRmVM.md)


