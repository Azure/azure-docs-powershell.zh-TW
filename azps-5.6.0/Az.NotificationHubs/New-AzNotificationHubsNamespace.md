---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 20a4da67030962a238838247a7dcf137208e56b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901737"
---
# <span data-ttu-id="33c47-101">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="33c47-101">New-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="33c47-102">簡介</span><span class="sxs-lookup"><span data-stu-id="33c47-102">SYNOPSIS</span></span>
<span data-ttu-id="33c47-103">建立通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="33c47-103">Creates a notification hub namespace.</span></span>

## <span data-ttu-id="33c47-104">語法</span><span class="sxs-lookup"><span data-stu-id="33c47-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33c47-105">描述</span><span class="sxs-lookup"><span data-stu-id="33c47-105">DESCRIPTION</span></span>
<span data-ttu-id="33c47-106">**New-AzNotificationHubsNamespace** Cmdlet 會建立通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="33c47-106">The **New-AzNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="33c47-107">命名空間是邏輯容器，可協助組織及管理通知中樞。</span><span class="sxs-lookup"><span data-stu-id="33c47-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="33c47-108">您至少必須有一個通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="33c47-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="33c47-109">單一命名空間可以包含多個中樞。</span><span class="sxs-lookup"><span data-stu-id="33c47-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="33c47-110">您可以有多個命名空間來組織中樞，或將管理所選中樞子集的許可權授予特定人員。</span><span class="sxs-lookup"><span data-stu-id="33c47-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="33c47-111">若要建立命名空間，請確定您為命名空間指定唯一名稱;指定命名空間所在的資料中心;，然後指定要指派命名空間的資源群組。</span><span class="sxs-lookup"><span data-stu-id="33c47-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="33c47-112">建立命名空間之後，您可以使用 New-AzNotificationHubsNamespaceAuthorizationRules Cmdlet 將授權規則指派給該命名空間。</span><span class="sxs-lookup"><span data-stu-id="33c47-112">After the namespace has been created you can use the New-AzNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="33c47-113">授權規則可用來管理命名空間的許可權。</span><span class="sxs-lookup"><span data-stu-id="33c47-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="33c47-114">例子</span><span class="sxs-lookup"><span data-stu-id="33c47-114">EXAMPLES</span></span>

### <span data-ttu-id="33c47-115">範例 1：建立通知中樞</span><span class="sxs-lookup"><span data-stu-id="33c47-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="33c47-116">此命令會建立名為 ContosoPartners 的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="33c47-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="33c47-117">命名空間將位於美國西部資料中心，並指派給 ContosoNotificationsGroup 資源群組。</span><span class="sxs-lookup"><span data-stu-id="33c47-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="33c47-118">範例 2：建立包含標記的通知中樞</span><span class="sxs-lookup"><span data-stu-id="33c47-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="33c47-119">此命令會建立名為 ContosoPartners 的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="33c47-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="33c47-120">命名空間將位於美國西部資料中心，並指派給 ContosoNotificationsGroup 資源群組。</span><span class="sxs-lookup"><span data-stu-id="33c47-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="33c47-121">此外，此命令會建立一個標記，其名稱為物件和 PartnerOrganizations 值，並指派給命名空間。</span><span class="sxs-lookup"><span data-stu-id="33c47-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="33c47-122">這可確保每次篩選物件標記設定為 PartnerOrganizations 的專案時，都會顯示命名空間。</span><span class="sxs-lookup"><span data-stu-id="33c47-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="33c47-123">參數</span><span class="sxs-lookup"><span data-stu-id="33c47-123">PARAMETERS</span></span>

### <span data-ttu-id="33c47-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c47-124">-DefaultProfile</span></span>
<span data-ttu-id="33c47-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="33c47-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33c47-126">-位置</span><span class="sxs-lookup"><span data-stu-id="33c47-126">-Location</span></span>
<span data-ttu-id="33c47-127">指定將託管命名空間之資料中心的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="33c47-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="33c47-128">雖然您可以將此參數設定為任何有效的位置，但為了獲得最佳的績效，您可能會想要使用靠近大多數使用者的資料中心。</span><span class="sxs-lookup"><span data-stu-id="33c47-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="33c47-129">-命名空間</span><span class="sxs-lookup"><span data-stu-id="33c47-129">-Namespace</span></span>
<span data-ttu-id="33c47-130">指定新命名空間的名稱。</span><span class="sxs-lookup"><span data-stu-id="33c47-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="33c47-131">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="33c47-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="33c47-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="33c47-132">-ResourceGroup</span></span>
<span data-ttu-id="33c47-133">指定要指派命名空間的資源群組。</span><span class="sxs-lookup"><span data-stu-id="33c47-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="33c47-134">資源群組會以只協助庫存管理和管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="33c47-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="33c47-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="33c47-135">-SkuTier</span></span>
<span data-ttu-id="33c47-136">命名空間的 SKU 層級</span><span class="sxs-lookup"><span data-stu-id="33c47-136">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="33c47-137">-標記</span><span class="sxs-lookup"><span data-stu-id="33c47-137">-Tag</span></span>
<span data-ttu-id="33c47-138">指定可用來分類及組織 Azure 專案的名稱值組。</span><span class="sxs-lookup"><span data-stu-id="33c47-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="33c47-139">標記的運作方式類似關鍵字，而且可在整個部署中運作。</span><span class="sxs-lookup"><span data-stu-id="33c47-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="33c47-140">例如，如果您搜尋具有標記部門：IT 的所有專案，無論專案類型、位置或資源群組，搜尋都會返回所有具有該標記的 Azure 專案。</span><span class="sxs-lookup"><span data-stu-id="33c47-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="33c47-141">個別標記由兩個部分組成： *名稱* ，以及值 ，或者，選擇性地 *是值*。</span><span class="sxs-lookup"><span data-stu-id="33c47-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="33c47-142">例如，在部門：IT 中，標記名稱為部門，而標記值為 IT。</span><span class="sxs-lookup"><span data-stu-id="33c47-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="33c47-143">若要新增標記，請使用類似此的雜湊表格語法，這會建立標記 CalendarYear：2016：</span><span class="sxs-lookup"><span data-stu-id="33c47-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c47-144">-確認</span><span class="sxs-lookup"><span data-stu-id="33c47-144">-Confirm</span></span>
<span data-ttu-id="33c47-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="33c47-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33c47-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33c47-146">-WhatIf</span></span>
<span data-ttu-id="33c47-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="33c47-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33c47-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="33c47-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33c47-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c47-149">CommonParameters</span></span>
<span data-ttu-id="33c47-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="33c47-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c47-151">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="33c47-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c47-152">輸入</span><span class="sxs-lookup"><span data-stu-id="33c47-152">INPUTS</span></span>

### <span data-ttu-id="33c47-153">System.String</span><span class="sxs-lookup"><span data-stu-id="33c47-153">System.String</span></span>

### <span data-ttu-id="33c47-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="33c47-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="33c47-155">輸出</span><span class="sxs-lookup"><span data-stu-id="33c47-155">OUTPUTS</span></span>

### <span data-ttu-id="33c47-156">Microsoft.Azure.Commands.NotificationHubs.models.命名空間Attributes</span><span class="sxs-lookup"><span data-stu-id="33c47-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="33c47-157">筆記</span><span class="sxs-lookup"><span data-stu-id="33c47-157">NOTES</span></span>

## <span data-ttu-id="33c47-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="33c47-158">RELATED LINKS</span></span>

[<span data-ttu-id="33c47-159">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="33c47-159">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="33c47-160">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="33c47-160">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="33c47-161">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="33c47-161">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


