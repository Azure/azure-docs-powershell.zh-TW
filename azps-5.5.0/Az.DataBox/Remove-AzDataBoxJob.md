---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 545b99168d421fd9839d42bc8eb0af198dc48042
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141123"
---
# <span data-ttu-id="f5c59-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="f5c59-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="f5c59-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5c59-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c59-103">刪除 databox 工作</span><span class="sxs-lookup"><span data-stu-id="f5c59-103">Deletes the databox job</span></span>

## <span data-ttu-id="f5c59-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5c59-104">SYNTAX</span></span>

### <span data-ttu-id="f5c59-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f5c59-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5c59-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5c59-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5c59-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5c59-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5c59-108">說明</span><span class="sxs-lookup"><span data-stu-id="f5c59-108">DESCRIPTION</span></span>
<span data-ttu-id="f5c59-109">**AzDataBoxJob** Cmdlet 可用來從 databox 工作清單中刪除已完成的 databox 作業。</span><span class="sxs-lookup"><span data-stu-id="f5c59-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="f5c59-110">示例</span><span class="sxs-lookup"><span data-stu-id="f5c59-110">EXAMPLES</span></span>

### <span data-ttu-id="f5c59-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f5c59-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="f5c59-112">刪除指定的 databox 工作</span><span class="sxs-lookup"><span data-stu-id="f5c59-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="f5c59-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f5c59-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="f5c59-114">不需確認就能強制刪除指定的 databox 工作</span><span class="sxs-lookup"><span data-stu-id="f5c59-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="f5c59-115">範例3</span><span class="sxs-lookup"><span data-stu-id="f5c59-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="f5c59-116">刪除指定的 databox 工作</span><span class="sxs-lookup"><span data-stu-id="f5c59-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="f5c59-117">參數</span><span class="sxs-lookup"><span data-stu-id="f5c59-117">PARAMETERS</span></span>

### <span data-ttu-id="f5c59-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c59-118">-DefaultProfile</span></span>
<span data-ttu-id="f5c59-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5c59-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5c59-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f5c59-120">-Force</span></span>
<span data-ttu-id="f5c59-121">強制移除但不確認</span><span class="sxs-lookup"><span data-stu-id="f5c59-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="f5c59-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5c59-122">-InputObject</span></span>
<span data-ttu-id="f5c59-123">類型 PSDataBoxJob 的 InputObject</span><span class="sxs-lookup"><span data-stu-id="f5c59-123">InputObject of type PSDataBoxJob</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5c59-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5c59-124">-Name</span></span>
<span data-ttu-id="f5c59-125">Databox 工作名稱</span><span class="sxs-lookup"><span data-stu-id="f5c59-125">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5c59-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5c59-126">-PassThru</span></span>
<span data-ttu-id="f5c59-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="f5c59-127">PassThru</span></span>

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

### <span data-ttu-id="f5c59-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5c59-128">-ResourceGroupName</span></span>
<span data-ttu-id="f5c59-129">Databox 工作資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f5c59-129">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5c59-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5c59-130">-ResourceId</span></span>
<span data-ttu-id="f5c59-131">Databox 工作資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f5c59-131">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5c59-132">-確認</span><span class="sxs-lookup"><span data-stu-id="f5c59-132">-Confirm</span></span>
<span data-ttu-id="f5c59-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f5c59-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5c59-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5c59-134">-WhatIf</span></span>
<span data-ttu-id="f5c59-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5c59-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5c59-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5c59-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5c59-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c59-137">CommonParameters</span></span>
<span data-ttu-id="f5c59-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5c59-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c59-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f5c59-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c59-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f5c59-140">INPUTS</span></span>

### <span data-ttu-id="f5c59-141">System.object</span><span class="sxs-lookup"><span data-stu-id="f5c59-141">System.String</span></span>

## <span data-ttu-id="f5c59-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f5c59-142">OUTPUTS</span></span>

### <span data-ttu-id="f5c59-143">System.void</span><span class="sxs-lookup"><span data-stu-id="f5c59-143">System.Void</span></span>

## <span data-ttu-id="f5c59-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f5c59-144">NOTES</span></span>

## <span data-ttu-id="f5c59-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5c59-145">RELATED LINKS</span></span>
