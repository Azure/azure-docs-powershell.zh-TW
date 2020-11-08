---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127971"
---
# <span data-ttu-id="5ee23-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="5ee23-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="5ee23-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ee23-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee23-103">取得 Synapse 分析 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="5ee23-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="5ee23-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ee23-104">SYNTAX</span></span>

### <span data-ttu-id="5ee23-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5ee23-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ee23-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ee23-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ee23-107">說明</span><span class="sxs-lookup"><span data-stu-id="5ee23-107">DESCRIPTION</span></span>
<span data-ttu-id="5ee23-108">**AzSynapseSparkSession** Cmdlet 會取得 Azure Synapse 分析 Spark 會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5ee23-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="5ee23-109">示例</span><span class="sxs-lookup"><span data-stu-id="5ee23-109">EXAMPLES</span></span>

### <span data-ttu-id="5ee23-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5ee23-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="5ee23-111">這個命令會在指定的 Spark 池中取得所有的 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="5ee23-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="5ee23-112">範例2</span><span class="sxs-lookup"><span data-stu-id="5ee23-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="5ee23-113">這個命令會取得具有指定 livy 識別碼的 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="5ee23-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="5ee23-114">範例3</span><span class="sxs-lookup"><span data-stu-id="5ee23-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="5ee23-115">這個命令會透過管線取得指定 Spark 池中的所有 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="5ee23-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="5ee23-116">參數</span><span class="sxs-lookup"><span data-stu-id="5ee23-116">PARAMETERS</span></span>

### <span data-ttu-id="5ee23-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="5ee23-117">-ApplicationId</span></span>
<span data-ttu-id="5ee23-118">會話的 [應用程式識別碼]。</span><span class="sxs-lookup"><span data-stu-id="5ee23-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="5ee23-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee23-119">-DefaultProfile</span></span>
<span data-ttu-id="5ee23-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ee23-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ee23-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="5ee23-121">-LivyId</span></span>
<span data-ttu-id="5ee23-122">Spark 會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ee23-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="5ee23-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ee23-123">-Name</span></span>
<span data-ttu-id="5ee23-124">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ee23-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="5ee23-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="5ee23-125">-SparkPoolName</span></span>
<span data-ttu-id="5ee23-126">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ee23-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee23-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="5ee23-127">-SparkPoolObject</span></span>
<span data-ttu-id="5ee23-128">Spark 池輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="5ee23-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee23-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5ee23-129">-WorkspaceName</span></span>
<span data-ttu-id="5ee23-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ee23-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee23-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee23-131">CommonParameters</span></span>
<span data-ttu-id="5ee23-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ee23-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee23-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5ee23-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee23-134">輸入</span><span class="sxs-lookup"><span data-stu-id="5ee23-134">INPUTS</span></span>

### <span data-ttu-id="5ee23-135">PSSynapseSparkPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="5ee23-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="5ee23-136">輸出</span><span class="sxs-lookup"><span data-stu-id="5ee23-136">OUTPUTS</span></span>

### <span data-ttu-id="5ee23-137">PSSynapseSparkSession 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="5ee23-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="5ee23-138">筆記</span><span class="sxs-lookup"><span data-stu-id="5ee23-138">NOTES</span></span>

## <span data-ttu-id="5ee23-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ee23-139">RELATED LINKS</span></span>
