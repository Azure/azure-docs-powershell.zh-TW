---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 0d941289f0798854a3647bcb5fbf4d1e6be1053d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126484"
---
# <span data-ttu-id="c0621-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c0621-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="c0621-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0621-102">SYNOPSIS</span></span>
<span data-ttu-id="c0621-103">從路由資料表取得路由。</span><span class="sxs-lookup"><span data-stu-id="c0621-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="c0621-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0621-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0621-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0621-105">DESCRIPTION</span></span>
<span data-ttu-id="c0621-106">**AzRouteConfig** Cmdlet 會從 Azure 路由表取得路由。</span><span class="sxs-lookup"><span data-stu-id="c0621-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="c0621-107">您可以依名稱指定路由。</span><span class="sxs-lookup"><span data-stu-id="c0621-107">You can specify a route by name.</span></span>

## <span data-ttu-id="c0621-108">示例</span><span class="sxs-lookup"><span data-stu-id="c0621-108">EXAMPLES</span></span>

### <span data-ttu-id="c0621-109">範例1：取得路由資料表</span><span class="sxs-lookup"><span data-stu-id="c0621-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="c0621-110">這個命令會使用 **AzRouteTable** Cmdlet 取得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="c0621-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="c0621-111">命令會使用管線運算子，將該表傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0621-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c0621-112">目前的 Cmdlet 會在路由表中取得名為 RouteTable01 的名為 Route07 的路由。</span><span class="sxs-lookup"><span data-stu-id="c0621-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="c0621-113">參數</span><span class="sxs-lookup"><span data-stu-id="c0621-113">PARAMETERS</span></span>

### <span data-ttu-id="c0621-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0621-114">-DefaultProfile</span></span>
<span data-ttu-id="c0621-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0621-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0621-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0621-116">-Name</span></span>
<span data-ttu-id="c0621-117">指定此 Cmdlet 所取得之路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0621-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c0621-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c0621-118">-RouteTable</span></span>
<span data-ttu-id="c0621-119">指定由此 Cmdlet 取得路由的路由表。</span><span class="sxs-lookup"><span data-stu-id="c0621-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="c0621-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0621-120">CommonParameters</span></span>
<span data-ttu-id="c0621-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0621-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0621-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c0621-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0621-123">輸入</span><span class="sxs-lookup"><span data-stu-id="c0621-123">INPUTS</span></span>

### <span data-ttu-id="c0621-124">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c0621-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c0621-125">輸出</span><span class="sxs-lookup"><span data-stu-id="c0621-125">OUTPUTS</span></span>

### <span data-ttu-id="c0621-126">PSRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c0621-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="c0621-127">筆記</span><span class="sxs-lookup"><span data-stu-id="c0621-127">NOTES</span></span>

## <span data-ttu-id="c0621-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0621-128">RELATED LINKS</span></span>

[<span data-ttu-id="c0621-129">附加 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c0621-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="c0621-130">AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c0621-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="c0621-131">新-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c0621-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="c0621-132">移除-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c0621-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="c0621-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c0621-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


