---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: b44d3bbf7c594f5f9114488b536d28fd17fe56c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453083"
---
# Get-AzureRmADApplication

## 摘要
列出現有的 azure active directory 應用程式。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### EmptyParameterSet (預設) 
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ApplicationObjectIdParameterSet
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ApplicationDisplayNameParameterSet
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ApplicationIdentifierUriParameterSet
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
列出現有的 azure active directory 應用程式。
應用程式查閱可以由 ObjectId、ApplicationId、IdentifierUri 或 DisplayName 來完成。
如果未提供任何參數，則它會提取租使用者下的所有應用程式。

## 示例

### 範例1
```
PS E:\> Get-AzureRmADApplication
```

列出租使用者下的所有應用程式。

### 範例2
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

取得識別碼 uri 為 "" 的應用程式 http://mySecretApp1 。

## 參數

### -ApplicationId
要提取之應用程式的應用程式識別碼。

```yaml
Type: Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -DisplayNameStartWith
從顯示名稱開始提取所有應用程式。

```yaml
Type: String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentifierUri
要提取之應用程式的唯一識別碼 Uri。

```yaml
Type: String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
要提取之應用程式的物件識別碼。

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### [System.object]。清單 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication]

## 筆記

## 相關連結

[移除-AzureRmADAppCredential](./Remove-AzureRmADAppCredential.md)

[新-AzureRmADAppCredential](./New-AzureRmADAppCredential.md)

[AzureRmADAppCredential](./Get-AzureRmADAppCredential.md)

[移除-AzureRmADApplication](./Remove-AzureRmADApplication.md)

[Set-AzureRmADApplication](./Set-AzureRmADApplication.md)

[新-AzureRmADApplication](./New-AzureRmADApplication.md)

