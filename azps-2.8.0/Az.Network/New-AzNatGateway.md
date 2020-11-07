---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: f62b7bb2b338247305c53199b7f1e7087f195ffd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789322"
---
# <span data-ttu-id="ad92c-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ad92c-101">New-AzNatGateway</span></span>

## <span data-ttu-id="ad92c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad92c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad92c-103">使用屬性公用 Ip 位址/公用 Ip 首碼、IdleTimeoutInMinutes 和 Sku 建立新的 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="ad92c-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="ad92c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad92c-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad92c-105">說明</span><span class="sxs-lookup"><span data-stu-id="ad92c-105">DESCRIPTION</span></span>
<span data-ttu-id="ad92c-106">**新的-AzNatGateway** Cmdlet 會建立 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="ad92c-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="ad92c-107">Natgateway 需要下列各項：</span><span class="sxs-lookup"><span data-stu-id="ad92c-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="ad92c-108">公用 Ip 位址和/或公用 Ip 首碼</span><span class="sxs-lookup"><span data-stu-id="ad92c-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="ad92c-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ad92c-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="ad92c-110">Sku</span><span class="sxs-lookup"><span data-stu-id="ad92c-110">Sku</span></span>
- <span data-ttu-id="ad92c-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad92c-111">ResourceGroupName</span></span>
- <span data-ttu-id="ad92c-112">CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="ad92c-112">ResourceName</span></span>
- <span data-ttu-id="ad92c-113">位於</span><span class="sxs-lookup"><span data-stu-id="ad92c-113">Location</span></span>

## <span data-ttu-id="ad92c-114">示例</span><span class="sxs-lookup"><span data-stu-id="ad92c-114">EXAMPLES</span></span>

### <span data-ttu-id="ad92c-115">範例1：建立含公用 Ip 位址的 Nat 閘道</span><span class="sxs-lookup"><span data-stu-id="ad92c-115">Example 1 : Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="ad92c-116">範例2：建立含公用 Ip 首碼的 Nat 閘道</span><span class="sxs-lookup"><span data-stu-id="ad92c-116">Example 2 : Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="ad92c-117">範例3：在可用性區域1中建立含公用 IP 位址的 Nat 閘道</span><span class="sxs-lookup"><span data-stu-id="ad92c-117">Example 3 : Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="ad92c-118">第一個命令會建立標準的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ad92c-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="ad92c-119">第二個命令會在可用性區域1中建立含公用 IP 位址的 NAT 閘道。</span><span class="sxs-lookup"><span data-stu-id="ad92c-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="ad92c-120">參數</span><span class="sxs-lookup"><span data-stu-id="ad92c-120">PARAMETERS</span></span>

### <span data-ttu-id="ad92c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad92c-121">-AsJob</span></span>
<span data-ttu-id="ad92c-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad92c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad92c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad92c-123">-DefaultProfile</span></span>
<span data-ttu-id="ad92c-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad92c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad92c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ad92c-125">-Force</span></span>
<span data-ttu-id="ad92c-126">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="ad92c-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ad92c-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ad92c-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ad92c-128">Nat 閘道的空閒超時。</span><span class="sxs-lookup"><span data-stu-id="ad92c-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="ad92c-129">-位置</span><span class="sxs-lookup"><span data-stu-id="ad92c-129">-Location</span></span>
<span data-ttu-id="ad92c-130">位置。</span><span class="sxs-lookup"><span data-stu-id="ad92c-130">The location.</span></span>

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

### <span data-ttu-id="ad92c-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad92c-131">-Name</span></span>
<span data-ttu-id="ad92c-132">Nat 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad92c-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="ad92c-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ad92c-133">-PublicIpAddress</span></span>
<span data-ttu-id="ad92c-134">與 nat 閘道資源相關聯之公用 ip 位址的陣列。</span><span class="sxs-lookup"><span data-stu-id="ad92c-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="ad92c-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ad92c-135">-PublicIpPrefix</span></span>
<span data-ttu-id="ad92c-136">與 nat 閘道資源相關聯之公用 ip 首碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="ad92c-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="ad92c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad92c-137">-ResourceGroupName</span></span>
<span data-ttu-id="ad92c-138">Nat 閘道的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ad92c-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="ad92c-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="ad92c-139">-Sku</span></span>
<span data-ttu-id="ad92c-140">NAT 閘道 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad92c-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="ad92c-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="ad92c-141">-Tag</span></span>
<span data-ttu-id="ad92c-142">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="ad92c-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ad92c-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="ad92c-143">-Zone</span></span>
<span data-ttu-id="ad92c-144">表示應在其中部署 Nat 閘道之區域的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="ad92c-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="ad92c-145">-確認</span><span class="sxs-lookup"><span data-stu-id="ad92c-145">-Confirm</span></span>
<span data-ttu-id="ad92c-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad92c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad92c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad92c-147">-WhatIf</span></span>
<span data-ttu-id="ad92c-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad92c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad92c-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad92c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad92c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad92c-150">CommonParameters</span></span>
<span data-ttu-id="ad92c-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad92c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad92c-152">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ad92c-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad92c-153">輸入</span><span class="sxs-lookup"><span data-stu-id="ad92c-153">INPUTS</span></span>

### <span data-ttu-id="ad92c-154">System.object</span><span class="sxs-lookup"><span data-stu-id="ad92c-154">System.String</span></span>

### <span data-ttu-id="ad92c-155">System.object</span><span class="sxs-lookup"><span data-stu-id="ad92c-155">System.Int32</span></span>

### <span data-ttu-id="ad92c-156">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ad92c-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ad92c-157">PSResourceId [] （[]）</span><span class="sxs-lookup"><span data-stu-id="ad92c-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="ad92c-158">輸出</span><span class="sxs-lookup"><span data-stu-id="ad92c-158">OUTPUTS</span></span>

### <span data-ttu-id="ad92c-159">PSNatGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ad92c-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="ad92c-160">筆記</span><span class="sxs-lookup"><span data-stu-id="ad92c-160">NOTES</span></span>

## <span data-ttu-id="ad92c-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad92c-161">RELATED LINKS</span></span>
