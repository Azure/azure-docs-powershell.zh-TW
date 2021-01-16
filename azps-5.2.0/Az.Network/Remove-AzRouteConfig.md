---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: 57ef72599cdb0500a9903aeb09f67437fe5cc2f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279981"
---
# <span data-ttu-id="ddb30-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ddb30-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="ddb30-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ddb30-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb30-103">從路由表中移除路由。</span><span class="sxs-lookup"><span data-stu-id="ddb30-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="ddb30-104">句法</span><span class="sxs-lookup"><span data-stu-id="ddb30-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddb30-105">說明</span><span class="sxs-lookup"><span data-stu-id="ddb30-105">DESCRIPTION</span></span>
<span data-ttu-id="ddb30-106">**AzRouteConfig** Cmdlet 會從 Azure 路由表中移除路由。</span><span class="sxs-lookup"><span data-stu-id="ddb30-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="ddb30-107">示例</span><span class="sxs-lookup"><span data-stu-id="ddb30-107">EXAMPLES</span></span>

### <span data-ttu-id="ddb30-108">範例1：移除路線</span><span class="sxs-lookup"><span data-stu-id="ddb30-108">Example 1: Remove a route</span></span>
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

<span data-ttu-id="ddb30-109">這個命令會使用 **AzRouteTable** Cmdlet 取得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="ddb30-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="ddb30-110">命令會使用管線運算子，將該表傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddb30-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ddb30-111">目前的 Cmdlet 會移除名為 Route02 的路由，並將結果傳遞到 **AzRouteTable** Cmdlet，這會更新資料表以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="ddb30-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="ddb30-112">該表不再包含名為 Route02 的路由。</span><span class="sxs-lookup"><span data-stu-id="ddb30-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="ddb30-113">參數</span><span class="sxs-lookup"><span data-stu-id="ddb30-113">PARAMETERS</span></span>

### <span data-ttu-id="ddb30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb30-114">-DefaultProfile</span></span>
<span data-ttu-id="ddb30-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ddb30-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddb30-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ddb30-116">-Name</span></span>
<span data-ttu-id="ddb30-117">指定此 Cmdlet 移除之路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddb30-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ddb30-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="ddb30-118">-RouteTable</span></span>
<span data-ttu-id="ddb30-119">指定包含此 Cmdlet 刪除之路由的路由表。</span><span class="sxs-lookup"><span data-stu-id="ddb30-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="ddb30-120">-確認</span><span class="sxs-lookup"><span data-stu-id="ddb30-120">-Confirm</span></span>
<span data-ttu-id="ddb30-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ddb30-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddb30-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddb30-122">-WhatIf</span></span>
<span data-ttu-id="ddb30-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ddb30-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddb30-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddb30-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddb30-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb30-125">CommonParameters</span></span>
<span data-ttu-id="ddb30-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ddb30-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb30-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ddb30-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb30-128">輸入</span><span class="sxs-lookup"><span data-stu-id="ddb30-128">INPUTS</span></span>

### <span data-ttu-id="ddb30-129">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ddb30-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="ddb30-130">輸出</span><span class="sxs-lookup"><span data-stu-id="ddb30-130">OUTPUTS</span></span>

### <span data-ttu-id="ddb30-131">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ddb30-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="ddb30-132">筆記</span><span class="sxs-lookup"><span data-stu-id="ddb30-132">NOTES</span></span>

## <span data-ttu-id="ddb30-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddb30-133">RELATED LINKS</span></span>

[<span data-ttu-id="ddb30-134">附加 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ddb30-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="ddb30-135">AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ddb30-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="ddb30-136">新-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ddb30-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="ddb30-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ddb30-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


