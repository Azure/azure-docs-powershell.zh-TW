---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 6cee5cc10fc9cbb1af014e2ad500b38111fc3564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443920"
---
# <span data-ttu-id="66b1f-101">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="66b1f-101">New-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="66b1f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="66b1f-103">建立容器註冊 webhook。</span><span class="sxs-lookup"><span data-stu-id="66b1f-103">Creates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66b1f-104">句法</span><span class="sxs-lookup"><span data-stu-id="66b1f-104">SYNTAX</span></span>

### <span data-ttu-id="66b1f-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="66b1f-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66b1f-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66b1f-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66b1f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66b1f-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66b1f-108">說明</span><span class="sxs-lookup"><span data-stu-id="66b1f-108">DESCRIPTION</span></span>
<span data-ttu-id="66b1f-109">New-AzureRmContainerRegistryWebhook Cmdlet 會建立容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="66b1f-109">The New-AzureRmContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="66b1f-110">示例</span><span class="sxs-lookup"><span data-stu-id="66b1f-110">EXAMPLES</span></span>

### <span data-ttu-id="66b1f-111">範例1：建立容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="66b1f-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="66b1f-112">建立容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="66b1f-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="66b1f-113">參數</span><span class="sxs-lookup"><span data-stu-id="66b1f-113">PARAMETERS</span></span>

### <span data-ttu-id="66b1f-114">-動作</span><span class="sxs-lookup"><span data-stu-id="66b1f-114">-Action</span></span>
<span data-ttu-id="66b1f-115">以空格分隔的動作清單，觸發 webhook 來張貼通知。</span><span class="sxs-lookup"><span data-stu-id="66b1f-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="66b1f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b1f-116">-DefaultProfile</span></span>
<span data-ttu-id="66b1f-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66b1f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66b1f-118">-頁首</span><span class="sxs-lookup"><span data-stu-id="66b1f-118">-Header</span></span>
<span data-ttu-id="66b1f-119">將新增至 webhook 通知的自訂標頭。</span><span class="sxs-lookup"><span data-stu-id="66b1f-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="66b1f-120">-位置</span><span class="sxs-lookup"><span data-stu-id="66b1f-120">-Location</span></span>
<span data-ttu-id="66b1f-121">Webhook 位置。</span><span class="sxs-lookup"><span data-stu-id="66b1f-121">Webhook Location.</span></span>
<span data-ttu-id="66b1f-122">預設為註冊表位置。</span><span class="sxs-lookup"><span data-stu-id="66b1f-122">Default to the location of the registry.</span></span>

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

### <span data-ttu-id="66b1f-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="66b1f-123">-Name</span></span>
<span data-ttu-id="66b1f-124">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="66b1f-124">Webhook Name.</span></span>

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

### <span data-ttu-id="66b1f-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="66b1f-125">-Registry</span></span>
<span data-ttu-id="66b1f-126">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="66b1f-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="66b1f-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="66b1f-127">-RegistryName</span></span>
<span data-ttu-id="66b1f-128">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="66b1f-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="66b1f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b1f-129">-ResourceGroupName</span></span>
<span data-ttu-id="66b1f-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="66b1f-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="66b1f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66b1f-131">-ResourceId</span></span>
<span data-ttu-id="66b1f-132">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="66b1f-132">The container registry resource id</span></span>

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

### <span data-ttu-id="66b1f-133">-範圍</span><span class="sxs-lookup"><span data-stu-id="66b1f-133">-Scope</span></span>
<span data-ttu-id="66b1f-134">Webhook 範圍。</span><span class="sxs-lookup"><span data-stu-id="66b1f-134">Webhook scope.</span></span>

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

### <span data-ttu-id="66b1f-135">-狀態</span><span class="sxs-lookup"><span data-stu-id="66b1f-135">-Status</span></span>
<span data-ttu-id="66b1f-136">Webhook 狀態，已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="66b1f-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="66b1f-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="66b1f-137">-Tag</span></span>
<span data-ttu-id="66b1f-138">Webhook 標籤。</span><span class="sxs-lookup"><span data-stu-id="66b1f-138">Webhook tags.</span></span>

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

### <span data-ttu-id="66b1f-139">-Uri</span><span class="sxs-lookup"><span data-stu-id="66b1f-139">-Uri</span></span>
<span data-ttu-id="66b1f-140">要公佈通知的 webhook 服務 URI。</span><span class="sxs-lookup"><span data-stu-id="66b1f-140">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="66b1f-141">-確認</span><span class="sxs-lookup"><span data-stu-id="66b1f-141">-Confirm</span></span>
<span data-ttu-id="66b1f-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="66b1f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66b1f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66b1f-143">-WhatIf</span></span>
<span data-ttu-id="66b1f-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66b1f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66b1f-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66b1f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66b1f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b1f-146">CommonParameters</span></span>
<span data-ttu-id="66b1f-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66b1f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b1f-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66b1f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b1f-149">輸入</span><span class="sxs-lookup"><span data-stu-id="66b1f-149">INPUTS</span></span>

### <span data-ttu-id="66b1f-150">System.object</span><span class="sxs-lookup"><span data-stu-id="66b1f-150">System.String</span></span>

## <span data-ttu-id="66b1f-151">輸出</span><span class="sxs-lookup"><span data-stu-id="66b1f-151">OUTPUTS</span></span>

### <span data-ttu-id="66b1f-152">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="66b1f-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="66b1f-153">筆記</span><span class="sxs-lookup"><span data-stu-id="66b1f-153">NOTES</span></span>

## <span data-ttu-id="66b1f-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="66b1f-154">RELATED LINKS</span></span>

[<span data-ttu-id="66b1f-155">AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="66b1f-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="66b1f-156">更新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="66b1f-156">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="66b1f-157">移除-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="66b1f-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="66b1f-158">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="66b1f-158">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
