---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 3acfbf1462a1f0ae75d95b9f3976c46fd07676f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453383"
---
# <span data-ttu-id="8c117-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c117-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="8c117-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c117-102">SYNOPSIS</span></span>
<span data-ttu-id="8c117-103">建立局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="8c117-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c117-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c117-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c117-105">說明</span><span class="sxs-lookup"><span data-stu-id="8c117-105">DESCRIPTION</span></span>
<span data-ttu-id="8c117-106">本機網路閘道是代表您的 VPN 裝置內部部署的物件。</span><span class="sxs-lookup"><span data-stu-id="8c117-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="8c117-107">**新的-AzureRmLocalNetworkGateway** Cmdlet 會根據閘道的名稱、資源組名稱、位置和 IP 位址，以及將連接到 Azure 的內部部署網路位址首碼，來建立代表您的在內部部署閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="8c117-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="8c117-108">示例</span><span class="sxs-lookup"><span data-stu-id="8c117-108">EXAMPLES</span></span>

### <span data-ttu-id="8c117-109">1：建立本機網路閘道</span><span class="sxs-lookup"><span data-stu-id="8c117-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="8c117-110">使用 IP 位址 "23.99.221.164"，以及位址首碼 "10.5.51.0/24" （位於內部部署），在資源群組 "myRG" 中，建立名為 "myLocalGW" 的本機網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="8c117-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="8c117-111">參數</span><span class="sxs-lookup"><span data-stu-id="8c117-111">PARAMETERS</span></span>

### <span data-ttu-id="8c117-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8c117-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="8c117-113">-Asn</span><span class="sxs-lookup"><span data-stu-id="8c117-113">-Asn</span></span>
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

### <span data-ttu-id="8c117-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="8c117-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="8c117-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8c117-115">-Force</span></span>
<span data-ttu-id="8c117-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="8c117-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8c117-117">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="8c117-117">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="8c117-118">-位置</span><span class="sxs-lookup"><span data-stu-id="8c117-118">-Location</span></span>
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

### <span data-ttu-id="8c117-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c117-119">-Name</span></span>
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

### <span data-ttu-id="8c117-120">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="8c117-120">-PeerWeight</span></span>
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

### <span data-ttu-id="8c117-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c117-121">-ResourceGroupName</span></span>
<span data-ttu-id="8c117-122">指定本機網路閘道所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8c117-122">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="8c117-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="8c117-123">-Tag</span></span>
<span data-ttu-id="8c117-124">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="8c117-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8c117-125">例如：</span><span class="sxs-lookup"><span data-stu-id="8c117-125">For example:</span></span>

<span data-ttu-id="8c117-126">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8c117-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8c117-127">-確認</span><span class="sxs-lookup"><span data-stu-id="8c117-127">-Confirm</span></span>
<span data-ttu-id="8c117-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c117-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c117-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c117-129">-WhatIf</span></span>
<span data-ttu-id="8c117-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c117-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c117-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c117-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c117-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c117-132">-DefaultProfile</span></span>
<span data-ttu-id="8c117-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c117-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c117-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c117-134">CommonParameters</span></span>
<span data-ttu-id="8c117-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c117-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c117-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c117-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c117-137">輸入</span><span class="sxs-lookup"><span data-stu-id="8c117-137">INPUTS</span></span>

## <span data-ttu-id="8c117-138">輸出</span><span class="sxs-lookup"><span data-stu-id="8c117-138">OUTPUTS</span></span>

### <span data-ttu-id="8c117-139">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8c117-139">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="8c117-140">筆記</span><span class="sxs-lookup"><span data-stu-id="8c117-140">NOTES</span></span>

## <span data-ttu-id="8c117-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c117-141">RELATED LINKS</span></span>

[<span data-ttu-id="8c117-142">AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c117-142">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="8c117-143">移除-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c117-143">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="8c117-144">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c117-144">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
