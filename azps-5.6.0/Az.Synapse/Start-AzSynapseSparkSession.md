---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: e7e873638e38ed8c0c561fce5c4cd425be7bafbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912202"
---
# <span data-ttu-id="c099c-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="c099c-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="c099c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c099c-102">SYNOPSIS</span></span>
<span data-ttu-id="c099c-103">啟動 Synapse Analytics Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="c099c-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="c099c-104">語法</span><span class="sxs-lookup"><span data-stu-id="c099c-104">SYNTAX</span></span>

### <span data-ttu-id="c099c-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c099c-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c099c-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c099c-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c099c-107">描述</span><span class="sxs-lookup"><span data-stu-id="c099c-107">DESCRIPTION</span></span>
<span data-ttu-id="c099c-108">**Start-AzSynapseSparkSession** Cmdlet 會啟動 Synapse Analytics Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="c099c-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="c099c-109">例子</span><span class="sxs-lookup"><span data-stu-id="c099c-109">EXAMPLES</span></span>

### <span data-ttu-id="c099c-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="c099c-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="c099c-111">此命令會啟動 Azure Synapse Analytics Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="c099c-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="c099c-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="c099c-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="c099c-113">此命令會透過管線啟動 Azure Synapse Analytics Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="c099c-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="c099c-114">參數</span><span class="sxs-lookup"><span data-stu-id="c099c-114">PARAMETERS</span></span>

### <span data-ttu-id="c099c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c099c-115">-AsJob</span></span>
<span data-ttu-id="c099c-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c099c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c099c-117">-組式</span><span class="sxs-lookup"><span data-stu-id="c099c-117">-Configuration</span></span>
<span data-ttu-id="c099c-118">Spark 組組屬性。</span><span class="sxs-lookup"><span data-stu-id="c099c-118">Spark configuration properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c099c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c099c-119">-DefaultProfile</span></span>
<span data-ttu-id="c099c-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c099c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c099c-121">-執行器計數</span><span class="sxs-lookup"><span data-stu-id="c099c-121">-ExecutorCount</span></span>
<span data-ttu-id="c099c-122">要配置於指定工作之 Spark 區中的執行者數目。</span><span class="sxs-lookup"><span data-stu-id="c099c-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c099c-123">-執行器Size</span><span class="sxs-lookup"><span data-stu-id="c099c-123">-ExecutorSize</span></span>
<span data-ttu-id="c099c-124">要用於指定工作之 Spark 資料集中之執行者的核心和記憶體數目。</span><span class="sxs-lookup"><span data-stu-id="c099c-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c099c-125">-語言</span><span class="sxs-lookup"><span data-stu-id="c099c-125">-Language</span></span>
<span data-ttu-id="c099c-126">執行程式碼的語言。</span><span class="sxs-lookup"><span data-stu-id="c099c-126">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c099c-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="c099c-127">-Name</span></span>
<span data-ttu-id="c099c-128">Spark 會話的名稱。</span><span class="sxs-lookup"><span data-stu-id="c099c-128">Name of Spark session.</span></span>

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

### <span data-ttu-id="c099c-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="c099c-129">-ReferenceFile</span></span>
<span data-ttu-id="c099c-130">用於主要定義檔案中供參考的其他檔案。</span><span class="sxs-lookup"><span data-stu-id="c099c-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="c099c-131">逗號分隔儲存 URI 清單。</span><span class="sxs-lookup"><span data-stu-id="c099c-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="c099c-132">例如 " abfss://filesystem@account.dfs.core.windows.net/file1.txt ， abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="c099c-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c099c-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="c099c-133">-SparkPoolName</span></span>
<span data-ttu-id="c099c-134">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c099c-134">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c099c-135">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="c099c-135">-SparkPoolObject</span></span>
<span data-ttu-id="c099c-136">Spark Pool 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="c099c-136">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c099c-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c099c-137">-WorkspaceName</span></span>
<span data-ttu-id="c099c-138">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="c099c-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c099c-139">-確認</span><span class="sxs-lookup"><span data-stu-id="c099c-139">-Confirm</span></span>
<span data-ttu-id="c099c-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c099c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c099c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c099c-141">-WhatIf</span></span>
<span data-ttu-id="c099c-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c099c-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c099c-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c099c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c099c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c099c-144">CommonParameters</span></span>
<span data-ttu-id="c099c-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c099c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c099c-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c099c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c099c-147">輸入</span><span class="sxs-lookup"><span data-stu-id="c099c-147">INPUTS</span></span>

### <span data-ttu-id="c099c-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c099c-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="c099c-149">輸出</span><span class="sxs-lookup"><span data-stu-id="c099c-149">OUTPUTS</span></span>

### <span data-ttu-id="c099c-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="c099c-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="c099c-151">筆記</span><span class="sxs-lookup"><span data-stu-id="c099c-151">NOTES</span></span>

## <span data-ttu-id="c099c-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="c099c-152">RELATED LINKS</span></span>
