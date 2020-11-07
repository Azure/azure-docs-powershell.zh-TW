---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: a5b80a15711314d5acc4f0288c1fd0304da772fc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794369"
---
# <span data-ttu-id="e8e7c-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e8e7c-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="e8e7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e7c-103">從路由資料表取得路由。</span><span class="sxs-lookup"><span data-stu-id="e8e7c-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="e8e7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8e7c-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8e7c-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8e7c-105">DESCRIPTION</span></span>
<span data-ttu-id="e8e7c-106">**AzRouteConfig** Cmdlet 會從 Azure 路由表取得路由。</span><span class="sxs-lookup"><span data-stu-id="e8e7c-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="e8e7c-107">您可以依名稱指定路由。</span><span class="sxs-lookup"><span data-stu-id="e8e7c-107">You can specify a route by name.</span></span>

## <span data-ttu-id="e8e7c-108">示例</span><span class="sxs-lookup"><span data-stu-id="e8e7c-108">EXAMPLES</span></span>

### <span data-ttu-id="e8e7c-109">範例1：取得路由資料表</span><span class="sxs-lookup"><span data-stu-id="e8e7c-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="e8e7c-110">這個命令會使用 **AzRouteTable** Cmdlet 取得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="e8e7c-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="e8e7c-111">命令會使用管線運算子，將該表傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8e7c-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e8e7c-112">目前的 Cmdlet 會在路由表中取得名為 RouteTable01 的名為 Route07 的路由。</span><span class="sxs-lookup"><span data-stu-id="e8e7c-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="e8e7c-113">參數</span><span class="sxs-lookup"><span data-stu-id="e8e7c-113">PARAMETERS</span></span>

### <span data-ttu-id="e8e7c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8e7c-114">-DefaultProfile</span></span>
<span data-ttu-id="e8e7c-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8e7c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8e7c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8e7c-116">-Name</span></span>
<span data-ttu-id="e8e7c-117">指定此 Cmdlet 所取得之路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e7c-117">Specifies the name of the route that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e7c-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e8e7c-118">-RouteTable</span></span>
<span data-ttu-id="e8e7c-119">指定由此 Cmdlet 取得路由的路由表。</span><span class="sxs-lookup"><span data-stu-id="e8e7c-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e7c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e7c-120">CommonParameters</span></span>
<span data-ttu-id="e8e7c-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8e7c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e7c-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8e7c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e7c-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e8e7c-123">INPUTS</span></span>

### <span data-ttu-id="e8e7c-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e8e7c-124">PSRouteTable</span></span>
<span data-ttu-id="e8e7c-125">形參 "RouteTable" 接受管線中 "PSRouteTable" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e8e7c-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="e8e7c-126">輸出</span><span class="sxs-lookup"><span data-stu-id="e8e7c-126">OUTPUTS</span></span>

### <span data-ttu-id="e8e7c-127">PSRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e8e7c-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="e8e7c-128">筆記</span><span class="sxs-lookup"><span data-stu-id="e8e7c-128">NOTES</span></span>

## <span data-ttu-id="e8e7c-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8e7c-129">RELATED LINKS</span></span>

[<span data-ttu-id="e8e7c-130">附加 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e8e7c-130">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="e8e7c-131">AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e8e7c-131">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="e8e7c-132">新-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e8e7c-132">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="e8e7c-133">移除-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e8e7c-133">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="e8e7c-134">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e8e7c-134">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


