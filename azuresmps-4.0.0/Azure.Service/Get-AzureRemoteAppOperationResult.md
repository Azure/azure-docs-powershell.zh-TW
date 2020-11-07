---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967768"
---
# Get-AzureRemoteAppOperationResult

## 摘要
檢索 Azure RemoteApp 作業的結果。

## 句法

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureRemoteAppOperationResult** Cmdlet 會檢索長時間執行的 Azure RemoteApp 作業的結果。
Azure RemoteApp 針對需要服務處理且無法立即傳回的許多動作，使用長時間執行的作業。
傳回追蹤識別碼的 Cmdlet 範例包括 [ **更新-AzureRemoteAppCollection** ]、[ **設定 AzureRemoteAppWorkspace** **]、[中斷連線] AzureRemoteAppSession** 及其他。

## 示例

### 範例1：使用追蹤識別碼來取得運算結果
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

這個命令會儲存從 Azure RemoteApp 作業傳回的追蹤識別碼。
追蹤識別碼會傳遞到下列命令中的 **AzureRemoteAppOperationResult** 。

## 參數

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrackingId
指定作業的追蹤識別碼。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[中斷連線-AzureRemoteAppSession](./Disconnect-AzureRemoteAppSession.md)

[Set-AzureRemoteAppWorkspace](./Set-AzureRemoteAppWorkspace.md)

[更新-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


