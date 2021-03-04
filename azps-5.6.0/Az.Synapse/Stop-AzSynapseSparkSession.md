---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: 204166bc48e01ea186ca18ad5aa95b0dcf05192a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912186"
---
# <span data-ttu-id="b0b98-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="b0b98-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="b0b98-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b0b98-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b98-103">停止 Synapse Analytics Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="b0b98-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="b0b98-104">語法</span><span class="sxs-lookup"><span data-stu-id="b0b98-104">SYNTAX</span></span>

### <span data-ttu-id="b0b98-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b0b98-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0b98-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0b98-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0b98-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0b98-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0b98-108">描述</span><span class="sxs-lookup"><span data-stu-id="b0b98-108">DESCRIPTION</span></span>
<span data-ttu-id="b0b98-109">**Stop-AzSynapseSparkSession** Cmdlet 會停止 Synapse Analytics Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="b0b98-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="b0b98-110">例子</span><span class="sxs-lookup"><span data-stu-id="b0b98-110">EXAMPLES</span></span>

### <span data-ttu-id="b0b98-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b0b98-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="b0b98-112">此命令會停止 Synapse Analytics Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="b0b98-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="b0b98-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="b0b98-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="b0b98-114">此命令會停止透過管線的 Synapse Analytics Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="b0b98-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="b0b98-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="b0b98-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="b0b98-116">此命令會停止透過管線的 Synapse Analytics Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="b0b98-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="b0b98-117">參數</span><span class="sxs-lookup"><span data-stu-id="b0b98-117">PARAMETERS</span></span>

### <span data-ttu-id="b0b98-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0b98-118">-AsJob</span></span>
<span data-ttu-id="b0b98-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b0b98-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0b98-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b98-120">-DefaultProfile</span></span>
<span data-ttu-id="b0b98-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0b98-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0b98-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0b98-122">-InputObject</span></span>
<span data-ttu-id="b0b98-123">Spark 會話輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="b0b98-123">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b0b98-124">-利維Id</span><span class="sxs-lookup"><span data-stu-id="b0b98-124">-LivyId</span></span>
<span data-ttu-id="b0b98-125">Spark 會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0b98-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="b0b98-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0b98-126">-PassThru</span></span>
<span data-ttu-id="b0b98-127">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="b0b98-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="b0b98-128">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="b0b98-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b0b98-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="b0b98-129">-SparkPoolName</span></span>
<span data-ttu-id="b0b98-130">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0b98-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="b0b98-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="b0b98-131">-SparkPoolObject</span></span>
<span data-ttu-id="b0b98-132">Spark Pool 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="b0b98-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b0b98-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b0b98-133">-WorkspaceName</span></span>
<span data-ttu-id="b0b98-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0b98-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b0b98-135">-確認</span><span class="sxs-lookup"><span data-stu-id="b0b98-135">-Confirm</span></span>
<span data-ttu-id="b0b98-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b0b98-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0b98-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0b98-137">-WhatIf</span></span>
<span data-ttu-id="b0b98-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b0b98-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0b98-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0b98-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0b98-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b98-140">CommonParameters</span></span>
<span data-ttu-id="b0b98-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b0b98-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b98-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0b98-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b98-143">輸入</span><span class="sxs-lookup"><span data-stu-id="b0b98-143">INPUTS</span></span>

### <span data-ttu-id="b0b98-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="b0b98-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="b0b98-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="b0b98-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="b0b98-146">輸出</span><span class="sxs-lookup"><span data-stu-id="b0b98-146">OUTPUTS</span></span>

### <span data-ttu-id="b0b98-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b0b98-147">System.Boolean</span></span>

## <span data-ttu-id="b0b98-148">筆記</span><span class="sxs-lookup"><span data-stu-id="b0b98-148">NOTES</span></span>

## <span data-ttu-id="b0b98-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0b98-149">RELATED LINKS</span></span>
