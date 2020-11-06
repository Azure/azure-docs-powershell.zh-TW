---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: 33dfd5a8c4bde0405351315543078558a5832aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446705"
---
# <span data-ttu-id="c2274-101">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c2274-101">New-AzureRmNotificationHub</span></span>

## <span data-ttu-id="c2274-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2274-102">SYNOPSIS</span></span>
<span data-ttu-id="c2274-103">建立通知中樞。</span><span class="sxs-lookup"><span data-stu-id="c2274-103">Creates a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2274-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2274-104">SYNTAX</span></span>

### <span data-ttu-id="c2274-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2274-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2274-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2274-106">NotificationHubParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2274-107">說明</span><span class="sxs-lookup"><span data-stu-id="c2274-107">DESCRIPTION</span></span>
<span data-ttu-id="c2274-108">**新的-AzureRmNotificationHub** Cmdlet 會建立通知中樞。</span><span class="sxs-lookup"><span data-stu-id="c2274-108">The **New-AzureRmNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="c2274-109">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="c2274-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="c2274-110">通知中樞大致相當於個別的應用程式：您的每個應用程式通常都有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="c2274-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="c2274-111">**新的 AzureRmNotificationHub** Cmdlet 提供兩種方式來建立新的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="c2274-111">The **New-AzureRmNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="c2274-112">您可以建立 **NotificationHubAttributes** 物件的實例，然後設定該物件。</span><span class="sxs-lookup"><span data-stu-id="c2274-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="c2274-113">然後，您可以透過 *NotificationHubObj* 參數，將這些屬性值複製到新的中樞。</span><span class="sxs-lookup"><span data-stu-id="c2274-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="c2274-114">或者，您也可以建立 JSON (JavaScript 物件符號) 檔案，其中包含相關的配置值，然後使用 *InputFile* 參數套用這些值。</span><span class="sxs-lookup"><span data-stu-id="c2274-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>

<span data-ttu-id="c2274-115">當與 **AzureRmNotificationHub** Cmdlet 搭配使用時，前面的 JSON 範例會建立名為 ContosoNotificationHub 的通知中心，該中樞位於美國西部資料中心。</span><span class="sxs-lookup"><span data-stu-id="c2274-115">When used in conjunction with the **New-AzureRmNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="c2274-116">示例</span><span class="sxs-lookup"><span data-stu-id="c2274-116">EXAMPLES</span></span>

### <span data-ttu-id="c2274-117">範例1：建立通知中樞</span><span class="sxs-lookup"><span data-stu-id="c2274-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="c2274-118">這個命令會在命名空間 ContosoNamespace 中建立通知中樞。</span><span class="sxs-lookup"><span data-stu-id="c2274-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="c2274-119">新的中樞會指派給 ContosoNotificationsGroup。</span><span class="sxs-lookup"><span data-stu-id="c2274-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="c2274-120">您不需要為中樞指定名稱或任何其他配置資訊;該資訊將會從 C:\Configurations\InternalHub.js的輸入檔案中取得。</span><span class="sxs-lookup"><span data-stu-id="c2274-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="c2274-121">參數</span><span class="sxs-lookup"><span data-stu-id="c2274-121">PARAMETERS</span></span>

### <span data-ttu-id="c2274-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="c2274-122">-InputFile</span></span>
<span data-ttu-id="c2274-123">指定 JSON 檔案的路徑，該檔案包含新通知中樞的配置值。</span><span class="sxs-lookup"><span data-stu-id="c2274-123">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="c2274-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="c2274-124">-Namespace</span></span>
<span data-ttu-id="c2274-125">指定要將通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="c2274-125">Specifies the namespace to which the notification hub will be assigned.</span></span>

<span data-ttu-id="c2274-126">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="c2274-126">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="c2274-127">通知中樞必須指派給現有的命名空間。</span><span class="sxs-lookup"><span data-stu-id="c2274-127">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="c2274-128">**新的-AzureRmNotificationHub** Cmdlet 無法建立新的命名空間。</span><span class="sxs-lookup"><span data-stu-id="c2274-128">The **New-AzureRmNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="c2274-129">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="c2274-129">-NotificationHubObj</span></span>
<span data-ttu-id="c2274-130">指定包含新中樞之配置資訊的 **NotificationHubAttributes** 物件。</span><span class="sxs-lookup"><span data-stu-id="c2274-130">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="c2274-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c2274-131">-ResourceGroup</span></span>
<span data-ttu-id="c2274-132">指定要將通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="c2274-132">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="c2274-133">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="c2274-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="c2274-134">您必須使用現有的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c2274-134">You must use an existing resource group.</span></span>
<span data-ttu-id="c2274-135">**新的-AzureRmNotificationHub** Cmdlet 無法建立新的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c2274-135">The **New-AzureRmNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="c2274-136">-確認</span><span class="sxs-lookup"><span data-stu-id="c2274-136">-Confirm</span></span>
<span data-ttu-id="c2274-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2274-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2274-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2274-138">-WhatIf</span></span>
<span data-ttu-id="c2274-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2274-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2274-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2274-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2274-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2274-141">-DefaultProfile</span></span>
<span data-ttu-id="c2274-142">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2274-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2274-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2274-143">CommonParameters</span></span>
<span data-ttu-id="c2274-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2274-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2274-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2274-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2274-146">輸入</span><span class="sxs-lookup"><span data-stu-id="c2274-146">INPUTS</span></span>

## <span data-ttu-id="c2274-147">輸出</span><span class="sxs-lookup"><span data-stu-id="c2274-147">OUTPUTS</span></span>

### <span data-ttu-id="c2274-148">NotificationHubAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="c2274-148">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="c2274-149">筆記</span><span class="sxs-lookup"><span data-stu-id="c2274-149">NOTES</span></span>

## <span data-ttu-id="c2274-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2274-150">RELATED LINKS</span></span>

[<span data-ttu-id="c2274-151">AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c2274-151">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="c2274-152">移除-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c2274-152">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="c2274-153">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c2274-153">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


