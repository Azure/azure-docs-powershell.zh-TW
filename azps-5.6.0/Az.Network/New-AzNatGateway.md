---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 168a1803781748eb81c3a2087876b2a7b18d9d39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901965"
---
# <span data-ttu-id="28082-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="28082-101">New-AzNatGateway</span></span>

## <span data-ttu-id="28082-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28082-102">SYNOPSIS</span></span>
<span data-ttu-id="28082-103">使用屬性公用 IP 位址/公用 Ip 首碼、IdleTimeoutInMinutes 和 SKU 來建立新的 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="28082-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="28082-104">語法</span><span class="sxs-lookup"><span data-stu-id="28082-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28082-105">描述</span><span class="sxs-lookup"><span data-stu-id="28082-105">DESCRIPTION</span></span>
<span data-ttu-id="28082-106">**New-AzNatGateway** Cmdlet 會建立 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="28082-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="28082-107">Natgateway 需要下列專案：</span><span class="sxs-lookup"><span data-stu-id="28082-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="28082-108">公用 Ip 位址和/或公用 Ip 首碼</span><span class="sxs-lookup"><span data-stu-id="28082-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="28082-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="28082-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="28082-110">Sku</span><span class="sxs-lookup"><span data-stu-id="28082-110">Sku</span></span>
- <span data-ttu-id="28082-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28082-111">ResourceGroupName</span></span>
- <span data-ttu-id="28082-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="28082-112">ResourceName</span></span>
- <span data-ttu-id="28082-113">位置</span><span class="sxs-lookup"><span data-stu-id="28082-113">Location</span></span>

## <span data-ttu-id="28082-114">例子</span><span class="sxs-lookup"><span data-stu-id="28082-114">EXAMPLES</span></span>

### <span data-ttu-id="28082-115">範例 1：使用公用 IP 位址建立 Nat 閘道</span><span class="sxs-lookup"><span data-stu-id="28082-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="28082-116">範例 2：建立具有公用 Ip 首碼的 Nat 閘道</span><span class="sxs-lookup"><span data-stu-id="28082-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="28082-117">範例 3：在可用性區域 1 中建立具有公用 IP 位址的 Nat 閘道</span><span class="sxs-lookup"><span data-stu-id="28082-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="28082-118">第一個命令會建立標準公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="28082-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="28082-119">第二個命令在可用性區域 1 中建立具有公用 IP 位址的 NAT 閘道。</span><span class="sxs-lookup"><span data-stu-id="28082-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="28082-120">參數</span><span class="sxs-lookup"><span data-stu-id="28082-120">PARAMETERS</span></span>

### <span data-ttu-id="28082-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28082-121">-AsJob</span></span>
<span data-ttu-id="28082-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="28082-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28082-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28082-123">-DefaultProfile</span></span>
<span data-ttu-id="28082-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28082-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28082-125">-強制</span><span class="sxs-lookup"><span data-stu-id="28082-125">-Force</span></span>
<span data-ttu-id="28082-126">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="28082-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="28082-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="28082-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="28082-128">nat 閘道的閒置超時。</span><span class="sxs-lookup"><span data-stu-id="28082-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="28082-129">-位置</span><span class="sxs-lookup"><span data-stu-id="28082-129">-Location</span></span>
<span data-ttu-id="28082-130">位置。</span><span class="sxs-lookup"><span data-stu-id="28082-130">The location.</span></span>

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

### <span data-ttu-id="28082-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="28082-131">-Name</span></span>
<span data-ttu-id="28082-132">nat 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="28082-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="28082-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="28082-133">-PublicIpAddress</span></span>
<span data-ttu-id="28082-134">與 nat 閘道資源相關聯的公用 ip 位址陣列。</span><span class="sxs-lookup"><span data-stu-id="28082-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="28082-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="28082-135">-PublicIpPrefix</span></span>
<span data-ttu-id="28082-136">與 nat 閘道資源相關聯的公用 ip 首碼陣列。</span><span class="sxs-lookup"><span data-stu-id="28082-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="28082-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28082-137">-ResourceGroupName</span></span>
<span data-ttu-id="28082-138">nat 閘道的資源組名。</span><span class="sxs-lookup"><span data-stu-id="28082-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="28082-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="28082-139">-Sku</span></span>
<span data-ttu-id="28082-140">NAT 閘道 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="28082-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="28082-141">-標記</span><span class="sxs-lookup"><span data-stu-id="28082-141">-Tag</span></span>
<span data-ttu-id="28082-142">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="28082-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="28082-143">-區域</span><span class="sxs-lookup"><span data-stu-id="28082-143">-Zone</span></span>
<span data-ttu-id="28082-144">表示應部署 Nat 閘道之區域的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="28082-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="28082-145">-確認</span><span class="sxs-lookup"><span data-stu-id="28082-145">-Confirm</span></span>
<span data-ttu-id="28082-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="28082-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28082-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28082-147">-WhatIf</span></span>
<span data-ttu-id="28082-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28082-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28082-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28082-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28082-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28082-150">CommonParameters</span></span>
<span data-ttu-id="28082-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28082-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28082-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28082-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28082-153">輸入</span><span class="sxs-lookup"><span data-stu-id="28082-153">INPUTS</span></span>

### <span data-ttu-id="28082-154">System.String</span><span class="sxs-lookup"><span data-stu-id="28082-154">System.String</span></span>

### <span data-ttu-id="28082-155">System.Int32</span><span class="sxs-lookup"><span data-stu-id="28082-155">System.Int32</span></span>

### <span data-ttu-id="28082-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="28082-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="28082-157">Microsoft.Azure.Commands.Network.models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="28082-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="28082-158">輸出</span><span class="sxs-lookup"><span data-stu-id="28082-158">OUTPUTS</span></span>

### <span data-ttu-id="28082-159">Microsoft.Azure.Commands.Network.models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="28082-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="28082-160">筆記</span><span class="sxs-lookup"><span data-stu-id="28082-160">NOTES</span></span>

## <span data-ttu-id="28082-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="28082-161">RELATED LINKS</span></span>
