---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 62894b5d879febdeeb7c14360c16c66fb8a28ea0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909913"
---
# <span data-ttu-id="cbc73-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="cbc73-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="cbc73-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cbc73-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc73-103">會使用 Synapse Analytics Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="cbc73-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="cbc73-104">語法</span><span class="sxs-lookup"><span data-stu-id="cbc73-104">SYNTAX</span></span>

### <span data-ttu-id="cbc73-105">RunSparkStatementByCodePathParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cbc73-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbc73-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbc73-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbc73-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbc73-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cbc73-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbc73-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbc73-109">描述</span><span class="sxs-lookup"><span data-stu-id="cbc73-109">DESCRIPTION</span></span>
<span data-ttu-id="cbc73-110">**Invoke-AzSynapseSparkStatement Cmdlet** 會調用 Synapse Analytics Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="cbc73-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="cbc73-111">例子</span><span class="sxs-lookup"><span data-stu-id="cbc73-111">EXAMPLES</span></span>

### <span data-ttu-id="cbc73-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="cbc73-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="cbc73-113">這些命令會啟動 Spark 會話，然後透過管線來啟動內嵌 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="cbc73-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="cbc73-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="cbc73-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="cbc73-115">這些命令會啟動 Spark 會話，然後啟動內嵌 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="cbc73-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="cbc73-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="cbc73-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="cbc73-117">這些命令會啟動 Spark 會話，然後在檔案中啟動 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="cbc73-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="cbc73-118">參數</span><span class="sxs-lookup"><span data-stu-id="cbc73-118">PARAMETERS</span></span>

### <span data-ttu-id="cbc73-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbc73-119">-AsJob</span></span>
<span data-ttu-id="cbc73-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cbc73-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbc73-121">-程式碼</span><span class="sxs-lookup"><span data-stu-id="cbc73-121">-Code</span></span>
<span data-ttu-id="cbc73-122">執行程式碼。</span><span class="sxs-lookup"><span data-stu-id="cbc73-122">The execution code.</span></span>

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

### <span data-ttu-id="cbc73-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbc73-123">-DefaultProfile</span></span>
<span data-ttu-id="cbc73-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cbc73-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbc73-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="cbc73-125">-FilePath</span></span>
<span data-ttu-id="cbc73-126">指定包含執行程式碼的一個本地檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="cbc73-126">Specifies a local file path that contains the execution code.</span></span>

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

### <span data-ttu-id="cbc73-127">-語言</span><span class="sxs-lookup"><span data-stu-id="cbc73-127">-Language</span></span>
<span data-ttu-id="cbc73-128">執行程式碼的語言。</span><span class="sxs-lookup"><span data-stu-id="cbc73-128">Language of the execution code.</span></span>

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

### <span data-ttu-id="cbc73-129">-回復</span><span class="sxs-lookup"><span data-stu-id="cbc73-129">-Response</span></span>
<span data-ttu-id="cbc73-130">表示應該會回復完整回應。</span><span class="sxs-lookup"><span data-stu-id="cbc73-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="cbc73-131">-SessionId</span><span class="sxs-lookup"><span data-stu-id="cbc73-131">-SessionId</span></span>
<span data-ttu-id="cbc73-132">Spark 會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbc73-132">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="cbc73-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="cbc73-133">-SessionObject</span></span>
<span data-ttu-id="cbc73-134">Spark 會話輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="cbc73-134">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cbc73-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="cbc73-135">-SparkPoolName</span></span>
<span data-ttu-id="cbc73-136">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbc73-136">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="cbc73-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cbc73-137">-WorkspaceName</span></span>
<span data-ttu-id="cbc73-138">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbc73-138">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cbc73-139">-確認</span><span class="sxs-lookup"><span data-stu-id="cbc73-139">-Confirm</span></span>
<span data-ttu-id="cbc73-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cbc73-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbc73-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbc73-141">-WhatIf</span></span>
<span data-ttu-id="cbc73-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cbc73-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbc73-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbc73-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbc73-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc73-144">CommonParameters</span></span>
<span data-ttu-id="cbc73-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cbc73-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc73-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbc73-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc73-147">輸入</span><span class="sxs-lookup"><span data-stu-id="cbc73-147">INPUTS</span></span>

### <span data-ttu-id="cbc73-148">System.String</span><span class="sxs-lookup"><span data-stu-id="cbc73-148">System.String</span></span>

### <span data-ttu-id="cbc73-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="cbc73-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="cbc73-150">輸出</span><span class="sxs-lookup"><span data-stu-id="cbc73-150">OUTPUTS</span></span>

### <span data-ttu-id="cbc73-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="cbc73-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="cbc73-152">筆記</span><span class="sxs-lookup"><span data-stu-id="cbc73-152">NOTES</span></span>

## <span data-ttu-id="cbc73-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbc73-153">RELATED LINKS</span></span>
