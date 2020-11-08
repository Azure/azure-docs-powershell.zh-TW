---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: f355d011bbd810fa309cd8b7d64ed95090a00ea6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796882"
---
# <span data-ttu-id="eafa7-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eafa7-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="eafa7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eafa7-102">SYNOPSIS</span></span>
<span data-ttu-id="eafa7-103">建立局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="eafa7-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="eafa7-104">句法</span><span class="sxs-lookup"><span data-stu-id="eafa7-104">SYNTAX</span></span>

### <span data-ttu-id="eafa7-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="eafa7-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eafa7-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="eafa7-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eafa7-107">說明</span><span class="sxs-lookup"><span data-stu-id="eafa7-107">DESCRIPTION</span></span>
<span data-ttu-id="eafa7-108">本機網路閘道是代表您的 VPN 裝置內部部署的物件。</span><span class="sxs-lookup"><span data-stu-id="eafa7-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="eafa7-109">**新的-AzLocalNetworkGateway** Cmdlet 會根據閘道的名稱、資源組名稱、位置和 IP 位址，以及將連接到 Azure 的內部部署網路位址首碼，來建立代表您的在內部部署閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="eafa7-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="eafa7-110">示例</span><span class="sxs-lookup"><span data-stu-id="eafa7-110">EXAMPLES</span></span>

### <span data-ttu-id="eafa7-111">1：建立本機網路閘道</span><span class="sxs-lookup"><span data-stu-id="eafa7-111">1: Create a Local Network Gateway</span></span>
```
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="eafa7-112">使用 IP 位址 "23.99.221.164"，以及位址首碼 "10.5.51.0/24" （位於內部部署），在資源群組 "myRG" 中，建立名為 "myLocalGW" 的本機網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="eafa7-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="eafa7-113">參數</span><span class="sxs-lookup"><span data-stu-id="eafa7-113">PARAMETERS</span></span>

### <span data-ttu-id="eafa7-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="eafa7-114">-AddressPrefix</span></span>
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

### <span data-ttu-id="eafa7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eafa7-115">-AsJob</span></span>
<span data-ttu-id="eafa7-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eafa7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eafa7-117">-Asn</span><span class="sxs-lookup"><span data-stu-id="eafa7-117">-Asn</span></span>
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

### <span data-ttu-id="eafa7-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="eafa7-118">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="eafa7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafa7-119">-DefaultProfile</span></span>
<span data-ttu-id="eafa7-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eafa7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eafa7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="eafa7-121">-Force</span></span>
<span data-ttu-id="eafa7-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="eafa7-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eafa7-123">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="eafa7-123">-Fqdn</span></span>
<span data-ttu-id="eafa7-124">本機網路閘道的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="eafa7-124">FQDN of local network gateway.</span></span>

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

### <span data-ttu-id="eafa7-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="eafa7-125">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="eafa7-126">-位置</span><span class="sxs-lookup"><span data-stu-id="eafa7-126">-Location</span></span>
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

### <span data-ttu-id="eafa7-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="eafa7-127">-Name</span></span>
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

### <span data-ttu-id="eafa7-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="eafa7-128">-PeerWeight</span></span>
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

### <span data-ttu-id="eafa7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eafa7-129">-ResourceGroupName</span></span>
<span data-ttu-id="eafa7-130">指定本機網路閘道所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="eafa7-130">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="eafa7-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="eafa7-131">-Tag</span></span>
<span data-ttu-id="eafa7-132">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="eafa7-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="eafa7-133">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="eafa7-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="eafa7-134">-確認</span><span class="sxs-lookup"><span data-stu-id="eafa7-134">-Confirm</span></span>
<span data-ttu-id="eafa7-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eafa7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eafa7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eafa7-136">-WhatIf</span></span>
<span data-ttu-id="eafa7-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eafa7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eafa7-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eafa7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eafa7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafa7-139">CommonParameters</span></span>
<span data-ttu-id="eafa7-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eafa7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafa7-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eafa7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafa7-142">輸入</span><span class="sxs-lookup"><span data-stu-id="eafa7-142">INPUTS</span></span>

### <span data-ttu-id="eafa7-143">System.object</span><span class="sxs-lookup"><span data-stu-id="eafa7-143">System.String</span></span>

### <span data-ttu-id="eafa7-144">System.object []</span><span class="sxs-lookup"><span data-stu-id="eafa7-144">System.String[]</span></span>

### <span data-ttu-id="eafa7-145">UInt32</span><span class="sxs-lookup"><span data-stu-id="eafa7-145">System.UInt32</span></span>

### <span data-ttu-id="eafa7-146">System.object</span><span class="sxs-lookup"><span data-stu-id="eafa7-146">System.Int32</span></span>

### <span data-ttu-id="eafa7-147">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="eafa7-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eafa7-148">輸出</span><span class="sxs-lookup"><span data-stu-id="eafa7-148">OUTPUTS</span></span>

### <span data-ttu-id="eafa7-149">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="eafa7-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="eafa7-150">筆記</span><span class="sxs-lookup"><span data-stu-id="eafa7-150">NOTES</span></span>

## <span data-ttu-id="eafa7-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="eafa7-151">RELATED LINKS</span></span>

[<span data-ttu-id="eafa7-152">AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eafa7-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="eafa7-153">移除-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eafa7-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="eafa7-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eafa7-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)