---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 260cf95d04d6a923acbdeaa91a412aa0046d9ea0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901774"
---
# <span data-ttu-id="29d9a-101">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="29d9a-101">Get-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="29d9a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="29d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="29d9a-103">獲得與通知中樞相關聯的授權規則相關資訊。</span><span class="sxs-lookup"><span data-stu-id="29d9a-103">Gets information about the authorization rules associated with a notification hub.</span></span>

## <span data-ttu-id="29d9a-104">語法</span><span class="sxs-lookup"><span data-stu-id="29d9a-104">SYNTAX</span></span>

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29d9a-105">描述</span><span class="sxs-lookup"><span data-stu-id="29d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="29d9a-106">**Get-AzNotificationHubAuthorizationRule** Cmdlet 會取得與通知中樞相關聯的共用存取簽章 (SAS) 授權規則相關資訊。</span><span class="sxs-lookup"><span data-stu-id="29d9a-106">The **Get-AzNotificationHubAuthorizationRule** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="29d9a-107">Cmdlet 會返回與中樞相關聯的所有規則相關資訊，或包含 *AuthorizationRule* 參數，以獲得特定規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="29d9a-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="29d9a-108">授權規則可管理您通知中樞的存取權。</span><span class="sxs-lookup"><span data-stu-id="29d9a-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="29d9a-109">授權規則會根據不同的許可權等級，建立連結作為 URI。</span><span class="sxs-lookup"><span data-stu-id="29d9a-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="29d9a-110">用戶端會依據適當的許可權等級，導向至其中一個 URI。</span><span class="sxs-lookup"><span data-stu-id="29d9a-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="29d9a-111">例如，具有聆聽許可權的用戶端會導向至該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="29d9a-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="29d9a-112">**Get-AzNotificationHubAuthorizationRule** Cmdlet 只會取得與通知中樞相關聯的授權規則相關資訊。</span><span class="sxs-lookup"><span data-stu-id="29d9a-112">The **Get-AzNotificationHubAuthorizationRule** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="29d9a-113">若要取得中樞本身的資訊，請使用 Get-AzNotificationHub。</span><span class="sxs-lookup"><span data-stu-id="29d9a-113">To get information about the hub itself, use Get-AzNotificationHub.</span></span>

## <span data-ttu-id="29d9a-114">例子</span><span class="sxs-lookup"><span data-stu-id="29d9a-114">EXAMPLES</span></span>

### <span data-ttu-id="29d9a-115">範例 1：取得指派給通知中心之所有授權規則的資訊</span><span class="sxs-lookup"><span data-stu-id="29d9a-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="29d9a-116">此命令會針對指派給命名空間 ContosoNamespace 中名為 ContosoInternalHub 之通知中樞的所有授權規則，獲得相關資訊。</span><span class="sxs-lookup"><span data-stu-id="29d9a-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="29d9a-117">您必須指定中樞所在的命名空間，以及中樞已指派給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="29d9a-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="29d9a-118">範例 2：取得指派給通知中樞之授權規則的資訊</span><span class="sxs-lookup"><span data-stu-id="29d9a-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="29d9a-119">此命令會針對指派給命名空間 ContosoNamespace 中名為 ContosoInternalHub 之通知中樞的所有授權規則，獲得相關資訊。</span><span class="sxs-lookup"><span data-stu-id="29d9a-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="29d9a-120">該命令使用 *AuthorizationRule* 參數，將所返回的資料限制為名為 ListenRule 的單一授權規則。</span><span class="sxs-lookup"><span data-stu-id="29d9a-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="29d9a-121">參數</span><span class="sxs-lookup"><span data-stu-id="29d9a-121">PARAMETERS</span></span>

### <span data-ttu-id="29d9a-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="29d9a-122">-AuthorizationRule</span></span>
<span data-ttu-id="29d9a-123">指定 SAS 驗證規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="29d9a-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="29d9a-124">這些規則會決定使用者對通知中樞的存取類型。</span><span class="sxs-lookup"><span data-stu-id="29d9a-124">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29d9a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d9a-125">-DefaultProfile</span></span>
<span data-ttu-id="29d9a-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="29d9a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29d9a-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="29d9a-127">-Namespace</span></span>
<span data-ttu-id="29d9a-128">指定指派通知中樞的命名空間。</span><span class="sxs-lookup"><span data-stu-id="29d9a-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="29d9a-129">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="29d9a-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="29d9a-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="29d9a-130">-NotificationHub</span></span>
<span data-ttu-id="29d9a-131">指定此 Cmdlet 指派授權規則的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="29d9a-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="29d9a-132">通知中樞可用來傳送推入通知給多個用戶端，無論這些用戶端使用哪個平臺。</span><span class="sxs-lookup"><span data-stu-id="29d9a-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="29d9a-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="29d9a-133">-ResourceGroup</span></span>
<span data-ttu-id="29d9a-134">指定指派通知中樞給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="29d9a-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="29d9a-135">資源群組會以有助於簡化庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="29d9a-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="29d9a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d9a-136">CommonParameters</span></span>
<span data-ttu-id="29d9a-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="29d9a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d9a-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="29d9a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d9a-139">輸入</span><span class="sxs-lookup"><span data-stu-id="29d9a-139">INPUTS</span></span>

### <span data-ttu-id="29d9a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="29d9a-140">System.String</span></span>

## <span data-ttu-id="29d9a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="29d9a-141">OUTPUTS</span></span>

### <span data-ttu-id="29d9a-142">Microsoft.Azure.Commands.NotificationHubs.models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="29d9a-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="29d9a-143">筆記</span><span class="sxs-lookup"><span data-stu-id="29d9a-143">NOTES</span></span>

## <span data-ttu-id="29d9a-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="29d9a-144">RELATED LINKS</span></span>

[<span data-ttu-id="29d9a-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="29d9a-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="29d9a-146">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="29d9a-146">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="29d9a-147">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="29d9a-147">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="29d9a-148">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="29d9a-148">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


