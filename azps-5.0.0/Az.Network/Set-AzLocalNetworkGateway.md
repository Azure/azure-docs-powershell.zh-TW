---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: ac93b104a8ccc1afbeb41bcd11910b76f7d4039f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140643"
---
# <span data-ttu-id="64436-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64436-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="64436-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64436-102">SYNOPSIS</span></span>
<span data-ttu-id="64436-103">修改本機網路閘道。</span><span class="sxs-lookup"><span data-stu-id="64436-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="64436-104">句法</span><span class="sxs-lookup"><span data-stu-id="64436-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway> [-AddressPrefix <String[]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64436-105">說明</span><span class="sxs-lookup"><span data-stu-id="64436-105">DESCRIPTION</span></span>
<span data-ttu-id="64436-106">**AzLocalNetworkGateway** Cmdlet 會修改本機網路閘道。</span><span class="sxs-lookup"><span data-stu-id="64436-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="64436-107">示例</span><span class="sxs-lookup"><span data-stu-id="64436-107">EXAMPLES</span></span>

### <span data-ttu-id="64436-108">範例1</span><span class="sxs-lookup"><span data-stu-id="64436-108">Example 1</span></span>
<span data-ttu-id="64436-109">設定現有閘道的配置</span><span class="sxs-lookup"><span data-stu-id="64436-109">Set configuration for an existing gateway</span></span>


```
$lgw = Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
Set-AzLocalNetworkGateway -LocalNetworkGateway $lgw

Name                     : myLocalGW
ResourceGroupName        : TestRG1
Location                 : westus
Id                       : /subscriptions/81ab786c-56eb-4a4d-bb5f-f60329772466/resourceGroups/TestRG1/providers/Microso
                           ft.Network/localNetworkGateways/myLocalGW
Etag                     : W/"d2de6968-315e-411d-a4b8-a8c335abe61b"
ResourceGuid             : 393acf8b-dbb8-4b08-a9ea-c714570710e1
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : 1.2.3.4
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

## <span data-ttu-id="64436-110">參數</span><span class="sxs-lookup"><span data-stu-id="64436-110">PARAMETERS</span></span>

### <span data-ttu-id="64436-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="64436-111">-AddressPrefix</span></span>
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

### <span data-ttu-id="64436-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64436-112">-AsJob</span></span>
<span data-ttu-id="64436-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="64436-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64436-114">-Asn</span><span class="sxs-lookup"><span data-stu-id="64436-114">-Asn</span></span>
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

### <span data-ttu-id="64436-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="64436-115">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="64436-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64436-116">-DefaultProfile</span></span>
<span data-ttu-id="64436-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="64436-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64436-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64436-118">-LocalNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64436-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="64436-119">-PeerWeight</span></span>
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

### <span data-ttu-id="64436-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64436-120">CommonParameters</span></span>
<span data-ttu-id="64436-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64436-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64436-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="64436-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64436-123">輸入</span><span class="sxs-lookup"><span data-stu-id="64436-123">INPUTS</span></span>

### <span data-ttu-id="64436-124">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="64436-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="64436-125">System.object []</span><span class="sxs-lookup"><span data-stu-id="64436-125">System.String[]</span></span>

### <span data-ttu-id="64436-126">UInt32</span><span class="sxs-lookup"><span data-stu-id="64436-126">System.UInt32</span></span>

### <span data-ttu-id="64436-127">System.object</span><span class="sxs-lookup"><span data-stu-id="64436-127">System.String</span></span>

### <span data-ttu-id="64436-128">System.object</span><span class="sxs-lookup"><span data-stu-id="64436-128">System.Int32</span></span>

## <span data-ttu-id="64436-129">輸出</span><span class="sxs-lookup"><span data-stu-id="64436-129">OUTPUTS</span></span>

### <span data-ttu-id="64436-130">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="64436-130">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="64436-131">筆記</span><span class="sxs-lookup"><span data-stu-id="64436-131">NOTES</span></span>

## <span data-ttu-id="64436-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="64436-132">RELATED LINKS</span></span>

[<span data-ttu-id="64436-133">AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64436-133">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="64436-134">新-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64436-134">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="64436-135">移除-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64436-135">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)
