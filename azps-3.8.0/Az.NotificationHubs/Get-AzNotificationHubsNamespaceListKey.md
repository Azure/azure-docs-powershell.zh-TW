---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 90e617f35442470cef2d11c2de032679698ea167
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798346"
---
# <span data-ttu-id="854df-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="854df-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="854df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="854df-102">SYNOPSIS</span></span>
<span data-ttu-id="854df-103">取得與通知中心命名空間授權規則相關聯的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="854df-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="854df-104">句法</span><span class="sxs-lookup"><span data-stu-id="854df-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="854df-105">說明</span><span class="sxs-lookup"><span data-stu-id="854df-105">DESCRIPTION</span></span>
<span data-ttu-id="854df-106">**AzNotificationHubsNamespaceListKey** Cmdlet 會傳回 (SAS) 指派給通知中心命名空間的授權規則的主要及次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="854df-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="854df-107">授權規則管理使用者對通知中心命名空間的權利。</span><span class="sxs-lookup"><span data-stu-id="854df-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="854df-108">每個規則都包含主要和次要的連線字串。</span><span class="sxs-lookup"><span data-stu-id="854df-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="854df-109">示例</span><span class="sxs-lookup"><span data-stu-id="854df-109">EXAMPLES</span></span>

### <span data-ttu-id="854df-110">範例1：取得授權規則的主要和次要連接字串</span><span class="sxs-lookup"><span data-stu-id="854df-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="854df-111">這個命令會傳回指派給 ContosoNamespace 命名空間之 [ListenRule] 授權規則的主要及次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="854df-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="854df-112">當您執行此命令時，您必須包含指定命名空間之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="854df-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="854df-113">參數</span><span class="sxs-lookup"><span data-stu-id="854df-113">PARAMETERS</span></span>

### <span data-ttu-id="854df-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="854df-114">-AuthorizationRule</span></span>
<span data-ttu-id="854df-115">指定 SAS 驗證規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="854df-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="854df-116">這些規則決定使用者對通知中樞所擁有的存取類型。</span><span class="sxs-lookup"><span data-stu-id="854df-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="854df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="854df-117">-DefaultProfile</span></span>
<span data-ttu-id="854df-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="854df-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="854df-119">-命名空間</span><span class="sxs-lookup"><span data-stu-id="854df-119">-Namespace</span></span>
<span data-ttu-id="854df-120">指定包含此 Cmdlet 所取得之連接字串的命名空間。</span><span class="sxs-lookup"><span data-stu-id="854df-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="854df-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="854df-121">-ResourceGroup</span></span>
<span data-ttu-id="854df-122">指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="854df-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="854df-123">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="854df-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="854df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="854df-124">CommonParameters</span></span>
<span data-ttu-id="854df-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="854df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="854df-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="854df-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="854df-127">輸入</span><span class="sxs-lookup"><span data-stu-id="854df-127">INPUTS</span></span>

### <span data-ttu-id="854df-128">System.object</span><span class="sxs-lookup"><span data-stu-id="854df-128">System.String</span></span>

## <span data-ttu-id="854df-129">輸出</span><span class="sxs-lookup"><span data-stu-id="854df-129">OUTPUTS</span></span>

### <span data-ttu-id="854df-130">ResourceListKeys 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="854df-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="854df-131">筆記</span><span class="sxs-lookup"><span data-stu-id="854df-131">NOTES</span></span>

## <span data-ttu-id="854df-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="854df-132">RELATED LINKS</span></span>

[<span data-ttu-id="854df-133">AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="854df-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="854df-134">AzNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="854df-134">Get-AzNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)


