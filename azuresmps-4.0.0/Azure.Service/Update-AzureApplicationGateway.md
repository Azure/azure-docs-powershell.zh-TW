---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967290"
---
# Update-AzureApplicationGateway

## 摘要
更新應用程式閘道。

## 句法

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureApplicationGateway** Cmdlet 會更新現有的應用程式閘道。

## 示例

### 範例1：使用名稱來修改應用程式閘道
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

第一個命令會停止名為 ApplicationGateway06 的應用程式閘道。
您必須先停止應用程式閘道，才能修改虛擬網路或子網。

第二個命令會修改名為 ApplicationGateway06 的應用程式閘道的虛擬子網和子網。

### 範例2：修改應用程式閘道的其他屬性
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

這個命令會修改名為 ApplicationGateway06 的應用程式閘道的實例計數、閘道大小及描述。
這個命令不會修改應用程式閘道的虛擬網路或子網。
因此，在執行這個命令之前，您不需要停止應用程式閘道。

### 範例3：使用管線修改應用程式閘道
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

第一個命令會使用 **AzureApplicationGateway** Cmdlet 取得名為 ApplicationGateway06 的應用程式閘道。
該命令會將它儲存在 $ApplicationGateway 變數中。

第二個命令會將 **GatewaySize** 屬性指派為值中。

最終命令會將更新的 $ApplicationGateway 傳遞至目前的 Cmdlet。

## 參數

### -描述
指定此 Cmdlet 指派給應用程式閘道的描述。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GatewaySize
指定此 Cmdlet 指派給應用程式閘道的大小。
有效值為：

- 小規模
- 深淺
- 大中型

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceCount
指定此 Cmdlet 指派給應用程式閘道的實例數。

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 更新之應用程式閘道的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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

### -子網
指定此 Cmdlet 在其中部署應用程式閘道的子網陣列。

當應用程式閘道正在執行時，您無法更新子網。
若要停止應用程式閘道，請使用 Stop-AzureApplicationGateway Cmdlet。

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VnetName
指定此 Cmdlet 在哪個虛擬網路中部署應用程式閘道。

當應用程式閘道正在執行時，您無法更新虛擬網路。
若要停止應用程式閘道，請使用 **停止 AzureApplicationGateway** 。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### ApplicationGatewayOperationResponse 的 ApplicationGateway。 WindowsAzure

## 筆記

## 相關連結

[AzureApplicationGateway](./Get-AzureApplicationGateway.md)

[新-AzureApplicationGateway](./New-AzureApplicationGateway.md)

[移除-AzureApplicationGateway](./Remove-AzureApplicationGateway.md)

[開始-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[停止 AzureApplicationGateway](./Stop-AzureApplicationGateway.md)
