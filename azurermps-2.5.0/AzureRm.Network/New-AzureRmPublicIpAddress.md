---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: 032090bb494718a6420f54960106fe9c5fa9871c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801222"
---
# <span data-ttu-id="bde52-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bde52-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="bde52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bde52-102">SYNOPSIS</span></span>
<span data-ttu-id="bde52-103">建立公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bde52-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bde52-104">句法</span><span class="sxs-lookup"><span data-stu-id="bde52-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bde52-105">說明</span><span class="sxs-lookup"><span data-stu-id="bde52-105">DESCRIPTION</span></span>
<span data-ttu-id="bde52-106">**新的-AzureRmPublicIpAddress** Cmdlet 會建立公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bde52-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="bde52-107">示例</span><span class="sxs-lookup"><span data-stu-id="bde52-107">EXAMPLES</span></span>

### <span data-ttu-id="bde52-108">1：建立新的公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="bde52-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="bde52-109">這個命令會建立新的公用 IP 位址資源。此時會建立 DNS 記錄，$location $dnsPrefix 指向此資源的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bde52-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="bde52-110">公用 IP 位址會立即分配給此資源，因為-AllocationMethod 被指定為「Static」。</span><span class="sxs-lookup"><span data-stu-id="bde52-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="bde52-111">如果將其指定為「動態」，則只有當您開始 (或建立) 相關聯的資源 (例如 VM 或負載平衡器) 時，才會指派公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bde52-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="bde52-112">2：使用反向 FQDN 建立公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="bde52-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="bde52-113">這個命令會建立新的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="bde52-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="bde52-114">在 ReverseFqdn 參數中，Azure 會為指派給此資源的公用 IP 位址 (反向查閱) 建立 DNS PTR 記錄，並指向命令中指定的 $customFqdn。</span><span class="sxs-lookup"><span data-stu-id="bde52-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="bde52-115">就像預先必備，$customFqdn (說 webapp.contoso.com) 應該有 DNS CNAME 記錄 (轉寄查詢) 指向 $dnsPrefix。 $location. cloudapp.azure.com。</span><span class="sxs-lookup"><span data-stu-id="bde52-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="bde52-116">參數</span><span class="sxs-lookup"><span data-stu-id="bde52-116">PARAMETERS</span></span>

### <span data-ttu-id="bde52-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="bde52-117">-AllocationMethod</span></span>
<span data-ttu-id="bde52-118">指定要用來指派公用 IP 位址的方法。</span><span class="sxs-lookup"><span data-stu-id="bde52-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="bde52-119">此參數可接受的值為： Static 或 Dynamic。</span><span class="sxs-lookup"><span data-stu-id="bde52-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bde52-120">-AsJob</span></span>
<span data-ttu-id="bde52-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bde52-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bde52-122">-DefaultProfile</span></span>
<span data-ttu-id="bde52-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bde52-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-124">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="bde52-124">-DomainNameLabel</span></span>
<span data-ttu-id="bde52-125">指定公用 IP 位址的相對 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="bde52-125">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="bde52-126">-Force</span><span class="sxs-lookup"><span data-stu-id="bde52-126">-Force</span></span>
<span data-ttu-id="bde52-127">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="bde52-127">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="bde52-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="bde52-129">指定空閒超時（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="bde52-129">Specifies the idle time-out, in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-130">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="bde52-130">-IpAddressVersion</span></span>
<span data-ttu-id="bde52-131">指定 IP 位址的版本。</span><span class="sxs-lookup"><span data-stu-id="bde52-131">Specifies the version of the IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-132">-位置</span><span class="sxs-lookup"><span data-stu-id="bde52-132">-Location</span></span>
<span data-ttu-id="bde52-133">指定建立公用 IP 位址的區域。</span><span class="sxs-lookup"><span data-stu-id="bde52-133">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="bde52-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="bde52-134">-Name</span></span>
<span data-ttu-id="bde52-135">指定此 Cmdlet 所建立之公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="bde52-135">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bde52-136">-ResourceGroupName</span></span>
<span data-ttu-id="bde52-137">指定要在其中建立公用 IP 位址的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bde52-137">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="bde52-138">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="bde52-138">-ReverseFqdn</span></span>
<span data-ttu-id="bde52-139">指定 (FQDN) 的反向完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="bde52-139">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="bde52-140">-Sku</span><span class="sxs-lookup"><span data-stu-id="bde52-140">-Sku</span></span>
<span data-ttu-id="bde52-141">公用 IP Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="bde52-141">The public IP Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="bde52-142">-Tag</span></span>
<span data-ttu-id="bde52-143">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="bde52-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bde52-144">例如：</span><span class="sxs-lookup"><span data-stu-id="bde52-144">For example:</span></span>

<span data-ttu-id="bde52-145">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="bde52-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="bde52-146">-Zone</span></span>
<span data-ttu-id="bde52-147">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="bde52-147">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="bde52-148">-確認</span><span class="sxs-lookup"><span data-stu-id="bde52-148">-Confirm</span></span>
<span data-ttu-id="bde52-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bde52-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bde52-150">-WhatIf</span></span>
<span data-ttu-id="bde52-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bde52-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bde52-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bde52-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde52-153">CommonParameters</span></span>
<span data-ttu-id="bde52-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bde52-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde52-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bde52-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde52-156">輸入</span><span class="sxs-lookup"><span data-stu-id="bde52-156">INPUTS</span></span>

## <span data-ttu-id="bde52-157">輸出</span><span class="sxs-lookup"><span data-stu-id="bde52-157">OUTPUTS</span></span>

### <span data-ttu-id="bde52-158">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bde52-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="bde52-159">筆記</span><span class="sxs-lookup"><span data-stu-id="bde52-159">NOTES</span></span>

## <span data-ttu-id="bde52-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="bde52-160">RELATED LINKS</span></span>

[<span data-ttu-id="bde52-161">AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bde52-161">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="bde52-162">移除-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bde52-162">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="bde52-163">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bde52-163">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)