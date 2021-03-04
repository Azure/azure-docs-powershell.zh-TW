---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: d1b5fb606262b680d4e83f9c8e0a9ea166070ed4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910109"
---
# <span data-ttu-id="8da57-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8da57-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="8da57-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8da57-102">SYNOPSIS</span></span>
<span data-ttu-id="8da57-103">更新 DNS 區域的屬性。</span><span class="sxs-lookup"><span data-stu-id="8da57-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="8da57-104">語法</span><span class="sxs-lookup"><span data-stu-id="8da57-104">SYNTAX</span></span>

### <span data-ttu-id="8da57-105">欄位 (預設) </span><span class="sxs-lookup"><span data-stu-id="8da57-105">Fields (Default)</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da57-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="8da57-106">FieldsObjects</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da57-107">物件</span><span class="sxs-lookup"><span data-stu-id="8da57-107">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8da57-108">描述</span><span class="sxs-lookup"><span data-stu-id="8da57-108">DESCRIPTION</span></span>
<span data-ttu-id="8da57-109">**Set-AzDnsZone Cmdlet** 會更新 Azure DNS 服務中指定的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="8da57-109">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="8da57-110">此 Cmdlet 不會更新區域中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="8da57-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="8da57-111">您可以傳遞 **DnsZone 物件** 做為參數，或是使用管線運算子，或者您也可以指定 *ZoneName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="8da57-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="8da57-112">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8da57-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8da57-113">使用 Zone 物件或管線 (以物件傳遞 DNS 區域時) ，自已取回本地 Dns Zone 物件之後，若已在 Azure DNS 中變更，則不會更新區域。</span><span class="sxs-lookup"><span data-stu-id="8da57-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="8da57-114">這可保護同時進行變更。</span><span class="sxs-lookup"><span data-stu-id="8da57-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="8da57-115">您可以使用覆寫參數隱藏此行為，無論同時變更，都會更新區域。</span><span class="sxs-lookup"><span data-stu-id="8da57-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="8da57-116">例子</span><span class="sxs-lookup"><span data-stu-id="8da57-116">EXAMPLES</span></span>

### <span data-ttu-id="8da57-117">範例 1：更新 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="8da57-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="8da57-118">第一個命令會從指定的資源群組myzone.com名為 myzone.com，然後將它儲存在$Zone變數中。</span><span class="sxs-lookup"><span data-stu-id="8da57-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="8da57-119">第二個命令會更新您$Zone。</span><span class="sxs-lookup"><span data-stu-id="8da57-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="8da57-120">最後一個命令會確定變更。</span><span class="sxs-lookup"><span data-stu-id="8da57-120">The final command commits the change.</span></span>

### <span data-ttu-id="8da57-121">範例 2：更新區域標記</span><span class="sxs-lookup"><span data-stu-id="8da57-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="8da57-122">此命令會更新名為 myzone.com 區域標記，而不需要先明確取得區域。</span><span class="sxs-lookup"><span data-stu-id="8da57-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="8da57-123">範例 3：指定私人區域識別碼以建立私人區域與虛擬網路的關聯</span><span class="sxs-lookup"><span data-stu-id="8da57-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="8da57-124">此命令會指定專用 DNS 區域myprivatezone.com與虛擬網路 myvnet 做為註冊網路關聯。</span><span class="sxs-lookup"><span data-stu-id="8da57-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="8da57-125">範例 4：指定網路物件，將私人區域與虛擬網路建立關聯。</span><span class="sxs-lookup"><span data-stu-id="8da57-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="8da57-126">此命令將專用 DNS 區域 myprivatezone.com 與虛擬網路 myvnet 建立關聯，將 $vnet 變數所代表的虛擬網路物件傳遞至 Set-AzDnsZone Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8da57-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzDnsZone cmdlet.</span></span>

## <span data-ttu-id="8da57-127">參數</span><span class="sxs-lookup"><span data-stu-id="8da57-127">PARAMETERS</span></span>

### <span data-ttu-id="8da57-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da57-128">-DefaultProfile</span></span>
<span data-ttu-id="8da57-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8da57-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8da57-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="8da57-130">-Name</span></span>
<span data-ttu-id="8da57-131">指定要更新的 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="8da57-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da57-132">-覆寫</span><span class="sxs-lookup"><span data-stu-id="8da57-132">-Overwrite</span></span>
<span data-ttu-id="8da57-133">使用 Zone 物件或管線 (以物件傳遞 DNS 區域時) ，自已取回本地 Dns Zone 物件之後，若已在 Azure DNS 中變更，則不會更新區域。</span><span class="sxs-lookup"><span data-stu-id="8da57-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="8da57-134">這可保護同時進行變更。</span><span class="sxs-lookup"><span data-stu-id="8da57-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="8da57-135">您可以使用覆寫參數隱藏此行為，無論同時變更，都會更新區域。</span><span class="sxs-lookup"><span data-stu-id="8da57-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da57-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8da57-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="8da57-137">在此 DNS 區域中註冊虛擬機器主機名稱記錄的虛擬網路清單，僅適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="8da57-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da57-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8da57-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="8da57-139">在此 DNS 區域中註冊虛擬機器主機名稱記錄的虛擬網路識別碼 清單，僅適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="8da57-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da57-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8da57-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="8da57-141">可解析此 DNS 區域中記錄的虛擬網路清單，僅適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="8da57-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da57-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8da57-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="8da57-143">可解析此 DNS 區域中記錄的虛擬網路識別碼 清單，僅適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="8da57-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da57-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da57-144">-ResourceGroupName</span></span>
<span data-ttu-id="8da57-145">指定包含要更新之區域的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8da57-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="8da57-146">您也必須指定 ZoneName 參數。</span><span class="sxs-lookup"><span data-stu-id="8da57-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="8da57-147">或者，您可以使用具有 Zone 參數或管線的 Dns Zone物件來指定區域。</span><span class="sxs-lookup"><span data-stu-id="8da57-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da57-148">-標記</span><span class="sxs-lookup"><span data-stu-id="8da57-148">-Tag</span></span>
<span data-ttu-id="8da57-149">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="8da57-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8da57-150">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="8da57-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da57-151">-區域</span><span class="sxs-lookup"><span data-stu-id="8da57-151">-Zone</span></span>
<span data-ttu-id="8da57-152">指定要更新的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="8da57-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="8da57-153">或者，您可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定區域。</span><span class="sxs-lookup"><span data-stu-id="8da57-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8da57-154">-確認</span><span class="sxs-lookup"><span data-stu-id="8da57-154">-Confirm</span></span>
<span data-ttu-id="8da57-155">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8da57-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8da57-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da57-156">-WhatIf</span></span>
<span data-ttu-id="8da57-157">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8da57-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8da57-158">不會執行 Cmdlet。顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8da57-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8da57-159">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8da57-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8da57-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da57-160">CommonParameters</span></span>
<span data-ttu-id="8da57-161">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8da57-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da57-162">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8da57-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da57-163">輸入</span><span class="sxs-lookup"><span data-stu-id="8da57-163">INPUTS</span></span>

### <span data-ttu-id="8da57-164">System.String</span><span class="sxs-lookup"><span data-stu-id="8da57-164">System.String</span></span>

### <span data-ttu-id="8da57-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8da57-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8da57-166">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8da57-166">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8da57-167">System.Collections.generic.List'1[[Microsoft.Azure.management.Internal.Network.Common.IResourceReference，Microsoft.Azure.PowerShell.Clients.Network， Version=1.0.0.0， Culture=neutral， PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8da57-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8da57-168">Microsoft.Azure.Commands.dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="8da57-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="8da57-169">輸出</span><span class="sxs-lookup"><span data-stu-id="8da57-169">OUTPUTS</span></span>

### <span data-ttu-id="8da57-170">Microsoft.Azure.Commands.dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="8da57-170">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="8da57-171">筆記</span><span class="sxs-lookup"><span data-stu-id="8da57-171">NOTES</span></span>
<span data-ttu-id="8da57-172">您可以使用 *確認參數來控制* 此 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8da57-172">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8da57-173">根據預設，如果 Windows PowerShell 變數的 $ConfirmPreference中或較低值，Cmdlet 會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8da57-173">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="8da57-174">如果您 *指定確認或* 確認 *：$True，* 此 Cmdlet 會先提示您確認再執行。</span><span class="sxs-lookup"><span data-stu-id="8da57-174">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="8da57-175">如果您指定 *確認：$False，Cmdlet* 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8da57-175">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8da57-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="8da57-176">RELATED LINKS</span></span>

[<span data-ttu-id="8da57-177">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8da57-177">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="8da57-178">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8da57-178">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="8da57-179">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8da57-179">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
