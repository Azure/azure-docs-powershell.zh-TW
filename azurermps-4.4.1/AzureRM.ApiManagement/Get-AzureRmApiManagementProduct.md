---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: ab0aeb77bd5f28520e39548f539d07516cd17ac8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450129"
---
# Get-AzureRmApiManagementProduct

## 摘要
取得清單或特定產品。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 取得所有 producst (預設) 
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### 依識別碼取得
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 依標題取得
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmApiManagementProduct** Cmdlet 會取得清單或特定產品。

## 示例

### 範例1：取得所有產品
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext
```

這個命令會取得所有 API 管理產品。

### 範例2：依識別碼取得產品
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789"
```

這個命令會透過識別碼取得 API 管理產品。

## 參數

### -內容
指定 **PsApiManagementCoNtext** 物件的實例。

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

### -產品識別碼
指定要搜尋的產品識別碼。

```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -標題
指定要尋找之產品的標題。
如果已指定，此 Cmdlet 會嘗試透過標題取得產品。

```yaml
Type: System.String
Parameter Sets: Get by Title
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

### IList<ApiManagement. ServiceManagement. PsApiManagementProduct]>

## 筆記

## 相關連結

[新-AzureRmApiManagementProduct](./New-AzureRmApiManagementProduct.md)

[移除-AzureRmApiManagementProduct](./Remove-AzureRmApiManagementProduct.md)

[Set-AzureRmApiManagementProduct](./Set-AzureRmApiManagementProduct.md)


