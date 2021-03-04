---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 34cae1bcc6020e2e0c2a8b2f6b70e302c8576f2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914453"
---
# <span data-ttu-id="c0a12-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="c0a12-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="c0a12-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c0a12-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a12-103">獲得無法解析的相依性清單。</span><span class="sxs-lookup"><span data-stu-id="c0a12-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="c0a12-104">語法</span><span class="sxs-lookup"><span data-stu-id="c0a12-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DependencyLevel <DependencyLevel>] [-Filter <String>] [-Orderby <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c0a12-105">描述</span><span class="sxs-lookup"><span data-stu-id="c0a12-105">DESCRIPTION</span></span>
<span data-ttu-id="c0a12-106">獲得無法解析的相依性清單。</span><span class="sxs-lookup"><span data-stu-id="c0a12-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="c0a12-107">例子</span><span class="sxs-lookup"><span data-stu-id="c0a12-107">EXAMPLES</span></span>

### <span data-ttu-id="c0a12-108">範例 1：取得移動集合的未解析從屬資源清單。</span><span class="sxs-lookup"><span data-stu-id="c0a12-108">Example 1: Get list of unresolved dependent resources for a Move Collection.</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -DependencyLevel Descendant
Count Id                                                                                                                                        
----- --                                                                                                                                        
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111   
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
    3 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm
```

<span data-ttu-id="c0a12-109">取得移動集合的未解析從屬資源清單。</span><span class="sxs-lookup"><span data-stu-id="c0a12-109">Get a list of unresolved dependent resources for a Move Collection.</span></span>

## <span data-ttu-id="c0a12-110">參數</span><span class="sxs-lookup"><span data-stu-id="c0a12-110">PARAMETERS</span></span>

### <span data-ttu-id="c0a12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a12-111">-DefaultProfile</span></span>
<span data-ttu-id="c0a12-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0a12-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0a12-113">-DependencyLevel</span><span class="sxs-lookup"><span data-stu-id="c0a12-113">-DependencyLevel</span></span>
<span data-ttu-id="c0a12-114">定義相依性層級。</span><span class="sxs-lookup"><span data-stu-id="c0a12-114">Defines the dependency level.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.DependencyLevel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a12-115">-篩選</span><span class="sxs-lookup"><span data-stu-id="c0a12-115">-Filter</span></span>
<span data-ttu-id="c0a12-116">要適用于作業的篩選。</span><span class="sxs-lookup"><span data-stu-id="c0a12-116">The filter to apply on the operation.</span></span>
<span data-ttu-id="c0a12-117">例如，$apply=filter (eq 2) 。</span><span class="sxs-lookup"><span data-stu-id="c0a12-117">For example, $apply=filter(count eq 2).</span></span>

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

### <span data-ttu-id="c0a12-118">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="c0a12-118">-MoveCollectionName</span></span>
<span data-ttu-id="c0a12-119">移動集合名稱。</span><span class="sxs-lookup"><span data-stu-id="c0a12-119">The Move Collection Name.</span></span>

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

### <span data-ttu-id="c0a12-120">-Orderby</span><span class="sxs-lookup"><span data-stu-id="c0a12-120">-Orderby</span></span>
<span data-ttu-id="c0a12-121">OData 順序的查詢選項。</span><span class="sxs-lookup"><span data-stu-id="c0a12-121">OData order by query option.</span></span>
<span data-ttu-id="c0a12-122">例如，您可以使用 $orderby=Count desc。</span><span class="sxs-lookup"><span data-stu-id="c0a12-122">For example, you can use $orderby=Count desc.</span></span>

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

### <span data-ttu-id="c0a12-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0a12-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0a12-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c0a12-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="c0a12-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0a12-125">-SubscriptionId</span></span>
<span data-ttu-id="c0a12-126">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0a12-126">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a12-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a12-127">CommonParameters</span></span>
<span data-ttu-id="c0a12-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c0a12-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a12-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0a12-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a12-130">輸入</span><span class="sxs-lookup"><span data-stu-id="c0a12-130">INPUTS</span></span>

## <span data-ttu-id="c0a12-131">輸出</span><span class="sxs-lookup"><span data-stu-id="c0a12-131">OUTPUTS</span></span>

### <span data-ttu-id="c0a12-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.models.Api202101.IUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="c0a12-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IUnresolvedDependency</span></span>

## <span data-ttu-id="c0a12-133">筆記</span><span class="sxs-lookup"><span data-stu-id="c0a12-133">NOTES</span></span>

<span data-ttu-id="c0a12-134">別名</span><span class="sxs-lookup"><span data-stu-id="c0a12-134">ALIASES</span></span>

## <span data-ttu-id="c0a12-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0a12-135">RELATED LINKS</span></span>

