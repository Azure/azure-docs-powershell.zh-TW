---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967187"
---
# Stop-AzureVM

## 摘要
關閉 Azure 虛擬機器。

## 句法

### ByName (預設) 
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### 輸出
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## 說明
**Stop-add-azurevm** Cmdlet 會關閉虛擬機器。

## 示例

### 範例1：關閉虛擬機器
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

這個命令會關閉指定服務所包含的虛擬機器。

### 範例2：使用虛擬電腦物件關閉虛擬機器
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

這個命令會透過使用由 **add-azurevm** 傳回的虛擬機器物件，來關閉指定服務所包含的虛擬機器。

### 範例3：關閉 VM 並保持 VM 已預配
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

這個命令會關閉指定服務所包含的虛擬機器，並保持其已預配。

### 範例4：關閉 VM 並允許解除在部署中的最後一個 VM
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

這個命令會關閉指定服務所包含的虛擬機器，並允許解除部署中的最後一個虛擬機器。

### 範例5：關閉多個 Vm
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

這個命令會關閉指定服務所包含的多個虛擬機器。

## 參數

### -Force
指定是否允許解除配置部署中的最後一個虛擬機器。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### -名稱
指定要關閉的虛擬機器的名稱。

使用萬用字元來非同步停止多個虛擬機器。
使用萬用字元時，這個 Cmdlet 會呼叫關閉角色作業 https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx (https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) ，而不是關閉角色 https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx 操作 (https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) 。

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
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
指定包含要關閉之虛擬機器之 Azure 服務的名稱。

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

### -StayProvisioned
指定此 Cmdlet 會保留預配的虛擬機器。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
指定識別要關閉之虛擬機器的虛擬機器物件。

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
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

[Add-azurevm](./Get-AzureVM.md)

[Add-azurevm](./New-AzureVM.md)

[Restart-Add-azurevm](./Restart-AzureVM.md)

[開始-Add-azurevm](./Start-AzureVM.md)


