---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 10acca5a89c4ea84d475e5eea2e89e18942116f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907786"
---
# <span data-ttu-id="de78e-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="de78e-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="de78e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="de78e-102">SYNOPSIS</span></span>
<span data-ttu-id="de78e-103">建立容器註冊表網頁建立。</span><span class="sxs-lookup"><span data-stu-id="de78e-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="de78e-104">語法</span><span class="sxs-lookup"><span data-stu-id="de78e-104">SYNTAX</span></span>

### <span data-ttu-id="de78e-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="de78e-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de78e-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de78e-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de78e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de78e-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de78e-108">描述</span><span class="sxs-lookup"><span data-stu-id="de78e-108">DESCRIPTION</span></span>
<span data-ttu-id="de78e-109">此New-AzContainerRegistryWebhook Cmdlet 會建立容器註冊表網頁建立。</span><span class="sxs-lookup"><span data-stu-id="de78e-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="de78e-110">例子</span><span class="sxs-lookup"><span data-stu-id="de78e-110">EXAMPLES</span></span>

### <span data-ttu-id="de78e-111">範例 1：建立容器註冊網站。</span><span class="sxs-lookup"><span data-stu-id="de78e-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="de78e-112">建立容器註冊表網頁。</span><span class="sxs-lookup"><span data-stu-id="de78e-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="de78e-113">參數</span><span class="sxs-lookup"><span data-stu-id="de78e-113">PARAMETERS</span></span>

### <span data-ttu-id="de78e-114">-動作</span><span class="sxs-lookup"><span data-stu-id="de78e-114">-Action</span></span>
<span data-ttu-id="de78e-115">會觸發網頁設計來張貼通知的動作空格分隔清單。</span><span class="sxs-lookup"><span data-stu-id="de78e-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de78e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de78e-116">-DefaultProfile</span></span>
<span data-ttu-id="de78e-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="de78e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de78e-118">-頁眉</span><span class="sxs-lookup"><span data-stu-id="de78e-118">-Header</span></span>
<span data-ttu-id="de78e-119">要新加入網頁化通知的自訂標題。</span><span class="sxs-lookup"><span data-stu-id="de78e-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="de78e-120">-位置</span><span class="sxs-lookup"><span data-stu-id="de78e-120">-Location</span></span>
<span data-ttu-id="de78e-121">Web下一個位置。</span><span class="sxs-lookup"><span data-stu-id="de78e-121">Webhook Location.</span></span>
<span data-ttu-id="de78e-122">預設為註冊表的位置。</span><span class="sxs-lookup"><span data-stu-id="de78e-122">Default to the location of the registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de78e-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="de78e-123">-Name</span></span>
<span data-ttu-id="de78e-124">Web下一個名稱。</span><span class="sxs-lookup"><span data-stu-id="de78e-124">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de78e-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="de78e-125">-Registry</span></span>
<span data-ttu-id="de78e-126">Container Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="de78e-126">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de78e-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="de78e-127">-RegistryName</span></span>
<span data-ttu-id="de78e-128">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="de78e-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="de78e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de78e-129">-ResourceGroupName</span></span>
<span data-ttu-id="de78e-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="de78e-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="de78e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de78e-131">-ResourceId</span></span>
<span data-ttu-id="de78e-132">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="de78e-132">The container registry resource id</span></span>

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

### <span data-ttu-id="de78e-133">-範圍</span><span class="sxs-lookup"><span data-stu-id="de78e-133">-Scope</span></span>
<span data-ttu-id="de78e-134">Web上的範圍。</span><span class="sxs-lookup"><span data-stu-id="de78e-134">Webhook scope.</span></span>

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

### <span data-ttu-id="de78e-135">-狀態</span><span class="sxs-lookup"><span data-stu-id="de78e-135">-Status</span></span>
<span data-ttu-id="de78e-136">Web上狀態，已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="de78e-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="de78e-137">-標記</span><span class="sxs-lookup"><span data-stu-id="de78e-137">-Tag</span></span>
<span data-ttu-id="de78e-138">Web下一個標記。</span><span class="sxs-lookup"><span data-stu-id="de78e-138">Webhook tags.</span></span>

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

### <span data-ttu-id="de78e-139">-Uri</span><span class="sxs-lookup"><span data-stu-id="de78e-139">-Uri</span></span>
<span data-ttu-id="de78e-140">Web 用服務 URI 張貼通知。</span><span class="sxs-lookup"><span data-stu-id="de78e-140">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de78e-141">-確認</span><span class="sxs-lookup"><span data-stu-id="de78e-141">-Confirm</span></span>
<span data-ttu-id="de78e-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="de78e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de78e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de78e-143">-WhatIf</span></span>
<span data-ttu-id="de78e-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de78e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de78e-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de78e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de78e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de78e-146">CommonParameters</span></span>
<span data-ttu-id="de78e-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="de78e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de78e-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de78e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de78e-149">輸入</span><span class="sxs-lookup"><span data-stu-id="de78e-149">INPUTS</span></span>

### <span data-ttu-id="de78e-150">System.String</span><span class="sxs-lookup"><span data-stu-id="de78e-150">System.String</span></span>

## <span data-ttu-id="de78e-151">輸出</span><span class="sxs-lookup"><span data-stu-id="de78e-151">OUTPUTS</span></span>

### <span data-ttu-id="de78e-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="de78e-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="de78e-153">筆記</span><span class="sxs-lookup"><span data-stu-id="de78e-153">NOTES</span></span>

## <span data-ttu-id="de78e-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="de78e-154">RELATED LINKS</span></span>

[<span data-ttu-id="de78e-155">Get-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="de78e-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="de78e-156">Update-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="de78e-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="de78e-157">Remove-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="de78e-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="de78e-158">Test-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="de78e-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)