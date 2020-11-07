---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: c1ba245f83db386e39f9fecf22f95d3681452d7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625601"
---
# <span data-ttu-id="10044-101">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="10044-101">Remove-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="10044-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10044-102">SYNOPSIS</span></span>
<span data-ttu-id="10044-103">移除容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="10044-103">Removes a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10044-104">句法</span><span class="sxs-lookup"><span data-stu-id="10044-104">SYNTAX</span></span>

### <span data-ttu-id="10044-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="10044-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10044-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10044-106">WebhookObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10044-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10044-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10044-108">說明</span><span class="sxs-lookup"><span data-stu-id="10044-108">DESCRIPTION</span></span>
<span data-ttu-id="10044-109">Remove-AzureRmContainerRegistryWebhook Cmdlet 會移除容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="10044-109">The Remove-AzureRmContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="10044-110">示例</span><span class="sxs-lookup"><span data-stu-id="10044-110">EXAMPLES</span></span>

### <span data-ttu-id="10044-111">範例1：移除容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="10044-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="10044-112">移除容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="10044-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="10044-113">參數</span><span class="sxs-lookup"><span data-stu-id="10044-113">PARAMETERS</span></span>

### <span data-ttu-id="10044-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10044-114">-DefaultProfile</span></span>
<span data-ttu-id="10044-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10044-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10044-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="10044-116">-Name</span></span>
<span data-ttu-id="10044-117">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="10044-117">Webhook Name.</span></span>

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

### <span data-ttu-id="10044-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10044-118">-PassThru</span></span>
<span data-ttu-id="10044-119">表示如果移除成功，此 Cmdlet 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="10044-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10044-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="10044-120">-RegistryName</span></span>
<span data-ttu-id="10044-121">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="10044-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="10044-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10044-122">-ResourceGroupName</span></span>
<span data-ttu-id="10044-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="10044-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="10044-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10044-124">-ResourceId</span></span>
<span data-ttu-id="10044-125">容器登錄 Webhook 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="10044-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="10044-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="10044-126">-Webhook</span></span>
<span data-ttu-id="10044-127">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="10044-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="10044-128">-確認</span><span class="sxs-lookup"><span data-stu-id="10044-128">-Confirm</span></span>
<span data-ttu-id="10044-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10044-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10044-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10044-130">-WhatIf</span></span>
<span data-ttu-id="10044-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10044-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10044-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10044-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10044-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10044-133">CommonParameters</span></span>
<span data-ttu-id="10044-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10044-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10044-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10044-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10044-136">輸入</span><span class="sxs-lookup"><span data-stu-id="10044-136">INPUTS</span></span>

### <span data-ttu-id="10044-137">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="10044-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="10044-138">參數： Webhook (ByValue) </span><span class="sxs-lookup"><span data-stu-id="10044-138">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="10044-139">System.object</span><span class="sxs-lookup"><span data-stu-id="10044-139">System.String</span></span>

## <span data-ttu-id="10044-140">輸出</span><span class="sxs-lookup"><span data-stu-id="10044-140">OUTPUTS</span></span>

### <span data-ttu-id="10044-141">System.object</span><span class="sxs-lookup"><span data-stu-id="10044-141">System.Boolean</span></span>

## <span data-ttu-id="10044-142">筆記</span><span class="sxs-lookup"><span data-stu-id="10044-142">NOTES</span></span>

## <span data-ttu-id="10044-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="10044-143">RELATED LINKS</span></span>

[<span data-ttu-id="10044-144">新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="10044-144">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="10044-145">AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="10044-145">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="10044-146">更新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="10044-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="10044-147">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="10044-147">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
