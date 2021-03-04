---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: c0c1b83f177b568e7058b973b788a633cfefe48c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906454"
---
# <span data-ttu-id="06a62-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="06a62-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="06a62-102">簡介</span><span class="sxs-lookup"><span data-stu-id="06a62-102">SYNOPSIS</span></span>
<span data-ttu-id="06a62-103">取得指定外部服務事件之事件觸發事件的訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="06a62-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="06a62-104">語法</span><span class="sxs-lookup"><span data-stu-id="06a62-104">SYNTAX</span></span>

### <span data-ttu-id="06a62-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="06a62-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06a62-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="06a62-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06a62-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="06a62-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06a62-108">描述</span><span class="sxs-lookup"><span data-stu-id="06a62-108">DESCRIPTION</span></span>
<span data-ttu-id="06a62-109">**Get-AzSynapseTriggerSubscriptionStatus** Cmdlet 會取得指定外部服務事件的事件觸發程式訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="06a62-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="06a62-110">在返回的狀態為「已啟用」之前，無法啟動觸發。</span><span class="sxs-lookup"><span data-stu-id="06a62-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="06a62-111">例子</span><span class="sxs-lookup"><span data-stu-id="06a62-111">EXAMPLES</span></span>

### <span data-ttu-id="06a62-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="06a62-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="06a62-113">此命令會取得外部服務事件的觸發程式 ContosoTri用訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="06a62-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="06a62-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="06a62-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="06a62-115">此命令會透過管道取得外部服務事件的觸發程式訂閱狀態，稱為 ContosoTrigger。</span><span class="sxs-lookup"><span data-stu-id="06a62-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="06a62-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="06a62-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="06a62-117">此命令會透過管道取得外部服務事件的觸發程式訂閱狀態，稱為 ContosoTrigger。</span><span class="sxs-lookup"><span data-stu-id="06a62-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="06a62-118">參數</span><span class="sxs-lookup"><span data-stu-id="06a62-118">PARAMETERS</span></span>

### <span data-ttu-id="06a62-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a62-119">-DefaultProfile</span></span>
<span data-ttu-id="06a62-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="06a62-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06a62-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06a62-121">-InputObject</span></span>
<span data-ttu-id="06a62-122">觸發物件。</span><span class="sxs-lookup"><span data-stu-id="06a62-122">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06a62-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="06a62-123">-Name</span></span>
<span data-ttu-id="06a62-124">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="06a62-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, GetByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a62-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="06a62-125">-WorkspaceName</span></span>
<span data-ttu-id="06a62-126">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="06a62-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="06a62-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="06a62-127">-WorkspaceObject</span></span>
<span data-ttu-id="06a62-128">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="06a62-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="06a62-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a62-129">CommonParameters</span></span>
<span data-ttu-id="06a62-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="06a62-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a62-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06a62-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a62-132">輸入</span><span class="sxs-lookup"><span data-stu-id="06a62-132">INPUTS</span></span>

### <span data-ttu-id="06a62-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="06a62-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="06a62-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="06a62-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="06a62-135">輸出</span><span class="sxs-lookup"><span data-stu-id="06a62-135">OUTPUTS</span></span>

### <span data-ttu-id="06a62-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="06a62-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="06a62-137">筆記</span><span class="sxs-lookup"><span data-stu-id="06a62-137">NOTES</span></span>

## <span data-ttu-id="06a62-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="06a62-138">RELATED LINKS</span></span>
