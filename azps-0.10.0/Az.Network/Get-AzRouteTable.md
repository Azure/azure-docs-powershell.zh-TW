---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: a881e438166729aea8956dc633b7a635499d3752
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794362"
---
# <span data-ttu-id="8f689-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8f689-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="8f689-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f689-102">SYNOPSIS</span></span>
<span data-ttu-id="8f689-103">取得路由表。</span><span class="sxs-lookup"><span data-stu-id="8f689-103">Gets route tables.</span></span>

## <span data-ttu-id="8f689-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f689-104">SYNTAX</span></span>

### <span data-ttu-id="8f689-105">擴充</span><span class="sxs-lookup"><span data-stu-id="8f689-105">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f689-106">NoExpand</span><span class="sxs-lookup"><span data-stu-id="8f689-106">NoExpand</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f689-107">說明</span><span class="sxs-lookup"><span data-stu-id="8f689-107">DESCRIPTION</span></span>
<span data-ttu-id="8f689-108">**AzRouteTable** Cmdlet 會取得 Azure 路由表。</span><span class="sxs-lookup"><span data-stu-id="8f689-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="8f689-109">您可以取得單一路由資料表，或取得資源群組或您訂閱中的所有路由表。</span><span class="sxs-lookup"><span data-stu-id="8f689-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="8f689-110">示例</span><span class="sxs-lookup"><span data-stu-id="8f689-110">EXAMPLES</span></span>

### <span data-ttu-id="8f689-111">範例1：取得路由資料表</span><span class="sxs-lookup"><span data-stu-id="8f689-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
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

<span data-ttu-id="8f689-112">這個命令會取得名為 ResourceGroup11 之資源群組中名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="8f689-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="8f689-113">參數</span><span class="sxs-lookup"><span data-stu-id="8f689-113">PARAMETERS</span></span>

### <span data-ttu-id="8f689-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f689-114">-DefaultProfile</span></span>
<span data-ttu-id="8f689-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f689-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f689-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="8f689-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f689-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f689-117">-Name</span></span>
<span data-ttu-id="8f689-118">指定此 Cmdlet 所取得之路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f689-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f689-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f689-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f689-120">指定包含此 Cmdlet 所取得之路由表之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f689-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f689-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f689-121">CommonParameters</span></span>
<span data-ttu-id="8f689-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f689-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f689-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f689-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f689-124">輸入</span><span class="sxs-lookup"><span data-stu-id="8f689-124">INPUTS</span></span>

## <span data-ttu-id="8f689-125">輸出</span><span class="sxs-lookup"><span data-stu-id="8f689-125">OUTPUTS</span></span>

### <span data-ttu-id="8f689-126">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8f689-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="8f689-127">筆記</span><span class="sxs-lookup"><span data-stu-id="8f689-127">NOTES</span></span>

## <span data-ttu-id="8f689-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f689-128">RELATED LINKS</span></span>

[<span data-ttu-id="8f689-129">新-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8f689-129">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="8f689-130">移除-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8f689-130">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="8f689-131">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8f689-131">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


