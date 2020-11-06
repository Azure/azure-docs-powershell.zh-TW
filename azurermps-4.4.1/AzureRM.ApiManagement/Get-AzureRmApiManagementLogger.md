---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: 48033c250286c59e2cadfadc1a5b5d28f869a66c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452631"
---
# Get-AzureRmApiManagementLogger

## 摘要
取得 API 記錄管理器物件。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 取得所有的記錄器 (預設) 
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### 依記錄器識別碼取得
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmApiManagementLogger** Cmdlet 會取得 Azure API 管理 **記錄器** 或所有的記錄器。

## 示例

### 範例1：取得所有的記錄器
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext
```

這個命令會取得指定內容的所有記錄器。

### 範例2：取得特定的記錄器
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123"
```

這個命令會移除 ID 為 Logger123 的記錄器。

## 參數

### -內容
指定 **PsApiManagementCoNtext** 物件。

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

### -LoggerId
指定要取得的特定記錄器的識別碼。

```yaml
Type: System.String
Parameter Sets: Get by logger ID
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

### IList<ApiManagement. ServiceManagement. PsApiManagementLogger]>

## 筆記

## 相關連結

[新-AzureRmApiManagementLogger](./New-AzureRmApiManagementLogger.md)

[移除-AzureRmApiManagementLogger](./Remove-AzureRmApiManagementLogger.md)

[Set-AzureRmApiManagementLogger](./Set-AzureRmApiManagementLogger.md)


