---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 8437c6037b52fd274415a59bea6ee66a2f9c0588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448143"
---
# <span data-ttu-id="2c99b-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2c99b-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="2c99b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c99b-102">SYNOPSIS</span></span>
<span data-ttu-id="2c99b-103">建立公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2c99b-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c99b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c99b-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c99b-105">說明</span><span class="sxs-lookup"><span data-stu-id="2c99b-105">DESCRIPTION</span></span>
<span data-ttu-id="2c99b-106">**新的-AzureRmPublicIpAddress** Cmdlet 會建立公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2c99b-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="2c99b-107">示例</span><span class="sxs-lookup"><span data-stu-id="2c99b-107">EXAMPLES</span></span>

### <span data-ttu-id="2c99b-108">1：建立新的公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="2c99b-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="2c99b-109">這個命令會建立新的公用 IP 位址資源。此時會建立 DNS 記錄，$location $dnsPrefix 指向此資源的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2c99b-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="2c99b-110">公用 IP 位址會立即分配給此資源，因為-AllocationMethod 被指定為「Static」。</span><span class="sxs-lookup"><span data-stu-id="2c99b-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="2c99b-111">如果將其指定為「動態」，則只有當您開始 (或建立) 相關聯的資源 (例如 VM 或負載平衡器) 時，才會指派公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2c99b-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="2c99b-112">2：使用反向 FQDN 建立公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="2c99b-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="2c99b-113">這個命令會建立新的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="2c99b-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="2c99b-114">在 ReverseFqdn 參數中，Azure 會為指派給此資源的公用 IP 位址 (反向查閱) 建立 DNS PTR 記錄，並指向命令中指定的 $customFqdn。</span><span class="sxs-lookup"><span data-stu-id="2c99b-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="2c99b-115">就像預先必備，$customFqdn (說 webapp.contoso.com) 應該有 DNS CNAME 記錄 (轉寄查詢) 指向 $dnsPrefix。 $location. cloudapp.azure.com。</span><span class="sxs-lookup"><span data-stu-id="2c99b-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="2c99b-116">參數</span><span class="sxs-lookup"><span data-stu-id="2c99b-116">PARAMETERS</span></span>

### <span data-ttu-id="2c99b-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="2c99b-117">-AllocationMethod</span></span>
<span data-ttu-id="2c99b-118">指定要用來指派公用 IP 位址的方法。</span><span class="sxs-lookup"><span data-stu-id="2c99b-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="2c99b-119">此參數可接受的值為： Static 或 Dynamic。</span><span class="sxs-lookup"><span data-stu-id="2c99b-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="2c99b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c99b-120">-DefaultProfile</span></span>
<span data-ttu-id="2c99b-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c99b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c99b-122">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="2c99b-122">-DomainNameLabel</span></span>
<span data-ttu-id="2c99b-123">指定公用 IP 位址的相對 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="2c99b-123">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="2c99b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2c99b-124">-Force</span></span>
<span data-ttu-id="2c99b-125">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2c99b-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c99b-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2c99b-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="2c99b-127">指定空閒超時（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="2c99b-127">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="2c99b-128">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="2c99b-128">-IpAddressVersion</span></span>
<span data-ttu-id="2c99b-129">指定 IP 位址的版本。</span><span class="sxs-lookup"><span data-stu-id="2c99b-129">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="2c99b-130">-位置</span><span class="sxs-lookup"><span data-stu-id="2c99b-130">-Location</span></span>
<span data-ttu-id="2c99b-131">指定建立公用 IP 位址的區域。</span><span class="sxs-lookup"><span data-stu-id="2c99b-131">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="2c99b-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c99b-132">-Name</span></span>
<span data-ttu-id="2c99b-133">指定此 Cmdlet 所建立之公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c99b-133">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2c99b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c99b-134">-ResourceGroupName</span></span>
<span data-ttu-id="2c99b-135">指定要在其中建立公用 IP 位址的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c99b-135">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="2c99b-136">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="2c99b-136">-ReverseFqdn</span></span>
<span data-ttu-id="2c99b-137">指定 (FQDN) 的反向完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="2c99b-137">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="2c99b-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="2c99b-138">-Sku</span></span>
<span data-ttu-id="2c99b-139">公用 IP Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="2c99b-139">The public IP Sku name.</span></span>

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

### <span data-ttu-id="2c99b-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="2c99b-140">-Tag</span></span>
<span data-ttu-id="2c99b-141">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="2c99b-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2c99b-142">例如：</span><span class="sxs-lookup"><span data-stu-id="2c99b-142">For example:</span></span>

<span data-ttu-id="2c99b-143">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2c99b-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2c99b-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="2c99b-144">-Zone</span></span>
<span data-ttu-id="2c99b-145">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="2c99b-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="2c99b-146">-確認</span><span class="sxs-lookup"><span data-stu-id="2c99b-146">-Confirm</span></span>
<span data-ttu-id="2c99b-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2c99b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c99b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c99b-148">-WhatIf</span></span>
<span data-ttu-id="2c99b-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c99b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c99b-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c99b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c99b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c99b-151">CommonParameters</span></span>
<span data-ttu-id="2c99b-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c99b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c99b-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2c99b-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c99b-154">輸入</span><span class="sxs-lookup"><span data-stu-id="2c99b-154">INPUTS</span></span>

## <span data-ttu-id="2c99b-155">輸出</span><span class="sxs-lookup"><span data-stu-id="2c99b-155">OUTPUTS</span></span>

### <span data-ttu-id="2c99b-156">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2c99b-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="2c99b-157">筆記</span><span class="sxs-lookup"><span data-stu-id="2c99b-157">NOTES</span></span>

## <span data-ttu-id="2c99b-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c99b-158">RELATED LINKS</span></span>

[<span data-ttu-id="2c99b-159">AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2c99b-159">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="2c99b-160">移除-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2c99b-160">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="2c99b-161">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2c99b-161">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
