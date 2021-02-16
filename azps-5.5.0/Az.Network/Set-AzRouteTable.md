---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
ms.openlocfilehash: bd419d3b6ec55af885a0f05b7be5c5de269fccdd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135687"
---
# <span data-ttu-id="0c5a6-101">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="0c5a6-101">Set-AzRouteTable</span></span>

## <span data-ttu-id="0c5a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c5a6-102">SYNOPSIS</span></span>
<span data-ttu-id="0c5a6-103">更新路由表。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-103">Updates a route table.</span></span>

## <span data-ttu-id="0c5a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c5a6-104">SYNTAX</span></span>

```
Set-AzRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c5a6-105">說明</span><span class="sxs-lookup"><span data-stu-id="0c5a6-105">DESCRIPTION</span></span>
<span data-ttu-id="0c5a6-106">**AzRouteTable** Cmdlet 會更新路由表。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-106">The **Set-AzRouteTable** cmdlet updates a route table.</span></span>

## <span data-ttu-id="0c5a6-107">示例</span><span class="sxs-lookup"><span data-stu-id="0c5a6-107">EXAMPLES</span></span>

### <span data-ttu-id="0c5a6-108">範例1：透過新增路由設定來更新路由資料表</span><span class="sxs-lookup"><span data-stu-id="0c5a6-108">Example 1: Update a route table by adding route configuration to it</span></span>
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

<span data-ttu-id="0c5a6-109">這個命令會使用 Get-AzRouteTable Cmdlet 來取得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-109">This command gets the route table named RouteTable01 by using Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="0c5a6-110">命令會使用管線運算子，將該表傳到 Add-AzRouteConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-110">The command passes that table to the Add-AzRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0c5a6-111">**AzRouteConfig** 會新增名為 Route07 的路由，然後將結果傳遞到目前的 Cmdlet，這會更新資料表以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-111">**Add-AzRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

### <span data-ttu-id="0c5a6-112">範例2：修改路由資料表</span><span class="sxs-lookup"><span data-stu-id="0c5a6-112">Example 2: Modify route table</span></span>

```
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
False
PS C:\> $rt.DisableBgpRoutePropagation = $true
PS C:\> Set-AzRouteTable -RouteTable $rt
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
True
```

<span data-ttu-id="0c5a6-113">第一個命令會取得名為 rtName 的路由資料表，並將它儲存在 $rt 變數中。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-113">The first command gets the route table named rtName and stores it in the $rt variable.</span></span>
<span data-ttu-id="0c5a6-114">第二個命令會顯示 DisableBgpRoutePropagation 的值。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-114">The second command displays the value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="0c5a6-115">第三個命令更新 DisableBgpRoutePropagation 的值。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-115">The third command updates value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="0c5a6-116">第四個命令會補救伺服器上的路由表。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-116">The fourth command updates route table on the server.</span></span>
<span data-ttu-id="0c5a6-117">第五個命令會取得更新的路由資料表，並將它儲存在 $rt 變數中。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-117">The fifth command gets updated route table and stores it in the $rt variable.</span></span>
<span data-ttu-id="0c5a6-118">第六個命令會顯示 DisableBgpRoutePropagation 的值。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-118">The sixth command displays the value of DisableBgpRoutePropagation.</span></span>

## <span data-ttu-id="0c5a6-119">參數</span><span class="sxs-lookup"><span data-stu-id="0c5a6-119">PARAMETERS</span></span>

### <span data-ttu-id="0c5a6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c5a6-120">-AsJob</span></span>
<span data-ttu-id="0c5a6-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0c5a6-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c5a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c5a6-122">-DefaultProfile</span></span>
<span data-ttu-id="0c5a6-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c5a6-124">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="0c5a6-124">-RouteTable</span></span>
<span data-ttu-id="0c5a6-125">指定代表路由資料表應該設定之狀態的路由資料表物件。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-125">Specifies a route table object representing the state to which the route table should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c5a6-126">-確認</span><span class="sxs-lookup"><span data-stu-id="0c5a6-126">-Confirm</span></span>
<span data-ttu-id="0c5a6-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c5a6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c5a6-128">-WhatIf</span></span>
<span data-ttu-id="0c5a6-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c5a6-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c5a6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c5a6-131">CommonParameters</span></span>
<span data-ttu-id="0c5a6-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c5a6-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0c5a6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c5a6-134">輸入</span><span class="sxs-lookup"><span data-stu-id="0c5a6-134">INPUTS</span></span>

### <span data-ttu-id="0c5a6-135">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0c5a6-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="0c5a6-136">輸出</span><span class="sxs-lookup"><span data-stu-id="0c5a6-136">OUTPUTS</span></span>

### <span data-ttu-id="0c5a6-137">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0c5a6-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="0c5a6-138">筆記</span><span class="sxs-lookup"><span data-stu-id="0c5a6-138">NOTES</span></span>

## <span data-ttu-id="0c5a6-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c5a6-139">RELATED LINKS</span></span>

[<span data-ttu-id="0c5a6-140">附加 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0c5a6-140">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="0c5a6-141">AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="0c5a6-141">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="0c5a6-142">新-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="0c5a6-142">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="0c5a6-143">移除-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="0c5a6-143">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)


