---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: b2c623d46dcc2d84e2c90ae5f3d94cfb54f7224a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450135"
---
# Get-AzureRmApiManagementOperation

## 摘要
取得清單或指定的 API 操作。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 所有 API 作業 (預設) 
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 依識別碼尋找
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmApiManagementOperation** 會取得清單或指定的 API 操作。

## 示例

### 範例1：取得所有 API 管理作業
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId
```

這個命令會取得所有 API 管理作業。

### 範例2：依作業 ID 取得 API 管理作業
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation003"
```

這個命令會透過名為 Operation0003 的操作 ID 取得 API 管理作業。

## 參數

### -ApiId
指定 API 操作的識別碼。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -OperationId
指定操作識別碼。

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
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

### IList<ApiManagement. ServiceManagement. PsApiManagementOperation]>

## 筆記

## 相關連結

[新-AzureRmApiManagementOperation](./New-AzureRmApiManagementOperation.md)

[移除-AzureRmApiManagementOperation](./Remove-AzureRmApiManagementOperation.md)

[Set-AzureRmApiManagementOperation](./Set-AzureRmApiManagementOperation.md)


