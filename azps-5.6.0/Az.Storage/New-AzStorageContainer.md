---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: d726ec3fe70ca329f6e5c07ea7aae46de4ad048a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915090"
---
# New-AzStorageContainer

## 簡介
建立 Azure 儲存容器。

## 語法

### ContainerName (預設) 
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### EncryptionScope
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## 描述
**New-AzStorageContainer** Cmdlet 會建立 Azure 儲存容器。

## 例子

### 範例 1：建立 Azure 儲存容器
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

此命令會建立儲存容器。

### 範例 2：建立多個 Azure 儲存容器
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

此範例會建立多個儲存容器。
它 **使用** .NET **String** 類的 Split 方法，然後傳遞管線上的名稱。

### 範例 3：使用加密範圍建立 Azure 儲存容器
```
PS C:\> $container = New-AzStorageContainer  -Name "mycontainer" -DefaultEncryptionScope "myencryptscope" -PreventEncryptionScopeOverride $true 

PS C:\> $container.BlobContainerProperties.DefaultEncryptionScope
myencryptscope

PS C:\> $container.BlobContainerProperties.PreventEncryptionScopeOverride
True
```

此命令會建立儲存容器，使用預設加密範圍做為 myencryptscope，並使用不同的加密範圍預先轉換 Blob 上傳至此容器。

## 參數

### -ClientTimeoutPerRequest
指定一個服務要求用戶端的時間間隔 ，以秒為單位。
如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。
如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
指定同時進行的最大網路通話數。
您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。
指定的值是絕對計數，不會乘以核心計數。
此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。
預設值為 10。

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -內容
指定新容器的上下文。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultEncryptionScope
將容器預設為針對所有寫入使用指定的加密範圍。

```yaml
Type: System.String
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定新容器的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -許可權
指定此容器的公用存取層級。
根據預設，容器及其中任何 Blob 只能由儲存帳戶的擁有者存取。
若要將匿名使用者的讀取權限授予容器及其 Blob，您可以設定容器許可權以啟用公用存取。
匿名使用者可以讀取公開容器中的 Blob，而不必驗證要求。
此參數可接受的值為：
- 容器。
提供容器及其 Blob 的完整讀取存取權。
用戶端可以透過匿名要求列舉容器中的 Blob，但無法列舉儲存帳戶中的容器。 
- Blob。
透過匿名要求，在整個容器內提供 Blob 資料的讀取存取，但不提供容器資料的存取權。
用戶端無法使用匿名要求列舉容器中的 Blob。 
- 關閉。
這只會限制存取儲存空間帳戶擁有者。

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreventEncryptionScopeOverride
從容器預設封鎖加密範圍的重寫。

```yaml
Type: System.Boolean
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
指定服務端要求的時間間隔 ，以秒為單位。
如果指定的時間間隔在服務處理要求之前已經過，儲存服務會返回錯誤。

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext

## 輸出

### Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageContainer

## 筆記

## 相關連結

[Get-AzStorageContainer](./Get-AzStorageContainer.md)

[Remove-AzStorageContainer](./Remove-AzStorageContainer.md)

[Set-AzStorageContainerAcl](./Set-AzStorageContainerAcl.md)


