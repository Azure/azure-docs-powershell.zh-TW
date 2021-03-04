---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 60fdd8223f073ffd6de76db659e6bd989f48fada
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914101"
---
# <span data-ttu-id="e1926-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="e1926-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="e1926-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e1926-102">SYNOPSIS</span></span>
<span data-ttu-id="e1926-103">如果工作在可取消的狀態，則取消進行中的資料箱工作。</span><span class="sxs-lookup"><span data-stu-id="e1926-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="e1926-104">語法</span><span class="sxs-lookup"><span data-stu-id="e1926-104">SYNTAX</span></span>

### <span data-ttu-id="e1926-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e1926-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1926-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1926-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1926-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1926-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1926-108">描述</span><span class="sxs-lookup"><span data-stu-id="e1926-108">DESCRIPTION</span></span>
<span data-ttu-id="e1926-109">**Stop-AzDataBoxJob** Cmdlet 是用來取消資料箱工作。</span><span class="sxs-lookup"><span data-stu-id="e1926-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="e1926-110">例子</span><span class="sxs-lookup"><span data-stu-id="e1926-110">EXAMPLES</span></span>

### <span data-ttu-id="e1926-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="e1926-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="e1926-112">取消指定的資料箱工作</span><span class="sxs-lookup"><span data-stu-id="e1926-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="e1926-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="e1926-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="e1926-114">在未確認的情況下強制取消指定的資料箱工作</span><span class="sxs-lookup"><span data-stu-id="e1926-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="e1926-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="e1926-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="e1926-116">取消指定的資料箱工作</span><span class="sxs-lookup"><span data-stu-id="e1926-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="e1926-117">參數</span><span class="sxs-lookup"><span data-stu-id="e1926-117">PARAMETERS</span></span>

### <span data-ttu-id="e1926-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1926-118">-DefaultProfile</span></span>
<span data-ttu-id="e1926-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1926-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1926-120">-強制</span><span class="sxs-lookup"><span data-stu-id="e1926-120">-Force</span></span>
<span data-ttu-id="e1926-121">強制停止而不確認</span><span class="sxs-lookup"><span data-stu-id="e1926-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="e1926-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1926-122">-InputObject</span></span>
<span data-ttu-id="e1926-123">類型 PSDataBoxJob 的 InputObject</span><span class="sxs-lookup"><span data-stu-id="e1926-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="e1926-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1926-124">-Name</span></span>
<span data-ttu-id="e1926-125">資料箱工作名稱</span><span class="sxs-lookup"><span data-stu-id="e1926-125">Databox Job Name</span></span>

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

### <span data-ttu-id="e1926-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1926-126">-PassThru</span></span>
<span data-ttu-id="e1926-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="e1926-127">PassThru</span></span>

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

### <span data-ttu-id="e1926-128">-原因</span><span class="sxs-lookup"><span data-stu-id="e1926-128">-Reason</span></span>
<span data-ttu-id="e1926-129">取消原因</span><span class="sxs-lookup"><span data-stu-id="e1926-129">Reason For Cancellation</span></span>

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

### <span data-ttu-id="e1926-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1926-130">-ResourceGroupName</span></span>
<span data-ttu-id="e1926-131">資料箱工作資源組名</span><span class="sxs-lookup"><span data-stu-id="e1926-131">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="e1926-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1926-132">-ResourceId</span></span>
<span data-ttu-id="e1926-133">資料箱資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e1926-133">Databox Resource Id</span></span>

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

### <span data-ttu-id="e1926-134">-確認</span><span class="sxs-lookup"><span data-stu-id="e1926-134">-Confirm</span></span>
<span data-ttu-id="e1926-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e1926-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1926-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1926-136">-WhatIf</span></span>
<span data-ttu-id="e1926-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1926-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1926-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1926-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1926-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1926-139">CommonParameters</span></span>
<span data-ttu-id="e1926-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e1926-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1926-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1926-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1926-142">輸入</span><span class="sxs-lookup"><span data-stu-id="e1926-142">INPUTS</span></span>

### <span data-ttu-id="e1926-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e1926-143">System.String</span></span>

## <span data-ttu-id="e1926-144">輸出</span><span class="sxs-lookup"><span data-stu-id="e1926-144">OUTPUTS</span></span>

### <span data-ttu-id="e1926-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="e1926-145">System.Void</span></span>

## <span data-ttu-id="e1926-146">筆記</span><span class="sxs-lookup"><span data-stu-id="e1926-146">NOTES</span></span>

## <span data-ttu-id="e1926-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1926-147">RELATED LINKS</span></span>
