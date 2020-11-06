---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 5657701475e81b302d761193cd542ee38ea9c16e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449496"
---
# Remove-AzureRmSiteRecoveryRecoveryPlan

## 摘要
從網站復原中移除網站復原方案。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByObject (預設) 
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmSiteRecoveryRecoveryPlan** Cmdlet 會從目前的 Azure site recovery 中移除網站復原方案。

## 示例

### 範例1：移除恢復方案
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

第一個命令使用 Get-AzureRmSiteRecoveryRecoveryPlan Cmdlet 來取得網站復原方案，然後將它儲存在 $RecoveryPlan 變數中。

第二個命令會在 $RecoveryPlan 中移除復原方案。

## 參數

### -名稱
指定此 Cmdlet 移除的復原方案名稱。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
指定此 Cmdlet 移除的復原方案。

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### ASRRecoveryPlan
形參 "RecoveryPlan" 接受管線中 "ASRRecoveryPlan" 類型的值

## 輸出

## 筆記

## 相關連結

[AzureRmSiteRecoveryRecoveryPlan](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[新-AzureRmSiteRecoveryRecoveryPlan](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[更新-AzureRmSiteRecoveryRecoveryPlan](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


