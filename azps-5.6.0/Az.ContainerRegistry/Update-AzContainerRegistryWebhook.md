---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: cede1001f475d820dfec7131a8c86815bd98adb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902985"
---
# <span data-ttu-id="74761-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="74761-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="74761-102">簡介</span><span class="sxs-lookup"><span data-stu-id="74761-102">SYNOPSIS</span></span>
<span data-ttu-id="74761-103">更新容器註冊表網頁。</span><span class="sxs-lookup"><span data-stu-id="74761-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="74761-104">語法</span><span class="sxs-lookup"><span data-stu-id="74761-104">SYNTAX</span></span>

### <span data-ttu-id="74761-105">ResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="74761-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74761-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="74761-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74761-107">Web有ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74761-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74761-108">描述</span><span class="sxs-lookup"><span data-stu-id="74761-108">DESCRIPTION</span></span>
<span data-ttu-id="74761-109">此Update-AzContainerRegistryWebhook Cmdlet 會更新容器註冊表網頁。</span><span class="sxs-lookup"><span data-stu-id="74761-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="74761-110">例子</span><span class="sxs-lookup"><span data-stu-id="74761-110">EXAMPLES</span></span>

### <span data-ttu-id="74761-111">範例 1：更新現有的容器註冊表 Web一。</span><span class="sxs-lookup"><span data-stu-id="74761-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="74761-112">更新現有的容器註冊表網頁。</span><span class="sxs-lookup"><span data-stu-id="74761-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="74761-113">參數</span><span class="sxs-lookup"><span data-stu-id="74761-113">PARAMETERS</span></span>

### <span data-ttu-id="74761-114">-動作</span><span class="sxs-lookup"><span data-stu-id="74761-114">-Action</span></span>
<span data-ttu-id="74761-115">會觸發網頁設計來張貼通知的動作空格分隔清單。</span><span class="sxs-lookup"><span data-stu-id="74761-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74761-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74761-116">-DefaultProfile</span></span>
<span data-ttu-id="74761-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="74761-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74761-118">-頁眉</span><span class="sxs-lookup"><span data-stu-id="74761-118">-Header</span></span>
<span data-ttu-id="74761-119">空格分隔自訂標題，格式為 'key \[ =value \] ' ，會新增加到 web一節通知中。</span><span class="sxs-lookup"><span data-stu-id="74761-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74761-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="74761-120">-Name</span></span>
<span data-ttu-id="74761-121">Web下一個名稱。</span><span class="sxs-lookup"><span data-stu-id="74761-121">Webhook Name.</span></span>

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

### <span data-ttu-id="74761-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="74761-122">-RegistryName</span></span>
<span data-ttu-id="74761-123">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="74761-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="74761-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74761-124">-ResourceGroupName</span></span>
<span data-ttu-id="74761-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="74761-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="74761-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74761-126">-ResourceId</span></span>
<span data-ttu-id="74761-127">容器登錄 Web方資源識別碼</span><span class="sxs-lookup"><span data-stu-id="74761-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="74761-128">-範圍</span><span class="sxs-lookup"><span data-stu-id="74761-128">-Scope</span></span>
<span data-ttu-id="74761-129">Web上的範圍。</span><span class="sxs-lookup"><span data-stu-id="74761-129">Webhook scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74761-130">-狀態</span><span class="sxs-lookup"><span data-stu-id="74761-130">-Status</span></span>
<span data-ttu-id="74761-131">Web上狀態</span><span class="sxs-lookup"><span data-stu-id="74761-131">Webhook status</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74761-132">-標記</span><span class="sxs-lookup"><span data-stu-id="74761-132">-Tag</span></span>
<span data-ttu-id="74761-133">以 'key \[ =value \] ' 格式分隔標記。</span><span class="sxs-lookup"><span data-stu-id="74761-133">Space separated tags in 'key\[=value\]' format.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74761-134">-Uri</span><span class="sxs-lookup"><span data-stu-id="74761-134">-Uri</span></span>
<span data-ttu-id="74761-135">Web 用服務 URI 張貼通知。</span><span class="sxs-lookup"><span data-stu-id="74761-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74761-136">-Web上</span><span class="sxs-lookup"><span data-stu-id="74761-136">-Webhook</span></span>
<span data-ttu-id="74761-137">Container Registry Web有物件。</span><span class="sxs-lookup"><span data-stu-id="74761-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="74761-138">-確認</span><span class="sxs-lookup"><span data-stu-id="74761-138">-Confirm</span></span>
<span data-ttu-id="74761-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="74761-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74761-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74761-140">-WhatIf</span></span>
<span data-ttu-id="74761-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74761-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74761-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74761-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74761-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74761-143">CommonParameters</span></span>
<span data-ttu-id="74761-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="74761-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74761-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74761-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74761-146">輸入</span><span class="sxs-lookup"><span data-stu-id="74761-146">INPUTS</span></span>

### <span data-ttu-id="74761-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="74761-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="74761-148">System.String</span><span class="sxs-lookup"><span data-stu-id="74761-148">System.String</span></span>

## <span data-ttu-id="74761-149">輸出</span><span class="sxs-lookup"><span data-stu-id="74761-149">OUTPUTS</span></span>

### <span data-ttu-id="74761-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="74761-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="74761-151">筆記</span><span class="sxs-lookup"><span data-stu-id="74761-151">NOTES</span></span>

## <span data-ttu-id="74761-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="74761-152">RELATED LINKS</span></span>

[<span data-ttu-id="74761-153">New-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="74761-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="74761-154">Get-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="74761-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="74761-155">Test-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="74761-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="74761-156">Remove-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="74761-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)