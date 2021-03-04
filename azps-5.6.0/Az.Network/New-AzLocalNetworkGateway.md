---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 2a5b3260aff2167de9d46ad276d7ced1f0373b95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912354"
---
# <span data-ttu-id="18a82-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18a82-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="18a82-102">簡介</span><span class="sxs-lookup"><span data-stu-id="18a82-102">SYNOPSIS</span></span>
<span data-ttu-id="18a82-103">建立本地網路閘道</span><span class="sxs-lookup"><span data-stu-id="18a82-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="18a82-104">語法</span><span class="sxs-lookup"><span data-stu-id="18a82-104">SYNTAX</span></span>

### <span data-ttu-id="18a82-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="18a82-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18a82-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="18a82-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18a82-107">描述</span><span class="sxs-lookup"><span data-stu-id="18a82-107">DESCRIPTION</span></span>
<span data-ttu-id="18a82-108">Local Network Gateway 是代表您的 VPN 裝置內部部署的物件。</span><span class="sxs-lookup"><span data-stu-id="18a82-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="18a82-109">**New-AzLocalNetworkGateway** Cmdlet 會根據閘道的名稱、資源組名、位置和 IP 位址，以及將連接至 Azure 之內部部署網路的位址首碼，來建立代表內部部署閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="18a82-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="18a82-110">例子</span><span class="sxs-lookup"><span data-stu-id="18a82-110">EXAMPLES</span></span>

### <span data-ttu-id="18a82-111">範例 1：建立本地網路閘道</span><span class="sxs-lookup"><span data-stu-id="18a82-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="18a82-112">在位置 "myRG" 中，以 IP 位址 "23.99.221.164" 和位址首碼 "10.5.51.0/24" 為內部部署之位置"myLocalGW" 建立本地網路閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="18a82-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="18a82-113">參數</span><span class="sxs-lookup"><span data-stu-id="18a82-113">PARAMETERS</span></span>

### <span data-ttu-id="18a82-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="18a82-114">-AddressPrefix</span></span>
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

### <span data-ttu-id="18a82-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18a82-115">-AsJob</span></span>
<span data-ttu-id="18a82-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="18a82-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18a82-117">-Asn</span><span class="sxs-lookup"><span data-stu-id="18a82-117">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18a82-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="18a82-118">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="18a82-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a82-119">-DefaultProfile</span></span>
<span data-ttu-id="18a82-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="18a82-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18a82-121">-強制</span><span class="sxs-lookup"><span data-stu-id="18a82-121">-Force</span></span>
<span data-ttu-id="18a82-122">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="18a82-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="18a82-123">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="18a82-123">-Fqdn</span></span>
<span data-ttu-id="18a82-124">本地網路閘道的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="18a82-124">FQDN of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayFqdn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18a82-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="18a82-125">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18a82-126">-位置</span><span class="sxs-lookup"><span data-stu-id="18a82-126">-Location</span></span>
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

### <span data-ttu-id="18a82-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="18a82-127">-Name</span></span>
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

### <span data-ttu-id="18a82-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="18a82-128">-PeerWeight</span></span>
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

### <span data-ttu-id="18a82-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18a82-129">-ResourceGroupName</span></span>
<span data-ttu-id="18a82-130">指定本地網路閘道所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="18a82-130">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="18a82-131">-標記</span><span class="sxs-lookup"><span data-stu-id="18a82-131">-Tag</span></span>
<span data-ttu-id="18a82-132">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="18a82-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="18a82-133">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="18a82-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="18a82-134">-確認</span><span class="sxs-lookup"><span data-stu-id="18a82-134">-Confirm</span></span>
<span data-ttu-id="18a82-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="18a82-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18a82-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18a82-136">-WhatIf</span></span>
<span data-ttu-id="18a82-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="18a82-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18a82-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="18a82-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18a82-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a82-139">CommonParameters</span></span>
<span data-ttu-id="18a82-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="18a82-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a82-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18a82-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a82-142">輸入</span><span class="sxs-lookup"><span data-stu-id="18a82-142">INPUTS</span></span>

### <span data-ttu-id="18a82-143">System.String</span><span class="sxs-lookup"><span data-stu-id="18a82-143">System.String</span></span>

### <span data-ttu-id="18a82-144">System.String[]</span><span class="sxs-lookup"><span data-stu-id="18a82-144">System.String[]</span></span>

### <span data-ttu-id="18a82-145">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="18a82-145">System.UInt32</span></span>

### <span data-ttu-id="18a82-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="18a82-146">System.Int32</span></span>

### <span data-ttu-id="18a82-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="18a82-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="18a82-148">輸出</span><span class="sxs-lookup"><span data-stu-id="18a82-148">OUTPUTS</span></span>

### <span data-ttu-id="18a82-149">Microsoft.Azure.Commands.Network.models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18a82-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="18a82-150">筆記</span><span class="sxs-lookup"><span data-stu-id="18a82-150">NOTES</span></span>

## <span data-ttu-id="18a82-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="18a82-151">RELATED LINKS</span></span>

[<span data-ttu-id="18a82-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18a82-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="18a82-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18a82-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="18a82-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18a82-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
