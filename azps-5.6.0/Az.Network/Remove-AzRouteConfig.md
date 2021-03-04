---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: e48da3a5f300d39051a9d1b07e9789855ed7dca1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913373"
---
# <span data-ttu-id="587fb-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="587fb-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="587fb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="587fb-102">SYNOPSIS</span></span>
<span data-ttu-id="587fb-103">從路由資料表移除路由。</span><span class="sxs-lookup"><span data-stu-id="587fb-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="587fb-104">語法</span><span class="sxs-lookup"><span data-stu-id="587fb-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="587fb-105">描述</span><span class="sxs-lookup"><span data-stu-id="587fb-105">DESCRIPTION</span></span>
<span data-ttu-id="587fb-106">**Remove-AzRouteConfig** Cmdlet 會從 Azure 路由資料表移除路由。</span><span class="sxs-lookup"><span data-stu-id="587fb-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="587fb-107">例子</span><span class="sxs-lookup"><span data-stu-id="587fb-107">EXAMPLES</span></span>

### <span data-ttu-id="587fb-108">範例 1：移除路由</span><span class="sxs-lookup"><span data-stu-id="587fb-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzRouteConfig -Name "Route02" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="587fb-109">此命令會使用 **Get-AzRouteTable Cmdlet** 取得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="587fb-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="587fb-110">該命令會使用管線運算子，將表格傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="587fb-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="587fb-111">目前的 Cmdlet 會移除名為 Route02 的路由，且會將結果傳遞至 **Set-AzRouteTable** Cmdlet，此 Cmdlet 會更新資料表以反映您的變更。</span><span class="sxs-lookup"><span data-stu-id="587fb-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="587fb-112">資料表不再包含名為 Route02 的路由。</span><span class="sxs-lookup"><span data-stu-id="587fb-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="587fb-113">參數</span><span class="sxs-lookup"><span data-stu-id="587fb-113">PARAMETERS</span></span>

### <span data-ttu-id="587fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="587fb-114">-DefaultProfile</span></span>
<span data-ttu-id="587fb-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="587fb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="587fb-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="587fb-116">-Name</span></span>
<span data-ttu-id="587fb-117">指定此 Cmdlet 移除的路由名稱。</span><span class="sxs-lookup"><span data-stu-id="587fb-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="587fb-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="587fb-118">-RouteTable</span></span>
<span data-ttu-id="587fb-119">指定包含此 Cmdlet 刪除之路由的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="587fb-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="587fb-120">-確認</span><span class="sxs-lookup"><span data-stu-id="587fb-120">-Confirm</span></span>
<span data-ttu-id="587fb-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="587fb-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="587fb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="587fb-122">-WhatIf</span></span>
<span data-ttu-id="587fb-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="587fb-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="587fb-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="587fb-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="587fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="587fb-125">CommonParameters</span></span>
<span data-ttu-id="587fb-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="587fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="587fb-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="587fb-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="587fb-128">輸入</span><span class="sxs-lookup"><span data-stu-id="587fb-128">INPUTS</span></span>

### <span data-ttu-id="587fb-129">Microsoft.Azure.Commands.Network.models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="587fb-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="587fb-130">輸出</span><span class="sxs-lookup"><span data-stu-id="587fb-130">OUTPUTS</span></span>

### <span data-ttu-id="587fb-131">Microsoft.Azure.Commands.Network.models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="587fb-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="587fb-132">筆記</span><span class="sxs-lookup"><span data-stu-id="587fb-132">NOTES</span></span>

## <span data-ttu-id="587fb-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="587fb-133">RELATED LINKS</span></span>

[<span data-ttu-id="587fb-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="587fb-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="587fb-135">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="587fb-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="587fb-136">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="587fb-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="587fb-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="587fb-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


