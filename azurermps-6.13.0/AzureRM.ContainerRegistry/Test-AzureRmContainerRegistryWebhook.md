---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a5894a411f4ffb5b3bde28db68961d321584e1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623760"
---
# <span data-ttu-id="fb699-101">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fb699-101">Test-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="fb699-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb699-102">SYNOPSIS</span></span>
<span data-ttu-id="fb699-103">觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="fb699-103">Triggers a webhook ping event.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb699-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb699-104">SYNTAX</span></span>

### <span data-ttu-id="fb699-105">ResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fb699-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb699-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb699-106">NameResourceGroupParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb699-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb699-107">WebhookObjectParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb699-108">說明</span><span class="sxs-lookup"><span data-stu-id="fb699-108">DESCRIPTION</span></span>
<span data-ttu-id="fb699-109">Test-AzureRmContainerRegistryWebhook Cmdlet 會觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="fb699-109">The Test-AzureRmContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="fb699-110">示例</span><span class="sxs-lookup"><span data-stu-id="fb699-110">EXAMPLES</span></span>

### <span data-ttu-id="fb699-111">範例1：觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="fb699-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="fb699-112">觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="fb699-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="fb699-113">參數</span><span class="sxs-lookup"><span data-stu-id="fb699-113">PARAMETERS</span></span>

### <span data-ttu-id="fb699-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb699-114">-DefaultProfile</span></span>
<span data-ttu-id="fb699-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb699-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb699-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb699-116">-Name</span></span>
<span data-ttu-id="fb699-117">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="fb699-117">Webhook Name.</span></span>

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

### <span data-ttu-id="fb699-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="fb699-118">-RegistryName</span></span>
<span data-ttu-id="fb699-119">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="fb699-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="fb699-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb699-120">-ResourceGroupName</span></span>
<span data-ttu-id="fb699-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="fb699-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="fb699-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb699-122">-ResourceId</span></span>
<span data-ttu-id="fb699-123">容器登錄 Webhook 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fb699-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="fb699-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="fb699-124">-Webhook</span></span>
<span data-ttu-id="fb699-125">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="fb699-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="fb699-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb699-126">CommonParameters</span></span>
<span data-ttu-id="fb699-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb699-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb699-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fb699-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb699-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fb699-129">INPUTS</span></span>

### <span data-ttu-id="fb699-130">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb699-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="fb699-131">參數： Webhook (ByValue) </span><span class="sxs-lookup"><span data-stu-id="fb699-131">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="fb699-132">System.object</span><span class="sxs-lookup"><span data-stu-id="fb699-132">System.String</span></span>

## <span data-ttu-id="fb699-133">輸出</span><span class="sxs-lookup"><span data-stu-id="fb699-133">OUTPUTS</span></span>

### <span data-ttu-id="fb699-134">PSContainerRegistryEventInfo 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb699-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="fb699-135">筆記</span><span class="sxs-lookup"><span data-stu-id="fb699-135">NOTES</span></span>

## <span data-ttu-id="fb699-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb699-136">RELATED LINKS</span></span>

[<span data-ttu-id="fb699-137">新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fb699-137">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="fb699-138">AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fb699-138">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="fb699-139">更新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fb699-139">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="fb699-140">移除-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fb699-140">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
