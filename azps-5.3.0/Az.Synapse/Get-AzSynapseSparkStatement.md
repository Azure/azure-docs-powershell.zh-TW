---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288291"
---
# <span data-ttu-id="a882f-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="a882f-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="a882f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a882f-102">SYNOPSIS</span></span>
<span data-ttu-id="a882f-103">取得 Synapse 分析 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="a882f-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="a882f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a882f-104">SYNTAX</span></span>

### <span data-ttu-id="a882f-105">GetSparkStatementsByIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a882f-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a882f-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a882f-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a882f-107">說明</span><span class="sxs-lookup"><span data-stu-id="a882f-107">DESCRIPTION</span></span>
<span data-ttu-id="a882f-108">**AzSynapseSparkStatement** Cmdlet 會取得有關 Azure Synapse 分析 Spark 語句的資訊。</span><span class="sxs-lookup"><span data-stu-id="a882f-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="a882f-109">示例</span><span class="sxs-lookup"><span data-stu-id="a882f-109">EXAMPLES</span></span>

### <span data-ttu-id="a882f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a882f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="a882f-111">這個命令會在 Spark 會話下取得所有的 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="a882f-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="a882f-112">範例2</span><span class="sxs-lookup"><span data-stu-id="a882f-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="a882f-113">這個命令會取得具有指定 livy 識別碼的 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="a882f-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="a882f-114">範例3</span><span class="sxs-lookup"><span data-stu-id="a882f-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="a882f-115">這個命令會透過管線透過觸發會話來取得所有的 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="a882f-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="a882f-116">參數</span><span class="sxs-lookup"><span data-stu-id="a882f-116">PARAMETERS</span></span>

### <span data-ttu-id="a882f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a882f-117">-DefaultProfile</span></span>
<span data-ttu-id="a882f-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a882f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a882f-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="a882f-119">-LivyId</span></span>
<span data-ttu-id="a882f-120">Spark 語句的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a882f-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="a882f-121">-SessionId</span><span class="sxs-lookup"><span data-stu-id="a882f-121">-SessionId</span></span>
<span data-ttu-id="a882f-122">Spark 會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a882f-122">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a882f-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="a882f-123">-SessionObject</span></span>
<span data-ttu-id="a882f-124">Spark 池輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="a882f-124">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a882f-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="a882f-125">-SparkPoolName</span></span>
<span data-ttu-id="a882f-126">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="a882f-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a882f-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a882f-127">-WorkspaceName</span></span>
<span data-ttu-id="a882f-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a882f-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a882f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a882f-129">CommonParameters</span></span>
<span data-ttu-id="a882f-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a882f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a882f-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a882f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a882f-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a882f-132">INPUTS</span></span>

### <span data-ttu-id="a882f-133">PSSynapseSparkSession 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a882f-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="a882f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a882f-134">OUTPUTS</span></span>

### <span data-ttu-id="a882f-135">PSSynapseSparkStatement 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a882f-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="a882f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a882f-136">NOTES</span></span>

## <span data-ttu-id="a882f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="a882f-137">RELATED LINKS</span></span>
