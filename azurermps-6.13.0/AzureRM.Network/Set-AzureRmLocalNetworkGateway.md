---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: a37cb732aed95a2c31c970d83558a3eff8ab31c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443796"
---
# <span data-ttu-id="ad413-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad413-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="ad413-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad413-102">SYNOPSIS</span></span>
<span data-ttu-id="ad413-103">修改本機網路閘道。</span><span class="sxs-lookup"><span data-stu-id="ad413-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad413-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad413-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad413-105">說明</span><span class="sxs-lookup"><span data-stu-id="ad413-105">DESCRIPTION</span></span>
<span data-ttu-id="ad413-106">**AzureRmLocalNetworkGateway** Cmdlet 會修改本機網路閘道。</span><span class="sxs-lookup"><span data-stu-id="ad413-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="ad413-107">示例</span><span class="sxs-lookup"><span data-stu-id="ad413-107">EXAMPLES</span></span>

### <span data-ttu-id="ad413-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ad413-108">Example 1</span></span>
<span data-ttu-id="ad413-109">設定現有閘道的配置</span><span class="sxs-lookup"><span data-stu-id="ad413-109">Set configuration for an existing gateway</span></span>


```
$lgw = Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway $lgw

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

## <span data-ttu-id="ad413-110">參數</span><span class="sxs-lookup"><span data-stu-id="ad413-110">PARAMETERS</span></span>

### <span data-ttu-id="ad413-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ad413-111">-AddressPrefix</span></span>
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

### <span data-ttu-id="ad413-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad413-112">-AsJob</span></span>
<span data-ttu-id="ad413-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad413-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad413-114">-Asn</span><span class="sxs-lookup"><span data-stu-id="ad413-114">-Asn</span></span>
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

### <span data-ttu-id="ad413-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="ad413-115">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="ad413-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad413-116">-DefaultProfile</span></span>
<span data-ttu-id="ad413-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad413-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad413-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad413-118">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="ad413-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="ad413-119">-PeerWeight</span></span>
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

### <span data-ttu-id="ad413-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad413-120">CommonParameters</span></span>
<span data-ttu-id="ad413-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad413-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad413-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad413-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad413-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ad413-123">INPUTS</span></span>

### <span data-ttu-id="ad413-124">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ad413-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>
<span data-ttu-id="ad413-125">參數： LocalNetworkGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ad413-125">Parameters: LocalNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="ad413-126">[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ad413-126">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ad413-127">UInt32</span><span class="sxs-lookup"><span data-stu-id="ad413-127">System.UInt32</span></span>

### <span data-ttu-id="ad413-128">System.object</span><span class="sxs-lookup"><span data-stu-id="ad413-128">System.String</span></span>

### <span data-ttu-id="ad413-129">System.object</span><span class="sxs-lookup"><span data-stu-id="ad413-129">System.Int32</span></span>

## <span data-ttu-id="ad413-130">輸出</span><span class="sxs-lookup"><span data-stu-id="ad413-130">OUTPUTS</span></span>

### <span data-ttu-id="ad413-131">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ad413-131">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="ad413-132">筆記</span><span class="sxs-lookup"><span data-stu-id="ad413-132">NOTES</span></span>

## <span data-ttu-id="ad413-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad413-133">RELATED LINKS</span></span>

[<span data-ttu-id="ad413-134">AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad413-134">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="ad413-135">新-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad413-135">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="ad413-136">移除-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad413-136">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


