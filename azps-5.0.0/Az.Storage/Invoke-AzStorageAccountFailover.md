---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139910"
---
# Invoke-AzStorageAccountFailover

## 摘要
喚醒存儲帳戶的容錯移轉。

## 句法

### AccountName (預設) 
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountObject
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
喚醒存儲帳戶的容錯移轉。 如果出現可用性問題，可能會針對儲存帳戶觸發容錯移轉要求。 從存儲帳戶的主要群集到 GRS 帳戶的輔助群集，進行容錯移轉。 在容錯移轉之後，次要群集就會成為主要群集。
啟動容錯移轉之前，請先瞭解下列儲存空間的影響：1.1。 請檢查上次同步處理時間使用 [取得 Blob 服務的統計資料] (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) 、取得資料表服務統計資料 (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) 並取得 https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) 您帳戶的佇列服務 (統計資料。 如果您啟動容錯移轉，這就是您可能會遺失的資料。
2. 在容錯移轉之後，您的儲存帳戶類型將會轉換為本機冗余儲存空間 (LRS) 。 您可以將您的帳戶轉換為使用地域冗余儲存空間， (GRS) 。
3. 針對您的儲存空間帳戶重新啟用 GRS 後，Microsoft 會將資料複製到您的新次要區域。 複製時間取決於要複製的資料量。 請注意，引導程式有頻寬費用。 https://azure.microsoft.com/en-us/pricing/details/bandwidth/

## 示例

### 範例1：喚醒儲存空間帳戶的容錯移轉
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

這個命令會檢查儲存帳戶的 [上次同步處理時間]，然後對其進行容錯移轉，次要群集會成為容錯移轉後的主要。 因為容錯移轉需要花很長的時間，建議您在後端使用-Asjob 參數執行此操作，然後等待工作完成。

## 參數

### -AsJob
在背景中執行 Cmdlet

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

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
強制將帳戶容錯移轉

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

### -InputObject
儲存空間帳戶物件

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
儲存空間帳戶名稱。

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源組名稱。

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### PSStorageAccount 中的 [管理]。

## 筆記

## 相關連結
