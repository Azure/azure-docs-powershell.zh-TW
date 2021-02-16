---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 5244602a6b6266ebabf02bbb927facda93e61d8b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403794"
---
# <span data-ttu-id="8b2c6-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="8b2c6-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="8b2c6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8b2c6-102">SYNOPSIS</span></span>
<span data-ttu-id="8b2c6-103">獲得與通知中樞命名空間授權規則相關聯的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="8b2c6-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="8b2c6-104">語法</span><span class="sxs-lookup"><span data-stu-id="8b2c6-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b2c6-105">描述</span><span class="sxs-lookup"><span data-stu-id="8b2c6-105">DESCRIPTION</span></span>
<span data-ttu-id="8b2c6-106">**Get-AzNotificationHubsNamespaceListKey** Cmdlet 會針對指派給通知中樞命名空間的共用存取簽章 (SAS) 授權規則，會返回主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="8b2c6-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="8b2c6-107">授權規則會管理通知中樞命名空間的使用者許可權。</span><span class="sxs-lookup"><span data-stu-id="8b2c6-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="8b2c6-108">每個規則包含主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="8b2c6-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="8b2c6-109">例子</span><span class="sxs-lookup"><span data-stu-id="8b2c6-109">EXAMPLES</span></span>

### <span data-ttu-id="8b2c6-110">範例 1：取得授權規則的主要和次要連接字串</span><span class="sxs-lookup"><span data-stu-id="8b2c6-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="8b2c6-111">此命令會針對指派給 ContosoNamespace 命名空間的授權規則 ListenRule，會返回主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="8b2c6-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="8b2c6-112">當您執行此命令時，您必須包含命名空間指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8b2c6-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="8b2c6-113">參數</span><span class="sxs-lookup"><span data-stu-id="8b2c6-113">PARAMETERS</span></span>

### <span data-ttu-id="8b2c6-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8b2c6-114">-AuthorizationRule</span></span>
<span data-ttu-id="8b2c6-115">指定 SAS 驗證規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b2c6-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="8b2c6-116">這些規則會決定使用者對通知中樞的存取類型。</span><span class="sxs-lookup"><span data-stu-id="8b2c6-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="8b2c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b2c6-117">-DefaultProfile</span></span>
<span data-ttu-id="8b2c6-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8b2c6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b2c6-119">-命名空間</span><span class="sxs-lookup"><span data-stu-id="8b2c6-119">-Namespace</span></span>
<span data-ttu-id="8b2c6-120">指定包含此 Cmdlet 所獲取之連接字串的命名空間。</span><span class="sxs-lookup"><span data-stu-id="8b2c6-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8b2c6-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b2c6-121">-ResourceGroup</span></span>
<span data-ttu-id="8b2c6-122">指定指派命名空間的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8b2c6-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="8b2c6-123">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="8b2c6-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8b2c6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b2c6-124">CommonParameters</span></span>
<span data-ttu-id="8b2c6-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8b2c6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b2c6-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8b2c6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b2c6-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8b2c6-127">INPUTS</span></span>

### <span data-ttu-id="8b2c6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8b2c6-128">System.String</span></span>

## <span data-ttu-id="8b2c6-129">輸出</span><span class="sxs-lookup"><span data-stu-id="8b2c6-129">OUTPUTS</span></span>

### <span data-ttu-id="8b2c6-130">Microsoft.Azure.management.NotificationHubs.models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="8b2c6-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="8b2c6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8b2c6-131">NOTES</span></span>

## <span data-ttu-id="8b2c6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b2c6-132">RELATED LINKS</span></span>

[<span data-ttu-id="8b2c6-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="8b2c6-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)



