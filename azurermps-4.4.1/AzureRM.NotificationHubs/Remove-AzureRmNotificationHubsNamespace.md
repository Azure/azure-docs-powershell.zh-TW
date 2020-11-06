---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: ff315c7f3634c0a8a4afd5c4b54926c0a260ed75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448080"
---
# <span data-ttu-id="cc38a-101">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cc38a-101">Remove-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="cc38a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc38a-102">SYNOPSIS</span></span>
<span data-ttu-id="cc38a-103">移除 [通知中心] 命名空間。</span><span class="sxs-lookup"><span data-stu-id="cc38a-103">Removes a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc38a-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc38a-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc38a-105">說明</span><span class="sxs-lookup"><span data-stu-id="cc38a-105">DESCRIPTION</span></span>
<span data-ttu-id="cc38a-106">**AzureRmNotificationHubsNamespace** Cmdlet 會從您的部署中移除通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="cc38a-106">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>

<span data-ttu-id="cc38a-107">命名空間是邏輯容器，可協助您組織和管理通知中樞。</span><span class="sxs-lookup"><span data-stu-id="cc38a-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="cc38a-108">**AzureRmNotificationHubsNamespace** Cmdlet 會從您的部署中移除通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="cc38a-108">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="cc38a-109">當您執行此 Cmdlet 時，會刪除指定的命名空間，以及與該命名空間關聯的所有通知中樞。</span><span class="sxs-lookup"><span data-stu-id="cc38a-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="cc38a-110">示例</span><span class="sxs-lookup"><span data-stu-id="cc38a-110">EXAMPLES</span></span>

### <span data-ttu-id="cc38a-111">範例1：移除通知中心命名空間</span><span class="sxs-lookup"><span data-stu-id="cc38a-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="cc38a-112">這個命令會移除名為 ContosoNamespace 的命名空間。</span><span class="sxs-lookup"><span data-stu-id="cc38a-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="cc38a-113">您必須指定命名空間的指派資源群組。</span><span class="sxs-lookup"><span data-stu-id="cc38a-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="cc38a-114">參數</span><span class="sxs-lookup"><span data-stu-id="cc38a-114">PARAMETERS</span></span>

### <span data-ttu-id="cc38a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cc38a-115">-Force</span></span>
<span data-ttu-id="cc38a-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="cc38a-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cc38a-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="cc38a-117">-Namespace</span></span>
<span data-ttu-id="cc38a-118">指定此 Cmdlet 移除的命名空間。</span><span class="sxs-lookup"><span data-stu-id="cc38a-118">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="cc38a-119">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="cc38a-119">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="cc38a-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cc38a-120">-ResourceGroup</span></span>
<span data-ttu-id="cc38a-121">指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="cc38a-121">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="cc38a-122">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="cc38a-122">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="cc38a-123">-確認</span><span class="sxs-lookup"><span data-stu-id="cc38a-123">-Confirm</span></span>
<span data-ttu-id="cc38a-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cc38a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc38a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc38a-125">-WhatIf</span></span>
<span data-ttu-id="cc38a-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc38a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc38a-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc38a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc38a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc38a-128">-DefaultProfile</span></span>
<span data-ttu-id="cc38a-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc38a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc38a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc38a-130">CommonParameters</span></span>
<span data-ttu-id="cc38a-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc38a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc38a-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cc38a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc38a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="cc38a-133">INPUTS</span></span>

## <span data-ttu-id="cc38a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="cc38a-134">OUTPUTS</span></span>

## <span data-ttu-id="cc38a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="cc38a-135">NOTES</span></span>

## <span data-ttu-id="cc38a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc38a-136">RELATED LINKS</span></span>

[<span data-ttu-id="cc38a-137">AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cc38a-137">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="cc38a-138">新-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cc38a-138">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="cc38a-139">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cc38a-139">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


