---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: d03b52c477686f3aa724057771285eaf9d522a56
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794284"
---
# <span data-ttu-id="b4bf2-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b4bf2-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="b4bf2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4bf2-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bf2-103">建立 Azure express 路由回路。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="b4bf2-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4bf2-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4bf2-105">說明</span><span class="sxs-lookup"><span data-stu-id="b4bf2-105">DESCRIPTION</span></span>
<span data-ttu-id="b4bf2-106">**新的-AzExpressRouteCircuit** Cmdlet 會建立 Azure express 路由回路。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-106">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="b4bf2-107">示例</span><span class="sxs-lookup"><span data-stu-id="b4bf2-107">EXAMPLES</span></span>

### <span data-ttu-id="b4bf2-108">範例1：建立新的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="b4bf2-108">Example 1: Create a new ExpressRoute circuit</span></span>
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
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="b4bf2-109">參數</span><span class="sxs-lookup"><span data-stu-id="b4bf2-109">PARAMETERS</span></span>

### <span data-ttu-id="b4bf2-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="b4bf2-110">-AllowClassicOperations</span></span>
<span data-ttu-id="b4bf2-111">使用此參數可讓您使用傳統的 Azure PowerShell Cmdlet 來管理電路。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4bf2-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4bf2-112">-AsJob</span></span>
<span data-ttu-id="b4bf2-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b4bf2-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4bf2-114">-授權</span><span class="sxs-lookup"><span data-stu-id="b4bf2-114">-Authorization</span></span>
<span data-ttu-id="b4bf2-115">電路授權清單。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-115">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="b4bf2-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="b4bf2-116">-BandwidthInMbps</span></span>
<span data-ttu-id="b4bf2-117">電路頻寬。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="b4bf2-118">這必須是服務提供者支援的值。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-118">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4bf2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4bf2-119">-DefaultProfile</span></span>
<span data-ttu-id="b4bf2-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4bf2-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b4bf2-121">-Force</span></span>
<span data-ttu-id="b4bf2-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4bf2-123">-位置</span><span class="sxs-lookup"><span data-stu-id="b4bf2-123">-Location</span></span>
<span data-ttu-id="b4bf2-124">電路的位置。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-124">The location of the circuit.</span></span>

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

### <span data-ttu-id="b4bf2-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b4bf2-125">-Name</span></span>
<span data-ttu-id="b4bf2-126">所建立的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-126">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4bf2-127">對等</span><span class="sxs-lookup"><span data-stu-id="b4bf2-127">-Peering</span></span>
<span data-ttu-id="b4bf2-128">清單對等設定。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-128">A list peer configurations.</span></span>

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

### <span data-ttu-id="b4bf2-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="b4bf2-129">-PeeringLocation</span></span>
<span data-ttu-id="b4bf2-130">服務提供者支援之對等位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-130">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="b4bf2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4bf2-131">-ResourceGroupName</span></span>
<span data-ttu-id="b4bf2-132">將包含該電路的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-132">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="b4bf2-133">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="b4bf2-133">-ServiceProviderName</span></span>
<span data-ttu-id="b4bf2-134">電路服務提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-134">The name of the circuit service provider.</span></span> <span data-ttu-id="b4bf2-135">這必須符合 Get-AzExpressRouteServiceProvider Cmdlet 所列出的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-135">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="b4bf2-136">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="b4bf2-136">-SkuFamily</span></span>
<span data-ttu-id="b4bf2-137">SKU 系列決定帳單類型。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-137">SKU family determines the billing type.</span></span> <span data-ttu-id="b4bf2-138">此參數可能的值為： `MeteredData` 或 `UnlimitedData` 。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="b4bf2-139">請注意，您可以將帳單類型從 MeteredData 變更為 UnlimitedData，但您無法將類型從 UnlimitedData 變更為 MeteredData。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4bf2-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b4bf2-140">-SkuTier</span></span>
<span data-ttu-id="b4bf2-141">電路的服務層級。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-141">The tier of service for the circuit.</span></span> <span data-ttu-id="b4bf2-142">此參數可能的值為： `Standard` 或 `Premium` 。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4bf2-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4bf2-143">-Tag</span></span>
<span data-ttu-id="b4bf2-144">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b4bf2-145">例如：</span><span class="sxs-lookup"><span data-stu-id="b4bf2-145">For example:</span></span>

<span data-ttu-id="b4bf2-146">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b4bf2-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b4bf2-147">-確認</span><span class="sxs-lookup"><span data-stu-id="b4bf2-147">-Confirm</span></span>
<span data-ttu-id="b4bf2-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4bf2-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4bf2-149">-WhatIf</span></span>
<span data-ttu-id="b4bf2-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4bf2-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4bf2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bf2-152">CommonParameters</span></span>
<span data-ttu-id="b4bf2-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bf2-154">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b4bf2-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bf2-155">輸入</span><span class="sxs-lookup"><span data-stu-id="b4bf2-155">INPUTS</span></span>

## <span data-ttu-id="b4bf2-156">輸出</span><span class="sxs-lookup"><span data-stu-id="b4bf2-156">OUTPUTS</span></span>

### <span data-ttu-id="b4bf2-157">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b4bf2-157">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b4bf2-158">筆記</span><span class="sxs-lookup"><span data-stu-id="b4bf2-158">NOTES</span></span>

## <span data-ttu-id="b4bf2-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4bf2-159">RELATED LINKS</span></span>

[<span data-ttu-id="b4bf2-160">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b4bf2-160">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b4bf2-161">移動流覽 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b4bf2-161">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="b4bf2-162">移除-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b4bf2-162">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="b4bf2-163">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b4bf2-163">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
