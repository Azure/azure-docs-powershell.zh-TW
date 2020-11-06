---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
ms.openlocfilehash: 5cfd42ebbdae85d59bf6715f41ffbe99911ec35c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451540"
---
# Set-AzureStorageContainerAcl

## 摘要
將公用存取許可權設定為儲存容器。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## 說明
**AzureStorageContainerAcl** Cmdlet 會將公用存取許可權設定為 Azure 中指定的儲存空間容器。

## 示例

### 範例1：依名稱設定 azure 儲存空間容器 ACL
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

這個命令會建立沒有公開存取權的容器。

### 範例2：使用管線設定 azure 儲存體容器 ACL
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

這個命令會取得名稱以容器為開頭的所有儲存容器，然後在管線上傳遞結果，將它們的許可權設定為 Blob 存取。

## 參數

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

### -內容
指定 Azure 儲存區內容。
您可以使用 New-AzureStorageContext Cmdlet 來建立它。

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

### -名稱
指定容器名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PassThru
傳回代表您正在使用之專案的物件。
根據預設，這個 Cmdlet 不會產生任何輸出。

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

### -許可權
指定此容器的公開存取層級。
根據預設，容器及其中的任何 blob 只能由儲存空間帳戶的擁有者存取。
若要授權匿名使用者讀取容器及其 blob 的許可權，您可以設定容器許可權來啟用公用存取。
匿名使用者可以在公開提供的容器中讀取 blob，而不需驗證要求。
此參數可接受的值為：

--容器。
提供容器及其 blob 的完整讀取存取權。
用戶端可以透過匿名要求列舉容器中的 blob，但無法在儲存空間帳戶列舉容器。 --Blob。
透過匿名要求提供對容器中 blob 資料的讀取存取權，但不提供容器資料的存取權。
用戶端無法使用匿名要求來列舉容器中的 blob。 -關閉。
限制僅限儲存帳戶擁有者的存取權。

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
指定要求的服務端超時間隔（以秒為單位）。
如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。
針對每個要求的伺服器端超時。

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

### 字串

形參 "Name" 接受管線中類型 "String" 的值

## 輸出

### AzureStorageContainer WindowsAzure. ResourceModel。

## 筆記

## 相關連結

[AzureStorageContainer](./Get-AzureStorageContainer.md)

[新-AzureStorageContainer](./New-AzureStorageContainer.md)

[移除-AzureStorageContainer](./Remove-AzureStorageContainer.md)


