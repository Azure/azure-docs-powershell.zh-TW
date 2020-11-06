---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: f0d537e2729fc69f2a65563ab059f332d320e99a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449988"
---
# <span data-ttu-id="dbda3-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dbda3-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="dbda3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbda3-102">SYNOPSIS</span></span>
<span data-ttu-id="dbda3-103">從路由資料表取得路由。</span><span class="sxs-lookup"><span data-stu-id="dbda3-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbda3-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbda3-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig [-Name <String>] -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbda3-105">說明</span><span class="sxs-lookup"><span data-stu-id="dbda3-105">DESCRIPTION</span></span>
<span data-ttu-id="dbda3-106">**AzureRmRouteConfig** Cmdlet 會從 Azure 路由表取得路由。</span><span class="sxs-lookup"><span data-stu-id="dbda3-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="dbda3-107">您可以依名稱指定路由。</span><span class="sxs-lookup"><span data-stu-id="dbda3-107">You can specify a route by name.</span></span>

## <span data-ttu-id="dbda3-108">示例</span><span class="sxs-lookup"><span data-stu-id="dbda3-108">EXAMPLES</span></span>

### <span data-ttu-id="dbda3-109">範例1：取得路由資料表</span><span class="sxs-lookup"><span data-stu-id="dbda3-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="dbda3-110">這個命令會使用 **AzureRmRouteTable** Cmdlet 取得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="dbda3-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="dbda3-111">命令會使用管線運算子，將該表傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dbda3-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dbda3-112">目前的 Cmdlet 會在路由表中取得名為 RouteTable01 的名為 Route07 的路由。</span><span class="sxs-lookup"><span data-stu-id="dbda3-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="dbda3-113">參數</span><span class="sxs-lookup"><span data-stu-id="dbda3-113">PARAMETERS</span></span>

### <span data-ttu-id="dbda3-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="dbda3-114">-Name</span></span>
<span data-ttu-id="dbda3-115">指定此 Cmdlet 所取得之路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbda3-115">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dbda3-116">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="dbda3-116">-RouteTable</span></span>
<span data-ttu-id="dbda3-117">指定由此 Cmdlet 取得路由的路由表。</span><span class="sxs-lookup"><span data-stu-id="dbda3-117">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="dbda3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbda3-118">-DefaultProfile</span></span>
<span data-ttu-id="dbda3-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbda3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbda3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbda3-120">CommonParameters</span></span>
<span data-ttu-id="dbda3-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbda3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbda3-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dbda3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbda3-123">輸入</span><span class="sxs-lookup"><span data-stu-id="dbda3-123">INPUTS</span></span>

### <span data-ttu-id="dbda3-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="dbda3-124">PSRouteTable</span></span>
<span data-ttu-id="dbda3-125">形參 "RouteTable" 接受管線中 "PSRouteTable" 類型的值</span><span class="sxs-lookup"><span data-stu-id="dbda3-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="dbda3-126">輸出</span><span class="sxs-lookup"><span data-stu-id="dbda3-126">OUTPUTS</span></span>

### <span data-ttu-id="dbda3-127">PSRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dbda3-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="dbda3-128">筆記</span><span class="sxs-lookup"><span data-stu-id="dbda3-128">NOTES</span></span>

## <span data-ttu-id="dbda3-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbda3-129">RELATED LINKS</span></span>

[<span data-ttu-id="dbda3-130">附加 AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dbda3-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="dbda3-131">AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="dbda3-131">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="dbda3-132">新-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dbda3-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="dbda3-133">移除-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dbda3-133">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="dbda3-134">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dbda3-134">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


