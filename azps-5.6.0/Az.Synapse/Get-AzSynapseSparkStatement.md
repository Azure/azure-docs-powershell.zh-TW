---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: 612ca41bf96a1372cda2b2abe984a56c1ec5411c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917854"
---
# <span data-ttu-id="c9521-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="c9521-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="c9521-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c9521-102">SYNOPSIS</span></span>
<span data-ttu-id="c9521-103">獲得 Synapse Analytics Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="c9521-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="c9521-104">語法</span><span class="sxs-lookup"><span data-stu-id="c9521-104">SYNTAX</span></span>

### <span data-ttu-id="c9521-105">GetSparkStatementsByIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c9521-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9521-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9521-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9521-107">描述</span><span class="sxs-lookup"><span data-stu-id="c9521-107">DESCRIPTION</span></span>
<span data-ttu-id="c9521-108">**Get-AzSynapseSparkStatement Cmdlet** 會取得有關 Azure Synapse Analytics Spark 語句的資訊。</span><span class="sxs-lookup"><span data-stu-id="c9521-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="c9521-109">例子</span><span class="sxs-lookup"><span data-stu-id="c9521-109">EXAMPLES</span></span>

### <span data-ttu-id="c9521-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="c9521-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="c9521-111">此命令會獲得 Spark 會話下的所有 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="c9521-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="c9521-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="c9521-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="c9521-113">此命令會獲得具有指定 利維識別碼的 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="c9521-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="c9521-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="c9521-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="c9521-115">此命令會透過管線，在 Spark 會話下獲得所有 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="c9521-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="c9521-116">參數</span><span class="sxs-lookup"><span data-stu-id="c9521-116">PARAMETERS</span></span>

### <span data-ttu-id="c9521-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9521-117">-DefaultProfile</span></span>
<span data-ttu-id="c9521-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9521-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9521-119">-利維Id</span><span class="sxs-lookup"><span data-stu-id="c9521-119">-LivyId</span></span>
<span data-ttu-id="c9521-120">Spark 語句的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9521-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="c9521-121">-SessionId</span><span class="sxs-lookup"><span data-stu-id="c9521-121">-SessionId</span></span>
<span data-ttu-id="c9521-122">Spark 會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9521-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="c9521-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="c9521-123">-SessionObject</span></span>
<span data-ttu-id="c9521-124">Spark Pool 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="c9521-124">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c9521-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="c9521-125">-SparkPoolName</span></span>
<span data-ttu-id="c9521-126">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9521-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="c9521-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c9521-127">-WorkspaceName</span></span>
<span data-ttu-id="c9521-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9521-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c9521-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9521-129">CommonParameters</span></span>
<span data-ttu-id="c9521-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c9521-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9521-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9521-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9521-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c9521-132">INPUTS</span></span>

### <span data-ttu-id="c9521-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="c9521-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="c9521-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c9521-134">OUTPUTS</span></span>

### <span data-ttu-id="c9521-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="c9521-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="c9521-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c9521-136">NOTES</span></span>

## <span data-ttu-id="c9521-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9521-137">RELATED LINKS</span></span>
