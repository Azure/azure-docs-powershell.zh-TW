---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967993"
---
# Get-AzureVM

## 摘要
從一或多個 Azure 虛擬機器中檢索資訊。

## 句法

### ListAllVMs (預設) 
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### GetVMByServiceAndVMName
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**Add-azurevm** Cmdlet 會檢索在 Azure 中執行之虛擬機器的相關資訊。
它會傳回包含特定虛擬機器上資訊的物件，或者如果沒有指定虛擬機器，則會針對目前訂閱的指定服務中的所有虛擬機器傳回該物件。

## 示例

### 範例1：在指定的虛擬機器上檢索資訊
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

這個命令會傳回一個物件，其中包含在 ContosoService01 雲端服務中執行之 VirtualMachine02 虛擬機器的資訊。

### 範例2：在所有虛擬機器上檢索資訊
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

這個命令會以 ContosoService01 雲端服務中執行的所有虛擬機器資訊來檢索清單物件。

### 範例3：顯示虛擬機器狀態資料表
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

這個命令會顯示一個表格，其中顯示在 ContosoService01 服務上執行的虛擬機器、其升級網域，以及每個虛擬機器的目前狀態。

## 參數

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

### -名稱
指定要為其檢索資訊之虛擬機器的名稱。
如果未提供此參數，則 Cmdlet 會傳回清單物件，其中包含有關指定服務中所有虛擬機器的資訊。

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ServiceName
指定要傳回虛擬機器資訊之雲端服務的名稱。

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
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

[Add-azurevm](./New-AzureVM.md)

[新-AzureVMConfig](./New-AzureVMConfig.md)

[Add-azurevm](./Remove-AzureVM.md)

[Restart-Add-azurevm](./Restart-AzureVM.md)

[開始-Add-azurevm](./Start-AzureVM.md)

[靜幀](./Stop-AzureVM.md)

[更新-Add-azurevm](./Update-AzureVM.md)


