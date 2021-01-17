---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437208"
---
# <span data-ttu-id="90e47-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="90e47-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="90e47-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90e47-102">SYNOPSIS</span></span>
<span data-ttu-id="90e47-103">取得未解析的相依性清單。</span><span class="sxs-lookup"><span data-stu-id="90e47-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="90e47-104">句法</span><span class="sxs-lookup"><span data-stu-id="90e47-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="90e47-105">說明</span><span class="sxs-lookup"><span data-stu-id="90e47-105">DESCRIPTION</span></span>
<span data-ttu-id="90e47-106">取得未解析的相依性清單。</span><span class="sxs-lookup"><span data-stu-id="90e47-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="90e47-107">示例</span><span class="sxs-lookup"><span data-stu-id="90e47-107">EXAMPLES</span></span>

### <span data-ttu-id="90e47-108">範例1：取得未解析相依資源的清單</span><span class="sxs-lookup"><span data-stu-id="90e47-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="90e47-109">取得移動收藏的未解析相依資源清單。</span><span class="sxs-lookup"><span data-stu-id="90e47-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="90e47-110">參數</span><span class="sxs-lookup"><span data-stu-id="90e47-110">PARAMETERS</span></span>

### <span data-ttu-id="90e47-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e47-111">-DefaultProfile</span></span>
<span data-ttu-id="90e47-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90e47-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90e47-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="90e47-113">-MoveCollectionName</span></span>
<span data-ttu-id="90e47-114">[移動集合名稱]。</span><span class="sxs-lookup"><span data-stu-id="90e47-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="90e47-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e47-115">-ResourceGroupName</span></span>
<span data-ttu-id="90e47-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90e47-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="90e47-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90e47-117">-SubscriptionId</span></span>
<span data-ttu-id="90e47-118">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="90e47-118">The Subscription ID.</span></span>

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

### <span data-ttu-id="90e47-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e47-119">CommonParameters</span></span>
<span data-ttu-id="90e47-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90e47-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e47-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="90e47-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e47-122">輸入</span><span class="sxs-lookup"><span data-stu-id="90e47-122">INPUTS</span></span>

## <span data-ttu-id="90e47-123">輸出</span><span class="sxs-lookup"><span data-stu-id="90e47-123">OUTPUTS</span></span>

### <span data-ttu-id="90e47-124">IUnresolvedDependencyCollection （ResourceMover）。 Api20191001Preview。</span><span class="sxs-lookup"><span data-stu-id="90e47-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="90e47-125">筆記</span><span class="sxs-lookup"><span data-stu-id="90e47-125">NOTES</span></span>

<span data-ttu-id="90e47-126">別名</span><span class="sxs-lookup"><span data-stu-id="90e47-126">ALIASES</span></span>

## <span data-ttu-id="90e47-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="90e47-127">RELATED LINKS</span></span>

