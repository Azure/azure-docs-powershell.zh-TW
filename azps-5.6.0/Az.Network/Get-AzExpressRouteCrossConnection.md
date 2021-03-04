---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 6561037b9174fd732d616f425324c164529e6367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905877"
---
# <span data-ttu-id="7e7d2-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7e7d2-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="7e7d2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7e7d2-102">SYNOPSIS</span></span>
<span data-ttu-id="7e7d2-103">從 Azure 獲得 Azure ExpressRoute 交叉連接。</span><span class="sxs-lookup"><span data-stu-id="7e7d2-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="7e7d2-104">語法</span><span class="sxs-lookup"><span data-stu-id="7e7d2-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e7d2-105">描述</span><span class="sxs-lookup"><span data-stu-id="7e7d2-105">DESCRIPTION</span></span>
<span data-ttu-id="7e7d2-106">**Get-AzExpressRouteCrossConnection** Cmdlet 可用來從訂閱中取回 ExpressRoute 交叉連線物件。</span><span class="sxs-lookup"><span data-stu-id="7e7d2-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="7e7d2-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7e7d2-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="7e7d2-108">例子</span><span class="sxs-lookup"><span data-stu-id="7e7d2-108">EXAMPLES</span></span>

### <span data-ttu-id="7e7d2-109">範例 1：取得 ExpressRoute 交叉連接</span><span class="sxs-lookup"><span data-stu-id="7e7d2-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="7e7d2-110">範例 2：使用篩選列出 ExpressRoute 交叉連接</span><span class="sxs-lookup"><span data-stu-id="7e7d2-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="7e7d2-111">此 Cmdlet 會列出以「測試」開頭的所有 ExpressRoute 交叉連接</span><span class="sxs-lookup"><span data-stu-id="7e7d2-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="7e7d2-112">參數</span><span class="sxs-lookup"><span data-stu-id="7e7d2-112">PARAMETERS</span></span>

### <span data-ttu-id="7e7d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e7d2-113">-DefaultProfile</span></span>
<span data-ttu-id="7e7d2-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e7d2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e7d2-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e7d2-115">-Name</span></span>
<span data-ttu-id="7e7d2-116">ExpressRoute 交叉連接的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e7d2-116">The name of the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7e7d2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e7d2-117">-ResourceGroupName</span></span>
<span data-ttu-id="7e7d2-118">包含 ExpressRoute 交叉連接的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7e7d2-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7e7d2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e7d2-119">CommonParameters</span></span>
<span data-ttu-id="7e7d2-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7e7d2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e7d2-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e7d2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e7d2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7e7d2-122">INPUTS</span></span>

### <span data-ttu-id="7e7d2-123">沒有</span><span class="sxs-lookup"><span data-stu-id="7e7d2-123">None</span></span>
<span data-ttu-id="7e7d2-124">此 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="7e7d2-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e7d2-125">輸出</span><span class="sxs-lookup"><span data-stu-id="7e7d2-125">OUTPUTS</span></span>

### <span data-ttu-id="7e7d2-126">Microsoft.Azure.Commands.Network.models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7e7d2-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="7e7d2-127">筆記</span><span class="sxs-lookup"><span data-stu-id="7e7d2-127">NOTES</span></span>

## <span data-ttu-id="7e7d2-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e7d2-128">RELATED LINKS</span></span>

[<span data-ttu-id="7e7d2-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7e7d2-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)