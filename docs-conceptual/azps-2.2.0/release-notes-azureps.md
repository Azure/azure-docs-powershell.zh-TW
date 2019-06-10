---
ms.openlocfilehash: 911e1f7ff56feab2735f397a0128aab4aa7757c7
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498670"
---
## <a name="220---june-2019"></a><span data-ttu-id="a33e4-101">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-101">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="a33e4-102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a33e4-102">Az.Cdn</span></span>
* <span data-ttu-id="a33e4-103">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="a33e4-103">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a33e4-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-104">Az.Compute</span></span>
* <span data-ttu-id="a33e4-105">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="a33e4-105">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="a33e4-106">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a33e4-106">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a33e4-107">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a33e4-107">Az.EventHub</span></span>
* <span data-ttu-id="a33e4-108">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="a33e4-108">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="a33e4-109">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a33e4-109">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a33e4-110">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a33e4-110">Az.Network</span></span>
* <span data-ttu-id="a33e4-111">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="a33e4-111">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="a33e4-112">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="a33e4-112">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a33e4-113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a33e4-113">Az.PolicyInsights</span></span>
* <span data-ttu-id="a33e4-114">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-114">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a33e4-115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-115">Az.RecoveryServices</span></span>
* <span data-ttu-id="a33e4-116">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="a33e4-116">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a33e4-117">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a33e4-117">Az.ServiceBus</span></span>
* <span data-ttu-id="a33e4-118">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a33e4-118">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a33e4-119">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a33e4-119">Az.ServiceFabric</span></span>
* <span data-ttu-id="a33e4-120">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="a33e4-120">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="a33e4-121">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="a33e4-121">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="a33e4-122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a33e4-122">Az.Sql</span></span>
* <span data-ttu-id="a33e4-123">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="a33e4-123">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="a33e4-124">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-124">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a33e4-125">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="a33e4-125">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="a33e4-126">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="a33e4-126">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a33e4-127">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a33e4-127">Az.Websites</span></span>
* <span data-ttu-id="a33e4-128">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-128">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="a33e4-129">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-129">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a33e4-130">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a33e4-130">Az.ApiManagement</span></span>
* <span data-ttu-id="a33e4-131">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="a33e4-131">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="a33e4-132">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="a33e4-132">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="a33e4-133">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="a33e4-133">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="a33e4-134">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="a33e4-134">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="a33e4-135">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="a33e4-135">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="a33e4-136">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="a33e4-136">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="a33e4-137">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="a33e4-137">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="a33e4-138">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="a33e4-138">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="a33e4-139">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="a33e4-139">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="a33e4-140">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="a33e4-140">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="a33e4-141">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="a33e4-141">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="a33e4-142">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="a33e4-142">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="a33e4-143">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="a33e4-143">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="a33e4-144">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="a33e4-144">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="a33e4-145">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="a33e4-145">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="a33e4-146">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="a33e4-146">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="a33e4-147">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="a33e4-147">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="a33e4-148">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="a33e4-148">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="a33e4-149">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="a33e4-149">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="a33e4-150">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="a33e4-150">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="a33e4-151">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="a33e4-151">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="a33e4-152">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="a33e4-152">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="a33e4-153">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="a33e4-153">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="a33e4-154">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="a33e4-154">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="a33e4-155">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-155">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="a33e4-156">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-156">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="a33e4-157">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="a33e4-157">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="a33e4-158">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="a33e4-158">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="a33e4-159">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="a33e4-159">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="a33e4-160">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="a33e4-160">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="a33e4-161">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="a33e4-161">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="a33e4-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="a33e4-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="a33e4-163">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="a33e4-163">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="a33e4-164">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a33e4-164">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a33e4-165">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="a33e4-165">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="a33e4-166">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="a33e4-166">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="a33e4-167">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="a33e4-167">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="a33e4-168">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="a33e4-168">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="a33e4-169">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="a33e4-169">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="a33e4-170">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a33e4-170">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="a33e4-171">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="a33e4-171">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a33e4-172">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="a33e4-172">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a33e4-173">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="a33e4-173">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="a33e4-174">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="a33e4-174">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="a33e4-175">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a33e4-175">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a33e4-176">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="a33e4-176">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a33e4-177">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="a33e4-177">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="a33e4-178">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="a33e4-178">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="a33e4-179">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="a33e4-179">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="a33e4-180">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="a33e4-180">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="a33e4-181">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="a33e4-181">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="a33e4-182">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="a33e4-182">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="a33e4-183">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="a33e4-183">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="a33e4-184">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="a33e4-184">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="a33e4-185">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="a33e4-185">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="a33e4-186">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="a33e4-186">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="a33e4-187">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a33e4-187">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a33e4-188">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="a33e4-188">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a33e4-189">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="a33e4-189">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a33e4-190">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="a33e4-190">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a33e4-191">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a33e4-191">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a33e4-192">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="a33e4-192">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a33e4-193">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="a33e4-193">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a33e4-194">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="a33e4-194">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a33e4-195">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="a33e4-195">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="a33e4-196">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="a33e4-196">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="a33e4-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="a33e4-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="a33e4-198">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="a33e4-198">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="a33e4-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="a33e4-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="a33e4-200">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a33e4-200">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="a33e4-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="a33e4-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="a33e4-202">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="a33e4-202">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="a33e4-203">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="a33e4-203">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="a33e4-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="a33e4-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="a33e4-205">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="a33e4-205">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="a33e4-206">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a33e4-206">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="a33e4-207">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="a33e4-207">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a33e4-208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a33e4-208">Az.Automation</span></span>
* <span data-ttu-id="a33e4-209">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="a33e4-209">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="a33e4-210">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-210">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="a33e4-211">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-211">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="a33e4-212">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="a33e4-212">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="a33e4-213">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-213">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="a33e4-214">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="a33e4-214">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="a33e4-215">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="a33e4-215">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a33e4-216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-216">Az.Compute</span></span>
* <span data-ttu-id="a33e4-217">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a33e4-217">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="a33e4-218">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="a33e4-218">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a33e4-219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a33e4-219">Az.DataLakeStore</span></span>
* <span data-ttu-id="a33e4-220">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="a33e4-220">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a33e4-221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a33e4-221">Az.Monitor</span></span>
* <span data-ttu-id="a33e4-222">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="a33e4-222">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a33e4-223">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a33e4-223">Az.Network</span></span>
* <span data-ttu-id="a33e4-224">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="a33e4-224">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="a33e4-225">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="a33e4-225">Updated cmdlet:</span></span>
        - <span data-ttu-id="a33e4-226">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a33e4-226">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="a33e4-227">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="a33e4-227">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="a33e4-228">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-228">Az.Resources</span></span>
* <span data-ttu-id="a33e4-229">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="a33e4-229">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="a33e4-230">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a33e4-230">Az.Sql</span></span>
* <span data-ttu-id="a33e4-231">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="a33e4-231">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="a33e4-232">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-232">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a33e4-233">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a33e4-233">Az.Accounts</span></span>
* <span data-ttu-id="a33e4-234">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-234">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a33e4-235">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-235">Az.CognitiveServices</span></span>
* <span data-ttu-id="a33e4-236">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="a33e4-236">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="a33e4-237">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a33e4-237">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a33e4-238">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-238">Az.Compute</span></span>
* <span data-ttu-id="a33e4-239">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="a33e4-239">Proximity placement group feature.</span></span>
    - <span data-ttu-id="a33e4-240">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a33e4-240">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="a33e4-241">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a33e4-241">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="a33e4-242">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="a33e4-242">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="a33e4-243">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="a33e4-243">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="a33e4-244">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a33e4-244">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="a33e4-245">重大變更</span><span class="sxs-lookup"><span data-stu-id="a33e4-245">Breaking changes</span></span>
    - <span data-ttu-id="a33e4-246">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="a33e4-246">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="a33e4-247">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="a33e4-247">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a33e4-248">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a33e4-248">Az.DeploymentManager</span></span>
* <span data-ttu-id="a33e4-249">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-249">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="a33e4-250">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a33e4-250">Az.Dns</span></span>
* <span data-ttu-id="a33e4-251">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="a33e4-251">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="a33e4-252">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="a33e4-252">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="a33e4-253">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="a33e4-253">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a33e4-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a33e4-254">Az.FrontDoor</span></span>
* <span data-ttu-id="a33e4-255">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-255">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="a33e4-256">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="a33e4-256">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="a33e4-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a33e4-257">Az.HDInsight</span></span>
* <span data-ttu-id="a33e4-258">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="a33e4-258">Removed two cmdlets:</span></span>
    - <span data-ttu-id="a33e4-259">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a33e4-259">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="a33e4-260">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a33e4-260">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a33e4-261">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a33e4-261">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a33e4-262">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="a33e4-262">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="a33e4-263">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a33e4-263">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="a33e4-264">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="a33e4-264">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a33e4-265">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a33e4-265">Az.Monitor</span></span>
* <span data-ttu-id="a33e4-266">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="a33e4-266">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="a33e4-267">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a33e4-267">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="a33e4-268">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="a33e4-268">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="a33e4-269">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a33e4-269">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="a33e4-270">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a33e4-270">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="a33e4-271">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="a33e4-271">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="a33e4-272">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a33e4-272">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="a33e4-273">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a33e4-273">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a33e4-274">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a33e4-274">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a33e4-275">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a33e4-275">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a33e4-276">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a33e4-276">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a33e4-277">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a33e4-277">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a33e4-278">[更多](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="a33e4-278">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="a33e4-279">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-279">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a33e4-280">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a33e4-280">Az.Network</span></span>
* <span data-ttu-id="a33e4-281">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-281">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="a33e4-282">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-282">New cmdlets</span></span>
        - <span data-ttu-id="a33e4-283">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a33e4-283">New-AzNatGateway</span></span>
        - <span data-ttu-id="a33e4-284">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a33e4-284">Get-AzNatGateway</span></span>
        - <span data-ttu-id="a33e4-285">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a33e4-285">Set-AzNatGateway</span></span>
        - <span data-ttu-id="a33e4-286">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a33e4-286">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="a33e4-287">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-287">Updated cmdlets</span></span>
        - <span data-ttu-id="a33e4-288">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a33e4-288">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="a33e4-289">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a33e4-289">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="a33e4-290">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="a33e4-290">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="a33e4-291">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="a33e4-291">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="a33e4-292">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="a33e4-292">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a33e4-293">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a33e4-293">Az.PolicyInsights</span></span>
* <span data-ttu-id="a33e4-294">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a33e4-294">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="a33e4-295">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="a33e4-295">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="a33e4-296">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="a33e4-296">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a33e4-297">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-297">Az.RecoveryServices</span></span>
* <span data-ttu-id="a33e4-298">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="a33e4-298">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="a33e4-299">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="a33e4-299">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="a33e4-300">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="a33e4-300">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="a33e4-301">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="a33e4-301">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="a33e4-302">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="a33e4-302">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="a33e4-303">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="a33e4-303">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="a33e4-304">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a33e4-304">Az.Relay</span></span>
* <span data-ttu-id="a33e4-305">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="a33e4-305">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a33e4-306">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a33e4-306">Az.ServiceBus</span></span>
* <span data-ttu-id="a33e4-307">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-307">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a33e4-308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a33e4-308">Az.Storage</span></span>
* <span data-ttu-id="a33e4-309">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="a33e4-309">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="a33e4-310">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="a33e4-310">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="a33e4-311">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="a33e4-311">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="a33e4-312">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a33e4-312">New-AzStorageAccount</span></span>
* <span data-ttu-id="a33e4-313">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="a33e4-313">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="a33e4-314">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a33e4-314">New-AzStorageAccount</span></span>
    - <span data-ttu-id="a33e4-315">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a33e4-315">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="a33e4-316">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a33e4-316">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a33e4-317">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a33e4-317">Az.Websites</span></span>
* <span data-ttu-id="a33e4-318">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="a33e4-318">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="a33e4-319">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="a33e4-319">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="a33e4-320">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-320">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a33e4-321">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="a33e4-321">Highlights since the last major release</span></span>
* <span data-ttu-id="a33e4-322">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="a33e4-322">General availability of `Az` module</span></span>
* <span data-ttu-id="a33e4-323">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a33e4-323">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a33e4-324">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a33e4-324">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a33e4-325">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-325">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a33e4-326">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="a33e4-326">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a33e4-327">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-327">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a33e4-328">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-328">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a33e4-329">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a33e4-329">Az.Accounts</span></span>
* <span data-ttu-id="a33e4-330">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="a33e4-330">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a33e4-331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a33e4-331">Az.Batch</span></span>
* <span data-ttu-id="a33e4-332">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a33e4-333">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a33e4-333">Az.Cdn</span></span>
* <span data-ttu-id="a33e4-334">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-334">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a33e4-335">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-335">Az.CognitiveServices</span></span>
* <span data-ttu-id="a33e4-336">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-336">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a33e4-337">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-337">Az.Compute</span></span>
* <span data-ttu-id="a33e4-338">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-338">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="a33e4-339">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-339">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a33e4-340">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="a33e4-340">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a33e4-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a33e4-341">Az.DataFactory</span></span>
* <span data-ttu-id="a33e4-342">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="a33e4-342">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a33e4-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a33e4-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="a33e4-344">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-344">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a33e4-345">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a33e4-345">Az.EventGrid</span></span>
* <span data-ttu-id="a33e4-346">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a33e4-346">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a33e4-347">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a33e4-347">Az.EventHub</span></span>
* <span data-ttu-id="a33e4-348">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-348">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="a33e4-349">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a33e4-349">Az.HDInsight</span></span>
* <span data-ttu-id="a33e4-350">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a33e4-351">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a33e4-351">Az.IotHub</span></span>
* <span data-ttu-id="a33e4-352">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a33e4-353">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a33e4-353">Az.KeyVault</span></span>
* <span data-ttu-id="a33e4-354">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-354">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a33e4-355">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="a33e4-355">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a33e4-356">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a33e4-356">Az.MachineLearning</span></span>
* <span data-ttu-id="a33e4-357">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-357">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="a33e4-358">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a33e4-358">Az.Media</span></span>
* <span data-ttu-id="a33e4-359">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-359">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a33e4-360">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a33e4-360">Az.Monitor</span></span>
  * <span data-ttu-id="a33e4-361">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-361">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="a33e4-362">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="a33e4-362">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="a33e4-363">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="a33e4-363">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="a33e4-364">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a33e4-364">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a33e4-365">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a33e4-365">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a33e4-366">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a33e4-366">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="a33e4-367">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="a33e4-367">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a33e4-368">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a33e4-368">Az.Network</span></span>
* <span data-ttu-id="a33e4-369">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a33e4-370">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="a33e4-370">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="a33e4-371">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a33e4-371">Az.NotificationHubs</span></span>
* <span data-ttu-id="a33e4-372">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-372">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a33e4-373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a33e4-373">Az.OperationalInsights</span></span>
* <span data-ttu-id="a33e4-374">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-374">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a33e4-375">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a33e4-375">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a33e4-376">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a33e4-377">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-377">Az.RecoveryServices</span></span>
* <span data-ttu-id="a33e4-378">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-378">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a33e4-379">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="a33e4-379">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="a33e4-380">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="a33e4-380">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="a33e4-381">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="a33e4-381">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a33e4-382">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a33e4-382">Az.RedisCache</span></span>
* <span data-ttu-id="a33e4-383">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-383">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a33e4-384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-384">Az.Resources</span></span>
* <span data-ttu-id="a33e4-385">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="a33e4-385">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="a33e4-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a33e4-386">Az.Sql</span></span>
* <span data-ttu-id="a33e4-387">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="a33e4-387">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="a33e4-388">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-388">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a33e4-389">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="a33e4-389">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="a33e4-390">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="a33e4-390">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="a33e4-391">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="a33e4-391">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="a33e4-392">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="a33e4-392">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="a33e4-393">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="a33e4-393">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a33e4-394">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a33e4-394">Az.Websites</span></span>
* <span data-ttu-id="a33e4-395">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="a33e4-395">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="a33e4-396">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-396">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a33e4-397">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="a33e4-397">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="a33e4-398">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="a33e4-398">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="a33e4-399">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-399">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a33e4-400">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="a33e4-400">Highlights since the last major release</span></span>
* <span data-ttu-id="a33e4-401">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="a33e4-401">General availability of `Az` module</span></span>
* <span data-ttu-id="a33e4-402">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a33e4-402">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a33e4-403">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a33e4-403">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a33e4-404">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-404">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a33e4-405">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="a33e4-405">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a33e4-406">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-406">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a33e4-407">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-407">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a33e4-408">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a33e4-408">Az.Accounts</span></span>
* <span data-ttu-id="a33e4-409">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="a33e4-409">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a33e4-410">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-410">Az.AnalysisServices</span></span>
* <span data-ttu-id="a33e4-411">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="a33e4-411">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="a33e4-412">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="a33e4-412">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a33e4-413">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a33e4-413">Az.Automation</span></span>
* <span data-ttu-id="a33e4-414">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="a33e4-414">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="a33e4-415">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="a33e4-415">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="a33e4-416">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="a33e4-416">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a33e4-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-417">Az.Compute</span></span>
* <span data-ttu-id="a33e4-418">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a33e4-418">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a33e4-419">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="a33e4-419">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="a33e4-420">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a33e4-420">Az.ContainerInstance</span></span>
* <span data-ttu-id="a33e4-421">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="a33e4-421">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a33e4-422">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a33e4-422">Az.DataFactory</span></span>
* <span data-ttu-id="a33e4-423">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="a33e4-423">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="a33e4-424">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a33e4-424">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a33e4-425">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-425">Az.Resources</span></span>
* <span data-ttu-id="a33e4-426">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="a33e4-426">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="a33e4-427">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="a33e4-427">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a33e4-428">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="a33e4-428">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="a33e4-429">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a33e4-429">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="a33e4-430">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="a33e4-430">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="a33e4-431">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a33e4-431">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="a33e4-432">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a33e4-432">Az.Sql</span></span>
* <span data-ttu-id="a33e4-433">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="a33e4-433">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a33e4-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a33e4-434">Az.Storage</span></span>
* <span data-ttu-id="a33e4-435">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="a33e4-435">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="a33e4-436">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a33e4-436">New-AzStorageContext</span></span>
* <span data-ttu-id="a33e4-437">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="a33e4-437">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="a33e4-438">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a33e4-438">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a33e4-439">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a33e4-439">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a33e4-440">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a33e4-440">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="a33e4-441">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a33e4-441">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="a33e4-442">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-442">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="a33e4-443">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a33e4-443">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a33e4-444">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a33e4-444">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a33e4-445">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a33e4-445">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="a33e4-446">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a33e4-446">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="a33e4-447">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-447">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a33e4-448">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="a33e4-448">Highlights since the last major release</span></span>
* <span data-ttu-id="a33e4-449">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="a33e4-449">General availability of `Az` module</span></span>
* <span data-ttu-id="a33e4-450">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a33e4-450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a33e4-451">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a33e4-451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a33e4-452">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a33e4-453">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="a33e4-453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a33e4-454">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a33e4-455">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a33e4-456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a33e4-456">Az.Automation</span></span>
* <span data-ttu-id="a33e4-457">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="a33e4-457">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="a33e4-458">動態分組</span><span class="sxs-lookup"><span data-stu-id="a33e4-458">Dynamic grouping</span></span>
    * <span data-ttu-id="a33e4-459">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="a33e4-459">Pre-Post script</span></span>
    * <span data-ttu-id="a33e4-460">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="a33e4-460">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a33e4-461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-461">Az.Compute</span></span>
* <span data-ttu-id="a33e4-462">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-462">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="a33e4-463">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="a33e4-463">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a33e4-464">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a33e4-464">Az.KeyVault</span></span>
* <span data-ttu-id="a33e4-465">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-465">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a33e4-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a33e4-466">Az.Network</span></span>
* <span data-ttu-id="a33e4-467">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-467">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="a33e4-468">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="a33e4-468">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a33e4-469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-469">Az.RecoveryServices</span></span>
* <span data-ttu-id="a33e4-470">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="a33e4-470">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="a33e4-471">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-471">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="a33e4-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-472">Az.Resources</span></span>
* <span data-ttu-id="a33e4-473">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-473">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="a33e4-474">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="a33e4-474">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="a33e4-475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a33e4-475">Az.Sql</span></span>
* <span data-ttu-id="a33e4-476">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="a33e4-476">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a33e4-477">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a33e4-477">Az.Storage</span></span>
* <span data-ttu-id="a33e4-478">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="a33e4-478">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="a33e4-479">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a33e4-479">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a33e4-480">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a33e4-480">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a33e4-481">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a33e4-481">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a33e4-482">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="a33e4-482">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="a33e4-483">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="a33e4-483">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="a33e4-484">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a33e4-484">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a33e4-485">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a33e4-485">Az.Websites</span></span>
* <span data-ttu-id="a33e4-486">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="a33e4-486">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="a33e4-487">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-487">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a33e4-488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a33e4-488">Az.Accounts</span></span>
* <span data-ttu-id="a33e4-489">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-489">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="a33e4-490">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="a33e4-490">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a33e4-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a33e4-491">Az.Automation</span></span>
* <span data-ttu-id="a33e4-492">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-492">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="a33e4-493">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="a33e4-493">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="a33e4-494">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="a33e4-494">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a33e4-495">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a33e4-495">Az.Cdn</span></span>
* <span data-ttu-id="a33e4-496">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-496">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a33e4-497">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-497">Az.Compute</span></span>
* <span data-ttu-id="a33e4-498">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-498">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a33e4-499">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a33e4-499">Az.DataFactory</span></span>
* <span data-ttu-id="a33e4-500">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="a33e4-500">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a33e4-501">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a33e4-501">Az.LogicApp</span></span>
* <span data-ttu-id="a33e4-502">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="a33e4-502">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a33e4-503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a33e4-503">Az.Network</span></span>
* <span data-ttu-id="a33e4-504">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-504">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a33e4-505">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-505">Az.RecoveryServices</span></span>
* <span data-ttu-id="a33e4-506">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-506">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="a33e4-507">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="a33e4-507">SDK Update</span></span>
* <span data-ttu-id="a33e4-508">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="a33e4-508">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="a33e4-509">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="a33e4-509">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="a33e4-510">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-510">Az.Resources</span></span>
* <span data-ttu-id="a33e4-511">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-511">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="a33e4-512">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="a33e4-512">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="a33e4-513">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-513">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="a33e4-514">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="a33e4-514">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="a33e4-515">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-515">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="a33e4-516">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="a33e4-516">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="a33e4-517">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a33e4-517">Az.Sql</span></span>
* <span data-ttu-id="a33e4-518">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="a33e4-518">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="a33e4-519">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="a33e4-519">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a33e4-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a33e4-520">Az.Storage</span></span>
* <span data-ttu-id="a33e4-521">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a33e4-521">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="a33e4-522">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-522">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a33e4-523">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-523">Az.AnalysisServices</span></span>
* <span data-ttu-id="a33e4-524">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-524">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a33e4-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a33e4-525">Az.Automation</span></span>
* <span data-ttu-id="a33e4-526">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="a33e4-526">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a33e4-527">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-527">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a33e4-528">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="a33e4-528">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a33e4-529">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-529">Az.CognitiveServices</span></span>
* <span data-ttu-id="a33e4-530">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="a33e4-530">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a33e4-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-531">Az.Compute</span></span>
* <span data-ttu-id="a33e4-532">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-532">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a33e4-533">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="a33e4-533">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a33e4-534">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-534">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a33e4-535">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="a33e4-535">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a33e4-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a33e4-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="a33e4-537">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-537">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a33e4-538">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a33e4-538">Az.EventHub</span></span>
* <span data-ttu-id="a33e4-539">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="a33e4-539">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="a33e4-540">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a33e4-540">Az.KeyVault</span></span>
* <span data-ttu-id="a33e4-541">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="a33e4-541">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a33e4-542">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a33e4-542">Az.LogicApp</span></span>
* <span data-ttu-id="a33e4-543">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="a33e4-543">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a33e4-544">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="a33e4-544">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a33e4-545">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-545">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a33e4-546">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a33e4-546">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a33e4-547">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a33e4-547">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a33e4-548">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a33e4-548">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a33e4-549">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a33e4-549">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a33e4-550">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-550">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a33e4-551">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a33e4-551">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a33e4-552">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a33e4-552">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a33e4-553">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a33e4-553">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a33e4-554">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a33e4-554">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a33e4-555">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="a33e4-555">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a33e4-556">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a33e4-556">Az.Monitor</span></span>
* <span data-ttu-id="a33e4-557">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="a33e4-557">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a33e4-558">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a33e4-558">Az.Network</span></span>
* <span data-ttu-id="a33e4-559">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="a33e4-559">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a33e4-560">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a33e4-560">Az.OperationalInsights</span></span>
* <span data-ttu-id="a33e4-561">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="a33e4-561">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a33e4-562">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="a33e4-562">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="a33e4-563">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="a33e4-563">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="a33e4-564">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-564">Az.Resources</span></span>
* <span data-ttu-id="a33e4-565">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-565">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a33e4-566">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-566">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a33e4-567">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-567">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a33e4-568">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="a33e4-568">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a33e4-569">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a33e4-569">Az.Sql</span></span>
* <span data-ttu-id="a33e4-570">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-570">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a33e4-571">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="a33e4-571">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a33e4-572">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a33e4-572">Az.Websites</span></span>
* <span data-ttu-id="a33e4-573">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="a33e4-573">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a33e4-574">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-574">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a33e4-575">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a33e4-575">Az.Accounts</span></span>
* <span data-ttu-id="a33e4-576">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a33e4-576">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a33e4-577">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-577">Az.AnalysisServices</span></span>
<span data-ttu-id="a33e4-578">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="a33e4-578">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a33e4-579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-579">Az.Compute</span></span>
* <span data-ttu-id="a33e4-580">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-580">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a33e4-581">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="a33e4-581">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a33e4-582">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="a33e4-582">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a33e4-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-583">Az.RecoveryServices</span></span>
<span data-ttu-id="a33e4-584">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="a33e4-584">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a33e4-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-585">Az.Resources</span></span>
* <span data-ttu-id="a33e4-586">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="a33e4-586">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="a33e4-587">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a33e4-587">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a33e4-588">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-588">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="a33e4-589">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a33e4-589">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a33e4-590">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a33e4-590">Az.Sql</span></span>
* <span data-ttu-id="a33e4-591">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a33e4-591">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a33e4-592">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-592">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a33e4-593">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="a33e4-593">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a33e4-594">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-594">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a33e4-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a33e4-595">Az.Accounts</span></span>
* <span data-ttu-id="a33e4-596">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="a33e4-596">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a33e4-597">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-597">Az.AnalysisServices</span></span>
* <span data-ttu-id="a33e4-598">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="a33e4-598">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a33e4-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="a33e4-600">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="a33e4-600">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a33e4-601">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-601">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a33e4-602">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a33e4-602">Az.Accounts</span></span>
* <span data-ttu-id="a33e4-603">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="a33e4-603">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a33e4-604">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="a33e4-604">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a33e4-605">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="a33e4-605">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a33e4-606">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a33e4-606">Az.Aks</span></span>
* <span data-ttu-id="a33e4-607">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="a33e4-607">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a33e4-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a33e4-608">Az.Automation</span></span>
* <span data-ttu-id="a33e4-609">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-609">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a33e4-610">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="a33e4-610">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a33e4-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a33e4-611">Az.Cdn</span></span>
* <span data-ttu-id="a33e4-612">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="a33e4-612">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a33e4-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-613">Az.Compute</span></span>
* <span data-ttu-id="a33e4-614">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-614">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a33e4-615">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a33e4-615">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a33e4-616">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="a33e4-616">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a33e4-617">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a33e4-617">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a33e4-618">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="a33e4-618">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a33e4-619">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a33e4-619">Az.DataFactory</span></span>
* <span data-ttu-id="a33e4-620">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="a33e4-620">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a33e4-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a33e4-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="a33e4-622">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-622">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a33e4-623">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="a33e4-623">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a33e4-624">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="a33e4-624">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a33e4-625">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a33e4-625">Az.IotHub</span></span>
* <span data-ttu-id="a33e4-626">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a33e4-626">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a33e4-627">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a33e4-627">Az.KeyVault</span></span>
* <span data-ttu-id="a33e4-628">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="a33e4-628">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a33e4-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a33e4-629">Az.Network</span></span>
* <span data-ttu-id="a33e4-630">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="a33e4-630">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a33e4-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-631">Az.Resources</span></span>
* <span data-ttu-id="a33e4-632">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="a33e4-632">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a33e4-633">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-633">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a33e4-634">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="a33e4-634">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a33e4-635">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-635">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a33e4-636">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-636">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a33e4-637">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-637">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a33e4-638">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="a33e4-638">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a33e4-639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a33e4-639">Az.ServiceFabric</span></span>
* <span data-ttu-id="a33e4-640">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="a33e4-640">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a33e4-641">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="a33e4-641">Fix some error messages.</span></span>
* <span data-ttu-id="a33e4-642">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="a33e4-642">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a33e4-643">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="a33e4-643">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a33e4-644">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a33e4-644">Az.SignalR</span></span>
* <span data-ttu-id="a33e4-645">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="a33e4-645">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a33e4-646">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a33e4-646">Az.Sql</span></span>
* <span data-ttu-id="a33e4-647">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="a33e4-647">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a33e4-648">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="a33e4-648">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a33e4-649">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-649">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a33e4-650">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="a33e4-650">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a33e4-651">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a33e4-651">Az.Storage</span></span>
* <span data-ttu-id="a33e4-652">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="a33e4-652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a33e4-653">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="a33e4-653">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a33e4-654">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a33e4-654">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a33e4-655">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a33e4-655">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a33e4-656">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a33e4-656">Az.TrafficManager</span></span>
* <span data-ttu-id="a33e4-657">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="a33e4-657">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a33e4-658">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a33e4-658">Az.Websites</span></span>
* <span data-ttu-id="a33e4-659">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="a33e4-659">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a33e4-660">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="a33e4-660">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a33e4-661">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="a33e4-661">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a33e4-662">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-662">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a33e4-663">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a33e4-663">Az.Accounts</span></span>
* <span data-ttu-id="a33e4-664">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="a33e4-664">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a33e4-665">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-665">Az.Compute</span></span>
* <span data-ttu-id="a33e4-666">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="a33e4-666">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a33e4-667">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="a33e4-667">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a33e4-668">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-668">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a33e4-669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a33e4-669">Az.DataLakeStore</span></span>
* <span data-ttu-id="a33e4-670">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="a33e4-670">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a33e4-671">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="a33e4-671">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a33e4-672">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a33e4-672">Az.EventGrid</span></span>
* <span data-ttu-id="a33e4-673">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="a33e4-673">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a33e4-674">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="a33e4-674">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a33e4-675">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="a33e4-675">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a33e4-676">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="a33e4-676">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a33e4-677">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="a33e4-677">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a33e4-678">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="a33e4-678">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a33e4-679">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="a33e4-679">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a33e4-680">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="a33e4-680">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a33e4-681">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="a33e4-681">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a33e4-682">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="a33e4-682">Dead letter endpoint.</span></span>
* <span data-ttu-id="a33e4-683">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="a33e4-683">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a33e4-684">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="a33e4-684">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a33e4-685">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a33e4-685">Az.IotHub</span></span>
* <span data-ttu-id="a33e4-686">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="a33e4-686">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a33e4-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a33e4-687">Az.LogicApp</span></span>
* <span data-ttu-id="a33e4-688">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="a33e4-688">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a33e4-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-689">Az.Resources</span></span>
* <span data-ttu-id="a33e4-690">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-690">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a33e4-691">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="a33e4-691">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a33e4-692">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="a33e4-692">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a33e4-693">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="a33e4-693">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a33e4-694">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="a33e4-694">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a33e4-695">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="a33e4-695">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a33e4-696">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a33e4-696">Az.SignalR</span></span>
* <span data-ttu-id="a33e4-697">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-697">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a33e4-698">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a33e4-698">Az.Sql</span></span>
* <span data-ttu-id="a33e4-699">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="a33e4-699">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a33e4-700">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a33e4-700">Az.Storage</span></span>
* <span data-ttu-id="a33e4-701">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="a33e4-701">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a33e4-702">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a33e4-702">New-AzStorageContext</span></span>
* <span data-ttu-id="a33e4-703">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="a33e4-703">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a33e4-704">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a33e4-704">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a33e4-705">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a33e4-705">Az.Websites</span></span>
* <span data-ttu-id="a33e4-706">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="a33e4-706">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a33e4-707">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-707">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a33e4-708">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-708">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a33e4-709">一般</span><span class="sxs-lookup"><span data-stu-id="a33e4-709">General</span></span>

- <span data-ttu-id="a33e4-710">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="a33e4-710">General Availability of Az Module</span></span>
- <span data-ttu-id="a33e4-711">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="a33e4-711">Online help for each module</span></span>
- <span data-ttu-id="a33e4-712">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="a33e4-712">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a33e4-713">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-713">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a33e4-714">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a33e4-714">Az.Accounts</span></span>
- <span data-ttu-id="a33e4-715">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="a33e4-715">Changed from Az.Profile</span></span>
- <span data-ttu-id="a33e4-716">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="a33e4-716">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a33e4-717">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a33e4-717">Az.ApiManagement</span></span>
- <span data-ttu-id="a33e4-718">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="a33e4-718">Fixes for #7002</span></span>
- <span data-ttu-id="a33e4-719">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-719">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a33e4-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a33e4-720">Az.Batch</span></span>
- <span data-ttu-id="a33e4-721">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="a33e4-721">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a33e4-722">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="a33e4-722">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a33e4-723">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-723">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a33e4-724">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a33e4-724">Az.Billing</span></span>
- <span data-ttu-id="a33e4-725">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-725">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a33e4-726">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-726">Az.CognitivServices</span></span>
- <span data-ttu-id="a33e4-727">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="a33e4-727">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a33e4-728">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="a33e4-728">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a33e4-729">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a33e4-729">Az.ContainerInstance</span></span>
- <span data-ttu-id="a33e4-730">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-730">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a33e4-731">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a33e4-731">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a33e4-732">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-732">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a33e4-733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a33e4-733">Az.DataLakeStore</span></span>
- <span data-ttu-id="a33e4-734">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-734">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a33e4-735">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a33e4-735">Az.Monitor</span></span>
- <span data-ttu-id="a33e4-736">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-736">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a33e4-737">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a33e4-737">Az.KeyVault</span></span>
- <span data-ttu-id="a33e4-738">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="a33e4-738">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a33e4-739">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a33e4-739">Az.MachineLearning</span></span>
- <span data-ttu-id="a33e4-740">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-740">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a33e4-741">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a33e4-741">Az.Media</span></span>
- <span data-ttu-id="a33e4-742">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="a33e4-742">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a33e4-743">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a33e4-743">Az.Network</span></span>
<span data-ttu-id="a33e4-744">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-744">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a33e4-745">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="a33e4-745">New cmdlets added:</span></span>
        - <span data-ttu-id="a33e4-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a33e4-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a33e4-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a33e4-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a33e4-748">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a33e4-748">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a33e4-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a33e4-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a33e4-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a33e4-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a33e4-751">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a33e4-751">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a33e4-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a33e4-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a33e4-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a33e4-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a33e4-754">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a33e4-754">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a33e4-755">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a33e4-755">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a33e4-756">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a33e4-756">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a33e4-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a33e4-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a33e4-758">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a33e4-758">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a33e4-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a33e4-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a33e4-760">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="a33e4-760">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a33e4-761">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-761">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a33e4-762">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a33e4-762">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a33e4-763">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a33e4-763">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a33e4-764">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a33e4-764">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a33e4-765">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-765">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a33e4-766">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-766">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a33e4-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a33e4-767">Az.OperationalInsights</span></span>
- <span data-ttu-id="a33e4-768">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-768">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a33e4-769">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a33e4-769">Az.Profile</span></span>
- <span data-ttu-id="a33e4-770">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a33e4-770">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a33e4-771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-771">Az.RecoveryServices</span></span>
- <span data-ttu-id="a33e4-772">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-772">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a33e4-773">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-773">Az.Resources</span></span>
- <span data-ttu-id="a33e4-774">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-774">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a33e4-775">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a33e4-775">Az.ServiceFabric</span></span>
- <span data-ttu-id="a33e4-776">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="a33e4-776">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a33e4-777">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-777">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a33e4-778">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a33e4-778">Az.SIgnalR</span></span>
- <span data-ttu-id="a33e4-779">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="a33e4-779">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a33e4-780">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a33e4-780">Az.Sql</span></span>
- <span data-ttu-id="a33e4-781">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="a33e4-781">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a33e4-782">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="a33e4-782">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a33e4-783">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-783">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a33e4-784">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a33e4-784">Az.Storage</span></span>
- <span data-ttu-id="a33e4-785">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-785">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a33e4-786">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a33e4-786">Az.Websites</span></span>
- <span data-ttu-id="a33e4-787">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a33e4-787">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a33e4-788">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-788">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a33e4-789">一般</span><span class="sxs-lookup"><span data-stu-id="a33e4-789">General</span></span>

* <span data-ttu-id="a33e4-790">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="a33e4-790">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a33e4-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-791">Az.Compute</span></span>

* <span data-ttu-id="a33e4-792">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="a33e4-792">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a33e4-793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a33e4-793">Az.DataLakeStore</span></span>

* <span data-ttu-id="a33e4-794">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="a33e4-794">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a33e4-795">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a33e4-795">Az.FrontDoor</span></span>

* <span data-ttu-id="a33e4-796">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="a33e4-796">Fixed some broken links</span></span>
    - <span data-ttu-id="a33e4-797">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="a33e4-797">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a33e4-798">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="a33e4-798">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a33e4-799">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-799">Az.RecoveryServices</span></span>

* <span data-ttu-id="a33e4-800">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="a33e4-800">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a33e4-801">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="a33e4-801">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a33e4-802">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-802">Az.Resources</span></span>

* <span data-ttu-id="a33e4-803">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="a33e4-803">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a33e4-804">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="a33e4-804">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a33e4-805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a33e4-805">Az.Sql</span></span>

* <span data-ttu-id="a33e4-806">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="a33e4-806">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a33e4-807">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-807">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a33e4-808">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="a33e4-808">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a33e4-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a33e4-809">Az.Storage</span></span>

* <span data-ttu-id="a33e4-810">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="a33e4-810">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a33e4-811">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="a33e4-811">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a33e4-812">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a33e4-812">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a33e4-813">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="a33e4-813">Support Static Website configuration</span></span>
    - <span data-ttu-id="a33e4-814">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a33e4-814">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a33e4-815">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a33e4-815">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a33e4-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a33e4-816">Az.Websites</span></span>

* <span data-ttu-id="a33e4-817">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a33e4-817">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="a33e4-818">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="a33e4-818">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a33e4-819">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="a33e4-819">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a33e4-820">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-820">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a33e4-821">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a33e4-821">Az.ApiManagement</span></span>
* <span data-ttu-id="a33e4-822">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="a33e4-822">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a33e4-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a33e4-823">Az.Automation</span></span>
* <span data-ttu-id="a33e4-824">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-824">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a33e4-825">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-825">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a33e4-826">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-826">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a33e4-827">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-827">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a33e4-828">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="a33e4-828">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a33e4-829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-829">Az.Compute</span></span>
* <span data-ttu-id="a33e4-830">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-830">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a33e4-831">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="a33e4-831">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a33e4-832">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a33e4-832">Az.ContainerInstance</span></span>
* <span data-ttu-id="a33e4-833">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="a33e4-833">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a33e4-834">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a33e4-834">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a33e4-835">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="a33e4-835">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a33e4-836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a33e4-836">Az.Network</span></span>
* <span data-ttu-id="a33e4-837">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a33e4-837">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a33e4-838">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="a33e4-838">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a33e4-839">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="a33e4-839">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="a33e4-840">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-840">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a33e4-841">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a33e4-841">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a33e4-842">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="a33e4-842">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a33e4-843">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="a33e4-843">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a33e4-844">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a33e4-844">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a33e4-845">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="a33e4-845">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a33e4-846">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="a33e4-846">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a33e4-847">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a33e4-847">Az.Relay</span></span>
* <span data-ttu-id="a33e4-848">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="a33e4-848">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a33e4-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-849">Az.Resources</span></span>
* <span data-ttu-id="a33e4-850">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="a33e4-850">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="a33e4-851">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="a33e4-851">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a33e4-852">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="a33e4-852">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a33e4-853">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a33e4-853">Az.ServiceFabric</span></span>
* <span data-ttu-id="a33e4-854">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="a33e4-854">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a33e4-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a33e4-855">Az.Sql</span></span>
* <span data-ttu-id="a33e4-856">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-856">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a33e4-857">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a33e4-857">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a33e4-858">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a33e4-858">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a33e4-859">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a33e4-859">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a33e4-860">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a33e4-860">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a33e4-861">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a33e4-861">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a33e4-862">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a33e4-862">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a33e4-863">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a33e4-863">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a33e4-864">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a33e4-864">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a33e4-865">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="a33e4-865">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a33e4-866">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="a33e4-866">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a33e4-867">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="a33e4-867">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a33e4-868">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="a33e4-868">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a33e4-869">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="a33e4-869">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a33e4-870">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="a33e4-870">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a33e4-871">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="a33e4-871">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a33e4-872">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-872">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a33e4-873">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-873">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a33e4-874">一般</span><span class="sxs-lookup"><span data-stu-id="a33e4-874">General</span></span>
* <span data-ttu-id="a33e4-875">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="a33e4-875">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a33e4-876">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a33e4-876">Az.Profile</span></span>
* <span data-ttu-id="a33e4-877">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a33e4-877">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a33e4-878">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="a33e4-878">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a33e4-879">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="a33e4-879">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a33e4-880">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="a33e4-880">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a33e4-881">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-881">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a33e4-882">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-882">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a33e4-883">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-883">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a33e4-884">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-884">Az.CognitiveServices</span></span>
* <span data-ttu-id="a33e4-885">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="a33e4-885">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a33e4-886">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-886">Az.Compute</span></span>
* <span data-ttu-id="a33e4-887">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-887">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a33e4-888">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="a33e4-888">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a33e4-889">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="a33e4-889">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a33e4-890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a33e4-890">Az.DataLakeStore</span></span>
* <span data-ttu-id="a33e4-891">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="a33e4-891">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a33e4-892">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="a33e4-892">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a33e4-893">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a33e4-893">Az.Insights</span></span>
* <span data-ttu-id="a33e4-894">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="a33e4-894">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a33e4-895">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="a33e4-895">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a33e4-896">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="a33e4-896">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a33e4-897">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="a33e4-897">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a33e4-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a33e4-898">Az.Network</span></span>
* <span data-ttu-id="a33e4-899">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="a33e4-899">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a33e4-900">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a33e4-900">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a33e4-901">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a33e4-901">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a33e4-902">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a33e4-902">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a33e4-903">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a33e4-903">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a33e4-904">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a33e4-904">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a33e4-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a33e4-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a33e4-906">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a33e4-906">Az.PolicyInsights</span></span>
* <span data-ttu-id="a33e4-907">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-907">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a33e4-908">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-908">Az.Resources</span></span>
* <span data-ttu-id="a33e4-909">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="a33e4-909">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a33e4-910">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="a33e4-910">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a33e4-911">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a33e4-911">Az.ServiceBus</span></span>
* <span data-ttu-id="a33e4-912">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="a33e4-912">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a33e4-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a33e4-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="a33e4-914">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="a33e4-914">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a33e4-915">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="a33e4-915">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a33e4-916">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="a33e4-916">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a33e4-917">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="a33e4-917">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a33e4-918">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="a33e4-918">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a33e4-919">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-919">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a33e4-920">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a33e4-920">Az.Profile</span></span>
* <span data-ttu-id="a33e4-921">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-921">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a33e4-922">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a33e4-922">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a33e4-923">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-923">Az.Compute</span></span>
* <span data-ttu-id="a33e4-924">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="a33e4-924">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a33e4-925">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a33e4-925">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a33e4-926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a33e4-926">Az.DataLakeStore</span></span>
* <span data-ttu-id="a33e4-927">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="a33e4-927">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a33e4-928">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a33e4-928">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a33e4-929">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="a33e4-929">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a33e4-930">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a33e4-930">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a33e4-931">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a33e4-931">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a33e4-932">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a33e4-932">Az.Network</span></span>
* <span data-ttu-id="a33e4-933">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="a33e4-933">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a33e4-934">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a33e4-934">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a33e4-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-935">Az.Resources</span></span>
* <span data-ttu-id="a33e4-936">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="a33e4-936">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a33e4-937">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="a33e4-937">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a33e4-938">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-938">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a33e4-939">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a33e4-939">Azure.Storage</span></span>
* <span data-ttu-id="a33e4-940">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-940">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a33e4-941">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a33e4-941">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a33e4-942">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a33e4-942">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a33e4-943">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="a33e4-943">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a33e4-944">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a33e4-944">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="a33e4-945">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a33e4-945">Az.CognitiveServices</span></span>
* <span data-ttu-id="a33e4-946">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="a33e4-946">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a33e4-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a33e4-947">Az.Compute</span></span>
* <span data-ttu-id="a33e4-948">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="a33e4-948">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a33e4-949">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="a33e4-949">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a33e4-950">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="a33e4-950">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a33e4-951">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a33e4-951">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a33e4-952">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="a33e4-952">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a33e4-953">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a33e4-953">Az.Network</span></span>
* <span data-ttu-id="a33e4-954">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="a33e4-954">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a33e4-955">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-955">new cmdlets added</span></span>
    - <span data-ttu-id="a33e4-956">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a33e4-956">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a33e4-957">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a33e4-957">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a33e4-958">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a33e4-958">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a33e4-959">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a33e4-959">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a33e4-960">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a33e4-960">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a33e4-961">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a33e4-961">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a33e4-962">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="a33e4-962">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a33e4-963">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-963">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a33e4-964">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a33e4-964">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a33e4-965">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a33e4-965">Az.RedisCache</span></span>
* <span data-ttu-id="a33e4-966">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="a33e4-966">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a33e4-967">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="a33e4-967">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a33e4-968">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a33e4-968">Az.Resources</span></span>
* <span data-ttu-id="a33e4-969">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a33e4-969">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a33e4-970">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="a33e4-970">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a33e4-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a33e4-971">Az.Sql</span></span>
* <span data-ttu-id="a33e4-972">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="a33e4-972">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a33e4-973">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a33e4-973">Az.Websites</span></span>
* <span data-ttu-id="a33e4-974">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="a33e4-974">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a33e4-975">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="a33e4-975">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a33e4-976">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="a33e4-976">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a33e4-977">初始版本</span><span class="sxs-lookup"><span data-stu-id="a33e4-977">Initial Release</span></span>