---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: 67997145a327d7f9e47f4cf346cbfd5e3a6bf0f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624389"
---
# <span data-ttu-id="782d5-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="782d5-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="782d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="782d5-102">SYNOPSIS</span></span>
<span data-ttu-id="782d5-103">更新 DNS 區域的屬性。</span><span class="sxs-lookup"><span data-stu-id="782d5-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="782d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="782d5-104">SYNTAX</span></span>

### <span data-ttu-id="782d5-105">預設)  (的欄位</span><span class="sxs-lookup"><span data-stu-id="782d5-105">Fields (Default)</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="782d5-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="782d5-106">FieldsObjects</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="782d5-107">面向</span><span class="sxs-lookup"><span data-stu-id="782d5-107">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="782d5-108">說明</span><span class="sxs-lookup"><span data-stu-id="782d5-108">DESCRIPTION</span></span>
<span data-ttu-id="782d5-109">**AzureRmDnsZone** Cmdlet 會更新 Azure DNS 服務中指定的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="782d5-109">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="782d5-110">這個 Cmdlet 不會更新區域中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="782d5-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="782d5-111">您可以將 **DnsZone** 物件傳遞為參數或使用管線運算子，或者也可以指定 *ZoneName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="782d5-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="782d5-112">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="782d5-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="782d5-113">當您使用 Zone 物件或透過) 管線將 DNS 區域傳輸成物件 (，如果在已檢索到本機 DnsZone 物件之後，在 Azure DNS 中已變更，則不會更新它。</span><span class="sxs-lookup"><span data-stu-id="782d5-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="782d5-114">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="782d5-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="782d5-115">您可以使用 *Overwrite* 參數來抑制此行為，不論併發變更為何，都會更新區域。</span><span class="sxs-lookup"><span data-stu-id="782d5-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="782d5-116">示例</span><span class="sxs-lookup"><span data-stu-id="782d5-116">EXAMPLES</span></span>

### <span data-ttu-id="782d5-117">範例1：更新 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="782d5-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="782d5-118">第一個命令會從指定的資源群組中取得名為 myzone.com 的區域，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="782d5-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="782d5-119">第二個命令會更新 $Zone 的標記。</span><span class="sxs-lookup"><span data-stu-id="782d5-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="782d5-120">最後一個命令會提交變更。</span><span class="sxs-lookup"><span data-stu-id="782d5-120">The final command commits the change.</span></span>

### <span data-ttu-id="782d5-121">範例2：更新區域的標記</span><span class="sxs-lookup"><span data-stu-id="782d5-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="782d5-122">這個命令會更新名為 myzone.com 區域的標籤，而不需要先明確取得該區域。</span><span class="sxs-lookup"><span data-stu-id="782d5-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="782d5-123">範例3：指定其識別碼以將私人區域與虛擬網路建立關聯</span><span class="sxs-lookup"><span data-stu-id="782d5-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="782d5-124">這個命令會透過指定其識別碼，將私人 DNS 區域 myprivatezone.com 與虛擬網路 myvnet 相關聯。</span><span class="sxs-lookup"><span data-stu-id="782d5-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="782d5-125">範例4：透過指定 network 物件，將私人區域與虛擬網路建立關聯。</span><span class="sxs-lookup"><span data-stu-id="782d5-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="782d5-126">這個命令會將私人 DNS 區域 myprivatezone.com 與虛擬網路 myvnet，傳送成註冊網路，方法是將 $vnet 變數所代表的虛擬網路物件傳遞給 Set-AzureRmDnsZone Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="782d5-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzureRmDnsZone cmdlet.</span></span>

## <span data-ttu-id="782d5-127">參數</span><span class="sxs-lookup"><span data-stu-id="782d5-127">PARAMETERS</span></span>

### <span data-ttu-id="782d5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="782d5-128">-DefaultProfile</span></span>
<span data-ttu-id="782d5-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="782d5-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="782d5-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="782d5-130">-Name</span></span>
<span data-ttu-id="782d5-131">指定要更新之 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="782d5-131">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="782d5-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="782d5-132">-Overwrite</span></span>
<span data-ttu-id="782d5-133">當您使用 Zone 物件或透過) 管線將 DNS 區域傳輸成物件 (，如果在已檢索到本機 DnsZone 物件之後，在 Azure DNS 中已變更，則不會更新它。</span><span class="sxs-lookup"><span data-stu-id="782d5-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="782d5-134">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="782d5-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="782d5-135">您可以使用 *Overwrite* 參數來抑制此行為，不論併發變更為何，都會更新區域。</span><span class="sxs-lookup"><span data-stu-id="782d5-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="782d5-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="782d5-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="782d5-137">將在這個 DNS 區域中註冊虛擬機器主機名稱記錄的虛擬網路清單，只適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="782d5-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="782d5-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="782d5-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="782d5-139">將在這個 DNS 區域中登錄虛擬機器主機名稱記錄的虛擬網路 Id 清單，只適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="782d5-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="782d5-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="782d5-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="782d5-141">可解析此 DNS 區域中之記錄的虛擬網路清單，只能供私人區域使用。</span><span class="sxs-lookup"><span data-stu-id="782d5-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="782d5-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="782d5-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="782d5-143">可解析此 DNS 區域中之記錄的虛擬網路 Id 清單，只適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="782d5-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="782d5-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="782d5-144">-ResourceGroupName</span></span>
<span data-ttu-id="782d5-145">指定包含要更新之區域之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="782d5-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="782d5-146">您也必須指定 ZoneName 參數。</span><span class="sxs-lookup"><span data-stu-id="782d5-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="782d5-147">或者，您也可以使用 DnsZone 物件與 *zone* 參數或管線來指定區域。</span><span class="sxs-lookup"><span data-stu-id="782d5-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="782d5-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="782d5-148">-Tag</span></span>
<span data-ttu-id="782d5-149">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="782d5-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="782d5-150">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="782d5-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="782d5-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="782d5-151">-Zone</span></span>
<span data-ttu-id="782d5-152">指定要更新的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="782d5-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="782d5-153">或者，您也可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定區域。</span><span class="sxs-lookup"><span data-stu-id="782d5-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="782d5-154">-確認</span><span class="sxs-lookup"><span data-stu-id="782d5-154">-Confirm</span></span>
<span data-ttu-id="782d5-155">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="782d5-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="782d5-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="782d5-156">-WhatIf</span></span>
<span data-ttu-id="782d5-157">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="782d5-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="782d5-158">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="782d5-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="782d5-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="782d5-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="782d5-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="782d5-160">CommonParameters</span></span>
<span data-ttu-id="782d5-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="782d5-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="782d5-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="782d5-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="782d5-163">輸入</span><span class="sxs-lookup"><span data-stu-id="782d5-163">INPUTS</span></span>

### <span data-ttu-id="782d5-164">System.object</span><span class="sxs-lookup"><span data-stu-id="782d5-164">System.String</span></span>

### <span data-ttu-id="782d5-165">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="782d5-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="782d5-166">[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="782d5-166">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="782d5-167">[System.object]. 清單 ' 1 [IResourceReference]。 common. Network、Version = 1.0.0.0、Culture = 中性、PublicKeyToken = null]]。）），）的區域性 = 非特定語言。</span><span class="sxs-lookup"><span data-stu-id="782d5-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.Commands.Common.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="782d5-168">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="782d5-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="782d5-169">參數： Zone (ByValue) </span><span class="sxs-lookup"><span data-stu-id="782d5-169">Parameters: Zone (ByValue)</span></span>

## <span data-ttu-id="782d5-170">輸出</span><span class="sxs-lookup"><span data-stu-id="782d5-170">OUTPUTS</span></span>

### <span data-ttu-id="782d5-171">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="782d5-171">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="782d5-172">筆記</span><span class="sxs-lookup"><span data-stu-id="782d5-172">NOTES</span></span>
<span data-ttu-id="782d5-173">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="782d5-173">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="782d5-174">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="782d5-174">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="782d5-175">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="782d5-175">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="782d5-176">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="782d5-176">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="782d5-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="782d5-177">RELATED LINKS</span></span>

[<span data-ttu-id="782d5-178">AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="782d5-178">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="782d5-179">新-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="782d5-179">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="782d5-180">移除-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="782d5-180">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
