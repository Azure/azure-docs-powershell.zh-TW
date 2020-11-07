---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 37255dfda50d7c055aad6941bbf417d1aa852d35
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794264"
---
# <span data-ttu-id="74aca-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="74aca-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="74aca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74aca-102">SYNOPSIS</span></span>
<span data-ttu-id="74aca-103">建立局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="74aca-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="74aca-104">句法</span><span class="sxs-lookup"><span data-stu-id="74aca-104">SYNTAX</span></span>

```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74aca-105">說明</span><span class="sxs-lookup"><span data-stu-id="74aca-105">DESCRIPTION</span></span>
<span data-ttu-id="74aca-106">本機網路閘道是代表您的 VPN 裝置內部部署的物件。</span><span class="sxs-lookup"><span data-stu-id="74aca-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="74aca-107">**新的-AzLocalNetworkGateway** Cmdlet 會根據閘道的名稱、資源組名稱、位置和 IP 位址，以及將連接到 Azure 的內部部署網路位址首碼，來建立代表您的在內部部署閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="74aca-107">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="74aca-108">示例</span><span class="sxs-lookup"><span data-stu-id="74aca-108">EXAMPLES</span></span>

### <span data-ttu-id="74aca-109">1：建立本機網路閘道</span><span class="sxs-lookup"><span data-stu-id="74aca-109">1: Create a Local Network Gateway</span></span>
```
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="74aca-110">使用 IP 位址 "23.99.221.164"，以及位址首碼 "10.5.51.0/24" （位於內部部署），在資源群組 "myRG" 中，建立名為 "myLocalGW" 的本機網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="74aca-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="74aca-111">參數</span><span class="sxs-lookup"><span data-stu-id="74aca-111">PARAMETERS</span></span>

### <span data-ttu-id="74aca-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="74aca-112">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74aca-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74aca-113">-AsJob</span></span>
<span data-ttu-id="74aca-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="74aca-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74aca-115">-Asn</span><span class="sxs-lookup"><span data-stu-id="74aca-115">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74aca-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="74aca-116">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74aca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74aca-117">-DefaultProfile</span></span>
<span data-ttu-id="74aca-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74aca-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74aca-119">-Force</span><span class="sxs-lookup"><span data-stu-id="74aca-119">-Force</span></span>
<span data-ttu-id="74aca-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="74aca-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="74aca-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="74aca-121">-GatewayIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74aca-122">-位置</span><span class="sxs-lookup"><span data-stu-id="74aca-122">-Location</span></span>
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

### <span data-ttu-id="74aca-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="74aca-123">-Name</span></span>
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

### <span data-ttu-id="74aca-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="74aca-124">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74aca-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74aca-125">-ResourceGroupName</span></span>
<span data-ttu-id="74aca-126">指定本機網路閘道所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="74aca-126">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="74aca-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="74aca-127">-Tag</span></span>
<span data-ttu-id="74aca-128">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="74aca-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="74aca-129">例如：</span><span class="sxs-lookup"><span data-stu-id="74aca-129">For example:</span></span>

<span data-ttu-id="74aca-130">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="74aca-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="74aca-131">-確認</span><span class="sxs-lookup"><span data-stu-id="74aca-131">-Confirm</span></span>
<span data-ttu-id="74aca-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74aca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74aca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74aca-133">-WhatIf</span></span>
<span data-ttu-id="74aca-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74aca-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74aca-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74aca-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74aca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74aca-136">CommonParameters</span></span>
<span data-ttu-id="74aca-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74aca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74aca-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74aca-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74aca-139">輸入</span><span class="sxs-lookup"><span data-stu-id="74aca-139">INPUTS</span></span>

## <span data-ttu-id="74aca-140">輸出</span><span class="sxs-lookup"><span data-stu-id="74aca-140">OUTPUTS</span></span>

### <span data-ttu-id="74aca-141">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="74aca-141">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="74aca-142">筆記</span><span class="sxs-lookup"><span data-stu-id="74aca-142">NOTES</span></span>

## <span data-ttu-id="74aca-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="74aca-143">RELATED LINKS</span></span>

[<span data-ttu-id="74aca-144">AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="74aca-144">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="74aca-145">移除-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="74aca-145">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="74aca-146">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="74aca-146">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
