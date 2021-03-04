---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: dce2736329fe4cfac6406a6646de7388869d20e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901753"
---
# <span data-ttu-id="14af5-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="14af5-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="14af5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="14af5-102">SYNOPSIS</span></span>
<span data-ttu-id="14af5-103">獲得與通知中樞授權規則相關聯的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="14af5-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="14af5-104">語法</span><span class="sxs-lookup"><span data-stu-id="14af5-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14af5-105">描述</span><span class="sxs-lookup"><span data-stu-id="14af5-105">DESCRIPTION</span></span>
<span data-ttu-id="14af5-106">**Get-AzNotificationHubListKey** Cmdlet 會返回通知中樞共用存取簽名 (SAS) 授權規則的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="14af5-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="14af5-107">授權規則會管理中樞的使用者許可權。</span><span class="sxs-lookup"><span data-stu-id="14af5-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="14af5-108">每個規則包含主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="14af5-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="14af5-109">這些連接字串 (URI) 執行下列操作：</span><span class="sxs-lookup"><span data-stu-id="14af5-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="14af5-110">將使用者指向資源。</span><span class="sxs-lookup"><span data-stu-id="14af5-110">Point users to a resource.</span></span>
- <span data-ttu-id="14af5-111">包含包含查詢參數的權杖。</span><span class="sxs-lookup"><span data-stu-id="14af5-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="14af5-112">其中一個參數簽名可用來驗證使用者，並提供指定的存取層級。</span><span class="sxs-lookup"><span data-stu-id="14af5-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="14af5-113">例子</span><span class="sxs-lookup"><span data-stu-id="14af5-113">EXAMPLES</span></span>

### <span data-ttu-id="14af5-114">範例 1：取得授權規則的主要和次要連接字串</span><span class="sxs-lookup"><span data-stu-id="14af5-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="14af5-115">此命令會獲得授權規則 ListenRule 的主要和次要連接字串，這是指派給 ContosoInternalHub 通知中樞的規則。</span><span class="sxs-lookup"><span data-stu-id="14af5-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="14af5-116">命令必須包含中樞命名空間和資源群組。</span><span class="sxs-lookup"><span data-stu-id="14af5-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="14af5-117">參數</span><span class="sxs-lookup"><span data-stu-id="14af5-117">PARAMETERS</span></span>

### <span data-ttu-id="14af5-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="14af5-118">-AuthorizationRule</span></span>
<span data-ttu-id="14af5-119">指定 SAS 驗證規則的共用存取簽 (名稱) 名稱。</span><span class="sxs-lookup"><span data-stu-id="14af5-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="14af5-120">這些規則會決定使用者對通知中樞的存取類型。</span><span class="sxs-lookup"><span data-stu-id="14af5-120">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14af5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14af5-121">-DefaultProfile</span></span>
<span data-ttu-id="14af5-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="14af5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14af5-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="14af5-123">-Namespace</span></span>
<span data-ttu-id="14af5-124">指定指派通知中樞的命名空間。</span><span class="sxs-lookup"><span data-stu-id="14af5-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="14af5-125">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="14af5-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="14af5-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="14af5-126">-NotificationHub</span></span>
<span data-ttu-id="14af5-127">指定此 Cmdlet 指派授權規則的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="14af5-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="14af5-128">通知中樞可用來傳送推入通知給多個用戶端，無論這些用戶端使用哪個平臺。</span><span class="sxs-lookup"><span data-stu-id="14af5-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="14af5-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="14af5-129">-ResourceGroup</span></span>
<span data-ttu-id="14af5-130">指定指派通知中樞給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="14af5-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="14af5-131">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="14af5-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="14af5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14af5-132">CommonParameters</span></span>
<span data-ttu-id="14af5-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="14af5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14af5-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="14af5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14af5-135">輸入</span><span class="sxs-lookup"><span data-stu-id="14af5-135">INPUTS</span></span>

### <span data-ttu-id="14af5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="14af5-136">System.String</span></span>

## <span data-ttu-id="14af5-137">輸出</span><span class="sxs-lookup"><span data-stu-id="14af5-137">OUTPUTS</span></span>

### <span data-ttu-id="14af5-138">Microsoft.Azure.management.NotificationHubs.models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="14af5-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="14af5-139">筆記</span><span class="sxs-lookup"><span data-stu-id="14af5-139">NOTES</span></span>

## <span data-ttu-id="14af5-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="14af5-140">RELATED LINKS</span></span>

[<span data-ttu-id="14af5-141">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="14af5-141">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)


