---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: 7535ff45b8350cb107b7593dc78ab0709d747f8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901701"
---
# <span data-ttu-id="87cf7-101">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="87cf7-101">Set-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="87cf7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="87cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="87cf7-103">設定通知中樞命名空間的屬性值。</span><span class="sxs-lookup"><span data-stu-id="87cf7-103">Sets property values for a notification hub namespace.</span></span>

## <span data-ttu-id="87cf7-104">語法</span><span class="sxs-lookup"><span data-stu-id="87cf7-104">SYNTAX</span></span>

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87cf7-105">描述</span><span class="sxs-lookup"><span data-stu-id="87cf7-105">DESCRIPTION</span></span>
<span data-ttu-id="87cf7-106">**Set-AzNotificationHubsNamespace** Cmdlet 會設定現有通知中樞命名空間的屬性值。</span><span class="sxs-lookup"><span data-stu-id="87cf7-106">The **Set-AzNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="87cf7-107">命名空間是邏輯容器，可協助組織及管理通知中樞。</span><span class="sxs-lookup"><span data-stu-id="87cf7-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="87cf7-108">您至少必須有一個通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="87cf7-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="87cf7-109">此外，所有通知中樞都必須有指派的命名空間。</span><span class="sxs-lookup"><span data-stu-id="87cf7-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="87cf7-110">此 Cmdlet 主要用來啟用和停用命名空間。</span><span class="sxs-lookup"><span data-stu-id="87cf7-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="87cf7-111">當命名空間停用時，使用者無法連接到命名空間中任何通知中樞，系統管理員也無法使用這些中樞來傳送推入通知。</span><span class="sxs-lookup"><span data-stu-id="87cf7-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="87cf7-112">若要重新啟用停用的命名空間，請使用此 Cmdlet 將 **命名空間的 State** 屬性設為 Active。</span><span class="sxs-lookup"><span data-stu-id="87cf7-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="87cf7-113">您也可以使用此 Cmdlet 將命名空間標記為重要。</span><span class="sxs-lookup"><span data-stu-id="87cf7-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="87cf7-114">這可防止命名空間遭到刪除。</span><span class="sxs-lookup"><span data-stu-id="87cf7-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="87cf7-115">若要移除重要命名空間，您必須先移除重要標記。</span><span class="sxs-lookup"><span data-stu-id="87cf7-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="87cf7-116">例子</span><span class="sxs-lookup"><span data-stu-id="87cf7-116">EXAMPLES</span></span>

### <span data-ttu-id="87cf7-117">範例 1：停用命名空間</span><span class="sxs-lookup"><span data-stu-id="87cf7-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="87cf7-118">此命令會停用名稱為 ContosoPartners 的命名空間，該命名空間位於美國西部資料中心，並指派給 ContosoNotificationsGroup 資源群組。</span><span class="sxs-lookup"><span data-stu-id="87cf7-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="87cf7-119">範例 2：啟用命名空間</span><span class="sxs-lookup"><span data-stu-id="87cf7-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="87cf7-120">此命令啟用名稱為 ContosoPartners 的命名空間，位於美國西部資料中心，並指派給 ContosoNotificationsGroup 資源群組。</span><span class="sxs-lookup"><span data-stu-id="87cf7-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="87cf7-121">參數</span><span class="sxs-lookup"><span data-stu-id="87cf7-121">PARAMETERS</span></span>

### <span data-ttu-id="87cf7-122">-重要</span><span class="sxs-lookup"><span data-stu-id="87cf7-122">-Critical</span></span>
<span data-ttu-id="87cf7-123">指出命名空間是否是重要的命名空間。</span><span class="sxs-lookup"><span data-stu-id="87cf7-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="87cf7-124">無法刪除重要命名空間。</span><span class="sxs-lookup"><span data-stu-id="87cf7-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="87cf7-125">若要刪除重要命名空間，您必須將此屬性的值設為 False，才能將命名空間標記為非重要。</span><span class="sxs-lookup"><span data-stu-id="87cf7-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cf7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87cf7-126">-DefaultProfile</span></span>
<span data-ttu-id="87cf7-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="87cf7-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87cf7-128">-強制</span><span class="sxs-lookup"><span data-stu-id="87cf7-128">-Force</span></span>
<span data-ttu-id="87cf7-129">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="87cf7-129">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87cf7-130">-位置</span><span class="sxs-lookup"><span data-stu-id="87cf7-130">-Location</span></span>
<span data-ttu-id="87cf7-131">指定託管命名空間之資料中心的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="87cf7-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="87cf7-132">雖然您可以將此參數設定為任何有效的 Azure 位置，但為了獲得最佳的績效，您應該使用靠近大多數使用者的資料中心。</span><span class="sxs-lookup"><span data-stu-id="87cf7-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="87cf7-133">若要取得最新的 Azure 位置清單，請執行下列命令： `Get-AzLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="87cf7-133">To get an up-to-date list of Azure locations run the following command: `Get-AzLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="87cf7-134">-命名空間</span><span class="sxs-lookup"><span data-stu-id="87cf7-134">-Namespace</span></span>
<span data-ttu-id="87cf7-135">指定此 Cmdlet 修改的命名空間。</span><span class="sxs-lookup"><span data-stu-id="87cf7-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="87cf7-136">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="87cf7-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="87cf7-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="87cf7-137">-ResourceGroup</span></span>
<span data-ttu-id="87cf7-138">指定指派命名空間的資源群組。</span><span class="sxs-lookup"><span data-stu-id="87cf7-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="87cf7-139">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="87cf7-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="87cf7-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="87cf7-140">-SkuTier</span></span>
<span data-ttu-id="87cf7-141">命名空間的 SKU 層級</span><span class="sxs-lookup"><span data-stu-id="87cf7-141">Sku tier of the namespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cf7-142">-State</span><span class="sxs-lookup"><span data-stu-id="87cf7-142">-State</span></span>
<span data-ttu-id="87cf7-143">指定命名空間的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="87cf7-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="87cf7-144">此參數可接受的值為：使用中和已停用。</span><span class="sxs-lookup"><span data-stu-id="87cf7-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cf7-145">-標記</span><span class="sxs-lookup"><span data-stu-id="87cf7-145">-Tag</span></span>
<span data-ttu-id="87cf7-146">指定可用來分類及組織 Azure 專案的名稱值組。</span><span class="sxs-lookup"><span data-stu-id="87cf7-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="87cf7-147">標記的運作方式類似關鍵字，而且可在整個部署中運作。</span><span class="sxs-lookup"><span data-stu-id="87cf7-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="87cf7-148">例如，如果您搜尋具有標記部門：IT 的所有專案，無論專案類型、位置或資源群組，搜尋都會返回所有具有該標記的 Azure 專案。</span><span class="sxs-lookup"><span data-stu-id="87cf7-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="87cf7-149">個別標記包含兩個部分：名稱 (選擇性地) *值*。</span><span class="sxs-lookup"><span data-stu-id="87cf7-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="87cf7-150">例如，在 Department：IT 中，標記名稱為部門，而標記值為 IT。</span><span class="sxs-lookup"><span data-stu-id="87cf7-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="87cf7-151">若要新增標記，請使用類似此的雜湊表格語法，這會建立標記 CalendarYear：2016：-Tag @{Name="CalendarYear";Value="2016"} 若要在同一個命令中新增多個標記，請以逗號分隔個別標記：-Tag @{Name="CalendarYear";Value="2016"}， @{Name="FiscalYear";Value="2017"}</span><span class="sxs-lookup"><span data-stu-id="87cf7-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cf7-152">-確認</span><span class="sxs-lookup"><span data-stu-id="87cf7-152">-Confirm</span></span>
<span data-ttu-id="87cf7-153">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="87cf7-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87cf7-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87cf7-154">-WhatIf</span></span>
<span data-ttu-id="87cf7-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87cf7-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87cf7-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87cf7-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87cf7-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87cf7-157">CommonParameters</span></span>
<span data-ttu-id="87cf7-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="87cf7-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87cf7-159">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="87cf7-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87cf7-160">輸入</span><span class="sxs-lookup"><span data-stu-id="87cf7-160">INPUTS</span></span>

### <span data-ttu-id="87cf7-161">System.String</span><span class="sxs-lookup"><span data-stu-id="87cf7-161">System.String</span></span>

### <span data-ttu-id="87cf7-162">Microsoft.Azure.Commands.NotificationHubs.models.命名空間狀態</span><span class="sxs-lookup"><span data-stu-id="87cf7-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="87cf7-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="87cf7-163">System.Boolean</span></span>

### <span data-ttu-id="87cf7-164">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="87cf7-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="87cf7-165">輸出</span><span class="sxs-lookup"><span data-stu-id="87cf7-165">OUTPUTS</span></span>

### <span data-ttu-id="87cf7-166">Microsoft.Azure.Commands.NotificationHubs.models.命名空間Attributes</span><span class="sxs-lookup"><span data-stu-id="87cf7-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="87cf7-167">筆記</span><span class="sxs-lookup"><span data-stu-id="87cf7-167">NOTES</span></span>

## <span data-ttu-id="87cf7-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="87cf7-168">RELATED LINKS</span></span>

[<span data-ttu-id="87cf7-169">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="87cf7-169">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="87cf7-170">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="87cf7-170">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="87cf7-171">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="87cf7-171">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)


