---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 74ad4f80a25250129d050ed3a2769dca6f776376
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901741"
---
# <span data-ttu-id="e7e4f-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e7e4f-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="e7e4f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e7e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e4f-103">建立授權規則，並將規則指派給通知中樞。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="e7e4f-104">語法</span><span class="sxs-lookup"><span data-stu-id="e7e4f-104">SYNTAX</span></span>

### <span data-ttu-id="e7e4f-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7e4f-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7e4f-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7e4f-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7e4f-107">描述</span><span class="sxs-lookup"><span data-stu-id="e7e4f-107">DESCRIPTION</span></span>
<span data-ttu-id="e7e4f-108">**New-AzNotificationHubAuthorizationRule** Cmdlet 會建立通知中樞共用存取簽名 (SAS) 規則。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="e7e4f-109">授權規則可用來管理通知中樞的存取權。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="e7e4f-110">這是以不同許可權等級為基礎建立連結做為 URI 所完成。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="e7e4f-111">用戶端會依據適當的許可權等級，導向至其中一個 URI。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="e7e4f-112">例如，提供聆聽許可權的用戶端會導向至該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="e7e4f-113">例子</span><span class="sxs-lookup"><span data-stu-id="e7e4f-113">EXAMPLES</span></span>

### <span data-ttu-id="e7e4f-114">範例 1：建立通知中樞授權規則</span><span class="sxs-lookup"><span data-stu-id="e7e4f-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="e7e4f-115">此命令會建立新授權規則，並將它指派給名為 ContosoInternalHub 的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="e7e4f-116">此中樞位於 ContosoNamespace 命名空間中，並指派給 ContosoNotificationsGroup 資源群組。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="e7e4f-117">請注意，規則的所有組案資訊 ，包括規則名稱，都會取自您C:\Configuration\ExternalAccessRule.js檔案。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="e7e4f-118">參數</span><span class="sxs-lookup"><span data-stu-id="e7e4f-118">PARAMETERS</span></span>

### <span data-ttu-id="e7e4f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e4f-119">-DefaultProfile</span></span>
<span data-ttu-id="e7e4f-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e7e4f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7e4f-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="e7e4f-121">-InputFile</span></span>
<span data-ttu-id="e7e4f-122">指定此 Cmdlet 所建立之授權規則的輸入檔案。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e7e4f-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e7e4f-123">-Namespace</span></span>
<span data-ttu-id="e7e4f-124">指定指派授權規則的命名空間。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="e7e4f-125">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="e7e4f-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="e7e4f-126">-NotificationHub</span></span>
<span data-ttu-id="e7e4f-127">指定指派授權規則的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="e7e4f-128">通知中樞可用來傳送推入通知給多個用戶端，無論這些用戶端使用哪個平臺。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="e7e4f-129">請注意，您必須指定現有通知中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="e7e4f-130">**New-AzNotificationHubAuthorizationRule** Cmdlet 無法建立新通知中樞。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="e7e4f-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e7e4f-131">-ResourceGroup</span></span>
<span data-ttu-id="e7e4f-132">指定指派通知中樞的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="e7e4f-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="e7e4f-133">-SASRule</span></span>
<span data-ttu-id="e7e4f-134">指定 **SharedAccessAuthorizationRuleAttributes** 物件，其中包含新規則的組定資訊。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="e7e4f-135">-確認</span><span class="sxs-lookup"><span data-stu-id="e7e4f-135">-Confirm</span></span>
<span data-ttu-id="e7e4f-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7e4f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7e4f-137">-WhatIf</span></span>
<span data-ttu-id="e7e4f-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7e4f-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7e4f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e4f-140">CommonParameters</span></span>
<span data-ttu-id="e7e4f-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e4f-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e7e4f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e4f-143">輸入</span><span class="sxs-lookup"><span data-stu-id="e7e4f-143">INPUTS</span></span>

### <span data-ttu-id="e7e4f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e7e4f-144">System.String</span></span>

## <span data-ttu-id="e7e4f-145">輸出</span><span class="sxs-lookup"><span data-stu-id="e7e4f-145">OUTPUTS</span></span>

### <span data-ttu-id="e7e4f-146">Microsoft.Azure.Commands.NotificationHubs.models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e7e4f-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e7e4f-147">筆記</span><span class="sxs-lookup"><span data-stu-id="e7e4f-147">NOTES</span></span>

## <span data-ttu-id="e7e4f-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7e4f-148">RELATED LINKS</span></span>

[<span data-ttu-id="e7e4f-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e7e4f-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="e7e4f-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e7e4f-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="e7e4f-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e7e4f-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


