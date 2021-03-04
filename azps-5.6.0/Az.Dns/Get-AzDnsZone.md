---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: a788cf3638d124dac164f19171f1be89afc2e385
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910145"
---
# Get-AzDnsZone

## 簡介
獲得 DNS 區域。

## 語法

### 預設 (預設) 
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroup
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 描述
**Get-AzDnsZone** Cmdlet 會從指定的資源群組 (DNS) 區域取得網域名稱系統。
如果您指定 *Name* 參數，會返回單 **一 DnsZone** 物件。
如果您未指定 *Name* 參數，則包含指定資源群組中所有區域之陣列會返回。
您可以使用 **DnsZone 物件** 來更新區域，例如，您可以新增 **RecordSet** 物件至該區域。

## 例子

### 範例 1：取得區域
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

此範例會從指定的資源群組myzone.com DNS 區功能變數名稱稱，然後將它儲存在 $Zone 變數中。

### 範例 2：取得資源群組的所有區域
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

此範例會獲得指定資源群組中所有的 DNS 區域，然後將它儲存在$Zones變數。

### 範例 3：取得訂閱的所有區域
```
PS C:\> $Zones = Get-AzDnsZone
```

此範例會獲得目前 Azure 訂閱中所有的 DNS 區域，然後將它們儲存在 $Zones 變數中。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

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

### -名稱
指定要取得之 DNS 區域的名稱。
如果您沒有為 Name 參數指定值，此 Cmdlet 會獲得指定資源群組中所有的 DNS 區域。
如果您也省略 *ResourceGroupName* 參數，此 Cmdlet 會獲得目前 Azure 訂閱中所有的 DNS 區域。

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含要取得 DNS 區域的資源組名。
如果您未指定 *ResourceGroupName，* 則也必須省略 *Name* 參數。
在此案例中，此 Cmdlet 會獲得目前 Azure 訂閱中所有的 DNS 區域。

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.dns.DnsZone

## 筆記

## 相關連結

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
