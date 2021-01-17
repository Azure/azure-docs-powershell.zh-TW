---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450101"
---
# <span data-ttu-id="bc10f-101">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bc10f-101">Get-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="bc10f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc10f-102">SYNOPSIS</span></span>
<span data-ttu-id="bc10f-103">取得與通知中樞相關聯之授權規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bc10f-103">Gets information about the authorization rules associated with a notification hub.</span></span>

## <span data-ttu-id="bc10f-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc10f-104">SYNTAX</span></span>

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc10f-105">說明</span><span class="sxs-lookup"><span data-stu-id="bc10f-105">DESCRIPTION</span></span>
<span data-ttu-id="bc10f-106">**AzNotificationHubAuthorizationRule** Cmdlet 會取得共用存取簽章 (SAS) 與通知中樞相關聯的授權規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="bc10f-106">The **Get-AzNotificationHubAuthorizationRule** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="bc10f-107">Cmdlet 會傳回與中心有關的所有規則的相關資訊，或包含 *AuthorizationRule* 參數，取得特定規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bc10f-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="bc10f-108">授權規則可管理您通知中樞的存取權。</span><span class="sxs-lookup"><span data-stu-id="bc10f-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="bc10f-109">授權規則將根據不同的許可權等級，以 URI 來建立連結。</span><span class="sxs-lookup"><span data-stu-id="bc10f-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="bc10f-110">用戶端會根據適當的許可權等級，導向到其中一個 Uri。</span><span class="sxs-lookup"><span data-stu-id="bc10f-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="bc10f-111">例如，擁有 [偵聽] 許可權的客戶將會被導向該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="bc10f-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="bc10f-112">**AzNotificationHubAuthorizationRule** Cmdlet 只會取得與通知中樞相關聯之授權規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bc10f-112">The **Get-AzNotificationHubAuthorizationRule** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="bc10f-113">若要取得中心本身的相關資訊，請使用 AzNotificationHub。</span><span class="sxs-lookup"><span data-stu-id="bc10f-113">To get information about the hub itself, use Get-AzNotificationHub.</span></span>

## <span data-ttu-id="bc10f-114">示例</span><span class="sxs-lookup"><span data-stu-id="bc10f-114">EXAMPLES</span></span>

### <span data-ttu-id="bc10f-115">範例1：取得指派給通知中心的所有授權規則資訊</span><span class="sxs-lookup"><span data-stu-id="bc10f-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="bc10f-116">這個命令會取得指派給命名空間 ContosoNamespace 中名為 ContosoInternalHub 之通知中樞之所有授權規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="bc10f-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="bc10f-117">您必須指定中樞所在的命名空間，以及該中樞已獲指派的資源群組。</span><span class="sxs-lookup"><span data-stu-id="bc10f-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="bc10f-118">範例2：取得指派給通知中心的授權規則資訊</span><span class="sxs-lookup"><span data-stu-id="bc10f-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="bc10f-119">這個命令會取得指派給命名空間 ContosoNamespace 中名為 ContosoInternalHub 之通知中樞之所有授權規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="bc10f-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="bc10f-120">此命令會使用 *AuthorizationRule* 參數，將傳回的資料限制為單一的名為 ListenRule 的授權規則。</span><span class="sxs-lookup"><span data-stu-id="bc10f-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="bc10f-121">參數</span><span class="sxs-lookup"><span data-stu-id="bc10f-121">PARAMETERS</span></span>

### <span data-ttu-id="bc10f-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bc10f-122">-AuthorizationRule</span></span>
<span data-ttu-id="bc10f-123">指定 SAS 驗證規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc10f-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="bc10f-124">這些規則決定使用者對通知中樞所擁有的存取類型。</span><span class="sxs-lookup"><span data-stu-id="bc10f-124">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="bc10f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc10f-125">-DefaultProfile</span></span>
<span data-ttu-id="bc10f-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bc10f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc10f-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="bc10f-127">-Namespace</span></span>
<span data-ttu-id="bc10f-128">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="bc10f-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="bc10f-129">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="bc10f-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="bc10f-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="bc10f-130">-NotificationHub</span></span>
<span data-ttu-id="bc10f-131">指定此 Cmdlet 指派授權規則的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="bc10f-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="bc10f-132">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="bc10f-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="bc10f-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bc10f-133">-ResourceGroup</span></span>
<span data-ttu-id="bc10f-134">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="bc10f-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="bc10f-135">資源群組會以協助簡化庫存管理和 Azure 管理的方式，來組織諸如命名空間、通知中心及授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="bc10f-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="bc10f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc10f-136">CommonParameters</span></span>
<span data-ttu-id="bc10f-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc10f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc10f-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bc10f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc10f-139">輸入</span><span class="sxs-lookup"><span data-stu-id="bc10f-139">INPUTS</span></span>

### <span data-ttu-id="bc10f-140">System.object</span><span class="sxs-lookup"><span data-stu-id="bc10f-140">System.String</span></span>

## <span data-ttu-id="bc10f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="bc10f-141">OUTPUTS</span></span>

### <span data-ttu-id="bc10f-142">SharedAccessAuthorizationRuleAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="bc10f-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="bc10f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="bc10f-143">NOTES</span></span>

## <span data-ttu-id="bc10f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc10f-144">RELATED LINKS</span></span>

[<span data-ttu-id="bc10f-145">AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bc10f-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="bc10f-146">新-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bc10f-146">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="bc10f-147">移除-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bc10f-147">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="bc10f-148">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bc10f-148">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


