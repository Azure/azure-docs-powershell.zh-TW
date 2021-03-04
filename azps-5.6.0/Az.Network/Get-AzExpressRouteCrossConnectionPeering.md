---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 415c084ebf6c1c83872a16d01ce4eb556f688103
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908826"
---
# <span data-ttu-id="db950-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="db950-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="db950-102">簡介</span><span class="sxs-lookup"><span data-stu-id="db950-102">SYNOPSIS</span></span>
<span data-ttu-id="db950-103">獲得 ExpressRoute 交叉連接對等互連組。</span><span class="sxs-lookup"><span data-stu-id="db950-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="db950-104">語法</span><span class="sxs-lookup"><span data-stu-id="db950-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db950-105">描述</span><span class="sxs-lookup"><span data-stu-id="db950-105">DESCRIPTION</span></span>
<span data-ttu-id="db950-106">**Get-AzExpressRouteCrossConnectionPeering** Cmdlet 會針對 ExpressRoute 交叉連接，取得對等互連關係的組式。</span><span class="sxs-lookup"><span data-stu-id="db950-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="db950-107">例子</span><span class="sxs-lookup"><span data-stu-id="db950-107">EXAMPLES</span></span>

### <span data-ttu-id="db950-108">範例 1：顯示 ExpressRoute 交叉連接的對等組</span><span class="sxs-lookup"><span data-stu-id="db950-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="db950-109">參數</span><span class="sxs-lookup"><span data-stu-id="db950-109">PARAMETERS</span></span>

### <span data-ttu-id="db950-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db950-110">-DefaultProfile</span></span>
<span data-ttu-id="db950-111">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="db950-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db950-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="db950-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="db950-113">包含對等配置的 ExpressRoute 交叉連線物件。</span><span class="sxs-lookup"><span data-stu-id="db950-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

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

### <span data-ttu-id="db950-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="db950-114">-Name</span></span>
<span data-ttu-id="db950-115">要取取的對等組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="db950-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="db950-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db950-116">CommonParameters</span></span>
<span data-ttu-id="db950-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="db950-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db950-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db950-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db950-119">輸入</span><span class="sxs-lookup"><span data-stu-id="db950-119">INPUTS</span></span>

### <span data-ttu-id="db950-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="db950-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="db950-121">參數 'ExpressRouteCrossConnection' 接受來自管線之類型 'PSExpressRouteCrossConnection'的值</span><span class="sxs-lookup"><span data-stu-id="db950-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="db950-122">輸出</span><span class="sxs-lookup"><span data-stu-id="db950-122">OUTPUTS</span></span>

### <span data-ttu-id="db950-123">Microsoft.Azure.Commands.Network.models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="db950-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="db950-124">筆記</span><span class="sxs-lookup"><span data-stu-id="db950-124">NOTES</span></span>

## <span data-ttu-id="db950-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="db950-125">RELATED LINKS</span></span>

[<span data-ttu-id="db950-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="db950-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="db950-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="db950-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="db950-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="db950-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="db950-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="db950-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
