---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 73bb67577a9160440c2e42e1e5b3259ad8435c5c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128840"
---
# <span data-ttu-id="5bfaf-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="5bfaf-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="5bfaf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5bfaf-102">SYNOPSIS</span></span>
<span data-ttu-id="5bfaf-103">取得移動集合。</span><span class="sxs-lookup"><span data-stu-id="5bfaf-103">Gets the move collection.</span></span>

## <span data-ttu-id="5bfaf-104">句法</span><span class="sxs-lookup"><span data-stu-id="5bfaf-104">SYNTAX</span></span>

### <span data-ttu-id="5bfaf-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="5bfaf-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5bfaf-106">獲取</span><span class="sxs-lookup"><span data-stu-id="5bfaf-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5bfaf-107">List1</span><span class="sxs-lookup"><span data-stu-id="5bfaf-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5bfaf-108">說明</span><span class="sxs-lookup"><span data-stu-id="5bfaf-108">DESCRIPTION</span></span>
<span data-ttu-id="5bfaf-109">取得移動集合。</span><span class="sxs-lookup"><span data-stu-id="5bfaf-109">Gets the move collection.</span></span>

## <span data-ttu-id="5bfaf-110">示例</span><span class="sxs-lookup"><span data-stu-id="5bfaf-110">EXAMPLES</span></span>

### <span data-ttu-id="5bfaf-111">範例1：取得訂閱中所有移動集合的詳細資料</span><span class="sxs-lookup"><span data-stu-id="5bfaf-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId e80eb9fa-c996-4435-aa32-5af6f3d3077c

Location    Name                                            Type
--------    ----                                            ----
eastus2     mvcolle2e07001                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e34745                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e56720                                  Microsoft.Migrate/moveCollections


```

<span data-ttu-id="5bfaf-112">取得訂閱中所有移動集合的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5bfaf-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="5bfaf-113">範例2：在訂閱中取得指定移動集合名稱的移動集合詳細資料</span><span class="sxs-lookup"><span data-stu-id="5bfaf-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM -Name PS-centralus-westcentralus-demoRM

Location    Name                              Type
--------    ----                              ----
eastus2     PS-centralus-westcentralus-demoRM Microsoft.Migrate/moveCollections

```

<span data-ttu-id="5bfaf-114">取得訂閱中指定的移動收藏名稱的移動集合詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5bfaf-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="5bfaf-115">範例3：在訂閱中取得指定資源組名稱的移動集合詳細資料</span><span class="sxs-lookup"><span data-stu-id="5bfaf-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
eastus2euap PS-centralus-westcentralus-demoRM2 Microsoft.Migrate/moveCollections


```

<span data-ttu-id="5bfaf-116">在訂閱中取得指定資源群組名稱的移動集合詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5bfaf-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="5bfaf-117">參數</span><span class="sxs-lookup"><span data-stu-id="5bfaf-117">PARAMETERS</span></span>

### <span data-ttu-id="5bfaf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bfaf-118">-DefaultProfile</span></span>
<span data-ttu-id="5bfaf-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5bfaf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bfaf-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="5bfaf-120">-Name</span></span>
<span data-ttu-id="5bfaf-121">[移動集合名稱]。</span><span class="sxs-lookup"><span data-stu-id="5bfaf-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="5bfaf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bfaf-122">-ResourceGroupName</span></span>
<span data-ttu-id="5bfaf-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bfaf-123">The Resource Group Name.</span></span>

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

### <span data-ttu-id="5bfaf-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5bfaf-124">-SubscriptionId</span></span>
<span data-ttu-id="5bfaf-125">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="5bfaf-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="5bfaf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bfaf-126">CommonParameters</span></span>
<span data-ttu-id="5bfaf-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5bfaf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bfaf-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5bfaf-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bfaf-129">輸入</span><span class="sxs-lookup"><span data-stu-id="5bfaf-129">INPUTS</span></span>

## <span data-ttu-id="5bfaf-130">輸出</span><span class="sxs-lookup"><span data-stu-id="5bfaf-130">OUTPUTS</span></span>

### <span data-ttu-id="5bfaf-131">IMoveCollection （ResourceMover）。 Api20191001Preview。</span><span class="sxs-lookup"><span data-stu-id="5bfaf-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="5bfaf-132">筆記</span><span class="sxs-lookup"><span data-stu-id="5bfaf-132">NOTES</span></span>

<span data-ttu-id="5bfaf-133">別名</span><span class="sxs-lookup"><span data-stu-id="5bfaf-133">ALIASES</span></span>

## <span data-ttu-id="5bfaf-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bfaf-134">RELATED LINKS</span></span>

