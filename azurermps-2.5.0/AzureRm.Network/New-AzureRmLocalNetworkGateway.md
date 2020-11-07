---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: c450d2f6fd3d9a9b0368a667573aadadbd218d8f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801258"
---
# <span data-ttu-id="89b3b-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="89b3b-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="89b3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="89b3b-103">建立局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="89b3b-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89b3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="89b3b-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89b3b-105">說明</span><span class="sxs-lookup"><span data-stu-id="89b3b-105">DESCRIPTION</span></span>
<span data-ttu-id="89b3b-106">本機網路閘道是代表您的 VPN 裝置內部部署的物件。</span><span class="sxs-lookup"><span data-stu-id="89b3b-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="89b3b-107">**新的-AzureRmLocalNetworkGateway** Cmdlet 會根據閘道的名稱、資源組名稱、位置和 IP 位址，以及將連接到 Azure 的內部部署網路位址首碼，來建立代表您的在內部部署閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="89b3b-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="89b3b-108">示例</span><span class="sxs-lookup"><span data-stu-id="89b3b-108">EXAMPLES</span></span>

### <span data-ttu-id="89b3b-109">1：建立本機網路閘道</span><span class="sxs-lookup"><span data-stu-id="89b3b-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="89b3b-110">使用 IP 位址 "23.99.221.164"，以及位址首碼 "10.5.51.0/24" （位於內部部署），在資源群組 "myRG" 中，建立名為 "myLocalGW" 的本機網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="89b3b-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="89b3b-111">參數</span><span class="sxs-lookup"><span data-stu-id="89b3b-111">PARAMETERS</span></span>

### <span data-ttu-id="89b3b-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="89b3b-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="89b3b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89b3b-113">-AsJob</span></span>
<span data-ttu-id="89b3b-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="89b3b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89b3b-115">-Asn</span><span class="sxs-lookup"><span data-stu-id="89b3b-115">-Asn</span></span>
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

### <span data-ttu-id="89b3b-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="89b3b-116">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="89b3b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b3b-117">-DefaultProfile</span></span>
<span data-ttu-id="89b3b-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89b3b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89b3b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="89b3b-119">-Force</span></span>
<span data-ttu-id="89b3b-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="89b3b-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89b3b-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="89b3b-121">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="89b3b-122">-位置</span><span class="sxs-lookup"><span data-stu-id="89b3b-122">-Location</span></span>
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

### <span data-ttu-id="89b3b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="89b3b-123">-Name</span></span>
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

### <span data-ttu-id="89b3b-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="89b3b-124">-PeerWeight</span></span>
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

### <span data-ttu-id="89b3b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89b3b-125">-ResourceGroupName</span></span>
<span data-ttu-id="89b3b-126">指定本機網路閘道所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="89b3b-126">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="89b3b-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="89b3b-127">-Tag</span></span>
<span data-ttu-id="89b3b-128">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="89b3b-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="89b3b-129">例如：</span><span class="sxs-lookup"><span data-stu-id="89b3b-129">For example:</span></span>

<span data-ttu-id="89b3b-130">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="89b3b-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="89b3b-131">-確認</span><span class="sxs-lookup"><span data-stu-id="89b3b-131">-Confirm</span></span>
<span data-ttu-id="89b3b-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="89b3b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89b3b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89b3b-133">-WhatIf</span></span>
<span data-ttu-id="89b3b-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="89b3b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89b3b-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89b3b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89b3b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b3b-136">CommonParameters</span></span>
<span data-ttu-id="89b3b-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89b3b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b3b-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="89b3b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b3b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="89b3b-139">INPUTS</span></span>

## <span data-ttu-id="89b3b-140">輸出</span><span class="sxs-lookup"><span data-stu-id="89b3b-140">OUTPUTS</span></span>

### <span data-ttu-id="89b3b-141">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="89b3b-141">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="89b3b-142">筆記</span><span class="sxs-lookup"><span data-stu-id="89b3b-142">NOTES</span></span>

## <span data-ttu-id="89b3b-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="89b3b-143">RELATED LINKS</span></span>

[<span data-ttu-id="89b3b-144">AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="89b3b-144">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="89b3b-145">移除-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="89b3b-145">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="89b3b-146">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="89b3b-146">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
