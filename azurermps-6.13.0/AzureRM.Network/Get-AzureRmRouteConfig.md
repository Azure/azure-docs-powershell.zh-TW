---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: dd23891bc56ac2eb8fce30708d9a72055a567bf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448379"
---
# <span data-ttu-id="aa29d-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="aa29d-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="aa29d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa29d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa29d-103">從路由資料表取得路由。</span><span class="sxs-lookup"><span data-stu-id="aa29d-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa29d-104">句法</span><span class="sxs-lookup"><span data-stu-id="aa29d-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa29d-105">說明</span><span class="sxs-lookup"><span data-stu-id="aa29d-105">DESCRIPTION</span></span>
<span data-ttu-id="aa29d-106">**AzureRmRouteConfig** Cmdlet 會從 Azure 路由表取得路由。</span><span class="sxs-lookup"><span data-stu-id="aa29d-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="aa29d-107">您可以依名稱指定路由。</span><span class="sxs-lookup"><span data-stu-id="aa29d-107">You can specify a route by name.</span></span>

## <span data-ttu-id="aa29d-108">示例</span><span class="sxs-lookup"><span data-stu-id="aa29d-108">EXAMPLES</span></span>

### <span data-ttu-id="aa29d-109">範例1：取得路由資料表</span><span class="sxs-lookup"><span data-stu-id="aa29d-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzureRmRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="aa29d-110">這個命令會使用 **AzureRmRouteTable** Cmdlet 取得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="aa29d-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="aa29d-111">命令會使用管線運算子，將該表傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aa29d-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="aa29d-112">目前的 Cmdlet 會在路由表中取得名為 RouteTable01 的名為 Route07 的路由。</span><span class="sxs-lookup"><span data-stu-id="aa29d-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="aa29d-113">參數</span><span class="sxs-lookup"><span data-stu-id="aa29d-113">PARAMETERS</span></span>

### <span data-ttu-id="aa29d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa29d-114">-DefaultProfile</span></span>
<span data-ttu-id="aa29d-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa29d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa29d-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="aa29d-116">-Name</span></span>
<span data-ttu-id="aa29d-117">指定此 Cmdlet 所取得之路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa29d-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="aa29d-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="aa29d-118">-RouteTable</span></span>
<span data-ttu-id="aa29d-119">指定由此 Cmdlet 取得路由的路由表。</span><span class="sxs-lookup"><span data-stu-id="aa29d-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="aa29d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa29d-120">CommonParameters</span></span>
<span data-ttu-id="aa29d-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa29d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa29d-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aa29d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa29d-123">輸入</span><span class="sxs-lookup"><span data-stu-id="aa29d-123">INPUTS</span></span>

### <span data-ttu-id="aa29d-124">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="aa29d-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="aa29d-125">輸出</span><span class="sxs-lookup"><span data-stu-id="aa29d-125">OUTPUTS</span></span>

### <span data-ttu-id="aa29d-126">PSRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="aa29d-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="aa29d-127">筆記</span><span class="sxs-lookup"><span data-stu-id="aa29d-127">NOTES</span></span>

## <span data-ttu-id="aa29d-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa29d-128">RELATED LINKS</span></span>

[<span data-ttu-id="aa29d-129">附加 AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="aa29d-129">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="aa29d-130">AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="aa29d-130">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="aa29d-131">新-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="aa29d-131">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="aa29d-132">移除-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="aa29d-132">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="aa29d-133">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="aa29d-133">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


