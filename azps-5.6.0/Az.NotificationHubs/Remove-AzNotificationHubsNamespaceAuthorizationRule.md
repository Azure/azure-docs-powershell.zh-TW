---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 0b16a7feb2d0cba7355b6064c1a0e1e6fb327066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901705"
---
# <span data-ttu-id="7028a-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7028a-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="7028a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7028a-102">SYNOPSIS</span></span>
<span data-ttu-id="7028a-103">從通知中樞命名空間移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="7028a-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="7028a-104">語法</span><span class="sxs-lookup"><span data-stu-id="7028a-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7028a-105">描述</span><span class="sxs-lookup"><span data-stu-id="7028a-105">DESCRIPTION</span></span>
<span data-ttu-id="7028a-106">**Remove-AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 會從通知中樞命名空間移除共用存取簽章 (SAS) 授權規則。</span><span class="sxs-lookup"><span data-stu-id="7028a-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="7028a-107">授權規則可管理命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="7028a-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="7028a-108">這是透過根據不同許可權等級建立連結以做為 URI 的方式完成。</span><span class="sxs-lookup"><span data-stu-id="7028a-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="7028a-109">許可權等級可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="7028a-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="7028a-110">聽</span><span class="sxs-lookup"><span data-stu-id="7028a-110">Listen</span></span>
- <span data-ttu-id="7028a-111">發送</span><span class="sxs-lookup"><span data-stu-id="7028a-111">Send</span></span>
- <span data-ttu-id="7028a-112">管理用戶端會依據適當的許可權等級，導向至其中一個 URI。</span><span class="sxs-lookup"><span data-stu-id="7028a-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="7028a-113">例如，提供聆聽許可權的用戶端會導向至該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="7028a-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="7028a-114">移除授權規則也會移除對應的使用者許可權。</span><span class="sxs-lookup"><span data-stu-id="7028a-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="7028a-115">例子</span><span class="sxs-lookup"><span data-stu-id="7028a-115">EXAMPLES</span></span>

### <span data-ttu-id="7028a-116">範例 1：從命名空間移除授權規則</span><span class="sxs-lookup"><span data-stu-id="7028a-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="7028a-117">此命令會從名稱為 ContosoNamespace 的命名空間移除名為 ListenRule 的授權規則。</span><span class="sxs-lookup"><span data-stu-id="7028a-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="7028a-118">當您執行此命令時，您必須指定命名空間指派給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="7028a-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="7028a-119">參數</span><span class="sxs-lookup"><span data-stu-id="7028a-119">PARAMETERS</span></span>

### <span data-ttu-id="7028a-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7028a-120">-AuthorizationRule</span></span>
<span data-ttu-id="7028a-121">指定要移除的 SAS 驗證規則名稱。</span><span class="sxs-lookup"><span data-stu-id="7028a-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="7028a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7028a-122">-DefaultProfile</span></span>
<span data-ttu-id="7028a-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7028a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7028a-124">-強制</span><span class="sxs-lookup"><span data-stu-id="7028a-124">-Force</span></span>
<span data-ttu-id="7028a-125">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="7028a-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7028a-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="7028a-126">-Namespace</span></span>
<span data-ttu-id="7028a-127">指定指派授權規則的命名空間。</span><span class="sxs-lookup"><span data-stu-id="7028a-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="7028a-128">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="7028a-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="7028a-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7028a-129">-ResourceGroup</span></span>
<span data-ttu-id="7028a-130">指定指派命名空間的資源群組。</span><span class="sxs-lookup"><span data-stu-id="7028a-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="7028a-131">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="7028a-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="7028a-132">-確認</span><span class="sxs-lookup"><span data-stu-id="7028a-132">-Confirm</span></span>
<span data-ttu-id="7028a-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7028a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7028a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7028a-134">-WhatIf</span></span>
<span data-ttu-id="7028a-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7028a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7028a-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7028a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7028a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7028a-137">CommonParameters</span></span>
<span data-ttu-id="7028a-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7028a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7028a-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7028a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7028a-140">輸入</span><span class="sxs-lookup"><span data-stu-id="7028a-140">INPUTS</span></span>

### <span data-ttu-id="7028a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7028a-141">System.String</span></span>

## <span data-ttu-id="7028a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="7028a-142">OUTPUTS</span></span>

### <span data-ttu-id="7028a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7028a-143">System.Boolean</span></span>

## <span data-ttu-id="7028a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="7028a-144">NOTES</span></span>

## <span data-ttu-id="7028a-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="7028a-145">RELATED LINKS</span></span>

[<span data-ttu-id="7028a-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7028a-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="7028a-147">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7028a-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="7028a-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7028a-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)


