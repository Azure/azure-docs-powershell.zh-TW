---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 40efc9e6afbb4f1424fcbcfe70e3376eb9ab5a23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456604"
---
# <span data-ttu-id="493d7-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="493d7-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="493d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="493d7-102">SYNOPSIS</span></span>
<span data-ttu-id="493d7-103">建立新的活動記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="493d7-103">Creates a new activity log profile.</span></span> <span data-ttu-id="493d7-104">此設定檔是用來將活動記錄封存至 Azure 儲存空間帳戶，或在相同訂閱中將它資料流程至 Azure 事件中樞。</span><span class="sxs-lookup"><span data-stu-id="493d7-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="493d7-105">僅支援 **儲存空間** 帳戶標準儲存空間帳戶 (premium 儲存空間帳戶不支援) 。</span><span class="sxs-lookup"><span data-stu-id="493d7-105">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="493d7-106">它可能是 ARM 類型或傳統模式。</span><span class="sxs-lookup"><span data-stu-id="493d7-106">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="493d7-107">如果它是記錄在儲存空間帳戶中，則儲存活動記錄的成本會以標準的標準儲存費率計費。</span><span class="sxs-lookup"><span data-stu-id="493d7-107">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="493d7-108">每個訂閱只能有一個記錄 consequentially 每個訂閱只能使用一個儲存空間帳戶來匯出活動記錄。</span><span class="sxs-lookup"><span data-stu-id="493d7-108">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="493d7-109">**事件中心** -每個訂閱只能有一個記錄設定檔 consequentially 每個訂閱只能使用一個事件中樞來匯出活動記錄。</span><span class="sxs-lookup"><span data-stu-id="493d7-109">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="493d7-110">如果活動記錄是流入事件中樞，則會套用標準事件中樞定價。</span><span class="sxs-lookup"><span data-stu-id="493d7-110">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="493d7-111">在活動記錄檔中，事件可與區域或「全域」相關。</span><span class="sxs-lookup"><span data-stu-id="493d7-111">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="493d7-112">[全域] 是指這些事件是地區 agnostics，且與區域無關，事實上大部分事件都屬於這種類別。</span><span class="sxs-lookup"><span data-stu-id="493d7-112">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="493d7-113">如果活動記錄設定檔是從入口網站進行設定，則會將 [全域] 與您在使用者介面中選取的任何其他區域一起隱出。</span><span class="sxs-lookup"><span data-stu-id="493d7-113">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="493d7-114">使用 Cmdlet 時，"Global" 是「全域」的位置，必須從任何其他區域明確提及。</span><span class="sxs-lookup"><span data-stu-id="493d7-114">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="493d7-115">**注意** ：- **在位置中設定「全域」失敗，會導致大部分的活動記錄不會匯出。**</span><span class="sxs-lookup"><span data-stu-id="493d7-115">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="493d7-116">句法</span><span class="sxs-lookup"><span data-stu-id="493d7-116">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Locations <System.Collections.Generic.List`1[System.String]>
 [-Categories <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="493d7-117">說明</span><span class="sxs-lookup"><span data-stu-id="493d7-117">DESCRIPTION</span></span>
<span data-ttu-id="493d7-118">**AzureRmLogProfile** Cmdlet 會建立記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="493d7-118">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

## <span data-ttu-id="493d7-119">示例</span><span class="sxs-lookup"><span data-stu-id="493d7-119">EXAMPLES</span></span>

### <span data-ttu-id="493d7-120">範例1：新增記錄設定檔，將符合位置條件的活動記錄匯出至儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="493d7-120">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="493d7-121">參數</span><span class="sxs-lookup"><span data-stu-id="493d7-121">PARAMETERS</span></span>

### <span data-ttu-id="493d7-122">-類別</span><span class="sxs-lookup"><span data-stu-id="493d7-122">-Categories</span></span>
<span data-ttu-id="493d7-123">指定類別清單。</span><span class="sxs-lookup"><span data-stu-id="493d7-123">Specifies the list of categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="493d7-124">-位置</span><span class="sxs-lookup"><span data-stu-id="493d7-124">-Locations</span></span>
<span data-ttu-id="493d7-125">指定記錄設定檔的位置。</span><span class="sxs-lookup"><span data-stu-id="493d7-125">Specifies the location of the log profile.</span></span>
<span data-ttu-id="493d7-126">有效值：請在下方執行 Cmdlet，以取得最新的位置清單。</span><span class="sxs-lookup"><span data-stu-id="493d7-126">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="493d7-127">Get-AzureLocation |選取 DisplayName</span><span class="sxs-lookup"><span data-stu-id="493d7-127">Get-AzureLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="493d7-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="493d7-128">-Name</span></span>
<span data-ttu-id="493d7-129">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="493d7-129">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="493d7-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="493d7-130">-RetentionInDays</span></span>
<span data-ttu-id="493d7-131">指定保留原則（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="493d7-131">Specifies the retention policy, in days.</span></span> <span data-ttu-id="493d7-132">這是記錄在指定的儲存空間帳戶中保留的天數。</span><span class="sxs-lookup"><span data-stu-id="493d7-132">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="493d7-133">若要永久保留資料，請將此設定為 **0** 。</span><span class="sxs-lookup"><span data-stu-id="493d7-133">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="493d7-134">如果沒有指定，則預設為 **0** 。</span><span class="sxs-lookup"><span data-stu-id="493d7-134">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="493d7-135">一般標準儲存或活動中心帳單費用會套用到資料保留。</span><span class="sxs-lookup"><span data-stu-id="493d7-135">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="493d7-136">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="493d7-136">-ServiceBusRuleId</span></span>
<span data-ttu-id="493d7-137">指定服務匯流排規則的 ID。</span><span class="sxs-lookup"><span data-stu-id="493d7-137">Specifies the ID of the Service Bus rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="493d7-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="493d7-138">-StorageAccountId</span></span>
<span data-ttu-id="493d7-139">指定儲存空間帳戶的 ID。</span><span class="sxs-lookup"><span data-stu-id="493d7-139">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="493d7-140">[識別碼] 是儲存帳戶的完全合格的資源識別碼（例如</span><span class="sxs-lookup"><span data-stu-id="493d7-140">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="493d7-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="493d7-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="493d7-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493d7-142">-DefaultProfile</span></span>
<span data-ttu-id="493d7-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="493d7-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="493d7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493d7-144">CommonParameters</span></span>
<span data-ttu-id="493d7-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="493d7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493d7-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="493d7-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493d7-147">輸入</span><span class="sxs-lookup"><span data-stu-id="493d7-147">INPUTS</span></span>

## <span data-ttu-id="493d7-148">輸出</span><span class="sxs-lookup"><span data-stu-id="493d7-148">OUTPUTS</span></span>

### <span data-ttu-id="493d7-149">PSLogProfile 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="493d7-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="493d7-150">筆記</span><span class="sxs-lookup"><span data-stu-id="493d7-150">NOTES</span></span>

## <span data-ttu-id="493d7-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="493d7-151">RELATED LINKS</span></span>

[<span data-ttu-id="493d7-152">AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="493d7-152">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="493d7-153">移除-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="493d7-153">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


