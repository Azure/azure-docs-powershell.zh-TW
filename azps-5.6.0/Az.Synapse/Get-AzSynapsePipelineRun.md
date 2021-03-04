---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 98c0f5ed1dee4c5cd25c69a1a88e596a2f99a7c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911829"
---
# <span data-ttu-id="16987-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="16987-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="16987-102">簡介</span><span class="sxs-lookup"><span data-stu-id="16987-102">SYNOPSIS</span></span>
<span data-ttu-id="16987-103">瞭解管線執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="16987-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="16987-104">語法</span><span class="sxs-lookup"><span data-stu-id="16987-104">SYNTAX</span></span>

### <span data-ttu-id="16987-105">GetByNameAndId (預設) </span><span class="sxs-lookup"><span data-stu-id="16987-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16987-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="16987-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16987-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="16987-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16987-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="16987-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16987-109">描述</span><span class="sxs-lookup"><span data-stu-id="16987-109">DESCRIPTION</span></span>
<span data-ttu-id="16987-110">**Get-AzSynapsePipelineRun** 命令會針對指定的管線，會返回執行相關資訊。</span><span class="sxs-lookup"><span data-stu-id="16987-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="16987-111">如果指定 PipelineRunId，它會以該識別碼顯示執行詳細資料。</span><span class="sxs-lookup"><span data-stu-id="16987-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="16987-112">如果未指定 PipelineRunId，則會顯示 RunStartedAfter 和 RunStartedBefore 值之間發生之管線的所有執行資訊。</span><span class="sxs-lookup"><span data-stu-id="16987-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="16987-113">例子</span><span class="sxs-lookup"><span data-stu-id="16987-113">EXAMPLES</span></span>

### <span data-ttu-id="16987-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="16987-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="16987-115">此命令會獲得使用 ID "61eb095a-fe23-4591-8a97-fade6c65ca72" 執行管線的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="16987-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="16987-116">參數</span><span class="sxs-lookup"><span data-stu-id="16987-116">PARAMETERS</span></span>

### <span data-ttu-id="16987-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16987-117">-DefaultProfile</span></span>
<span data-ttu-id="16987-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="16987-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16987-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="16987-119">-PipelineName</span></span>
<span data-ttu-id="16987-120">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="16987-120">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16987-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="16987-121">-PipelineRunId</span></span>
<span data-ttu-id="16987-122">管線執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="16987-122">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByObjectAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16987-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="16987-123">-RunStartedAfter</span></span>
<span data-ttu-id="16987-124">執行事件更新為 'ISO 8601' 格式的時間。</span><span class="sxs-lookup"><span data-stu-id="16987-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16987-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="16987-125">-RunStartedBefore</span></span>
<span data-ttu-id="16987-126">以 'ISO 8601' 格式更新執行事件的時間。</span><span class="sxs-lookup"><span data-stu-id="16987-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16987-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="16987-127">-WorkspaceName</span></span>
<span data-ttu-id="16987-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="16987-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByNameAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16987-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="16987-129">-WorkspaceObject</span></span>
<span data-ttu-id="16987-130">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="16987-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObjectAndId, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16987-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16987-131">CommonParameters</span></span>
<span data-ttu-id="16987-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="16987-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16987-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16987-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16987-134">輸入</span><span class="sxs-lookup"><span data-stu-id="16987-134">INPUTS</span></span>

### <span data-ttu-id="16987-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="16987-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="16987-136">輸出</span><span class="sxs-lookup"><span data-stu-id="16987-136">OUTPUTS</span></span>

### <span data-ttu-id="16987-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="16987-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="16987-138">筆記</span><span class="sxs-lookup"><span data-stu-id="16987-138">NOTES</span></span>

## <span data-ttu-id="16987-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="16987-139">RELATED LINKS</span></span>
