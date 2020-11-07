---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: eee4d9db5cbc64f8ae7e17f18026f5bd2aeca310
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626422"
---
# <span data-ttu-id="364b6-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="364b6-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="364b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="364b6-102">SYNOPSIS</span></span>
<span data-ttu-id="364b6-103">從通知中心命名空間移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="364b6-103">Removes an authorization rule from a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="364b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="364b6-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="364b6-105">說明</span><span class="sxs-lookup"><span data-stu-id="364b6-105">DESCRIPTION</span></span>
<span data-ttu-id="364b6-106">**AzureRmNotificationHubsNamespaceAuthorizationRules** Cmdlet 會從通知中心命名空間中移除 (SAS) 授權規則的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="364b6-106">The **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>

<span data-ttu-id="364b6-107">授權規則可管理命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="364b6-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="364b6-108">這是透過根據不同的許可權等級建立連結（例如 Uri）來完成。</span><span class="sxs-lookup"><span data-stu-id="364b6-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="364b6-109">許可權等級可以是下列各項：</span><span class="sxs-lookup"><span data-stu-id="364b6-109">Permission levels can be of the following:</span></span> 

- <span data-ttu-id="364b6-110">聆聽</span><span class="sxs-lookup"><span data-stu-id="364b6-110">Listen</span></span>
- <span data-ttu-id="364b6-111">發送</span><span class="sxs-lookup"><span data-stu-id="364b6-111">Send</span></span>
- <span data-ttu-id="364b6-112">管理</span><span class="sxs-lookup"><span data-stu-id="364b6-112">Manage</span></span>

<span data-ttu-id="364b6-113">用戶端會根據適當的許可權等級，導向到其中一個 Uri。</span><span class="sxs-lookup"><span data-stu-id="364b6-113">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="364b6-114">例如，擁有 [偵聽] 許可權的用戶端會定向至該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="364b6-114">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>

<span data-ttu-id="364b6-115">移除授權規則也會移除對應的使用者許可權。</span><span class="sxs-lookup"><span data-stu-id="364b6-115">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="364b6-116">示例</span><span class="sxs-lookup"><span data-stu-id="364b6-116">EXAMPLES</span></span>

### <span data-ttu-id="364b6-117">範例1：從命名空間移除授權規則</span><span class="sxs-lookup"><span data-stu-id="364b6-117">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="364b6-118">這個命令會將名為 ListenRule 的授權規則從名為 ContosoNamespace 的命名空間中移除。</span><span class="sxs-lookup"><span data-stu-id="364b6-118">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="364b6-119">當您執行此命令時，您必須指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="364b6-119">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="364b6-120">參數</span><span class="sxs-lookup"><span data-stu-id="364b6-120">PARAMETERS</span></span>

### <span data-ttu-id="364b6-121">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="364b6-121">-AuthorizationRule</span></span>
<span data-ttu-id="364b6-122">指定要移除的 SAS 驗證規則名稱。</span><span class="sxs-lookup"><span data-stu-id="364b6-122">Specifies the name of the SAS authentication rule to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="364b6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="364b6-123">-DefaultProfile</span></span>
<span data-ttu-id="364b6-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="364b6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="364b6-125">-Force</span><span class="sxs-lookup"><span data-stu-id="364b6-125">-Force</span></span>
<span data-ttu-id="364b6-126">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="364b6-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="364b6-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="364b6-127">-Namespace</span></span>
<span data-ttu-id="364b6-128">指定授權規則指派的命名空間。</span><span class="sxs-lookup"><span data-stu-id="364b6-128">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="364b6-129">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="364b6-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="364b6-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="364b6-130">-ResourceGroup</span></span>
<span data-ttu-id="364b6-131">指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="364b6-131">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="364b6-132">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="364b6-132">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="364b6-133">-確認</span><span class="sxs-lookup"><span data-stu-id="364b6-133">-Confirm</span></span>
<span data-ttu-id="364b6-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="364b6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="364b6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="364b6-135">-WhatIf</span></span>
<span data-ttu-id="364b6-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="364b6-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="364b6-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="364b6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="364b6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="364b6-138">CommonParameters</span></span>
<span data-ttu-id="364b6-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="364b6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="364b6-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="364b6-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="364b6-141">輸入</span><span class="sxs-lookup"><span data-stu-id="364b6-141">INPUTS</span></span>

### <span data-ttu-id="364b6-142">所有</span><span class="sxs-lookup"><span data-stu-id="364b6-142">None</span></span>
<span data-ttu-id="364b6-143">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="364b6-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="364b6-144">輸出</span><span class="sxs-lookup"><span data-stu-id="364b6-144">OUTPUTS</span></span>

### <span data-ttu-id="364b6-145">System.object</span><span class="sxs-lookup"><span data-stu-id="364b6-145">System.Boolean</span></span>

## <span data-ttu-id="364b6-146">筆記</span><span class="sxs-lookup"><span data-stu-id="364b6-146">NOTES</span></span>

## <span data-ttu-id="364b6-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="364b6-147">RELATED LINKS</span></span>

[<span data-ttu-id="364b6-148">AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="364b6-148">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="364b6-149">新-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="364b6-149">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="364b6-150">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="364b6-150">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


