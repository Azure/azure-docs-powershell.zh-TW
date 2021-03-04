---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: 601ab4b0602a83b708418c626eb48695e18eb7c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912193"
---
# <span data-ttu-id="61314-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="61314-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="61314-102">簡介</span><span class="sxs-lookup"><span data-stu-id="61314-102">SYNOPSIS</span></span>
<span data-ttu-id="61314-103">取消 Synapse Analytics Spark 工作。</span><span class="sxs-lookup"><span data-stu-id="61314-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="61314-104">語法</span><span class="sxs-lookup"><span data-stu-id="61314-104">SYNTAX</span></span>

### <span data-ttu-id="61314-105">StopSparkJobByIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="61314-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61314-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61314-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61314-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61314-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61314-108">描述</span><span class="sxs-lookup"><span data-stu-id="61314-108">DESCRIPTION</span></span>
<span data-ttu-id="61314-109">**Stop-AzSynapseSparkJob** Cmdlet 會取消 Synapse Analytics Spark 工作。</span><span class="sxs-lookup"><span data-stu-id="61314-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="61314-110">例子</span><span class="sxs-lookup"><span data-stu-id="61314-110">EXAMPLES</span></span>

### <span data-ttu-id="61314-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="61314-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="61314-112">此命令會取消 Synapse Analytics Spark 工作。</span><span class="sxs-lookup"><span data-stu-id="61314-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="61314-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="61314-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="61314-114">此命令會取消透過管線的 Synapse Analytics Spark 工作。</span><span class="sxs-lookup"><span data-stu-id="61314-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="61314-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="61314-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="61314-116">此命令會取消透過管線的 Synapse Analytics Spark 工作。</span><span class="sxs-lookup"><span data-stu-id="61314-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="61314-117">參數</span><span class="sxs-lookup"><span data-stu-id="61314-117">PARAMETERS</span></span>

### <span data-ttu-id="61314-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61314-118">-DefaultProfile</span></span>
<span data-ttu-id="61314-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="61314-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61314-120">-強制</span><span class="sxs-lookup"><span data-stu-id="61314-120">-Force</span></span>
<span data-ttu-id="61314-121">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="61314-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="61314-122">-利維Id</span><span class="sxs-lookup"><span data-stu-id="61314-122">-LivyId</span></span>
<span data-ttu-id="61314-123">Spark 工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="61314-123">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdParameterSet, StopSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61314-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61314-124">-PassThru</span></span>
<span data-ttu-id="61314-125">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="61314-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="61314-126">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="61314-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="61314-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="61314-127">-SparkJobObject</span></span>
<span data-ttu-id="61314-128">觸發工作輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="61314-128">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61314-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="61314-129">-SparkPoolName</span></span>
<span data-ttu-id="61314-130">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="61314-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61314-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="61314-131">-SparkPoolObject</span></span>
<span data-ttu-id="61314-132">Spark Pool 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="61314-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: StopSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61314-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="61314-133">-WorkspaceName</span></span>
<span data-ttu-id="61314-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="61314-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61314-135">-確認</span><span class="sxs-lookup"><span data-stu-id="61314-135">-Confirm</span></span>
<span data-ttu-id="61314-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="61314-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61314-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61314-137">-WhatIf</span></span>
<span data-ttu-id="61314-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61314-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61314-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61314-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61314-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61314-140">CommonParameters</span></span>
<span data-ttu-id="61314-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="61314-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61314-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61314-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61314-143">輸入</span><span class="sxs-lookup"><span data-stu-id="61314-143">INPUTS</span></span>

### <span data-ttu-id="61314-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="61314-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="61314-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="61314-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="61314-146">輸出</span><span class="sxs-lookup"><span data-stu-id="61314-146">OUTPUTS</span></span>

### <span data-ttu-id="61314-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61314-147">System.Boolean</span></span>

## <span data-ttu-id="61314-148">筆記</span><span class="sxs-lookup"><span data-stu-id="61314-148">NOTES</span></span>

## <span data-ttu-id="61314-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="61314-149">RELATED LINKS</span></span>
