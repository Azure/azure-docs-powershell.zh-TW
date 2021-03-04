---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: e5f961b5bd3acc1db716d68f43147e1a6c5611f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911506"
---
# <span data-ttu-id="e3ebb-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="e3ebb-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="e3ebb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e3ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ebb-103">列出對等的接收路由。</span><span class="sxs-lookup"><span data-stu-id="e3ebb-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="e3ebb-104">語法</span><span class="sxs-lookup"><span data-stu-id="e3ebb-104">SYNTAX</span></span>

### <span data-ttu-id="e3ebb-105">ByResourceGroupAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="e3ebb-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3ebb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e3ebb-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3ebb-107">描述</span><span class="sxs-lookup"><span data-stu-id="e3ebb-107">DESCRIPTION</span></span>
<span data-ttu-id="e3ebb-108">列出來自對等的接收路由</span><span class="sxs-lookup"><span data-stu-id="e3ebb-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="e3ebb-109">例子</span><span class="sxs-lookup"><span data-stu-id="e3ebb-109">EXAMPLES</span></span>

### <span data-ttu-id="e3ebb-110">列出對等的前 100 個接收路由</span><span class="sxs-lookup"><span data-stu-id="e3ebb-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="e3ebb-111">列出對等的所有接收路由</span><span class="sxs-lookup"><span data-stu-id="e3ebb-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="e3ebb-112">根據 AS 路徑篩選</span><span class="sxs-lookup"><span data-stu-id="e3ebb-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="e3ebb-113">使用 AS 上的篩選列出對等的所有接收路由</span><span class="sxs-lookup"><span data-stu-id="e3ebb-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="e3ebb-114">根據 RPKIValidationState 篩選</span><span class="sxs-lookup"><span data-stu-id="e3ebb-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="e3ebb-115">使用 RPKIValidationState 上的篩選列出對等的所有接收路由</span><span class="sxs-lookup"><span data-stu-id="e3ebb-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="e3ebb-116">根據 OriginAsValidationState 篩選</span><span class="sxs-lookup"><span data-stu-id="e3ebb-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="e3ebb-117">使用 OriginAsValidationState 上的篩選列出對等的所有接收路由</span><span class="sxs-lookup"><span data-stu-id="e3ebb-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="e3ebb-118">參數</span><span class="sxs-lookup"><span data-stu-id="e3ebb-118">PARAMETERS</span></span>

### <span data-ttu-id="e3ebb-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="e3ebb-119">-AsPath</span></span>
<span data-ttu-id="e3ebb-120">根據 AS 路徑篩選。</span><span class="sxs-lookup"><span data-stu-id="e3ebb-120">Filter by AS Path.</span></span>
<span data-ttu-id="e3ebb-121">範例：'9342 1234 4567'</span><span class="sxs-lookup"><span data-stu-id="e3ebb-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="e3ebb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ebb-122">-DefaultProfile</span></span>
<span data-ttu-id="e3ebb-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3ebb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3ebb-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3ebb-124">-Name</span></span>
<span data-ttu-id="e3ebb-125">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="e3ebb-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ebb-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="e3ebb-126">-OriginAsValidationState</span></span>
<span data-ttu-id="e3ebb-127">根據原始 AS 驗證狀態篩選。</span><span class="sxs-lookup"><span data-stu-id="e3ebb-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="e3ebb-128">-首碼</span><span class="sxs-lookup"><span data-stu-id="e3ebb-128">-Prefix</span></span>
<span data-ttu-id="e3ebb-129">根據首碼篩選。</span><span class="sxs-lookup"><span data-stu-id="e3ebb-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="e3ebb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3ebb-130">-ResourceGroupName</span></span>
<span data-ttu-id="e3ebb-131">建立或使用現有的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e3ebb-131">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ebb-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3ebb-132">-ResourceId</span></span>
<span data-ttu-id="e3ebb-133">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="e3ebb-133">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3ebb-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="e3ebb-134">-RPKIValidationState</span></span>
<span data-ttu-id="e3ebb-135">根據 RPKI 驗證狀態篩選。</span><span class="sxs-lookup"><span data-stu-id="e3ebb-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="e3ebb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ebb-136">CommonParameters</span></span>
<span data-ttu-id="e3ebb-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e3ebb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ebb-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3ebb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ebb-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e3ebb-139">INPUTS</span></span>

### <span data-ttu-id="e3ebb-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e3ebb-140">System.String</span></span>

## <span data-ttu-id="e3ebb-141">輸出</span><span class="sxs-lookup"><span data-stu-id="e3ebb-141">OUTPUTS</span></span>

### <span data-ttu-id="e3ebb-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="e3ebb-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="e3ebb-143">筆記</span><span class="sxs-lookup"><span data-stu-id="e3ebb-143">NOTES</span></span>

## <span data-ttu-id="e3ebb-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3ebb-144">RELATED LINKS</span></span>
