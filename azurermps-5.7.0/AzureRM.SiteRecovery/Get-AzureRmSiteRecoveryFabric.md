---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 63d28696370f5219a4c2a21c6fb3097441a11433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450472"
---
# Get-AzureRmSiteRecoveryFabric

## 摘要
取得 Azure Site Recovery 結構的屬性。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 預設 (預設) 
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmSiteRecoveryFabric** Cmdlet 會取得指定 Azure 網站復原結構的屬性，或在恢復服務電子倉庫中的所有 azure 網站復原結構。

## 示例

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### FriendlyName
指定 Azure 網站復原結構的易記名稱。

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定 Azure 網站復原結構的名稱。

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### [System.object]。清單 ' 1 [SiteRecovery. ASRFabric，SiteRecovery，版本 = 2.0.1.0，Culture = 中性，PublicKeyToken = null]] （通用）

## 筆記

## 相關連結

[新-AzureRmSiteRecoveryFabric](./New-AzureRmSiteRecoveryFabric.md)

[移除-AzureRmSiteRecoveryFabric](./Remove-AzureRmSiteRecoveryFabric.md)
