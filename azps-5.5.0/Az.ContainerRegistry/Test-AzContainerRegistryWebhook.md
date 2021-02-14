---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1245c92e13af691b0b439d6745a35a917bdf4d89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143302"
---
# <span data-ttu-id="7d26c-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7d26c-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="7d26c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d26c-102">SYNOPSIS</span></span>
<span data-ttu-id="7d26c-103">觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="7d26c-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="7d26c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d26c-104">SYNTAX</span></span>

### <span data-ttu-id="7d26c-105">ResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7d26c-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d26c-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d26c-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d26c-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d26c-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d26c-108">說明</span><span class="sxs-lookup"><span data-stu-id="7d26c-108">DESCRIPTION</span></span>
<span data-ttu-id="7d26c-109">Test-AzContainerRegistryWebhook Cmdlet 會觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="7d26c-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="7d26c-110">示例</span><span class="sxs-lookup"><span data-stu-id="7d26c-110">EXAMPLES</span></span>

### <span data-ttu-id="7d26c-111">範例1：觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="7d26c-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="7d26c-112">觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="7d26c-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="7d26c-113">參數</span><span class="sxs-lookup"><span data-stu-id="7d26c-113">PARAMETERS</span></span>

### <span data-ttu-id="7d26c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d26c-114">-DefaultProfile</span></span>
<span data-ttu-id="7d26c-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d26c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d26c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d26c-116">-Name</span></span>
<span data-ttu-id="7d26c-117">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="7d26c-117">Webhook Name.</span></span>

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

### <span data-ttu-id="7d26c-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="7d26c-118">-RegistryName</span></span>
<span data-ttu-id="7d26c-119">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="7d26c-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="7d26c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d26c-120">-ResourceGroupName</span></span>
<span data-ttu-id="7d26c-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7d26c-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="7d26c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d26c-122">-ResourceId</span></span>
<span data-ttu-id="7d26c-123">容器登錄 Webhook 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7d26c-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="7d26c-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="7d26c-124">-Webhook</span></span>
<span data-ttu-id="7d26c-125">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="7d26c-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="7d26c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d26c-126">CommonParameters</span></span>
<span data-ttu-id="7d26c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d26c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d26c-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7d26c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d26c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="7d26c-129">INPUTS</span></span>

### <span data-ttu-id="7d26c-130">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7d26c-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="7d26c-131">System.object</span><span class="sxs-lookup"><span data-stu-id="7d26c-131">System.String</span></span>

## <span data-ttu-id="7d26c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="7d26c-132">OUTPUTS</span></span>

### <span data-ttu-id="7d26c-133">PSContainerRegistryEventInfo 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7d26c-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="7d26c-134">筆記</span><span class="sxs-lookup"><span data-stu-id="7d26c-134">NOTES</span></span>

## <span data-ttu-id="7d26c-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d26c-135">RELATED LINKS</span></span>

[<span data-ttu-id="7d26c-136">新-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7d26c-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7d26c-137">AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7d26c-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7d26c-138">更新-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7d26c-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7d26c-139">移除-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7d26c-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)