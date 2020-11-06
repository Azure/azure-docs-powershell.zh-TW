---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: a33fb510e351a8f1c762801947cf4bbac9a66e28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451360"
---
# <span data-ttu-id="906d5-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="906d5-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="906d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="906d5-102">SYNOPSIS</span></span>
<span data-ttu-id="906d5-103">修改本機網路閘道。</span><span class="sxs-lookup"><span data-stu-id="906d5-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="906d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="906d5-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="906d5-105">說明</span><span class="sxs-lookup"><span data-stu-id="906d5-105">DESCRIPTION</span></span>
<span data-ttu-id="906d5-106">**AzureRmLocalNetworkGateway** Cmdlet 會修改本機網路閘道。</span><span class="sxs-lookup"><span data-stu-id="906d5-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="906d5-107">示例</span><span class="sxs-lookup"><span data-stu-id="906d5-107">EXAMPLES</span></span>

## <span data-ttu-id="906d5-108">參數</span><span class="sxs-lookup"><span data-stu-id="906d5-108">PARAMETERS</span></span>

### <span data-ttu-id="906d5-109">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="906d5-109">-AddressPrefix</span></span>
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

### <span data-ttu-id="906d5-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="906d5-110">-AsJob</span></span>
<span data-ttu-id="906d5-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="906d5-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="906d5-112">-Asn</span><span class="sxs-lookup"><span data-stu-id="906d5-112">-Asn</span></span>
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

### <span data-ttu-id="906d5-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="906d5-113">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="906d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="906d5-114">-DefaultProfile</span></span>
<span data-ttu-id="906d5-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="906d5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="906d5-116">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="906d5-116">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="906d5-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="906d5-117">-PeerWeight</span></span>
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

### <span data-ttu-id="906d5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="906d5-118">CommonParameters</span></span>
<span data-ttu-id="906d5-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="906d5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="906d5-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="906d5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="906d5-121">輸入</span><span class="sxs-lookup"><span data-stu-id="906d5-121">INPUTS</span></span>

### <span data-ttu-id="906d5-122">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="906d5-122">PSLocalNetworkGateway</span></span>
<span data-ttu-id="906d5-123">形參 "LocalNetworkGateway" 接受管線中 "PSLocalNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="906d5-123">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="906d5-124">輸出</span><span class="sxs-lookup"><span data-stu-id="906d5-124">OUTPUTS</span></span>

### <span data-ttu-id="906d5-125">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="906d5-125">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="906d5-126">筆記</span><span class="sxs-lookup"><span data-stu-id="906d5-126">NOTES</span></span>

## <span data-ttu-id="906d5-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="906d5-127">RELATED LINKS</span></span>

[<span data-ttu-id="906d5-128">AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="906d5-128">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="906d5-129">新-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="906d5-129">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="906d5-130">移除-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="906d5-130">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


