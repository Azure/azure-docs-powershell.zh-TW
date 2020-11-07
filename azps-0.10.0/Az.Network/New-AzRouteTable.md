---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: f00840afac4a4d1f0d92316bc859e0a66e7806ff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794238"
---
# <span data-ttu-id="96023-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="96023-101">New-AzRouteTable</span></span>

## <span data-ttu-id="96023-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96023-102">SYNOPSIS</span></span>
<span data-ttu-id="96023-103">建立路由表。</span><span class="sxs-lookup"><span data-stu-id="96023-103">Creates a route table.</span></span>

## <span data-ttu-id="96023-104">句法</span><span class="sxs-lookup"><span data-stu-id="96023-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96023-105">說明</span><span class="sxs-lookup"><span data-stu-id="96023-105">DESCRIPTION</span></span>
<span data-ttu-id="96023-106">**新的-AzRouteTable** Cmdlet 會建立 Azure 路由表。</span><span class="sxs-lookup"><span data-stu-id="96023-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="96023-107">示例</span><span class="sxs-lookup"><span data-stu-id="96023-107">EXAMPLES</span></span>

### <span data-ttu-id="96023-108">範例1：建立包含路由的路由資料表</span><span class="sxs-lookup"><span data-stu-id="96023-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="96023-109">第一個命令會使用 New-AzRouteConfig Cmdlet 來建立名為 Route07 的路由，然後將它儲存在 $Route 變數中。</span><span class="sxs-lookup"><span data-stu-id="96023-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="96023-110">此路由會將資料包轉寄到本機虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="96023-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="96023-111">第二個命令會建立名為 RouteTable01 的路由資料表，並將儲存在 $Route 中的路由新增到新的資料表中。</span><span class="sxs-lookup"><span data-stu-id="96023-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="96023-112">該命令會指定資料表所屬的資源群組，以及表格的位置。</span><span class="sxs-lookup"><span data-stu-id="96023-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="96023-113">參數</span><span class="sxs-lookup"><span data-stu-id="96023-113">PARAMETERS</span></span>

### <span data-ttu-id="96023-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96023-114">-AsJob</span></span>
<span data-ttu-id="96023-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="96023-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96023-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96023-116">-DefaultProfile</span></span>
<span data-ttu-id="96023-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96023-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96023-118">-Force</span><span class="sxs-lookup"><span data-stu-id="96023-118">-Force</span></span>
<span data-ttu-id="96023-119">表示此 Cmdlet 會建立路由資料表，即使已存在相同名稱的路由資料表也一樣。</span><span class="sxs-lookup"><span data-stu-id="96023-119">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="96023-120">-位置</span><span class="sxs-lookup"><span data-stu-id="96023-120">-Location</span></span>
<span data-ttu-id="96023-121">指定此 Cmdlet 建立路由表的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="96023-121">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="96023-122">如需詳細資訊，請參閱 [Azure 地區](http://azure.microsoft.com/en-us/regions/)。</span><span class="sxs-lookup"><span data-stu-id="96023-122">For more information, see [Azure Regions](http://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96023-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="96023-123">-Name</span></span>
<span data-ttu-id="96023-124">指定路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="96023-124">Specifies a name for the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96023-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96023-125">-ResourceGroupName</span></span>
<span data-ttu-id="96023-126">指定此 Cmdlet 建立路由資料表的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="96023-126">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96023-127">-Route</span><span class="sxs-lookup"><span data-stu-id="96023-127">-Route</span></span>
<span data-ttu-id="96023-128">指定要與路由表建立關聯的 **路由** 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="96023-128">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="96023-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="96023-129">-Tag</span></span>
<span data-ttu-id="96023-130">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="96023-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="96023-131">例如：</span><span class="sxs-lookup"><span data-stu-id="96023-131">For example:</span></span>

<span data-ttu-id="96023-132">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="96023-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96023-133">-確認</span><span class="sxs-lookup"><span data-stu-id="96023-133">-Confirm</span></span>
<span data-ttu-id="96023-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="96023-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96023-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96023-135">-WhatIf</span></span>
<span data-ttu-id="96023-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96023-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96023-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96023-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96023-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96023-138">CommonParameters</span></span>
<span data-ttu-id="96023-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96023-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96023-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="96023-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96023-141">輸入</span><span class="sxs-lookup"><span data-stu-id="96023-141">INPUTS</span></span>

## <span data-ttu-id="96023-142">輸出</span><span class="sxs-lookup"><span data-stu-id="96023-142">OUTPUTS</span></span>

### <span data-ttu-id="96023-143">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="96023-143">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="96023-144">筆記</span><span class="sxs-lookup"><span data-stu-id="96023-144">NOTES</span></span>

## <span data-ttu-id="96023-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="96023-145">RELATED LINKS</span></span>

[<span data-ttu-id="96023-146">AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="96023-146">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="96023-147">新-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="96023-147">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="96023-148">移除-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="96023-148">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="96023-149">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="96023-149">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
