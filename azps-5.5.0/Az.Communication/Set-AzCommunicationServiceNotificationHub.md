---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/set-azcommunicationservicenotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
ms.openlocfilehash: aa9084f067131abb780de798dcd1af0ed8f9d235
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127910"
---
# <span data-ttu-id="1e752-101">Set-AzCommunicationServiceNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1e752-101">Set-AzCommunicationServiceNotificationHub</span></span>

## <span data-ttu-id="1e752-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e752-102">SYNOPSIS</span></span>
<span data-ttu-id="1e752-103">將 Azure 通知中樞連結至此通訊服務。</span><span class="sxs-lookup"><span data-stu-id="1e752-103">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="1e752-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e752-104">SYNTAX</span></span>

### <span data-ttu-id="1e752-105">LinkExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="1e752-105">LinkExpanded (Default)</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -ConnectionString <String> -NotificationHubResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1e752-106">鏈路</span><span class="sxs-lookup"><span data-stu-id="1e752-106">Link</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -LinkNotificationHubParameter <ILinkNotificationHubParameters> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1e752-107">說明</span><span class="sxs-lookup"><span data-stu-id="1e752-107">DESCRIPTION</span></span>
<span data-ttu-id="1e752-108">將 Azure 通知中樞連結至此通訊服務。</span><span class="sxs-lookup"><span data-stu-id="1e752-108">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="1e752-109">示例</span><span class="sxs-lookup"><span data-stu-id="1e752-109">EXAMPLES</span></span>

### <span data-ttu-id="1e752-110">範例1：以互動方式提供通知中樞的詳細資料</span><span class="sxs-lookup"><span data-stu-id="1e752-110">Example 1: Provide Notification Hub details interactively</span></span>
```powershell
PS C:\> Set-AzCommunicationServiceNotificationHub -CommunicationServiceName ContosoAcsResource2 -ResourceGroupName ContosoResourceProvider1 -ConnectionString "<notificationhub-connectionstring>" -NotificationHubResourceId "<notificationhub-resourceid>"
```

<span data-ttu-id="1e752-111">連結的通知中樞可讓 ACS 資源傳送特定事件的通知。</span><span class="sxs-lookup"><span data-stu-id="1e752-111">A linked notification hub allows a ACS resource to send notifications for certain events.</span></span>

## <span data-ttu-id="1e752-112">參數</span><span class="sxs-lookup"><span data-stu-id="1e752-112">PARAMETERS</span></span>

### <span data-ttu-id="1e752-113">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="1e752-113">-CommunicationServiceName</span></span>
<span data-ttu-id="1e752-114">CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e752-114">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="1e752-115">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1e752-115">-ConnectionString</span></span>
<span data-ttu-id="1e752-116">通知中樞的連接字串</span><span class="sxs-lookup"><span data-stu-id="1e752-116">Connection string for the notification hub</span></span>

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

### <span data-ttu-id="1e752-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e752-117">-DefaultProfile</span></span>
<span data-ttu-id="1e752-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e752-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e752-119">-LinkNotificationHubParameter</span><span class="sxs-lookup"><span data-stu-id="1e752-119">-LinkNotificationHubParameter</span></span>
<span data-ttu-id="1e752-120">Azure 通知中樞的描述若要連結至要構造的通訊服務，請參閱 LINKNOTIFICATIONHUBPARAMETER 屬性和建立雜湊資料表的備忘稿一節。</span><span class="sxs-lookup"><span data-stu-id="1e752-120">Description of an Azure Notification Hub to link to the communication service To construct, see NOTES section for LINKNOTIFICATIONHUBPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="1e752-121">-NotificationHubResourceId</span><span class="sxs-lookup"><span data-stu-id="1e752-121">-NotificationHubResourceId</span></span>
<span data-ttu-id="1e752-122">通知中樞的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1e752-122">The resource ID of the notification hub</span></span>

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

### <span data-ttu-id="1e752-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e752-123">-ResourceGroupName</span></span>
<span data-ttu-id="1e752-124">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e752-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1e752-125">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="1e752-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1e752-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e752-126">-SubscriptionId</span></span>
<span data-ttu-id="1e752-127">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="1e752-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1e752-128">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="1e752-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1e752-129">-確認</span><span class="sxs-lookup"><span data-stu-id="1e752-129">-Confirm</span></span>
<span data-ttu-id="1e752-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e752-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e752-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e752-131">-WhatIf</span></span>
<span data-ttu-id="1e752-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e752-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e752-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e752-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e752-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e752-134">CommonParameters</span></span>
<span data-ttu-id="1e752-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e752-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e752-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1e752-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e752-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1e752-137">INPUTS</span></span>

### <span data-ttu-id="1e752-138">ILinkNotificationHubParameters 中的 Api20200820Preview （）。</span><span class="sxs-lookup"><span data-stu-id="1e752-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span></span>

## <span data-ttu-id="1e752-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1e752-139">OUTPUTS</span></span>

### <span data-ttu-id="1e752-140">System.object</span><span class="sxs-lookup"><span data-stu-id="1e752-140">System.String</span></span>

## <span data-ttu-id="1e752-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1e752-141">NOTES</span></span>

<span data-ttu-id="1e752-142">別名</span><span class="sxs-lookup"><span data-stu-id="1e752-142">ALIASES</span></span>

<span data-ttu-id="1e752-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="1e752-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1e752-144">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="1e752-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1e752-145">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="1e752-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1e752-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters> ： Azure 通知中樞的描述，以連結至通訊服務</span><span class="sxs-lookup"><span data-stu-id="1e752-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters>: Description of an Azure Notification Hub to link to the communication service</span></span>
  - <span data-ttu-id="1e752-147">`ConnectionString <String>`：通知中樞的連接字串</span><span class="sxs-lookup"><span data-stu-id="1e752-147">`ConnectionString <String>`: Connection string for the notification hub</span></span>
  - <span data-ttu-id="1e752-148">`ResourceId <String>`：通知中樞的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1e752-148">`ResourceId <String>`: The resource ID of the notification hub</span></span>

## <span data-ttu-id="1e752-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e752-149">RELATED LINKS</span></span>

