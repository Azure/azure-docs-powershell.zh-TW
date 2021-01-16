---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278267"
---
# <span data-ttu-id="72326-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="72326-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="72326-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72326-102">SYNOPSIS</span></span>
<span data-ttu-id="72326-103">取得 Synapse 分析 Spark 作業。</span><span class="sxs-lookup"><span data-stu-id="72326-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="72326-104">句法</span><span class="sxs-lookup"><span data-stu-id="72326-104">SYNTAX</span></span>

### <span data-ttu-id="72326-105">GetSparkJobsByIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="72326-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72326-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72326-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72326-107">說明</span><span class="sxs-lookup"><span data-stu-id="72326-107">DESCRIPTION</span></span>
<span data-ttu-id="72326-108">**AzSynapseSparkJob** Cmdlet 會取得 Azure Synapse 分析 Spark 作業。</span><span class="sxs-lookup"><span data-stu-id="72326-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="72326-109">如果您沒有指定作業，此 Cmdlet 會取得所有作業。</span><span class="sxs-lookup"><span data-stu-id="72326-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="72326-110">示例</span><span class="sxs-lookup"><span data-stu-id="72326-110">EXAMPLES</span></span>

### <span data-ttu-id="72326-111">範例1</span><span class="sxs-lookup"><span data-stu-id="72326-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="72326-112">這個命令會取得 Spark 池下的所有作業。</span><span class="sxs-lookup"><span data-stu-id="72326-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="72326-113">範例2</span><span class="sxs-lookup"><span data-stu-id="72326-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="72326-114">這個命令會取得具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="72326-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="72326-115">範例3</span><span class="sxs-lookup"><span data-stu-id="72326-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="72326-116">這個命令會以指定的應用程式識別碼來取得作業。</span><span class="sxs-lookup"><span data-stu-id="72326-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="72326-117">範例4</span><span class="sxs-lookup"><span data-stu-id="72326-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="72326-118">這個命令會透過管線在 Spark 池底下取得所有作業。</span><span class="sxs-lookup"><span data-stu-id="72326-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="72326-119">參數</span><span class="sxs-lookup"><span data-stu-id="72326-119">PARAMETERS</span></span>

### <span data-ttu-id="72326-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="72326-120">-ApplicationId</span></span>
<span data-ttu-id="72326-121">會話的 [應用程式識別碼]。</span><span class="sxs-lookup"><span data-stu-id="72326-121">The Application identifier of the session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72326-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72326-122">-DefaultProfile</span></span>
<span data-ttu-id="72326-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72326-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72326-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="72326-124">-LivyId</span></span>
<span data-ttu-id="72326-125">Spark 作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="72326-125">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72326-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="72326-126">-Name</span></span>
<span data-ttu-id="72326-127">Spark 作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="72326-127">Name of Spark job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72326-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="72326-128">-SparkPoolName</span></span>
<span data-ttu-id="72326-129">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="72326-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72326-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="72326-130">-SparkPoolObject</span></span>
<span data-ttu-id="72326-131">Spark 池輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="72326-131">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetSparkJobsByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72326-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="72326-132">-WorkspaceName</span></span>
<span data-ttu-id="72326-133">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="72326-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72326-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72326-134">CommonParameters</span></span>
<span data-ttu-id="72326-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72326-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72326-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="72326-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72326-137">輸入</span><span class="sxs-lookup"><span data-stu-id="72326-137">INPUTS</span></span>

### <span data-ttu-id="72326-138">PSSynapseSparkPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="72326-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="72326-139">輸出</span><span class="sxs-lookup"><span data-stu-id="72326-139">OUTPUTS</span></span>

### <span data-ttu-id="72326-140">PSSynapseSparkJob 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="72326-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="72326-141">筆記</span><span class="sxs-lookup"><span data-stu-id="72326-141">NOTES</span></span>

## <span data-ttu-id="72326-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="72326-142">RELATED LINKS</span></span>
