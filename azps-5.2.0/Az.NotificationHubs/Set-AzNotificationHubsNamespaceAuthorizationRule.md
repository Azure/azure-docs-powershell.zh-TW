---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 34f63dfc89f2bb1b3b9601e8ff51b280fee9ee42
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277267"
---
# <span data-ttu-id="93ede-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="93ede-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="93ede-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93ede-102">SYNOPSIS</span></span>
<span data-ttu-id="93ede-103">設定通知中心命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="93ede-103">Sets authorization rules for a notification hub namespace.</span></span>

## <span data-ttu-id="93ede-104">句法</span><span class="sxs-lookup"><span data-stu-id="93ede-104">SYNTAX</span></span>

### <span data-ttu-id="93ede-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="93ede-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93ede-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="93ede-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93ede-107">說明</span><span class="sxs-lookup"><span data-stu-id="93ede-107">DESCRIPTION</span></span>
<span data-ttu-id="93ede-108">**AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 會修改指派給通知中心命名空間之 (SAS) 授權規則的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="93ede-108">The **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="93ede-109">授權規則會管理使用者權利，以及該命名空間中所包含的通知中心。</span><span class="sxs-lookup"><span data-stu-id="93ede-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="93ede-110">這個 Cmdlet 提供兩種方式來修改指派給命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="93ede-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="93ede-111">若是一個，您可以建立 **SharedAccessAuthorizationRuleAttributes** 物件的實例，然後使用您希望規則擁有的屬性值來設定該物件。</span><span class="sxs-lookup"><span data-stu-id="93ede-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="93ede-112">您可以使用 .NET 架構來完成此作業。</span><span class="sxs-lookup"><span data-stu-id="93ede-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="93ede-113">然後，您可以透過 *SASRule* 參數將這些屬性值複製到規則。</span><span class="sxs-lookup"><span data-stu-id="93ede-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="93ede-114">或者，您也可以建立 JSON (JavaScript 物件符號) 檔案，其中包含相關的配置值，然後透過 *InputFile* 參數套用這些值。</span><span class="sxs-lookup"><span data-stu-id="93ede-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="93ede-115">JSON 檔案是使用類似以下語法的文字檔： {</span><span class="sxs-lookup"><span data-stu-id="93ede-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="93ede-116">"Name"： "ContosoAuthorizationRule"，</span><span class="sxs-lookup"><span data-stu-id="93ede-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="93ede-117">"PrimaryKey"： "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y ="，</span><span class="sxs-lookup"><span data-stu-id="93ede-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="93ede-118">"版權"： \[</span><span class="sxs-lookup"><span data-stu-id="93ede-118">"Rights": \[</span></span>  
        <span data-ttu-id="93ede-119">[聆聽]，</span><span class="sxs-lookup"><span data-stu-id="93ede-119">"Listen",</span></span>  
        <span data-ttu-id="93ede-120">收發</span><span class="sxs-lookup"><span data-stu-id="93ede-120">"Send"</span></span>  
    \]  
<span data-ttu-id="93ede-121">} 與 **AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 搭配使用時，前面的 JSON 範例會修改名為 ContosoAuthorizationRule 的授權規則，讓使用者聆聽並傳送該命名空間的許可權。</span><span class="sxs-lookup"><span data-stu-id="93ede-121">} When used in conjunction with the **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="93ede-122">示例</span><span class="sxs-lookup"><span data-stu-id="93ede-122">EXAMPLES</span></span>

### <span data-ttu-id="93ede-123">範例1：修改指派給命名空間的授權規則</span><span class="sxs-lookup"><span data-stu-id="93ede-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="93ede-124">這個命令會修改指派給名為 ContosoNamespace 的命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="93ede-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="93ede-125">您必須指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="93ede-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="93ede-126">有關授權規則的資訊不會包含在命令本身中。</span><span class="sxs-lookup"><span data-stu-id="93ede-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="93ede-127">相反地，這些資訊是從 C:\Configuration\AuthorizationRules.js的輸入檔案中取得。</span><span class="sxs-lookup"><span data-stu-id="93ede-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="93ede-128">參數</span><span class="sxs-lookup"><span data-stu-id="93ede-128">PARAMETERS</span></span>

### <span data-ttu-id="93ede-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ede-129">-DefaultProfile</span></span>
<span data-ttu-id="93ede-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="93ede-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93ede-131">-Force</span><span class="sxs-lookup"><span data-stu-id="93ede-131">-Force</span></span>
<span data-ttu-id="93ede-132">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="93ede-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="93ede-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="93ede-133">-InputFile</span></span>
<span data-ttu-id="93ede-134">指定包含新規則之配置資訊的 JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="93ede-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93ede-135">-命名空間</span><span class="sxs-lookup"><span data-stu-id="93ede-135">-Namespace</span></span>
<span data-ttu-id="93ede-136">指定包含此 Cmdlet 所修改之授權規則的命名空間。</span><span class="sxs-lookup"><span data-stu-id="93ede-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="93ede-137">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="93ede-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="93ede-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93ede-138">-ResourceGroup</span></span>
<span data-ttu-id="93ede-139">指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="93ede-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="93ede-140">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="93ede-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="93ede-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="93ede-141">-SASRule</span></span>
<span data-ttu-id="93ede-142">指定包含此 Cmdlet 所修改之授權規則之設定資訊的 **SharedAccessAuthorizationRuleAttributes** 物件。</span><span class="sxs-lookup"><span data-stu-id="93ede-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93ede-143">-確認</span><span class="sxs-lookup"><span data-stu-id="93ede-143">-Confirm</span></span>
<span data-ttu-id="93ede-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="93ede-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93ede-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93ede-145">-WhatIf</span></span>
<span data-ttu-id="93ede-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93ede-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93ede-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93ede-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93ede-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ede-148">CommonParameters</span></span>
<span data-ttu-id="93ede-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93ede-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ede-150">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="93ede-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ede-151">輸入</span><span class="sxs-lookup"><span data-stu-id="93ede-151">INPUTS</span></span>

### <span data-ttu-id="93ede-152">System.object</span><span class="sxs-lookup"><span data-stu-id="93ede-152">System.String</span></span>

## <span data-ttu-id="93ede-153">輸出</span><span class="sxs-lookup"><span data-stu-id="93ede-153">OUTPUTS</span></span>

### <span data-ttu-id="93ede-154">SharedAccessAuthorizationRuleAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="93ede-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="93ede-155">筆記</span><span class="sxs-lookup"><span data-stu-id="93ede-155">NOTES</span></span>

## <span data-ttu-id="93ede-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="93ede-156">RELATED LINKS</span></span>

[<span data-ttu-id="93ede-157">AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="93ede-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="93ede-158">新-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="93ede-158">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="93ede-159">移除-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="93ede-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


