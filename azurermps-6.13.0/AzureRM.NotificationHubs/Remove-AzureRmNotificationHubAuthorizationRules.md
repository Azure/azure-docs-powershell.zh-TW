---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 7e731052219c796b6e8453c64accd0cf8c25895a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448993"
---
# <span data-ttu-id="a95d1-101">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a95d1-101">Remove-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="a95d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a95d1-102">SYNOPSIS</span></span>
<span data-ttu-id="a95d1-103">從通知中樞移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="a95d1-103">Removes an authorization rule from a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a95d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="a95d1-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a95d1-105">說明</span><span class="sxs-lookup"><span data-stu-id="a95d1-105">DESCRIPTION</span></span>
<span data-ttu-id="a95d1-106">**AzureRmNotificationHubAuthorizationRules** Cmdlet 會從通知中樞中移除 (SAS) 授權規則的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="a95d1-106">The **Remove-AzureRmNotificationHubAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="a95d1-107">授權規則會根據不同的許可權等級，透過建立連結（例如 Uri）來管理通知中樞的存取權。</span><span class="sxs-lookup"><span data-stu-id="a95d1-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="a95d1-108">許可權等級可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="a95d1-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="a95d1-109">聆聽</span><span class="sxs-lookup"><span data-stu-id="a95d1-109">Listen</span></span>
- <span data-ttu-id="a95d1-110">發送</span><span class="sxs-lookup"><span data-stu-id="a95d1-110">Send</span></span>
- <span data-ttu-id="a95d1-111">系統會根據適當的許可權等級，將管理用戶端導向到其中一個 Uri。</span><span class="sxs-lookup"><span data-stu-id="a95d1-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="a95d1-112">例如，擁有偵聽許可權的用戶端將會導向該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="a95d1-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="a95d1-113">移除授權規則也會移除對應的使用者許可權。</span><span class="sxs-lookup"><span data-stu-id="a95d1-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="a95d1-114">示例</span><span class="sxs-lookup"><span data-stu-id="a95d1-114">EXAMPLES</span></span>

### <span data-ttu-id="a95d1-115">範例1：從通知中樞移除授權規則</span><span class="sxs-lookup"><span data-stu-id="a95d1-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="a95d1-116">這個命令會從名為 [ContosoExternalHub] 的通知中心中移除名為 ListenRule 的授權規則。</span><span class="sxs-lookup"><span data-stu-id="a95d1-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="a95d1-117">當您執行此命令時，您必須指定該中樞所指派的命名空間和資源群組。</span><span class="sxs-lookup"><span data-stu-id="a95d1-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="a95d1-118">參數</span><span class="sxs-lookup"><span data-stu-id="a95d1-118">PARAMETERS</span></span>

### <span data-ttu-id="a95d1-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a95d1-119">-AuthorizationRule</span></span>
<span data-ttu-id="a95d1-120">指定此 Cmdlet 移除之 SAS 驗證規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95d1-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95d1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95d1-121">-DefaultProfile</span></span>
<span data-ttu-id="a95d1-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a95d1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a95d1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a95d1-123">-Force</span></span>
<span data-ttu-id="a95d1-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="a95d1-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a95d1-125">-命名空間</span><span class="sxs-lookup"><span data-stu-id="a95d1-125">-Namespace</span></span>
<span data-ttu-id="a95d1-126">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="a95d1-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="a95d1-127">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="a95d1-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="a95d1-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="a95d1-128">-NotificationHub</span></span>
<span data-ttu-id="a95d1-129">指定授權規則指派給哪個通知中樞。</span><span class="sxs-lookup"><span data-stu-id="a95d1-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="a95d1-130">通知中樞可用來傳送推播通知給多個用戶端，而不論平臺為何。</span><span class="sxs-lookup"><span data-stu-id="a95d1-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="a95d1-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a95d1-131">-ResourceGroup</span></span>
<span data-ttu-id="a95d1-132">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="a95d1-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="a95d1-133">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="a95d1-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="a95d1-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a95d1-134">-Confirm</span></span>
<span data-ttu-id="a95d1-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a95d1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a95d1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a95d1-136">-WhatIf</span></span>
<span data-ttu-id="a95d1-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a95d1-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a95d1-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a95d1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a95d1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95d1-139">CommonParameters</span></span>
<span data-ttu-id="a95d1-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a95d1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95d1-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a95d1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95d1-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a95d1-142">INPUTS</span></span>

### <span data-ttu-id="a95d1-143">System.object</span><span class="sxs-lookup"><span data-stu-id="a95d1-143">System.String</span></span>

## <span data-ttu-id="a95d1-144">輸出</span><span class="sxs-lookup"><span data-stu-id="a95d1-144">OUTPUTS</span></span>

### <span data-ttu-id="a95d1-145">System.void</span><span class="sxs-lookup"><span data-stu-id="a95d1-145">System.Void</span></span>

## <span data-ttu-id="a95d1-146">筆記</span><span class="sxs-lookup"><span data-stu-id="a95d1-146">NOTES</span></span>

## <span data-ttu-id="a95d1-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="a95d1-147">RELATED LINKS</span></span>

[<span data-ttu-id="a95d1-148">AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a95d1-148">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="a95d1-149">新-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a95d1-149">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="a95d1-150">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a95d1-150">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


