---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: fff89f2b6d37dc75923527fdb07a71d79dee80a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455984"
---
# <span data-ttu-id="cd2a9-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd2a9-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="cd2a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd2a9-102">SYNOPSIS</span></span>
<span data-ttu-id="cd2a9-103">建立路由表。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd2a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd2a9-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation]
 -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd2a9-105">說明</span><span class="sxs-lookup"><span data-stu-id="cd2a9-105">DESCRIPTION</span></span>
<span data-ttu-id="cd2a9-106">**新的-AzureRmRouteTable** Cmdlet 會建立 Azure 路由表。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="cd2a9-107">示例</span><span class="sxs-lookup"><span data-stu-id="cd2a9-107">EXAMPLES</span></span>

### <span data-ttu-id="cd2a9-108">範例1：建立包含路由的路由資料表</span><span class="sxs-lookup"><span data-stu-id="cd2a9-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzureRmRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
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

<span data-ttu-id="cd2a9-109">第一個命令會使用 New-AzureRmRouteConfig Cmdlet 來建立名為 Route07 的路由，然後將它儲存在 $Route 變數中。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="cd2a9-110">此路由會將資料包轉寄到本機虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="cd2a9-111">第二個命令會建立名為 RouteTable01 的路由資料表，並將儲存在 $Route 中的路由新增到新的資料表中。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="cd2a9-112">該命令會指定資料表所屬的資源群組，以及表格的位置。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="cd2a9-113">參數</span><span class="sxs-lookup"><span data-stu-id="cd2a9-113">PARAMETERS</span></span>

### <span data-ttu-id="cd2a9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd2a9-114">-AsJob</span></span>
<span data-ttu-id="cd2a9-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd2a9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd2a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd2a9-116">-DefaultProfile</span></span>
<span data-ttu-id="cd2a9-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd2a9-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="cd2a9-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="cd2a9-119">停用 BGP 路由自動傳播。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-119">Disable BGP Route auto propagation.</span></span>

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

### <span data-ttu-id="cd2a9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cd2a9-120">-Force</span></span>
<span data-ttu-id="cd2a9-121">表示此 Cmdlet 會建立路由資料表，即使已存在相同名稱的路由資料表也一樣。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="cd2a9-122">-位置</span><span class="sxs-lookup"><span data-stu-id="cd2a9-122">-Location</span></span>
<span data-ttu-id="cd2a9-123">指定此 Cmdlet 建立路由表的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="cd2a9-124">如需詳細資訊，請參閱 [Azure 地區](https://azure.microsoft.com/en-us/regions/)。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="cd2a9-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd2a9-125">-Name</span></span>
<span data-ttu-id="cd2a9-126">指定路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-126">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="cd2a9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd2a9-127">-ResourceGroupName</span></span>
<span data-ttu-id="cd2a9-128">指定此 Cmdlet 建立路由資料表的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="cd2a9-129">-Route</span><span class="sxs-lookup"><span data-stu-id="cd2a9-129">-Route</span></span>
<span data-ttu-id="cd2a9-130">指定要與路由表建立關聯的 **路由** 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd2a9-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd2a9-131">-Tag</span></span>
<span data-ttu-id="cd2a9-132">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cd2a9-133">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="cd2a9-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cd2a9-134">-確認</span><span class="sxs-lookup"><span data-stu-id="cd2a9-134">-Confirm</span></span>
<span data-ttu-id="cd2a9-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd2a9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd2a9-136">-WhatIf</span></span>
<span data-ttu-id="cd2a9-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd2a9-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd2a9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd2a9-139">CommonParameters</span></span>
<span data-ttu-id="cd2a9-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd2a9-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cd2a9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd2a9-142">輸入</span><span class="sxs-lookup"><span data-stu-id="cd2a9-142">INPUTS</span></span>

### <span data-ttu-id="cd2a9-143">System.object</span><span class="sxs-lookup"><span data-stu-id="cd2a9-143">System.String</span></span>

### <span data-ttu-id="cd2a9-144">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cd2a9-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cd2a9-145">[System.object]。清單 \` 1 [PSRoute，6.4.1.0. network，版本 =，Culture = 中性，PublicKeyToken = null]]。））））</span><span class="sxs-lookup"><span data-stu-id="cd2a9-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSRoute, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cd2a9-146">輸出</span><span class="sxs-lookup"><span data-stu-id="cd2a9-146">OUTPUTS</span></span>

### <span data-ttu-id="cd2a9-147">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cd2a9-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="cd2a9-148">筆記</span><span class="sxs-lookup"><span data-stu-id="cd2a9-148">NOTES</span></span>

## <span data-ttu-id="cd2a9-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd2a9-149">RELATED LINKS</span></span>

[<span data-ttu-id="cd2a9-150">AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd2a9-150">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="cd2a9-151">新-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cd2a9-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="cd2a9-152">移除-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd2a9-152">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="cd2a9-153">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd2a9-153">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
