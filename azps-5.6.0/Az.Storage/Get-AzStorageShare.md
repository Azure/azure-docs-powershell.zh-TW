---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: 88655ed408242794c6f23a7b170dc007a11ced50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915714"
---
# Get-AzStorageShare

## 簡介
獲得檔案共用清單。

## 語法

### 比對Prefix (預設) 
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### 特定
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## 描述
**Get-AzStorageShare** Cmdlet 會取得儲存帳戶的檔案共用清單。

## 例子

### 範例 1：取得檔案共用
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

此命令會獲得名為 ContosoShare06 的檔案共用。

### 範例 2：取得以字串開頭的所有檔案共用
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

此命令會獲得名稱以 Contoso 開頭的所有檔案共用。

### 範例 3：取得指定內容的所有檔案共用
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

第一個命令使用 **New-AzStorageCoNtext** Cmdlet 使用 *Local* 參數建立上下文，然後將該上下文物件儲存在 $CoNtext 變數中。
第二個命令會針對儲存在檔案中的上下文物件$CoNtext。

### 範例 4：取得具有特定共用名稱稱和 SnapshotTime 的檔案共用快照
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

此命令會獲得具有特定共用名稱稱和 SnapshotTime 的檔案共用快照。

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
若要取得內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。

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

### -名稱
指定檔案共用的名稱。
此 Cmdlet 會獲得此參數指定的檔案共用，如果您指定不存在的檔案共用名稱稱，則沒有任何專案。

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -首碼
指定檔案共用首碼。
此 Cmdlet 會獲得符合此參數指定之首碼的檔案共用，如果沒有檔案共用符合指定的首碼，則不會共用任何檔案。

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
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

### -SnapshotTime
要接收之檔案共用快照的快照時間。

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext

## 輸出

### Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageFileShare

## 筆記

## 相關連結

[New-AzStorageShare](./New-AzStorageShare.md)

[Remove-AzStorageShare](./Remove-AzStorageShare.md)
