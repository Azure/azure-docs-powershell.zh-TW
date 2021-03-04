---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: e189be8f04081bbc51c5cc19b981c164ce4e9c2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903021"
---
# <span data-ttu-id="fc707-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fc707-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="fc707-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fc707-102">SYNOPSIS</span></span>
<span data-ttu-id="fc707-103">移除容器註冊表網頁。</span><span class="sxs-lookup"><span data-stu-id="fc707-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="fc707-104">語法</span><span class="sxs-lookup"><span data-stu-id="fc707-104">SYNTAX</span></span>

### <span data-ttu-id="fc707-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fc707-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc707-106">Web有ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc707-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc707-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc707-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc707-108">描述</span><span class="sxs-lookup"><span data-stu-id="fc707-108">DESCRIPTION</span></span>
<span data-ttu-id="fc707-109">此Remove-AzContainerRegistryWebhook Cmdlet 會移除容器註冊表網頁。</span><span class="sxs-lookup"><span data-stu-id="fc707-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="fc707-110">例子</span><span class="sxs-lookup"><span data-stu-id="fc707-110">EXAMPLES</span></span>

### <span data-ttu-id="fc707-111">範例 1：移除容器註冊網站。</span><span class="sxs-lookup"><span data-stu-id="fc707-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="fc707-112">移除容器註冊表網頁。</span><span class="sxs-lookup"><span data-stu-id="fc707-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="fc707-113">參數</span><span class="sxs-lookup"><span data-stu-id="fc707-113">PARAMETERS</span></span>

### <span data-ttu-id="fc707-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc707-114">-DefaultProfile</span></span>
<span data-ttu-id="fc707-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc707-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc707-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc707-116">-Name</span></span>
<span data-ttu-id="fc707-117">Web下一個名稱。</span><span class="sxs-lookup"><span data-stu-id="fc707-117">Webhook Name.</span></span>

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

### <span data-ttu-id="fc707-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc707-118">-PassThru</span></span>
<span data-ttu-id="fc707-119">表示移除成功時，此 Cmdlet 會返回 True。</span><span class="sxs-lookup"><span data-stu-id="fc707-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="fc707-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="fc707-120">-RegistryName</span></span>
<span data-ttu-id="fc707-121">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="fc707-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="fc707-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc707-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc707-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="fc707-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="fc707-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc707-124">-ResourceId</span></span>
<span data-ttu-id="fc707-125">容器登錄 Web方資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fc707-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="fc707-126">-Web上</span><span class="sxs-lookup"><span data-stu-id="fc707-126">-Webhook</span></span>
<span data-ttu-id="fc707-127">Container Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="fc707-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="fc707-128">-確認</span><span class="sxs-lookup"><span data-stu-id="fc707-128">-Confirm</span></span>
<span data-ttu-id="fc707-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fc707-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc707-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc707-130">-WhatIf</span></span>
<span data-ttu-id="fc707-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc707-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc707-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc707-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc707-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc707-133">CommonParameters</span></span>
<span data-ttu-id="fc707-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fc707-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc707-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc707-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc707-136">輸入</span><span class="sxs-lookup"><span data-stu-id="fc707-136">INPUTS</span></span>

### <span data-ttu-id="fc707-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="fc707-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="fc707-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fc707-138">System.String</span></span>

## <span data-ttu-id="fc707-139">輸出</span><span class="sxs-lookup"><span data-stu-id="fc707-139">OUTPUTS</span></span>

### <span data-ttu-id="fc707-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fc707-140">System.Boolean</span></span>

## <span data-ttu-id="fc707-141">筆記</span><span class="sxs-lookup"><span data-stu-id="fc707-141">NOTES</span></span>

## <span data-ttu-id="fc707-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc707-142">RELATED LINKS</span></span>

[<span data-ttu-id="fc707-143">New-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="fc707-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fc707-144">Get-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="fc707-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fc707-145">Update-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="fc707-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fc707-146">Test-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="fc707-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)