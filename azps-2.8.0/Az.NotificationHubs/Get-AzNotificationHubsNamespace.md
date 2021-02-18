---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 5c5517faa5dbd65cc6a76a02209cb2b8c429300a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410475"
---
# <span data-ttu-id="eafc5-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="eafc5-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="eafc5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eafc5-102">SYNOPSIS</span></span>
<span data-ttu-id="eafc5-103">獲得通知中樞命名空間相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eafc5-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="eafc5-104">語法</span><span class="sxs-lookup"><span data-stu-id="eafc5-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eafc5-105">描述</span><span class="sxs-lookup"><span data-stu-id="eafc5-105">DESCRIPTION</span></span>
<span data-ttu-id="eafc5-106">**Get-AzNotificationHubsNamespace** Cmdlet 會取得通知中樞命名空間相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eafc5-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="eafc5-107">此 Cmdlet 提供您取得所有命名空間資訊、指派給指定資源群組之命名空間相關資訊的選項;或用於退回特定命名空間的資訊。</span><span class="sxs-lookup"><span data-stu-id="eafc5-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="eafc5-108">命名空間是邏輯容器，可協助組織及管理通知中樞。</span><span class="sxs-lookup"><span data-stu-id="eafc5-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="eafc5-109">您至少必須有一個通知中樞命名空間：所有通知中樞都必須指派給命名空間。</span><span class="sxs-lookup"><span data-stu-id="eafc5-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="eafc5-110">單一命名空間可以包含多個中樞，這表示您可能只需要貴組織的一個命名空間。</span><span class="sxs-lookup"><span data-stu-id="eafc5-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="eafc5-111">不過，您也可以有多個命名空間，以更有效地組織中樞，或給予特定人員管理所選中樞子集的許可權。</span><span class="sxs-lookup"><span data-stu-id="eafc5-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="eafc5-112">**Get-AzNotificationHubsNamespace** Cmdlet 會返回命名空間本身的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="eafc5-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="eafc5-113">若要取得與命名空間相關聯的授權規則相關資訊，請使用 Get-AzNotificationHubsNamespaceAuthorizationRules。</span><span class="sxs-lookup"><span data-stu-id="eafc5-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="eafc5-114">例子</span><span class="sxs-lookup"><span data-stu-id="eafc5-114">EXAMPLES</span></span>

### <span data-ttu-id="eafc5-115">範例 1：取得所有通知中樞命名空間的資訊</span><span class="sxs-lookup"><span data-stu-id="eafc5-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="eafc5-116">此命令會針對您所有的通知中樞命名空間，會返回資訊。</span><span class="sxs-lookup"><span data-stu-id="eafc5-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="eafc5-117">範例 2：取得單一通知中樞命名空間的資訊</span><span class="sxs-lookup"><span data-stu-id="eafc5-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="eafc5-118">此命令會獲得單一通知中樞命名空間的資訊：ContosoNamespace。</span><span class="sxs-lookup"><span data-stu-id="eafc5-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="eafc5-119">範例 3：取得指派給特定命名空間之所有通知中樞的資訊</span><span class="sxs-lookup"><span data-stu-id="eafc5-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="eafc5-120">此命令會獲得指派給資源群組 ContosoNotificationsGroup 的所有通知中樞命名空間的資訊。</span><span class="sxs-lookup"><span data-stu-id="eafc5-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="eafc5-121">參數</span><span class="sxs-lookup"><span data-stu-id="eafc5-121">PARAMETERS</span></span>

### <span data-ttu-id="eafc5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafc5-122">-DefaultProfile</span></span>
<span data-ttu-id="eafc5-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="eafc5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eafc5-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="eafc5-124">-Namespace</span></span>
<span data-ttu-id="eafc5-125">指定命名空間的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="eafc5-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="eafc5-126">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="eafc5-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="eafc5-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eafc5-127">-ResourceGroup</span></span>
<span data-ttu-id="eafc5-128">指定指派命名空間的資源群組。</span><span class="sxs-lookup"><span data-stu-id="eafc5-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="eafc5-129">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="eafc5-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="eafc5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafc5-130">CommonParameters</span></span>
<span data-ttu-id="eafc5-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eafc5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafc5-132">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="eafc5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafc5-133">輸入</span><span class="sxs-lookup"><span data-stu-id="eafc5-133">INPUTS</span></span>

### <span data-ttu-id="eafc5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="eafc5-134">System.String</span></span>

## <span data-ttu-id="eafc5-135">輸出</span><span class="sxs-lookup"><span data-stu-id="eafc5-135">OUTPUTS</span></span>

### <span data-ttu-id="eafc5-136">Microsoft.Azure.Commands.NotificationHubs.models.命名空間Attributes</span><span class="sxs-lookup"><span data-stu-id="eafc5-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="eafc5-137">筆記</span><span class="sxs-lookup"><span data-stu-id="eafc5-137">NOTES</span></span>

## <span data-ttu-id="eafc5-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="eafc5-138">RELATED LINKS</span></span>


[<span data-ttu-id="eafc5-139">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="eafc5-139">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="eafc5-140">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="eafc5-140">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="eafc5-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="eafc5-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


