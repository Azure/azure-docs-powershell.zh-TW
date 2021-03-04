---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a1c9743d02f10102d9343709599dbed694d37a2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901746"
---
# <span data-ttu-id="ae513-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ae513-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="ae513-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ae513-102">SYNOPSIS</span></span>
<span data-ttu-id="ae513-103">與通知中樞命名空間相關聯的授權規則相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ae513-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="ae513-104">語法</span><span class="sxs-lookup"><span data-stu-id="ae513-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae513-105">描述</span><span class="sxs-lookup"><span data-stu-id="ae513-105">DESCRIPTION</span></span>
<span data-ttu-id="ae513-106">**Get-AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 會返回與通知中樞命名空間相關聯的共用存取簽章 (SAS) 授權規則相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ae513-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="ae513-107">您可以返回與命名空間相關聯的所有規則相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ae513-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="ae513-108">或者，您也可以包含 *AuthorizationRule* 參數，以返回特定規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="ae513-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="ae513-109">授權規則可管理命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="ae513-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="ae513-110">這是透過根據不同許可權等級建立連結以做為 URI 的方式完成。</span><span class="sxs-lookup"><span data-stu-id="ae513-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="ae513-111">平台層級可以是下列其中一個：</span><span class="sxs-lookup"><span data-stu-id="ae513-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="ae513-112">聽</span><span class="sxs-lookup"><span data-stu-id="ae513-112">Listen</span></span>
- <span data-ttu-id="ae513-113">發送</span><span class="sxs-lookup"><span data-stu-id="ae513-113">Send</span></span>
- <span data-ttu-id="ae513-114">管理用戶端會依據適當的許可權等級，導向至其中一個 URI。</span><span class="sxs-lookup"><span data-stu-id="ae513-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="ae513-115">例如，提供聆聽許可權的用戶端會導向至該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="ae513-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="ae513-116">此 Cmdlet 只會獲得與命名空間相關聯的授權規則。</span><span class="sxs-lookup"><span data-stu-id="ae513-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="ae513-117">若要取得命名空間本身的資訊，請使用 Get-AzNotificationHubsNamespace。</span><span class="sxs-lookup"><span data-stu-id="ae513-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="ae513-118">例子</span><span class="sxs-lookup"><span data-stu-id="ae513-118">EXAMPLES</span></span>

### <span data-ttu-id="ae513-119">範例 1：取得指派給命名空間之所有授權規則的資訊</span><span class="sxs-lookup"><span data-stu-id="ae513-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="ae513-120">此命令會獲得指派給命名空間 ContosoNamespace 和 ContosoNotificationsGroup 資源群組之所有授權規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="ae513-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="ae513-121">範例 2：取得授權規則相關資訊</span><span class="sxs-lookup"><span data-stu-id="ae513-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="ae513-122">此命令會獲得名為 ListenRule 的單一命名空間授權規則相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ae513-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="ae513-123">當您取得特定授權規則的資訊時，必須包含命名空間和資源群組。</span><span class="sxs-lookup"><span data-stu-id="ae513-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="ae513-124">參數</span><span class="sxs-lookup"><span data-stu-id="ae513-124">PARAMETERS</span></span>

### <span data-ttu-id="ae513-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ae513-125">-AuthorizationRule</span></span>
<span data-ttu-id="ae513-126">指定 SAS 驗證規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae513-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="ae513-127">這些規則會決定使用者對於命名空間的存取類型。</span><span class="sxs-lookup"><span data-stu-id="ae513-127">These rules determine the type of access that users have to the namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae513-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae513-128">-DefaultProfile</span></span>
<span data-ttu-id="ae513-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ae513-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae513-130">-命名空間</span><span class="sxs-lookup"><span data-stu-id="ae513-130">-Namespace</span></span>
<span data-ttu-id="ae513-131">指定指派授權規則的命名空間。</span><span class="sxs-lookup"><span data-stu-id="ae513-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="ae513-132">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="ae513-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="ae513-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ae513-133">-ResourceGroup</span></span>
<span data-ttu-id="ae513-134">指定指派授權規則給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ae513-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="ae513-135">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="ae513-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="ae513-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae513-136">CommonParameters</span></span>
<span data-ttu-id="ae513-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ae513-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae513-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ae513-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae513-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ae513-139">INPUTS</span></span>

### <span data-ttu-id="ae513-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ae513-140">System.String</span></span>

## <span data-ttu-id="ae513-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ae513-141">OUTPUTS</span></span>

### <span data-ttu-id="ae513-142">Microsoft.Azure.Commands.NotificationHubs.models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ae513-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ae513-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ae513-143">NOTES</span></span>

## <span data-ttu-id="ae513-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae513-144">RELATED LINKS</span></span>

[<span data-ttu-id="ae513-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ae513-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="ae513-146">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ae513-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="ae513-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ae513-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="ae513-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ae513-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


