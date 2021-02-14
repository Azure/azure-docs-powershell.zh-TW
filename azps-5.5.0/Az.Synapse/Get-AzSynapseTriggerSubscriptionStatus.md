---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134319"
---
# <span data-ttu-id="21a54-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="21a54-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="21a54-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21a54-102">SYNOPSIS</span></span>
<span data-ttu-id="21a54-103">取得事件觸發程式的訂閱狀態，移至指定的外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="21a54-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="21a54-104">句法</span><span class="sxs-lookup"><span data-stu-id="21a54-104">SYNTAX</span></span>

### <span data-ttu-id="21a54-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="21a54-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21a54-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="21a54-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21a54-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="21a54-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21a54-108">說明</span><span class="sxs-lookup"><span data-stu-id="21a54-108">DESCRIPTION</span></span>
<span data-ttu-id="21a54-109">**AzSynapseTriggerSubscriptionStatus** Cmdlet 會將事件觸發程式的訂閱狀態，取得至指定的外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="21a54-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="21a54-110">在傳回的狀態為「已啟用」前，無法啟動觸發程式。</span><span class="sxs-lookup"><span data-stu-id="21a54-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="21a54-111">示例</span><span class="sxs-lookup"><span data-stu-id="21a54-111">EXAMPLES</span></span>

### <span data-ttu-id="21a54-112">範例1</span><span class="sxs-lookup"><span data-stu-id="21a54-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="21a54-113">這個命令會取得 subscribtion 的觸發程式狀態，稱為 ContosoTrigger 至外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="21a54-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="21a54-114">範例2</span><span class="sxs-lookup"><span data-stu-id="21a54-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="21a54-115">這個命令會透過流水線取得稱為「ContosoTrigger」的觸發程式 subscribtion 的狀態。</span><span class="sxs-lookup"><span data-stu-id="21a54-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="21a54-116">範例3</span><span class="sxs-lookup"><span data-stu-id="21a54-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="21a54-117">這個命令會透過流水線取得稱為「ContosoTrigger」的觸發程式 subscribtion 的狀態。</span><span class="sxs-lookup"><span data-stu-id="21a54-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="21a54-118">參數</span><span class="sxs-lookup"><span data-stu-id="21a54-118">PARAMETERS</span></span>

### <span data-ttu-id="21a54-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a54-119">-DefaultProfile</span></span>
<span data-ttu-id="21a54-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21a54-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21a54-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21a54-121">-InputObject</span></span>
<span data-ttu-id="21a54-122">觸發程式物件。</span><span class="sxs-lookup"><span data-stu-id="21a54-122">The trigger object.</span></span>

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

### <span data-ttu-id="21a54-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="21a54-123">-Name</span></span>
<span data-ttu-id="21a54-124">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="21a54-124">The trigger name.</span></span>

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

### <span data-ttu-id="21a54-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="21a54-125">-WorkspaceName</span></span>
<span data-ttu-id="21a54-126">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="21a54-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="21a54-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="21a54-127">-WorkspaceObject</span></span>
<span data-ttu-id="21a54-128">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="21a54-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="21a54-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a54-129">CommonParameters</span></span>
<span data-ttu-id="21a54-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21a54-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a54-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="21a54-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a54-132">輸入</span><span class="sxs-lookup"><span data-stu-id="21a54-132">INPUTS</span></span>

### <span data-ttu-id="21a54-133">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="21a54-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="21a54-134">PSTriggerResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="21a54-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="21a54-135">輸出</span><span class="sxs-lookup"><span data-stu-id="21a54-135">OUTPUTS</span></span>

### <span data-ttu-id="21a54-136">PSTriggerSubscriptionOperationStatus 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="21a54-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="21a54-137">筆記</span><span class="sxs-lookup"><span data-stu-id="21a54-137">NOTES</span></span>

## <span data-ttu-id="21a54-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="21a54-138">RELATED LINKS</span></span>
