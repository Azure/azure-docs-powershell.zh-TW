---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 5396605719908d468399c126fbeca116060c25b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448078"
---
# <span data-ttu-id="bd0f5-101">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="bd0f5-101">Set-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="bd0f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="bd0f5-103">設定通知中樞的授權規則。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-103">Sets authorization rules for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd0f5-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd0f5-104">SYNTAX</span></span>

### <span data-ttu-id="bd0f5-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd0f5-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd0f5-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd0f5-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd0f5-107">說明</span><span class="sxs-lookup"><span data-stu-id="bd0f5-107">DESCRIPTION</span></span>
<span data-ttu-id="bd0f5-108">**AzureRmNotificationHubAuthorizationRules** Cmdlet 會修改指派給通知中樞 (SAS) 授權規則的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-108">The **Set-AzureRmNotificationHubAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>

<span data-ttu-id="bd0f5-109">授權規則會根據不同的許可權等級，以 Uri 來管理通知中樞的存取權。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="bd0f5-110">許可權等級可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="bd0f5-110">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="bd0f5-111">聆聽</span><span class="sxs-lookup"><span data-stu-id="bd0f5-111">Listen</span></span>
- <span data-ttu-id="bd0f5-112">發送</span><span class="sxs-lookup"><span data-stu-id="bd0f5-112">Send</span></span>
- <span data-ttu-id="bd0f5-113">管理</span><span class="sxs-lookup"><span data-stu-id="bd0f5-113">Manage</span></span>

<span data-ttu-id="bd0f5-114">用戶端會根據適當的許可權等級，導向到其中一個 Uri。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-114">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="bd0f5-115">例如，擁有 [偵聽] 許可權的用戶端將會導向該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-115">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="bd0f5-116">這個 Cmdlet 提供兩種方式來修改指派給通知中樞的授權規則。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-116">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="bd0f5-117">若是一個，您可以建立 **SharedAccessAuthorizationRuleAttributes** 物件的實例，然後使用您希望規則擁有的屬性值來設定該物件。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-117">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="bd0f5-118">您可以透過 .NET Framework 來設定物件。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-118">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="bd0f5-119">然後，您可以使用 *SASRule* 參數，將這些屬性值複製到規則。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-119">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="bd0f5-120">或者，您也可以建立 JSON (JavaScript 物件符號) 檔案，其中包含相關的配置值，然後透過 *InputFile* 參數套用這些值。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-120">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="bd0f5-121">JSON 檔案是一個文字檔，該檔案使用類似以下的語法：</span><span class="sxs-lookup"><span data-stu-id="bd0f5-121">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="bd0f5-122">{"Name"： "ContosoAuthorizationRule"，</span><span class="sxs-lookup"><span data-stu-id="bd0f5-122">{      "Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="bd0f5-123">"PrimaryKey"： "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y ="，</span><span class="sxs-lookup"><span data-stu-id="bd0f5-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="bd0f5-124">"版權"： \[</span><span class="sxs-lookup"><span data-stu-id="bd0f5-124">"Rights": \[</span></span>  
        <span data-ttu-id="bd0f5-125">[聆聽]，</span><span class="sxs-lookup"><span data-stu-id="bd0f5-125">"Listen",</span></span>  
        <span data-ttu-id="bd0f5-126">收發</span><span class="sxs-lookup"><span data-stu-id="bd0f5-126">"Send"</span></span>  
    \]  
<span data-ttu-id="bd0f5-127">}</span><span class="sxs-lookup"><span data-stu-id="bd0f5-127">}</span></span>

<span data-ttu-id="bd0f5-128">與 New-AzureRmNotificationHubAuthorizationRules Cmdlet 搭配使用時，前面的 JSON 範例會修改名為 ContosoAuthorizationRule 的授權規則，讓使用者聆聽並傳送許可權給中樞。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-128">When used in conjunction with the New-AzureRmNotificationHubAuthorizationRules cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="bd0f5-129">示例</span><span class="sxs-lookup"><span data-stu-id="bd0f5-129">EXAMPLES</span></span>

### <span data-ttu-id="bd0f5-130">範例1：修改指派給通知中樞的授權規則</span><span class="sxs-lookup"><span data-stu-id="bd0f5-130">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="bd0f5-131">這個命令會修改指派給名為 ContosoExternalHub 之通知中樞的授權規則。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-131">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="bd0f5-132">您必須指定中樞所在的命名空間，以及該中樞指派的資源群組。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-132">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="bd0f5-133">在命令本身中不會包含已修改之規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-133">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="bd0f5-134">相反地，該資訊會在 C:\Configuration\AuthorizationRules.js的輸入檔案中找到。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-134">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="bd0f5-135">參數</span><span class="sxs-lookup"><span data-stu-id="bd0f5-135">PARAMETERS</span></span>

### <span data-ttu-id="bd0f5-136">-Force</span><span class="sxs-lookup"><span data-stu-id="bd0f5-136">-Force</span></span>
<span data-ttu-id="bd0f5-137">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-137">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bd0f5-138">-InputFile</span><span class="sxs-lookup"><span data-stu-id="bd0f5-138">-InputFile</span></span>
<span data-ttu-id="bd0f5-139">指定包含新規則之配置資訊的 JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-139">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="bd0f5-140">-命名空間</span><span class="sxs-lookup"><span data-stu-id="bd0f5-140">-Namespace</span></span>
<span data-ttu-id="bd0f5-141">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-141">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="bd0f5-142">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-142">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="bd0f5-143">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="bd0f5-143">-NotificationHub</span></span>
<span data-ttu-id="bd0f5-144">指定此 Cmdlet 指派授權規則的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-144">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="bd0f5-145">通知中心是用來傳送推播通知給多個用戶端，而不考慮這些用戶端的用途。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-145">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="bd0f5-146">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bd0f5-146">-ResourceGroup</span></span>
<span data-ttu-id="bd0f5-147">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-147">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="bd0f5-148">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-148">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="bd0f5-149">-SASRule</span><span class="sxs-lookup"><span data-stu-id="bd0f5-149">-SASRule</span></span>
<span data-ttu-id="bd0f5-150">指定包含已修改之授權規則之設定資訊的 **SharedAccessAuthorizationRuleAttributes** 物件。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-150">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="bd0f5-151">-確認</span><span class="sxs-lookup"><span data-stu-id="bd0f5-151">-Confirm</span></span>
<span data-ttu-id="bd0f5-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd0f5-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd0f5-153">-WhatIf</span></span>
<span data-ttu-id="bd0f5-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd0f5-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd0f5-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd0f5-156">-DefaultProfile</span></span>
<span data-ttu-id="bd0f5-157">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd0f5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd0f5-158">CommonParameters</span></span>
<span data-ttu-id="bd0f5-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd0f5-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd0f5-161">輸入</span><span class="sxs-lookup"><span data-stu-id="bd0f5-161">INPUTS</span></span>

## <span data-ttu-id="bd0f5-162">輸出</span><span class="sxs-lookup"><span data-stu-id="bd0f5-162">OUTPUTS</span></span>

### <span data-ttu-id="bd0f5-163">SharedAccessAuthorizationRuleAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="bd0f5-163">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="bd0f5-164">筆記</span><span class="sxs-lookup"><span data-stu-id="bd0f5-164">NOTES</span></span>

## <span data-ttu-id="bd0f5-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd0f5-165">RELATED LINKS</span></span>

[<span data-ttu-id="bd0f5-166">AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="bd0f5-166">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="bd0f5-167">新-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="bd0f5-167">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="bd0f5-168">移除-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="bd0f5-168">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

