---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 3c37376aa475e8b0797d4ff4433ab54a11d2b6bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450943"
---
# Get-AzureRmApiManagementAuthorizationServer

## 摘要
取得 API 管理授權伺服器。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 取得所有授權伺服器 (預設) 
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 依識別碼取得
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmApiManagementAuthorizationServer** Cmdlet 會取得所有 Azure API 管理授權伺服器或指定的授權伺服器。

## 示例

### 範例1：取得所有授權伺服器
```
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

這個命令會取得所有 API 管理授權伺服器。

### 範例2：取得指定的授權伺服器
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

這個命令會取得指定的授權伺服器。

## 參數

### -內容
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerId
```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## 輸出

### IList<ApiManagement. ServiceManagement. PsApiManagementOAuth2AuthrozationServer]>

## 筆記

## 相關連結

[新-AzureRmApiManagementAuthorizationServer](./New-AzureRmApiManagementAuthorizationServer.md)

[移除-AzureRmApiManagementAuthorizationServer](./Remove-AzureRmApiManagementAuthorizationServer.md)

[Set-AzureRmApiManagementAuthorizationServer](./Set-AzureRmApiManagementAuthorizationServer.md)


