---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: e03be5a1daae753e1538b171586d9a8e46ad8021
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134774"
---
# <span data-ttu-id="c18ea-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c18ea-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="c18ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c18ea-102">SYNOPSIS</span></span>
<span data-ttu-id="c18ea-103">移除 [通知中心] 命名空間。</span><span class="sxs-lookup"><span data-stu-id="c18ea-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="c18ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="c18ea-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c18ea-105">說明</span><span class="sxs-lookup"><span data-stu-id="c18ea-105">DESCRIPTION</span></span>
<span data-ttu-id="c18ea-106">**AzNotificationHubsNamespace** Cmdlet 會從您的部署中移除通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="c18ea-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="c18ea-107">命名空間是邏輯容器，可協助您組織和管理通知中樞。</span><span class="sxs-lookup"><span data-stu-id="c18ea-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="c18ea-108">**AzNotificationHubsNamespace** Cmdlet 會從您的部署中移除通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="c18ea-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="c18ea-109">當您執行此 Cmdlet 時，會刪除指定的命名空間，以及與該命名空間關聯的所有通知中樞。</span><span class="sxs-lookup"><span data-stu-id="c18ea-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="c18ea-110">示例</span><span class="sxs-lookup"><span data-stu-id="c18ea-110">EXAMPLES</span></span>

### <span data-ttu-id="c18ea-111">範例1：移除通知中心命名空間</span><span class="sxs-lookup"><span data-stu-id="c18ea-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="c18ea-112">這個命令會移除名為 ContosoNamespace 的命名空間。</span><span class="sxs-lookup"><span data-stu-id="c18ea-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="c18ea-113">您必須指定命名空間的指派資源群組。</span><span class="sxs-lookup"><span data-stu-id="c18ea-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="c18ea-114">參數</span><span class="sxs-lookup"><span data-stu-id="c18ea-114">PARAMETERS</span></span>

### <span data-ttu-id="c18ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c18ea-115">-DefaultProfile</span></span>
<span data-ttu-id="c18ea-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c18ea-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c18ea-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c18ea-117">-Force</span></span>
<span data-ttu-id="c18ea-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="c18ea-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c18ea-119">-命名空間</span><span class="sxs-lookup"><span data-stu-id="c18ea-119">-Namespace</span></span>
<span data-ttu-id="c18ea-120">指定此 Cmdlet 移除的命名空間。</span><span class="sxs-lookup"><span data-stu-id="c18ea-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="c18ea-121">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="c18ea-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="c18ea-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c18ea-122">-ResourceGroup</span></span>
<span data-ttu-id="c18ea-123">指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="c18ea-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="c18ea-124">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="c18ea-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="c18ea-125">-確認</span><span class="sxs-lookup"><span data-stu-id="c18ea-125">-Confirm</span></span>
<span data-ttu-id="c18ea-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c18ea-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c18ea-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c18ea-127">-WhatIf</span></span>
<span data-ttu-id="c18ea-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c18ea-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c18ea-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c18ea-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c18ea-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c18ea-130">CommonParameters</span></span>
<span data-ttu-id="c18ea-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c18ea-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c18ea-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c18ea-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c18ea-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c18ea-133">INPUTS</span></span>

### <span data-ttu-id="c18ea-134">System.object</span><span class="sxs-lookup"><span data-stu-id="c18ea-134">System.String</span></span>

## <span data-ttu-id="c18ea-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c18ea-135">OUTPUTS</span></span>

### <span data-ttu-id="c18ea-136">System.void</span><span class="sxs-lookup"><span data-stu-id="c18ea-136">System.Void</span></span>

## <span data-ttu-id="c18ea-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c18ea-137">NOTES</span></span>

## <span data-ttu-id="c18ea-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c18ea-138">RELATED LINKS</span></span>

[<span data-ttu-id="c18ea-139">AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c18ea-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="c18ea-140">新-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c18ea-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="c18ea-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c18ea-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


