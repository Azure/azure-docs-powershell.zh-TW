---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 101440e65fbc0bb21311757a8792a2d45f855364
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612496"
---
# New-AzDnsZone

## 摘要
建立新的 DNS 區域。

## 句法

### 識別碼 (預設) 
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 名稱
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 物件
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzDnsZone** Cmdlet 會在指定的資源群組 (DNS) 區域中建立新的網域名稱系統。 您必須為 *name* 參數指定唯一的 DNS 區功能變數名稱稱，否則 Cmdlet 會傳回錯誤。 建立區域之後，請使用 New-AzDnsRecordSet Cmdlet 來建立區域中的記錄集。
您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。

## 示例

### 範例1：建立 DNS 區域
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

這個命令會在指定的資源群組中建立名為 myzone.com 的新 DNS 區域，然後將它儲存在 $Zone 變數中。

### 範例2：透過指定虛擬網路識別碼來建立私人 DNS 區域
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

這個命令會在指定的資源群組中，建立一個名為 myprivatezone.com 的新私人 DNS 區域， (指定其識別碼) ，然後將其儲存在 $Zone 變數中。

### 範例3：透過指定虛擬網路物件來建立私人 DNS 區域
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

這個命令會在指定的資源 (群組中，建立一個名為 myprivatezone.com 的新私人 DNS 區域，並 $ResVirtualNetwork 變數) ，然後將它儲存在 $Zone 變數中。

### 範例4：透過指定父區功能變數名稱稱來建立含委派的 DNS 區域
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

這個命令會在指定的資源群組中建立名為 mychild.zone.com 的新的子 DNS 區域，並將其儲存在 $Zone 變數中。
它也會在名為 zone.com 的父 DNS 區域中新增委派，且該區域位於與子領域相同的訂閱和資源群組中。

### 範例5：透過指定父區域識別碼來建立含委派的 DNS 區域
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

這個命令會在指定的資源群組中建立名為 mychild.zone.com 的新的子 DNS 區域，並將其儲存在 $Zone 變數中。
它也會在資源群組中名為 zone.com 的父 DNS 區域中新增委派，而另一個 rg 提供的訂閱與建立的子領域相同。

### 範例6：透過指定父區域物件來建立含委派的 DNS 區域
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

這個命令會在指定的資源群組中建立名為 mychild.zone.com 的新的子 DNS 區域，並將其儲存在 $Zone 變數中。
它也會在名為 zone.com 的父 DNS 區域中新增委派，就像在 ParentZone 物件中傳遞一樣

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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
指定要建立之 DNS 區域的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentZone
父區域的完整名稱，以新增委派 (，但不需終止點) 。

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentZoneId
要新增 (委派的父區域的資源識別碼，不需終止點) 。

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentZoneName
父區域的完整名稱，以新增委派 (，但不需終止點) 。

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationVirtualNetwork
將在這個 DNS 區域中註冊虛擬機器主機名稱記錄的虛擬網路清單，只適用于私人區域。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationVirtualNetworkId
將在這個 DNS 區域中登錄虛擬機器主機名稱記錄的虛擬網路 Id 清單，只適用于私人區域。

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetwork
可解析此 DNS 區域中之記錄的虛擬網路清單，只能供私人區域使用。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetworkId
可解析此 DNS 區域中之記錄的虛擬網路 Id 清單，只適用于私人區域。

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定要在其中建立區域的資源群組。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
雜湊資料表形式的索引鍵/值對。 例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ZoneType
該區域的類型為 [公用] 或 [私人]。 在 DNS 階層中使用的公用 DNS 服務平面上提供不含類型或屬於 Public 類型的區域。 具有私人類型的區域只會與一組關聯的虛擬網路一起顯示 (這項功能在預覽) 中。 此屬性無法針對區域進行變更。

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### "ZoneType" 1 [[3.0.0.0 版]。 Dns，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]] （"）]

### [System.object] 集合. Hashtable

### [System.object]。清單 ' 1 [CoreLib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]

### [System.object]. 清單 ' 1 [IResourceReference] （31bf3856ad364e35）。網路，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = "]] （區域性 = 中立）

## 輸出

### DnsZone （）

## 筆記
您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。
根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。
如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。
如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。

## 相關連結

[AzDnsZone](./Get-AzDnsZone.md)

[新-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[移除-AzDnsZone](./Remove-AzDnsZone.md)
