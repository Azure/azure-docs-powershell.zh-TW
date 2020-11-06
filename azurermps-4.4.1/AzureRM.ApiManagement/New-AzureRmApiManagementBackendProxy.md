---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d3699347d21f17452d521afb3bc5524f8e68e40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450110"
---
# New-AzureRmApiManagementBackendProxy

## 摘要
建立新的後端 Proxy 物件。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmApiManagementBackendProxy -Url <String> [-UserName <String>] [-Password <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
建立新的後端 Proxy 物件，可在建立新的後端實體時進行管道。

## 示例

### 建立後端 Proxy In-Memory 物件
```
$proxy= New-AzureRmApiManagementBackendProxy -Url "https://abbc.def.g" -UserName "apim" -Password "password"
```

建立後端 Proxy 物件

## 參數

### -Password
用來連接後端 Proxy 的 Proxy 密碼。
這個參數是選用的。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Url
將來電轉接到後端時要使用之 Proxy 伺服器的 Url。
這個參數是必要的。

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

### -UserName
用來連接後端 Proxy 的 Proxy 使用者名稱。
這個參數是選用的。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### ServiceManagement. PsApiManagementBackendProxy （ApiManagement）

## 筆記

## 相關連結

[AzureRmApiManagementBackend](./Get-AzureRmApiManagementBackend)

[新-AzureRmApiManagementBackend](./New-AzureRmApiManagementBackend.md)

[新-AzureRmApiManagementBackendCredential](./New-AzureRmApiManagementBackendCredential.md)

[Set-AzureRmApiManagementBackend](./Set-AzureRmApiManagementBackend.md)

[移除-AzureRmApiManagementBackend](./Remove-AzureRmApiManagementBackend.md)
