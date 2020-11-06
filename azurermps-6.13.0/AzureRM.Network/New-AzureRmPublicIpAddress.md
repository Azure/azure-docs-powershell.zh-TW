---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 7ef0d3ce20868c4240abc43278cdc38a33efa5b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456968"
---
# <span data-ttu-id="751fa-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="751fa-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="751fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="751fa-102">SYNOPSIS</span></span>
<span data-ttu-id="751fa-103">建立公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="751fa-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="751fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="751fa-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]>]
 [-PublicIpPrefix <Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix>]
 [-ReverseFqdn <String>] [-IdleTimeoutInMinutes <Int32>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="751fa-105">說明</span><span class="sxs-lookup"><span data-stu-id="751fa-105">DESCRIPTION</span></span>
<span data-ttu-id="751fa-106">**新的-AzureRmPublicIpAddress** Cmdlet 會建立公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="751fa-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="751fa-107">示例</span><span class="sxs-lookup"><span data-stu-id="751fa-107">EXAMPLES</span></span>

### <span data-ttu-id="751fa-108">1：建立新的公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="751fa-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="751fa-109">這個命令會建立新的公用 IP 位址資源。此時會建立 DNS 記錄，$location $dnsPrefix 指向此資源的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="751fa-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="751fa-110">公用 IP 位址會立即分配給此資源，因為-AllocationMethod 被指定為「Static」。</span><span class="sxs-lookup"><span data-stu-id="751fa-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="751fa-111">如果將其指定為「動態」，則只有當您開始 (或建立) 相關聯的資源 (例如 VM 或負載平衡器) 時，才會指派公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="751fa-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="751fa-112">2：使用反向 FQDN 建立公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="751fa-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="751fa-113">這個命令會建立新的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="751fa-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="751fa-114">在 ReverseFqdn 參數中，Azure 會為指派給此資源的公用 IP 位址 (反向查閱) 建立 DNS PTR 記錄，並指向命令中指定的 $customFqdn。</span><span class="sxs-lookup"><span data-stu-id="751fa-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="751fa-115">就像預先必備，$customFqdn (說 webapp.contoso.com) 應該有 DNS CNAME 記錄 (轉寄查詢) 指向 $dnsPrefix。 $location. cloudapp.azure.com。</span><span class="sxs-lookup"><span data-stu-id="751fa-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="751fa-116">3：使用 IpTag 建立新的公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="751fa-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="751fa-117">這個命令會建立新的公用 IP 位址資源。此時會建立 DNS 記錄，$location $dnsPrefix 指向此資源的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="751fa-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="751fa-118">公用 IP 位址會立即分配給此資源，因為-AllocationMethod 被指定為「Static」。</span><span class="sxs-lookup"><span data-stu-id="751fa-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="751fa-119">如果將其指定為「動態」，則只有當您開始 (或建立) 相關聯的資源 (例如 VM 或負載平衡器) 時，才會指派公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="751fa-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="751fa-120">Iptag 是用來指定與資源相關的標籤。</span><span class="sxs-lookup"><span data-stu-id="751fa-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="751fa-121">Iptag 可以使用 New-AzureRmPublicIpTag 來指定，並透過 IpTags 傳送為輸入。</span><span class="sxs-lookup"><span data-stu-id="751fa-121">Iptag can be specified using New-AzureRmPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="751fa-122">4：從首碼建立新的公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="751fa-122">4: Create a new public IP address from a Prefix</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="751fa-123">這個命令會建立新的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="751fa-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="751fa-124">此時會建立 DNS 記錄，$location $dnsPrefix 指向此資源的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="751fa-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="751fa-125">從指定的 publicIpPrefix，會立即將公用 IP 位址指派給此資源。</span><span class="sxs-lookup"><span data-stu-id="751fa-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="751fa-126">此選項僅支援「標準」 Sku 和「靜態」 AllocationMethod。</span><span class="sxs-lookup"><span data-stu-id="751fa-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="751fa-127">參數</span><span class="sxs-lookup"><span data-stu-id="751fa-127">PARAMETERS</span></span>

### <span data-ttu-id="751fa-128">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="751fa-128">-AllocationMethod</span></span>
<span data-ttu-id="751fa-129">指定要用來指派公用 IP 位址的方法。</span><span class="sxs-lookup"><span data-stu-id="751fa-129">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="751fa-130">此參數可接受的值為： Static 或 Dynamic。</span><span class="sxs-lookup"><span data-stu-id="751fa-130">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="751fa-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="751fa-131">-AsJob</span></span>
<span data-ttu-id="751fa-132">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="751fa-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="751fa-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="751fa-133">-DefaultProfile</span></span>
<span data-ttu-id="751fa-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="751fa-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="751fa-135">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="751fa-135">-DomainNameLabel</span></span>
<span data-ttu-id="751fa-136">指定公用 IP 位址的相對 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="751fa-136">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="751fa-137">-Force</span><span class="sxs-lookup"><span data-stu-id="751fa-137">-Force</span></span>
<span data-ttu-id="751fa-138">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="751fa-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="751fa-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="751fa-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="751fa-140">指定空閒超時（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="751fa-140">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="751fa-141">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="751fa-141">-IpAddressVersion</span></span>
<span data-ttu-id="751fa-142">指定 IP 位址的版本。</span><span class="sxs-lookup"><span data-stu-id="751fa-142">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="751fa-143">-IpTag</span><span class="sxs-lookup"><span data-stu-id="751fa-143">-IpTag</span></span>
<span data-ttu-id="751fa-144">IpTag 清單]。</span><span class="sxs-lookup"><span data-stu-id="751fa-144">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="751fa-145">-位置</span><span class="sxs-lookup"><span data-stu-id="751fa-145">-Location</span></span>
<span data-ttu-id="751fa-146">指定建立公用 IP 位址的區域。</span><span class="sxs-lookup"><span data-stu-id="751fa-146">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="751fa-147">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="751fa-147">-PublicIpPrefix</span></span>
<span data-ttu-id="751fa-148">指定要從哪個 PSPublicIpPrefix 指派公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="751fa-148">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="751fa-149">-名稱</span><span class="sxs-lookup"><span data-stu-id="751fa-149">-Name</span></span>
<span data-ttu-id="751fa-150">指定此 Cmdlet 所建立之公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="751fa-150">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="751fa-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="751fa-151">-ResourceGroupName</span></span>
<span data-ttu-id="751fa-152">指定要在其中建立公用 IP 位址的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="751fa-152">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="751fa-153">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="751fa-153">-ReverseFqdn</span></span>
<span data-ttu-id="751fa-154">指定 (FQDN) 的反向完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="751fa-154">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="751fa-155">-Sku</span><span class="sxs-lookup"><span data-stu-id="751fa-155">-Sku</span></span>
<span data-ttu-id="751fa-156">公用 IP Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="751fa-156">The public IP Sku name.</span></span>

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

### <span data-ttu-id="751fa-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="751fa-157">-Tag</span></span>
<span data-ttu-id="751fa-158">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="751fa-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="751fa-159">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="751fa-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="751fa-160">-Zone</span><span class="sxs-lookup"><span data-stu-id="751fa-160">-Zone</span></span>
<span data-ttu-id="751fa-161">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="751fa-161">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="751fa-162">-確認</span><span class="sxs-lookup"><span data-stu-id="751fa-162">-Confirm</span></span>
<span data-ttu-id="751fa-163">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="751fa-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="751fa-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="751fa-164">-WhatIf</span></span>
<span data-ttu-id="751fa-165">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="751fa-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="751fa-166">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="751fa-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="751fa-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="751fa-167">CommonParameters</span></span>
<span data-ttu-id="751fa-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="751fa-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="751fa-169">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="751fa-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="751fa-170">輸入</span><span class="sxs-lookup"><span data-stu-id="751fa-170">INPUTS</span></span>

### <span data-ttu-id="751fa-171">System.object</span><span class="sxs-lookup"><span data-stu-id="751fa-171">System.String</span></span>

### <span data-ttu-id="751fa-172">[System.object]. 清單 ' 1 [PSPublicIpTag，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="751fa-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="751fa-173">System.object</span><span class="sxs-lookup"><span data-stu-id="751fa-173">System.Int32</span></span>

### <span data-ttu-id="751fa-174">[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="751fa-174">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="751fa-175">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="751fa-175">System.Collections.Hashtable</span></span>

## <span data-ttu-id="751fa-176">輸出</span><span class="sxs-lookup"><span data-stu-id="751fa-176">OUTPUTS</span></span>

### <span data-ttu-id="751fa-177">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="751fa-177">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="751fa-178">筆記</span><span class="sxs-lookup"><span data-stu-id="751fa-178">NOTES</span></span>

## <span data-ttu-id="751fa-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="751fa-179">RELATED LINKS</span></span>

[<span data-ttu-id="751fa-180">AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="751fa-180">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="751fa-181">移除-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="751fa-181">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="751fa-182">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="751fa-182">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
