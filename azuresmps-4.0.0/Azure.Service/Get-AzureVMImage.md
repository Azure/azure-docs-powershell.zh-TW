---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967978"
---
# Get-AzureVMImage

## 摘要
取得其中一個或一組作業系統或影像存放庫中的虛擬機器影像的屬性。

## 句法

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**AzureVMImage** Cmdlet 會在一個或多個作業系統清單或影像存放庫中的虛擬機器影像上取得屬性。
這個 Cmdlet 會傳回存放庫中所有影像的資訊，如果提供其影像名稱，則會傳回特定影像的資訊。

## 示例

### 範例1：從目前的影像存放庫取得特定影像物件。
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

這個命令會從目前的影像存放庫取得名為 Image001 的 image 物件。

### 範例2：從目前的影像存放庫取得所有影像
```
PS C:\> Get-AzureVMImage
```

這個命令會從目前的影像存放庫中檢索所有影像。

### 範例3：設定訂閱內容，然後取得所有影像
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

這個命令會設定訂閱內容，然後從影像存放庫中檢索所有影像。

## 參數

### -ImageName
指定影像存放庫中的作業系統或虛擬機器影像的名稱。
如果您沒有指定此參數，則會傳回所有影像。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
指定這個 Cmdlet 回應資訊事件的方式。

此參數可接受的值為：

- 持續
- 理會
- 看
- SilentlyContinue
- 停止
- 封存

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
指定資訊變數。

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[附加 AzureVMImage](./Add-AzureVMImage.md)

[移除-AzureVMImage](./Remove-AzureVMImage.md)

[儲存-AzureVMImage](./Save-AzureVMImage.md)

[更新-AzureVMImage](./Update-AzureVMImage.md)


