---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: cccc0d3cffd9eb313e2983d81a3492bdf89e9e44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142383"
---
# <span data-ttu-id="6b9ae-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="6b9ae-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="6b9ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6b9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="6b9ae-103">重設 Synapse Analytics Spark 會話的超時。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="6b9ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="6b9ae-104">SYNTAX</span></span>

### <span data-ttu-id="6b9ae-105">ResetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6b9ae-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b9ae-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b9ae-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b9ae-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b9ae-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b9ae-108">說明</span><span class="sxs-lookup"><span data-stu-id="6b9ae-108">DESCRIPTION</span></span>
<span data-ttu-id="6b9ae-109">**AzSynapseSparkSessionTimeout** Cmdlet 會重設 Synapse 分析 Spark 會話的超時。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="6b9ae-110">示例</span><span class="sxs-lookup"><span data-stu-id="6b9ae-110">EXAMPLES</span></span>

### <span data-ttu-id="6b9ae-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6b9ae-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="6b9ae-112">這個命令會將 Synapse 分析 Spark 會話的超時重設為指定的 livy ID。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="6b9ae-113">範例2</span><span class="sxs-lookup"><span data-stu-id="6b9ae-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="6b9ae-114">這個命令會透過管線將 Synapse Analytics Spark 會話的超時重設為指定的 livy ID。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="6b9ae-115">範例3</span><span class="sxs-lookup"><span data-stu-id="6b9ae-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="6b9ae-116">這個命令會透過管線將 Synapse Analytics Spark 會話的超時重設為指定的 livy ID。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="6b9ae-117">參數</span><span class="sxs-lookup"><span data-stu-id="6b9ae-117">PARAMETERS</span></span>

### <span data-ttu-id="6b9ae-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b9ae-118">-AsJob</span></span>
<span data-ttu-id="6b9ae-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6b9ae-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b9ae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b9ae-120">-DefaultProfile</span></span>
<span data-ttu-id="6b9ae-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b9ae-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b9ae-122">-InputObject</span></span>
<span data-ttu-id="6b9ae-123">觸發會話輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: ResetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b9ae-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="6b9ae-124">-LivyId</span></span>
<span data-ttu-id="6b9ae-125">Spark 會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResetByNameParameterSet, ResetByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b9ae-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b9ae-126">-PassThru</span></span>
<span data-ttu-id="6b9ae-127">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="6b9ae-128">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6b9ae-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="6b9ae-129">-SparkPoolName</span></span>
<span data-ttu-id="6b9ae-130">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b9ae-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="6b9ae-131">-SparkPoolObject</span></span>
<span data-ttu-id="6b9ae-132">Spark 池輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: ResetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b9ae-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6b9ae-133">-WorkspaceName</span></span>
<span data-ttu-id="6b9ae-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b9ae-135">-確認</span><span class="sxs-lookup"><span data-stu-id="6b9ae-135">-Confirm</span></span>
<span data-ttu-id="6b9ae-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b9ae-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b9ae-137">-WhatIf</span></span>
<span data-ttu-id="6b9ae-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b9ae-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b9ae-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b9ae-140">CommonParameters</span></span>
<span data-ttu-id="6b9ae-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b9ae-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b9ae-143">輸入</span><span class="sxs-lookup"><span data-stu-id="6b9ae-143">INPUTS</span></span>

### <span data-ttu-id="6b9ae-144">PSSynapseSparkPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="6b9ae-145">PSSynapseSparkSession 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6b9ae-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="6b9ae-146">輸出</span><span class="sxs-lookup"><span data-stu-id="6b9ae-146">OUTPUTS</span></span>

### <span data-ttu-id="6b9ae-147">System.object</span><span class="sxs-lookup"><span data-stu-id="6b9ae-147">System.Boolean</span></span>

## <span data-ttu-id="6b9ae-148">筆記</span><span class="sxs-lookup"><span data-stu-id="6b9ae-148">NOTES</span></span>

## <span data-ttu-id="6b9ae-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b9ae-149">RELATED LINKS</span></span>
