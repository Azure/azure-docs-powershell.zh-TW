---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 8c48c7ec1f651348309c012275287bd88dd42bcc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275455"
---
# New-AzPublicIpAddress

## 摘要
建立公用 IP 位址。

## 句法

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzPublicIpAddress** Cmdlet 會建立公用 IP 位址。

## 示例

### 範例1：建立新的公用 IP 位址
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

這個命令會建立新的公用 IP 位址資源。此時會建立 DNS 記錄，$location $dnsPrefix 指向此資源的公用 IP 位址。 公用 IP 位址會立即分配給此資源，因為-AllocationMethod 被指定為「Static」。 如果將其指定為「動態」，則只有當您開始 (或建立) 相關聯的資源 (例如 VM 或負載平衡器) 時，才會指派公用 IP 位址。

### 範例2：使用反向 FQDN 建立公用 IP 位址
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

這個命令會建立新的公用 IP 位址資源。 在 ReverseFqdn 參數中，Azure 會為指派給此資源的公用 IP 位址 (反向查閱) 建立 DNS PTR 記錄，並指向命令中指定的 $customFqdn。 就像預先必備，$customFqdn (說 webapp.contoso.com) 應該有 DNS CNAME 記錄 (轉寄查詢) 指向 $dnsPrefix。 $location. cloudapp.azure.com。

### 範例3：使用 IpTag 建立新的公用 IP 位址
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

這個命令會建立新的公用 IP 位址資源。此時會建立 DNS 記錄，$location $dnsPrefix 指向此資源的公用 IP 位址。 公用 IP 位址會立即分配給此資源，因為-AllocationMethod 被指定為「Static」。 如果將其指定為「動態」，則只有當您開始 (或建立) 相關聯的資源 (例如 VM 或負載平衡器) 時，才會指派公用 IP 位址。 Iptag 是用來指定與資源相關的標籤。 Iptag 可以使用 New-AzPublicIpTag 來指定，並透過 IpTags 傳送為輸入。

### 範例4：從首碼建立新的公用 IP 位址
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

這個命令會建立新的公用 IP 位址資源。 此時會建立 DNS 記錄，$location $dnsPrefix 指向此資源的公用 IP 位址。 從指定的 publicIpPrefix，會立即將公用 IP 位址指派給此資源。
此選項僅支援「標準」 Sku 和「靜態」 AllocationMethod。

### 範例5：建立新的全域公用 IP 位址
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

這個命令會建立新的全域公用 IP 位址資源。此時會建立 DNS 記錄，$location $dnsPrefix 指向此資源的公用 IP 位址。 全域公用 IP 位址會立即指派給此資源。
此選項僅支援「標準」 Sku 和「靜態」 AllocationMethod。

## 參數

### -AllocationMethod
指定要用來指派公用 IP 位址的方法。
此參數可接受的值為： Static 或 Dynamic。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AsJob
在背景中執行 Cmdlet

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -DomainNameLabel
指定公用 IP 位址的相對 DNS 名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
強制執行命令，而不要求使用者確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
指定空閒超時（以分鐘為單位）。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpAddressVersion
指定 IP 位址的版本。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
IpTag 清單]。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -位置
指定建立公用 IP 位址的區域。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 所建立之公用 IP 位址的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIpPrefix
指定要從哪個 PSPublicIpPrefix 指派公用 IP 位址。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定要在其中建立公用 IP 位址的資源群組的名稱。

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

### -ReverseFqdn
指定 (FQDN) 的反向完整功能變數名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
公用 IP Sku 名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
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
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 層級
公用 IP Sku 層。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
代表資源所分派的 IP 必須來自的可用性區域清單。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

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
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### PSPublicIpTag [] （[]）

### PSPublicIpPrefix 中的 [.]

### System.object

### System.object []

### [System.object] 集合. Hashtable

## 輸出

### PSPublicIpAddress 中的 [.]

## 筆記

## 相關連結

[AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[移除-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)

[Set-AzPublicIpAddress](./Set-AzPublicIpAddress.md)
