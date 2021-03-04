---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 49a856ef38d529c7d60b7c09b4d4a4fcdab5b59b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901734"
---
# <span data-ttu-id="8160e-101">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8160e-101">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="8160e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8160e-102">SYNOPSIS</span></span>
<span data-ttu-id="8160e-103">建立授權規則，並將該規則指派給通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="8160e-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

## <span data-ttu-id="8160e-104">語法</span><span class="sxs-lookup"><span data-stu-id="8160e-104">SYNTAX</span></span>

### <span data-ttu-id="8160e-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="8160e-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8160e-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="8160e-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8160e-107">描述</span><span class="sxs-lookup"><span data-stu-id="8160e-107">DESCRIPTION</span></span>
<span data-ttu-id="8160e-108">**New-AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 會建立共用存取簽章 (SAS) 授權規則，並將它指派給通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="8160e-108">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="8160e-109">授權規則會管理命名空間及該命名空間中包含的通知中樞的使用者許可權。</span><span class="sxs-lookup"><span data-stu-id="8160e-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="8160e-110">此 Cmdlet 提供兩種方式來建立新授權規則，並將它指派給命名空間。</span><span class="sxs-lookup"><span data-stu-id="8160e-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="8160e-111">您可以建立 **SharedAccessAuthorizationRuleAttributes** 物件的實例，然後將該物件設定為您想要新規則擁有的屬性值。</span><span class="sxs-lookup"><span data-stu-id="8160e-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="8160e-112">這可以使用 .NET Framework 完成。</span><span class="sxs-lookup"><span data-stu-id="8160e-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="8160e-113">接著，您可以使用 *SASRule* 參數，將那些屬性值複製到新規則。</span><span class="sxs-lookup"><span data-stu-id="8160e-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="8160e-114">或者，您可以建立 JSON (JavaScript 物件標記法) 包含相關組設定值的檔案，然後使用 *InputFile* 參數來使用這些值。</span><span class="sxs-lookup"><span data-stu-id="8160e-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="8160e-115">JSON 檔案是使用類似下列語法的文字檔： {</span><span class="sxs-lookup"><span data-stu-id="8160e-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="8160e-116">"Name"： "ContosoAuthorizationRule"，</span><span class="sxs-lookup"><span data-stu-id="8160e-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="8160e-117">"PrimaryKey"："WE4qH0398AyXjlekt56gg1g VM3NHoMs29KkUnnpUk01Y="，</span><span class="sxs-lookup"><span data-stu-id="8160e-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="8160e-118">"Rights"： \[</span><span class="sxs-lookup"><span data-stu-id="8160e-118">"Rights": \[</span></span>  
        <span data-ttu-id="8160e-119">「聆聽」，</span><span class="sxs-lookup"><span data-stu-id="8160e-119">"Listen",</span></span>  
        <span data-ttu-id="8160e-120">「傳送」</span><span class="sxs-lookup"><span data-stu-id="8160e-120">"Send"</span></span>  
    \]  
<span data-ttu-id="8160e-121">} 與 **New-AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 一起使用時，上述 JSON 範例會建立一個名為 ContosoAuthorizationRule 的授權規則，提供使用者對命名空間的聆聽和傳送許可權。</span><span class="sxs-lookup"><span data-stu-id="8160e-121">} When used in conjunction with the **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="8160e-122">用來 *驗證* 的主鍵，可以使用下列 Windows PowerShell 命令隨機產生： \[ 轉換 \] ：：ToBase64String ( (1.32 |% { \[ byte/] (Get-Random -Minimum 0 -最大值 255) }) ) </span><span class="sxs-lookup"><span data-stu-id="8160e-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="8160e-123">例子</span><span class="sxs-lookup"><span data-stu-id="8160e-123">EXAMPLES</span></span>

### <span data-ttu-id="8160e-124">範例 1：建立授權規則並指派給命名空間</span><span class="sxs-lookup"><span data-stu-id="8160e-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="8160e-125">此命令會建立授權規則，並將該規則指派給命名空間 ContosoNamespace。</span><span class="sxs-lookup"><span data-stu-id="8160e-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="8160e-126">建立此規則時，您必須指定適當的命名空間，以及命名空間指派給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8160e-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="8160e-127">不過，您不需要指定規則本身的任何相關資訊：規則資訊會取自輸入C:\Configuration\NamespaceAuthorizationRules.js中。</span><span class="sxs-lookup"><span data-stu-id="8160e-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="8160e-128">參數</span><span class="sxs-lookup"><span data-stu-id="8160e-128">PARAMETERS</span></span>

### <span data-ttu-id="8160e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8160e-129">-DefaultProfile</span></span>
<span data-ttu-id="8160e-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8160e-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8160e-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="8160e-131">-InputFile</span></span>
<span data-ttu-id="8160e-132">指定 JSON 檔案的路徑，其中包含新授權規則的組程資訊。</span><span class="sxs-lookup"><span data-stu-id="8160e-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

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

### <span data-ttu-id="8160e-133">-命名空間</span><span class="sxs-lookup"><span data-stu-id="8160e-133">-Namespace</span></span>
<span data-ttu-id="8160e-134">指定指派授權規則的命名空間。</span><span class="sxs-lookup"><span data-stu-id="8160e-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="8160e-135">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="8160e-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="8160e-136">新規則必須指派給現有的命名空間。</span><span class="sxs-lookup"><span data-stu-id="8160e-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="8160e-137">**New-AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 無法建立新命名空間。</span><span class="sxs-lookup"><span data-stu-id="8160e-137">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="8160e-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8160e-138">-ResourceGroup</span></span>
<span data-ttu-id="8160e-139">指定指派命名空間的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8160e-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="8160e-140">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="8160e-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="8160e-141">您必須使用現有的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8160e-141">You must use an existing resource group.</span></span>
<span data-ttu-id="8160e-142">此 Cmdlet 無法建立新資源群組。</span><span class="sxs-lookup"><span data-stu-id="8160e-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="8160e-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="8160e-143">-SASRule</span></span>
<span data-ttu-id="8160e-144">指定 **SharedAccessAuthorizationRuleAttributes** 物件，其中包含新規則的組定資訊。</span><span class="sxs-lookup"><span data-stu-id="8160e-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="8160e-145">-確認</span><span class="sxs-lookup"><span data-stu-id="8160e-145">-Confirm</span></span>
<span data-ttu-id="8160e-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8160e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8160e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8160e-147">-WhatIf</span></span>
<span data-ttu-id="8160e-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8160e-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8160e-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8160e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8160e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8160e-150">CommonParameters</span></span>
<span data-ttu-id="8160e-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8160e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8160e-152">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8160e-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8160e-153">輸入</span><span class="sxs-lookup"><span data-stu-id="8160e-153">INPUTS</span></span>

### <span data-ttu-id="8160e-154">System.String</span><span class="sxs-lookup"><span data-stu-id="8160e-154">System.String</span></span>

## <span data-ttu-id="8160e-155">輸出</span><span class="sxs-lookup"><span data-stu-id="8160e-155">OUTPUTS</span></span>

### <span data-ttu-id="8160e-156">Microsoft.Azure.Commands.NotificationHubs.models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8160e-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8160e-157">筆記</span><span class="sxs-lookup"><span data-stu-id="8160e-157">NOTES</span></span>

## <span data-ttu-id="8160e-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="8160e-158">RELATED LINKS</span></span>

[<span data-ttu-id="8160e-159">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8160e-159">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="8160e-160">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8160e-160">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="8160e-161">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8160e-161">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


