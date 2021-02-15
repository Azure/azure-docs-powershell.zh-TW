---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: 613519f6d9d3d2d8ce1c83ff0ad5a2d9421859b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131346"
---
# <span data-ttu-id="f716e-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f716e-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="f716e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f716e-102">SYNOPSIS</span></span>
<span data-ttu-id="f716e-103">取得路由表。</span><span class="sxs-lookup"><span data-stu-id="f716e-103">Gets route tables.</span></span>

## <span data-ttu-id="f716e-104">句法</span><span class="sxs-lookup"><span data-stu-id="f716e-104">SYNTAX</span></span>

### <span data-ttu-id="f716e-105">NoExpand (預設) </span><span class="sxs-lookup"><span data-stu-id="f716e-105">NoExpand (Default)</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f716e-106">擴充</span><span class="sxs-lookup"><span data-stu-id="f716e-106">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f716e-107">說明</span><span class="sxs-lookup"><span data-stu-id="f716e-107">DESCRIPTION</span></span>
<span data-ttu-id="f716e-108">**AzRouteTable** Cmdlet 會取得 Azure 路由表。</span><span class="sxs-lookup"><span data-stu-id="f716e-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="f716e-109">您可以取得單一路由資料表，或取得資源群組或您訂閱中的所有路由表。</span><span class="sxs-lookup"><span data-stu-id="f716e-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="f716e-110">示例</span><span class="sxs-lookup"><span data-stu-id="f716e-110">EXAMPLES</span></span>

### <span data-ttu-id="f716e-111">範例1：取得路由資料表</span><span class="sxs-lookup"><span data-stu-id="f716e-111">Example 1: Get a route table</span></span>
```
PS C:\> Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"

Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
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

<span data-ttu-id="f716e-112">這個命令會取得名為 ResourceGroup11 之資源群組中名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="f716e-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="f716e-113">範例2：使用篩選來列出路由表</span><span class="sxs-lookup"><span data-stu-id="f716e-113">Example 2: List route tables using filtering</span></span>
```
PS C:\> Get-AzRouteTable -Name RouteTable*

Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
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

Name              : routetable02
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable02
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable02/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="f716e-114">這個命令會取得名稱開頭為 "RouteTable" 的所有路由資料表</span><span class="sxs-lookup"><span data-stu-id="f716e-114">This command gets all route tables whose name starts with "RouteTable"</span></span>

## <span data-ttu-id="f716e-115">參數</span><span class="sxs-lookup"><span data-stu-id="f716e-115">PARAMETERS</span></span>

### <span data-ttu-id="f716e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f716e-116">-DefaultProfile</span></span>
<span data-ttu-id="f716e-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f716e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f716e-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f716e-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f716e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f716e-119">-Name</span></span>
<span data-ttu-id="f716e-120">指定此 Cmdlet 所取得之路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="f716e-120">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f716e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f716e-121">-ResourceGroupName</span></span>
<span data-ttu-id="f716e-122">指定包含此 Cmdlet 所取得之路由表之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f716e-122">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f716e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f716e-123">CommonParameters</span></span>
<span data-ttu-id="f716e-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f716e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f716e-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f716e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f716e-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f716e-126">INPUTS</span></span>

### <span data-ttu-id="f716e-127">System.object</span><span class="sxs-lookup"><span data-stu-id="f716e-127">System.String</span></span>

## <span data-ttu-id="f716e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f716e-128">OUTPUTS</span></span>

### <span data-ttu-id="f716e-129">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f716e-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="f716e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f716e-130">NOTES</span></span>

## <span data-ttu-id="f716e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f716e-131">RELATED LINKS</span></span>

[<span data-ttu-id="f716e-132">新-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f716e-132">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="f716e-133">移除-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f716e-133">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="f716e-134">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f716e-134">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


