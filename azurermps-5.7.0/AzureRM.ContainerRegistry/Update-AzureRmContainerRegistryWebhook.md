---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 7515046ed6e9fd6ba5c64b8123f8113b28b53f9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624192"
---
# <span data-ttu-id="d1489-101">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d1489-101">Update-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="d1489-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1489-102">SYNOPSIS</span></span>
<span data-ttu-id="d1489-103">更新容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="d1489-103">Updates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1489-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1489-104">SYNTAX</span></span>

### <span data-ttu-id="d1489-105">ResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d1489-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1489-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1489-106">NameResourceGroupParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1489-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1489-107">WebhookObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1489-108">說明</span><span class="sxs-lookup"><span data-stu-id="d1489-108">DESCRIPTION</span></span>
<span data-ttu-id="d1489-109">Update-AzureRmContainerRegistryWebhook Cmdlet 會更新容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="d1489-109">The Update-AzureRmContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="d1489-110">示例</span><span class="sxs-lookup"><span data-stu-id="d1489-110">EXAMPLES</span></span>

### <span data-ttu-id="d1489-111">範例1：更新現有的容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="d1489-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="d1489-112">更新現有的容器註冊表 webhook。</span><span class="sxs-lookup"><span data-stu-id="d1489-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="d1489-113">參數</span><span class="sxs-lookup"><span data-stu-id="d1489-113">PARAMETERS</span></span>

### <span data-ttu-id="d1489-114">-動作</span><span class="sxs-lookup"><span data-stu-id="d1489-114">-Action</span></span>
<span data-ttu-id="d1489-115">以空格分隔的動作清單，觸發 webhook 來張貼通知。</span><span class="sxs-lookup"><span data-stu-id="d1489-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1489-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1489-116">-DefaultProfile</span></span>
<span data-ttu-id="d1489-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1489-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1489-118">-頁首</span><span class="sxs-lookup"><span data-stu-id="d1489-118">-Header</span></span>
<span data-ttu-id="d1489-119">\[ \] 將新增至 webhook 通知的 [金鑰 = 值] 格式中的自訂標頭（以空格分隔）。</span><span class="sxs-lookup"><span data-stu-id="d1489-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="d1489-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d1489-120">-Name</span></span>
<span data-ttu-id="d1489-121">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="d1489-121">Webhook Name.</span></span>

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

### <span data-ttu-id="d1489-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d1489-122">-RegistryName</span></span>
<span data-ttu-id="d1489-123">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="d1489-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="d1489-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1489-124">-ResourceGroupName</span></span>
<span data-ttu-id="d1489-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d1489-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="d1489-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1489-126">-ResourceId</span></span>
<span data-ttu-id="d1489-127">容器登錄 Webhook 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d1489-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="d1489-128">-範圍</span><span class="sxs-lookup"><span data-stu-id="d1489-128">-Scope</span></span>
<span data-ttu-id="d1489-129">Webhook 範圍。</span><span class="sxs-lookup"><span data-stu-id="d1489-129">Webhook scope.</span></span>

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

### <span data-ttu-id="d1489-130">-狀態</span><span class="sxs-lookup"><span data-stu-id="d1489-130">-Status</span></span>
<span data-ttu-id="d1489-131">Webhook 狀態</span><span class="sxs-lookup"><span data-stu-id="d1489-131">Webhook status</span></span>

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

### <span data-ttu-id="d1489-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1489-132">-Tag</span></span>
<span data-ttu-id="d1489-133">[鍵 = 值] 格式中的空格分隔標記 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="d1489-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="d1489-134">-Uri</span><span class="sxs-lookup"><span data-stu-id="d1489-134">-Uri</span></span>
<span data-ttu-id="d1489-135">要公佈通知的 webhook 服務 URI。</span><span class="sxs-lookup"><span data-stu-id="d1489-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1489-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="d1489-136">-Webhook</span></span>
<span data-ttu-id="d1489-137">容器註冊表 Webhook 物件。</span><span class="sxs-lookup"><span data-stu-id="d1489-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="d1489-138">-確認</span><span class="sxs-lookup"><span data-stu-id="d1489-138">-Confirm</span></span>
<span data-ttu-id="d1489-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d1489-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1489-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1489-140">-WhatIf</span></span>
<span data-ttu-id="d1489-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1489-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1489-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1489-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1489-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1489-143">CommonParameters</span></span>
<span data-ttu-id="d1489-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1489-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1489-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d1489-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1489-146">輸入</span><span class="sxs-lookup"><span data-stu-id="d1489-146">INPUTS</span></span>

### <span data-ttu-id="d1489-147">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d1489-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="d1489-148">System.object</span><span class="sxs-lookup"><span data-stu-id="d1489-148">System.String</span></span>

## <span data-ttu-id="d1489-149">輸出</span><span class="sxs-lookup"><span data-stu-id="d1489-149">OUTPUTS</span></span>

### <span data-ttu-id="d1489-150">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d1489-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="d1489-151">筆記</span><span class="sxs-lookup"><span data-stu-id="d1489-151">NOTES</span></span>

## <span data-ttu-id="d1489-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1489-152">RELATED LINKS</span></span>

[<span data-ttu-id="d1489-153">新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d1489-153">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="d1489-154">AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d1489-154">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="d1489-155">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d1489-155">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="d1489-156">移除-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d1489-156">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
