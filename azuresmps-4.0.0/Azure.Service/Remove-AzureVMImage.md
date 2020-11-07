---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967900"
---
# Remove-AzureVMImage

## 摘要
從影像存放庫移除作業系統影像。

## 句法

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**AzureVMImage** Cmdlet 會從影像存放庫中移除作業系統影像。
根據預設，這個 Cmdlet 不會從儲存空間帳戶中刪除關聯的物理影像 blob。
若要刪除關聯的虛擬硬碟 (VHD) ，請使用 **DeleteVHD** 參數。

## 示例

### 範例1：從影像存放庫移除影像
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

這個命令會從影像存放庫中移除名為 Image001 的影像。

### 範例2：從影像存放庫及 VHD 中移除影像
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

這個命令會從影像存放庫中移除名為 Image001 的影像，同時也會從儲存空間帳戶中刪除物理 VHD 影像。

### 範例3：設定訂閱內容，然後移除所有影像
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

這個命令會設定訂閱內容，然後從影像儲存庫中移除其標籤包含名稱 Beta 的所有影像。

## 參數

### -DeleteVHD
表示此 Cmdlet 會從儲存空間帳戶中刪除物理 VHD 映射 blob。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageName
指定要從影像存放庫中移除的作業系統或虛擬機器影像。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

[AzureVMImage](./Get-AzureVMImage.md)

[儲存-AzureVMImage](./Save-AzureVMImage.md)

[更新-AzureVMImage](./Update-AzureVMImage.md)


