---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: a10ac77515b225c5e5ef06335f9cee1e99ecd3b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914465"
---
# <span data-ttu-id="672a4-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="672a4-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="672a4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="672a4-102">SYNOPSIS</span></span>
<span data-ttu-id="672a4-103">獲得移動集合。</span><span class="sxs-lookup"><span data-stu-id="672a4-103">Gets the move collection.</span></span>

## <span data-ttu-id="672a4-104">語法</span><span class="sxs-lookup"><span data-stu-id="672a4-104">SYNTAX</span></span>

### <span data-ttu-id="672a4-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="672a4-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="672a4-106">獲取</span><span class="sxs-lookup"><span data-stu-id="672a4-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="672a4-107">清單1</span><span class="sxs-lookup"><span data-stu-id="672a4-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="672a4-108">描述</span><span class="sxs-lookup"><span data-stu-id="672a4-108">DESCRIPTION</span></span>
<span data-ttu-id="672a4-109">獲得移動集合。</span><span class="sxs-lookup"><span data-stu-id="672a4-109">Gets the move collection.</span></span>

## <span data-ttu-id="672a4-110">例子</span><span class="sxs-lookup"><span data-stu-id="672a4-110">EXAMPLES</span></span>

### <span data-ttu-id="672a4-111">範例 1：取得訂閱中所有 Move 集合的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="672a4-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"270119e0-0000-0c00-0000-5f5c94940000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"39015ed4-0000-0c00-0000-5f5ce2760000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections
"1000b505-0000-0c00-0000-5f69db6e0000" centraluseuap MoveCollection-cus-eus-ccy         Microsoft.Migrate/moveCollections


```

<span data-ttu-id="672a4-112">取得訂閱中所有移動集合的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="672a4-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="672a4-113">範例 2：取得訂閱中具有指定移動集合名稱的 Move 集合詳細資料</span><span class="sxs-lookup"><span data-stu-id="672a4-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -Name "PS-centralus-westcentralus-demoRMS"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="672a4-114">取得訂閱中具有指定移動集合名稱的 Move 集合詳細資料。</span><span class="sxs-lookup"><span data-stu-id="672a4-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="672a4-115">範例 3：取得訂閱中具有指定資源組名的 Move 集合詳細資料</span><span class="sxs-lookup"><span data-stu-id="672a4-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"4e02b0a9-0000-0c00-0000-5fd101cc0000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="672a4-116">取得訂閱中具有指定資源組名的移動集合詳細資料。</span><span class="sxs-lookup"><span data-stu-id="672a4-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="672a4-117">參數</span><span class="sxs-lookup"><span data-stu-id="672a4-117">PARAMETERS</span></span>

### <span data-ttu-id="672a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="672a4-118">-DefaultProfile</span></span>
<span data-ttu-id="672a4-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="672a4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="672a4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="672a4-120">-Name</span></span>
<span data-ttu-id="672a4-121">移動集合名稱。</span><span class="sxs-lookup"><span data-stu-id="672a4-121">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="672a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="672a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="672a4-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="672a4-123">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="672a4-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="672a4-124">-SubscriptionId</span></span>
<span data-ttu-id="672a4-125">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="672a4-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="672a4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="672a4-126">CommonParameters</span></span>
<span data-ttu-id="672a4-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="672a4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="672a4-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="672a4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="672a4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="672a4-129">INPUTS</span></span>

## <span data-ttu-id="672a4-130">輸出</span><span class="sxs-lookup"><span data-stu-id="672a4-130">OUTPUTS</span></span>

### <span data-ttu-id="672a4-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="672a4-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="672a4-132">筆記</span><span class="sxs-lookup"><span data-stu-id="672a4-132">NOTES</span></span>

<span data-ttu-id="672a4-133">別名</span><span class="sxs-lookup"><span data-stu-id="672a4-133">ALIASES</span></span>

## <span data-ttu-id="672a4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="672a4-134">RELATED LINKS</span></span>

