---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverrequiredforresources
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
ms.openlocfilehash: 9aa09de52a6b731fbf57b309fb605c0ba07325da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914457"
---
# <span data-ttu-id="6dea6-101">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="6dea6-101">Get-AzResourceMoverRequiredForResources</span></span>

## <span data-ttu-id="6dea6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6dea6-102">SYNOPSIS</span></span>
<span data-ttu-id="6dea6-103">需要 ARM 資源之移動資源的清單。</span><span class="sxs-lookup"><span data-stu-id="6dea6-103">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="6dea6-104">語法</span><span class="sxs-lookup"><span data-stu-id="6dea6-104">SYNTAX</span></span>

```
Get-AzResourceMoverRequiredForResources -MoveCollectionName <String> -ResourceGroupName <String>
 -SourceId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6dea6-105">描述</span><span class="sxs-lookup"><span data-stu-id="6dea6-105">DESCRIPTION</span></span>
<span data-ttu-id="6dea6-106">需要 ARM 資源之移動資源的清單。</span><span class="sxs-lookup"><span data-stu-id="6dea6-106">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="6dea6-107">例子</span><span class="sxs-lookup"><span data-stu-id="6dea6-107">EXAMPLES</span></span>

### <span data-ttu-id="6dea6-108">範例 1：取得新增所需資源 ARMIDs 的清單，以新增指定的資源。</span><span class="sxs-lookup"><span data-stu-id="6dea6-108">Example 1: Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>
```powershell
PS C:\> Get-AzResourceMoverRequiredForResources -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups"

/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="6dea6-109">取得新增指定資源所需的資源 ARMID 清單。</span><span class="sxs-lookup"><span data-stu-id="6dea6-109">Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>

## <span data-ttu-id="6dea6-110">參數</span><span class="sxs-lookup"><span data-stu-id="6dea6-110">PARAMETERS</span></span>

### <span data-ttu-id="6dea6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dea6-111">-DefaultProfile</span></span>
<span data-ttu-id="6dea6-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6dea6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dea6-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="6dea6-113">-MoveCollectionName</span></span>
<span data-ttu-id="6dea6-114">移動集合名稱。</span><span class="sxs-lookup"><span data-stu-id="6dea6-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="6dea6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dea6-115">-ResourceGroupName</span></span>
<span data-ttu-id="6dea6-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="6dea6-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="6dea6-117">-SourceId</span><span class="sxs-lookup"><span data-stu-id="6dea6-117">-SourceId</span></span>
<span data-ttu-id="6dea6-118">這是 Api 的被調用來源Id。</span><span class="sxs-lookup"><span data-stu-id="6dea6-118">The sourceId for which the api is invoked.</span></span>

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

### <span data-ttu-id="6dea6-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6dea6-119">-SubscriptionId</span></span>
<span data-ttu-id="6dea6-120">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="6dea6-120">The Subscription ID.</span></span>

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

### <span data-ttu-id="6dea6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dea6-121">CommonParameters</span></span>
<span data-ttu-id="6dea6-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6dea6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dea6-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6dea6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dea6-124">輸入</span><span class="sxs-lookup"><span data-stu-id="6dea6-124">INPUTS</span></span>

## <span data-ttu-id="6dea6-125">輸出</span><span class="sxs-lookup"><span data-stu-id="6dea6-125">OUTPUTS</span></span>

### <span data-ttu-id="6dea6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6dea6-126">System.String</span></span>

## <span data-ttu-id="6dea6-127">筆記</span><span class="sxs-lookup"><span data-stu-id="6dea6-127">NOTES</span></span>

<span data-ttu-id="6dea6-128">別名</span><span class="sxs-lookup"><span data-stu-id="6dea6-128">ALIASES</span></span>

## <span data-ttu-id="6dea6-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="6dea6-129">RELATED LINKS</span></span>

