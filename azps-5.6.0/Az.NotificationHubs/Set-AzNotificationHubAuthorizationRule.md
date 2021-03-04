---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 30c6a16d7b9cfb94f1fb2032940aa4587d27e550
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901698"
---
# <span data-ttu-id="acd9a-101">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="acd9a-101">Set-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="acd9a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="acd9a-102">SYNOPSIS</span></span>
<span data-ttu-id="acd9a-103">設定通知中樞的授權規則。</span><span class="sxs-lookup"><span data-stu-id="acd9a-103">Sets authorization rules for a notification hub.</span></span>

## <span data-ttu-id="acd9a-104">語法</span><span class="sxs-lookup"><span data-stu-id="acd9a-104">SYNTAX</span></span>

### <span data-ttu-id="acd9a-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="acd9a-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acd9a-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="acd9a-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acd9a-107">描述</span><span class="sxs-lookup"><span data-stu-id="acd9a-107">DESCRIPTION</span></span>
<span data-ttu-id="acd9a-108">**Set-AzNotificationHubAuthorizationRule** Cmdlet 會修改指派給通知中樞的共用存取簽名 (SAS) 授權規則。</span><span class="sxs-lookup"><span data-stu-id="acd9a-108">The **Set-AzNotificationHubAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="acd9a-109">授權規則會依據不同的許可權等級，建立連結做為 URI 來管理通知中樞的存取權。</span><span class="sxs-lookup"><span data-stu-id="acd9a-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="acd9a-110">許可權等級可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="acd9a-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="acd9a-111">聽</span><span class="sxs-lookup"><span data-stu-id="acd9a-111">Listen</span></span>
- <span data-ttu-id="acd9a-112">發送</span><span class="sxs-lookup"><span data-stu-id="acd9a-112">Send</span></span>
- <span data-ttu-id="acd9a-113">管理用戶端會依據適當的許可權等級，導向至其中一個 URI。</span><span class="sxs-lookup"><span data-stu-id="acd9a-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="acd9a-114">例如，提供聆聽許可權的用戶端會導向至該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="acd9a-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="acd9a-115">此 Cmdlet 提供兩種方式來修改指派給通知中樞的授權規則。</span><span class="sxs-lookup"><span data-stu-id="acd9a-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="acd9a-116">例如，您可以建立 **SharedAccessAuthorizationRuleAttributes** 物件的實例，然後將該物件設定為您想要規則擁有的屬性值。</span><span class="sxs-lookup"><span data-stu-id="acd9a-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="acd9a-117">您可以透過 .NET Framework 設定物件。</span><span class="sxs-lookup"><span data-stu-id="acd9a-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="acd9a-118">接著，您可以使用 *SASRule* 參數，將那些屬性值複製到規則。</span><span class="sxs-lookup"><span data-stu-id="acd9a-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="acd9a-119">或者，您可以建立 JSON (JavaScript 物件表示) 包含相關組設定值的檔案，然後透過 *InputFile* 參數來使用這些值。</span><span class="sxs-lookup"><span data-stu-id="acd9a-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="acd9a-120">JSON 檔案是使用類似以下語法的文字檔：{ "Name"： "ContosoAuthorizationRule"，</span><span class="sxs-lookup"><span data-stu-id="acd9a-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="acd9a-121">"PrimaryKey"："WE4qH0398AyXjlekt56gg1g VM3NHoMs29KkUnnpUk01Y="，</span><span class="sxs-lookup"><span data-stu-id="acd9a-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="acd9a-122">"Rights"： \[</span><span class="sxs-lookup"><span data-stu-id="acd9a-122">"Rights": \[</span></span>  
        <span data-ttu-id="acd9a-123">「聆聽」，</span><span class="sxs-lookup"><span data-stu-id="acd9a-123">"Listen",</span></span>  
        <span data-ttu-id="acd9a-124">「傳送」</span><span class="sxs-lookup"><span data-stu-id="acd9a-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="acd9a-125">} 與 New-AzNotificationHubAuthorizationRule Cmdlet 一起使用時，上述 JSON 範例會修改名為 ContosoAuthorizationRule 的授權規則，以便讓使用者擁有中樞的聆聽和傳送許可權。</span><span class="sxs-lookup"><span data-stu-id="acd9a-125">} When used in conjunction with the New-AzNotificationHubAuthorizationRule cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="acd9a-126">例子</span><span class="sxs-lookup"><span data-stu-id="acd9a-126">EXAMPLES</span></span>

### <span data-ttu-id="acd9a-127">範例 1：修改指派給通知中樞的授權規則</span><span class="sxs-lookup"><span data-stu-id="acd9a-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="acd9a-128">此命令會修改指派給 ContosoExternalHub 通知中樞的授權規則。</span><span class="sxs-lookup"><span data-stu-id="acd9a-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="acd9a-129">您必須指定中樞所在的命名空間，以及指派中樞的資源群組。</span><span class="sxs-lookup"><span data-stu-id="acd9a-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="acd9a-130">已修改規則的資訊不會包含在命令本身中。</span><span class="sxs-lookup"><span data-stu-id="acd9a-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="acd9a-131">相反地，該資訊會位於您C:\Configuration\AuthorizationRules.js檔案中。</span><span class="sxs-lookup"><span data-stu-id="acd9a-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="acd9a-132">參數</span><span class="sxs-lookup"><span data-stu-id="acd9a-132">PARAMETERS</span></span>

### <span data-ttu-id="acd9a-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd9a-133">-DefaultProfile</span></span>
<span data-ttu-id="acd9a-134">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="acd9a-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acd9a-135">-強制</span><span class="sxs-lookup"><span data-stu-id="acd9a-135">-Force</span></span>
<span data-ttu-id="acd9a-136">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="acd9a-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="acd9a-137">-InputFile</span><span class="sxs-lookup"><span data-stu-id="acd9a-137">-InputFile</span></span>
<span data-ttu-id="acd9a-138">指定 JSON 檔案的路徑，其中包含新規則的組程資訊。</span><span class="sxs-lookup"><span data-stu-id="acd9a-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="acd9a-139">-命名空間</span><span class="sxs-lookup"><span data-stu-id="acd9a-139">-Namespace</span></span>
<span data-ttu-id="acd9a-140">指定指派通知中樞的命名空間。</span><span class="sxs-lookup"><span data-stu-id="acd9a-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="acd9a-141">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="acd9a-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="acd9a-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="acd9a-142">-NotificationHub</span></span>
<span data-ttu-id="acd9a-143">指定此 Cmdlet 指派授權規則的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="acd9a-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="acd9a-144">通知中樞可用來傳送推入通知給多個用戶端，而不管這些用戶端使用什麼。</span><span class="sxs-lookup"><span data-stu-id="acd9a-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="acd9a-145">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="acd9a-145">-ResourceGroup</span></span>
<span data-ttu-id="acd9a-146">指定指派通知中樞給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="acd9a-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="acd9a-147">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="acd9a-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="acd9a-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="acd9a-148">-SASRule</span></span>
<span data-ttu-id="acd9a-149">指定 **SharedAccessAuthorizationRuleAttributes** 物件，該物件包含已修改之授權規則的組定資訊。</span><span class="sxs-lookup"><span data-stu-id="acd9a-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="acd9a-150">-確認</span><span class="sxs-lookup"><span data-stu-id="acd9a-150">-Confirm</span></span>
<span data-ttu-id="acd9a-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="acd9a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acd9a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acd9a-152">-WhatIf</span></span>
<span data-ttu-id="acd9a-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="acd9a-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="acd9a-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="acd9a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acd9a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd9a-155">CommonParameters</span></span>
<span data-ttu-id="acd9a-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="acd9a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd9a-157">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="acd9a-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd9a-158">輸入</span><span class="sxs-lookup"><span data-stu-id="acd9a-158">INPUTS</span></span>

### <span data-ttu-id="acd9a-159">System.String</span><span class="sxs-lookup"><span data-stu-id="acd9a-159">System.String</span></span>

## <span data-ttu-id="acd9a-160">輸出</span><span class="sxs-lookup"><span data-stu-id="acd9a-160">OUTPUTS</span></span>

### <span data-ttu-id="acd9a-161">Microsoft.Azure.Commands.NotificationHubs.models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="acd9a-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="acd9a-162">筆記</span><span class="sxs-lookup"><span data-stu-id="acd9a-162">NOTES</span></span>

## <span data-ttu-id="acd9a-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="acd9a-163">RELATED LINKS</span></span>

[<span data-ttu-id="acd9a-164">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="acd9a-164">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="acd9a-165">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="acd9a-165">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="acd9a-166">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="acd9a-166">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)


