---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 436ed6aaa720074be2014d9c736ab0636a09869f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791421"
---
# <span data-ttu-id="85451-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="85451-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="85451-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85451-102">SYNOPSIS</span></span>
<span data-ttu-id="85451-103">建立授權規則，並將規則指派給通知中樞。</span><span class="sxs-lookup"><span data-stu-id="85451-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="85451-104">句法</span><span class="sxs-lookup"><span data-stu-id="85451-104">SYNTAX</span></span>

### <span data-ttu-id="85451-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="85451-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85451-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="85451-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85451-107">說明</span><span class="sxs-lookup"><span data-stu-id="85451-107">DESCRIPTION</span></span>
<span data-ttu-id="85451-108">**新的-AzNotificationHubAuthorizationRule** Cmdlet 會在 (SAS) 授權規則中建立通知中樞共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="85451-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="85451-109">授權規則可用來管理您的通知中樞的存取權。</span><span class="sxs-lookup"><span data-stu-id="85451-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="85451-110">根據不同許可權等級建立連結（例如 Uri）來完成。</span><span class="sxs-lookup"><span data-stu-id="85451-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="85451-111">用戶端會根據適當的許可權等級，導向到其中一個 Uri。</span><span class="sxs-lookup"><span data-stu-id="85451-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="85451-112">例如，擁有 [偵聽] 許可權的用戶端將會導向該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="85451-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="85451-113">示例</span><span class="sxs-lookup"><span data-stu-id="85451-113">EXAMPLES</span></span>

### <span data-ttu-id="85451-114">範例1：建立通知中心授權規則</span><span class="sxs-lookup"><span data-stu-id="85451-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="85451-115">這個命令會建立新的授權規則，並將它指派給名為 ContosoInternalHub 的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="85451-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="85451-116">此中樞位於 ContosoNamespace 命名空間中，且已指派給 ContosoNotificationsGroup 資源群組。</span><span class="sxs-lookup"><span data-stu-id="85451-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="85451-117">請注意，規則的所有配置資訊，包括規則名稱，都將從 C:\Configuration\ExternalAccessRule.js的輸入檔案中取得。</span><span class="sxs-lookup"><span data-stu-id="85451-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="85451-118">參數</span><span class="sxs-lookup"><span data-stu-id="85451-118">PARAMETERS</span></span>

### <span data-ttu-id="85451-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85451-119">-DefaultProfile</span></span>
<span data-ttu-id="85451-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="85451-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85451-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="85451-121">-InputFile</span></span>
<span data-ttu-id="85451-122">指定此 Cmdlet 所建立之授權規則的輸入檔。</span><span class="sxs-lookup"><span data-stu-id="85451-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85451-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="85451-123">-Namespace</span></span>
<span data-ttu-id="85451-124">指定授權規則指派的命名空間。</span><span class="sxs-lookup"><span data-stu-id="85451-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="85451-125">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="85451-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="85451-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="85451-126">-NotificationHub</span></span>
<span data-ttu-id="85451-127">指定授權規則將指派給哪個通知中樞。</span><span class="sxs-lookup"><span data-stu-id="85451-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="85451-128">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="85451-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="85451-129">請注意，您必須指定現有通知中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="85451-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="85451-130">**新的-AzNotificationHubAuthorizationRule** Cmdlet 無法建立新的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="85451-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="85451-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="85451-131">-ResourceGroup</span></span>
<span data-ttu-id="85451-132">指定將通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="85451-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="85451-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="85451-133">-SASRule</span></span>
<span data-ttu-id="85451-134">指定包含新規則之配置資訊的 **SharedAccessAuthorizationRuleAttributes** 物件。</span><span class="sxs-lookup"><span data-stu-id="85451-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85451-135">-確認</span><span class="sxs-lookup"><span data-stu-id="85451-135">-Confirm</span></span>
<span data-ttu-id="85451-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="85451-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85451-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85451-137">-WhatIf</span></span>
<span data-ttu-id="85451-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="85451-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85451-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85451-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85451-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85451-140">CommonParameters</span></span>
<span data-ttu-id="85451-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85451-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85451-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85451-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85451-143">輸入</span><span class="sxs-lookup"><span data-stu-id="85451-143">INPUTS</span></span>

### <span data-ttu-id="85451-144">System.object</span><span class="sxs-lookup"><span data-stu-id="85451-144">System.String</span></span>

## <span data-ttu-id="85451-145">輸出</span><span class="sxs-lookup"><span data-stu-id="85451-145">OUTPUTS</span></span>

### <span data-ttu-id="85451-146">SharedAccessAuthorizationRuleAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="85451-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="85451-147">筆記</span><span class="sxs-lookup"><span data-stu-id="85451-147">NOTES</span></span>

## <span data-ttu-id="85451-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="85451-148">RELATED LINKS</span></span>

[<span data-ttu-id="85451-149">AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="85451-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="85451-150">移除-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="85451-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="85451-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="85451-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


