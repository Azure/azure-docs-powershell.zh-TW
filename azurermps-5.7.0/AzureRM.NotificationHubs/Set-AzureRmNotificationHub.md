---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
ms.openlocfilehash: e035cb24c6341eb6d5b3d8aba5cd86b67fdafca2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457083"
---
# <span data-ttu-id="159a9-101">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="159a9-101">Set-AzureRmNotificationHub</span></span>

## <span data-ttu-id="159a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="159a9-102">SYNOPSIS</span></span>
<span data-ttu-id="159a9-103">設定通知中樞的屬性值。</span><span class="sxs-lookup"><span data-stu-id="159a9-103">Sets property values for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="159a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="159a9-104">SYNTAX</span></span>

### <span data-ttu-id="159a9-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="159a9-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="159a9-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="159a9-106">NotificationHubParameterSet</span></span>
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="159a9-107">說明</span><span class="sxs-lookup"><span data-stu-id="159a9-107">DESCRIPTION</span></span>
<span data-ttu-id="159a9-108">**AzureRmNotificationHub** Cmdlet 會修改通知中樞的屬性值。</span><span class="sxs-lookup"><span data-stu-id="159a9-108">The **Set-AzureRmNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>

<span data-ttu-id="159a9-109">您可以透過兩種方式來修改通知中樞屬性值。</span><span class="sxs-lookup"><span data-stu-id="159a9-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="159a9-110">若是一個，您可以建立 **NotificationHubAttributes** 物件的實例，然後使用您想要新的中樞擁有的屬性值來設定該物件。</span><span class="sxs-lookup"><span data-stu-id="159a9-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="159a9-111">這可以透過 .NET 架構來完成。</span><span class="sxs-lookup"><span data-stu-id="159a9-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="159a9-112">然後，您可以透過 *NotificationHubObj* 參數，將這些屬性值複製到您的中樞。</span><span class="sxs-lookup"><span data-stu-id="159a9-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="159a9-113">或者，您也可以建立包含相關設定值) 檔案的 JSON (JavaScript 物件符號，然後透過 *InputFile* 參數套用這些值。</span><span class="sxs-lookup"><span data-stu-id="159a9-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="159a9-114">JSON 檔案是一個文字檔，該檔案使用類似下列的語法：</span><span class="sxs-lookup"><span data-stu-id="159a9-114">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="159a9-115">{</span><span class="sxs-lookup"><span data-stu-id="159a9-115">{</span></span>  
    <span data-ttu-id="159a9-116">"Name"： "ContosoNotificationHub"，</span><span class="sxs-lookup"><span data-stu-id="159a9-116">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="159a9-117">"位置"： "西 US"，</span><span class="sxs-lookup"><span data-stu-id="159a9-117">"Location": "West US",</span></span>  
<span data-ttu-id="159a9-118">}</span><span class="sxs-lookup"><span data-stu-id="159a9-118">}</span></span>

<span data-ttu-id="159a9-119">當與 **AzureRmNotificationHub** Cmdlet 搭配使用時，前面的 JSON 範例會將名為 ContosoNotificationHub 之通知中樞的 Location 值設為 [西部]。</span><span class="sxs-lookup"><span data-stu-id="159a9-119">When used in conjunction with the **Set-AzureRmNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="159a9-120">示例</span><span class="sxs-lookup"><span data-stu-id="159a9-120">EXAMPLES</span></span>

### <span data-ttu-id="159a9-121">範例1：修改通知中樞的屬性值</span><span class="sxs-lookup"><span data-stu-id="159a9-121">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="159a9-122">這個命令會修改在 ContosoNamespace 命名空間中找到之通知中心的屬性值，並將其指派給資源群組 ContosoNotificationsGroup。</span><span class="sxs-lookup"><span data-stu-id="159a9-122">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="159a9-123">在命令中不會指定屬性值，以及要修改之中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="159a9-123">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="159a9-124">相反地，該資訊會包含在 C:\Configuration\Hubs.js的輸入檔案中。</span><span class="sxs-lookup"><span data-stu-id="159a9-124">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="159a9-125">參數</span><span class="sxs-lookup"><span data-stu-id="159a9-125">PARAMETERS</span></span>

### <span data-ttu-id="159a9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="159a9-126">-DefaultProfile</span></span>
<span data-ttu-id="159a9-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="159a9-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159a9-128">-Force</span><span class="sxs-lookup"><span data-stu-id="159a9-128">-Force</span></span>
<span data-ttu-id="159a9-129">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="159a9-129">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159a9-130">-InputFile</span><span class="sxs-lookup"><span data-stu-id="159a9-130">-InputFile</span></span>
<span data-ttu-id="159a9-131">指定包含通知中樞配置資訊的 JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="159a9-131">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159a9-132">-命名空間</span><span class="sxs-lookup"><span data-stu-id="159a9-132">-Namespace</span></span>
<span data-ttu-id="159a9-133">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="159a9-133">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="159a9-134">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="159a9-134">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159a9-135">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="159a9-135">-NotificationHubObj</span></span>
<span data-ttu-id="159a9-136">指定包含此 Cmdlet 所修改之中樞之配置資訊的 **NotificationHubAttributes** 物件。</span><span class="sxs-lookup"><span data-stu-id="159a9-136">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159a9-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="159a9-137">-ResourceGroup</span></span>
<span data-ttu-id="159a9-138">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="159a9-138">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="159a9-139">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="159a9-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159a9-140">-確認</span><span class="sxs-lookup"><span data-stu-id="159a9-140">-Confirm</span></span>
<span data-ttu-id="159a9-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="159a9-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159a9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="159a9-142">-WhatIf</span></span>
<span data-ttu-id="159a9-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="159a9-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="159a9-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="159a9-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159a9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="159a9-145">CommonParameters</span></span>
<span data-ttu-id="159a9-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="159a9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="159a9-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="159a9-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="159a9-148">輸入</span><span class="sxs-lookup"><span data-stu-id="159a9-148">INPUTS</span></span>

### <span data-ttu-id="159a9-149">所有</span><span class="sxs-lookup"><span data-stu-id="159a9-149">None</span></span>
<span data-ttu-id="159a9-150">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="159a9-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="159a9-151">輸出</span><span class="sxs-lookup"><span data-stu-id="159a9-151">OUTPUTS</span></span>

### <span data-ttu-id="159a9-152">NotificationHubAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="159a9-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="159a9-153">筆記</span><span class="sxs-lookup"><span data-stu-id="159a9-153">NOTES</span></span>

## <span data-ttu-id="159a9-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="159a9-154">RELATED LINKS</span></span>

[<span data-ttu-id="159a9-155">AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="159a9-155">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="159a9-156">新-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="159a9-156">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="159a9-157">移除-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="159a9-157">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)


