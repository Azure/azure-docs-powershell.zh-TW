---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3ba7ab00076a3a0634a0d4394270fe4a83ec8ede
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398252"
---
# New-AzVMSqlServerAutoPatchingConfig

## 簡介
建立虛擬機器上自動修補的組塊物件。

## 語法

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
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
Type: String
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
Type: SwitchParameter
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
Type: Int32
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
Type: Int32
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
Type: String
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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### 沒有
此 Cmdlet 不接受任何輸入。

## 輸出

### 自動修補設定
此 Cmdlet 會返回包含自動修補設定的物件。

## 筆記

## 相關連結

[New-AzureMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Set-AzMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


