---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277299"
---
# <span data-ttu-id="aaef7-101">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="aaef7-101">New-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="aaef7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aaef7-102">SYNOPSIS</span></span>
<span data-ttu-id="aaef7-103">建立通知中心命名空間。</span><span class="sxs-lookup"><span data-stu-id="aaef7-103">Creates a notification hub namespace.</span></span>

## <span data-ttu-id="aaef7-104">句法</span><span class="sxs-lookup"><span data-stu-id="aaef7-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aaef7-105">說明</span><span class="sxs-lookup"><span data-stu-id="aaef7-105">DESCRIPTION</span></span>
<span data-ttu-id="aaef7-106">**新的-AzNotificationHubsNamespace** Cmdlet 會建立通知中心命名空間。</span><span class="sxs-lookup"><span data-stu-id="aaef7-106">The **New-AzNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="aaef7-107">命名空間是邏輯容器，可協助您組織和管理通知中樞。</span><span class="sxs-lookup"><span data-stu-id="aaef7-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="aaef7-108">您至少必須有一個通知中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="aaef7-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="aaef7-109">單一命名空間可以存放多個中心。</span><span class="sxs-lookup"><span data-stu-id="aaef7-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="aaef7-110">您可以有多個命名空間來組織您的中樞，或提供特定的個人許可權來管理您的中樞的選取子集。</span><span class="sxs-lookup"><span data-stu-id="aaef7-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="aaef7-111">若要建立命名空間，請確定您指定的是命名空間的唯一名稱;指定命名空間所在的資料中心;然後，指定要將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="aaef7-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="aaef7-112">在命名空間建立之後，您可以使用 New-AzNotificationHubsNamespaceAuthorizationRules Cmdlet 來將授權規則指派給該命名空間。</span><span class="sxs-lookup"><span data-stu-id="aaef7-112">After the namespace has been created you can use the New-AzNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="aaef7-113">授權規則是用來管理命名空間的許可權。</span><span class="sxs-lookup"><span data-stu-id="aaef7-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="aaef7-114">示例</span><span class="sxs-lookup"><span data-stu-id="aaef7-114">EXAMPLES</span></span>

### <span data-ttu-id="aaef7-115">範例1：建立通知中樞</span><span class="sxs-lookup"><span data-stu-id="aaef7-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="aaef7-116">這個命令會建立名為 ContosoPartners 的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="aaef7-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="aaef7-117">該命名空間會位於 [西部美國資料中心]，並指派給 ContosoNotificationsGroup 資源群組。</span><span class="sxs-lookup"><span data-stu-id="aaef7-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="aaef7-118">範例2：使用標記建立通知中樞</span><span class="sxs-lookup"><span data-stu-id="aaef7-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="aaef7-119">這個命令會建立名為 ContosoPartners 的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="aaef7-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="aaef7-120">該命名空間會位於 [西部美國資料中心]，並指派給 ContosoNotificationsGroup 資源群組。</span><span class="sxs-lookup"><span data-stu-id="aaef7-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="aaef7-121">此外，這個命令會建立一個含有名稱物件和值 PartnerOrganizations 的標記，並指派給命名空間。</span><span class="sxs-lookup"><span data-stu-id="aaef7-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="aaef7-122">這可確保您在每次篩選物件都設定為 PartnerOrganizations 的專案時，都會顯示該命名空間。</span><span class="sxs-lookup"><span data-stu-id="aaef7-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="aaef7-123">參數</span><span class="sxs-lookup"><span data-stu-id="aaef7-123">PARAMETERS</span></span>

### <span data-ttu-id="aaef7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaef7-124">-DefaultProfile</span></span>
<span data-ttu-id="aaef7-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="aaef7-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaef7-126">-位置</span><span class="sxs-lookup"><span data-stu-id="aaef7-126">-Location</span></span>
<span data-ttu-id="aaef7-127">指定將主控命名空間的資料中心的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="aaef7-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="aaef7-128">雖然您可以將此參數設定為任何有效的位置，但若要獲得最佳效能，您可能會想要使用靠近使用者的資料中心。</span><span class="sxs-lookup"><span data-stu-id="aaef7-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="aaef7-129">-命名空間</span><span class="sxs-lookup"><span data-stu-id="aaef7-129">-Namespace</span></span>
<span data-ttu-id="aaef7-130">指定新命名空間的名稱。</span><span class="sxs-lookup"><span data-stu-id="aaef7-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="aaef7-131">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="aaef7-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="aaef7-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aaef7-132">-ResourceGroup</span></span>
<span data-ttu-id="aaef7-133">指定要將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="aaef7-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="aaef7-134">資源群組會以協助您輕鬆清點管理和管理的方式來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="aaef7-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="aaef7-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="aaef7-135">-SkuTier</span></span>
<span data-ttu-id="aaef7-136">命名空間的 Sku 層級</span><span class="sxs-lookup"><span data-stu-id="aaef7-136">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="aaef7-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="aaef7-137">-Tag</span></span>
<span data-ttu-id="aaef7-138">指定可用於分類及組織 Azure 專案的名稱-值對。</span><span class="sxs-lookup"><span data-stu-id="aaef7-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="aaef7-139">標記的功能與關鍵字類似，且可在整個部署中運作。</span><span class="sxs-lookup"><span data-stu-id="aaef7-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="aaef7-140">例如，如果您在所有專案中搜尋標籤部：這項搜尋將會傳回所有具有該標記的 Azure 專案，不論專案類型、位置或資源群組為何。</span><span class="sxs-lookup"><span data-stu-id="aaef7-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="aaef7-141">個別標籤由兩個部分組成： *名稱* 與（可選擇） *值*。</span><span class="sxs-lookup"><span data-stu-id="aaef7-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="aaef7-142">例如，在 [部門] 中，標記名稱是 [部門]，而標記值是 [部門]。</span><span class="sxs-lookup"><span data-stu-id="aaef7-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="aaef7-143">若要新增標籤，請使用類似這個的雜湊資料表語法，這會建立 tag CalendarYear：2016：</span><span class="sxs-lookup"><span data-stu-id="aaef7-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

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

### <span data-ttu-id="aaef7-144">-確認</span><span class="sxs-lookup"><span data-stu-id="aaef7-144">-Confirm</span></span>
<span data-ttu-id="aaef7-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aaef7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaef7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaef7-146">-WhatIf</span></span>
<span data-ttu-id="aaef7-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aaef7-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aaef7-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aaef7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaef7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaef7-149">CommonParameters</span></span>
<span data-ttu-id="aaef7-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aaef7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaef7-151">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aaef7-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaef7-152">輸入</span><span class="sxs-lookup"><span data-stu-id="aaef7-152">INPUTS</span></span>

### <span data-ttu-id="aaef7-153">System.object</span><span class="sxs-lookup"><span data-stu-id="aaef7-153">System.String</span></span>

### <span data-ttu-id="aaef7-154">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="aaef7-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="aaef7-155">輸出</span><span class="sxs-lookup"><span data-stu-id="aaef7-155">OUTPUTS</span></span>

### <span data-ttu-id="aaef7-156">NamespaceAttributes 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="aaef7-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="aaef7-157">筆記</span><span class="sxs-lookup"><span data-stu-id="aaef7-157">NOTES</span></span>

## <span data-ttu-id="aaef7-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="aaef7-158">RELATED LINKS</span></span>

[<span data-ttu-id="aaef7-159">AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="aaef7-159">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="aaef7-160">移除-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="aaef7-160">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="aaef7-161">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="aaef7-161">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


