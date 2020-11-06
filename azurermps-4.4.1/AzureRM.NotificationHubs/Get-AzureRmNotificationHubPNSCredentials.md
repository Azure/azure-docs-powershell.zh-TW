---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
ms.openlocfilehash: 29f4871b6299685ae5791f82498083956a7e4048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448092"
---
# <span data-ttu-id="8cfe6-101">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="8cfe6-101">Get-AzureRmNotificationHubPNSCredentials</span></span>

## <span data-ttu-id="8cfe6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8cfe6-102">SYNOPSIS</span></span>
<span data-ttu-id="8cfe6-103">取得通知中樞的 PNS 認證。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-103">Gets the PNS credentials for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cfe6-104">句法</span><span class="sxs-lookup"><span data-stu-id="8cfe6-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubPNSCredentials [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cfe6-105">說明</span><span class="sxs-lookup"><span data-stu-id="8cfe6-105">DESCRIPTION</span></span>
<span data-ttu-id="8cfe6-106">**AzureRmNotificationHubPNSCredentials** Cmdlet 會取得平臺通知服務， () PNS 通知中樞的認證。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-106">The **Get-AzureRmNotificationHubPNSCredentials** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="8cfe6-107">每個通知中樞都有一組 PNS 認證。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="8cfe6-108">這些認證會套用到個別的推播通知服務，例如但不限於;iOS 推播通知服務、Android 推播通知服務和 Windows Phone 8。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="8cfe6-109">示例</span><span class="sxs-lookup"><span data-stu-id="8cfe6-109">EXAMPLES</span></span>

### <span data-ttu-id="8cfe6-110">範例1：取得特定通知中樞的 PNS 認證</span><span class="sxs-lookup"><span data-stu-id="8cfe6-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubPNSCredentials -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="8cfe6-111">這個命令會取得名為 ContosoInternalHub 的通知中樞的 PNS 認證，該通知中心屬於名為 ContosoNotificationsGroup 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="8cfe6-112">參數</span><span class="sxs-lookup"><span data-stu-id="8cfe6-112">PARAMETERS</span></span>

### <span data-ttu-id="8cfe6-113">-命名空間</span><span class="sxs-lookup"><span data-stu-id="8cfe6-113">-Namespace</span></span>
<span data-ttu-id="8cfe6-114">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-114">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="8cfe6-115">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-115">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8cfe6-116">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="8cfe6-116">-NotificationHub</span></span>
<span data-ttu-id="8cfe6-117">指定指派 PNS 認證的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-117">Specifies the notification hub that the PNS credentials are assigned to.</span></span>

<span data-ttu-id="8cfe6-118">通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-118">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="8cfe6-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8cfe6-119">-ResourceGroup</span></span>
<span data-ttu-id="8cfe6-120">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-120">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="8cfe6-121">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-121">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8cfe6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cfe6-122">-DefaultProfile</span></span>
<span data-ttu-id="8cfe6-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cfe6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cfe6-124">CommonParameters</span></span>
<span data-ttu-id="8cfe6-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cfe6-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cfe6-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8cfe6-127">INPUTS</span></span>

## <span data-ttu-id="8cfe6-128">輸出</span><span class="sxs-lookup"><span data-stu-id="8cfe6-128">OUTPUTS</span></span>

### <span data-ttu-id="8cfe6-129">NotificationHubAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="8cfe6-129">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="8cfe6-130">筆記</span><span class="sxs-lookup"><span data-stu-id="8cfe6-130">NOTES</span></span>

## <span data-ttu-id="8cfe6-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="8cfe6-131">RELATED LINKS</span></span>

[<span data-ttu-id="8cfe6-132">AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8cfe6-132">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)


