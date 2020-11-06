---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 60bcdad644f07f627373c90791c8cd115d590bcd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621012"
---
# Update-AzRecoveryServicesAsrServicesProvider

## 摘要
更新) 從 Azure Site Recovery 服務提供者收到的資訊， (重新整理伺服器。

## 句法

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzRecoveryServicesAsrServicesProvider** Cmdlet 會更新從 Azure Site Recovery 服務提供者收到的資訊。 您可以使用這個 Cmdlet 觸發從復原服務提供者收到的資訊重新整理。

## 示例

### 範例1
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

開始從指定的 ASR 服務提供者中重新整理資訊的作業，並傳回用來追蹤作業的 ASR 作業。

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

### -InputObject
指定 ASR 服務提供者物件，該物件會識別要更新之資訊的伺服器 (進行刷新。 ) 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

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

### RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider

## 輸出

### RecoveryServices. SiteRecovery. ASRJob

## 筆記

## 相關連結

[AzRecoveryServicesAsrServicesProvider](./Get-AzRecoveryServicesAsrServicesProvider.md)

[移除-AzRecoveryServicesAsrServicesProvider](./Remove-AzRecoveryServicesAsrServicesProvider.md)
