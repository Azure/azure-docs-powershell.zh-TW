---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137500"
---
# <span data-ttu-id="b378f-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b378f-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="b378f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b378f-102">SYNOPSIS</span></span>
<span data-ttu-id="b378f-103">取得通知中心命名空間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b378f-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="b378f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b378f-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b378f-105">說明</span><span class="sxs-lookup"><span data-stu-id="b378f-105">DESCRIPTION</span></span>
<span data-ttu-id="b378f-106">**AzNotificationHubsNamespace** Cmdlet 會取得通知中心命名空間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b378f-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="b378f-107">這個 Cmdlet 可讓您選擇取得所有命名空間的資訊，以及指派給指定資源群組的命名空間資訊;或傳回特定命名空間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b378f-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="b378f-108">命名空間是邏輯容器，可協助您組織和管理通知中樞。</span><span class="sxs-lookup"><span data-stu-id="b378f-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="b378f-109">您必須至少有一個通知中心命名空間：所有通知中樞都必須指派給命名空間。</span><span class="sxs-lookup"><span data-stu-id="b378f-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="b378f-110">單一命名空間可以存放多個中心，這表示您在組織中可能只需要一個命名空間。</span><span class="sxs-lookup"><span data-stu-id="b378f-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="b378f-111">不過，您也可以使用多個命名空間來更完善地組織您的中樞，或提供特定的個人許可權來管理選取的中樞子集。</span><span class="sxs-lookup"><span data-stu-id="b378f-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="b378f-112">**AzNotificationHubsNamespace** Cmdlet 會傳回有關命名空間本身的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="b378f-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="b378f-113">若要取得與命名空間相關聯之授權規則的相關資訊，請使用 AzNotificationHubsNamespaceAuthorizationRules。</span><span class="sxs-lookup"><span data-stu-id="b378f-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="b378f-114">示例</span><span class="sxs-lookup"><span data-stu-id="b378f-114">EXAMPLES</span></span>

### <span data-ttu-id="b378f-115">範例1：取得所有通知中心命名空間的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b378f-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="b378f-116">這個命令會傳回所有通知中心命名空間的資訊。</span><span class="sxs-lookup"><span data-stu-id="b378f-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="b378f-117">範例2：取得單一通知中樞命名空間的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b378f-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="b378f-118">這個命令會取得單一通知中樞命名空間的資訊： ContosoNamespace。</span><span class="sxs-lookup"><span data-stu-id="b378f-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="b378f-119">範例3：取得指派給特定命名空間之所有通知中心的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b378f-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="b378f-120">這個命令會取得指派給資源群組 ContosoNotificationsGroup 的所有通知中心命名空間的資訊。</span><span class="sxs-lookup"><span data-stu-id="b378f-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="b378f-121">參數</span><span class="sxs-lookup"><span data-stu-id="b378f-121">PARAMETERS</span></span>

### <span data-ttu-id="b378f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b378f-122">-DefaultProfile</span></span>
<span data-ttu-id="b378f-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b378f-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b378f-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="b378f-124">-Namespace</span></span>
<span data-ttu-id="b378f-125">指定命名空間的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="b378f-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="b378f-126">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="b378f-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b378f-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b378f-127">-ResourceGroup</span></span>
<span data-ttu-id="b378f-128">指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="b378f-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="b378f-129">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="b378f-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b378f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b378f-130">CommonParameters</span></span>
<span data-ttu-id="b378f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b378f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b378f-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b378f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b378f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b378f-133">INPUTS</span></span>

### <span data-ttu-id="b378f-134">System.object</span><span class="sxs-lookup"><span data-stu-id="b378f-134">System.String</span></span>

## <span data-ttu-id="b378f-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b378f-135">OUTPUTS</span></span>

### <span data-ttu-id="b378f-136">NamespaceAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="b378f-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="b378f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b378f-137">NOTES</span></span>

## <span data-ttu-id="b378f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b378f-138">RELATED LINKS</span></span>

[<span data-ttu-id="b378f-139">AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b378f-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="b378f-140">新-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b378f-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="b378f-141">移除-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b378f-141">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="b378f-142">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b378f-142">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


