---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: 479b89296ae52221f714992791ed73cd14bf2fe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128949"
---
# <span data-ttu-id="3fbd3-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3fbd3-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="3fbd3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fbd3-102">SYNOPSIS</span></span>
<span data-ttu-id="3fbd3-103">建立 Azure express 路由回路。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="3fbd3-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fbd3-104">SYNTAX</span></span>

### <span data-ttu-id="3fbd3-105">ServiceProvider (預設) </span><span class="sxs-lookup"><span data-stu-id="3fbd3-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fbd3-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3fbd3-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fbd3-107">說明</span><span class="sxs-lookup"><span data-stu-id="3fbd3-107">DESCRIPTION</span></span>
<span data-ttu-id="3fbd3-108">**新的-AzExpressRouteCircuit** Cmdlet 會建立 Azure express 路由回路。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="3fbd3-109">示例</span><span class="sxs-lookup"><span data-stu-id="3fbd3-109">EXAMPLES</span></span>

### <span data-ttu-id="3fbd3-110">範例1：建立新的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="3fbd3-110">Example 1: Create a new ExpressRoute circuit</span></span>
```powershell
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

### <span data-ttu-id="3fbd3-111">範例2：在 ExpressRoutePort 上建立新的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="3fbd3-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```powershell
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="3fbd3-112">參數</span><span class="sxs-lookup"><span data-stu-id="3fbd3-112">PARAMETERS</span></span>

### <span data-ttu-id="3fbd3-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="3fbd3-113">-AllowClassicOperations</span></span>
<span data-ttu-id="3fbd3-114">使用此參數可讓您使用傳統的 Azure PowerShell Cmdlet 來管理電路。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbd3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fbd3-115">-AsJob</span></span>
<span data-ttu-id="3fbd3-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3fbd3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fbd3-117">-授權</span><span class="sxs-lookup"><span data-stu-id="3fbd3-117">-Authorization</span></span>
<span data-ttu-id="3fbd3-118">電路授權清單。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-118">A list of circuit authorizations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbd3-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="3fbd3-119">-BandwidthInGbps</span></span>
<span data-ttu-id="3fbd3-120">在 ExpressRoutePort 資源上預配電路時的電路頻寬。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: System.Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbd3-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="3fbd3-121">-BandwidthInMbps</span></span>
<span data-ttu-id="3fbd3-122">電路頻寬。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="3fbd3-123">這必須是服務提供者支援的值。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbd3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fbd3-124">-DefaultProfile</span></span>
<span data-ttu-id="3fbd3-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fbd3-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3fbd3-126">-ExpressRoutePort</span></span>
<span data-ttu-id="3fbd3-127">在 ExpressRoutePort 資源上預配電路時，對 ExpressRoutePort 資源的參照。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbd3-128">-Force</span><span class="sxs-lookup"><span data-stu-id="3fbd3-128">-Force</span></span>
<span data-ttu-id="3fbd3-129">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3fbd3-130">-位置</span><span class="sxs-lookup"><span data-stu-id="3fbd3-130">-Location</span></span>
<span data-ttu-id="3fbd3-131">電路的位置。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="3fbd3-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="3fbd3-132">-Name</span></span>
<span data-ttu-id="3fbd3-133">所建立的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="3fbd3-134">對等</span><span class="sxs-lookup"><span data-stu-id="3fbd3-134">-Peering</span></span>
<span data-ttu-id="3fbd3-135">清單對等設定。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-135">A list peer configurations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbd3-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="3fbd3-136">-PeeringLocation</span></span>
<span data-ttu-id="3fbd3-137">服務提供者支援之對等位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbd3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fbd3-138">-ResourceGroupName</span></span>
<span data-ttu-id="3fbd3-139">將包含該電路的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="3fbd3-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="3fbd3-140">-ServiceProviderName</span></span>
<span data-ttu-id="3fbd3-141">電路服務提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-141">The name of the circuit service provider.</span></span> <span data-ttu-id="3fbd3-142">這必須符合 Get-AzExpressRouteServiceProvider Cmdlet 所列出的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbd3-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="3fbd3-143">-SkuFamily</span></span>
<span data-ttu-id="3fbd3-144">SKU 系列決定帳單類型。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-144">SKU family determines the billing type.</span></span> <span data-ttu-id="3fbd3-145">此參數可能的值為： `MeteredData` 或 `UnlimitedData` 。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="3fbd3-146">請注意，您可以將帳單類型從 MeteredData 變更為 UnlimitedData，但您無法將類型從 UnlimitedData 變更為 MeteredData。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbd3-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="3fbd3-147">-SkuTier</span></span>
<span data-ttu-id="3fbd3-148">電路的服務層級。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-148">The tier of service for the circuit.</span></span> <span data-ttu-id="3fbd3-149">此參數可能的值為： `Standard` `Premium` 或 `Local` 。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium, Local

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbd3-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="3fbd3-150">-Tag</span></span>
<span data-ttu-id="3fbd3-151">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3fbd3-152">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3fbd3-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3fbd3-153">-確認</span><span class="sxs-lookup"><span data-stu-id="3fbd3-153">-Confirm</span></span>
<span data-ttu-id="3fbd3-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fbd3-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fbd3-155">-WhatIf</span></span>
<span data-ttu-id="3fbd3-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fbd3-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fbd3-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fbd3-158">CommonParameters</span></span>
<span data-ttu-id="3fbd3-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fbd3-160">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3fbd3-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fbd3-161">輸入</span><span class="sxs-lookup"><span data-stu-id="3fbd3-161">INPUTS</span></span>

### <span data-ttu-id="3fbd3-162">System.object</span><span class="sxs-lookup"><span data-stu-id="3fbd3-162">System.String</span></span>

### <span data-ttu-id="3fbd3-163">System.object</span><span class="sxs-lookup"><span data-stu-id="3fbd3-163">System.Int32</span></span>

### <span data-ttu-id="3fbd3-164">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3fbd3-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="3fbd3-165">Double</span><span class="sxs-lookup"><span data-stu-id="3fbd3-165">System.Double</span></span>

### <span data-ttu-id="3fbd3-166">PSPeering [] （[]）</span><span class="sxs-lookup"><span data-stu-id="3fbd3-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="3fbd3-167">PSExpressRouteCircuitAuthorization [] （[]）</span><span class="sxs-lookup"><span data-stu-id="3fbd3-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="3fbd3-168">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3fbd3-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3fbd3-169">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3fbd3-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3fbd3-170">輸出</span><span class="sxs-lookup"><span data-stu-id="3fbd3-170">OUTPUTS</span></span>

### <span data-ttu-id="3fbd3-171">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3fbd3-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3fbd3-172">筆記</span><span class="sxs-lookup"><span data-stu-id="3fbd3-172">NOTES</span></span>

## <span data-ttu-id="3fbd3-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fbd3-173">RELATED LINKS</span></span>

[<span data-ttu-id="3fbd3-174">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3fbd3-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="3fbd3-175">移動流覽 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3fbd3-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="3fbd3-176">移除-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3fbd3-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="3fbd3-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3fbd3-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
