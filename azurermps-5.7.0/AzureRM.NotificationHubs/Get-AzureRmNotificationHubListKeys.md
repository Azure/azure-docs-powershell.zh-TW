---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhublistkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
ms.openlocfilehash: 49bb03e903d465b372bc00118e15369f158661e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449266"
---
# <span data-ttu-id="6d5ee-101">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="6d5ee-101">Get-AzureRmNotificationHubListKeys</span></span>

## <span data-ttu-id="6d5ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d5ee-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5ee-103">取得與通知中樞授權規則相關聯的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d5ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d5ee-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubListKeys [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d5ee-105">說明</span><span class="sxs-lookup"><span data-stu-id="6d5ee-105">DESCRIPTION</span></span>
<span data-ttu-id="6d5ee-106">**AzureRmNotificationHubListKeys** Cmdlet 會傳回通知中樞共用存取簽章的主要和次要連接字串， (SAS) 授權規則。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-106">The **Get-AzureRmNotificationHubListKeys** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>

<span data-ttu-id="6d5ee-107">授權規則可管理使用者對中心的許可權。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="6d5ee-108">每個規則都包含主要和次要的連線字串。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="6d5ee-109">這些連接字串 (Uri) 執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="6d5ee-109">These connection strings (URIs) perform the following:</span></span>

- <span data-ttu-id="6d5ee-110">將使用者指向資源。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-110">Point users to a resource.</span></span>
- <span data-ttu-id="6d5ee-111">包含含查詢參數的權杖。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-111">Include a token containing query parameters.</span></span>

<span data-ttu-id="6d5ee-112">其中一個參數（即簽名）是用來驗證使用者，並提供指定的存取層級。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="6d5ee-113">示例</span><span class="sxs-lookup"><span data-stu-id="6d5ee-113">EXAMPLES</span></span>

### <span data-ttu-id="6d5ee-114">範例1：取得授權規則的主要和次要連接字串</span><span class="sxs-lookup"><span data-stu-id="6d5ee-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubListKeys -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="6d5ee-115">這個命令會取得授權規則 ListenRule （指派給 ContosoInternalHub 通知中樞的規則）的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="6d5ee-116">命令必須包含中樞命名空間和資源群組。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="6d5ee-117">參數</span><span class="sxs-lookup"><span data-stu-id="6d5ee-117">PARAMETERS</span></span>

### <span data-ttu-id="6d5ee-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6d5ee-118">-AuthorizationRule</span></span>
<span data-ttu-id="6d5ee-119">指定 (SAS) 驗證規則的共用存取簽章名稱。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="6d5ee-120">這些規則決定使用者對通知中樞所擁有的存取類型。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-120">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5ee-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5ee-121">-DefaultProfile</span></span>
<span data-ttu-id="6d5ee-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6d5ee-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d5ee-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="6d5ee-123">-Namespace</span></span>
<span data-ttu-id="6d5ee-124">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-124">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="6d5ee-125">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="6d5ee-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="6d5ee-126">-NotificationHub</span></span>
<span data-ttu-id="6d5ee-127">指定此 Cmdlet 指派授權規則的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="6d5ee-128">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5ee-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6d5ee-129">-ResourceGroup</span></span>
<span data-ttu-id="6d5ee-130">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="6d5ee-131">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="6d5ee-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5ee-132">CommonParameters</span></span>
<span data-ttu-id="6d5ee-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5ee-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5ee-135">輸入</span><span class="sxs-lookup"><span data-stu-id="6d5ee-135">INPUTS</span></span>

### <span data-ttu-id="6d5ee-136">所有</span><span class="sxs-lookup"><span data-stu-id="6d5ee-136">None</span></span>
<span data-ttu-id="6d5ee-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6d5ee-138">輸出</span><span class="sxs-lookup"><span data-stu-id="6d5ee-138">OUTPUTS</span></span>

### <span data-ttu-id="6d5ee-139">ResourceListKeys 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="6d5ee-139">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="6d5ee-140">筆記</span><span class="sxs-lookup"><span data-stu-id="6d5ee-140">NOTES</span></span>

## <span data-ttu-id="6d5ee-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d5ee-141">RELATED LINKS</span></span>

[<span data-ttu-id="6d5ee-142">AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6d5ee-142">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)


