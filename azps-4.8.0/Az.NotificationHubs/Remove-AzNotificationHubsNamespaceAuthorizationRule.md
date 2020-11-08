---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a25535e3aef21894091197d816c61f2aa5131df9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135488"
---
# <span data-ttu-id="ac65c-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ac65c-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="ac65c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac65c-102">SYNOPSIS</span></span>
<span data-ttu-id="ac65c-103">從通知中心命名空間移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="ac65c-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="ac65c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac65c-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac65c-105">說明</span><span class="sxs-lookup"><span data-stu-id="ac65c-105">DESCRIPTION</span></span>
<span data-ttu-id="ac65c-106">**AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 會從通知中心命名空間中移除 (SAS) 授權規則的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="ac65c-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="ac65c-107">授權規則可管理命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="ac65c-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="ac65c-108">這是透過根據不同的許可權等級建立連結（例如 Uri）來完成。</span><span class="sxs-lookup"><span data-stu-id="ac65c-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="ac65c-109">許可權等級可以是下列各項：</span><span class="sxs-lookup"><span data-stu-id="ac65c-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="ac65c-110">聆聽</span><span class="sxs-lookup"><span data-stu-id="ac65c-110">Listen</span></span>
- <span data-ttu-id="ac65c-111">發送</span><span class="sxs-lookup"><span data-stu-id="ac65c-111">Send</span></span>
- <span data-ttu-id="ac65c-112">系統會根據適當的許可權等級，將管理用戶端導向到其中一個 Uri。</span><span class="sxs-lookup"><span data-stu-id="ac65c-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="ac65c-113">例如，擁有 [偵聽] 許可權的用戶端會定向至該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="ac65c-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="ac65c-114">移除授權規則也會移除對應的使用者許可權。</span><span class="sxs-lookup"><span data-stu-id="ac65c-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="ac65c-115">示例</span><span class="sxs-lookup"><span data-stu-id="ac65c-115">EXAMPLES</span></span>

### <span data-ttu-id="ac65c-116">範例1：從命名空間移除授權規則</span><span class="sxs-lookup"><span data-stu-id="ac65c-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="ac65c-117">這個命令會將名為 ListenRule 的授權規則從名為 ContosoNamespace 的命名空間中移除。</span><span class="sxs-lookup"><span data-stu-id="ac65c-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="ac65c-118">當您執行此命令時，您必須指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="ac65c-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="ac65c-119">參數</span><span class="sxs-lookup"><span data-stu-id="ac65c-119">PARAMETERS</span></span>

### <span data-ttu-id="ac65c-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ac65c-120">-AuthorizationRule</span></span>
<span data-ttu-id="ac65c-121">指定要移除的 SAS 驗證規則名稱。</span><span class="sxs-lookup"><span data-stu-id="ac65c-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac65c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac65c-122">-DefaultProfile</span></span>
<span data-ttu-id="ac65c-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ac65c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac65c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ac65c-124">-Force</span></span>
<span data-ttu-id="ac65c-125">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="ac65c-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ac65c-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="ac65c-126">-Namespace</span></span>
<span data-ttu-id="ac65c-127">指定授權規則指派的命名空間。</span><span class="sxs-lookup"><span data-stu-id="ac65c-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="ac65c-128">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="ac65c-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac65c-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ac65c-129">-ResourceGroup</span></span>
<span data-ttu-id="ac65c-130">指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="ac65c-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="ac65c-131">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="ac65c-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac65c-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ac65c-132">-Confirm</span></span>
<span data-ttu-id="ac65c-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ac65c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac65c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac65c-134">-WhatIf</span></span>
<span data-ttu-id="ac65c-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac65c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac65c-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac65c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac65c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac65c-137">CommonParameters</span></span>
<span data-ttu-id="ac65c-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac65c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac65c-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac65c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac65c-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ac65c-140">INPUTS</span></span>

### <span data-ttu-id="ac65c-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ac65c-141">System.String</span></span>

## <span data-ttu-id="ac65c-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ac65c-142">OUTPUTS</span></span>

### <span data-ttu-id="ac65c-143">System.object</span><span class="sxs-lookup"><span data-stu-id="ac65c-143">System.Boolean</span></span>

## <span data-ttu-id="ac65c-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ac65c-144">NOTES</span></span>

## <span data-ttu-id="ac65c-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac65c-145">RELATED LINKS</span></span>

[<span data-ttu-id="ac65c-146">AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ac65c-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="ac65c-147">新-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ac65c-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="ac65c-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ac65c-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)


