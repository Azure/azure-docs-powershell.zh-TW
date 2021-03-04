---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 88ed662dc9938e6d4c9c3caa07ce733530dff6b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901745"
---
# <span data-ttu-id="e91d9-101">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e91d9-101">New-AzNotificationHub</span></span>

## <span data-ttu-id="e91d9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e91d9-102">SYNOPSIS</span></span>
<span data-ttu-id="e91d9-103">建立通知中樞。</span><span class="sxs-lookup"><span data-stu-id="e91d9-103">Creates a notification hub.</span></span>

## <span data-ttu-id="e91d9-104">語法</span><span class="sxs-lookup"><span data-stu-id="e91d9-104">SYNTAX</span></span>

### <span data-ttu-id="e91d9-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e91d9-105">InputFileParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e91d9-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="e91d9-106">NotificationHubParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e91d9-107">描述</span><span class="sxs-lookup"><span data-stu-id="e91d9-107">DESCRIPTION</span></span>
<span data-ttu-id="e91d9-108">**New-AzNotificationHub** Cmdlet 會建立通知中樞。</span><span class="sxs-lookup"><span data-stu-id="e91d9-108">The **New-AzNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="e91d9-109">通知中樞可用來傳送推入通知給多個用戶端，無論這些用戶端使用哪個平臺。</span><span class="sxs-lookup"><span data-stu-id="e91d9-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="e91d9-110">通知中樞大致相當於個別的應用程式：每一個 App 通常會有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="e91d9-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="e91d9-111">**New-AzNotificationHub** Cmdlet 提供兩種方式來建立新通知中樞。</span><span class="sxs-lookup"><span data-stu-id="e91d9-111">The **New-AzNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="e91d9-112">您可以建立 **NotificationHubAttributes** 物件的實例，然後設定該物件。</span><span class="sxs-lookup"><span data-stu-id="e91d9-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="e91d9-113">接著，您可以透過 *NotificationHubObj* 參數，將那些屬性值複製到新的中樞。</span><span class="sxs-lookup"><span data-stu-id="e91d9-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="e91d9-114">或者，您可以建立 JSON (JavaScript 物件標記法) 包含相關組設定值的檔案，然後使用 *InputFile* 參數來使用這些值。</span><span class="sxs-lookup"><span data-stu-id="e91d9-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="e91d9-115">與 **New-AzNotificationHub** Cmdlet 一起使用時，上述 JSON 範例會建立一個名為 ContosoNotificationHub 的通知中樞，位於美國西部資料中心。</span><span class="sxs-lookup"><span data-stu-id="e91d9-115">When used in conjunction with the **New-AzNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="e91d9-116">例子</span><span class="sxs-lookup"><span data-stu-id="e91d9-116">EXAMPLES</span></span>

### <span data-ttu-id="e91d9-117">範例 1：建立通知中樞</span><span class="sxs-lookup"><span data-stu-id="e91d9-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="e91d9-118">此命令在命名空間 ContosoNamespace 中建立通知中樞。</span><span class="sxs-lookup"><span data-stu-id="e91d9-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="e91d9-119">新的中樞會指派給 ContosoNotificationsGroup。</span><span class="sxs-lookup"><span data-stu-id="e91d9-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="e91d9-120">您不需要為中樞指定名稱或其他任何組組資訊;資訊會從您輸入的C:\Configurations\InternalHub.js取。</span><span class="sxs-lookup"><span data-stu-id="e91d9-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="e91d9-121">參數</span><span class="sxs-lookup"><span data-stu-id="e91d9-121">PARAMETERS</span></span>

### <span data-ttu-id="e91d9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e91d9-122">-DefaultProfile</span></span>
<span data-ttu-id="e91d9-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e91d9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e91d9-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="e91d9-124">-InputFile</span></span>
<span data-ttu-id="e91d9-125">指定 JSON 檔案的路徑，其中包含新通知中樞的組程值。</span><span class="sxs-lookup"><span data-stu-id="e91d9-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="e91d9-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e91d9-126">-Namespace</span></span>
<span data-ttu-id="e91d9-127">指定指派通知中樞的命名空間。</span><span class="sxs-lookup"><span data-stu-id="e91d9-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="e91d9-128">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="e91d9-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="e91d9-129">通知中樞必須指派給現有的命名空間。</span><span class="sxs-lookup"><span data-stu-id="e91d9-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="e91d9-130">**New-AzNotificationHub** Cmdlet 無法建立新命名空間。</span><span class="sxs-lookup"><span data-stu-id="e91d9-130">The **New-AzNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="e91d9-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="e91d9-131">-NotificationHubObj</span></span>
<span data-ttu-id="e91d9-132">指定包含新中樞之群組原則資訊的 **NotificationHubAttributes** 物件。</span><span class="sxs-lookup"><span data-stu-id="e91d9-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="e91d9-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e91d9-133">-ResourceGroup</span></span>
<span data-ttu-id="e91d9-134">指定將通知中樞指派給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e91d9-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="e91d9-135">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="e91d9-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="e91d9-136">您必須使用現有的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e91d9-136">You must use an existing resource group.</span></span>
<span data-ttu-id="e91d9-137">**New-AzNotificationHub** Cmdlet 無法建立新資源群組。</span><span class="sxs-lookup"><span data-stu-id="e91d9-137">The **New-AzNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="e91d9-138">-確認</span><span class="sxs-lookup"><span data-stu-id="e91d9-138">-Confirm</span></span>
<span data-ttu-id="e91d9-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e91d9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e91d9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e91d9-140">-WhatIf</span></span>
<span data-ttu-id="e91d9-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e91d9-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e91d9-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e91d9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e91d9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e91d9-143">CommonParameters</span></span>
<span data-ttu-id="e91d9-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e91d9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e91d9-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e91d9-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e91d9-146">輸入</span><span class="sxs-lookup"><span data-stu-id="e91d9-146">INPUTS</span></span>

### <span data-ttu-id="e91d9-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e91d9-147">System.String</span></span>

## <span data-ttu-id="e91d9-148">輸出</span><span class="sxs-lookup"><span data-stu-id="e91d9-148">OUTPUTS</span></span>

### <span data-ttu-id="e91d9-149">Microsoft.Azure.Commands.NotificationHubs.models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="e91d9-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="e91d9-150">筆記</span><span class="sxs-lookup"><span data-stu-id="e91d9-150">NOTES</span></span>

## <span data-ttu-id="e91d9-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="e91d9-151">RELATED LINKS</span></span>

[<span data-ttu-id="e91d9-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e91d9-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="e91d9-153">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e91d9-153">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="e91d9-154">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e91d9-154">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


