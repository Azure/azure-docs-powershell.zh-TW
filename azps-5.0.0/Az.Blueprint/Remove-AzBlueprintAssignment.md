---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137543"
---
# <span data-ttu-id="e10f8-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="e10f8-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="e10f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e10f8-102">SYNOPSIS</span></span>
<span data-ttu-id="e10f8-103">從訂閱或管理群組中移除藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="e10f8-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="e10f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="e10f8-104">SYNTAX</span></span>

### <span data-ttu-id="e10f8-105">BySubscriptionAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="e10f8-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e10f8-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="e10f8-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e10f8-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="e10f8-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e10f8-108">說明</span><span class="sxs-lookup"><span data-stu-id="e10f8-108">DESCRIPTION</span></span>
<span data-ttu-id="e10f8-109">移除已指派給訂閱的藍圖。</span><span class="sxs-lookup"><span data-stu-id="e10f8-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="e10f8-110">示例</span><span class="sxs-lookup"><span data-stu-id="e10f8-110">EXAMPLES</span></span>

### <span data-ttu-id="e10f8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e10f8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="e10f8-112">從指定的訂閱中移除名稱指定的藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="e10f8-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="e10f8-113">在執行命令前，Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e10f8-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="e10f8-114">參數</span><span class="sxs-lookup"><span data-stu-id="e10f8-114">PARAMETERS</span></span>

### <span data-ttu-id="e10f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e10f8-115">-DefaultProfile</span></span>
<span data-ttu-id="e10f8-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e10f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e10f8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e10f8-117">-InputObject</span></span>
<span data-ttu-id="e10f8-118">藍圖指派物件。</span><span class="sxs-lookup"><span data-stu-id="e10f8-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e10f8-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="e10f8-119">-ManagementGroupId</span></span>
<span data-ttu-id="e10f8-120">儲存藍圖分派的管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e10f8-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e10f8-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e10f8-121">-Name</span></span>
<span data-ttu-id="e10f8-122">藍圖作業名稱。</span><span class="sxs-lookup"><span data-stu-id="e10f8-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e10f8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e10f8-123">-PassThru</span></span>
<span data-ttu-id="e10f8-124">設定之後，Cmdlet 會傳回代表已移除藍圖指派的物件。</span><span class="sxs-lookup"><span data-stu-id="e10f8-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="e10f8-125">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e10f8-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e10f8-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e10f8-126">-SubscriptionId</span></span>
<span data-ttu-id="e10f8-127">已部署藍圖指派的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="e10f8-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e10f8-128">-確認</span><span class="sxs-lookup"><span data-stu-id="e10f8-128">-Confirm</span></span>
<span data-ttu-id="e10f8-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e10f8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e10f8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e10f8-130">-WhatIf</span></span>
<span data-ttu-id="e10f8-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e10f8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e10f8-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e10f8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e10f8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e10f8-133">CommonParameters</span></span>
<span data-ttu-id="e10f8-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e10f8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e10f8-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e10f8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e10f8-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e10f8-136">INPUTS</span></span>

### <span data-ttu-id="e10f8-137">System.object</span><span class="sxs-lookup"><span data-stu-id="e10f8-137">System.String</span></span>

### <span data-ttu-id="e10f8-138">PSBlueprintAssignment [] （[]）</span><span class="sxs-lookup"><span data-stu-id="e10f8-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="e10f8-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e10f8-139">OUTPUTS</span></span>

### <span data-ttu-id="e10f8-140">System.object</span><span class="sxs-lookup"><span data-stu-id="e10f8-140">System.Object</span></span>
## <span data-ttu-id="e10f8-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e10f8-141">NOTES</span></span>

## <span data-ttu-id="e10f8-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e10f8-142">RELATED LINKS</span></span>