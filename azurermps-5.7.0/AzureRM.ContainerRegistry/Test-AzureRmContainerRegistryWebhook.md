---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 02d16be7c41a95c32d4aa7b6f3231b68c0ba7244
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449907"
---
# <span data-ttu-id="62a4a-101">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="62a4a-101">Test-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="62a4a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="62a4a-103">觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="62a4a-103">Triggers a webhook ping event.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62a4a-104">句法</span><span class="sxs-lookup"><span data-stu-id="62a4a-104">SYNTAX</span></span>

### <span data-ttu-id="62a4a-105">ResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="62a4a-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62a4a-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="62a4a-106">NameResourceGroupParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62a4a-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62a4a-107">WebhookObjectParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62a4a-108">說明</span><span class="sxs-lookup"><span data-stu-id="62a4a-108">DESCRIPTION</span></span>
<span data-ttu-id="62a4a-109">Test-AzureRmContainerRegistryWebhook Cmdlet 會觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="62a4a-109">The Test-AzureRmContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="62a4a-110">示例</span><span class="sxs-lookup"><span data-stu-id="62a4a-110">EXAMPLES</span></span>

### <span data-ttu-id="62a4a-111">範例1：觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="62a4a-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="62a4a-112">觸發 webhook ping 事件。</span><span class="sxs-lookup"><span data-stu-id="62a4a-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="62a4a-113">參數</span><span class="sxs-lookup"><span data-stu-id="62a4a-113">PARAMETERS</span></span>

### <span data-ttu-id="62a4a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a4a-114">-DefaultProfile</span></span>
<span data-ttu-id="62a4a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62a4a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a4a-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="62a4a-116">-Name</span></span>
<span data-ttu-id="62a4a-117">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="62a4a-117">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a4a-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="62a4a-118">-RegistryName</span></span>
<span data-ttu-id="62a4a-119">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="62a4a-119">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a4a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62a4a-120">-ResourceGroupName</span></span>
<span data-ttu-id="62a4a-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="62a4a-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a4a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62a4a-122">-ResourceId</span></span>
<span data-ttu-id="62a4a-123">容器登錄 Webhook 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="62a4a-123">The container registry Webhook resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62a4a-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="62a4a-124">-Webhook</span></span>
<span data-ttu-id="62a4a-125">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="62a4a-125">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62a4a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a4a-126">CommonParameters</span></span>
<span data-ttu-id="62a4a-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62a4a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a4a-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62a4a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a4a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="62a4a-129">INPUTS</span></span>

### <span data-ttu-id="62a4a-130">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="62a4a-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="62a4a-131">System.object</span><span class="sxs-lookup"><span data-stu-id="62a4a-131">System.String</span></span>

## <span data-ttu-id="62a4a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="62a4a-132">OUTPUTS</span></span>

### <span data-ttu-id="62a4a-133">EventInfo 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="62a4a-133">Microsoft.Azure.Management.ContainerRegistry.Models.EventInfo</span></span>

## <span data-ttu-id="62a4a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="62a4a-134">NOTES</span></span>

## <span data-ttu-id="62a4a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="62a4a-135">RELATED LINKS</span></span>

[<span data-ttu-id="62a4a-136">新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="62a4a-136">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="62a4a-137">AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="62a4a-137">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="62a4a-138">更新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="62a4a-138">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="62a4a-139">移除-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="62a4a-139">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
