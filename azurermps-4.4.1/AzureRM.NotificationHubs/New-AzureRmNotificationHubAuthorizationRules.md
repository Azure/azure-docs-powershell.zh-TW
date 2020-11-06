---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: c3a30457e6fd25aa633a0faa0510ed4ce61efbd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449594"
---
# <span data-ttu-id="bb42a-101">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="bb42a-101">New-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="bb42a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb42a-102">SYNOPSIS</span></span>
<span data-ttu-id="bb42a-103">建立授權規則，並將規則指派給通知中樞。</span><span class="sxs-lookup"><span data-stu-id="bb42a-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb42a-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb42a-104">SYNTAX</span></span>

### <span data-ttu-id="bb42a-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb42a-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb42a-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb42a-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb42a-107">說明</span><span class="sxs-lookup"><span data-stu-id="bb42a-107">DESCRIPTION</span></span>
<span data-ttu-id="bb42a-108">**新的-AzureRmNotificationHubAuthorizationRules** Cmdlet 會在 (SAS) 授權規則中建立通知中樞共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="bb42a-108">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>

<span data-ttu-id="bb42a-109">授權規則可用來管理您的通知中樞的存取權。</span><span class="sxs-lookup"><span data-stu-id="bb42a-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="bb42a-110">根據不同許可權等級建立連結（例如 Uri）來完成。</span><span class="sxs-lookup"><span data-stu-id="bb42a-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="bb42a-111">用戶端會根據適當的許可權等級，導向到其中一個 Uri。</span><span class="sxs-lookup"><span data-stu-id="bb42a-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="bb42a-112">例如，擁有 [偵聽] 許可權的用戶端將會導向該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="bb42a-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="bb42a-113">示例</span><span class="sxs-lookup"><span data-stu-id="bb42a-113">EXAMPLES</span></span>

### <span data-ttu-id="bb42a-114">範例1：建立通知中心授權規則</span><span class="sxs-lookup"><span data-stu-id="bb42a-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="bb42a-115">這個命令會建立新的授權規則，並將它指派給名為 ContosoInternalHub 的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="bb42a-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="bb42a-116">此中樞位於 ContosoNamespace 命名空間中，且已指派給 ContosoNotificationsGroup 資源群組。</span><span class="sxs-lookup"><span data-stu-id="bb42a-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="bb42a-117">請注意，規則的所有配置資訊，包括規則名稱，都將從 C:\Configuration\ExternalAccessRule.js的輸入檔案中取得。</span><span class="sxs-lookup"><span data-stu-id="bb42a-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="bb42a-118">參數</span><span class="sxs-lookup"><span data-stu-id="bb42a-118">PARAMETERS</span></span>

### <span data-ttu-id="bb42a-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="bb42a-119">-InputFile</span></span>
<span data-ttu-id="bb42a-120">指定此 Cmdlet 所建立之授權規則的輸入檔。</span><span class="sxs-lookup"><span data-stu-id="bb42a-120">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bb42a-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="bb42a-121">-Namespace</span></span>
<span data-ttu-id="bb42a-122">指定授權規則指派的命名空間。</span><span class="sxs-lookup"><span data-stu-id="bb42a-122">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="bb42a-123">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="bb42a-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="bb42a-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="bb42a-124">-NotificationHub</span></span>
<span data-ttu-id="bb42a-125">指定授權規則將指派給哪個通知中樞。</span><span class="sxs-lookup"><span data-stu-id="bb42a-125">Specifies the notification hub that the authorization rules will be assigned to.</span></span>

<span data-ttu-id="bb42a-126">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="bb42a-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="bb42a-127">請注意，您必須指定現有通知中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb42a-127">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="bb42a-128">**新的-AzureRmNotificationHubAuthorizationRules** Cmdlet 無法建立新的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="bb42a-128">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="bb42a-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bb42a-129">-ResourceGroup</span></span>
<span data-ttu-id="bb42a-130">指定將通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="bb42a-130">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="bb42a-131">-SASRule</span><span class="sxs-lookup"><span data-stu-id="bb42a-131">-SASRule</span></span>
<span data-ttu-id="bb42a-132">指定包含新規則之配置資訊的 **SharedAccessAuthorizationRuleAttributes** 物件。</span><span class="sxs-lookup"><span data-stu-id="bb42a-132">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="bb42a-133">-確認</span><span class="sxs-lookup"><span data-stu-id="bb42a-133">-Confirm</span></span>
<span data-ttu-id="bb42a-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bb42a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb42a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb42a-135">-WhatIf</span></span>
<span data-ttu-id="bb42a-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb42a-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb42a-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb42a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb42a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb42a-138">-DefaultProfile</span></span>
<span data-ttu-id="bb42a-139">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb42a-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb42a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb42a-140">CommonParameters</span></span>
<span data-ttu-id="bb42a-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb42a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb42a-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb42a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb42a-143">輸入</span><span class="sxs-lookup"><span data-stu-id="bb42a-143">INPUTS</span></span>

## <span data-ttu-id="bb42a-144">輸出</span><span class="sxs-lookup"><span data-stu-id="bb42a-144">OUTPUTS</span></span>

### <span data-ttu-id="bb42a-145">SharedAccessAuthorizationRuleAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="bb42a-145">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="bb42a-146">筆記</span><span class="sxs-lookup"><span data-stu-id="bb42a-146">NOTES</span></span>

## <span data-ttu-id="bb42a-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb42a-147">RELATED LINKS</span></span>

[<span data-ttu-id="bb42a-148">AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="bb42a-148">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="bb42a-149">移除-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="bb42a-149">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="bb42a-150">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="bb42a-150">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


