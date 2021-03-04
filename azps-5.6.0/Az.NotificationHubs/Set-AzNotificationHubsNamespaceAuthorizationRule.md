---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 2f5ff44e6d96900afe36b9ade8360fb0a69ec726
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901697"
---
# <span data-ttu-id="e57fd-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e57fd-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="e57fd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e57fd-102">SYNOPSIS</span></span>
<span data-ttu-id="e57fd-103">設定通知中樞命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="e57fd-103">Sets authorization rules for a notification hub namespace.</span></span>

## <span data-ttu-id="e57fd-104">語法</span><span class="sxs-lookup"><span data-stu-id="e57fd-104">SYNTAX</span></span>

### <span data-ttu-id="e57fd-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e57fd-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e57fd-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="e57fd-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e57fd-107">描述</span><span class="sxs-lookup"><span data-stu-id="e57fd-107">DESCRIPTION</span></span>
<span data-ttu-id="e57fd-108">**Set-AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 會修改指派給通知中樞命名空間的共用存取簽章 (SAS) 授權規則。</span><span class="sxs-lookup"><span data-stu-id="e57fd-108">The **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="e57fd-109">授權規則會管理命名空間及該命名空間中包含的通知中樞的使用者許可權。</span><span class="sxs-lookup"><span data-stu-id="e57fd-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="e57fd-110">此 Cmdlet 提供兩種方式來修改指派給命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="e57fd-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="e57fd-111">例如，您可以建立 **SharedAccessAuthorizationRuleAttributes** 物件的實例，然後將該物件設定為您想要規則擁有的屬性值。</span><span class="sxs-lookup"><span data-stu-id="e57fd-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="e57fd-112">您可以使用 .NET Framework 來完成此工作。</span><span class="sxs-lookup"><span data-stu-id="e57fd-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="e57fd-113">接著，您可以透過 *SASRule* 參數，將那些屬性值複製到規則。</span><span class="sxs-lookup"><span data-stu-id="e57fd-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="e57fd-114">或者，您可以建立 JSON (JavaScript 物件表示) 包含相關組設定值的檔案，然後透過 *InputFile* 參數來使用這些值。</span><span class="sxs-lookup"><span data-stu-id="e57fd-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="e57fd-115">JSON 檔案是使用類似以下語法的文字檔： {</span><span class="sxs-lookup"><span data-stu-id="e57fd-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="e57fd-116">"Name"： "ContosoAuthorizationRule"，</span><span class="sxs-lookup"><span data-stu-id="e57fd-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="e57fd-117">"PrimaryKey"："WE4qH0398AyXjlekt56gg1g VM3NHoMs29KkUnnpUk01Y="，</span><span class="sxs-lookup"><span data-stu-id="e57fd-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="e57fd-118">"Rights"： \[</span><span class="sxs-lookup"><span data-stu-id="e57fd-118">"Rights": \[</span></span>  
        <span data-ttu-id="e57fd-119">「聆聽」，</span><span class="sxs-lookup"><span data-stu-id="e57fd-119">"Listen",</span></span>  
        <span data-ttu-id="e57fd-120">「傳送」</span><span class="sxs-lookup"><span data-stu-id="e57fd-120">"Send"</span></span>  
    \]  
<span data-ttu-id="e57fd-121">} 與 **Set-AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 一起使用時，上一個 JSON 範例會修改名為 ContosoAuthorizationRule 的授權規則，為使用者提供命名空間的聆聽和傳送許可權。</span><span class="sxs-lookup"><span data-stu-id="e57fd-121">} When used in conjunction with the **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="e57fd-122">例子</span><span class="sxs-lookup"><span data-stu-id="e57fd-122">EXAMPLES</span></span>

### <span data-ttu-id="e57fd-123">範例 1：修改指派給命名空間的授權規則</span><span class="sxs-lookup"><span data-stu-id="e57fd-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="e57fd-124">此命令會修改指派給名稱為 ContosoNamespace 之命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="e57fd-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="e57fd-125">您必須指定指派命名空間的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e57fd-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="e57fd-126">命令本身不會包含授權規則相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e57fd-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="e57fd-127">該資訊會改為從輸入檔案中取得，C:\Configuration\AuthorizationRules.js上。</span><span class="sxs-lookup"><span data-stu-id="e57fd-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="e57fd-128">參數</span><span class="sxs-lookup"><span data-stu-id="e57fd-128">PARAMETERS</span></span>

### <span data-ttu-id="e57fd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e57fd-129">-DefaultProfile</span></span>
<span data-ttu-id="e57fd-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e57fd-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e57fd-131">-強制</span><span class="sxs-lookup"><span data-stu-id="e57fd-131">-Force</span></span>
<span data-ttu-id="e57fd-132">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="e57fd-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e57fd-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="e57fd-133">-InputFile</span></span>
<span data-ttu-id="e57fd-134">指定 JSON 檔案的路徑，其中包含新規則的組程資訊。</span><span class="sxs-lookup"><span data-stu-id="e57fd-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="e57fd-135">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e57fd-135">-Namespace</span></span>
<span data-ttu-id="e57fd-136">指定包含此 Cmdlet 修改之授權規則的命名空間。</span><span class="sxs-lookup"><span data-stu-id="e57fd-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="e57fd-137">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="e57fd-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="e57fd-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e57fd-138">-ResourceGroup</span></span>
<span data-ttu-id="e57fd-139">指定指派命名空間的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e57fd-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="e57fd-140">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="e57fd-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="e57fd-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="e57fd-141">-SASRule</span></span>
<span data-ttu-id="e57fd-142">指定 **SharedAccessAuthorizationRuleAttributes** 物件，該物件包含此 Cmdlet 修改之授權規則的組定資訊。</span><span class="sxs-lookup"><span data-stu-id="e57fd-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e57fd-143">-確認</span><span class="sxs-lookup"><span data-stu-id="e57fd-143">-Confirm</span></span>
<span data-ttu-id="e57fd-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e57fd-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e57fd-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e57fd-145">-WhatIf</span></span>
<span data-ttu-id="e57fd-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e57fd-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e57fd-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e57fd-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e57fd-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57fd-148">CommonParameters</span></span>
<span data-ttu-id="e57fd-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e57fd-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57fd-150">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e57fd-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57fd-151">輸入</span><span class="sxs-lookup"><span data-stu-id="e57fd-151">INPUTS</span></span>

### <span data-ttu-id="e57fd-152">System.String</span><span class="sxs-lookup"><span data-stu-id="e57fd-152">System.String</span></span>

## <span data-ttu-id="e57fd-153">輸出</span><span class="sxs-lookup"><span data-stu-id="e57fd-153">OUTPUTS</span></span>

### <span data-ttu-id="e57fd-154">Microsoft.Azure.Commands.NotificationHubs.models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e57fd-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e57fd-155">筆記</span><span class="sxs-lookup"><span data-stu-id="e57fd-155">NOTES</span></span>

## <span data-ttu-id="e57fd-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="e57fd-156">RELATED LINKS</span></span>

[<span data-ttu-id="e57fd-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e57fd-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="e57fd-158">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e57fd-158">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="e57fd-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e57fd-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


