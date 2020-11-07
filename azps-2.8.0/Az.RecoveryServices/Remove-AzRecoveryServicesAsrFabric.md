---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 9a67729b384703ccc102b14d521d4422825bdb6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792360"
---
# Remove-AzRecoveryServicesAsrFabric

## 摘要
從 [恢復服務] 保存庫刪除指定的 Azure 網站復原結構。

## 句法

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzRecoveryServicesAsrFabric** Cmdlet 會從 [恢復服務] 保存庫中移除指定的 Azure 網站復原結構。

## 示例

### 範例1
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

開始刪除指定的結構，並傳回用於追蹤操作的 ASR 作業。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。


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

### -Force
強制執行命令，但不提供額外的警告。

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

### -InputObject
Cmdlet 的輸入物件：對應到要刪除之結構的 ASR fabric 物件。

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -確認
指定是否需要確認。 將確認參數的值設定為 [$false]，以略過確認。

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
顯示在未實際執行 Cmdlet 的情況下執行 Cmdlet 時會發生什麼情況。

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

### RecoveryServices. SiteRecovery. ASRFabric

## 輸出

### RecoveryServices. SiteRecovery. ASRJob

## 筆記

## 相關連結

[AzRecoveryServicesAsrFabric](./Get-AzRecoveryServicesAsrFabric.md)

[新-AzRecoveryServicesAsrFabric](./New-AzRecoveryServicesAsrFabric.md)
