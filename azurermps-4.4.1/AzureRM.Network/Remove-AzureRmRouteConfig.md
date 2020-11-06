---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
ms.openlocfilehash: b64fe52b95fb116b08aade300f622b8ea612dcc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455691"
---
# <span data-ttu-id="7d920-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7d920-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="7d920-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d920-102">SYNOPSIS</span></span>
<span data-ttu-id="7d920-103">從路由表中移除路由。</span><span class="sxs-lookup"><span data-stu-id="7d920-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d920-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d920-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d920-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d920-105">DESCRIPTION</span></span>
<span data-ttu-id="7d920-106">**AzureRmRouteConfig** Cmdlet 會從 Azure 路由表中移除路由。</span><span class="sxs-lookup"><span data-stu-id="7d920-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="7d920-107">示例</span><span class="sxs-lookup"><span data-stu-id="7d920-107">EXAMPLES</span></span>

### <span data-ttu-id="7d920-108">範例1：移除路線</span><span class="sxs-lookup"><span data-stu-id="7d920-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzureRmRouteConfig -Name "Route02" | Set-AzureRmRouteTable
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

<span data-ttu-id="7d920-109">這個命令會使用 **AzureRmRouteTable** Cmdlet 取得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="7d920-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="7d920-110">命令會使用管線運算子，將該表傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d920-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7d920-111">目前的 Cmdlet 會移除名為 Route02 的路由，並將結果傳遞到 **AzureRmRouteTable** Cmdlet，這會更新資料表以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="7d920-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="7d920-112">該表不再包含名為 Route02 的路由。</span><span class="sxs-lookup"><span data-stu-id="7d920-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="7d920-113">參數</span><span class="sxs-lookup"><span data-stu-id="7d920-113">PARAMETERS</span></span>

### <span data-ttu-id="7d920-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d920-114">-Name</span></span>
<span data-ttu-id="7d920-115">指定此 Cmdlet 移除之路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d920-115">Specifies the name of the route that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d920-116">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="7d920-116">-RouteTable</span></span>
<span data-ttu-id="7d920-117">指定包含此 Cmdlet 刪除之路由的路由表。</span><span class="sxs-lookup"><span data-stu-id="7d920-117">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="7d920-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d920-118">-DefaultProfile</span></span>
<span data-ttu-id="7d920-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d920-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d920-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d920-120">CommonParameters</span></span>
<span data-ttu-id="7d920-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d920-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d920-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d920-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d920-123">輸入</span><span class="sxs-lookup"><span data-stu-id="7d920-123">INPUTS</span></span>

### <span data-ttu-id="7d920-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d920-124">PSRouteTable</span></span>
<span data-ttu-id="7d920-125">形參 "RouteTable" 接受管線中 "PSRouteTable" 類型的值</span><span class="sxs-lookup"><span data-stu-id="7d920-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="7d920-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7d920-126">OUTPUTS</span></span>

### <span data-ttu-id="7d920-127">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7d920-127">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="7d920-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7d920-128">NOTES</span></span>

## <span data-ttu-id="7d920-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d920-129">RELATED LINKS</span></span>

[<span data-ttu-id="7d920-130">附加 AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7d920-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="7d920-131">AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7d920-131">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="7d920-132">新-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7d920-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="7d920-133">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7d920-133">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


