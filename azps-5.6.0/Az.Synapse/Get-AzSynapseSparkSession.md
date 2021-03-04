---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: efe733250c43d79aa8296db380ac453d44231c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916840"
---
# <span data-ttu-id="e5feb-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="e5feb-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="e5feb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e5feb-102">SYNOPSIS</span></span>
<span data-ttu-id="e5feb-103">獲得 Synapse Analytics Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="e5feb-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="e5feb-104">語法</span><span class="sxs-lookup"><span data-stu-id="e5feb-104">SYNTAX</span></span>

### <span data-ttu-id="e5feb-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e5feb-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5feb-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5feb-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5feb-107">描述</span><span class="sxs-lookup"><span data-stu-id="e5feb-107">DESCRIPTION</span></span>
<span data-ttu-id="e5feb-108">**Get-AzSynapseSparkSession** Cmdlet 會取得 Azure Synapse Analytics Spark 會話相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e5feb-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="e5feb-109">例子</span><span class="sxs-lookup"><span data-stu-id="e5feb-109">EXAMPLES</span></span>

### <span data-ttu-id="e5feb-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="e5feb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="e5feb-111">此命令會獲得指定的 Spark 資料庫下的所有 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="e5feb-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="e5feb-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="e5feb-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="e5feb-113">此命令會獲得具有指定 利忘識別碼的 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="e5feb-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="e5feb-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="e5feb-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="e5feb-115">此命令會透過管線，在指定的 Spark 區段下，獲得所有 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="e5feb-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="e5feb-116">參數</span><span class="sxs-lookup"><span data-stu-id="e5feb-116">PARAMETERS</span></span>

### <span data-ttu-id="e5feb-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e5feb-117">-ApplicationId</span></span>
<span data-ttu-id="e5feb-118">會話的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5feb-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="e5feb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5feb-119">-DefaultProfile</span></span>
<span data-ttu-id="e5feb-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5feb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5feb-121">-利維Id</span><span class="sxs-lookup"><span data-stu-id="e5feb-121">-LivyId</span></span>
<span data-ttu-id="e5feb-122">Spark 會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5feb-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="e5feb-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5feb-123">-Name</span></span>
<span data-ttu-id="e5feb-124">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5feb-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="e5feb-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="e5feb-125">-SparkPoolName</span></span>
<span data-ttu-id="e5feb-126">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5feb-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="e5feb-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="e5feb-127">-SparkPoolObject</span></span>
<span data-ttu-id="e5feb-128">Spark Pool 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="e5feb-128">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e5feb-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e5feb-129">-WorkspaceName</span></span>
<span data-ttu-id="e5feb-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5feb-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e5feb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5feb-131">CommonParameters</span></span>
<span data-ttu-id="e5feb-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e5feb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5feb-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5feb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5feb-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e5feb-134">INPUTS</span></span>

### <span data-ttu-id="e5feb-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="e5feb-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="e5feb-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e5feb-136">OUTPUTS</span></span>

### <span data-ttu-id="e5feb-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="e5feb-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="e5feb-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e5feb-138">NOTES</span></span>

## <span data-ttu-id="e5feb-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5feb-139">RELATED LINKS</span></span>
