---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 6a55a1b6b032bf2354d7d88699744f9cc5dbaea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448999"
---
# <span data-ttu-id="1c269-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="1c269-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="1c269-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c269-102">SYNOPSIS</span></span>
<span data-ttu-id="1c269-103">建立授權規則，並將該規則指派給通知中心命名空間。</span><span class="sxs-lookup"><span data-stu-id="1c269-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c269-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c269-104">SYNTAX</span></span>

### <span data-ttu-id="1c269-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c269-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c269-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c269-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c269-107">說明</span><span class="sxs-lookup"><span data-stu-id="1c269-107">DESCRIPTION</span></span>
<span data-ttu-id="1c269-108">**新的-AzureRmNotificationHubsNamespaceAuthorizationRules** Cmdlet 會 (SAS) 授權規則建立共用的存取簽章，並將它指派給通知中心命名空間。</span><span class="sxs-lookup"><span data-stu-id="1c269-108">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="1c269-109">授權規則會管理使用者權利，以及該命名空間所含的通知中心。</span><span class="sxs-lookup"><span data-stu-id="1c269-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="1c269-110">這個 Cmdlet 提供兩種方式來建立新的授權規則，並將它指派給命名空間。</span><span class="sxs-lookup"><span data-stu-id="1c269-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="1c269-111">您可以建立 **SharedAccessAuthorizationRuleAttributes** 物件的實例，然後使用您想要新規則擁有的屬性值來設定該物件。</span><span class="sxs-lookup"><span data-stu-id="1c269-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="1c269-112">這可以使用 .NET Framework 來完成。</span><span class="sxs-lookup"><span data-stu-id="1c269-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="1c269-113">然後，您可以使用 *SASRule* 參數，將這些屬性值複製到您的新規則。</span><span class="sxs-lookup"><span data-stu-id="1c269-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="1c269-114">或者，您也可以建立 JSON (JavaScript 物件符號) 檔案，其中包含相關的配置值，然後使用 *InputFile* 參數套用這些值。</span><span class="sxs-lookup"><span data-stu-id="1c269-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="1c269-115">JSON 檔案是一個文字檔，該檔案使用類似下列的語法： {</span><span class="sxs-lookup"><span data-stu-id="1c269-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="1c269-116">"Name"： "ContosoAuthorizationRule"，</span><span class="sxs-lookup"><span data-stu-id="1c269-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="1c269-117">"PrimaryKey"： "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y ="，</span><span class="sxs-lookup"><span data-stu-id="1c269-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="1c269-118">"版權"： \[</span><span class="sxs-lookup"><span data-stu-id="1c269-118">"Rights": \[</span></span>  
        <span data-ttu-id="1c269-119">[聆聽]，</span><span class="sxs-lookup"><span data-stu-id="1c269-119">"Listen",</span></span>  
        <span data-ttu-id="1c269-120">收發</span><span class="sxs-lookup"><span data-stu-id="1c269-120">"Send"</span></span>  
    \]  
<span data-ttu-id="1c269-121">} 與 **新的-AzureRmNotificationHubsNamespaceAuthorizationRules** Cmdlet 搭配使用時，前面的 JSON 範例會建立名為 ContosoAuthorizationRule 的授權規則，讓使用者聆聽並傳送該命名空間的許可權。</span><span class="sxs-lookup"><span data-stu-id="1c269-121">} When used in conjunction with the **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="1c269-122">使用下列 Windows PowerShell 命令時，可以隨機產生用於驗證的 *PrimaryKey* ： \[ Convert \] ：： ToBase64String ( # B1 1. 32 |% { \[ Byte/] (取得最小值-最小值 0-最高 255) } ) # A5</span><span class="sxs-lookup"><span data-stu-id="1c269-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="1c269-123">示例</span><span class="sxs-lookup"><span data-stu-id="1c269-123">EXAMPLES</span></span>

### <span data-ttu-id="1c269-124">範例1：建立授權規則並將它指派給命名空間</span><span class="sxs-lookup"><span data-stu-id="1c269-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="1c269-125">這個命令會建立授權規則，並將該規則指派給命名空間 ContosoNamespace。</span><span class="sxs-lookup"><span data-stu-id="1c269-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="1c269-126">建立此規則時，您必須指定適當的命名空間和命名空間所指派的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1c269-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="1c269-127">不過，您不需要指定規則本身的任何相關資訊：將會從輸入檔案中取得規則資訊 C:\Configuration\NamespaceAuthorizationRules.js[開啟]。</span><span class="sxs-lookup"><span data-stu-id="1c269-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="1c269-128">參數</span><span class="sxs-lookup"><span data-stu-id="1c269-128">PARAMETERS</span></span>

### <span data-ttu-id="1c269-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c269-129">-DefaultProfile</span></span>
<span data-ttu-id="1c269-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1c269-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c269-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="1c269-131">-InputFile</span></span>
<span data-ttu-id="1c269-132">指定包含新授權規則之配置資訊的 JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="1c269-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

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

### <span data-ttu-id="1c269-133">-命名空間</span><span class="sxs-lookup"><span data-stu-id="1c269-133">-Namespace</span></span>
<span data-ttu-id="1c269-134">指定將指派授權規則的命名空間。</span><span class="sxs-lookup"><span data-stu-id="1c269-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="1c269-135">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="1c269-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="1c269-136">新規則必須指派給現有的命名空間。</span><span class="sxs-lookup"><span data-stu-id="1c269-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="1c269-137">**新的-AzureRmNotificationHubsNamespaceAuthorizationRules** Cmdlet 無法建立新的命名空間。</span><span class="sxs-lookup"><span data-stu-id="1c269-137">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="1c269-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1c269-138">-ResourceGroup</span></span>
<span data-ttu-id="1c269-139">指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="1c269-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="1c269-140">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="1c269-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="1c269-141">您必須使用現有的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1c269-141">You must use an existing resource group.</span></span>
<span data-ttu-id="1c269-142">這個 Cmdlet 無法建立新的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1c269-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="1c269-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="1c269-143">-SASRule</span></span>
<span data-ttu-id="1c269-144">指定包含新規則之配置資訊的 **SharedAccessAuthorizationRuleAttributes** 物件。</span><span class="sxs-lookup"><span data-stu-id="1c269-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="1c269-145">-確認</span><span class="sxs-lookup"><span data-stu-id="1c269-145">-Confirm</span></span>
<span data-ttu-id="1c269-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1c269-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c269-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c269-147">-WhatIf</span></span>
<span data-ttu-id="1c269-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1c269-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c269-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1c269-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c269-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c269-150">CommonParameters</span></span>
<span data-ttu-id="1c269-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c269-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c269-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1c269-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c269-153">輸入</span><span class="sxs-lookup"><span data-stu-id="1c269-153">INPUTS</span></span>

### <span data-ttu-id="1c269-154">System.object</span><span class="sxs-lookup"><span data-stu-id="1c269-154">System.String</span></span>

## <span data-ttu-id="1c269-155">輸出</span><span class="sxs-lookup"><span data-stu-id="1c269-155">OUTPUTS</span></span>

### <span data-ttu-id="1c269-156">SharedAccessAuthorizationRuleAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="1c269-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="1c269-157">筆記</span><span class="sxs-lookup"><span data-stu-id="1c269-157">NOTES</span></span>

## <span data-ttu-id="1c269-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c269-158">RELATED LINKS</span></span>

[<span data-ttu-id="1c269-159">AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="1c269-159">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="1c269-160">移除-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="1c269-160">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="1c269-161">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="1c269-161">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


