---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 0d6d3bb99062177e1d75c4ab496562782cf142c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276579"
---
# <span data-ttu-id="5b262-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="5b262-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="5b262-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b262-102">SYNOPSIS</span></span>
<span data-ttu-id="5b262-103">傳回有關觸發程式執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="5b262-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="5b262-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b262-104">SYNTAX</span></span>

### <span data-ttu-id="5b262-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="5b262-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b262-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="5b262-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b262-107">說明</span><span class="sxs-lookup"><span data-stu-id="5b262-107">DESCRIPTION</span></span>
<span data-ttu-id="5b262-108">[ **取得 AzSynapseTriggerRun** ] 命令會傳回指定的觸發程式在指定時間範圍內觸發程式執行的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5b262-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="5b262-109">示例</span><span class="sxs-lookup"><span data-stu-id="5b262-109">EXAMPLES</span></span>

### <span data-ttu-id="5b262-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5b262-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="5b262-111">這個命令會顯示在 [2018-09-01T21： 00 "和" 2019-09-01T21： 00 "之間開始的工作區 ContosoWorkspace 中的 ContosoTrigger 執行資訊。</span><span class="sxs-lookup"><span data-stu-id="5b262-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="5b262-112">範例2</span><span class="sxs-lookup"><span data-stu-id="5b262-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="5b262-113">這個命令會顯示在工作區 ContosoWorkspace 中，在「2018-09-01T21： 00 "和" 2019-09-01T21： 00 "到管線之間啟動的 ContosoTrigger 中執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="5b262-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="5b262-114">參數</span><span class="sxs-lookup"><span data-stu-id="5b262-114">PARAMETERS</span></span>

### <span data-ttu-id="5b262-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b262-115">-DefaultProfile</span></span>
<span data-ttu-id="5b262-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b262-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b262-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b262-117">-Name</span></span>
<span data-ttu-id="5b262-118">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="5b262-118">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b262-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="5b262-119">-RunStartedAfter</span></span>
<span data-ttu-id="5b262-120">以 "ISO 8601" 格式更新 run 事件的時間或之後。</span><span class="sxs-lookup"><span data-stu-id="5b262-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b262-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="5b262-121">-RunStartedBefore</span></span>
<span data-ttu-id="5b262-122">以 "ISO 8601" 格式更新 run 事件之前或之前的時間。</span><span class="sxs-lookup"><span data-stu-id="5b262-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b262-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5b262-123">-WorkspaceName</span></span>
<span data-ttu-id="5b262-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b262-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b262-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5b262-125">-WorkspaceObject</span></span>
<span data-ttu-id="5b262-126">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="5b262-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b262-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b262-127">CommonParameters</span></span>
<span data-ttu-id="5b262-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b262-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b262-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5b262-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b262-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5b262-130">INPUTS</span></span>

### <span data-ttu-id="5b262-131">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="5b262-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5b262-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5b262-132">OUTPUTS</span></span>

### <span data-ttu-id="5b262-133">PSTriggerRun 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="5b262-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="5b262-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5b262-134">NOTES</span></span>

## <span data-ttu-id="5b262-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b262-135">RELATED LINKS</span></span>
