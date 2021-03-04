---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: c72c4ad67f6096f5ba86924219670be53a725d26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902397"
---
# <span data-ttu-id="4fe79-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4fe79-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="4fe79-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4fe79-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe79-103">建立公用 IP 首碼</span><span class="sxs-lookup"><span data-stu-id="4fe79-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="4fe79-104">語法</span><span class="sxs-lookup"><span data-stu-id="4fe79-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fe79-105">描述</span><span class="sxs-lookup"><span data-stu-id="4fe79-105">DESCRIPTION</span></span>
<span data-ttu-id="4fe79-106">**New-AzPublicIpPrefix** Cmdlet 會建立公用 IP 首碼。</span><span class="sxs-lookup"><span data-stu-id="4fe79-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="4fe79-107">例子</span><span class="sxs-lookup"><span data-stu-id="4fe79-107">EXAMPLES</span></span>

### <span data-ttu-id="4fe79-108">範例 1：建立新的公用 Ip 首碼</span><span class="sxs-lookup"><span data-stu-id="4fe79-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="4fe79-109">此命令會建立新的公用 IP 首碼資源。</span><span class="sxs-lookup"><span data-stu-id="4fe79-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="4fe79-110">範例 2：建立新的全域公用 Ip 首碼</span><span class="sxs-lookup"><span data-stu-id="4fe79-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="4fe79-111">此命令會建立一個新的全域公用 IP 首碼資源。</span><span class="sxs-lookup"><span data-stu-id="4fe79-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="4fe79-112">參數</span><span class="sxs-lookup"><span data-stu-id="4fe79-112">PARAMETERS</span></span>

### <span data-ttu-id="4fe79-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fe79-113">-AsJob</span></span>
<span data-ttu-id="4fe79-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4fe79-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4fe79-115">-CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4fe79-115">-CustomIpPrefix</span></span>
<span data-ttu-id="4fe79-116">此 PublicIpPrefix 將關聯的 CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4fe79-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe79-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe79-117">-DefaultProfile</span></span>
<span data-ttu-id="4fe79-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4fe79-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fe79-119">-強制</span><span class="sxs-lookup"><span data-stu-id="4fe79-119">-Force</span></span>
<span data-ttu-id="4fe79-120">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="4fe79-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4fe79-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="4fe79-121">-IpAddressVersion</span></span>
<span data-ttu-id="4fe79-122">公用 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="4fe79-122">The public IP address version.</span></span>

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

### <span data-ttu-id="4fe79-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="4fe79-123">-IpTag</span></span>
<span data-ttu-id="4fe79-124">IpTag 清單。</span><span class="sxs-lookup"><span data-stu-id="4fe79-124">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe79-125">-位置</span><span class="sxs-lookup"><span data-stu-id="4fe79-125">-Location</span></span>
<span data-ttu-id="4fe79-126">公用 IP 首碼位置。</span><span class="sxs-lookup"><span data-stu-id="4fe79-126">The public IP prefix location.</span></span>

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

### <span data-ttu-id="4fe79-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="4fe79-127">-Name</span></span>
<span data-ttu-id="4fe79-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4fe79-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe79-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="4fe79-129">-PrefixLength</span></span>
<span data-ttu-id="4fe79-130">PublicIPPrefix 長度</span><span class="sxs-lookup"><span data-stu-id="4fe79-130">The PublicIPPrefix length</span></span>

```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe79-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fe79-131">-ResourceGroupName</span></span>
<span data-ttu-id="4fe79-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4fe79-132">The resource group name.</span></span>

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

### <span data-ttu-id="4fe79-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="4fe79-133">-Sku</span></span>
<span data-ttu-id="4fe79-134">公用 IP 首碼 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="4fe79-134">The public IP Prefix Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe79-135">-標記</span><span class="sxs-lookup"><span data-stu-id="4fe79-135">-Tag</span></span>
<span data-ttu-id="4fe79-136">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4fe79-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4fe79-137">-Tier</span><span class="sxs-lookup"><span data-stu-id="4fe79-137">-Tier</span></span>
<span data-ttu-id="4fe79-138">公用 IP 首碼 SKU 層級。</span><span class="sxs-lookup"><span data-stu-id="4fe79-138">The public IP Prefix Sku tier.</span></span>

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

### <span data-ttu-id="4fe79-139">-區域</span><span class="sxs-lookup"><span data-stu-id="4fe79-139">-Zone</span></span>
<span data-ttu-id="4fe79-140">表示資源需要配置之 IP 的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="4fe79-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="4fe79-141">-確認</span><span class="sxs-lookup"><span data-stu-id="4fe79-141">-Confirm</span></span>
<span data-ttu-id="4fe79-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4fe79-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe79-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fe79-143">-WhatIf</span></span>
<span data-ttu-id="4fe79-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4fe79-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fe79-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4fe79-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe79-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe79-146">CommonParameters</span></span>
<span data-ttu-id="4fe79-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4fe79-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe79-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fe79-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe79-149">輸入</span><span class="sxs-lookup"><span data-stu-id="4fe79-149">INPUTS</span></span>

### <span data-ttu-id="4fe79-150">System.String</span><span class="sxs-lookup"><span data-stu-id="4fe79-150">System.String</span></span>

### <span data-ttu-id="4fe79-151">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="4fe79-151">System.UInt16</span></span>

### <span data-ttu-id="4fe79-152">Microsoft.Azure.Commands.Network.models.PSPublicIpPrefixTag[]</span><span class="sxs-lookup"><span data-stu-id="4fe79-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="4fe79-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4fe79-153">System.String[]</span></span>

### <span data-ttu-id="4fe79-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4fe79-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4fe79-155">輸出</span><span class="sxs-lookup"><span data-stu-id="4fe79-155">OUTPUTS</span></span>

### <span data-ttu-id="4fe79-156">Microsoft.Azure.Commands.Network.models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4fe79-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="4fe79-157">筆記</span><span class="sxs-lookup"><span data-stu-id="4fe79-157">NOTES</span></span>

## <span data-ttu-id="4fe79-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="4fe79-158">RELATED LINKS</span></span>

[<span data-ttu-id="4fe79-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4fe79-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="4fe79-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4fe79-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="4fe79-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4fe79-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
