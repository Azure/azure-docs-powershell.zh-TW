---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: e4313dda57632fbc2a5381b1f92067da85c1a905
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915117"
---
# Get-AzStorageCORSRule

## 簡介
為儲存服務類型獲得 CORS 規則。

## 語法

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## 描述
**Get-AzStorageCORSRule** Cmdlet 會取得 Azure 儲存服務類型的 (CORS) 規則。

## 例子

### 範例 1：取得 Blob 服務的 CORS 規則
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

此命令會獲得 Blob 服務類型的 CORS 規則。

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
指定 Azure 儲存內容。
若要取得內容，請使用 New-AzStorageContext Cmdlet。

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

### -ServerTimeoutPerRequest
指定要求的伺服器部分之時間長度。

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

### -ServiceType
指定此 Cmdlet 會獲得 CORS 規則的 Azure 儲存體服務類型。
此參數可接受的值為：
- Blob 
- 表 
- 佇列 
- 檔

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext

## 輸出

### Microsoft.WindowsAzure.Commands.storage.Model.ResourceModel.PSCorsRule

## 筆記

## 相關連結

[Remove-AzStorageCORSRule](./Remove-AzStorageCORSRule.md)

[Set-AzStorageCORSRule](./Set-AzStorageCORSRule.md)


