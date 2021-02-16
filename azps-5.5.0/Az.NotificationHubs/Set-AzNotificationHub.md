---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7083c6872981cefaa12dc01612f3eb27cc7676ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142047"
---
# <span data-ttu-id="841a7-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="841a7-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="841a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="841a7-102">SYNOPSIS</span></span>
<span data-ttu-id="841a7-103">設定通知中樞的屬性值。</span><span class="sxs-lookup"><span data-stu-id="841a7-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="841a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="841a7-104">SYNTAX</span></span>

### <span data-ttu-id="841a7-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="841a7-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="841a7-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="841a7-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="841a7-107">說明</span><span class="sxs-lookup"><span data-stu-id="841a7-107">DESCRIPTION</span></span>
<span data-ttu-id="841a7-108">**AzNotificationHub** Cmdlet 會修改通知中樞的屬性值。</span><span class="sxs-lookup"><span data-stu-id="841a7-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="841a7-109">您可以透過兩種方式來修改通知中樞屬性值。</span><span class="sxs-lookup"><span data-stu-id="841a7-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="841a7-110">若是一個，您可以建立 **NotificationHubAttributes** 物件的實例，然後使用您想要新的中樞擁有的屬性值來設定該物件。</span><span class="sxs-lookup"><span data-stu-id="841a7-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="841a7-111">這可以透過 .NET 架構來完成。</span><span class="sxs-lookup"><span data-stu-id="841a7-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="841a7-112">然後，您可以透過 *NotificationHubObj* 參數，將這些屬性值複製到您的中樞。</span><span class="sxs-lookup"><span data-stu-id="841a7-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="841a7-113">或者，您也可以建立包含相關設定值) 檔案的 JSON (JavaScript 物件符號，然後透過 *InputFile* 參數套用這些值。</span><span class="sxs-lookup"><span data-stu-id="841a7-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="841a7-114">JSON 檔案是一個文字檔，該檔案使用類似下列的語法： {</span><span class="sxs-lookup"><span data-stu-id="841a7-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="841a7-115">"Name"： "ContosoNotificationHub"，</span><span class="sxs-lookup"><span data-stu-id="841a7-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="841a7-116">"位置"： "西 US"，</span><span class="sxs-lookup"><span data-stu-id="841a7-116">"Location": "West US",</span></span>  
<span data-ttu-id="841a7-117">} 與 **AzNotificationHub** Cmdlet 搭配使用時，前面的 JSON 範例會將名為 ContosoNotificationHub 之通知中樞的 Location 值設為 [西部]。</span><span class="sxs-lookup"><span data-stu-id="841a7-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="841a7-118">示例</span><span class="sxs-lookup"><span data-stu-id="841a7-118">EXAMPLES</span></span>

### <span data-ttu-id="841a7-119">範例1：修改通知中樞的屬性值</span><span class="sxs-lookup"><span data-stu-id="841a7-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="841a7-120">這個命令會修改在 ContosoNamespace 命名空間中找到之通知中心的屬性值，並將其指派給資源群組 ContosoNotificationsGroup。</span><span class="sxs-lookup"><span data-stu-id="841a7-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="841a7-121">在命令中不會指定屬性值，以及要修改之中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="841a7-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="841a7-122">相反地，該資訊會包含在 C:\Configuration\Hubs.js的輸入檔案中。</span><span class="sxs-lookup"><span data-stu-id="841a7-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="841a7-123">範例2</span><span class="sxs-lookup"><span data-stu-id="841a7-123">Example 2</span></span>

<span data-ttu-id="841a7-124">設定通知中樞的屬性值。</span><span class="sxs-lookup"><span data-stu-id="841a7-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="841a7-125"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="841a7-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="841a7-126">參數</span><span class="sxs-lookup"><span data-stu-id="841a7-126">PARAMETERS</span></span>

### <span data-ttu-id="841a7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="841a7-127">-DefaultProfile</span></span>
<span data-ttu-id="841a7-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="841a7-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="841a7-129">-Force</span><span class="sxs-lookup"><span data-stu-id="841a7-129">-Force</span></span>
<span data-ttu-id="841a7-130">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="841a7-130">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="841a7-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="841a7-131">-InputFile</span></span>
<span data-ttu-id="841a7-132">指定包含通知中樞配置資訊的 JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="841a7-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="841a7-133">-命名空間</span><span class="sxs-lookup"><span data-stu-id="841a7-133">-Namespace</span></span>
<span data-ttu-id="841a7-134">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="841a7-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="841a7-135">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="841a7-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="841a7-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="841a7-136">-NotificationHubObj</span></span>
<span data-ttu-id="841a7-137">指定包含此 Cmdlet 所修改之中樞之配置資訊的 **NotificationHubAttributes** 物件。</span><span class="sxs-lookup"><span data-stu-id="841a7-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="841a7-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="841a7-138">-ResourceGroup</span></span>
<span data-ttu-id="841a7-139">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="841a7-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="841a7-140">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="841a7-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="841a7-141">-確認</span><span class="sxs-lookup"><span data-stu-id="841a7-141">-Confirm</span></span>
<span data-ttu-id="841a7-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="841a7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="841a7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="841a7-143">-WhatIf</span></span>
<span data-ttu-id="841a7-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="841a7-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="841a7-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="841a7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="841a7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="841a7-146">CommonParameters</span></span>
<span data-ttu-id="841a7-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="841a7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="841a7-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="841a7-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="841a7-149">輸入</span><span class="sxs-lookup"><span data-stu-id="841a7-149">INPUTS</span></span>

### <span data-ttu-id="841a7-150">System.object</span><span class="sxs-lookup"><span data-stu-id="841a7-150">System.String</span></span>

## <span data-ttu-id="841a7-151">輸出</span><span class="sxs-lookup"><span data-stu-id="841a7-151">OUTPUTS</span></span>

### <span data-ttu-id="841a7-152">NotificationHubAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="841a7-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="841a7-153">筆記</span><span class="sxs-lookup"><span data-stu-id="841a7-153">NOTES</span></span>

## <span data-ttu-id="841a7-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="841a7-154">RELATED LINKS</span></span>

[<span data-ttu-id="841a7-155">AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="841a7-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="841a7-156">新-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="841a7-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="841a7-157">移除-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="841a7-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


