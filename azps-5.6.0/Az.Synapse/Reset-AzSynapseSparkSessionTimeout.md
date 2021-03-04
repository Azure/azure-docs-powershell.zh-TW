---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: 485558c47fa8b879999777b79341fc855085b81a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907350"
---
# <span data-ttu-id="398e9-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="398e9-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="398e9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="398e9-102">SYNOPSIS</span></span>
<span data-ttu-id="398e9-103">重設 Synapse Analytics Spark 會話的超時。</span><span class="sxs-lookup"><span data-stu-id="398e9-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="398e9-104">語法</span><span class="sxs-lookup"><span data-stu-id="398e9-104">SYNTAX</span></span>

### <span data-ttu-id="398e9-105">ResetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="398e9-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="398e9-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="398e9-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="398e9-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="398e9-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="398e9-108">描述</span><span class="sxs-lookup"><span data-stu-id="398e9-108">DESCRIPTION</span></span>
<span data-ttu-id="398e9-109">**Remove-AzSynapseSparkSessionTimeout** Cmdlet 會重設 Synapse Analytics Spark 會話的超時。</span><span class="sxs-lookup"><span data-stu-id="398e9-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="398e9-110">例子</span><span class="sxs-lookup"><span data-stu-id="398e9-110">EXAMPLES</span></span>

### <span data-ttu-id="398e9-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="398e9-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="398e9-112">此命令會以指定的 利維識別碼重設 Synapse Analytics Spark 會話的超時。</span><span class="sxs-lookup"><span data-stu-id="398e9-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="398e9-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="398e9-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="398e9-114">此命令會重設 Synapse Analytics Spark 會話的超時，以及透過管線指定的 利忘識別碼。</span><span class="sxs-lookup"><span data-stu-id="398e9-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="398e9-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="398e9-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="398e9-116">此命令會重設 Synapse Analytics Spark 會話的超時，以及透過管線指定的 利忘識別碼。</span><span class="sxs-lookup"><span data-stu-id="398e9-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="398e9-117">參數</span><span class="sxs-lookup"><span data-stu-id="398e9-117">PARAMETERS</span></span>

### <span data-ttu-id="398e9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="398e9-118">-AsJob</span></span>
<span data-ttu-id="398e9-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="398e9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="398e9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="398e9-120">-DefaultProfile</span></span>
<span data-ttu-id="398e9-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="398e9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="398e9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="398e9-122">-InputObject</span></span>
<span data-ttu-id="398e9-123">Spark 會話輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="398e9-123">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="398e9-124">-利維Id</span><span class="sxs-lookup"><span data-stu-id="398e9-124">-LivyId</span></span>
<span data-ttu-id="398e9-125">Spark 會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="398e9-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="398e9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="398e9-126">-PassThru</span></span>
<span data-ttu-id="398e9-127">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="398e9-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="398e9-128">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="398e9-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="398e9-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="398e9-129">-SparkPoolName</span></span>
<span data-ttu-id="398e9-130">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="398e9-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="398e9-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="398e9-131">-SparkPoolObject</span></span>
<span data-ttu-id="398e9-132">Spark Pool 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="398e9-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="398e9-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="398e9-133">-WorkspaceName</span></span>
<span data-ttu-id="398e9-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="398e9-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="398e9-135">-確認</span><span class="sxs-lookup"><span data-stu-id="398e9-135">-Confirm</span></span>
<span data-ttu-id="398e9-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="398e9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="398e9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="398e9-137">-WhatIf</span></span>
<span data-ttu-id="398e9-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="398e9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="398e9-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="398e9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="398e9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="398e9-140">CommonParameters</span></span>
<span data-ttu-id="398e9-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="398e9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="398e9-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="398e9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="398e9-143">輸入</span><span class="sxs-lookup"><span data-stu-id="398e9-143">INPUTS</span></span>

### <span data-ttu-id="398e9-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="398e9-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="398e9-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="398e9-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="398e9-146">輸出</span><span class="sxs-lookup"><span data-stu-id="398e9-146">OUTPUTS</span></span>

### <span data-ttu-id="398e9-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="398e9-147">System.Boolean</span></span>

## <span data-ttu-id="398e9-148">筆記</span><span class="sxs-lookup"><span data-stu-id="398e9-148">NOTES</span></span>

## <span data-ttu-id="398e9-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="398e9-149">RELATED LINKS</span></span>
