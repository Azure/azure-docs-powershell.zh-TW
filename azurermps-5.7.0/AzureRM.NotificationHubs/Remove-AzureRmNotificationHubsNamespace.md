---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 2a728cdae95c117e73f38b16cdea5407c1f4954e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447735"
---
# <span data-ttu-id="81235-101">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="81235-101">Remove-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="81235-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81235-102">SYNOPSIS</span></span>
<span data-ttu-id="81235-103">移除 [通知中心] 命名空間。</span><span class="sxs-lookup"><span data-stu-id="81235-103">Removes a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81235-104">句法</span><span class="sxs-lookup"><span data-stu-id="81235-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81235-105">說明</span><span class="sxs-lookup"><span data-stu-id="81235-105">DESCRIPTION</span></span>
<span data-ttu-id="81235-106">**AzureRmNotificationHubsNamespace** Cmdlet 會從您的部署中移除通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="81235-106">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>

<span data-ttu-id="81235-107">命名空間是邏輯容器，可協助您組織和管理通知中樞。</span><span class="sxs-lookup"><span data-stu-id="81235-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="81235-108">**AzureRmNotificationHubsNamespace** Cmdlet 會從您的部署中移除通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="81235-108">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="81235-109">當您執行此 Cmdlet 時，會刪除指定的命名空間，以及與該命名空間關聯的所有通知中樞。</span><span class="sxs-lookup"><span data-stu-id="81235-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="81235-110">示例</span><span class="sxs-lookup"><span data-stu-id="81235-110">EXAMPLES</span></span>

### <span data-ttu-id="81235-111">範例1：移除通知中心命名空間</span><span class="sxs-lookup"><span data-stu-id="81235-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="81235-112">這個命令會移除名為 ContosoNamespace 的命名空間。</span><span class="sxs-lookup"><span data-stu-id="81235-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="81235-113">您必須指定命名空間的指派資源群組。</span><span class="sxs-lookup"><span data-stu-id="81235-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="81235-114">參數</span><span class="sxs-lookup"><span data-stu-id="81235-114">PARAMETERS</span></span>

### <span data-ttu-id="81235-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81235-115">-DefaultProfile</span></span>
<span data-ttu-id="81235-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="81235-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81235-117">-Force</span><span class="sxs-lookup"><span data-stu-id="81235-117">-Force</span></span>
<span data-ttu-id="81235-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="81235-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="81235-119">-命名空間</span><span class="sxs-lookup"><span data-stu-id="81235-119">-Namespace</span></span>
<span data-ttu-id="81235-120">指定此 Cmdlet 移除的命名空間。</span><span class="sxs-lookup"><span data-stu-id="81235-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="81235-121">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="81235-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="81235-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="81235-122">-ResourceGroup</span></span>
<span data-ttu-id="81235-123">指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="81235-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="81235-124">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="81235-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="81235-125">-確認</span><span class="sxs-lookup"><span data-stu-id="81235-125">-Confirm</span></span>
<span data-ttu-id="81235-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81235-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81235-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81235-127">-WhatIf</span></span>
<span data-ttu-id="81235-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81235-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81235-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81235-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81235-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81235-130">CommonParameters</span></span>
<span data-ttu-id="81235-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81235-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81235-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81235-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81235-133">輸入</span><span class="sxs-lookup"><span data-stu-id="81235-133">INPUTS</span></span>

### <span data-ttu-id="81235-134">所有</span><span class="sxs-lookup"><span data-stu-id="81235-134">None</span></span>
<span data-ttu-id="81235-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="81235-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="81235-136">輸出</span><span class="sxs-lookup"><span data-stu-id="81235-136">OUTPUTS</span></span>

## <span data-ttu-id="81235-137">筆記</span><span class="sxs-lookup"><span data-stu-id="81235-137">NOTES</span></span>

## <span data-ttu-id="81235-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="81235-138">RELATED LINKS</span></span>

[<span data-ttu-id="81235-139">AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="81235-139">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="81235-140">新-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="81235-140">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="81235-141">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="81235-141">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


