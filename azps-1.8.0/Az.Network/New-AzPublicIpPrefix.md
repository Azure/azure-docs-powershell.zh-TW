---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 6ee4f046281a36f0d0da798f1954a29f8d98d9c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621733"
---
# <span data-ttu-id="b1f36-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b1f36-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="b1f36-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1f36-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f36-103">建立公用 IP 首碼</span><span class="sxs-lookup"><span data-stu-id="b1f36-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="b1f36-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1f36-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1f36-105">說明</span><span class="sxs-lookup"><span data-stu-id="b1f36-105">DESCRIPTION</span></span>
<span data-ttu-id="b1f36-106">**新的-AzPublicIpPrefix** Cmdlet 會建立公用 IP 首碼。</span><span class="sxs-lookup"><span data-stu-id="b1f36-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="b1f36-107">示例</span><span class="sxs-lookup"><span data-stu-id="b1f36-107">EXAMPLES</span></span>

### <span data-ttu-id="b1f36-108">1：建立新的公用 Ip 首碼</span><span class="sxs-lookup"><span data-stu-id="b1f36-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="b1f36-109">這個命令會建立新的公用 IP 首碼資源。</span><span class="sxs-lookup"><span data-stu-id="b1f36-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="b1f36-110">參數</span><span class="sxs-lookup"><span data-stu-id="b1f36-110">PARAMETERS</span></span>

### <span data-ttu-id="b1f36-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1f36-111">-AsJob</span></span>
<span data-ttu-id="b1f36-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b1f36-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1f36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f36-113">-DefaultProfile</span></span>
<span data-ttu-id="b1f36-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1f36-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1f36-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b1f36-115">-Force</span></span>
<span data-ttu-id="b1f36-116">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="b1f36-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="b1f36-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="b1f36-117">-IpAddressVersion</span></span>
<span data-ttu-id="b1f36-118">公用 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="b1f36-118">The public IP address version.</span></span>

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

### <span data-ttu-id="b1f36-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="b1f36-119">-IpTag</span></span>
<span data-ttu-id="b1f36-120">IpTag 清單]。</span><span class="sxs-lookup"><span data-stu-id="b1f36-120">IpTag List.</span></span>

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

### <span data-ttu-id="b1f36-121">-位置</span><span class="sxs-lookup"><span data-stu-id="b1f36-121">-Location</span></span>
<span data-ttu-id="b1f36-122">公用 IP 首碼位置。</span><span class="sxs-lookup"><span data-stu-id="b1f36-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="b1f36-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1f36-123">-Name</span></span>
<span data-ttu-id="b1f36-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b1f36-124">The resource name.</span></span>

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

### <span data-ttu-id="b1f36-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="b1f36-125">-PrefixLength</span></span>
<span data-ttu-id="b1f36-126">PublicIPPrefix 長度</span><span class="sxs-lookup"><span data-stu-id="b1f36-126">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="b1f36-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1f36-127">-ResourceGroupName</span></span>
<span data-ttu-id="b1f36-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1f36-128">The resource group name.</span></span>

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

### <span data-ttu-id="b1f36-129">-Sku</span><span class="sxs-lookup"><span data-stu-id="b1f36-129">-Sku</span></span>
<span data-ttu-id="b1f36-130">公用 IP 首碼 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="b1f36-130">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="b1f36-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="b1f36-131">-Tag</span></span>
<span data-ttu-id="b1f36-132">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="b1f36-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b1f36-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="b1f36-133">-Zone</span></span>
<span data-ttu-id="b1f36-134">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="b1f36-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="b1f36-135">-確認</span><span class="sxs-lookup"><span data-stu-id="b1f36-135">-Confirm</span></span>
<span data-ttu-id="b1f36-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1f36-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1f36-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1f36-137">-WhatIf</span></span>
<span data-ttu-id="b1f36-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1f36-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1f36-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1f36-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1f36-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f36-140">CommonParameters</span></span>
<span data-ttu-id="b1f36-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1f36-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f36-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b1f36-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f36-143">輸入</span><span class="sxs-lookup"><span data-stu-id="b1f36-143">INPUTS</span></span>

### <span data-ttu-id="b1f36-144">System.object</span><span class="sxs-lookup"><span data-stu-id="b1f36-144">System.String</span></span>

### <span data-ttu-id="b1f36-145">System.object</span><span class="sxs-lookup"><span data-stu-id="b1f36-145">System.UInt16</span></span>

### <span data-ttu-id="b1f36-146">PSPublicIpPrefixTag [] （[]）</span><span class="sxs-lookup"><span data-stu-id="b1f36-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="b1f36-147">System.object []</span><span class="sxs-lookup"><span data-stu-id="b1f36-147">System.String[]</span></span>

### <span data-ttu-id="b1f36-148">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b1f36-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b1f36-149">輸出</span><span class="sxs-lookup"><span data-stu-id="b1f36-149">OUTPUTS</span></span>

### <span data-ttu-id="b1f36-150">PSPublicIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b1f36-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="b1f36-151">筆記</span><span class="sxs-lookup"><span data-stu-id="b1f36-151">NOTES</span></span>

## <span data-ttu-id="b1f36-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1f36-152">RELATED LINKS</span></span>

[<span data-ttu-id="b1f36-153">AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b1f36-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="b1f36-154">移除-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b1f36-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="b1f36-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b1f36-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
