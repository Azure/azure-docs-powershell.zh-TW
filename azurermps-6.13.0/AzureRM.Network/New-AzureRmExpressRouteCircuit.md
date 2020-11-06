---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: cee0318367ad764a9cc9e37995f092462cd157a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449040"
---
# <span data-ttu-id="dc703-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dc703-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="dc703-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc703-102">SYNOPSIS</span></span>
<span data-ttu-id="dc703-103">建立 Azure express 路由回路。</span><span class="sxs-lookup"><span data-stu-id="dc703-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc703-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc703-104">SYNTAX</span></span>

### <span data-ttu-id="dc703-105">ServiceProvider</span><span class="sxs-lookup"><span data-stu-id="dc703-105">ServiceProvider</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ServiceProviderName <String>] [-PeeringLocation <String>]
 [-BandwidthInMbps <Int32>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc703-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="dc703-106">ExpressRoutePort</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ExpressRoutePort <PSExpressRoutePort>] [-BandwidthInGbps <Double>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc703-107">說明</span><span class="sxs-lookup"><span data-stu-id="dc703-107">DESCRIPTION</span></span>
<span data-ttu-id="dc703-108">**新的-AzureRmExpressRouteCircuit** Cmdlet 會建立 Azure express 路由回路。</span><span class="sxs-lookup"><span data-stu-id="dc703-108">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="dc703-109">示例</span><span class="sxs-lookup"><span data-stu-id="dc703-109">EXAMPLES</span></span>

### <span data-ttu-id="dc703-110">範例1：建立新的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="dc703-110">Example 1: Create a new ExpressRoute circuit</span></span>
```
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
New-AzureRmExpressRouteCircuit @parameters
```

### <span data-ttu-id="dc703-111">範例2：在 ExpressRoutePort 上建立新的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="dc703-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="dc703-112">參數</span><span class="sxs-lookup"><span data-stu-id="dc703-112">PARAMETERS</span></span>

### <span data-ttu-id="dc703-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="dc703-113">-AllowClassicOperations</span></span>
<span data-ttu-id="dc703-114">使用此參數可讓您使用傳統的 Azure PowerShell Cmdlet 來管理電路。</span><span class="sxs-lookup"><span data-stu-id="dc703-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="dc703-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc703-115">-AsJob</span></span>
<span data-ttu-id="dc703-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dc703-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc703-117">-授權</span><span class="sxs-lookup"><span data-stu-id="dc703-117">-Authorization</span></span>
<span data-ttu-id="dc703-118">電路授權清單。</span><span class="sxs-lookup"><span data-stu-id="dc703-118">A list of circuit authorizations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc703-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="dc703-119">-BandwidthInGbps</span></span>
<span data-ttu-id="dc703-120">在 ExpressRoutePort 資源上預配電路時的電路頻寬。</span><span class="sxs-lookup"><span data-stu-id="dc703-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc703-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="dc703-121">-BandwidthInMbps</span></span>
<span data-ttu-id="dc703-122">電路頻寬。</span><span class="sxs-lookup"><span data-stu-id="dc703-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="dc703-123">這必須是服務提供者支援的值。</span><span class="sxs-lookup"><span data-stu-id="dc703-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc703-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc703-124">-DefaultProfile</span></span>
<span data-ttu-id="dc703-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc703-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc703-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="dc703-126">-ExpressRoutePort</span></span>
<span data-ttu-id="dc703-127">在 ExpressRoutePort 資源上預配電路時，對 ExpressRoutePort 資源的參照。</span><span class="sxs-lookup"><span data-stu-id="dc703-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc703-128">-Force</span><span class="sxs-lookup"><span data-stu-id="dc703-128">-Force</span></span>
<span data-ttu-id="dc703-129">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="dc703-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dc703-130">-位置</span><span class="sxs-lookup"><span data-stu-id="dc703-130">-Location</span></span>
<span data-ttu-id="dc703-131">電路的位置。</span><span class="sxs-lookup"><span data-stu-id="dc703-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="dc703-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc703-132">-Name</span></span>
<span data-ttu-id="dc703-133">所建立的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="dc703-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="dc703-134">對等</span><span class="sxs-lookup"><span data-stu-id="dc703-134">-Peering</span></span>
<span data-ttu-id="dc703-135">清單對等設定。</span><span class="sxs-lookup"><span data-stu-id="dc703-135">A list peer configurations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc703-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="dc703-136">-PeeringLocation</span></span>
<span data-ttu-id="dc703-137">服務提供者支援之對等位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc703-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc703-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc703-138">-ResourceGroupName</span></span>
<span data-ttu-id="dc703-139">將包含該電路的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="dc703-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="dc703-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="dc703-140">-ServiceProviderName</span></span>
<span data-ttu-id="dc703-141">電路服務提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc703-141">The name of the circuit service provider.</span></span> <span data-ttu-id="dc703-142">這必須符合 Get-AzureRmExpressRouteServiceProvider Cmdlet 所列出的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc703-142">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc703-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="dc703-143">-SkuFamily</span></span>
<span data-ttu-id="dc703-144">SKU 系列決定帳單類型。</span><span class="sxs-lookup"><span data-stu-id="dc703-144">SKU family determines the billing type.</span></span> <span data-ttu-id="dc703-145">此參數可能的值為： `MeteredData` 或 `UnlimitedData` 。</span><span class="sxs-lookup"><span data-stu-id="dc703-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="dc703-146">請注意，您可以將帳單類型從 MeteredData 變更為 UnlimitedData，但您無法將類型從 UnlimitedData 變更為 MeteredData。</span><span class="sxs-lookup"><span data-stu-id="dc703-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="dc703-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="dc703-147">-SkuTier</span></span>
<span data-ttu-id="dc703-148">電路的服務層級。</span><span class="sxs-lookup"><span data-stu-id="dc703-148">The tier of service for the circuit.</span></span> <span data-ttu-id="dc703-149">此參數可能的值為： `Standard` 或 `Premium` 。</span><span class="sxs-lookup"><span data-stu-id="dc703-149">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc703-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="dc703-150">-Tag</span></span>
<span data-ttu-id="dc703-151">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="dc703-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dc703-152">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="dc703-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="dc703-153">-確認</span><span class="sxs-lookup"><span data-stu-id="dc703-153">-Confirm</span></span>
<span data-ttu-id="dc703-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dc703-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc703-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc703-155">-WhatIf</span></span>
<span data-ttu-id="dc703-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dc703-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc703-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc703-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc703-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc703-158">CommonParameters</span></span>
<span data-ttu-id="dc703-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc703-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc703-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc703-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc703-161">輸入</span><span class="sxs-lookup"><span data-stu-id="dc703-161">INPUTS</span></span>

### <span data-ttu-id="dc703-162">System.object</span><span class="sxs-lookup"><span data-stu-id="dc703-162">System.String</span></span>

### <span data-ttu-id="dc703-163">System.object</span><span class="sxs-lookup"><span data-stu-id="dc703-163">System.Int32</span></span>

### <span data-ttu-id="dc703-164">[System.object]. 清單 ' 1 [PSPeering，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="dc703-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPeering, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="dc703-165">[System.object]. 清單 ' 1 [PSExpressRouteCircuitAuthorization，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="dc703-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="dc703-166">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="dc703-166">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="dc703-167">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dc703-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dc703-168">輸出</span><span class="sxs-lookup"><span data-stu-id="dc703-168">OUTPUTS</span></span>

### <span data-ttu-id="dc703-169">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dc703-169">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="dc703-170">筆記</span><span class="sxs-lookup"><span data-stu-id="dc703-170">NOTES</span></span>

## <span data-ttu-id="dc703-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc703-171">RELATED LINKS</span></span>

[<span data-ttu-id="dc703-172">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dc703-172">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="dc703-173">移動流覽 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dc703-173">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="dc703-174">移除-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dc703-174">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="dc703-175">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dc703-175">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
