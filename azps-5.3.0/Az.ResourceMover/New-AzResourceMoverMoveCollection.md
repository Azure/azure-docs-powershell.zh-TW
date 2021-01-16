---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435570"
---
# <span data-ttu-id="08489-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="08489-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="08489-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08489-102">SYNOPSIS</span></span>
<span data-ttu-id="08489-103">建立或更新移動收藏。</span><span class="sxs-lookup"><span data-stu-id="08489-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="08489-104">句法</span><span class="sxs-lookup"><span data-stu-id="08489-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="08489-105">說明</span><span class="sxs-lookup"><span data-stu-id="08489-105">DESCRIPTION</span></span>
<span data-ttu-id="08489-106">建立或更新移動收藏。</span><span class="sxs-lookup"><span data-stu-id="08489-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="08489-107">示例</span><span class="sxs-lookup"><span data-stu-id="08489-107">EXAMPLES</span></span>

### <span data-ttu-id="08489-108">範例1：建立新的移動收藏。</span><span class="sxs-lookup"><span data-stu-id="08489-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="08489-109">在訂閱中建立新的移動收藏。</span><span class="sxs-lookup"><span data-stu-id="08489-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="08489-110">參數</span><span class="sxs-lookup"><span data-stu-id="08489-110">PARAMETERS</span></span>

### <span data-ttu-id="08489-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08489-111">-DefaultProfile</span></span>
<span data-ttu-id="08489-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="08489-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08489-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="08489-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="08489-114">取得或設定主體識別碼。</span><span class="sxs-lookup"><span data-stu-id="08489-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="08489-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="08489-115">-IdentityTenantId</span></span>
<span data-ttu-id="08489-116">取得或設定租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="08489-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="08489-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="08489-117">-IdentityType</span></span>
<span data-ttu-id="08489-118">用於區域移動服務的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="08489-118">The type of identity used for the region move service.</span></span>

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

### <span data-ttu-id="08489-119">-位置</span><span class="sxs-lookup"><span data-stu-id="08489-119">-Location</span></span>
<span data-ttu-id="08489-120">資源所在的地理位置。</span><span class="sxs-lookup"><span data-stu-id="08489-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="08489-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="08489-121">-Name</span></span>
<span data-ttu-id="08489-122">[移動集合名稱]。</span><span class="sxs-lookup"><span data-stu-id="08489-122">The Move Collection Name.</span></span>

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

### <span data-ttu-id="08489-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08489-123">-ResourceGroupName</span></span>
<span data-ttu-id="08489-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="08489-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="08489-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="08489-125">-SourceRegion</span></span>
<span data-ttu-id="08489-126">取得或設定源區域。</span><span class="sxs-lookup"><span data-stu-id="08489-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="08489-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="08489-127">-SubscriptionId</span></span>
<span data-ttu-id="08489-128">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="08489-128">The Subscription ID.</span></span>

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

### <span data-ttu-id="08489-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="08489-129">-Tag</span></span>
<span data-ttu-id="08489-130">資源標記。</span><span class="sxs-lookup"><span data-stu-id="08489-130">Resource tags.</span></span>

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

### <span data-ttu-id="08489-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="08489-131">-TargetRegion</span></span>
<span data-ttu-id="08489-132">取得或設定目的地區域。</span><span class="sxs-lookup"><span data-stu-id="08489-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="08489-133">-確認</span><span class="sxs-lookup"><span data-stu-id="08489-133">-Confirm</span></span>
<span data-ttu-id="08489-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="08489-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08489-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08489-135">-WhatIf</span></span>
<span data-ttu-id="08489-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="08489-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08489-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08489-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08489-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08489-138">CommonParameters</span></span>
<span data-ttu-id="08489-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08489-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08489-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="08489-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08489-141">輸入</span><span class="sxs-lookup"><span data-stu-id="08489-141">INPUTS</span></span>

## <span data-ttu-id="08489-142">輸出</span><span class="sxs-lookup"><span data-stu-id="08489-142">OUTPUTS</span></span>

### <span data-ttu-id="08489-143">IMoveCollection （ResourceMover）。 Api20191001Preview。</span><span class="sxs-lookup"><span data-stu-id="08489-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="08489-144">筆記</span><span class="sxs-lookup"><span data-stu-id="08489-144">NOTES</span></span>

<span data-ttu-id="08489-145">別名</span><span class="sxs-lookup"><span data-stu-id="08489-145">ALIASES</span></span>

## <span data-ttu-id="08489-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="08489-146">RELATED LINKS</span></span>

