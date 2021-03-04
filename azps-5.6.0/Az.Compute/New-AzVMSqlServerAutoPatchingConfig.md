---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3433d6bf5d3886978b75024e34c873e38230212b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914889"
---
# New-AzVMSqlServerAutoPatchingConfig

## 簡介
建立虛擬機器上自動修補的組塊物件。

## 語法

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## 描述
**New-AzMSqlServerAutoPatchingConfig** Cmdlet 會建立一個組塊物件，以在虛擬機器上自動修補。

## 例子

### 範例 1：建立設定物件以設定自動修補
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

此命令會建立修補的組塊物件。
命令會指定一周中的星期，並定義維護視窗。
此組塊可啟用使用這些值的修補。
該命令會將結果儲存在$AutoBackupConfig變數中。
您可以為其他 Cmdlet 指定此組Set-AzVMSqlServerExtension專案。

## 參數

### -DayOfWeek
指定一周中應該安裝更新的日子。
此參數可接受的值為：
- 星期天
- 星期一
- 星期二
- 星期三
- 星期四
- 星期五
- 星期六
- 每天

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -啟用
表示已啟用虛擬機器的自動修補功能。
如果您啟用自動修補，Cmdlet 會將 Windows Update 進入互動式模式。
如果您停用自動修補，Windows Update 設定不會變更。

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

### -MaintenanceWindowDuration
指定維護視窗的工期 ，以分鐘表示。
自動修補可避免執行可能會影響該視窗外部虛擬機器可用性的動作。
指定 30 分鐘的倍數。

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

### -MaintenanceWindowStartingHour
指定維護視窗啟動時的一天中小時。
這次會定義何時開始安裝更新。

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

### -PatchCategory
指定是否應該包含重要的更新。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### 沒有

## 輸出

### Microsoft.Azure.Commands.Compute.AutoPatchingSettings

## 筆記

## 相關連結

[New-AzMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Set-AzMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


