---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 284974cc2d4cb98519b82c5c5a50e40d323dc354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908409"
---
# <span data-ttu-id="a2dd1-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="a2dd1-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="a2dd1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a2dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="a2dd1-103">會返回觸發程式執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="a2dd1-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="a2dd1-104">語法</span><span class="sxs-lookup"><span data-stu-id="a2dd1-104">SYNTAX</span></span>

### <span data-ttu-id="a2dd1-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a2dd1-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2dd1-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="a2dd1-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2dd1-107">描述</span><span class="sxs-lookup"><span data-stu-id="a2dd1-107">DESCRIPTION</span></span>
<span data-ttu-id="a2dd1-108">**Get-AzSynapseTriggerRun** 命令會針對指定時間範圍內指定的觸發程式，會針對觸發程式執行，以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a2dd1-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="a2dd1-109">例子</span><span class="sxs-lookup"><span data-stu-id="a2dd1-109">EXAMPLES</span></span>

### <span data-ttu-id="a2dd1-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="a2dd1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="a2dd1-111">此命令會顯示在 「2018-09-01T21：00」和「2019-09-01T21：00」之間開始之工作區 ContosoTrigger 執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="a2dd1-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="a2dd1-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="a2dd1-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="a2dd1-113">此命令會顯示在工作區 ContosoWorkspace 中，從 「2018-09-01T21：00」到「2019-09-01T21：00」透過管線開始執行 ContosoTrigger 的資訊。</span><span class="sxs-lookup"><span data-stu-id="a2dd1-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="a2dd1-114">參數</span><span class="sxs-lookup"><span data-stu-id="a2dd1-114">PARAMETERS</span></span>

### <span data-ttu-id="a2dd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2dd1-115">-DefaultProfile</span></span>
<span data-ttu-id="a2dd1-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2dd1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2dd1-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2dd1-117">-Name</span></span>
<span data-ttu-id="a2dd1-118">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="a2dd1-118">The trigger name.</span></span>

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

### <span data-ttu-id="a2dd1-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="a2dd1-119">-RunStartedAfter</span></span>
<span data-ttu-id="a2dd1-120">執行事件更新為 'ISO 8601' 格式的時間。</span><span class="sxs-lookup"><span data-stu-id="a2dd1-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="a2dd1-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="a2dd1-121">-RunStartedBefore</span></span>
<span data-ttu-id="a2dd1-122">以 'ISO 8601' 格式更新執行事件的時間。</span><span class="sxs-lookup"><span data-stu-id="a2dd1-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="a2dd1-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a2dd1-123">-WorkspaceName</span></span>
<span data-ttu-id="a2dd1-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2dd1-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a2dd1-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a2dd1-125">-WorkspaceObject</span></span>
<span data-ttu-id="a2dd1-126">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="a2dd1-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a2dd1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2dd1-127">CommonParameters</span></span>
<span data-ttu-id="a2dd1-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a2dd1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2dd1-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2dd1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2dd1-130">輸入</span><span class="sxs-lookup"><span data-stu-id="a2dd1-130">INPUTS</span></span>

### <span data-ttu-id="a2dd1-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a2dd1-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a2dd1-132">輸出</span><span class="sxs-lookup"><span data-stu-id="a2dd1-132">OUTPUTS</span></span>

### <span data-ttu-id="a2dd1-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="a2dd1-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="a2dd1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="a2dd1-134">NOTES</span></span>

## <span data-ttu-id="a2dd1-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2dd1-135">RELATED LINKS</span></span>
