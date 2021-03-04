---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: b3ea1ab3bbe3edbc72b81c25817af40e9e5fc2a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903478"
---
# <span data-ttu-id="53ab4-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="53ab4-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="53ab4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="53ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="53ab4-103">建立公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="53ab4-103">Creates a public IP address.</span></span>

## <span data-ttu-id="53ab4-104">語法</span><span class="sxs-lookup"><span data-stu-id="53ab4-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53ab4-105">描述</span><span class="sxs-lookup"><span data-stu-id="53ab4-105">DESCRIPTION</span></span>
<span data-ttu-id="53ab4-106">**New-AzPublicIpAddress** Cmdlet 會建立公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="53ab4-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="53ab4-107">例子</span><span class="sxs-lookup"><span data-stu-id="53ab4-107">EXAMPLES</span></span>

### <span data-ttu-id="53ab4-108">範例 1：建立新公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="53ab4-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="53ab4-109">此命令會建立新的公用 IP 位址資源。針對指向此資源的公用 IP 位址的 $dnsPrefix.$location.cloudapp.azure.com 建立 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="53ab4-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="53ab4-110">公用 IP 位址會立即配置給此資源，因為 -AllocationMethod 被指定為 "Static"。</span><span class="sxs-lookup"><span data-stu-id="53ab4-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="53ab4-111">如果指定為 'Dynamic'，則公用 IP 位址只有在您啟動 (或建立) 關聯資源 (例如 VM 或負載平衡器) 時才能配置。</span><span class="sxs-lookup"><span data-stu-id="53ab4-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="53ab4-112">範例 2：使用反向 FQDN 建立公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="53ab4-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="53ab4-113">此命令會建立新的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="53ab4-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="53ab4-114">使用 -ReverseFqdn 參數，Azure 會針對配置給此資源的公用 IP 位址 (建立 DNS PTR 記錄) 反向查詢 $customFqdn，指向命令中指定的 $customFqdn。</span><span class="sxs-lookup"><span data-stu-id="53ab4-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="53ab4-115">先決條件是，假設 $customFqdn (應該webapp.contoso.com) DNS CNAME 記錄 (指向 $dnsPrefix.$location.cloudapp.azure.com) 的 DNS CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="53ab4-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="53ab4-116">範例 3：使用 IpTag 建立新公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="53ab4-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="53ab4-117">此命令會建立新的公用 IP 位址資源。針對指向此資源的公用 IP 位址的 $dnsPrefix.$location.cloudapp.azure.com 建立 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="53ab4-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="53ab4-118">公用 IP 位址會立即配置給此資源，因為 -AllocationMethod 被指定為 "Static"。</span><span class="sxs-lookup"><span data-stu-id="53ab4-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="53ab4-119">如果指定為 'Dynamic'，則公用 IP 位址只有在您啟動 (或建立) 關聯資源 (例如 VM 或負載平衡器) 時才能配置。</span><span class="sxs-lookup"><span data-stu-id="53ab4-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="53ab4-120">Iptag 會用於特定與資源相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="53ab4-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="53ab4-121">Iptag 可以使用 New-AzPublicIpTag 指定，並透過 -IpTags 以輸入方式傳遞。</span><span class="sxs-lookup"><span data-stu-id="53ab4-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="53ab4-122">範例 4：從首碼建立新公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="53ab4-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="53ab4-123">此命令會建立新的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="53ab4-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="53ab4-124">針對指向此資源的公用 IP 位址的 $dnsPrefix.$location.cloudapp.azure.com 建立 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="53ab4-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="53ab4-125">公用 IP 位址會立即從指定的 publicIpPrefix 配置給此資源。</span><span class="sxs-lookup"><span data-stu-id="53ab4-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="53ab4-126">此選項僅支援 'Standard' SKU 和 'Static' AllocationMethod。</span><span class="sxs-lookup"><span data-stu-id="53ab4-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

### <span data-ttu-id="53ab4-127">範例 5：建立新的全域公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="53ab4-127">Example 5: Create a new global public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

<span data-ttu-id="53ab4-128">此命令會建立一個新的全域公用 IP 位址資源。針對指向此資源的公用 IP 位址的 $dnsPrefix.$location.cloudapp.azure.com 建立 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="53ab4-128">This command creates a new global public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="53ab4-129">全域公用 IP 位址會立即配置給此資源。</span><span class="sxs-lookup"><span data-stu-id="53ab4-129">A global public IP address is immediately allocated to this resource.</span></span>
<span data-ttu-id="53ab4-130">此選項僅支援 'Standard' SKU 和 'Static' AllocationMethod。</span><span class="sxs-lookup"><span data-stu-id="53ab4-130">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="53ab4-131">參數</span><span class="sxs-lookup"><span data-stu-id="53ab4-131">PARAMETERS</span></span>

### <span data-ttu-id="53ab4-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="53ab4-132">-AllocationMethod</span></span>
<span data-ttu-id="53ab4-133">指定配置公用 IP 位址的方法。</span><span class="sxs-lookup"><span data-stu-id="53ab4-133">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="53ab4-134">此參數可接受的值為：靜態或動態。</span><span class="sxs-lookup"><span data-stu-id="53ab4-134">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="53ab4-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53ab4-135">-AsJob</span></span>
<span data-ttu-id="53ab4-136">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="53ab4-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53ab4-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53ab4-137">-DefaultProfile</span></span>
<span data-ttu-id="53ab4-138">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="53ab4-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53ab4-139">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="53ab4-139">-DomainNameLabel</span></span>
<span data-ttu-id="53ab4-140">指定公用 IP 位址的相對 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="53ab4-140">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="53ab4-141">-強制</span><span class="sxs-lookup"><span data-stu-id="53ab4-141">-Force</span></span>
<span data-ttu-id="53ab4-142">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="53ab4-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="53ab4-143">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="53ab4-143">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="53ab4-144">指定閒置時間 ，以分鐘表示。</span><span class="sxs-lookup"><span data-stu-id="53ab4-144">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="53ab4-145">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="53ab4-145">-IpAddressVersion</span></span>
<span data-ttu-id="53ab4-146">指定 IP 位址的版本。</span><span class="sxs-lookup"><span data-stu-id="53ab4-146">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="53ab4-147">-IpTag</span><span class="sxs-lookup"><span data-stu-id="53ab4-147">-IpTag</span></span>
<span data-ttu-id="53ab4-148">IpTag 清單。</span><span class="sxs-lookup"><span data-stu-id="53ab4-148">IpTag List.</span></span>

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

### <span data-ttu-id="53ab4-149">-位置</span><span class="sxs-lookup"><span data-stu-id="53ab4-149">-Location</span></span>
<span data-ttu-id="53ab4-150">指定要建立公用 IP 位址的區域。</span><span class="sxs-lookup"><span data-stu-id="53ab4-150">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="53ab4-151">-名稱</span><span class="sxs-lookup"><span data-stu-id="53ab4-151">-Name</span></span>
<span data-ttu-id="53ab4-152">指定此 Cmdlet 所建立之公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="53ab4-152">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="53ab4-153">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53ab4-153">-PublicIpPrefix</span></span>
<span data-ttu-id="53ab4-154">指定要配置公用 IP 位址的 PSPublicIpPrefix。</span><span class="sxs-lookup"><span data-stu-id="53ab4-154">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="53ab4-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53ab4-155">-ResourceGroupName</span></span>
<span data-ttu-id="53ab4-156">指定要建立公用 IP 位址的資源組名。</span><span class="sxs-lookup"><span data-stu-id="53ab4-156">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="53ab4-157">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="53ab4-157">-ReverseFqdn</span></span>
<span data-ttu-id="53ab4-158">指定 FQDN (完全) 。</span><span class="sxs-lookup"><span data-stu-id="53ab4-158">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="53ab4-159">-SKU</span><span class="sxs-lookup"><span data-stu-id="53ab4-159">-Sku</span></span>
<span data-ttu-id="53ab4-160">公用 IP SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="53ab4-160">The public IP Sku name.</span></span>

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

### <span data-ttu-id="53ab4-161">-標記</span><span class="sxs-lookup"><span data-stu-id="53ab4-161">-Tag</span></span>
<span data-ttu-id="53ab4-162">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="53ab4-162">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="53ab4-163">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="53ab4-163">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="53ab4-164">-Tier</span><span class="sxs-lookup"><span data-stu-id="53ab4-164">-Tier</span></span>
<span data-ttu-id="53ab4-165">公用 IP SKU 層。</span><span class="sxs-lookup"><span data-stu-id="53ab4-165">The public IP Sku Tier.</span></span>

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

### <span data-ttu-id="53ab4-166">-區域</span><span class="sxs-lookup"><span data-stu-id="53ab4-166">-Zone</span></span>
<span data-ttu-id="53ab4-167">表示資源需要配置之 IP 的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="53ab4-167">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="53ab4-168">-確認</span><span class="sxs-lookup"><span data-stu-id="53ab4-168">-Confirm</span></span>
<span data-ttu-id="53ab4-169">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="53ab4-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53ab4-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53ab4-170">-WhatIf</span></span>
<span data-ttu-id="53ab4-171">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53ab4-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53ab4-172">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53ab4-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53ab4-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ab4-173">CommonParameters</span></span>
<span data-ttu-id="53ab4-174">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="53ab4-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53ab4-175">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53ab4-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ab4-176">輸入</span><span class="sxs-lookup"><span data-stu-id="53ab4-176">INPUTS</span></span>

### <span data-ttu-id="53ab4-177">System.String</span><span class="sxs-lookup"><span data-stu-id="53ab4-177">System.String</span></span>

### <span data-ttu-id="53ab4-178">Microsoft.Azure.Commands.Network.models.PSPublicIpTag[]</span><span class="sxs-lookup"><span data-stu-id="53ab4-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="53ab4-179">Microsoft.Azure.Commands.Network.models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53ab4-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="53ab4-180">System.Int32</span><span class="sxs-lookup"><span data-stu-id="53ab4-180">System.Int32</span></span>

### <span data-ttu-id="53ab4-181">System.String[]</span><span class="sxs-lookup"><span data-stu-id="53ab4-181">System.String[]</span></span>

### <span data-ttu-id="53ab4-182">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="53ab4-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="53ab4-183">輸出</span><span class="sxs-lookup"><span data-stu-id="53ab4-183">OUTPUTS</span></span>

### <span data-ttu-id="53ab4-184">Microsoft.Azure.Commands.Network.models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="53ab4-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="53ab4-185">筆記</span><span class="sxs-lookup"><span data-stu-id="53ab4-185">NOTES</span></span>

## <span data-ttu-id="53ab4-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="53ab4-186">RELATED LINKS</span></span>

[<span data-ttu-id="53ab4-187">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="53ab4-187">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="53ab4-188">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="53ab4-188">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="53ab4-189">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="53ab4-189">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
