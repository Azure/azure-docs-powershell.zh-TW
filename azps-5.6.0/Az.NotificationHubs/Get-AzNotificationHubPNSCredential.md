---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 44da06fa8237880be154100d05eeee60cd7db7b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901750"
---
# <span data-ttu-id="df723-101">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="df723-101">Get-AzNotificationHubPNSCredential</span></span>

## <span data-ttu-id="df723-102">簡介</span><span class="sxs-lookup"><span data-stu-id="df723-102">SYNOPSIS</span></span>
<span data-ttu-id="df723-103">獲得通知中樞的 PNS 認證。</span><span class="sxs-lookup"><span data-stu-id="df723-103">Gets the PNS credentials for a notification hub.</span></span>

## <span data-ttu-id="df723-104">語法</span><span class="sxs-lookup"><span data-stu-id="df723-104">SYNTAX</span></span>

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df723-105">描述</span><span class="sxs-lookup"><span data-stu-id="df723-105">DESCRIPTION</span></span>
<span data-ttu-id="df723-106">**Get-AzNotificationHubPNSCredential Cmdlet** 會取得通知中樞的平臺 (PNS) 認證。</span><span class="sxs-lookup"><span data-stu-id="df723-106">The **Get-AzNotificationHubPNSCredential** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="df723-107">每個通知中樞都有一組 PNS 認證。</span><span class="sxs-lookup"><span data-stu-id="df723-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="df723-108">這些認證會適用于個別推入通知服務，例如，但不限於;iOS 推入通知服務、Android 推入通知服務和 Windows Phone 8。</span><span class="sxs-lookup"><span data-stu-id="df723-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="df723-109">例子</span><span class="sxs-lookup"><span data-stu-id="df723-109">EXAMPLES</span></span>

### <span data-ttu-id="df723-110">範例 1：取得特定通知中樞的 PNS 認證</span><span class="sxs-lookup"><span data-stu-id="df723-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="df723-111">此命令會為名稱為 ContosoInternalHub 的通知中樞獲得 PNS 認證，該通知中樞屬於名為 ContosoNotificationsGroup 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="df723-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="df723-112">參數</span><span class="sxs-lookup"><span data-stu-id="df723-112">PARAMETERS</span></span>

### <span data-ttu-id="df723-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df723-113">-DefaultProfile</span></span>
<span data-ttu-id="df723-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="df723-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df723-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="df723-115">-Namespace</span></span>
<span data-ttu-id="df723-116">指定指派通知中樞的命名空間。</span><span class="sxs-lookup"><span data-stu-id="df723-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="df723-117">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="df723-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="df723-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="df723-118">-NotificationHub</span></span>
<span data-ttu-id="df723-119">指定指派 PNS 認證的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="df723-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="df723-120">通知中樞可用來傳送推入通知給多個用戶端，無論這些用戶端使用哪個平臺。</span><span class="sxs-lookup"><span data-stu-id="df723-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="df723-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="df723-121">-ResourceGroup</span></span>
<span data-ttu-id="df723-122">指定指派通知中樞給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="df723-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="df723-123">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="df723-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="df723-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df723-124">CommonParameters</span></span>
<span data-ttu-id="df723-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="df723-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df723-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="df723-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df723-127">輸入</span><span class="sxs-lookup"><span data-stu-id="df723-127">INPUTS</span></span>

### <span data-ttu-id="df723-128">System.String</span><span class="sxs-lookup"><span data-stu-id="df723-128">System.String</span></span>

## <span data-ttu-id="df723-129">輸出</span><span class="sxs-lookup"><span data-stu-id="df723-129">OUTPUTS</span></span>

### <span data-ttu-id="df723-130">Microsoft.Azure.Commands.NotificationHubs.models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="df723-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="df723-131">筆記</span><span class="sxs-lookup"><span data-stu-id="df723-131">NOTES</span></span>

## <span data-ttu-id="df723-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="df723-132">RELATED LINKS</span></span>

[<span data-ttu-id="df723-133">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="df723-133">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)


