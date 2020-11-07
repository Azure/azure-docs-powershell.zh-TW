---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967274"
---
# Set-AzureOSDisk

## 摘要
修改 Azure 虛擬機器的主機緩存模式。

## 句法

### NoResize
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### 大小
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## 說明
**AzureOSDisk** Cmdlet 會修改 Azure 虛擬機器之作業系統磁片的主機緩存模式。
支援的 host cache 模式為 ReadOnly 和 ReadWrite。
如果您在執行中的虛擬機器上執行這個 Cmdlet，該虛擬機器就會重新開機。

## 示例

### 範例1：使用管線將主機快取模式設定為 ReadOnly
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

這個命令會透過使用 **VirtualMachine02 Cmdlet，** 在名為 ContosoService 的服務中，取得名為的虛擬機器。
命令會使用管線運算子，將虛擬機器傳至目前的 Cmdlet。
目前的 Cmdlet 會將該虛擬機器的作業系統磁片的主機快取模式設定為 ReadOnly。

### 範例2：將主機快取模式設定為 ReadWrite
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

第一個命令會在名為 ContosoService 的服務中取得名為 VirtualMachine02 的虛擬機器，然後將它儲存在變數中。

第二個命令會將該虛擬機器之作業系統磁片的主機快取模式設定為 ReadWrite。

## 參數

### -HostCaching
指定作業系統磁片的 host cache 屬性。
有效值為： 

- 唯讀 
- 讀

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
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

### -ResizedSizeInGB
指定作業系統磁片的新大小（以 gb 為位元組）。
大小必須大於目前的大小。

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
指定此 Cmdlet 修改作業系統磁片的虛擬機器。
若要取得虛擬機器物件，請使用 **add-azurevm** Cmdlet。

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[附加 AzureVMImage](./Add-AzureVMImage.md)

[AzureOSDisk](./Get-AzureOSDisk.md)

[Add-azurevm](./Get-AzureVM.md)

[AzureVMImage](./Get-AzureVMImage.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[更新-Add-azurevm](./Update-AzureVM.md)


