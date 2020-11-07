---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: b7f10fd96d8f746db1ff37b1461cdd8394bdf75d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625600"
---
# <span data-ttu-id="931e5-101">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="931e5-101">Update-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="931e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="931e5-102">SYNOPSIS</span></span>
<span data-ttu-id="931e5-103">更新容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="931e5-103">Updates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="931e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="931e5-104">SYNTAX</span></span>

### <span data-ttu-id="931e5-105">ResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="931e5-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="931e5-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="931e5-106">NameResourceGroupParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="931e5-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="931e5-107">WebhookObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="931e5-108">說明</span><span class="sxs-lookup"><span data-stu-id="931e5-108">DESCRIPTION</span></span>
<span data-ttu-id="931e5-109">Update-AzureRmContainerRegistryWebhook Cmdlet 會更新容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="931e5-109">The Update-AzureRmContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="931e5-110">示例</span><span class="sxs-lookup"><span data-stu-id="931e5-110">EXAMPLES</span></span>

### <span data-ttu-id="931e5-111">範例1：更新現有的容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="931e5-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="931e5-112">更新現有的容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="931e5-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="931e5-113">參數</span><span class="sxs-lookup"><span data-stu-id="931e5-113">PARAMETERS</span></span>

### <span data-ttu-id="931e5-114">-動作</span><span class="sxs-lookup"><span data-stu-id="931e5-114">-Action</span></span>
<span data-ttu-id="931e5-115">以空格分隔的動作清單，觸發 webhook 來張貼通知。</span><span class="sxs-lookup"><span data-stu-id="931e5-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="931e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="931e5-116">-DefaultProfile</span></span>
<span data-ttu-id="931e5-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="931e5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="931e5-118">-頁首</span><span class="sxs-lookup"><span data-stu-id="931e5-118">-Header</span></span>
<span data-ttu-id="931e5-119">\[ \] 將新增至 webhook 通知的 [金鑰 = 值] 格式中的自訂標頭（以空格分隔）。</span><span class="sxs-lookup"><span data-stu-id="931e5-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="931e5-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="931e5-120">-Name</span></span>
<span data-ttu-id="931e5-121">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="931e5-121">Webhook Name.</span></span>

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

### <span data-ttu-id="931e5-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="931e5-122">-RegistryName</span></span>
<span data-ttu-id="931e5-123">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="931e5-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="931e5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="931e5-124">-ResourceGroupName</span></span>
<span data-ttu-id="931e5-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="931e5-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="931e5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="931e5-126">-ResourceId</span></span>
<span data-ttu-id="931e5-127">容器登錄 Webhook 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="931e5-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="931e5-128">-範圍</span><span class="sxs-lookup"><span data-stu-id="931e5-128">-Scope</span></span>
<span data-ttu-id="931e5-129">Webhook 範圍。</span><span class="sxs-lookup"><span data-stu-id="931e5-129">Webhook scope.</span></span>

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

### <span data-ttu-id="931e5-130">-狀態</span><span class="sxs-lookup"><span data-stu-id="931e5-130">-Status</span></span>
<span data-ttu-id="931e5-131">Webhook 狀態</span><span class="sxs-lookup"><span data-stu-id="931e5-131">Webhook status</span></span>

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

### <span data-ttu-id="931e5-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="931e5-132">-Tag</span></span>
<span data-ttu-id="931e5-133">[鍵 = 值] 格式中的空格分隔標記 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="931e5-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="931e5-134">-Uri</span><span class="sxs-lookup"><span data-stu-id="931e5-134">-Uri</span></span>
<span data-ttu-id="931e5-135">要公佈通知的 webhook 服務 URI。</span><span class="sxs-lookup"><span data-stu-id="931e5-135">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="931e5-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="931e5-136">-Webhook</span></span>
<span data-ttu-id="931e5-137">容器註冊表 Webhook 物件。</span><span class="sxs-lookup"><span data-stu-id="931e5-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="931e5-138">-確認</span><span class="sxs-lookup"><span data-stu-id="931e5-138">-Confirm</span></span>
<span data-ttu-id="931e5-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="931e5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="931e5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="931e5-140">-WhatIf</span></span>
<span data-ttu-id="931e5-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="931e5-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="931e5-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="931e5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="931e5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="931e5-143">CommonParameters</span></span>
<span data-ttu-id="931e5-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="931e5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="931e5-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="931e5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="931e5-146">輸入</span><span class="sxs-lookup"><span data-stu-id="931e5-146">INPUTS</span></span>

### <span data-ttu-id="931e5-147">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="931e5-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="931e5-148">參數： Webhook (ByValue) </span><span class="sxs-lookup"><span data-stu-id="931e5-148">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="931e5-149">System.object</span><span class="sxs-lookup"><span data-stu-id="931e5-149">System.String</span></span>

## <span data-ttu-id="931e5-150">輸出</span><span class="sxs-lookup"><span data-stu-id="931e5-150">OUTPUTS</span></span>

### <span data-ttu-id="931e5-151">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="931e5-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="931e5-152">筆記</span><span class="sxs-lookup"><span data-stu-id="931e5-152">NOTES</span></span>

## <span data-ttu-id="931e5-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="931e5-153">RELATED LINKS</span></span>

[<span data-ttu-id="931e5-154">新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="931e5-154">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="931e5-155">AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="931e5-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="931e5-156">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="931e5-156">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="931e5-157">移除-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="931e5-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
