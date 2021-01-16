---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277268"
---
# <span data-ttu-id="0a374-101">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0a374-101">Set-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="0a374-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a374-102">SYNOPSIS</span></span>
<span data-ttu-id="0a374-103">設定通知中心命名空間的屬性值。</span><span class="sxs-lookup"><span data-stu-id="0a374-103">Sets property values for a notification hub namespace.</span></span>

## <span data-ttu-id="0a374-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a374-104">SYNTAX</span></span>

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a374-105">說明</span><span class="sxs-lookup"><span data-stu-id="0a374-105">DESCRIPTION</span></span>
<span data-ttu-id="0a374-106">**AzNotificationHubsNamespace** Cmdlet 會設定現有通知中心命名空間的屬性值。</span><span class="sxs-lookup"><span data-stu-id="0a374-106">The **Set-AzNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="0a374-107">命名空間是邏輯容器，可協助您組織和管理通知中樞。</span><span class="sxs-lookup"><span data-stu-id="0a374-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="0a374-108">您至少必須有一個通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="0a374-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="0a374-109">此外，所有通知中樞都必須有指派的命名空間。</span><span class="sxs-lookup"><span data-stu-id="0a374-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="0a374-110">這個 Cmdlet 主要是用來啟用和停用命名空間。</span><span class="sxs-lookup"><span data-stu-id="0a374-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="0a374-111">當命名空間停用時，使用者無法連線到命名空間中的任何通知中樞，也不能使用這些中樞傳送推播通知。</span><span class="sxs-lookup"><span data-stu-id="0a374-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="0a374-112">若要重新啟用停用的命名空間，請使用此 Cmdlet 將命名空間的 **State** 屬性設定為 [作用中]。</span><span class="sxs-lookup"><span data-stu-id="0a374-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="0a374-113">您也可以使用此 Cmdlet 將命名空間標記為重要。</span><span class="sxs-lookup"><span data-stu-id="0a374-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="0a374-114">這可防止刪除命名空間。</span><span class="sxs-lookup"><span data-stu-id="0a374-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="0a374-115">若要移除重要的命名空間，您必須先移除 [重要] 標籤。</span><span class="sxs-lookup"><span data-stu-id="0a374-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="0a374-116">示例</span><span class="sxs-lookup"><span data-stu-id="0a374-116">EXAMPLES</span></span>

### <span data-ttu-id="0a374-117">範例1：停用命名空間</span><span class="sxs-lookup"><span data-stu-id="0a374-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="0a374-118">這個命令會停用位於 [美國西部] 資料中心並指派給 ContosoNotificationsGroup 資源群組的命名空間 ContosoPartners。</span><span class="sxs-lookup"><span data-stu-id="0a374-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="0a374-119">範例2：啟用命名空間</span><span class="sxs-lookup"><span data-stu-id="0a374-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="0a374-120">這個命令會啟用位於西部美國資料中心並指派給 ContosoNotificationsGroup 資源群組的命名空間 ContosoPartners。</span><span class="sxs-lookup"><span data-stu-id="0a374-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="0a374-121">參數</span><span class="sxs-lookup"><span data-stu-id="0a374-121">PARAMETERS</span></span>

### <span data-ttu-id="0a374-122">-重要</span><span class="sxs-lookup"><span data-stu-id="0a374-122">-Critical</span></span>
<span data-ttu-id="0a374-123">指出命名空間是否為關鍵命名空間。</span><span class="sxs-lookup"><span data-stu-id="0a374-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="0a374-124">無法刪除關鍵命名空間。</span><span class="sxs-lookup"><span data-stu-id="0a374-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="0a374-125">若要刪除關鍵命名空間，您必須將此屬性的值設為 False，才能將命名空間標示為非重要。</span><span class="sxs-lookup"><span data-stu-id="0a374-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

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

### <span data-ttu-id="0a374-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a374-126">-DefaultProfile</span></span>
<span data-ttu-id="0a374-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0a374-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a374-128">-Force</span><span class="sxs-lookup"><span data-stu-id="0a374-128">-Force</span></span>
<span data-ttu-id="0a374-129">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="0a374-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0a374-130">-位置</span><span class="sxs-lookup"><span data-stu-id="0a374-130">-Location</span></span>
<span data-ttu-id="0a374-131">指定承載命名空間的資料中心的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0a374-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="0a374-132">雖然您可以將此參數設定為任何有效的 Azure 位置，但若要獲得最佳效能，您應該使用接近大多數使用者的資料中心。</span><span class="sxs-lookup"><span data-stu-id="0a374-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="0a374-133">若要取得最新的 Azure 位置清單，請執行下列命令： `Get-AzLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="0a374-133">To get an up-to-date list of Azure locations run the following command: `Get-AzLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="0a374-134">-命名空間</span><span class="sxs-lookup"><span data-stu-id="0a374-134">-Namespace</span></span>
<span data-ttu-id="0a374-135">指定此 Cmdlet 修改的命名空間。</span><span class="sxs-lookup"><span data-stu-id="0a374-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="0a374-136">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="0a374-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="0a374-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0a374-137">-ResourceGroup</span></span>
<span data-ttu-id="0a374-138">指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="0a374-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="0a374-139">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="0a374-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="0a374-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="0a374-140">-SkuTier</span></span>
<span data-ttu-id="0a374-141">命名空間的 Sku 層級</span><span class="sxs-lookup"><span data-stu-id="0a374-141">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="0a374-142">-State</span><span class="sxs-lookup"><span data-stu-id="0a374-142">-State</span></span>
<span data-ttu-id="0a374-143">指定命名空間的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0a374-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="0a374-144">此參數可接受的值為： [作用中] 和 [已停用]。</span><span class="sxs-lookup"><span data-stu-id="0a374-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

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

### <span data-ttu-id="0a374-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a374-145">-Tag</span></span>
<span data-ttu-id="0a374-146">指定可用於分類及組織 Azure 專案的名稱-值對。</span><span class="sxs-lookup"><span data-stu-id="0a374-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="0a374-147">標記的功能與關鍵字類似，且可在整個部署中運作。</span><span class="sxs-lookup"><span data-stu-id="0a374-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="0a374-148">例如，如果您在所有專案中搜尋標籤部：這項搜尋將會傳回所有具有該標記的 Azure 專案，不論專案類型、位置或資源群組為何。</span><span class="sxs-lookup"><span data-stu-id="0a374-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="0a374-149">個別標記由兩個部分組成： [ *名稱* ] 和 [ (] 可選擇) *值*。</span><span class="sxs-lookup"><span data-stu-id="0a374-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="0a374-150">例如，在 [部門]： IT 中，標籤名稱是 [部門]，而 tag 值則是。</span><span class="sxs-lookup"><span data-stu-id="0a374-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="0a374-151">若要新增標籤，請使用類似這個的雜湊表語法，這會建立標記 CalendarYear：2016：-Tags @ {Name = "CalendarYear";值 = "2016"} 若要在相同的命令中新增多個標籤，請使用逗號分隔個別的標記：-Tag @ {Name = "CalendarYear";值 = "2016"}，@ {Name = "FiscalYear";Value = "2017"}</span><span class="sxs-lookup"><span data-stu-id="0a374-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

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

### <span data-ttu-id="0a374-152">-確認</span><span class="sxs-lookup"><span data-stu-id="0a374-152">-Confirm</span></span>
<span data-ttu-id="0a374-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0a374-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a374-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a374-154">-WhatIf</span></span>
<span data-ttu-id="0a374-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a374-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a374-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a374-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a374-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a374-157">CommonParameters</span></span>
<span data-ttu-id="0a374-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a374-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a374-159">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a374-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a374-160">輸入</span><span class="sxs-lookup"><span data-stu-id="0a374-160">INPUTS</span></span>

### <span data-ttu-id="0a374-161">System.object</span><span class="sxs-lookup"><span data-stu-id="0a374-161">System.String</span></span>

### <span data-ttu-id="0a374-162">NamespaceState 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="0a374-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="0a374-163">System.object</span><span class="sxs-lookup"><span data-stu-id="0a374-163">System.Boolean</span></span>

### <span data-ttu-id="0a374-164">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0a374-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0a374-165">輸出</span><span class="sxs-lookup"><span data-stu-id="0a374-165">OUTPUTS</span></span>

### <span data-ttu-id="0a374-166">NamespaceAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="0a374-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="0a374-167">筆記</span><span class="sxs-lookup"><span data-stu-id="0a374-167">NOTES</span></span>

## <span data-ttu-id="0a374-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a374-168">RELATED LINKS</span></span>

[<span data-ttu-id="0a374-169">AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0a374-169">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="0a374-170">新-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0a374-170">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="0a374-171">移除-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0a374-171">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)


