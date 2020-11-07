---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967503"
---
# Set-AzureEndpoint

## 摘要
修改指派給虛擬機器的端點。

## 句法

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**AzureEndpoint** Cmdlet 會修改指派給 Azure 虛擬機器的端點。
您可以指定對未進行負載平衡的端點所做的變更。

## 示例

### 範例1：修改端點以偵聽埠
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

這個命令會使用 **add-azurevm** Cmdlet 來檢索名為 VirtualMachine01 的虛擬機器的設定。
命令會使用管線運算子將它傳遞到目前的 Cmdlet。
這個 Cmdlet 會修改名為 [Web] 的端點，以在埠443上聆聽。
該命令會將虛擬機器物件傳遞到會實現變更的 **add-azurevm** Cmdlet。

## 參數

### -ACL
指定 (ACL) 設定物件的存取控制清單，此 Cmdlet 會套用到端點。

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DirectServerReturn
指定此 Cmdlet 是否允許直接返回伺服器。
指定要啟用 $True，或 $False 以停用。

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
指定端點的 TCP 空閒超時期間（以分鐘為單位）。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### -InternalLoadBalancerName
指定內部負載平衡器的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerDistribution
指定負載平衡器分配演算法。
有效值為： 

- sourceIP.
兩個元組關聯：來源 IP、目的地 IP 
- sourceIPProtocol.
三個元組關聯：來源 IP、目的地 IP、通訊協定 
- 所有.
五個元組關聯：來源 IP、來源埠、目的地 IP、目的地埠、通訊協定 

預設值為 [無]。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalPort
指定此端點所使用的本機、私人埠。
虛擬機器中的應用程式在此埠上偵聽此端點的服務輸入要求。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定端點的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

### -通訊協定
指定端點的通訊協定。
有效值為： 

- tcp-out 
- udp-in

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicPort
指定端點使用的公用埠。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualIPName
指定 Azure 與端點相關聯之虛擬 IP 位址的名稱。
您的服務可以有多個虛擬 Ip。
若要建立虛擬 Ip，請使用 **AzureVirtualIP** Cmdlet。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
指定端點所屬的虛擬機器。

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

### System.object

## 筆記

## 相關連結

[附加 AzureEndpoint](./Add-AzureEndpoint.md)

[附加 AzureVirtualIP](./Add-AzureVirtualIP.md)

[AzureEndpoint](./Get-AzureEndpoint.md)

[Add-azurevm](./Get-AzureVM.md)

[移除-AzureEndpoint](./Remove-AzureEndpoint.md)

[更新-Add-azurevm](./Update-AzureVM.md)


