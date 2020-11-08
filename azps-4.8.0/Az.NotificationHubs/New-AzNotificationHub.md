---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 3fb98dc1ef4b13b87fc7cfa41e165d9bc24fc17c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136201"
---
# <span data-ttu-id="91c4a-101">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="91c4a-101">New-AzNotificationHub</span></span>

## <span data-ttu-id="91c4a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="91c4a-103">建立通知中樞。</span><span class="sxs-lookup"><span data-stu-id="91c4a-103">Creates a notification hub.</span></span>

## <span data-ttu-id="91c4a-104">句法</span><span class="sxs-lookup"><span data-stu-id="91c4a-104">SYNTAX</span></span>

### <span data-ttu-id="91c4a-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="91c4a-105">InputFileParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91c4a-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="91c4a-106">NotificationHubParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91c4a-107">說明</span><span class="sxs-lookup"><span data-stu-id="91c4a-107">DESCRIPTION</span></span>
<span data-ttu-id="91c4a-108">**新的-AzNotificationHub** Cmdlet 會建立通知中樞。</span><span class="sxs-lookup"><span data-stu-id="91c4a-108">The **New-AzNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="91c4a-109">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="91c4a-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="91c4a-110">通知中樞大致相當於個別的應用程式：您的每個應用程式通常都有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="91c4a-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="91c4a-111">**新的 AzNotificationHub** Cmdlet 提供兩種方式來建立新的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="91c4a-111">The **New-AzNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="91c4a-112">您可以建立 **NotificationHubAttributes** 物件的實例，然後設定該物件。</span><span class="sxs-lookup"><span data-stu-id="91c4a-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="91c4a-113">然後，您可以透過 *NotificationHubObj* 參數，將這些屬性值複製到新的中樞。</span><span class="sxs-lookup"><span data-stu-id="91c4a-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="91c4a-114">或者，您也可以建立 JSON (JavaScript 物件符號) 檔案，其中包含相關的配置值，然後使用 *InputFile* 參數套用這些值。</span><span class="sxs-lookup"><span data-stu-id="91c4a-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="91c4a-115">當與 **AzNotificationHub** Cmdlet 搭配使用時，前面的 JSON 範例會建立名為 ContosoNotificationHub 的通知中心，該中樞位於美國西部資料中心。</span><span class="sxs-lookup"><span data-stu-id="91c4a-115">When used in conjunction with the **New-AzNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="91c4a-116">示例</span><span class="sxs-lookup"><span data-stu-id="91c4a-116">EXAMPLES</span></span>

### <span data-ttu-id="91c4a-117">範例1：建立通知中樞</span><span class="sxs-lookup"><span data-stu-id="91c4a-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="91c4a-118">這個命令會在命名空間 ContosoNamespace 中建立通知中樞。</span><span class="sxs-lookup"><span data-stu-id="91c4a-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="91c4a-119">新的中樞會指派給 ContosoNotificationsGroup。</span><span class="sxs-lookup"><span data-stu-id="91c4a-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="91c4a-120">您不需要為中樞指定名稱或任何其他配置資訊;該資訊將會從 C:\Configurations\InternalHub.js的輸入檔案中取得。</span><span class="sxs-lookup"><span data-stu-id="91c4a-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="91c4a-121">參數</span><span class="sxs-lookup"><span data-stu-id="91c4a-121">PARAMETERS</span></span>

### <span data-ttu-id="91c4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c4a-122">-DefaultProfile</span></span>
<span data-ttu-id="91c4a-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="91c4a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91c4a-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="91c4a-124">-InputFile</span></span>
<span data-ttu-id="91c4a-125">指定 JSON 檔案的路徑，該檔案包含新通知中樞的配置值。</span><span class="sxs-lookup"><span data-stu-id="91c4a-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="91c4a-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="91c4a-126">-Namespace</span></span>
<span data-ttu-id="91c4a-127">指定要將通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="91c4a-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="91c4a-128">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="91c4a-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="91c4a-129">通知中樞必須指派給現有的命名空間。</span><span class="sxs-lookup"><span data-stu-id="91c4a-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="91c4a-130">**新的-AzNotificationHub** Cmdlet 無法建立新的命名空間。</span><span class="sxs-lookup"><span data-stu-id="91c4a-130">The **New-AzNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="91c4a-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="91c4a-131">-NotificationHubObj</span></span>
<span data-ttu-id="91c4a-132">指定包含新中樞之配置資訊的 **NotificationHubAttributes** 物件。</span><span class="sxs-lookup"><span data-stu-id="91c4a-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="91c4a-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="91c4a-133">-ResourceGroup</span></span>
<span data-ttu-id="91c4a-134">指定要將通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="91c4a-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="91c4a-135">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="91c4a-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="91c4a-136">您必須使用現有的資源群組。</span><span class="sxs-lookup"><span data-stu-id="91c4a-136">You must use an existing resource group.</span></span>
<span data-ttu-id="91c4a-137">**新的-AzNotificationHub** Cmdlet 無法建立新的資源群組。</span><span class="sxs-lookup"><span data-stu-id="91c4a-137">The **New-AzNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="91c4a-138">-確認</span><span class="sxs-lookup"><span data-stu-id="91c4a-138">-Confirm</span></span>
<span data-ttu-id="91c4a-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="91c4a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91c4a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91c4a-140">-WhatIf</span></span>
<span data-ttu-id="91c4a-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="91c4a-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91c4a-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91c4a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91c4a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c4a-143">CommonParameters</span></span>
<span data-ttu-id="91c4a-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91c4a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c4a-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91c4a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c4a-146">輸入</span><span class="sxs-lookup"><span data-stu-id="91c4a-146">INPUTS</span></span>

### <span data-ttu-id="91c4a-147">System.object</span><span class="sxs-lookup"><span data-stu-id="91c4a-147">System.String</span></span>

## <span data-ttu-id="91c4a-148">輸出</span><span class="sxs-lookup"><span data-stu-id="91c4a-148">OUTPUTS</span></span>

### <span data-ttu-id="91c4a-149">NotificationHubAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="91c4a-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="91c4a-150">筆記</span><span class="sxs-lookup"><span data-stu-id="91c4a-150">NOTES</span></span>

## <span data-ttu-id="91c4a-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="91c4a-151">RELATED LINKS</span></span>

[<span data-ttu-id="91c4a-152">AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="91c4a-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="91c4a-153">移除-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="91c4a-153">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="91c4a-154">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="91c4a-154">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


