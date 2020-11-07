---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteTable.md
ms.openlocfilehash: 531c2724289e90f92bf14347518d53b6208be932
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795387"
---
# <span data-ttu-id="c3fc8-101">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3fc8-101">Set-AzRouteTable</span></span>

## <span data-ttu-id="c3fc8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="c3fc8-103">設定路由資料表的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="c3fc8-103">Sets the goal state for a route table.</span></span>

## <span data-ttu-id="c3fc8-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3fc8-104">SYNTAX</span></span>

```
Set-AzRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3fc8-105">說明</span><span class="sxs-lookup"><span data-stu-id="c3fc8-105">DESCRIPTION</span></span>
<span data-ttu-id="c3fc8-106">**AzRouteTable** Cmdlet 會設定 Azure 路由資料表的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="c3fc8-106">The **Set-AzRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="c3fc8-107">示例</span><span class="sxs-lookup"><span data-stu-id="c3fc8-107">EXAMPLES</span></span>

### <span data-ttu-id="c3fc8-108">範例1：新增路線，然後設定路由資料表的目標狀態</span><span class="sxs-lookup"><span data-stu-id="c3fc8-108">Example 1: Add a route and then set the goal state of the route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="c3fc8-109">這個命令會使用 Get-AzRouteTable Cmdlet 來取得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="c3fc8-109">This command gets the route table named RouteTable01 by using Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="c3fc8-110">命令會使用管線運算子，將該表傳到 Add-AzRouteConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3fc8-110">The command passes that table to the Add-AzRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c3fc8-111">**AzRouteConfig** 會新增名為 Route07 的路由，然後將結果傳遞到目前的 Cmdlet，這會更新資料表以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="c3fc8-111">**Add-AzRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="c3fc8-112">參數</span><span class="sxs-lookup"><span data-stu-id="c3fc8-112">PARAMETERS</span></span>

### <span data-ttu-id="c3fc8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3fc8-113">-AsJob</span></span>
<span data-ttu-id="c3fc8-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c3fc8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3fc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3fc8-115">-DefaultProfile</span></span>
<span data-ttu-id="c3fc8-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3fc8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3fc8-117">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c3fc8-117">-RouteTable</span></span>
<span data-ttu-id="c3fc8-118">指定代表此 Cmdlet 設定路由資料表之目標狀態的路由資料表物件。</span><span class="sxs-lookup"><span data-stu-id="c3fc8-118">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3fc8-119">-確認</span><span class="sxs-lookup"><span data-stu-id="c3fc8-119">-Confirm</span></span>
<span data-ttu-id="c3fc8-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c3fc8-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fc8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3fc8-121">-WhatIf</span></span>
<span data-ttu-id="c3fc8-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c3fc8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3fc8-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3fc8-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fc8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3fc8-124">CommonParameters</span></span>
<span data-ttu-id="c3fc8-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3fc8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3fc8-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3fc8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3fc8-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c3fc8-127">INPUTS</span></span>

### <span data-ttu-id="c3fc8-128">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3fc8-128">PSRouteTable</span></span>
<span data-ttu-id="c3fc8-129">形參 "RouteTable" 接受管線中 "PSRouteTable" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c3fc8-129">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="c3fc8-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c3fc8-130">OUTPUTS</span></span>

### <span data-ttu-id="c3fc8-131">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c3fc8-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c3fc8-132">筆記</span><span class="sxs-lookup"><span data-stu-id="c3fc8-132">NOTES</span></span>

## <span data-ttu-id="c3fc8-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3fc8-133">RELATED LINKS</span></span>

[<span data-ttu-id="c3fc8-134">附加 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c3fc8-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="c3fc8-135">AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3fc8-135">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="c3fc8-136">新-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3fc8-136">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="c3fc8-137">移除-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3fc8-137">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)


