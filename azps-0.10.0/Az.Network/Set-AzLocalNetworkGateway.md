---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: 61e2fd8a4f6c073bbb900586b0d73dec97c3b662
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795413"
---
# <span data-ttu-id="86774-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86774-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="86774-102">摘要</span><span class="sxs-lookup"><span data-stu-id="86774-102">SYNOPSIS</span></span>
<span data-ttu-id="86774-103">修改本機網路閘道。</span><span class="sxs-lookup"><span data-stu-id="86774-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="86774-104">句法</span><span class="sxs-lookup"><span data-stu-id="86774-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86774-105">說明</span><span class="sxs-lookup"><span data-stu-id="86774-105">DESCRIPTION</span></span>
<span data-ttu-id="86774-106">**AzLocalNetworkGateway** Cmdlet 會修改本機網路閘道。</span><span class="sxs-lookup"><span data-stu-id="86774-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="86774-107">示例</span><span class="sxs-lookup"><span data-stu-id="86774-107">EXAMPLES</span></span>

### <span data-ttu-id="86774-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="86774-108">1:</span></span>
```

```

## <span data-ttu-id="86774-109">參數</span><span class="sxs-lookup"><span data-stu-id="86774-109">PARAMETERS</span></span>

### <span data-ttu-id="86774-110">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="86774-110">-AddressPrefix</span></span>
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

### <span data-ttu-id="86774-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86774-111">-AsJob</span></span>
<span data-ttu-id="86774-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="86774-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86774-113">-Asn</span><span class="sxs-lookup"><span data-stu-id="86774-113">-Asn</span></span>
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

### <span data-ttu-id="86774-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="86774-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="86774-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86774-115">-DefaultProfile</span></span>
<span data-ttu-id="86774-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="86774-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86774-117">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86774-117">-LocalNetworkGateway</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86774-118">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="86774-118">-PeerWeight</span></span>
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

### <span data-ttu-id="86774-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86774-119">CommonParameters</span></span>
<span data-ttu-id="86774-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="86774-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86774-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="86774-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86774-122">輸入</span><span class="sxs-lookup"><span data-stu-id="86774-122">INPUTS</span></span>

### <span data-ttu-id="86774-123">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86774-123">PSLocalNetworkGateway</span></span>
<span data-ttu-id="86774-124">形參 "LocalNetworkGateway" 接受管線中 "PSLocalNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="86774-124">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="86774-125">輸出</span><span class="sxs-lookup"><span data-stu-id="86774-125">OUTPUTS</span></span>

### <span data-ttu-id="86774-126">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="86774-126">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="86774-127">筆記</span><span class="sxs-lookup"><span data-stu-id="86774-127">NOTES</span></span>

## <span data-ttu-id="86774-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="86774-128">RELATED LINKS</span></span>

[<span data-ttu-id="86774-129">AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86774-129">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="86774-130">新-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86774-130">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="86774-131">移除-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86774-131">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)


