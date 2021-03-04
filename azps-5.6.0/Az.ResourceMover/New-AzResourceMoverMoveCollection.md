---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 317614d67138b185dc58334d398bb368fc85911e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914426"
---
# <span data-ttu-id="f93e9-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f93e9-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="f93e9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f93e9-102">SYNOPSIS</span></span>
<span data-ttu-id="f93e9-103">建立或更新移動集合。</span><span class="sxs-lookup"><span data-stu-id="f93e9-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="f93e9-104">語法</span><span class="sxs-lookup"><span data-stu-id="f93e9-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f93e9-105">描述</span><span class="sxs-lookup"><span data-stu-id="f93e9-105">DESCRIPTION</span></span>
<span data-ttu-id="f93e9-106">建立或更新移動集合。</span><span class="sxs-lookup"><span data-stu-id="f93e9-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="f93e9-107">例子</span><span class="sxs-lookup"><span data-stu-id="f93e9-107">EXAMPLES</span></span>

### <span data-ttu-id="f93e9-108">範例 1：建立新的移動集合。</span><span class="sxs-lookup"><span data-stu-id="f93e9-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name "PS-centralus-westcentralus-demoRMS"  -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceRegion "centralus" -TargetRegion "westcentralus" -Location "centraluseuap" -IdentityType "SystemAssigned"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"0200d92f-0000-3300-0000-6021e9ec0000" centraluseuap PS-centralus-westcentralus-demoRMs Microsoft.Migrate/moveCollections
```

<span data-ttu-id="f93e9-109">建立新的移動集合。</span><span class="sxs-lookup"><span data-stu-id="f93e9-109">Create a new Move Collection.</span></span>

## <span data-ttu-id="f93e9-110">參數</span><span class="sxs-lookup"><span data-stu-id="f93e9-110">PARAMETERS</span></span>

### <span data-ttu-id="f93e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f93e9-111">-DefaultProfile</span></span>
<span data-ttu-id="f93e9-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f93e9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93e9-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="f93e9-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="f93e9-114">獲取或設定主體識別碼。</span><span class="sxs-lookup"><span data-stu-id="f93e9-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="f93e9-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="f93e9-115">-IdentityTenantId</span></span>
<span data-ttu-id="f93e9-116">獲取或設定租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="f93e9-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="f93e9-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f93e9-117">-IdentityType</span></span>
<span data-ttu-id="f93e9-118">資源 Mover 服務所使用的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="f93e9-118">The type of identity used for the resource mover service.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.ResourceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93e9-119">-位置</span><span class="sxs-lookup"><span data-stu-id="f93e9-119">-Location</span></span>
<span data-ttu-id="f93e9-120">資源所位於的地理位置。</span><span class="sxs-lookup"><span data-stu-id="f93e9-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="f93e9-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f93e9-121">-Name</span></span>
<span data-ttu-id="f93e9-122">移動集合名稱。</span><span class="sxs-lookup"><span data-stu-id="f93e9-122">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93e9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f93e9-123">-ResourceGroupName</span></span>
<span data-ttu-id="f93e9-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f93e9-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="f93e9-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="f93e9-125">-SourceRegion</span></span>
<span data-ttu-id="f93e9-126">獲取或設定來源區域。</span><span class="sxs-lookup"><span data-stu-id="f93e9-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="f93e9-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f93e9-127">-SubscriptionId</span></span>
<span data-ttu-id="f93e9-128">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f93e9-128">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93e9-129">-標記</span><span class="sxs-lookup"><span data-stu-id="f93e9-129">-Tag</span></span>
<span data-ttu-id="f93e9-130">資源標記。</span><span class="sxs-lookup"><span data-stu-id="f93e9-130">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93e9-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="f93e9-131">-TargetRegion</span></span>
<span data-ttu-id="f93e9-132">獲取或設定目的地區域。</span><span class="sxs-lookup"><span data-stu-id="f93e9-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="f93e9-133">-確認</span><span class="sxs-lookup"><span data-stu-id="f93e9-133">-Confirm</span></span>
<span data-ttu-id="f93e9-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f93e9-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93e9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f93e9-135">-WhatIf</span></span>
<span data-ttu-id="f93e9-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f93e9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f93e9-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f93e9-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93e9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f93e9-138">CommonParameters</span></span>
<span data-ttu-id="f93e9-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f93e9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f93e9-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f93e9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f93e9-141">輸入</span><span class="sxs-lookup"><span data-stu-id="f93e9-141">INPUTS</span></span>

## <span data-ttu-id="f93e9-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f93e9-142">OUTPUTS</span></span>

### <span data-ttu-id="f93e9-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f93e9-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="f93e9-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f93e9-144">NOTES</span></span>

<span data-ttu-id="f93e9-145">別名</span><span class="sxs-lookup"><span data-stu-id="f93e9-145">ALIASES</span></span>

## <span data-ttu-id="f93e9-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="f93e9-146">RELATED LINKS</span></span>

