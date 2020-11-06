---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: a25e318aca1bca33c309a6f24b862e98c02659e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448071"
---
# <span data-ttu-id="f5a33-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f5a33-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="f5a33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5a33-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a33-103">設定通知中心命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="f5a33-103">Sets authorization rules for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5a33-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5a33-104">SYNTAX</span></span>

### <span data-ttu-id="f5a33-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5a33-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5a33-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5a33-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5a33-107">說明</span><span class="sxs-lookup"><span data-stu-id="f5a33-107">DESCRIPTION</span></span>
<span data-ttu-id="f5a33-108">**AzureRmNotificationHubsNamespaceAuthorizationRules** Cmdlet 會修改指派給通知中心命名空間之 (SAS) 授權規則的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="f5a33-108">The **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="f5a33-109">授權規則會管理使用者權利，以及該命名空間中所包含的通知中心。</span><span class="sxs-lookup"><span data-stu-id="f5a33-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>

<span data-ttu-id="f5a33-110">這個 Cmdlet 提供兩種方式來修改指派給命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="f5a33-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="f5a33-111">若是一個，您可以建立 **SharedAccessAuthorizationRuleAttributes** 物件的實例，然後使用您希望規則擁有的屬性值來設定該物件。</span><span class="sxs-lookup"><span data-stu-id="f5a33-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="f5a33-112">您可以使用 .NET 架構來完成此作業。</span><span class="sxs-lookup"><span data-stu-id="f5a33-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="f5a33-113">然後，您可以透過 *SASRule* 參數將這些屬性值複製到規則。</span><span class="sxs-lookup"><span data-stu-id="f5a33-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>

<span data-ttu-id="f5a33-114">或者，您也可以建立 JSON (JavaScript 物件符號) 檔案，其中包含相關的配置值，然後透過 *InputFile* 參數套用這些值。</span><span class="sxs-lookup"><span data-stu-id="f5a33-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="f5a33-115">JSON 檔案是一個文字檔，該檔案使用類似以下的語法：</span><span class="sxs-lookup"><span data-stu-id="f5a33-115">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="f5a33-116">{</span><span class="sxs-lookup"><span data-stu-id="f5a33-116">{</span></span>  
    <span data-ttu-id="f5a33-117">"Name"： "ContosoAuthorizationRule"，</span><span class="sxs-lookup"><span data-stu-id="f5a33-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="f5a33-118">"PrimaryKey"： "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y ="，</span><span class="sxs-lookup"><span data-stu-id="f5a33-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="f5a33-119">"版權"： \[</span><span class="sxs-lookup"><span data-stu-id="f5a33-119">"Rights": \[</span></span>  
        <span data-ttu-id="f5a33-120">[聆聽]，</span><span class="sxs-lookup"><span data-stu-id="f5a33-120">"Listen",</span></span>  
        <span data-ttu-id="f5a33-121">收發</span><span class="sxs-lookup"><span data-stu-id="f5a33-121">"Send"</span></span>  
    \]  
<span data-ttu-id="f5a33-122">}</span><span class="sxs-lookup"><span data-stu-id="f5a33-122">}</span></span>

<span data-ttu-id="f5a33-123">與 **AzureRmNotificationHubsNamespaceAuthorizationRules** Cmdlet 搭配使用時，前面的 JSON 範例會修改名為 ContosoAuthorizationRule 的授權規則，讓使用者聆聽並傳送該命名空間的許可權。</span><span class="sxs-lookup"><span data-stu-id="f5a33-123">When used in conjunction with the **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="f5a33-124">示例</span><span class="sxs-lookup"><span data-stu-id="f5a33-124">EXAMPLES</span></span>

### <span data-ttu-id="f5a33-125">範例1：修改指派給命名空間的授權規則</span><span class="sxs-lookup"><span data-stu-id="f5a33-125">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="f5a33-126">這個命令會修改指派給名為 ContosoNamespace 的命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="f5a33-126">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="f5a33-127">您必須指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="f5a33-127">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="f5a33-128">有關授權規則的資訊不會包含在命令本身中。</span><span class="sxs-lookup"><span data-stu-id="f5a33-128">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="f5a33-129">相反地，這些資訊是從 C:\Configuration\AuthorizationRules.js的輸入檔案中取得。</span><span class="sxs-lookup"><span data-stu-id="f5a33-129">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="f5a33-130">參數</span><span class="sxs-lookup"><span data-stu-id="f5a33-130">PARAMETERS</span></span>

### <span data-ttu-id="f5a33-131">-Force</span><span class="sxs-lookup"><span data-stu-id="f5a33-131">-Force</span></span>
<span data-ttu-id="f5a33-132">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="f5a33-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f5a33-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="f5a33-133">-InputFile</span></span>
<span data-ttu-id="f5a33-134">指定包含新規則之配置資訊的 JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="f5a33-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="f5a33-135">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f5a33-135">-Namespace</span></span>
<span data-ttu-id="f5a33-136">指定包含此 Cmdlet 所修改之授權規則的命名空間。</span><span class="sxs-lookup"><span data-stu-id="f5a33-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="f5a33-137">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="f5a33-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f5a33-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5a33-138">-ResourceGroup</span></span>
<span data-ttu-id="f5a33-139">指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="f5a33-139">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="f5a33-140">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="f5a33-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f5a33-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="f5a33-141">-SASRule</span></span>
<span data-ttu-id="f5a33-142">指定包含此 Cmdlet 所修改之授權規則之設定資訊的 **SharedAccessAuthorizationRuleAttributes** 物件。</span><span class="sxs-lookup"><span data-stu-id="f5a33-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f5a33-143">-確認</span><span class="sxs-lookup"><span data-stu-id="f5a33-143">-Confirm</span></span>
<span data-ttu-id="f5a33-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f5a33-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5a33-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5a33-145">-WhatIf</span></span>
<span data-ttu-id="f5a33-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5a33-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5a33-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5a33-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5a33-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a33-148">-DefaultProfile</span></span>
<span data-ttu-id="f5a33-149">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5a33-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5a33-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a33-150">CommonParameters</span></span>
<span data-ttu-id="f5a33-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5a33-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a33-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5a33-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a33-153">輸入</span><span class="sxs-lookup"><span data-stu-id="f5a33-153">INPUTS</span></span>

## <span data-ttu-id="f5a33-154">輸出</span><span class="sxs-lookup"><span data-stu-id="f5a33-154">OUTPUTS</span></span>

### <span data-ttu-id="f5a33-155">SharedAccessAuthorizationRuleAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="f5a33-155">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f5a33-156">筆記</span><span class="sxs-lookup"><span data-stu-id="f5a33-156">NOTES</span></span>

## <span data-ttu-id="f5a33-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5a33-157">RELATED LINKS</span></span>

[<span data-ttu-id="f5a33-158">AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f5a33-158">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="f5a33-159">新-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f5a33-159">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="f5a33-160">移除-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f5a33-160">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


