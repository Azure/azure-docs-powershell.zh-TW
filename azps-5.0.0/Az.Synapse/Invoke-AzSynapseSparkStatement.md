---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138055"
---
# <span data-ttu-id="c24f4-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="c24f4-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="c24f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c24f4-102">SYNOPSIS</span></span>
<span data-ttu-id="c24f4-103">調用 Synapse 分析 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="c24f4-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="c24f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="c24f4-104">SYNTAX</span></span>

### <span data-ttu-id="c24f4-105">RunSparkStatementByCodePathParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c24f4-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24f4-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="c24f4-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24f4-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c24f4-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c24f4-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c24f4-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c24f4-109">說明</span><span class="sxs-lookup"><span data-stu-id="c24f4-109">DESCRIPTION</span></span>
<span data-ttu-id="c24f4-110">**AzSynapseSparkStatement** Cmdlet 會呼叫 Synapse 分析 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="c24f4-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="c24f4-111">示例</span><span class="sxs-lookup"><span data-stu-id="c24f4-111">EXAMPLES</span></span>

### <span data-ttu-id="c24f4-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c24f4-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="c24f4-113">這些命令會啟動 Spark 會話，然後透過管線喚醒呼叫內嵌 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="c24f4-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="c24f4-114">範例2</span><span class="sxs-lookup"><span data-stu-id="c24f4-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="c24f4-115">這些命令會啟動 Spark 會話，然後喚醒呼叫內嵌的 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="c24f4-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="c24f4-116">範例3</span><span class="sxs-lookup"><span data-stu-id="c24f4-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="c24f4-117">這些命令會啟動 Spark 會話，然後在檔案中呼叫 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="c24f4-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="c24f4-118">參數</span><span class="sxs-lookup"><span data-stu-id="c24f4-118">PARAMETERS</span></span>

### <span data-ttu-id="c24f4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c24f4-119">-AsJob</span></span>
<span data-ttu-id="c24f4-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c24f4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c24f4-121">-程式碼</span><span class="sxs-lookup"><span data-stu-id="c24f4-121">-Code</span></span>
<span data-ttu-id="c24f4-122">執行程式碼。</span><span class="sxs-lookup"><span data-stu-id="c24f4-122">The execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeParameterSet, RunSparkStatementByCodeAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24f4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24f4-123">-DefaultProfile</span></span>
<span data-ttu-id="c24f4-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c24f4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c24f4-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="c24f4-125">-FilePath</span></span>
<span data-ttu-id="c24f4-126">指定包含執行程式碼的本機檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="c24f4-126">Specifies a local file path that contains the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24f4-127">-語言</span><span class="sxs-lookup"><span data-stu-id="c24f4-127">-Language</span></span>
<span data-ttu-id="c24f4-128">執行程式碼的語言。</span><span class="sxs-lookup"><span data-stu-id="c24f4-128">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24f4-129">-回應</span><span class="sxs-lookup"><span data-stu-id="c24f4-129">-Response</span></span>
<span data-ttu-id="c24f4-130">表示應傳回完整回應。</span><span class="sxs-lookup"><span data-stu-id="c24f4-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="c24f4-131">-SessionId</span><span class="sxs-lookup"><span data-stu-id="c24f4-131">-SessionId</span></span>
<span data-ttu-id="c24f4-132">Spark 會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c24f4-132">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24f4-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="c24f4-133">-SessionObject</span></span>
<span data-ttu-id="c24f4-134">觸發會話輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="c24f4-134">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c24f4-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="c24f4-135">-SparkPoolName</span></span>
<span data-ttu-id="c24f4-136">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="c24f4-136">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24f4-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c24f4-137">-WorkspaceName</span></span>
<span data-ttu-id="c24f4-138">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="c24f4-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24f4-139">-確認</span><span class="sxs-lookup"><span data-stu-id="c24f4-139">-Confirm</span></span>
<span data-ttu-id="c24f4-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c24f4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c24f4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c24f4-141">-WhatIf</span></span>
<span data-ttu-id="c24f4-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c24f4-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c24f4-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c24f4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c24f4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c24f4-144">CommonParameters</span></span>
<span data-ttu-id="c24f4-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c24f4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c24f4-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c24f4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c24f4-147">輸入</span><span class="sxs-lookup"><span data-stu-id="c24f4-147">INPUTS</span></span>

### <span data-ttu-id="c24f4-148">System.object</span><span class="sxs-lookup"><span data-stu-id="c24f4-148">System.String</span></span>

### <span data-ttu-id="c24f4-149">PSSynapseSparkSession 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="c24f4-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="c24f4-150">輸出</span><span class="sxs-lookup"><span data-stu-id="c24f4-150">OUTPUTS</span></span>

### <span data-ttu-id="c24f4-151">PSSynapseExtendedSparkStatement 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="c24f4-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="c24f4-152">筆記</span><span class="sxs-lookup"><span data-stu-id="c24f4-152">NOTES</span></span>

## <span data-ttu-id="c24f4-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="c24f4-153">RELATED LINKS</span></span>
