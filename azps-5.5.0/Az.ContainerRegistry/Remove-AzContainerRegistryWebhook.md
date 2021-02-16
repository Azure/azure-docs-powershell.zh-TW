---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137459"
---
# <span data-ttu-id="7b1b6-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7b1b6-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="7b1b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b1b6-102">SYNOPSIS</span></span>
<span data-ttu-id="7b1b6-103">移除容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="7b1b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b1b6-104">SYNTAX</span></span>

### <span data-ttu-id="7b1b6-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7b1b6-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b1b6-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b1b6-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b1b6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b1b6-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b1b6-108">說明</span><span class="sxs-lookup"><span data-stu-id="7b1b6-108">DESCRIPTION</span></span>
<span data-ttu-id="7b1b6-109">Remove-AzContainerRegistryWebhook Cmdlet 會移除容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="7b1b6-110">示例</span><span class="sxs-lookup"><span data-stu-id="7b1b6-110">EXAMPLES</span></span>

### <span data-ttu-id="7b1b6-111">範例1：移除容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="7b1b6-112">移除容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="7b1b6-113">參數</span><span class="sxs-lookup"><span data-stu-id="7b1b6-113">PARAMETERS</span></span>

### <span data-ttu-id="7b1b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b1b6-114">-DefaultProfile</span></span>
<span data-ttu-id="7b1b6-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b1b6-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b1b6-116">-Name</span></span>
<span data-ttu-id="7b1b6-117">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-117">Webhook Name.</span></span>

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

### <span data-ttu-id="7b1b6-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b1b6-118">-PassThru</span></span>
<span data-ttu-id="7b1b6-119">表示如果移除成功，此 Cmdlet 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="7b1b6-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="7b1b6-120">-RegistryName</span></span>
<span data-ttu-id="7b1b6-121">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="7b1b6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b1b6-122">-ResourceGroupName</span></span>
<span data-ttu-id="7b1b6-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="7b1b6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b1b6-124">-ResourceId</span></span>
<span data-ttu-id="7b1b6-125">容器登錄 Webhook 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7b1b6-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="7b1b6-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="7b1b6-126">-Webhook</span></span>
<span data-ttu-id="7b1b6-127">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="7b1b6-128">-確認</span><span class="sxs-lookup"><span data-stu-id="7b1b6-128">-Confirm</span></span>
<span data-ttu-id="7b1b6-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b1b6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b1b6-130">-WhatIf</span></span>
<span data-ttu-id="7b1b6-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b1b6-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b1b6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b1b6-133">CommonParameters</span></span>
<span data-ttu-id="7b1b6-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b1b6-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7b1b6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b1b6-136">輸入</span><span class="sxs-lookup"><span data-stu-id="7b1b6-136">INPUTS</span></span>

### <span data-ttu-id="7b1b6-137">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7b1b6-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="7b1b6-138">System.object</span><span class="sxs-lookup"><span data-stu-id="7b1b6-138">System.String</span></span>

## <span data-ttu-id="7b1b6-139">輸出</span><span class="sxs-lookup"><span data-stu-id="7b1b6-139">OUTPUTS</span></span>

### <span data-ttu-id="7b1b6-140">System.object</span><span class="sxs-lookup"><span data-stu-id="7b1b6-140">System.Boolean</span></span>

## <span data-ttu-id="7b1b6-141">筆記</span><span class="sxs-lookup"><span data-stu-id="7b1b6-141">NOTES</span></span>

## <span data-ttu-id="7b1b6-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b1b6-142">RELATED LINKS</span></span>

[<span data-ttu-id="7b1b6-143">新-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7b1b6-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7b1b6-144">AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7b1b6-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7b1b6-145">更新-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7b1b6-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7b1b6-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7b1b6-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)