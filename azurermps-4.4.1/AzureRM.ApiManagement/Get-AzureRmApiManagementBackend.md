---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 4f54b361482bad24826d7120e53f96ce8d3b9eef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450940"
---
# Get-AzureRmApiManagementBackend

## 摘要
取得後端的詳細資料。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 取得所有 backends (預設) 
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### 依後端識別碼取得
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
取得後端的詳細資料。

## 示例

### --------------------------範例 1--------------------------
@ {段落 = PS C： \\ \> }







```
Get-AzureRmApiManagementBackend -Context $apimContext
```

取得 Api 管理服務中設定的所有 Backends 的清單。

### --------------------------範例 2--------------------------
@ {段落 = PS C： \\ \> }







```
Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

取得識別碼「123」所識別之指定後端的詳細資料

## 參數

### -BackendId
後端的識別碼。
如果已指定，將會嘗試透過識別碼尋找後端。
這個參數是選用的。

```yaml
Type: System.String
Parameter Sets: Get by backend ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -內容
PsApiManagementCoNtext 的實例。
這個參數是必要的。

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

### IList<ApiManagement. ServiceManagement. PsApiManagementBackend]>

### PsApiManagementLogger.. PsApiManagementBackend （ApiManagement） ServiceManagement

## 筆記

## 相關連結

[新-AzureRmApiManagementBackend](./New-AzureRmApiManagementBackend.md)

[新-AzureRmApiManagementBackendCredential](./New-AzureRmApiManagementBackendCredential.md)

[新-AzureRmApiManagementBackendProxy](./New-AzureRmApiManagementBackendProxy.md)

[Set-AzureRmApiManagementBackend](./Set-AzureRmApiManagementBackend.md)

[移除-AzureRmApiManagementBackend](./Remove-AzureRmApiManagementBackend.md)
