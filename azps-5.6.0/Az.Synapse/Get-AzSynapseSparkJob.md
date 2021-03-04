---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: ea330bad812c7718d464a2ee237aa8c20c1f653f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912238"
---
# <span data-ttu-id="012be-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="012be-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="012be-102">簡介</span><span class="sxs-lookup"><span data-stu-id="012be-102">SYNOPSIS</span></span>
<span data-ttu-id="012be-103">獲得 Synapse Analytics Spark 工作。</span><span class="sxs-lookup"><span data-stu-id="012be-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="012be-104">語法</span><span class="sxs-lookup"><span data-stu-id="012be-104">SYNTAX</span></span>

### <span data-ttu-id="012be-105">GetSparkJobsByIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="012be-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="012be-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="012be-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="012be-107">描述</span><span class="sxs-lookup"><span data-stu-id="012be-107">DESCRIPTION</span></span>
<span data-ttu-id="012be-108">**Get-AzSynapseSparkJob** Cmdlet 會取得 Azure Synapse Analytics Spark 工作。</span><span class="sxs-lookup"><span data-stu-id="012be-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="012be-109">如果您未指定工作，此 Cmdlet 會獲得所有工作。</span><span class="sxs-lookup"><span data-stu-id="012be-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="012be-110">例子</span><span class="sxs-lookup"><span data-stu-id="012be-110">EXAMPLES</span></span>

### <span data-ttu-id="012be-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="012be-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="012be-112">此命令會獲得 Spark 資料區下的所有工作。</span><span class="sxs-lookup"><span data-stu-id="012be-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="012be-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="012be-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="012be-114">此命令會以指定的識別碼獲得工作。</span><span class="sxs-lookup"><span data-stu-id="012be-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="012be-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="012be-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="012be-116">此命令會以指定的應用程式識別碼獲得工作。</span><span class="sxs-lookup"><span data-stu-id="012be-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="012be-117">範例 4</span><span class="sxs-lookup"><span data-stu-id="012be-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="012be-118">此命令會透過管線，在 Spark 資料區下獲得所有工作。</span><span class="sxs-lookup"><span data-stu-id="012be-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="012be-119">參數</span><span class="sxs-lookup"><span data-stu-id="012be-119">PARAMETERS</span></span>

### <span data-ttu-id="012be-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="012be-120">-ApplicationId</span></span>
<span data-ttu-id="012be-121">會話的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="012be-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="012be-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="012be-122">-DefaultProfile</span></span>
<span data-ttu-id="012be-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="012be-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="012be-124">-利維Id</span><span class="sxs-lookup"><span data-stu-id="012be-124">-LivyId</span></span>
<span data-ttu-id="012be-125">Spark 工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="012be-125">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="012be-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="012be-126">-Name</span></span>
<span data-ttu-id="012be-127">Spark 工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="012be-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="012be-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="012be-128">-SparkPoolName</span></span>
<span data-ttu-id="012be-129">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="012be-129">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="012be-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="012be-130">-SparkPoolObject</span></span>
<span data-ttu-id="012be-131">Spark Pool 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="012be-131">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="012be-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="012be-132">-WorkspaceName</span></span>
<span data-ttu-id="012be-133">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="012be-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="012be-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="012be-134">CommonParameters</span></span>
<span data-ttu-id="012be-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="012be-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="012be-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="012be-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="012be-137">輸入</span><span class="sxs-lookup"><span data-stu-id="012be-137">INPUTS</span></span>

### <span data-ttu-id="012be-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="012be-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="012be-139">輸出</span><span class="sxs-lookup"><span data-stu-id="012be-139">OUTPUTS</span></span>

### <span data-ttu-id="012be-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="012be-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="012be-141">筆記</span><span class="sxs-lookup"><span data-stu-id="012be-141">NOTES</span></span>

## <span data-ttu-id="012be-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="012be-142">RELATED LINKS</span></span>
