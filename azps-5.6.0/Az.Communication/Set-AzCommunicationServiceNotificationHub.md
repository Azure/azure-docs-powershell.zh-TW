---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/set-azcommunicationservicenotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
ms.openlocfilehash: 1dbdbc6a616e9903c6a79192d089ea959835a9f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912078"
---
# <span data-ttu-id="e9f84-101">Set-AzCommunicationServiceNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e9f84-101">Set-AzCommunicationServiceNotificationHub</span></span>

## <span data-ttu-id="e9f84-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e9f84-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f84-103">將 Azure 通知中樞連結至此通訊服務。</span><span class="sxs-lookup"><span data-stu-id="e9f84-103">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="e9f84-104">語法</span><span class="sxs-lookup"><span data-stu-id="e9f84-104">SYNTAX</span></span>

### <span data-ttu-id="e9f84-105">LinkExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="e9f84-105">LinkExpanded (Default)</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -ConnectionString <String> -NotificationHubResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e9f84-106">連結</span><span class="sxs-lookup"><span data-stu-id="e9f84-106">Link</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -LinkNotificationHubParameter <ILinkNotificationHubParameters> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e9f84-107">描述</span><span class="sxs-lookup"><span data-stu-id="e9f84-107">DESCRIPTION</span></span>
<span data-ttu-id="e9f84-108">將 Azure 通知中樞連結至此通訊服務。</span><span class="sxs-lookup"><span data-stu-id="e9f84-108">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="e9f84-109">例子</span><span class="sxs-lookup"><span data-stu-id="e9f84-109">EXAMPLES</span></span>

### <span data-ttu-id="e9f84-110">範例 1：以互動式方式提供通知中樞詳細資料</span><span class="sxs-lookup"><span data-stu-id="e9f84-110">Example 1: Provide Notification Hub details interactively</span></span>
```powershell
PS C:\> Set-AzCommunicationServiceNotificationHub -CommunicationServiceName ContosoAcsResource2 -ResourceGroupName ContosoResourceProvider1 -ConnectionString "<notificationhub-connectionstring>" -NotificationHubResourceId "<notificationhub-resourceid>"
```

<span data-ttu-id="e9f84-111">連結的通知中樞可讓 ACS 資源傳送特定事件的通知。</span><span class="sxs-lookup"><span data-stu-id="e9f84-111">A linked notification hub allows a ACS resource to send notifications for certain events.</span></span>

## <span data-ttu-id="e9f84-112">參數</span><span class="sxs-lookup"><span data-stu-id="e9f84-112">PARAMETERS</span></span>

### <span data-ttu-id="e9f84-113">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="e9f84-113">-CommunicationServiceName</span></span>
<span data-ttu-id="e9f84-114">CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9f84-114">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f84-115">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e9f84-115">-ConnectionString</span></span>
<span data-ttu-id="e9f84-116">通知中樞的連接字串</span><span class="sxs-lookup"><span data-stu-id="e9f84-116">Connection string for the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f84-117">-DefaultProfile</span></span>
<span data-ttu-id="e9f84-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9f84-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f84-119">-LinkNotificationHubParameter</span><span class="sxs-lookup"><span data-stu-id="e9f84-119">-LinkNotificationHubParameter</span></span>
<span data-ttu-id="e9f84-120">若要連結至通訊服務若要建構，請參閱 LINKNOTIFICATIONHUBPARAMETER 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e9f84-120">Description of an Azure Notification Hub to link to the communication service To construct, see NOTES section for LINKNOTIFICATIONHUBPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters
Parameter Sets: Link
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f84-121">-NotificationHubResourceId</span><span class="sxs-lookup"><span data-stu-id="e9f84-121">-NotificationHubResourceId</span></span>
<span data-ttu-id="e9f84-122">通知中樞的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e9f84-122">The resource ID of the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f84-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f84-123">-ResourceGroupName</span></span>
<span data-ttu-id="e9f84-124">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e9f84-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e9f84-125">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="e9f84-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f84-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e9f84-126">-SubscriptionId</span></span>
<span data-ttu-id="e9f84-127">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9f84-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e9f84-128">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e9f84-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f84-129">-確認</span><span class="sxs-lookup"><span data-stu-id="e9f84-129">-Confirm</span></span>
<span data-ttu-id="e9f84-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e9f84-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9f84-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9f84-131">-WhatIf</span></span>
<span data-ttu-id="e9f84-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9f84-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9f84-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9f84-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9f84-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f84-134">CommonParameters</span></span>
<span data-ttu-id="e9f84-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e9f84-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f84-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9f84-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f84-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e9f84-137">INPUTS</span></span>

### <span data-ttu-id="e9f84-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span><span class="sxs-lookup"><span data-stu-id="e9f84-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span></span>

## <span data-ttu-id="e9f84-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e9f84-139">OUTPUTS</span></span>

### <span data-ttu-id="e9f84-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e9f84-140">System.String</span></span>

## <span data-ttu-id="e9f84-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e9f84-141">NOTES</span></span>

<span data-ttu-id="e9f84-142">別名</span><span class="sxs-lookup"><span data-stu-id="e9f84-142">ALIASES</span></span>

<span data-ttu-id="e9f84-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e9f84-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e9f84-144">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e9f84-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e9f84-145">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e9f84-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e9f84-146">LINKNOTIFICATIONHUBPARAMETER：連結至通訊服務的 <ILinkNotificationHubParameters> Azure 通知中樞描述</span><span class="sxs-lookup"><span data-stu-id="e9f84-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters>: Description of an Azure Notification Hub to link to the communication service</span></span>
  - <span data-ttu-id="e9f84-147">`ConnectionString <String>`：通知中樞的連接字串</span><span class="sxs-lookup"><span data-stu-id="e9f84-147">`ConnectionString <String>`: Connection string for the notification hub</span></span>
  - <span data-ttu-id="e9f84-148">`ResourceId <String>`：通知中樞的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e9f84-148">`ResourceId <String>`: The resource ID of the notification hub</span></span>

## <span data-ttu-id="e9f84-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9f84-149">RELATED LINKS</span></span>

