---
external help file: AzureRM.Compute.ManagedService-help.xml
Module Name: AzureRM.Compute.ManagedService
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: 0fa0f2d5cb78fe96f05b818b5cbfdabca47cbdee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445679"
---
# ConvertTo-AzureRmVhd

## 摘要
將 Hyper-v VM 轉換成 Azure 支援的虛擬硬碟檔案

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
將 Hyper-v VM 轉換成 Azure 支援的虛擬硬碟檔案

## 示例

### 範例1
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

將名為「test」的 Hyper-v VM 轉換為 Azure 支援的虛擬硬碟檔案至目前的資料夾。

## 參數

### -AsJob
在背景中執行 Cmdlet，然後返回作業來追蹤進度。

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

### -ExportPath
將包含磁片檔案的匯出資料夾路徑。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
強制匯出，即使找到現有資料夾也一樣。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -HyperVServer
Hyper-v 伺服器 DNS 名稱，並以 "localhost" 做為預設值。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### -HyperVVMName
Hyper-v 名稱名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### PathInfo 的系統管理功能

## 筆記

## 相關連結
