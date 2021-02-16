---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131039"
---
# <span data-ttu-id="3b0e9-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="3b0e9-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="3b0e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b0e9-102">SYNOPSIS</span></span>
<span data-ttu-id="3b0e9-103">列出對等的已接收路線。</span><span class="sxs-lookup"><span data-stu-id="3b0e9-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="3b0e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b0e9-104">SYNTAX</span></span>

### <span data-ttu-id="3b0e9-105">ByResourceGroupAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="3b0e9-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b0e9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b0e9-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b0e9-107">說明</span><span class="sxs-lookup"><span data-stu-id="3b0e9-107">DESCRIPTION</span></span>
<span data-ttu-id="3b0e9-108">列出從對等的已收到路線</span><span class="sxs-lookup"><span data-stu-id="3b0e9-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="3b0e9-109">示例</span><span class="sxs-lookup"><span data-stu-id="3b0e9-109">EXAMPLES</span></span>

### <span data-ttu-id="3b0e9-110">清單前100收到對等的路由</span><span class="sxs-lookup"><span data-stu-id="3b0e9-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="3b0e9-111">列出對等的所有已接收路線</span><span class="sxs-lookup"><span data-stu-id="3b0e9-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="3b0e9-112">以 Path 篩選</span><span class="sxs-lookup"><span data-stu-id="3b0e9-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="3b0e9-113">列出與篩選開啟之對等的所有已接收路線</span><span class="sxs-lookup"><span data-stu-id="3b0e9-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="3b0e9-114">依 RPKIValidationState 篩選</span><span class="sxs-lookup"><span data-stu-id="3b0e9-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="3b0e9-115">列出與 RPKIValidationState 上的篩選對等的所有已接收路線</span><span class="sxs-lookup"><span data-stu-id="3b0e9-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="3b0e9-116">依 OriginAsValidationState 篩選</span><span class="sxs-lookup"><span data-stu-id="3b0e9-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="3b0e9-117">列出與 OriginAsValidationState 上的篩選對等的所有已接收路線</span><span class="sxs-lookup"><span data-stu-id="3b0e9-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="3b0e9-118">參數</span><span class="sxs-lookup"><span data-stu-id="3b0e9-118">PARAMETERS</span></span>

### <span data-ttu-id="3b0e9-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="3b0e9-119">-AsPath</span></span>
<span data-ttu-id="3b0e9-120">[作為路徑篩選]。</span><span class="sxs-lookup"><span data-stu-id="3b0e9-120">Filter by AS Path.</span></span>
<span data-ttu-id="3b0e9-121">範例： "9342 1234 4567"</span><span class="sxs-lookup"><span data-stu-id="3b0e9-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="3b0e9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b0e9-122">-DefaultProfile</span></span>
<span data-ttu-id="3b0e9-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b0e9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b0e9-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b0e9-124">-Name</span></span>
<span data-ttu-id="3b0e9-125">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="3b0e9-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="3b0e9-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="3b0e9-126">-OriginAsValidationState</span></span>
<span data-ttu-id="3b0e9-127">[依來源篩選] 做為驗證狀態。</span><span class="sxs-lookup"><span data-stu-id="3b0e9-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="3b0e9-128">-Prefix</span><span class="sxs-lookup"><span data-stu-id="3b0e9-128">-Prefix</span></span>
<span data-ttu-id="3b0e9-129">依前置詞篩選。</span><span class="sxs-lookup"><span data-stu-id="3b0e9-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="3b0e9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b0e9-130">-ResourceGroupName</span></span>
<span data-ttu-id="3b0e9-131">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3b0e9-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="3b0e9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b0e9-132">-ResourceId</span></span>
<span data-ttu-id="3b0e9-133">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="3b0e9-133">The resource id string name.</span></span>

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

### <span data-ttu-id="3b0e9-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="3b0e9-134">-RPKIValidationState</span></span>
<span data-ttu-id="3b0e9-135">依 RPKI 驗證狀態進行篩選。</span><span class="sxs-lookup"><span data-stu-id="3b0e9-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="3b0e9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b0e9-136">CommonParameters</span></span>
<span data-ttu-id="3b0e9-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b0e9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b0e9-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3b0e9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b0e9-139">輸入</span><span class="sxs-lookup"><span data-stu-id="3b0e9-139">INPUTS</span></span>

### <span data-ttu-id="3b0e9-140">System.object</span><span class="sxs-lookup"><span data-stu-id="3b0e9-140">System.String</span></span>

## <span data-ttu-id="3b0e9-141">輸出</span><span class="sxs-lookup"><span data-stu-id="3b0e9-141">OUTPUTS</span></span>

### <span data-ttu-id="3b0e9-142">PSPeeringReceivedRoute 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="3b0e9-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="3b0e9-143">筆記</span><span class="sxs-lookup"><span data-stu-id="3b0e9-143">NOTES</span></span>

## <span data-ttu-id="3b0e9-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b0e9-144">RELATED LINKS</span></span>
