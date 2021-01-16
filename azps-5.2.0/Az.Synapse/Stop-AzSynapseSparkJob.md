---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278268"
---
# <span data-ttu-id="9ab1c-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="9ab1c-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="9ab1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ab1c-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab1c-103">取消 Synapse 分析 Spark 作業。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="9ab1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ab1c-104">SYNTAX</span></span>

### <span data-ttu-id="9ab1c-105">StopSparkJobByIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9ab1c-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ab1c-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ab1c-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ab1c-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ab1c-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ab1c-108">說明</span><span class="sxs-lookup"><span data-stu-id="9ab1c-108">DESCRIPTION</span></span>
<span data-ttu-id="9ab1c-109">**AzSynapseSparkJob** Cmdlet 會取消 Synapse 分析 Spark 作業。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="9ab1c-110">示例</span><span class="sxs-lookup"><span data-stu-id="9ab1c-110">EXAMPLES</span></span>

### <span data-ttu-id="9ab1c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9ab1c-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="9ab1c-112">這個命令會取消 Synapse 分析 Spark 作業。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="9ab1c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="9ab1c-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="9ab1c-114">這個命令會透過管線取消 Synapse 分析 Spark 作業。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="9ab1c-115">範例3</span><span class="sxs-lookup"><span data-stu-id="9ab1c-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="9ab1c-116">這個命令會透過管線取消 Synapse 分析 Spark 作業。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="9ab1c-117">參數</span><span class="sxs-lookup"><span data-stu-id="9ab1c-117">PARAMETERS</span></span>

### <span data-ttu-id="9ab1c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ab1c-118">-DefaultProfile</span></span>
<span data-ttu-id="9ab1c-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ab1c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9ab1c-120">-Force</span></span>
<span data-ttu-id="9ab1c-121">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9ab1c-122">-LivyId</span><span class="sxs-lookup"><span data-stu-id="9ab1c-122">-LivyId</span></span>
<span data-ttu-id="9ab1c-123">Spark 作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-123">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="9ab1c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ab1c-124">-PassThru</span></span>
<span data-ttu-id="9ab1c-125">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="9ab1c-126">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9ab1c-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="9ab1c-127">-SparkJobObject</span></span>
<span data-ttu-id="9ab1c-128">Spark 作業輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-128">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9ab1c-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="9ab1c-129">-SparkPoolName</span></span>
<span data-ttu-id="9ab1c-130">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="9ab1c-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="9ab1c-131">-SparkPoolObject</span></span>
<span data-ttu-id="9ab1c-132">Spark 池輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9ab1c-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9ab1c-133">-WorkspaceName</span></span>
<span data-ttu-id="9ab1c-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9ab1c-135">-確認</span><span class="sxs-lookup"><span data-stu-id="9ab1c-135">-Confirm</span></span>
<span data-ttu-id="9ab1c-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ab1c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ab1c-137">-WhatIf</span></span>
<span data-ttu-id="9ab1c-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ab1c-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ab1c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab1c-140">CommonParameters</span></span>
<span data-ttu-id="9ab1c-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab1c-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab1c-143">輸入</span><span class="sxs-lookup"><span data-stu-id="9ab1c-143">INPUTS</span></span>

### <span data-ttu-id="9ab1c-144">PSSynapseSparkPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="9ab1c-145">PSSynapseSparkJob 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="9ab1c-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="9ab1c-146">輸出</span><span class="sxs-lookup"><span data-stu-id="9ab1c-146">OUTPUTS</span></span>

### <span data-ttu-id="9ab1c-147">System.object</span><span class="sxs-lookup"><span data-stu-id="9ab1c-147">System.Boolean</span></span>

## <span data-ttu-id="9ab1c-148">筆記</span><span class="sxs-lookup"><span data-stu-id="9ab1c-148">NOTES</span></span>

## <span data-ttu-id="9ab1c-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ab1c-149">RELATED LINKS</span></span>
