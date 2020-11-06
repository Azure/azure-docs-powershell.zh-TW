---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: db2b3357b7db90b5d5b310c43afb3f29ca596878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450202"
---
# <span data-ttu-id="3b48b-101">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3b48b-101">Get-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="3b48b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b48b-102">SYNOPSIS</span></span>
<span data-ttu-id="3b48b-103">取得與通知中樞相關聯之授權規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3b48b-103">Gets information about the authorization rules associated with a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b48b-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b48b-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b48b-105">說明</span><span class="sxs-lookup"><span data-stu-id="3b48b-105">DESCRIPTION</span></span>
<span data-ttu-id="3b48b-106">**AzureRmNotificationHubAuthorizationRules** Cmdlet 會取得共用存取簽章 (SAS) 與通知中樞相關聯的授權規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="3b48b-106">The **Get-AzureRmNotificationHubAuthorizationRules** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="3b48b-107">Cmdlet 會傳回與中心有關的所有規則的相關資訊，或包含 *AuthorizationRule* 參數，取得特定規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3b48b-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="3b48b-108">授權規則可管理您通知中樞的存取權。</span><span class="sxs-lookup"><span data-stu-id="3b48b-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="3b48b-109">授權規則將根據不同的許可權等級，以 URI 來建立連結。</span><span class="sxs-lookup"><span data-stu-id="3b48b-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="3b48b-110">用戶端會根據適當的許可權等級，導向到其中一個 Uri。</span><span class="sxs-lookup"><span data-stu-id="3b48b-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="3b48b-111">例如，擁有 [偵聽] 許可權的客戶將會被導向該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="3b48b-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="3b48b-112">**AzureRmNotificationHubAuthorizationRules** Cmdlet 只會取得與通知中樞相關聯之授權規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3b48b-112">The **Get-AzureRmNotificationHubAuthorizationRules** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="3b48b-113">若要取得中心本身的相關資訊，請使用 AzureRmNotificationHub。</span><span class="sxs-lookup"><span data-stu-id="3b48b-113">To get information about the hub itself, use Get-AzureRmNotificationHub.</span></span>

## <span data-ttu-id="3b48b-114">示例</span><span class="sxs-lookup"><span data-stu-id="3b48b-114">EXAMPLES</span></span>

### <span data-ttu-id="3b48b-115">範例1：取得指派給通知中心的所有授權規則資訊</span><span class="sxs-lookup"><span data-stu-id="3b48b-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="3b48b-116">這個命令會取得指派給命名空間 ContosoNamespace 中名為 ContosoInternalHub 之通知中樞之所有授權規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="3b48b-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="3b48b-117">您必須指定中樞所在的命名空間，以及該中樞已獲指派的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3b48b-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="3b48b-118">範例2：取得指派給通知中心的授權規則資訊</span><span class="sxs-lookup"><span data-stu-id="3b48b-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="3b48b-119">這個命令會取得指派給命名空間 ContosoNamespace 中名為 ContosoInternalHub 之通知中樞之所有授權規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="3b48b-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="3b48b-120">此命令會使用 *AuthorizationRule* 參數，將傳回的資料限制為單一的名為 ListenRule 的授權規則。</span><span class="sxs-lookup"><span data-stu-id="3b48b-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="3b48b-121">參數</span><span class="sxs-lookup"><span data-stu-id="3b48b-121">PARAMETERS</span></span>

### <span data-ttu-id="3b48b-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3b48b-122">-AuthorizationRule</span></span>
<span data-ttu-id="3b48b-123">指定 SAS 驗證規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b48b-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="3b48b-124">這些規則決定使用者對通知中樞所擁有的存取類型。</span><span class="sxs-lookup"><span data-stu-id="3b48b-124">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="3b48b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b48b-125">-DefaultProfile</span></span>
<span data-ttu-id="3b48b-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3b48b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b48b-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="3b48b-127">-Namespace</span></span>
<span data-ttu-id="3b48b-128">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="3b48b-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="3b48b-129">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="3b48b-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3b48b-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="3b48b-130">-NotificationHub</span></span>
<span data-ttu-id="3b48b-131">指定此 Cmdlet 指派授權規則的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="3b48b-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="3b48b-132">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="3b48b-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="3b48b-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3b48b-133">-ResourceGroup</span></span>
<span data-ttu-id="3b48b-134">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="3b48b-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="3b48b-135">資源群組會以協助簡化庫存管理和 Azure 管理的方式，來組織諸如命名空間、通知中心及授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="3b48b-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="3b48b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b48b-136">CommonParameters</span></span>
<span data-ttu-id="3b48b-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b48b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b48b-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b48b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b48b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="3b48b-139">INPUTS</span></span>

### <span data-ttu-id="3b48b-140">System.object</span><span class="sxs-lookup"><span data-stu-id="3b48b-140">System.String</span></span>

## <span data-ttu-id="3b48b-141">輸出</span><span class="sxs-lookup"><span data-stu-id="3b48b-141">OUTPUTS</span></span>

### <span data-ttu-id="3b48b-142">SharedAccessAuthorizationRuleAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="3b48b-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="3b48b-143">筆記</span><span class="sxs-lookup"><span data-stu-id="3b48b-143">NOTES</span></span>

## <span data-ttu-id="3b48b-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b48b-144">RELATED LINKS</span></span>

[<span data-ttu-id="3b48b-145">AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3b48b-145">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="3b48b-146">新-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3b48b-146">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="3b48b-147">移除-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3b48b-147">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="3b48b-148">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3b48b-148">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


