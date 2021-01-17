---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: c13fef9b8d0dbf34b3b31ca4a9a1e405a2583ac7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288044"
---
# <span data-ttu-id="1d5c6-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="1d5c6-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="1d5c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d5c6-102">SYNOPSIS</span></span>
<span data-ttu-id="1d5c6-103">停止 Synapse 分析 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="1d5c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d5c6-104">SYNTAX</span></span>

### <span data-ttu-id="1d5c6-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1d5c6-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d5c6-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d5c6-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d5c6-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d5c6-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d5c6-108">說明</span><span class="sxs-lookup"><span data-stu-id="1d5c6-108">DESCRIPTION</span></span>
<span data-ttu-id="1d5c6-109">**AzSynapseSparkSession** Cmdlet 會停止 Synapse 分析 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="1d5c6-110">示例</span><span class="sxs-lookup"><span data-stu-id="1d5c6-110">EXAMPLES</span></span>

### <span data-ttu-id="1d5c6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1d5c6-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="1d5c6-112">這個命令會停止 Synapse 分析 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="1d5c6-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1d5c6-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="1d5c6-114">這個命令會透過管線停止 Synapse 分析 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="1d5c6-115">範例3</span><span class="sxs-lookup"><span data-stu-id="1d5c6-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="1d5c6-116">這個命令會透過管線停止 Synapse 分析 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="1d5c6-117">參數</span><span class="sxs-lookup"><span data-stu-id="1d5c6-117">PARAMETERS</span></span>

### <span data-ttu-id="1d5c6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d5c6-118">-AsJob</span></span>
<span data-ttu-id="1d5c6-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d5c6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d5c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d5c6-120">-DefaultProfile</span></span>
<span data-ttu-id="1d5c6-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d5c6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d5c6-122">-InputObject</span></span>
<span data-ttu-id="1d5c6-123">觸發會話輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d5c6-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="1d5c6-124">-LivyId</span></span>
<span data-ttu-id="1d5c6-125">Spark 會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d5c6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d5c6-126">-PassThru</span></span>
<span data-ttu-id="1d5c6-127">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="1d5c6-128">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1d5c6-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="1d5c6-129">-SparkPoolName</span></span>
<span data-ttu-id="1d5c6-130">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d5c6-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="1d5c6-131">-SparkPoolObject</span></span>
<span data-ttu-id="1d5c6-132">Spark 池輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d5c6-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1d5c6-133">-WorkspaceName</span></span>
<span data-ttu-id="1d5c6-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d5c6-135">-確認</span><span class="sxs-lookup"><span data-stu-id="1d5c6-135">-Confirm</span></span>
<span data-ttu-id="1d5c6-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d5c6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d5c6-137">-WhatIf</span></span>
<span data-ttu-id="1d5c6-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d5c6-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d5c6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d5c6-140">CommonParameters</span></span>
<span data-ttu-id="1d5c6-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d5c6-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d5c6-143">輸入</span><span class="sxs-lookup"><span data-stu-id="1d5c6-143">INPUTS</span></span>

### <span data-ttu-id="1d5c6-144">PSSynapseSparkPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="1d5c6-145">PSSynapseSparkSession 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="1d5c6-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="1d5c6-146">輸出</span><span class="sxs-lookup"><span data-stu-id="1d5c6-146">OUTPUTS</span></span>

### <span data-ttu-id="1d5c6-147">System.object</span><span class="sxs-lookup"><span data-stu-id="1d5c6-147">System.Boolean</span></span>

## <span data-ttu-id="1d5c6-148">筆記</span><span class="sxs-lookup"><span data-stu-id="1d5c6-148">NOTES</span></span>

## <span data-ttu-id="1d5c6-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d5c6-149">RELATED LINKS</span></span>
