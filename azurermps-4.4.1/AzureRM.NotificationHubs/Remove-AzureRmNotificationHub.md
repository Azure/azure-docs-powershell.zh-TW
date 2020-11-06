---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
ms.openlocfilehash: b0911045313b26b19fd1de70af926e8c8e066ca8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448085"
---
# <span data-ttu-id="6b3cd-101">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6b3cd-101">Remove-AzureRmNotificationHub</span></span>

## <span data-ttu-id="6b3cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6b3cd-102">SYNOPSIS</span></span>
<span data-ttu-id="6b3cd-103">移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-103">Removes an existing notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b3cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="6b3cd-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b3cd-105">說明</span><span class="sxs-lookup"><span data-stu-id="6b3cd-105">DESCRIPTION</span></span>
<span data-ttu-id="6b3cd-106">**AzureRmNotificationHub** Cmdlet 會移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-106">The **Remove-AzureRmNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="6b3cd-107">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="6b3cd-108">平臺包括但不限於： iOS、Android、Windows Phone 8 和 Windows 市集中。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="6b3cd-109">通知中樞大致相當於個別的應用程式：您的每個應用程式通常都有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="6b3cd-110">您可以使用 **AzureRmNotificationHub** Cmdlet 來移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-110">You can remove an existing notification hub by using the **Remove-AzureRmNotificationHub** cmdlet.</span></span>
<span data-ttu-id="6b3cd-111">在已移除中樞之後，您將無法再使用該中樞傳送推播通知給使用者。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="6b3cd-112">示例</span><span class="sxs-lookup"><span data-stu-id="6b3cd-112">EXAMPLES</span></span>

### <span data-ttu-id="6b3cd-113">範例1：移除通知中樞</span><span class="sxs-lookup"><span data-stu-id="6b3cd-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="6b3cd-114">這個命令會移除名為 ContosoInternalHub 的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="6b3cd-115">若要移除中樞，您必須指定中樞所在的命名空間，以及該中樞所指派給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="6b3cd-116">參數</span><span class="sxs-lookup"><span data-stu-id="6b3cd-116">PARAMETERS</span></span>

### <span data-ttu-id="6b3cd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6b3cd-117">-Force</span></span>
<span data-ttu-id="6b3cd-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6b3cd-119">-命名空間</span><span class="sxs-lookup"><span data-stu-id="6b3cd-119">-Namespace</span></span>
<span data-ttu-id="6b3cd-120">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-120">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="6b3cd-121">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="6b3cd-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="6b3cd-122">-NotificationHub</span></span>
<span data-ttu-id="6b3cd-123">指定要移除的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-123">Specifies the notification hub to be removed.</span></span>

<span data-ttu-id="6b3cd-124">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b3cd-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b3cd-125">-ResourceGroup</span></span>
<span data-ttu-id="6b3cd-126">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-126">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="6b3cd-127">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="6b3cd-128">-確認</span><span class="sxs-lookup"><span data-stu-id="6b3cd-128">-Confirm</span></span>
<span data-ttu-id="6b3cd-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b3cd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b3cd-130">-WhatIf</span></span>
<span data-ttu-id="6b3cd-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b3cd-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b3cd-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b3cd-133">-DefaultProfile</span></span>
<span data-ttu-id="6b3cd-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b3cd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b3cd-135">CommonParameters</span></span>
<span data-ttu-id="6b3cd-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b3cd-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6b3cd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b3cd-138">輸入</span><span class="sxs-lookup"><span data-stu-id="6b3cd-138">INPUTS</span></span>

## <span data-ttu-id="6b3cd-139">輸出</span><span class="sxs-lookup"><span data-stu-id="6b3cd-139">OUTPUTS</span></span>

## <span data-ttu-id="6b3cd-140">筆記</span><span class="sxs-lookup"><span data-stu-id="6b3cd-140">NOTES</span></span>

## <span data-ttu-id="6b3cd-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b3cd-141">RELATED LINKS</span></span>

[<span data-ttu-id="6b3cd-142">AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6b3cd-142">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="6b3cd-143">新-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6b3cd-143">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="6b3cd-144">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6b3cd-144">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


