---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 4bc06ca07c95986f75062a64a0f86475f7720ff1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915141"
---
# Get-AzStorageBlobCopyState

## 簡介
獲得 Azure 儲存體 Blob 的複製狀態。

## 語法

### NamePipeline (預設) 
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPipeline
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### ContainerPipeline
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## 描述
**Get-AzStorageBlobCopyState** Cmdlet 會取得 Azure 儲存體 Blob 的複製狀態。
它應該在複製目的地 Blob 上執行。

## 例子

### 範例 1：取得 Blob 的複製狀態
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

此命令會獲得容器 ContosoUploads 中名為 ContosoPlanning2015 的 Blob 的複製狀態。

### 範例 2：使用管線取得 Blob 的複製狀態
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

此命令會使用 **Get-AzStorageBlob** Cmdlet，在名為 ContosoUploads 的容器中取得名為 ContosoPlanning2015 的 Blob，然後使用管線運算子將結果傳遞至目前的 Cmdlet。
**Get-AzStorageBlobCopyState** Cmdlet 會取得該 Blob 的複製狀態。

### 範例 3：使用管線取得容器內 Blob 的複製狀態
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

此命令會使用 **Get-AzStorageBlob** Cmdlet 來命名容器，然後將結果傳遞至目前的 Cmdlet。
**Get-AzStorageContainer Cmdlet** 會取得該容器中名為 ContosoPlanning2015 之 Blob 的複製狀態。

### 範例 4：啟動複製和管線以取得複製狀態
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

第一個命令會開始將 Blob "ContosoPlanning2015" 複製到 "ContosoPlanning2015_copy"，並輸出 destiantion Blob 物件。 第二個命令管線將 destiantion Blob 物件用於 Get-AzStorageBlobCopyState，以取得 Blob 複製狀態。 

## 參數

### -Blob
指定 Blob 的名稱。
此 Cmdlet 會針對此參數指定的 Azure 儲存體 Blob，獲得 Blob 複製作業的狀態。

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -CloudBlob
從 **Azure 儲存用戶端文件庫指定 CloudBlob** 物件。
若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CloudBlobContainer
從 **Azure 儲存用戶端文件庫指定 CloudBlobContainer** 物件。
此 Cmdlet 會在此參數指定的容器中，獲得 Blob 的複製狀態。
若要取得 **CloudBlobContainer** 物件，請使用 Get-AzStorageContainer Cmdlet。

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Container
指定容器的名稱。
此 Cmdlet 會在此參數指定的容器中，獲得 Blob 的複製狀態。

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -內容
指定 Azure 儲存內容。
若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。

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

### -WaitForComplete
表示此 Cmdlet 會等待複製完成。
如果您未指定此參數，此 Cmdlet 會立即返回結果。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.storage.Blob.CloudBlob

### Microsoft.Azure.storage.Blob.CloudBlobContainer

### Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext

## 輸出

### Microsoft.Azure.storage.Blob.CopyState

## 筆記

## 相關連結

[Start-AzStorageBlobCopy](./Start-AzStorageBlobCopy.md)

[Stop-AzStorageBlobCopy](./Stop-AzStorageBlobCopy.md)


