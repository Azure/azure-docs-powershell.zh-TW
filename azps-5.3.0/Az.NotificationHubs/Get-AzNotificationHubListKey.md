---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 062d16155d4e1644e09f914a1114741e7bc5365f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448824"
---
# <span data-ttu-id="bbe2b-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="bbe2b-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="bbe2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bbe2b-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe2b-103">取得與通知中樞授權規則相關聯的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="bbe2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="bbe2b-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbe2b-105">說明</span><span class="sxs-lookup"><span data-stu-id="bbe2b-105">DESCRIPTION</span></span>
<span data-ttu-id="bbe2b-106">**AzNotificationHubListKey** Cmdlet 會傳回通知中樞共用存取簽章的主要和次要連接字串， (SAS) 授權規則。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="bbe2b-107">授權規則可管理使用者對中心的許可權。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="bbe2b-108">每個規則都包含主要和次要的連線字串。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="bbe2b-109">這些連接字串 (Uri) 執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="bbe2b-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="bbe2b-110">將使用者指向資源。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-110">Point users to a resource.</span></span>
- <span data-ttu-id="bbe2b-111">包含含查詢參數的權杖。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="bbe2b-112">其中一個參數（即簽名）是用來驗證使用者，並提供指定的存取層級。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="bbe2b-113">示例</span><span class="sxs-lookup"><span data-stu-id="bbe2b-113">EXAMPLES</span></span>

### <span data-ttu-id="bbe2b-114">範例1：取得授權規則的主要和次要連接字串</span><span class="sxs-lookup"><span data-stu-id="bbe2b-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="bbe2b-115">這個命令會取得授權規則 ListenRule （指派給 ContosoInternalHub 通知中樞的規則）的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="bbe2b-116">命令必須包含中樞命名空間和資源群組。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="bbe2b-117">參數</span><span class="sxs-lookup"><span data-stu-id="bbe2b-117">PARAMETERS</span></span>

### <span data-ttu-id="bbe2b-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bbe2b-118">-AuthorizationRule</span></span>
<span data-ttu-id="bbe2b-119">指定 (SAS) 驗證規則的共用存取簽章名稱。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="bbe2b-120">這些規則決定使用者對通知中樞所擁有的存取類型。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="bbe2b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe2b-121">-DefaultProfile</span></span>
<span data-ttu-id="bbe2b-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bbe2b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbe2b-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="bbe2b-123">-Namespace</span></span>
<span data-ttu-id="bbe2b-124">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="bbe2b-125">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="bbe2b-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="bbe2b-126">-NotificationHub</span></span>
<span data-ttu-id="bbe2b-127">指定此 Cmdlet 指派授權規則的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="bbe2b-128">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="bbe2b-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bbe2b-129">-ResourceGroup</span></span>
<span data-ttu-id="bbe2b-130">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="bbe2b-131">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="bbe2b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe2b-132">CommonParameters</span></span>
<span data-ttu-id="bbe2b-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe2b-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe2b-135">輸入</span><span class="sxs-lookup"><span data-stu-id="bbe2b-135">INPUTS</span></span>

### <span data-ttu-id="bbe2b-136">System.object</span><span class="sxs-lookup"><span data-stu-id="bbe2b-136">System.String</span></span>

## <span data-ttu-id="bbe2b-137">輸出</span><span class="sxs-lookup"><span data-stu-id="bbe2b-137">OUTPUTS</span></span>

### <span data-ttu-id="bbe2b-138">ResourceListKeys 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="bbe2b-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="bbe2b-139">筆記</span><span class="sxs-lookup"><span data-stu-id="bbe2b-139">NOTES</span></span>

## <span data-ttu-id="bbe2b-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbe2b-140">RELATED LINKS</span></span>

[<span data-ttu-id="bbe2b-141">AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bbe2b-141">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)


