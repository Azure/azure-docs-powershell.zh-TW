---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: AD76C752-2070-449D-BF4F-B4260B05AB02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 6afb5be21f1000cf2e18cd8a4b9e1dfa4f159ee0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452323"
---
# Update-AzureRmSiteRecoveryServer

## 摘要
刷新網站恢復伺服器。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Update-AzureRmSiteRecoveryServer -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmSiteRecoveryServer** Cmdlet 會重新整理 Azure Site Recovery 伺服器。

## 示例

## 參數

### -伺服器
指定此 Cmdlet 更新的網站恢復伺服器。

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
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

### ASRServer
形參 "Server" 接受管線中 "ASRServer" 類型的值

## 輸出

## 筆記

## 相關連結

[AzureRmSiteRecoveryServer](./Get-AzureRmSiteRecoveryServer.md)

[移除-AzureRmSiteRecoveryServer](./Remove-AzureRmSiteRecoveryServer.md)
