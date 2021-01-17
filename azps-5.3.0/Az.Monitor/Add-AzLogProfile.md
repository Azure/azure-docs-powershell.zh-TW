---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: bc0f1a6aacc6188a982fe75fa021bdafdc4e02de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438660"
---
# <span data-ttu-id="4133c-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="4133c-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="4133c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4133c-102">SYNOPSIS</span></span>
<span data-ttu-id="4133c-103">建立新的活動記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="4133c-103">Creates a new activity log profile.</span></span> <span data-ttu-id="4133c-104">此設定檔是用來將活動記錄封存至 Azure 儲存空間帳戶，或在相同訂閱中將它資料流程至 Azure 事件中樞。</span><span class="sxs-lookup"><span data-stu-id="4133c-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="4133c-105">句法</span><span class="sxs-lookup"><span data-stu-id="4133c-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4133c-106">說明</span><span class="sxs-lookup"><span data-stu-id="4133c-106">DESCRIPTION</span></span>
<span data-ttu-id="4133c-107">**AzLogProfile** Cmdlet 會建立記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="4133c-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="4133c-108">僅支援 **儲存空間** 帳戶標準儲存空間帳戶 (premium 儲存空間帳戶不支援) 。</span><span class="sxs-lookup"><span data-stu-id="4133c-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="4133c-109">它可能是 ARM 類型或傳統模式。</span><span class="sxs-lookup"><span data-stu-id="4133c-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="4133c-110">如果它是記錄在儲存空間帳戶中，則儲存活動記錄的成本會以標準的標準儲存費率計費。</span><span class="sxs-lookup"><span data-stu-id="4133c-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="4133c-111">每個訂閱只能有一個記錄 consequentially 每個訂閱只能使用一個儲存空間帳戶來匯出活動記錄。</span><span class="sxs-lookup"><span data-stu-id="4133c-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="4133c-112">**事件中心** -每個訂閱只能有一個記錄設定檔 consequentially 每個訂閱只能使用一個事件中樞來匯出活動記錄。</span><span class="sxs-lookup"><span data-stu-id="4133c-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="4133c-113">如果活動記錄是流入事件中樞，則會套用標準事件中樞定價。</span><span class="sxs-lookup"><span data-stu-id="4133c-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="4133c-114">在活動記錄檔中，事件可與區域或「全域」相關。</span><span class="sxs-lookup"><span data-stu-id="4133c-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="4133c-115">[全域] 是指這些事件是地區 agnostics，且與區域無關，事實上大部分事件都屬於這種類別。</span><span class="sxs-lookup"><span data-stu-id="4133c-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="4133c-116">如果活動記錄設定檔是從入口網站進行設定，則會將 [全域] 與您在使用者介面中選取的任何其他區域一起隱出。</span><span class="sxs-lookup"><span data-stu-id="4133c-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="4133c-117">使用 Cmdlet 時，"Global" 是「全域」的位置，必須從任何其他區域明確提及。</span><span class="sxs-lookup"><span data-stu-id="4133c-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="4133c-118">**注意** ：- **在位置中設定「全域」失敗，會導致大部分的活動記錄不會匯出。**</span><span class="sxs-lookup"><span data-stu-id="4133c-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="4133c-119">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="4133c-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="4133c-120">示例</span><span class="sxs-lookup"><span data-stu-id="4133c-120">EXAMPLES</span></span>

### <span data-ttu-id="4133c-121">範例1：新增記錄設定檔，將符合位置條件的活動記錄匯出至儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="4133c-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="4133c-122">範例2</span><span class="sxs-lookup"><span data-stu-id="4133c-122">Example 2</span></span>

<span data-ttu-id="4133c-123">建立新的活動記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="4133c-123">Creates a new activity log profile.</span></span> <span data-ttu-id="4133c-124"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="4133c-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="4133c-125">參數</span><span class="sxs-lookup"><span data-stu-id="4133c-125">PARAMETERS</span></span>

### <span data-ttu-id="4133c-126">-類別</span><span class="sxs-lookup"><span data-stu-id="4133c-126">-Category</span></span>
<span data-ttu-id="4133c-127">指定類別清單。</span><span class="sxs-lookup"><span data-stu-id="4133c-127">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="4133c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4133c-128">-DefaultProfile</span></span>
<span data-ttu-id="4133c-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4133c-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4133c-130">-位置</span><span class="sxs-lookup"><span data-stu-id="4133c-130">-Location</span></span>
<span data-ttu-id="4133c-131">指定記錄設定檔的位置。</span><span class="sxs-lookup"><span data-stu-id="4133c-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="4133c-132">有效值：請在下方執行 Cmdlet，以取得最新的位置清單。</span><span class="sxs-lookup"><span data-stu-id="4133c-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="4133c-133">Get-AzLocation |選取 DisplayName</span><span class="sxs-lookup"><span data-stu-id="4133c-133">Get-AzLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="4133c-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="4133c-134">-Name</span></span>
<span data-ttu-id="4133c-135">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="4133c-135">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="4133c-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4133c-136">-RetentionInDays</span></span>
<span data-ttu-id="4133c-137">指定保留原則（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="4133c-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="4133c-138">這是記錄在指定的儲存空間帳戶中保留的天數。</span><span class="sxs-lookup"><span data-stu-id="4133c-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="4133c-139">若要永久保留資料，請將此設定為 **0**。</span><span class="sxs-lookup"><span data-stu-id="4133c-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="4133c-140">如果沒有指定，則預設為 **0**。</span><span class="sxs-lookup"><span data-stu-id="4133c-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="4133c-141">一般標準儲存或活動中心帳單費用會套用到資料保留。</span><span class="sxs-lookup"><span data-stu-id="4133c-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="4133c-142">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="4133c-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="4133c-143">指定服務匯流排規則的 ID。</span><span class="sxs-lookup"><span data-stu-id="4133c-143">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="4133c-144">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4133c-144">-StorageAccountId</span></span>
<span data-ttu-id="4133c-145">指定儲存空間帳戶的 ID。</span><span class="sxs-lookup"><span data-stu-id="4133c-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="4133c-146">[識別碼] 是儲存帳戶的完全合格的資源識別碼（例如</span><span class="sxs-lookup"><span data-stu-id="4133c-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="4133c-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="4133c-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="4133c-148">-確認</span><span class="sxs-lookup"><span data-stu-id="4133c-148">-Confirm</span></span>
<span data-ttu-id="4133c-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4133c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4133c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4133c-150">-WhatIf</span></span>
<span data-ttu-id="4133c-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4133c-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4133c-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4133c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4133c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4133c-153">CommonParameters</span></span>
<span data-ttu-id="4133c-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4133c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4133c-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4133c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4133c-156">輸入</span><span class="sxs-lookup"><span data-stu-id="4133c-156">INPUTS</span></span>

### <span data-ttu-id="4133c-157">System.object</span><span class="sxs-lookup"><span data-stu-id="4133c-157">System.String</span></span>

### <span data-ttu-id="4133c-158">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4133c-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4133c-159">[System.object]。清單 ' 1 [CoreLib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4133c-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4133c-160">輸出</span><span class="sxs-lookup"><span data-stu-id="4133c-160">OUTPUTS</span></span>

### <span data-ttu-id="4133c-161">PSLogProfile 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="4133c-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="4133c-162">筆記</span><span class="sxs-lookup"><span data-stu-id="4133c-162">NOTES</span></span>

## <span data-ttu-id="4133c-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="4133c-163">RELATED LINKS</span></span>

[<span data-ttu-id="4133c-164">AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="4133c-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="4133c-165">移除-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="4133c-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


