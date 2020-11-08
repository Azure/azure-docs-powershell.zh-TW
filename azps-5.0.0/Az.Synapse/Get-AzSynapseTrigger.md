---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 9e39d6458ca330909e500a45532d0a9d66f404af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139363"
---
# <span data-ttu-id="d01a5-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="d01a5-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="d01a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d01a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d01a5-103">取得有關工作區中觸發程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="d01a5-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="d01a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d01a5-104">SYNTAX</span></span>

### <span data-ttu-id="d01a5-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="d01a5-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d01a5-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="d01a5-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d01a5-107">說明</span><span class="sxs-lookup"><span data-stu-id="d01a5-107">DESCRIPTION</span></span>
<span data-ttu-id="d01a5-108">AzSynapseTrigger Cmdlet 會取得有關工作區中觸發 **程式** 的資訊。</span><span class="sxs-lookup"><span data-stu-id="d01a5-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="d01a5-109">如果您指定了觸發程式的名稱，此 Cmdlet 會取得該觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d01a5-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="d01a5-110">如果您沒有指定名稱，此 Cmdlet 會取得有關工作區中所有觸發程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="d01a5-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="d01a5-111">示例</span><span class="sxs-lookup"><span data-stu-id="d01a5-111">EXAMPLES</span></span>

### <span data-ttu-id="d01a5-112">範例1</span><span class="sxs-lookup"><span data-stu-id="d01a5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d01a5-113">取得已在工作區 ContosoWorkspace 中建立之所有觸發程式的清單。</span><span class="sxs-lookup"><span data-stu-id="d01a5-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="d01a5-114">範例2</span><span class="sxs-lookup"><span data-stu-id="d01a5-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="d01a5-115">在工作區 ContosoWorkspace 中取得名為 ContosoTrigger 的單一觸發程式。</span><span class="sxs-lookup"><span data-stu-id="d01a5-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="d01a5-116">範例3</span><span class="sxs-lookup"><span data-stu-id="d01a5-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="d01a5-117">在工作區 ContosoWorkspace 透過管線中取得單一觸發程式（稱為 ContosoTrigger）。</span><span class="sxs-lookup"><span data-stu-id="d01a5-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d01a5-118">參數</span><span class="sxs-lookup"><span data-stu-id="d01a5-118">PARAMETERS</span></span>

### <span data-ttu-id="d01a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d01a5-119">-DefaultProfile</span></span>
<span data-ttu-id="d01a5-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d01a5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d01a5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d01a5-121">-Name</span></span>
<span data-ttu-id="d01a5-122">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="d01a5-122">The trigger name.</span></span>

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

### <span data-ttu-id="d01a5-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d01a5-123">-WorkspaceName</span></span>
<span data-ttu-id="d01a5-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="d01a5-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d01a5-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d01a5-125">-WorkspaceObject</span></span>
<span data-ttu-id="d01a5-126">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="d01a5-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d01a5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d01a5-127">CommonParameters</span></span>
<span data-ttu-id="d01a5-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d01a5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d01a5-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d01a5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d01a5-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d01a5-130">INPUTS</span></span>

### <span data-ttu-id="d01a5-131">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="d01a5-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d01a5-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d01a5-132">OUTPUTS</span></span>

### <span data-ttu-id="d01a5-133">PSTriggerResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="d01a5-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="d01a5-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d01a5-134">NOTES</span></span>

## <span data-ttu-id="d01a5-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d01a5-135">RELATED LINKS</span></span>
