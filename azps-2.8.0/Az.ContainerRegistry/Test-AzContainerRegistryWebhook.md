---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4d3a6cef78a644f5448b2825b77ef1d2beabac63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613055"
---
# <span data-ttu-id="bcaad-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="bcaad-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="bcaad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcaad-102">SYNOPSIS</span></span>
<span data-ttu-id="bcaad-103">觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="bcaad-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="bcaad-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcaad-104">SYNTAX</span></span>

### <span data-ttu-id="bcaad-105">ResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bcaad-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bcaad-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcaad-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcaad-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcaad-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcaad-108">說明</span><span class="sxs-lookup"><span data-stu-id="bcaad-108">DESCRIPTION</span></span>
<span data-ttu-id="bcaad-109">Test-AzContainerRegistryWebhook Cmdlet 會觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="bcaad-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="bcaad-110">示例</span><span class="sxs-lookup"><span data-stu-id="bcaad-110">EXAMPLES</span></span>

### <span data-ttu-id="bcaad-111">範例1：觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="bcaad-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="bcaad-112">觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="bcaad-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="bcaad-113">參數</span><span class="sxs-lookup"><span data-stu-id="bcaad-113">PARAMETERS</span></span>

### <span data-ttu-id="bcaad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcaad-114">-DefaultProfile</span></span>
<span data-ttu-id="bcaad-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcaad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcaad-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="bcaad-116">-Name</span></span>
<span data-ttu-id="bcaad-117">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="bcaad-117">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcaad-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="bcaad-118">-RegistryName</span></span>
<span data-ttu-id="bcaad-119">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="bcaad-119">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcaad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcaad-120">-ResourceGroupName</span></span>
<span data-ttu-id="bcaad-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="bcaad-121">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcaad-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcaad-122">-ResourceId</span></span>
<span data-ttu-id="bcaad-123">容器登錄 Webhook 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bcaad-123">The container registry Webhook resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcaad-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="bcaad-124">-Webhook</span></span>
<span data-ttu-id="bcaad-125">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="bcaad-125">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcaad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcaad-126">CommonParameters</span></span>
<span data-ttu-id="bcaad-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcaad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcaad-128">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bcaad-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcaad-129">輸入</span><span class="sxs-lookup"><span data-stu-id="bcaad-129">INPUTS</span></span>

### <span data-ttu-id="bcaad-130">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bcaad-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="bcaad-131">System.object</span><span class="sxs-lookup"><span data-stu-id="bcaad-131">System.String</span></span>

## <span data-ttu-id="bcaad-132">輸出</span><span class="sxs-lookup"><span data-stu-id="bcaad-132">OUTPUTS</span></span>

### <span data-ttu-id="bcaad-133">PSContainerRegistryEventInfo 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bcaad-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="bcaad-134">筆記</span><span class="sxs-lookup"><span data-stu-id="bcaad-134">NOTES</span></span>

## <span data-ttu-id="bcaad-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcaad-135">RELATED LINKS</span></span>

[<span data-ttu-id="bcaad-136">新-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="bcaad-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="bcaad-137">AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="bcaad-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="bcaad-138">更新-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="bcaad-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="bcaad-139">移除-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="bcaad-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)