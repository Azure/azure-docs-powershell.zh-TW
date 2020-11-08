---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127032"
---
# <span data-ttu-id="ca536-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ca536-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="ca536-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca536-102">SYNOPSIS</span></span>
<span data-ttu-id="ca536-103">取得 ExpressRoute 交叉連接對等設定。</span><span class="sxs-lookup"><span data-stu-id="ca536-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="ca536-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca536-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca536-105">說明</span><span class="sxs-lookup"><span data-stu-id="ca536-105">DESCRIPTION</span></span>
<span data-ttu-id="ca536-106">**AzExpressRouteCrossConnectionPeering** Cmdlet 會針對 ExpressRoute 交叉連線檢索對等關係的設定。</span><span class="sxs-lookup"><span data-stu-id="ca536-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="ca536-107">示例</span><span class="sxs-lookup"><span data-stu-id="ca536-107">EXAMPLES</span></span>

### <span data-ttu-id="ca536-108">範例1：顯示 ExpressRoute 交叉連線的對等設定</span><span class="sxs-lookup"><span data-stu-id="ca536-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="ca536-109">參數</span><span class="sxs-lookup"><span data-stu-id="ca536-109">PARAMETERS</span></span>

### <span data-ttu-id="ca536-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca536-110">-DefaultProfile</span></span>
<span data-ttu-id="ca536-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca536-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca536-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ca536-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="ca536-113">包含對等設定的 ExpressRoute 交叉連線物件。</span><span class="sxs-lookup"><span data-stu-id="ca536-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca536-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca536-114">-Name</span></span>
<span data-ttu-id="ca536-115">要檢索之對等配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca536-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="ca536-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca536-116">CommonParameters</span></span>
<span data-ttu-id="ca536-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca536-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca536-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ca536-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca536-119">輸入</span><span class="sxs-lookup"><span data-stu-id="ca536-119">INPUTS</span></span>

### <span data-ttu-id="ca536-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ca536-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="ca536-121">形參 "ExpressRouteCrossConnection" 接受管線中 "PSExpressRouteCrossConnection" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ca536-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="ca536-122">輸出</span><span class="sxs-lookup"><span data-stu-id="ca536-122">OUTPUTS</span></span>

### <span data-ttu-id="ca536-123">PSPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ca536-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="ca536-124">筆記</span><span class="sxs-lookup"><span data-stu-id="ca536-124">NOTES</span></span>

## <span data-ttu-id="ca536-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca536-125">RELATED LINKS</span></span>

[<span data-ttu-id="ca536-126">附加 AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ca536-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ca536-127">移除-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ca536-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ca536-128">AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ca536-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="ca536-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ca536-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
