---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 988d2f53ebf0bf69806bf06fedb5e2db31c9d0c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907189"
---
# <span data-ttu-id="8f8f5-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="8f8f5-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="8f8f5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8f8f5-102">SYNOPSIS</span></span>
<span data-ttu-id="8f8f5-103">在工作區中獲得觸發者相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8f8f5-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="8f8f5-104">語法</span><span class="sxs-lookup"><span data-stu-id="8f8f5-104">SYNTAX</span></span>

### <span data-ttu-id="8f8f5-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="8f8f5-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f8f5-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="8f8f5-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f8f5-107">描述</span><span class="sxs-lookup"><span data-stu-id="8f8f5-107">DESCRIPTION</span></span>
<span data-ttu-id="8f8f5-108">**Get-AzSynapseTrigger Cmdlet** 會取得工作區中觸發程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="8f8f5-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="8f8f5-109">如果您指定觸發者的名稱，Cmdlet 會獲得該觸發人的資訊。</span><span class="sxs-lookup"><span data-stu-id="8f8f5-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="8f8f5-110">如果您未指定名稱，Cmdlet 會獲得工作區中所有觸發者的資訊。</span><span class="sxs-lookup"><span data-stu-id="8f8f5-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="8f8f5-111">例子</span><span class="sxs-lookup"><span data-stu-id="8f8f5-111">EXAMPLES</span></span>

### <span data-ttu-id="8f8f5-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="8f8f5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="8f8f5-113">在工作區 ContosoWorkspace 中建立的所有觸發項清單。</span><span class="sxs-lookup"><span data-stu-id="8f8f5-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="8f8f5-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="8f8f5-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="8f8f5-115">在工作區 ContosoWorkspace 中，獲得一個稱為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8f8f5-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="8f8f5-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="8f8f5-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="8f8f5-117">透過管道在工作區 ContosoWorkspace 中，獲得名為 ContosoTrigger 的單一觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8f8f5-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="8f8f5-118">參數</span><span class="sxs-lookup"><span data-stu-id="8f8f5-118">PARAMETERS</span></span>

### <span data-ttu-id="8f8f5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f8f5-119">-DefaultProfile</span></span>
<span data-ttu-id="8f8f5-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f8f5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f8f5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f8f5-121">-Name</span></span>
<span data-ttu-id="8f8f5-122">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="8f8f5-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8f5-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8f8f5-123">-WorkspaceName</span></span>
<span data-ttu-id="8f8f5-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f8f5-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8f8f5-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8f8f5-125">-WorkspaceObject</span></span>
<span data-ttu-id="8f8f5-126">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="8f8f5-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8f8f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f8f5-127">CommonParameters</span></span>
<span data-ttu-id="8f8f5-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8f8f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f8f5-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f8f5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f8f5-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8f8f5-130">INPUTS</span></span>

### <span data-ttu-id="8f8f5-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8f8f5-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8f8f5-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8f8f5-132">OUTPUTS</span></span>

### <span data-ttu-id="8f8f5-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="8f8f5-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="8f8f5-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8f8f5-134">NOTES</span></span>

## <span data-ttu-id="8f8f5-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f8f5-135">RELATED LINKS</span></span>
