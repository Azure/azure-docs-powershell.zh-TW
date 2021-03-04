---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c205354b68def88b00fb67959669633d5ba1fc1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914449"
---
# <span data-ttu-id="80401-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="80401-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="80401-102">簡介</span><span class="sxs-lookup"><span data-stu-id="80401-102">SYNOPSIS</span></span>
<span data-ttu-id="80401-103">承諾要求內內容中包含的一組資源。</span><span class="sxs-lookup"><span data-stu-id="80401-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="80401-104">在 moveState 'CommitPending' 或 'CommitFailed' 的 moveResources 上觸發該提交作業，在成功完成時，moveResource moveState 會進行移轉至已提交。</span><span class="sxs-lookup"><span data-stu-id="80401-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="80401-105">為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。</span><span class="sxs-lookup"><span data-stu-id="80401-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="80401-106">語法</span><span class="sxs-lookup"><span data-stu-id="80401-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80401-107">描述</span><span class="sxs-lookup"><span data-stu-id="80401-107">DESCRIPTION</span></span>
<span data-ttu-id="80401-108">承諾要求內內容中包含的一組資源。</span><span class="sxs-lookup"><span data-stu-id="80401-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="80401-109">在 moveState 'CommitPending' 或 'CommitFailed' 的 moveResources 上觸發該提交作業，在成功完成時，moveResource moveState 會進行移轉至已提交。</span><span class="sxs-lookup"><span data-stu-id="80401-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="80401-110">為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。</span><span class="sxs-lookup"><span data-stu-id="80401-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="80401-111">例子</span><span class="sxs-lookup"><span data-stu-id="80401-111">EXAMPLES</span></span>

### <span data-ttu-id="80401-112">範例 1：在確認資源之前，先驗證信賴。</span><span class="sxs-lookup"><span data-stu-id="80401-112">Example 1: Validate the dependecies before commit of the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:38:26 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/c194298b-b2eb-4aab-80b4-129d1473b75c
Message        : 
Name           : c194298b-b2eb-4aab-80b4-129d1473b75c
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:38:25 PM
Status         : Succeeded

```

<span data-ttu-id="80401-113">確認資源之前，先驗證其可靠性。</span><span class="sxs-lookup"><span data-stu-id="80401-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="80401-114">範例 2：使用「MoveResource Name」做為輸入，在 Move 集合中確定一組資源。</span><span class="sxs-lookup"><span data-stu-id="80401-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:41:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/80c04850-7f3f-4e9c-aa68-b868978b59f3
Message        : 
Name           : 80c04850-7f3f-4e9c-aa68-b868978b59f3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:41:05 PM
Status         : Succeeded


```

<span data-ttu-id="80401-115">使用「MoveResource 名稱」做為輸入，在移動集合中確定一組資源。</span><span class="sxs-lookup"><span data-stu-id="80401-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="80401-116">範例 3：使用 "SourceARMID" 做為輸入，在 Move 集合中確定一組資源。</span><span class="sxs-lookup"><span data-stu-id="80401-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:42:46 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d36ca519-8ced-48c9-a968-cb5e9c4db731
Message        : 
Name           : d36ca519-8ced-48c9-a968-cb5e9c4db731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:42:41 PM
Status         : Succeeded


```

<span data-ttu-id="80401-117">使用「SourceARMID」做為輸入，在移動集合中承諾一組資源。</span><span class="sxs-lookup"><span data-stu-id="80401-117">Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="80401-118">參數</span><span class="sxs-lookup"><span data-stu-id="80401-118">PARAMETERS</span></span>

### <span data-ttu-id="80401-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80401-119">-AsJob</span></span>
<span data-ttu-id="80401-120">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="80401-120">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80401-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80401-121">-DefaultProfile</span></span>
<span data-ttu-id="80401-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="80401-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80401-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="80401-123">-MoveCollectionName</span></span>
<span data-ttu-id="80401-124">移動集合名稱。</span><span class="sxs-lookup"><span data-stu-id="80401-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="80401-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="80401-125">-MoveResource</span></span>
<span data-ttu-id="80401-126">根據預設，它會接受移動資源識別碼的清單，除非輸入類型是透過 moveResourceInputType 屬性切換。</span><span class="sxs-lookup"><span data-stu-id="80401-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80401-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="80401-127">-MoveResourceInputType</span></span>
<span data-ttu-id="80401-128">定義移動資源輸入類型。</span><span class="sxs-lookup"><span data-stu-id="80401-128">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80401-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="80401-129">-NoWait</span></span>
<span data-ttu-id="80401-130">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="80401-130">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80401-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80401-131">-ResourceGroupName</span></span>
<span data-ttu-id="80401-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="80401-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="80401-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80401-133">-SubscriptionId</span></span>
<span data-ttu-id="80401-134">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="80401-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="80401-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="80401-135">-ValidateOnly</span></span>
<span data-ttu-id="80401-136">獲取或設定一個值，指出該作業是否需要執行先決條件。</span><span class="sxs-lookup"><span data-stu-id="80401-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80401-137">-確認</span><span class="sxs-lookup"><span data-stu-id="80401-137">-Confirm</span></span>
<span data-ttu-id="80401-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="80401-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80401-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80401-139">-WhatIf</span></span>
<span data-ttu-id="80401-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80401-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80401-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80401-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80401-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80401-142">CommonParameters</span></span>
<span data-ttu-id="80401-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="80401-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80401-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80401-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80401-145">輸入</span><span class="sxs-lookup"><span data-stu-id="80401-145">INPUTS</span></span>

## <span data-ttu-id="80401-146">輸出</span><span class="sxs-lookup"><span data-stu-id="80401-146">OUTPUTS</span></span>

### <span data-ttu-id="80401-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="80401-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="80401-148">筆記</span><span class="sxs-lookup"><span data-stu-id="80401-148">NOTES</span></span>

<span data-ttu-id="80401-149">別名</span><span class="sxs-lookup"><span data-stu-id="80401-149">ALIASES</span></span>

## <span data-ttu-id="80401-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="80401-150">RELATED LINKS</span></span>

