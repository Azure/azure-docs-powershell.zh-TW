---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967998"
---
# Get-AzureStorSimpleAccessControlRecord

## 摘要
取得服務設定中的存取控制記錄。

## 句法

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureStorSimpleAccessControlRecord** Cmdlet 會取得 StorSimple Manager 服務設定中的存取控制記錄。
這個 Cmdlet 會取得所有記錄或命名記錄。

存取控制記錄是 iSCSI 啟動器參數的容器。
這些參數指定哪些啟動器可以存取卷。
當 iSCSI 啟動器嘗試連線到某個磁片時，裝置會檢查指派給該卷的存取控制記錄。
如果 iSCSI 啟動器參數與對應至該卷的存取控制記錄中的其中一個專案相符，iSCSI 啟動器就可以連線。

## 示例

### 範例1：取得所有存取控制記錄
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

這個命令會取得所有存取控制記錄。

### 範例2：取得特定的存取控制記錄
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

這個命令會取得名為 Acr11 的存取控制記錄。

## 參數

### -ACRName
指定要取得的存取控制記錄的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定 Azure 設定檔。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### AccessControlRecord、IList\<AccessControlRecord\>
這個 Cmdlet 會傳回 **AccessControlRecord** 物件或 **IList \<AccessControlRecord\>** 物件。
**AccessControlRecord** 物件包含下欄欄位： 

- **GlobalId** ( **字串** )  
- **InitiatorName** ( **字串** )  
- **InstanceId** ( **字串** )  
- **名稱** ( **字串** )  
- **OperationInProgress** ( **OperationInProgress** )  
- **VolumeCount** ( **int** ) 

## 筆記

## 相關連結

[新-AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[移除-AzureStorSimpleAccessControlRecord](./Remove-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)


