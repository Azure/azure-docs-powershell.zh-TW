---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 8ea10f2acbe69e31bf80e35f0a8ea1577ffac6f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970527"
---
# <span data-ttu-id="f142b-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f142b-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="f142b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f142b-102">SYNOPSIS</span></span>
<span data-ttu-id="f142b-103">建立容器註冊 webhook。</span><span class="sxs-lookup"><span data-stu-id="f142b-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="f142b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f142b-104">SYNTAX</span></span>

### <span data-ttu-id="f142b-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f142b-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f142b-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f142b-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f142b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f142b-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f142b-108">說明</span><span class="sxs-lookup"><span data-stu-id="f142b-108">DESCRIPTION</span></span>
<span data-ttu-id="f142b-109">New-AzContainerRegistryWebhook Cmdlet 會建立容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="f142b-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="f142b-110">示例</span><span class="sxs-lookup"><span data-stu-id="f142b-110">EXAMPLES</span></span>

### <span data-ttu-id="f142b-111">範例1：建立容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="f142b-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="f142b-112">建立容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="f142b-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="f142b-113">參數</span><span class="sxs-lookup"><span data-stu-id="f142b-113">PARAMETERS</span></span>

### <span data-ttu-id="f142b-114">-動作</span><span class="sxs-lookup"><span data-stu-id="f142b-114">-Action</span></span>
<span data-ttu-id="f142b-115">以空格分隔的動作清單，觸發 webhook 來張貼通知。</span><span class="sxs-lookup"><span data-stu-id="f142b-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="f142b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f142b-116">-DefaultProfile</span></span>
<span data-ttu-id="f142b-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f142b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f142b-118">-頁首</span><span class="sxs-lookup"><span data-stu-id="f142b-118">-Header</span></span>
<span data-ttu-id="f142b-119">將新增至 webhook 通知的自訂標頭。</span><span class="sxs-lookup"><span data-stu-id="f142b-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="f142b-120">-位置</span><span class="sxs-lookup"><span data-stu-id="f142b-120">-Location</span></span>
<span data-ttu-id="f142b-121">Webhook 位置。</span><span class="sxs-lookup"><span data-stu-id="f142b-121">Webhook Location.</span></span>
<span data-ttu-id="f142b-122">預設為註冊表位置。</span><span class="sxs-lookup"><span data-stu-id="f142b-122">Default to the location of the registry.</span></span>

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

### <span data-ttu-id="f142b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="f142b-123">-Name</span></span>
<span data-ttu-id="f142b-124">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="f142b-124">Webhook Name.</span></span>

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

### <span data-ttu-id="f142b-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="f142b-125">-Registry</span></span>
<span data-ttu-id="f142b-126">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="f142b-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="f142b-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="f142b-127">-RegistryName</span></span>
<span data-ttu-id="f142b-128">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="f142b-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="f142b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f142b-129">-ResourceGroupName</span></span>
<span data-ttu-id="f142b-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f142b-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="f142b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f142b-131">-ResourceId</span></span>
<span data-ttu-id="f142b-132">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f142b-132">The container registry resource id</span></span>

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

### <span data-ttu-id="f142b-133">-範圍</span><span class="sxs-lookup"><span data-stu-id="f142b-133">-Scope</span></span>
<span data-ttu-id="f142b-134">Webhook 範圍。</span><span class="sxs-lookup"><span data-stu-id="f142b-134">Webhook scope.</span></span>

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

### <span data-ttu-id="f142b-135">-狀態</span><span class="sxs-lookup"><span data-stu-id="f142b-135">-Status</span></span>
<span data-ttu-id="f142b-136">Webhook 狀態，已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="f142b-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="f142b-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="f142b-137">-Tag</span></span>
<span data-ttu-id="f142b-138">Webhook 標籤。</span><span class="sxs-lookup"><span data-stu-id="f142b-138">Webhook tags.</span></span>

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

### <span data-ttu-id="f142b-139">-Uri</span><span class="sxs-lookup"><span data-stu-id="f142b-139">-Uri</span></span>
<span data-ttu-id="f142b-140">要公佈通知的 webhook 服務 URI。</span><span class="sxs-lookup"><span data-stu-id="f142b-140">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="f142b-141">-確認</span><span class="sxs-lookup"><span data-stu-id="f142b-141">-Confirm</span></span>
<span data-ttu-id="f142b-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f142b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f142b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f142b-143">-WhatIf</span></span>
<span data-ttu-id="f142b-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f142b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f142b-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f142b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f142b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f142b-146">CommonParameters</span></span>
<span data-ttu-id="f142b-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f142b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f142b-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f142b-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f142b-149">輸入</span><span class="sxs-lookup"><span data-stu-id="f142b-149">INPUTS</span></span>

### <span data-ttu-id="f142b-150">System.object</span><span class="sxs-lookup"><span data-stu-id="f142b-150">System.String</span></span>

## <span data-ttu-id="f142b-151">輸出</span><span class="sxs-lookup"><span data-stu-id="f142b-151">OUTPUTS</span></span>

### <span data-ttu-id="f142b-152">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f142b-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="f142b-153">筆記</span><span class="sxs-lookup"><span data-stu-id="f142b-153">NOTES</span></span>

## <span data-ttu-id="f142b-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="f142b-154">RELATED LINKS</span></span>

[<span data-ttu-id="f142b-155">AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f142b-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f142b-156">更新-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f142b-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f142b-157">移除-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f142b-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f142b-158">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f142b-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)