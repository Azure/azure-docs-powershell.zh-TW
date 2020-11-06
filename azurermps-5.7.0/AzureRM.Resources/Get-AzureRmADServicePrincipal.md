---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8344d9e794189d67a69c1be9a88e135b721a0d4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447682"
---
# Get-AzureRmADServicePrincipal

## 摘要
篩選 active directory 服務主體。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### EmptyParameterSet (預設) 
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SearchStringParameterSet
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ObjectIdParameterSet
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
篩選 active directory 服務主體。

## 示例

### 使用 SPN 篩選服務主體
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

取得具有 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN 的服務主體。

### 使用搜尋字串篩選服務主體
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

篩選所有顯示名稱以 "Web" 開頭的廣告服務主體。

### 清單廣告服務原則
```
PS C:\> Get-AzureRmADServicePrincipal
```

取得所有廣告服務主體。

## 參數

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

### -ObjectId
服務主體的物件識別碼。

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SearchString
從這個值開始，提取所有顯示名稱的服務主體。

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
服務的 SPN。

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases: SPN

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

### [System.object]。清單 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal]

## 筆記

## 相關連結

[新-AzureRmADServicePrincipal](./New-AzureRmADServicePrincipal.md)

[Set-AzureRmADServicePrincipal](./Set-AzureRmADServicePrincipal.md)

[移除-AzureRmADServicePrincipal](./Remove-AzureRmADServicePrincipal.md)

[AzureRmADApplication](./Get-AzureRmADApplication.md)

[AzureRmADSpCredential](./Get-AzureRmADSpCredential.md)

