---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
ms.openlocfilehash: fb675f1d834160bd1fcf5e2dde60dc00e697d629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624209"
---
# <span data-ttu-id="66ebd-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="66ebd-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="66ebd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="66ebd-103">取得路由表。</span><span class="sxs-lookup"><span data-stu-id="66ebd-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66ebd-104">句法</span><span class="sxs-lookup"><span data-stu-id="66ebd-104">SYNTAX</span></span>

### <span data-ttu-id="66ebd-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="66ebd-105">NoExpand</span></span>
```
Get-AzureRmRouteTable [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66ebd-106">擴充</span><span class="sxs-lookup"><span data-stu-id="66ebd-106">Expand</span></span>
```
Get-AzureRmRouteTable -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66ebd-107">說明</span><span class="sxs-lookup"><span data-stu-id="66ebd-107">DESCRIPTION</span></span>
<span data-ttu-id="66ebd-108">**AzureRmRouteTable** Cmdlet 會取得 Azure 路由表。</span><span class="sxs-lookup"><span data-stu-id="66ebd-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="66ebd-109">您可以取得單一路由資料表，或取得資源群組或您訂閱中的所有路由表。</span><span class="sxs-lookup"><span data-stu-id="66ebd-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="66ebd-110">示例</span><span class="sxs-lookup"><span data-stu-id="66ebd-110">EXAMPLES</span></span>

### <span data-ttu-id="66ebd-111">範例1：取得路由資料表</span><span class="sxs-lookup"><span data-stu-id="66ebd-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
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

<span data-ttu-id="66ebd-112">這個命令會取得名為 ResourceGroup11 之資源群組中名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="66ebd-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="66ebd-113">參數</span><span class="sxs-lookup"><span data-stu-id="66ebd-113">PARAMETERS</span></span>

### <span data-ttu-id="66ebd-114">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="66ebd-114">-ExpandResource</span></span>
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

### <span data-ttu-id="66ebd-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="66ebd-115">-Name</span></span>
<span data-ttu-id="66ebd-116">指定此 Cmdlet 所取得之路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="66ebd-116">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ebd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66ebd-117">-ResourceGroupName</span></span>
<span data-ttu-id="66ebd-118">指定包含此 Cmdlet 所取得之路由表之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="66ebd-118">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="66ebd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ebd-119">-DefaultProfile</span></span>
<span data-ttu-id="66ebd-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66ebd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66ebd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ebd-121">CommonParameters</span></span>
<span data-ttu-id="66ebd-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66ebd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ebd-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66ebd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ebd-124">輸入</span><span class="sxs-lookup"><span data-stu-id="66ebd-124">INPUTS</span></span>

## <span data-ttu-id="66ebd-125">輸出</span><span class="sxs-lookup"><span data-stu-id="66ebd-125">OUTPUTS</span></span>

### <span data-ttu-id="66ebd-126">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="66ebd-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="66ebd-127">筆記</span><span class="sxs-lookup"><span data-stu-id="66ebd-127">NOTES</span></span>

## <span data-ttu-id="66ebd-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="66ebd-128">RELATED LINKS</span></span>

[<span data-ttu-id="66ebd-129">新-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="66ebd-129">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="66ebd-130">移除-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="66ebd-130">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="66ebd-131">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="66ebd-131">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


