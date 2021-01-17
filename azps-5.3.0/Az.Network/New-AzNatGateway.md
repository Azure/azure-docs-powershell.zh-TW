---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 0855ba4e7e16503045d13c370838cd5d3fffb033
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438848"
---
# <span data-ttu-id="c0b85-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c0b85-101">New-AzNatGateway</span></span>

## <span data-ttu-id="c0b85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0b85-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b85-103">使用屬性公用 Ip 位址/公用 Ip 首碼、IdleTimeoutInMinutes 和 Sku 建立新的 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="c0b85-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="c0b85-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0b85-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0b85-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0b85-105">DESCRIPTION</span></span>
<span data-ttu-id="c0b85-106">**新的-AzNatGateway** Cmdlet 會建立 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="c0b85-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="c0b85-107">Natgateway 需要下列各項：</span><span class="sxs-lookup"><span data-stu-id="c0b85-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="c0b85-108">公用 Ip 位址和/或公用 Ip 首碼</span><span class="sxs-lookup"><span data-stu-id="c0b85-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="c0b85-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c0b85-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="c0b85-110">Sku</span><span class="sxs-lookup"><span data-stu-id="c0b85-110">Sku</span></span>
- <span data-ttu-id="c0b85-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0b85-111">ResourceGroupName</span></span>
- <span data-ttu-id="c0b85-112">CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="c0b85-112">ResourceName</span></span>
- <span data-ttu-id="c0b85-113">位於</span><span class="sxs-lookup"><span data-stu-id="c0b85-113">Location</span></span>

## <span data-ttu-id="c0b85-114">示例</span><span class="sxs-lookup"><span data-stu-id="c0b85-114">EXAMPLES</span></span>

### <span data-ttu-id="c0b85-115">範例1：建立含公用 Ip 位址的 Nat 閘道</span><span class="sxs-lookup"><span data-stu-id="c0b85-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="c0b85-116">範例2：建立含公用 Ip 首碼的 Nat 閘道</span><span class="sxs-lookup"><span data-stu-id="c0b85-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="c0b85-117">範例3：在可用性區域1中建立含公用 IP 位址的 Nat 閘道</span><span class="sxs-lookup"><span data-stu-id="c0b85-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="c0b85-118">第一個命令會建立標準的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c0b85-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="c0b85-119">第二個命令會在可用性區域1中建立含公用 IP 位址的 NAT 閘道。</span><span class="sxs-lookup"><span data-stu-id="c0b85-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="c0b85-120">參數</span><span class="sxs-lookup"><span data-stu-id="c0b85-120">PARAMETERS</span></span>

### <span data-ttu-id="c0b85-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0b85-121">-AsJob</span></span>
<span data-ttu-id="c0b85-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c0b85-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0b85-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b85-123">-DefaultProfile</span></span>
<span data-ttu-id="c0b85-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0b85-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0b85-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c0b85-125">-Force</span></span>
<span data-ttu-id="c0b85-126">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="c0b85-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c0b85-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c0b85-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c0b85-128">Nat 閘道的空閒超時。</span><span class="sxs-lookup"><span data-stu-id="c0b85-128">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b85-129">-位置</span><span class="sxs-lookup"><span data-stu-id="c0b85-129">-Location</span></span>
<span data-ttu-id="c0b85-130">位置。</span><span class="sxs-lookup"><span data-stu-id="c0b85-130">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b85-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0b85-131">-Name</span></span>
<span data-ttu-id="c0b85-132">Nat 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0b85-132">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b85-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c0b85-133">-PublicIpAddress</span></span>
<span data-ttu-id="c0b85-134">與 nat 閘道資源相關聯之公用 ip 位址的陣列。</span><span class="sxs-lookup"><span data-stu-id="c0b85-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b85-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c0b85-135">-PublicIpPrefix</span></span>
<span data-ttu-id="c0b85-136">與 nat 閘道資源相關聯之公用 ip 首碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="c0b85-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b85-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0b85-137">-ResourceGroupName</span></span>
<span data-ttu-id="c0b85-138">Nat 閘道的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c0b85-138">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b85-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="c0b85-139">-Sku</span></span>
<span data-ttu-id="c0b85-140">NAT 閘道 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0b85-140">Name of a NAT gateway SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b85-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="c0b85-141">-Tag</span></span>
<span data-ttu-id="c0b85-142">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="c0b85-142">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b85-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="c0b85-143">-Zone</span></span>
<span data-ttu-id="c0b85-144">表示應在其中部署 Nat 閘道之區域的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="c0b85-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b85-145">-確認</span><span class="sxs-lookup"><span data-stu-id="c0b85-145">-Confirm</span></span>
<span data-ttu-id="c0b85-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c0b85-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0b85-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0b85-147">-WhatIf</span></span>
<span data-ttu-id="c0b85-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0b85-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0b85-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0b85-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0b85-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b85-150">CommonParameters</span></span>
<span data-ttu-id="c0b85-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0b85-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b85-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c0b85-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b85-153">輸入</span><span class="sxs-lookup"><span data-stu-id="c0b85-153">INPUTS</span></span>

### <span data-ttu-id="c0b85-154">System.object</span><span class="sxs-lookup"><span data-stu-id="c0b85-154">System.String</span></span>

### <span data-ttu-id="c0b85-155">System.object</span><span class="sxs-lookup"><span data-stu-id="c0b85-155">System.Int32</span></span>

### <span data-ttu-id="c0b85-156">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c0b85-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c0b85-157">PSResourceId [] （[]）</span><span class="sxs-lookup"><span data-stu-id="c0b85-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="c0b85-158">輸出</span><span class="sxs-lookup"><span data-stu-id="c0b85-158">OUTPUTS</span></span>

### <span data-ttu-id="c0b85-159">PSNatGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c0b85-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="c0b85-160">筆記</span><span class="sxs-lookup"><span data-stu-id="c0b85-160">NOTES</span></span>

## <span data-ttu-id="c0b85-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0b85-161">RELATED LINKS</span></span>
