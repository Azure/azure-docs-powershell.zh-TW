---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a23cfb79c341fb4fcee5b5688b0780ba178e978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449917"
---
# <span data-ttu-id="3ed23-101">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3ed23-101">New-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="3ed23-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ed23-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed23-103">建立容器註冊 webhook。</span><span class="sxs-lookup"><span data-stu-id="3ed23-103">Creates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ed23-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ed23-104">SYNTAX</span></span>

### <span data-ttu-id="3ed23-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3ed23-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ed23-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ed23-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ed23-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ed23-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ed23-108">說明</span><span class="sxs-lookup"><span data-stu-id="3ed23-108">DESCRIPTION</span></span>
<span data-ttu-id="3ed23-109">New-AzureRmContainerRegistryWebhook Cmdlet 會建立容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="3ed23-109">The New-AzureRmContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="3ed23-110">示例</span><span class="sxs-lookup"><span data-stu-id="3ed23-110">EXAMPLES</span></span>

### <span data-ttu-id="3ed23-111">範例1：建立容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="3ed23-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="3ed23-112">建立容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="3ed23-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="3ed23-113">參數</span><span class="sxs-lookup"><span data-stu-id="3ed23-113">PARAMETERS</span></span>

### <span data-ttu-id="3ed23-114">-動作</span><span class="sxs-lookup"><span data-stu-id="3ed23-114">-Action</span></span>
<span data-ttu-id="3ed23-115">以空格分隔的動作清單，觸發 webhook 來張貼通知。</span><span class="sxs-lookup"><span data-stu-id="3ed23-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed23-116">-確認</span><span class="sxs-lookup"><span data-stu-id="3ed23-116">-Confirm</span></span>
<span data-ttu-id="3ed23-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3ed23-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed23-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed23-118">-DefaultProfile</span></span>
<span data-ttu-id="3ed23-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ed23-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ed23-120">-頁首</span><span class="sxs-lookup"><span data-stu-id="3ed23-120">-Header</span></span>
<span data-ttu-id="3ed23-121">將新增至 webhook 通知的自訂標頭。</span><span class="sxs-lookup"><span data-stu-id="3ed23-121">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed23-122">-位置</span><span class="sxs-lookup"><span data-stu-id="3ed23-122">-Location</span></span>
<span data-ttu-id="3ed23-123">Webhook 位置。</span><span class="sxs-lookup"><span data-stu-id="3ed23-123">Webhook Location.</span></span>
<span data-ttu-id="3ed23-124">預設為註冊表位置。</span><span class="sxs-lookup"><span data-stu-id="3ed23-124">Default to the location of the registry.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed23-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="3ed23-125">-Name</span></span>
<span data-ttu-id="3ed23-126">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="3ed23-126">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed23-127">-Registry</span><span class="sxs-lookup"><span data-stu-id="3ed23-127">-Registry</span></span>
<span data-ttu-id="3ed23-128">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="3ed23-128">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed23-129">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="3ed23-129">-RegistryName</span></span>
<span data-ttu-id="3ed23-130">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="3ed23-130">Container Registry Name.</span></span>

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

### <span data-ttu-id="3ed23-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed23-131">-ResourceGroupName</span></span>
<span data-ttu-id="3ed23-132">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3ed23-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="3ed23-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ed23-133">-ResourceId</span></span>
<span data-ttu-id="3ed23-134">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3ed23-134">The container registry resource id</span></span>

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

### <span data-ttu-id="3ed23-135">-範圍</span><span class="sxs-lookup"><span data-stu-id="3ed23-135">-Scope</span></span>
<span data-ttu-id="3ed23-136">Webhook 範圍。</span><span class="sxs-lookup"><span data-stu-id="3ed23-136">Webhook scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed23-137">-狀態</span><span class="sxs-lookup"><span data-stu-id="3ed23-137">-Status</span></span>
<span data-ttu-id="3ed23-138">Webhook 狀態，已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="3ed23-138">Webhook status, default value is enabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed23-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="3ed23-139">-Tag</span></span>
<span data-ttu-id="3ed23-140">Webhook 標籤。</span><span class="sxs-lookup"><span data-stu-id="3ed23-140">Webhook tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed23-141">-Uri</span><span class="sxs-lookup"><span data-stu-id="3ed23-141">-Uri</span></span>
<span data-ttu-id="3ed23-142">要公佈通知的 webhook 服務 URI。</span><span class="sxs-lookup"><span data-stu-id="3ed23-142">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed23-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ed23-143">-WhatIf</span></span>
<span data-ttu-id="3ed23-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ed23-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ed23-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ed23-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed23-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed23-146">CommonParameters</span></span>
<span data-ttu-id="3ed23-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ed23-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed23-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3ed23-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed23-149">輸入</span><span class="sxs-lookup"><span data-stu-id="3ed23-149">INPUTS</span></span>

### <span data-ttu-id="3ed23-150">System.object</span><span class="sxs-lookup"><span data-stu-id="3ed23-150">System.String</span></span>

## <span data-ttu-id="3ed23-151">輸出</span><span class="sxs-lookup"><span data-stu-id="3ed23-151">OUTPUTS</span></span>

### <span data-ttu-id="3ed23-152">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3ed23-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="3ed23-153">筆記</span><span class="sxs-lookup"><span data-stu-id="3ed23-153">NOTES</span></span>

## <span data-ttu-id="3ed23-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ed23-154">RELATED LINKS</span></span>

[<span data-ttu-id="3ed23-155">AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3ed23-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="3ed23-156">更新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3ed23-156">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="3ed23-157">移除-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3ed23-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="3ed23-158">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3ed23-158">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
