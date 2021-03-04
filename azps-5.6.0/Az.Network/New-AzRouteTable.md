---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: 2c001da52c50f89aedea12b6049bce3ae5c42d44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909505"
---
# <span data-ttu-id="c6316-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c6316-101">New-AzRouteTable</span></span>

## <span data-ttu-id="c6316-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6316-102">SYNOPSIS</span></span>
<span data-ttu-id="c6316-103">建立路由資料表。</span><span class="sxs-lookup"><span data-stu-id="c6316-103">Creates a route table.</span></span>

## <span data-ttu-id="c6316-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6316-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6316-105">描述</span><span class="sxs-lookup"><span data-stu-id="c6316-105">DESCRIPTION</span></span>
<span data-ttu-id="c6316-106">**New-AzRouteTable** Cmdlet 會建立 Azure 路由資料表。</span><span class="sxs-lookup"><span data-stu-id="c6316-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="c6316-107">例子</span><span class="sxs-lookup"><span data-stu-id="c6316-107">EXAMPLES</span></span>

### <span data-ttu-id="c6316-108">範例 1：建立包含路由的路由資料表</span><span class="sxs-lookup"><span data-stu-id="c6316-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/myroutetable
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              :
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null,
                        "ProvisioningState": "Succeeded"
                      }
                    ]
Subnets           : []
```

<span data-ttu-id="c6316-109">第一個命令會使用 New-AzRouteConfig Cmdlet 建立名為 Route07 的路由，然後將它儲存在 $Route 變數中。</span><span class="sxs-lookup"><span data-stu-id="c6316-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="c6316-110">此路由會轉送封包到本地虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="c6316-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="c6316-111">第二個命令會建立名為 RouteTable01 的路由資料表，並將儲存在 $Route 的路由新資料表。</span><span class="sxs-lookup"><span data-stu-id="c6316-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="c6316-112">命令會指定資料表所屬的資源群組，以及資料表的位置。</span><span class="sxs-lookup"><span data-stu-id="c6316-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="c6316-113">參數</span><span class="sxs-lookup"><span data-stu-id="c6316-113">PARAMETERS</span></span>

### <span data-ttu-id="c6316-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6316-114">-AsJob</span></span>
<span data-ttu-id="c6316-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c6316-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6316-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6316-116">-DefaultProfile</span></span>
<span data-ttu-id="c6316-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6316-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6316-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="c6316-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="c6316-119">停用 BGP 路由自動傳播。</span><span class="sxs-lookup"><span data-stu-id="c6316-119">Disable BGP Route auto propagation.</span></span>

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

### <span data-ttu-id="c6316-120">-強制</span><span class="sxs-lookup"><span data-stu-id="c6316-120">-Force</span></span>
<span data-ttu-id="c6316-121">表示此 Cmdlet 會建立路由資料表，即使已存在相同名稱的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="c6316-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="c6316-122">-位置</span><span class="sxs-lookup"><span data-stu-id="c6316-122">-Location</span></span>
<span data-ttu-id="c6316-123">指定此 Cmdlet 建立路由資料表的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="c6316-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="c6316-124">詳細資訊請參閱 Azure [區域](http://azure.microsoft.com/en-us/regions/)。</span><span class="sxs-lookup"><span data-stu-id="c6316-124">For more information, see [Azure Regions](http://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6316-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6316-125">-Name</span></span>
<span data-ttu-id="c6316-126">指定路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6316-126">Specifies a name for the route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6316-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6316-127">-ResourceGroupName</span></span>
<span data-ttu-id="c6316-128">指定此 Cmdlet 建立路由資料表的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c6316-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6316-129">-路由</span><span class="sxs-lookup"><span data-stu-id="c6316-129">-Route</span></span>
<span data-ttu-id="c6316-130">指定要與 **路由資料** 表建立關聯的路由物件陣列。</span><span class="sxs-lookup"><span data-stu-id="c6316-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRoute[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6316-131">-標記</span><span class="sxs-lookup"><span data-stu-id="c6316-131">-Tag</span></span>
<span data-ttu-id="c6316-132">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="c6316-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c6316-133">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c6316-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6316-134">-確認</span><span class="sxs-lookup"><span data-stu-id="c6316-134">-Confirm</span></span>
<span data-ttu-id="c6316-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c6316-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6316-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6316-136">-WhatIf</span></span>
<span data-ttu-id="c6316-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6316-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6316-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6316-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6316-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6316-139">CommonParameters</span></span>
<span data-ttu-id="c6316-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6316-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6316-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c6316-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6316-142">輸入</span><span class="sxs-lookup"><span data-stu-id="c6316-142">INPUTS</span></span>

### <span data-ttu-id="c6316-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c6316-143">System.String</span></span>

### <span data-ttu-id="c6316-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c6316-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c6316-145">Microsoft.Azure.Commands.Network.models.PSRoute[]</span><span class="sxs-lookup"><span data-stu-id="c6316-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="c6316-146">輸出</span><span class="sxs-lookup"><span data-stu-id="c6316-146">OUTPUTS</span></span>

### <span data-ttu-id="c6316-147">Microsoft.Azure.Commands.Network.models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c6316-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c6316-148">筆記</span><span class="sxs-lookup"><span data-stu-id="c6316-148">NOTES</span></span>

## <span data-ttu-id="c6316-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6316-149">RELATED LINKS</span></span>

[<span data-ttu-id="c6316-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c6316-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="c6316-151">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c6316-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="c6316-152">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c6316-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="c6316-153">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c6316-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
