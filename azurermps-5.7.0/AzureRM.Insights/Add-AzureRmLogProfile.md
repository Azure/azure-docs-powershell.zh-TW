---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 0ef53015b3e07eeb69cdcfd0ab70c67317ab92cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456208"
---
# <span data-ttu-id="2f905-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="2f905-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="2f905-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f905-102">SYNOPSIS</span></span>
<span data-ttu-id="2f905-103">建立新的活動記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="2f905-103">Creates a new activity log profile.</span></span> <span data-ttu-id="2f905-104">此設定檔是用來將活動記錄封存至 Azure 儲存空間帳戶，或在相同訂閱中將它資料流程至 Azure 事件中樞。</span><span class="sxs-lookup"><span data-stu-id="2f905-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f905-105">句法</span><span class="sxs-lookup"><span data-stu-id="2f905-105">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f905-106">說明</span><span class="sxs-lookup"><span data-stu-id="2f905-106">DESCRIPTION</span></span>
<span data-ttu-id="2f905-107">**AzureRmLogProfile** Cmdlet 會建立記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="2f905-107">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

- <span data-ttu-id="2f905-108">僅支援 **儲存空間** 帳戶標準儲存空間帳戶 (premium 儲存空間帳戶不支援) 。</span><span class="sxs-lookup"><span data-stu-id="2f905-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="2f905-109">它可能是 ARM 類型或傳統模式。</span><span class="sxs-lookup"><span data-stu-id="2f905-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="2f905-110">如果它是記錄在儲存空間帳戶中，則儲存活動記錄的成本會以標準的標準儲存費率計費。</span><span class="sxs-lookup"><span data-stu-id="2f905-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="2f905-111">每個訂閱只能有一個記錄 consequentially 每個訂閱只能使用一個儲存空間帳戶來匯出活動記錄。</span><span class="sxs-lookup"><span data-stu-id="2f905-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="2f905-112">**事件中心** -每個訂閱只能有一個記錄設定檔 consequentially 每個訂閱只能使用一個事件中樞來匯出活動記錄。</span><span class="sxs-lookup"><span data-stu-id="2f905-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="2f905-113">如果活動記錄是流入事件中樞，則會套用標準事件中樞定價。</span><span class="sxs-lookup"><span data-stu-id="2f905-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="2f905-114">在活動記錄檔中，事件可與區域或「全域」相關。</span><span class="sxs-lookup"><span data-stu-id="2f905-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="2f905-115">[全域] 是指這些事件是地區 agnostics，且與區域無關，事實上大部分事件都屬於這種類別。</span><span class="sxs-lookup"><span data-stu-id="2f905-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="2f905-116">如果活動記錄設定檔是從入口網站進行設定，則會將 [全域] 與您在使用者介面中選取的任何其他區域一起隱出。</span><span class="sxs-lookup"><span data-stu-id="2f905-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="2f905-117">使用 Cmdlet 時，"Global" 是「全域」的位置，必須從任何其他區域明確提及。</span><span class="sxs-lookup"><span data-stu-id="2f905-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="2f905-118">**注意** ：- **在位置中設定「全域」失敗，會導致大部分的活動記錄不會匯出。**</span><span class="sxs-lookup"><span data-stu-id="2f905-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

<span data-ttu-id="2f905-119">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="2f905-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="2f905-120">示例</span><span class="sxs-lookup"><span data-stu-id="2f905-120">EXAMPLES</span></span>

### <span data-ttu-id="2f905-121">範例1：新增記錄設定檔，將符合位置條件的活動記錄匯出至儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="2f905-121">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="2f905-122">參數</span><span class="sxs-lookup"><span data-stu-id="2f905-122">PARAMETERS</span></span>

### <span data-ttu-id="2f905-123">-類別</span><span class="sxs-lookup"><span data-stu-id="2f905-123">-Category</span></span>
<span data-ttu-id="2f905-124">指定類別清單。</span><span class="sxs-lookup"><span data-stu-id="2f905-124">Specifies the list of categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Categories

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f905-125">-DefaultProfile</span></span>
<span data-ttu-id="2f905-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2f905-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-127">-位置</span><span class="sxs-lookup"><span data-stu-id="2f905-127">-Location</span></span>
<span data-ttu-id="2f905-128">指定記錄設定檔的位置。</span><span class="sxs-lookup"><span data-stu-id="2f905-128">Specifies the location of the log profile.</span></span>
<span data-ttu-id="2f905-129">有效值：請在下方執行 Cmdlet，以取得最新的位置清單。</span><span class="sxs-lookup"><span data-stu-id="2f905-129">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="2f905-130">Get-AzureLocation |選取 DisplayName</span><span class="sxs-lookup"><span data-stu-id="2f905-130">Get-AzureLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Locations

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f905-131">-Name</span></span>
<span data-ttu-id="2f905-132">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f905-132">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2f905-133">-RetentionInDays</span></span>
<span data-ttu-id="2f905-134">指定保留原則（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f905-134">Specifies the retention policy, in days.</span></span> <span data-ttu-id="2f905-135">這是記錄在指定的儲存空間帳戶中保留的天數。</span><span class="sxs-lookup"><span data-stu-id="2f905-135">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="2f905-136">若要永久保留資料，請將此設定為 **0** 。</span><span class="sxs-lookup"><span data-stu-id="2f905-136">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="2f905-137">如果沒有指定，則預設為 **0** 。</span><span class="sxs-lookup"><span data-stu-id="2f905-137">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="2f905-138">一般標準儲存或活動中心帳單費用會套用到資料保留。</span><span class="sxs-lookup"><span data-stu-id="2f905-138">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-139">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="2f905-139">-ServiceBusRuleId</span></span>
<span data-ttu-id="2f905-140">指定服務匯流排規則的 ID。</span><span class="sxs-lookup"><span data-stu-id="2f905-140">Specifies the ID of the Service Bus rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2f905-141">-StorageAccountId</span></span>
<span data-ttu-id="2f905-142">指定儲存空間帳戶的 ID。</span><span class="sxs-lookup"><span data-stu-id="2f905-142">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="2f905-143">[識別碼] 是儲存帳戶的完全合格的資源識別碼（例如</span><span class="sxs-lookup"><span data-stu-id="2f905-143">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="2f905-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="2f905-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f905-145">CommonParameters</span></span>
<span data-ttu-id="2f905-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f905-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f905-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f905-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f905-148">輸入</span><span class="sxs-lookup"><span data-stu-id="2f905-148">INPUTS</span></span>

### <span data-ttu-id="2f905-149">所有</span><span class="sxs-lookup"><span data-stu-id="2f905-149">None</span></span>
<span data-ttu-id="2f905-150">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2f905-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f905-151">輸出</span><span class="sxs-lookup"><span data-stu-id="2f905-151">OUTPUTS</span></span>

### <span data-ttu-id="2f905-152">PSLogProfile 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="2f905-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="2f905-153">筆記</span><span class="sxs-lookup"><span data-stu-id="2f905-153">NOTES</span></span>

## <span data-ttu-id="2f905-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f905-154">RELATED LINKS</span></span>

[<span data-ttu-id="2f905-155">AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="2f905-155">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="2f905-156">移除-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="2f905-156">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


