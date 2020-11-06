---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
ms.openlocfilehash: da3b5f969bfa8beafab20f256df237588ed87048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446592"
---
# Get-AzureStorageBlob

## 摘要
列出容器中的 blob。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### BlobName (預設) 
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPrefix
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## 說明
**AzureStorageBlob** Cmdlet 會在 Azure 儲存空間帳戶的指定容器中列出 blob。

## 示例

### 範例1：透過 blob 名稱取得 blob
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

這個命令使用 blob 名稱和萬用字元來取得 blob。

### 範例2：使用管線在容器中取得 blob
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False      
```

這個命令會使用管線來取得所有 blob (在容器中的 [刪除狀態]) 中包含 blob。

### 範例3：透過名稱首碼取得 blob
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

這個命令會使用名稱首碼來取得 blob。

### 範例4：多個批次中的清單 blob
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

這個範例使用 *MaxCount* 和 *ContinuationToken* 參數，以多個批次列出 Azure 存儲區 blob。
前四個命令會將值指派給要在範例中使用的變數。

第五個命令指定一個 **Do** 語句，該語句使用 **AzureStorageBlob** Cmdlet 來取得 blob。
該語句包含儲存在 $Token 變數中的延續標記。
在迴圈執行時 $Token 變更值。
如需詳細資訊，請輸入 `Get-Help About_Do` 。

最後一個命令會使用 **Echo** 命令來顯示合計。

## 參數

### -Blob
指定可用於萬用字元搜尋的名稱或名稱模式。
如果未指定任何 blob 名稱，則 Cmdlet 會列出指定容器中的所有 blob。
如果為此參數指定一個值，則 Cmdlet 會列出名稱與此參數相符的所有 blob。

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -ClientTimeoutPerRequest
指定一個服務要求的用戶端超時間隔（以秒為單位）。
如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。
如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
指定最大併發網路通話數。
您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。
指定的值是絕對計數，不會乘以核心計數。
這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。
預設值為10。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -容器
指定容器的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -內容
指定您想要取得其 blob 清單的 Azure 儲存空間帳戶。
您可以使用 New-AzureStorageContext Cmdlet 來建立儲存內容。

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContinuationToken
指定 blob 清單的延續標記。
使用此參數與 *MaxCount* 參數，在多個批次中列出 blob。

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeDeleted
包含刪除的 Blob，預設的 [取得 blob] 不會包含已刪除的 blob。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
指定此 Cmdlet 傳回的物件數目上限。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Prefix
針對您要取得的 blob 名稱指定一個前置詞。
這個參數不支援使用正則運算式或萬用字元來進行搜尋。
這表示如果容器只有一個名為 "My"、"MyBlob1" 和 "MyBlob2" 的 blob，且您指定了 "-Prefix My *"，則 Cmdlet 不會傳回 blob。
不過，如果您指定了 "-Prefix My"，此 Cmdlet 會傳回 "My"、"MyBlob1" 和 "MyBlob2"。

```yaml
Type: String
Parameter Sets: BlobPrefix
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
指定要求的服務端超時間隔（以秒為單位）。
如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### IStorageCoNtext
參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值

## 輸出

### AzureStorageBlob

## 筆記

## 相關連結

[AzureStorageBlobContent](./Get-AzureStorageBlobContent.md)

[移除-AzureStorageBlob](./Remove-AzureStorageBlob.md)

[Set-AzureStorageBlobContent](./Set-AzureStorageBlobContent.md)


