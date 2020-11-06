---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93442236"
---
# <span data-ttu-id="a3c40-101">AzureRM Insights 模組</span><span class="sxs-lookup"><span data-stu-id="a3c40-101">AzureRM.Insights Module</span></span>
## <span data-ttu-id="a3c40-102">說明</span><span class="sxs-lookup"><span data-stu-id="a3c40-102">Description</span></span>
<span data-ttu-id="a3c40-103">本主題顯示 Azure Insights Cmdlet 的說明主題。</span><span class="sxs-lookup"><span data-stu-id="a3c40-103">This topic displays help topics for the Azure Insights Cmdlets.</span></span>

## <span data-ttu-id="a3c40-104">AzureRM Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a3c40-104">AzureRM.Insights Cmdlets</span></span>
### [<span data-ttu-id="a3c40-105">附加 AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a3c40-105">Add-AzureRmAutoscaleSetting</span></span>](Add-AzureRmAutoscaleSetting.md)
<span data-ttu-id="a3c40-106">建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="a3c40-106">Creates an Autoscale setting.</span></span>

### [<span data-ttu-id="a3c40-107">附加 AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="a3c40-107">Add-AzureRmLogAlertRule</span></span>](Add-AzureRmLogAlertRule.md)
<span data-ttu-id="a3c40-108">新增或取代記錄提醒規則。</span><span class="sxs-lookup"><span data-stu-id="a3c40-108">Adds or replaces a log alert rule.</span></span>

### [<span data-ttu-id="a3c40-109">附加 AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="a3c40-109">Add-AzureRmLogProfile</span></span>](Add-AzureRmLogProfile.md)
<span data-ttu-id="a3c40-110">建立新的活動記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="a3c40-110">Creates a new activity log profile.</span></span> <span data-ttu-id="a3c40-111">此設定檔是用來將活動記錄封存至 Azure 儲存空間帳戶，或在相同訂閱中將它資料流程至 Azure 事件中樞。</span><span class="sxs-lookup"><span data-stu-id="a3c40-111">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="a3c40-112">僅支援 **儲存空間** 帳戶標準儲存空間帳戶 (premium 儲存空間帳戶不支援) 。</span><span class="sxs-lookup"><span data-stu-id="a3c40-112">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="a3c40-113">它可能是 ARM 類型或傳統模式。</span><span class="sxs-lookup"><span data-stu-id="a3c40-113">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="a3c40-114">如果它是記錄在儲存空間帳戶中，則儲存活動記錄的成本會以標準的標準儲存費率計費。</span><span class="sxs-lookup"><span data-stu-id="a3c40-114">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="a3c40-115">每個訂閱只能有一個記錄 consequentially 每個訂閱只能使用一個儲存空間帳戶來匯出活動記錄。</span><span class="sxs-lookup"><span data-stu-id="a3c40-115">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="a3c40-116">**事件中心** -每個訂閱只能有一個記錄設定檔 consequentially 每個訂閱只能使用一個事件中樞來匯出活動記錄。</span><span class="sxs-lookup"><span data-stu-id="a3c40-116">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="a3c40-117">如果活動記錄是流入事件中樞，則會套用標準事件中樞定價。</span><span class="sxs-lookup"><span data-stu-id="a3c40-117">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="a3c40-118">在活動記錄檔中，事件可與區域或「全域」相關。</span><span class="sxs-lookup"><span data-stu-id="a3c40-118">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="a3c40-119">[全域] 是指這些事件是地區 agnostics，且與區域無關，事實上大部分事件都屬於這種類別。</span><span class="sxs-lookup"><span data-stu-id="a3c40-119">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="a3c40-120">如果活動記錄設定檔是從入口網站進行設定，則會將 [全域] 與您在使用者介面中選取的任何其他區域一起隱出。</span><span class="sxs-lookup"><span data-stu-id="a3c40-120">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="a3c40-121">使用 Cmdlet 時，"Global" 是「全域」的位置，必須從任何其他區域明確提及。</span><span class="sxs-lookup"><span data-stu-id="a3c40-121">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="a3c40-122">**注意** ：- **在位置中設定「全域」失敗，會導致大部分的活動記錄不會匯出。**</span><span class="sxs-lookup"><span data-stu-id="a3c40-122">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

### [<span data-ttu-id="a3c40-123">附加 AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="a3c40-123">Add-AzureRmMetricAlertRule</span></span>](Add-AzureRmMetricAlertRule.md)
<span data-ttu-id="a3c40-124">新增或更新以公制為基礎的警示規則。</span><span class="sxs-lookup"><span data-stu-id="a3c40-124">Adds or updates a metric-based alert rule.</span></span>

### [<span data-ttu-id="a3c40-125">附加 AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="a3c40-125">Add-AzureRmWebtestAlertRule</span></span>](Add-AzureRmWebtestAlertRule.md)
<span data-ttu-id="a3c40-126">新增或更新 webtest 提醒規則。</span><span class="sxs-lookup"><span data-stu-id="a3c40-126">Adds or updates a webtest alert rule.</span></span>

### [<span data-ttu-id="a3c40-127">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a3c40-127">Disable-AzureRmActivityLogAlert</span></span>](Disable-AzureRmActivityLogAlert.md)
<span data-ttu-id="a3c40-128">停用活動記錄通知並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="a3c40-128">Disables an activity log alert and sets its tags.</span></span>

### [<span data-ttu-id="a3c40-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a3c40-129">Enable-AzureRmActivityLogAlert</span></span>](Enable-AzureRmActivityLogAlert.md)
<span data-ttu-id="a3c40-130">啟用活動記錄通知並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="a3c40-130">Enables an activity log alert and sets its Tags.</span></span>

### [<span data-ttu-id="a3c40-131">AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a3c40-131">Get-AzureRmActionGroup</span></span>](Get-AzureRmActionGroup.md)
<span data-ttu-id="a3c40-132">取得動作群組 (s) 。</span><span class="sxs-lookup"><span data-stu-id="a3c40-132">Gets action group(s).</span></span>

### [<span data-ttu-id="a3c40-133">AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a3c40-133">Get-AzureRmActivityLogAlert</span></span>](Get-AzureRmActivityLogAlert.md)
<span data-ttu-id="a3c40-134">取得一或多個活動記錄通知資源。</span><span class="sxs-lookup"><span data-stu-id="a3c40-134">Gets one or more activity log alert resources.</span></span>

### [<span data-ttu-id="a3c40-135">AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="a3c40-135">Get-AzureRmAlertHistory</span></span>](Get-AzureRmAlertHistory.md)
<span data-ttu-id="a3c40-136">取得預警的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="a3c40-136">Gets the history of alerts.</span></span>

### [<span data-ttu-id="a3c40-137">AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="a3c40-137">Get-AzureRmAlertRule</span></span>](Get-AzureRmAlertRule.md)
<span data-ttu-id="a3c40-138">取得警示規則。</span><span class="sxs-lookup"><span data-stu-id="a3c40-138">Gets alert rules.</span></span>

### [<span data-ttu-id="a3c40-139">AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="a3c40-139">Get-AzureRmAutoscaleHistory</span></span>](Get-AzureRmAutoscaleHistory.md)
<span data-ttu-id="a3c40-140">取得自動縮放歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="a3c40-140">Gets the Autoscale history.</span></span>

### [<span data-ttu-id="a3c40-141">AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a3c40-141">Get-AzureRmAutoscaleSetting</span></span>](Get-AzureRmAutoscaleSetting.md)
<span data-ttu-id="a3c40-142">取得自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="a3c40-142">Gets Autoscale settings.</span></span>

### [<span data-ttu-id="a3c40-143">AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="a3c40-143">Get-AzureRmDiagnosticSetting</span></span>](Get-AzureRmDiagnosticSetting.md)
<span data-ttu-id="a3c40-144">取得已記錄的類別和時間 grains。</span><span class="sxs-lookup"><span data-stu-id="a3c40-144">Gets the logged categories and time grains.</span></span>

### [<span data-ttu-id="a3c40-145">AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="a3c40-145">Get-AzureRmLog</span></span>](Get-AzureRmLog.md)
<span data-ttu-id="a3c40-146">取得事件的記錄。</span><span class="sxs-lookup"><span data-stu-id="a3c40-146">Gets a log of events.</span></span>

### [<span data-ttu-id="a3c40-147">AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="a3c40-147">Get-AzureRmLogProfile</span></span>](Get-AzureRmLogProfile.md)
<span data-ttu-id="a3c40-148">取得記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="a3c40-148">Gets a log profile.</span></span>

### [<span data-ttu-id="a3c40-149">AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="a3c40-149">Get-AzureRmMetric</span></span>](Get-AzureRmMetric.md)
<span data-ttu-id="a3c40-150">取得資源的度量值。</span><span class="sxs-lookup"><span data-stu-id="a3c40-150">Gets the metric values of a resource.</span></span>

### [<span data-ttu-id="a3c40-151">AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="a3c40-151">Get-AzureRmMetricDefinition</span></span>](Get-AzureRmMetricDefinition.md)
<span data-ttu-id="a3c40-152">取得公制定義。</span><span class="sxs-lookup"><span data-stu-id="a3c40-152">Gets metric definitions.</span></span>

### [<span data-ttu-id="a3c40-153">AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="a3c40-153">Get-AzureRmUsage</span></span>](Get-AzureRmUsage.md)
<span data-ttu-id="a3c40-154">取得資源的使用標準。</span><span class="sxs-lookup"><span data-stu-id="a3c40-154">Gets the usage metrics for a resource.</span></span>

### [<span data-ttu-id="a3c40-155">新-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a3c40-155">New-AzureRmActionGroup</span></span>](New-AzureRmActionGroup.md)
<span data-ttu-id="a3c40-156">在記憶體中建立 ActionGroup 參考物件。</span><span class="sxs-lookup"><span data-stu-id="a3c40-156">Creates an ActionGroup reference object in memory.</span></span>

### [<span data-ttu-id="a3c40-157">新-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="a3c40-157">New-AzureRmActionGroupReceiver</span></span>](New-AzureRmActionGroupReceiver.md)
<span data-ttu-id="a3c40-158">建立新的 [動作群組收件者]。</span><span class="sxs-lookup"><span data-stu-id="a3c40-158">Creates an new action group receiver.</span></span>

### [<span data-ttu-id="a3c40-159">新-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="a3c40-159">New-AzureRmActivityLogAlertCondition</span></span>](New-AzureRmActivityLogAlertCondition.md)
<span data-ttu-id="a3c40-160">在記憶體中建立新的活動記錄警示條件物件。</span><span class="sxs-lookup"><span data-stu-id="a3c40-160">Creates an new activity log alert condition object in memory.</span></span>

### [<span data-ttu-id="a3c40-161">新-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="a3c40-161">New-AzureRmAlertRuleEmail</span></span>](New-AzureRmAlertRuleEmail.md)
<span data-ttu-id="a3c40-162">建立警示規則的電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="a3c40-162">Creates an email action for an alert rule.</span></span>

### [<span data-ttu-id="a3c40-163">新-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="a3c40-163">New-AzureRmAlertRuleWebhook</span></span>](New-AzureRmAlertRuleWebhook.md)
<span data-ttu-id="a3c40-164">建立警示規則 webhook。</span><span class="sxs-lookup"><span data-stu-id="a3c40-164">Creates an alert rule webhook.</span></span>

### [<span data-ttu-id="a3c40-165">新-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="a3c40-165">New-AzureRmAutoscaleNotification</span></span>](New-AzureRmAutoscaleNotification.md)
<span data-ttu-id="a3c40-166">建立自動縮放電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="a3c40-166">Creates an Autoscale email notification.</span></span>

### [<span data-ttu-id="a3c40-167">新-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="a3c40-167">New-AzureRmAutoscaleProfile</span></span>](New-AzureRmAutoscaleProfile.md)
<span data-ttu-id="a3c40-168">建立自動縮放設定檔。</span><span class="sxs-lookup"><span data-stu-id="a3c40-168">Creates an Autoscale profile.</span></span>

### [<span data-ttu-id="a3c40-169">新-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="a3c40-169">New-AzureRmAutoscaleRule</span></span>](New-AzureRmAutoscaleRule.md)
<span data-ttu-id="a3c40-170">建立自動縮放規則。</span><span class="sxs-lookup"><span data-stu-id="a3c40-170">Creates an Autoscale rule.</span></span>

### [<span data-ttu-id="a3c40-171">新-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="a3c40-171">New-AzureRmAutoscaleWebhook</span></span>](New-AzureRmAutoscaleWebhook.md)
<span data-ttu-id="a3c40-172">建立自動縮放 webhook。</span><span class="sxs-lookup"><span data-stu-id="a3c40-172">Creates an Autoscale webhook.</span></span>

### [<span data-ttu-id="a3c40-173">移除-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a3c40-173">Remove-AzureRmActionGroup</span></span>](Remove-AzureRmActionGroup.md)
<span data-ttu-id="a3c40-174">移除動作群組。</span><span class="sxs-lookup"><span data-stu-id="a3c40-174">Removes an action group.</span></span>

### [<span data-ttu-id="a3c40-175">移除-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a3c40-175">Remove-AzureRmActivityLogAlert</span></span>](Remove-AzureRmActivityLogAlert.md)
<span data-ttu-id="a3c40-176">移除活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="a3c40-176">Removes an activity log alert.</span></span>

### [<span data-ttu-id="a3c40-177">移除-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="a3c40-177">Remove-AzureRmAlertRule</span></span>](Remove-AzureRmAlertRule.md)
<span data-ttu-id="a3c40-178">移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="a3c40-178">Removes an alert rule.</span></span>

### [<span data-ttu-id="a3c40-179">移除-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a3c40-179">Remove-AzureRmAutoscaleSetting</span></span>](Remove-AzureRmAutoscaleSetting.md)
<span data-ttu-id="a3c40-180">移除自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="a3c40-180">Removes an Autoscale setting.</span></span>

### [<span data-ttu-id="a3c40-181">移除-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="a3c40-181">Remove-AzureRmLogProfile</span></span>](Remove-AzureRmLogProfile.md)
<span data-ttu-id="a3c40-182">移除記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="a3c40-182">Removes a log profile.</span></span>

### [<span data-ttu-id="a3c40-183">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a3c40-183">Set-AzureRmActionGroup</span></span>](Set-AzureRmActionGroup.md)
<span data-ttu-id="a3c40-184">建立新的或更新現有的動作群組。</span><span class="sxs-lookup"><span data-stu-id="a3c40-184">Creates a new or updates an existing action group.</span></span>

### [<span data-ttu-id="a3c40-185">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a3c40-185">Set-AzureRmActivityLogAlert</span></span>](Set-AzureRmActivityLogAlert.md)
<span data-ttu-id="a3c40-186">建立新的或設定現有的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="a3c40-186">Creates a new or sets an existing activity log alert.</span></span>

### [<span data-ttu-id="a3c40-187">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="a3c40-187">Set-AzureRmDiagnosticSetting</span></span>](Set-AzureRmDiagnosticSetting.md)
<span data-ttu-id="a3c40-188">設定資源的記錄和標準設定。</span><span class="sxs-lookup"><span data-stu-id="a3c40-188">Sets the logs and metrics settings for the resource.</span></span>

