---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 892d160decb7bc595e25f2f0512996fe2bdce5da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902446"
---
# <span data-ttu-id="73f9a-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="73f9a-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="73f9a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="73f9a-102">SYNOPSIS</span></span>
<span data-ttu-id="73f9a-103">從路由資料表獲得路由。</span><span class="sxs-lookup"><span data-stu-id="73f9a-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="73f9a-104">語法</span><span class="sxs-lookup"><span data-stu-id="73f9a-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73f9a-105">描述</span><span class="sxs-lookup"><span data-stu-id="73f9a-105">DESCRIPTION</span></span>
<span data-ttu-id="73f9a-106">**Get-AzRouteConfig** Cmdlet 會從 Azure 路由資料表取得路由。</span><span class="sxs-lookup"><span data-stu-id="73f9a-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="73f9a-107">您可以根據名稱指定路由。</span><span class="sxs-lookup"><span data-stu-id="73f9a-107">You can specify a route by name.</span></span>

## <span data-ttu-id="73f9a-108">例子</span><span class="sxs-lookup"><span data-stu-id="73f9a-108">EXAMPLES</span></span>

### <span data-ttu-id="73f9a-109">範例 1：取得路由資料表</span><span class="sxs-lookup"><span data-stu-id="73f9a-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="73f9a-110">此命令會使用 **Get-AzRouteTable Cmdlet** 取得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="73f9a-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="73f9a-111">該命令會使用管線運算子，將表格傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73f9a-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="73f9a-112">目前的 Cmdlet 在名為 RouteTable01 的路由資料表中，會獲得名為 Route07 的路由。</span><span class="sxs-lookup"><span data-stu-id="73f9a-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="73f9a-113">參數</span><span class="sxs-lookup"><span data-stu-id="73f9a-113">PARAMETERS</span></span>

### <span data-ttu-id="73f9a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f9a-114">-DefaultProfile</span></span>
<span data-ttu-id="73f9a-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="73f9a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73f9a-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="73f9a-116">-Name</span></span>
<span data-ttu-id="73f9a-117">指定此 Cmdlet 所獲得路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="73f9a-117">Specifies the name of the route that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f9a-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="73f9a-118">-RouteTable</span></span>
<span data-ttu-id="73f9a-119">指定此 Cmdlet 從哪個路由資料表獲得路由。</span><span class="sxs-lookup"><span data-stu-id="73f9a-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73f9a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f9a-120">CommonParameters</span></span>
<span data-ttu-id="73f9a-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="73f9a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f9a-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73f9a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f9a-123">輸入</span><span class="sxs-lookup"><span data-stu-id="73f9a-123">INPUTS</span></span>

### <span data-ttu-id="73f9a-124">Microsoft.Azure.Commands.Network.models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="73f9a-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="73f9a-125">輸出</span><span class="sxs-lookup"><span data-stu-id="73f9a-125">OUTPUTS</span></span>

### <span data-ttu-id="73f9a-126">Microsoft.Azure.Commands.Network.models.PSRoute</span><span class="sxs-lookup"><span data-stu-id="73f9a-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="73f9a-127">筆記</span><span class="sxs-lookup"><span data-stu-id="73f9a-127">NOTES</span></span>

## <span data-ttu-id="73f9a-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="73f9a-128">RELATED LINKS</span></span>

[<span data-ttu-id="73f9a-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="73f9a-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="73f9a-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="73f9a-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="73f9a-131">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="73f9a-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="73f9a-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="73f9a-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="73f9a-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="73f9a-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


