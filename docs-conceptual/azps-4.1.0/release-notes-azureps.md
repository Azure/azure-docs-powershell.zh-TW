---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 60827fe7b4f8c351655046e3711660cdf7ce0513
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2020
ms.locfileid: "83631059"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="36b42-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="36b42-103">Azure PowerShell release notes</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="36b42-104">4.1.0 - 2020 年 5 月</span><span class="sxs-lookup"><span data-stu-id="36b42-104">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="36b42-105">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="36b42-105">Highlights since the last release</span></span>
* <span data-ttu-id="36b42-106">支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="36b42-106">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="36b42-107">Az.Functions 正式發行</span><span class="sxs-lookup"><span data-stu-id="36b42-107">General availability of Az.Functions</span></span> 
* <span data-ttu-id="36b42-108">Az.ApiManagement、Az.Batch、Az.Compute、Az.KeyVault、Az.Monitor、Az.Network、Az.OperationalInsights、Az.Resources 和 Az.Storage 具有主要版本</span><span class="sxs-lookup"><span data-stu-id="36b42-108">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36b42-109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-109">Az.Accounts</span></span>
* <span data-ttu-id="36b42-110">已更新 'Add-AzEnvironment' 和 'Set-AzEnvironment' 以接受 'AzureSynapseAnalyticsEndpointResourceId' 和 'AzureSynapseAnalyticsEndpointSuffix' 參數</span><span class="sxs-lookup"><span data-stu-id="36b42-110">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="36b42-111">已將 Azure.Core 相關組件新增至 Az.Accounts，支援的 PowerShell 平台包括 Windows PowerShell 5.1、PowerShell Core 6.2.4、PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="36b42-111">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="36b42-112">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="36b42-112">Az.Aks</span></span>
* <span data-ttu-id="36b42-113">已將 API 版本升級至 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="36b42-113">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="36b42-114">支援使用 Windows 容器建立 AKS</span><span class="sxs-lookup"><span data-stu-id="36b42-114">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="36b42-115">已提供新的 Cmdlet：'New-AzAksNodePool'、'Update-AzAksNodePool'、'Remove-AzAksNodePool'、        'Get-AzAksNodePool'、'Install-AzAksKubectl'、'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="36b42-115">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36b42-116">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36b42-116">Az.ApiManagement</span></span>
* <span data-ttu-id="36b42-117">'New-AzApiManagement' 與 'Set-AzApiManagement': [-AssignIdentity] 參數已重新命名為 [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="36b42-117">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="36b42-118">'New-AzApiManagement' 與 'Set-AzApiManagement'：已新增下列參數：[-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="36b42-118">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="36b42-119">'Get-AzApiManagementProperty'：已重新命名為 'Get-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="36b42-119">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="36b42-120">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="36b42-120">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="36b42-121">'New-AzApiManagementProperty'：已重新命名為 'New-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="36b42-121">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="36b42-122">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="36b42-122">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="36b42-123">'Set-AzApiManagementProperty'：已重新命名為 'Set-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="36b42-123">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="36b42-124">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="36b42-124">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="36b42-125">'Remove-AzApiManagementProperty'：已重新命名為 'Remove-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="36b42-125">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="36b42-126">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="36b42-126">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="36b42-127">新增的 'Get-AzApiManagementAuthorizationServerClientSecret' Cmdlet 和 'Get-AzApiManagementAuthorizationServer' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="36b42-127">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="36b42-128">新增的 'AzApiManagementNamedValueSecretValue' Cmdlet 和 'AzApiManagementNamedValue' 將不會傳回密碼值。</span><span class="sxs-lookup"><span data-stu-id="36b42-128">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="36b42-129">新增的 'Get-AzApiManagementOpenIdConnectProviderClientSecret' Cmdlet 和 'Get-AzApiManagementOpenIdConnectProvider' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="36b42-129">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="36b42-130">新增的 'AzApiManagementSubscriptionKey' Cmdlet 和 'AzApiManagementSubscription' 將不再傳回訂用帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="36b42-130">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="36b42-131">新增的 'AzApiManagementTenantAccessSecret' Cmdlet 和 'AzApiManagementTenantAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="36b42-131">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="36b42-132">新增的 'AzApiManagementTenantGitAccessSecret' Cmdlet 和 'AzApiManagementTenantGitAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="36b42-132">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="36b42-133">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-133">Az.ApplicationInsights</span></span>
* <span data-ttu-id="36b42-134">新增的參數：適用於 'New-AzApplicationInsights' 的 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="36b42-134">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="36b42-135">已建立 Cmdlet 'Update-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="36b42-135">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="36b42-136">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-136">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="36b42-137">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36b42-137">Az.Batch</span></span>
* <span data-ttu-id="36b42-138">已將 Az.Batch 更新為使用 'Microsoft.Azure.Batch' SDK 版本 13.0.0 和 'Microsoft.Azure.Management.Batch' SDK 版本 9.0.0。</span><span class="sxs-lookup"><span data-stu-id="36b42-138">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="36b42-139">已新增下列功能：使用新的 '-CertificateKind' 參數選取要新增至 'New-AzBatchCertificate' 的憑證種類。</span><span class="sxs-lookup"><span data-stu-id="36b42-139">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="36b42-140">已從 'PSApplication' 中移除先前一律為 '' 的 'ApplicationPackages' 屬性。</span><span class="sxs-lookup"><span data-stu-id="36b42-140">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="36b42-141">現在可以使用 'Get-AzBatchApplicationPackage' 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="36b42-141">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="36b42-142">例如：'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'。</span><span class="sxs-lookup"><span data-stu-id="36b42-142">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="36b42-143">使用 'New-AzBatchPool' 建立集區時，'PSImageReference' 的 'VirtualMachineImageId' 屬性現在只能參考共用映像庫映像。</span><span class="sxs-lookup"><span data-stu-id="36b42-143">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="36b42-144">使用 'New-AzBatchPool' 建立集區時，可以使用 'PSNetworkConfiguration' 的新 'PublicIPAddressConfiguration' 屬性來佈建集區，無需公用 IP。</span><span class="sxs-lookup"><span data-stu-id="36b42-144">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="36b42-145">'PSNetworkConfiguration' 的 'PublicIPs' 屬性也已移至 'PSPublicIPAddressConfiguration'。</span><span class="sxs-lookup"><span data-stu-id="36b42-145">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="36b42-146">只有當 'IPAddressProvisioningType' 是 'UserManaged' 時，才能指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="36b42-146">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-147">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-147">Az.Compute</span></span>
* <span data-ttu-id="36b42-148">已將 HostId 參數新增至 'Update-AzVM' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-148">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="36b42-149">已更新 'New-AzVMConfig'、'New-AzVmssConfig', 'Update-AzVmss'、'Set-AzVMOperatingSystem' 和 'Set-AzVmssOsProfile' Cmdlet 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="36b42-149">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="36b42-150">重大變更</span><span class="sxs-lookup"><span data-stu-id="36b42-150">Breaking changes</span></span>
    - <span data-ttu-id="36b42-151">已從 'Get-AzVMImage' Cmdlet 中移除 FilterExpression 參數。</span><span class="sxs-lookup"><span data-stu-id="36b42-151">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="36b42-152">已從 'New-AzVmssConfig'、'New-AzVMConfig' 和 'Update-AzVM' Cmdlet 中移除 AssignIdentity 參數。</span><span class="sxs-lookup"><span data-stu-id="36b42-152">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="36b42-153">已從 'New-AzVmssConfig' 和 'Update-AzVmss' Cmdlet 中移除 AutomaticRepairMaxInstanceRepairsPercent。</span><span class="sxs-lookup"><span data-stu-id="36b42-153">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="36b42-154">已從 ProximityPlacementGroup 中移除 AvailabilitySetsColocationStatus、VirtualMachinesColocationStatus 和 VirtualMachineScaleSetsColocationStatus。</span><span class="sxs-lookup"><span data-stu-id="36b42-154">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="36b42-155">已從 AutomaticRepairsPolicy 中移除 MaxInstanceRepairsPercent 屬性。</span><span class="sxs-lookup"><span data-stu-id="36b42-155">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="36b42-156">AvailabilitySets、VirtualMachines 和 VirtualMachineScaleSets 的類型已從 IList<SubResource> 變更為 IList<SubResourceWithColocationStatus>。</span><span class="sxs-lookup"><span data-stu-id="36b42-156">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="36b42-157">已更新 ' Update-azvm ' Cmdlet 的描述，以提供更好的描述。</span><span class="sxs-lookup"><span data-stu-id="36b42-157">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-158">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-158">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-159">支援受控 IR 中資料流程執行階段屬性的 CRUD。</span><span class="sxs-lookup"><span data-stu-id="36b42-159">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="36b42-160">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36b42-160">Az.FrontDoor</span></span>
* <span data-ttu-id="36b42-161">已新增用於建立、更新、取出及刪除 Front Door 規則引擎物件的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-161">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="36b42-162">已新增用於建構 Front Door 規則引擎物件的協助程式 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-162">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="36b42-163">已將規則引擎參考新增至 Front Door 路由規則物件。</span><span class="sxs-lookup"><span data-stu-id="36b42-163">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="36b42-164">已將私人連結參數新增至 Front Door 後端物件</span><span class="sxs-lookup"><span data-stu-id="36b42-164">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="36b42-165">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="36b42-165">Az.Functions</span></span>
* <span data-ttu-id="36b42-166">''Az.Functions'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="36b42-166">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36b42-167">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36b42-167">Az.HDInsight</span></span>
* <span data-ttu-id="36b42-168">支援客戶管理的金鑰磁碟加密。</span><span class="sxs-lookup"><span data-stu-id="36b42-168">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="36b42-169">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="36b42-169">Az.HealthcareApis</span></span>
* <span data-ttu-id="36b42-170">存取原則不再預設為目前的主體</span><span class="sxs-lookup"><span data-stu-id="36b42-170">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36b42-171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36b42-171">Az.IotHub</span></span>
* <span data-ttu-id="36b42-172">已新增 Cmdlet 來叫用 IoT 中樞內的查詢，以使用類似 SQL 的語言來取出資訊。</span><span class="sxs-lookup"><span data-stu-id="36b42-172">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="36b42-173">已修正下列問題：沒有子裝置，'Add-AzIotHubDevice' 無法建立已啟用 Edge 的裝置 [#11597]</span><span class="sxs-lookup"><span data-stu-id="36b42-173">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="36b42-174">已新增 Cmdlet 來產生 Iot 中樞、裝置或模組的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="36b42-174">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="36b42-175">已新增 Cmdlet 來叫用設定計量查詢。</span><span class="sxs-lookup"><span data-stu-id="36b42-175">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="36b42-176">管理大規模的 IoT Edge 自動部署。</span><span class="sxs-lookup"><span data-stu-id="36b42-176">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="36b42-177">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="36b42-177">New cmdlets are:</span></span>
    - <span data-ttu-id="36b42-178">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="36b42-178">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="36b42-179">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="36b42-179">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="36b42-180">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="36b42-180">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="36b42-181">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="36b42-181">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="36b42-182">已新增 Cmdlet 來叫用 IoT Edge 部署計量查詢。</span><span class="sxs-lookup"><span data-stu-id="36b42-182">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="36b42-183">已新增 Cmdlet 將設定內容套用至指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="36b42-183">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36b42-184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36b42-184">Az.KeyVault</span></span>
* <span data-ttu-id="36b42-185">已移除兩個別名：'New-AzKeyVaultCertificateAdministratorDetails' 和 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="36b42-185">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="36b42-186">建立金鑰保存庫時，依預設會啟用虛刪除</span><span class="sxs-lookup"><span data-stu-id="36b42-186">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="36b42-187">在建立金鑰保存庫時，可以設定網路規則，以管理來自特定網路位置的協助工具</span><span class="sxs-lookup"><span data-stu-id="36b42-187">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="36b42-188">已新增攜帶您自己的金鑰 (BYOK) 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-188">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="36b42-189">'Add-AzKeyVaultKey' 支援產生金鑰交換金鑰</span><span class="sxs-lookup"><span data-stu-id="36b42-189">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="36b42-190">'Get-AzKeyVaultKey' 支援以 PEM 格式下載公開金鑰</span><span class="sxs-lookup"><span data-stu-id="36b42-190">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="36b42-191">已更新 'Add-AzKeyVaultKey' 說明文件的 'KeyOps' 部分</span><span class="sxs-lookup"><span data-stu-id="36b42-191">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36b42-192">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-192">Az.Monitor</span></span>
* <span data-ttu-id="36b42-193">已修正 'AzDiagnosticSettings' 的下列錯誤 (bug)：保留原則不會套用到所有類別 [#11589]</span><span class="sxs-lookup"><span data-stu-id="36b42-193">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="36b42-194">計量警示 V2 支援 WebTest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="36b42-194">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="36b42-195">'New-AzMetricAlertRuleV2Criteria'：已新增建立 webtest 可用性準則的選項</span><span class="sxs-lookup"><span data-stu-id="36b42-195">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="36b42-196">'Add-AzMetricAlertRuleV2'：支援新的 webtest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="36b42-196">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="36b42-197">已移除 PSLogProfile 中 RetentionPolicy 的備援定義 [#7608]</span><span class="sxs-lookup"><span data-stu-id="36b42-197">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="36b42-198">已移除 PSEventData 中定義的備援屬性 [#11353]</span><span class="sxs-lookup"><span data-stu-id="36b42-198">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="36b42-199">已將 'Get-AzLog' 重新命名為 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="36b42-199">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-200">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-200">Az.Network</span></span>
* <span data-ttu-id="36b42-201">已新增重大變更屬性，以通知區域預設行為將會變更</span><span class="sxs-lookup"><span data-stu-id="36b42-201">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="36b42-202">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="36b42-202">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="36b42-203">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="36b42-203">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="36b42-204">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="36b42-204">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="36b42-205">已新增最上層資源 SecurityPartnerProvider 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-205">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="36b42-206">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-206">New cmdlets added:</span></span>
        - <span data-ttu-id="36b42-207">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="36b42-207">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="36b42-208">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="36b42-208">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="36b42-209">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="36b42-209">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="36b42-210">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="36b42-210">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="36b42-211">已在 'PSPrivateLinkResource' 上新增 'RequiredZoneNames'，並在 'PSPrivateEndpointConnection' 上新增 'GroupId'</span><span class="sxs-lookup"><span data-stu-id="36b42-211">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="36b42-212">已針對 New-AzNetworkWatcherConnectionMonitorTestConfigurationObject 修正 SuccessThresholdRoundTripTimeMs 參數的不正確類型</span><span class="sxs-lookup"><span data-stu-id="36b42-212">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="36b42-213">已更新 VirtualWan Cmdlet，將 AllowVnetToVnetTraffic 引數的預設值設為 True。</span><span class="sxs-lookup"><span data-stu-id="36b42-213">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="36b42-214">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="36b42-214">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="36b42-215">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="36b42-215">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="36b42-216">已新增 Cmdlet 來支援私人端點的 DNS 區域群組</span><span class="sxs-lookup"><span data-stu-id="36b42-216">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="36b42-217">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="36b42-217">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="36b42-218">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="36b42-218">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="36b42-219">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="36b42-219">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="36b42-220">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="36b42-220">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="36b42-221">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="36b42-221">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="36b42-222">已將 'DNSEnableProxy'、'DNSRequireProxyForNetworkRules' 和 'DNSServers' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="36b42-222">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="36b42-223">已將 'EnableDnsProxy'、'DnsProxyNotRequiredForNetworkRule' 和 'DnsServer' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="36b42-223">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="36b42-224">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-224">Updated cmdlet:</span></span>
        - <span data-ttu-id="36b42-225">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="36b42-225">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36b42-226">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-226">Az.OperationalInsights</span></span>
* <span data-ttu-id="36b42-227">已更新舊版程式碼以套用新產生的 SDK</span><span class="sxs-lookup"><span data-stu-id="36b42-227">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="36b42-228">由於已取代 API，刪除了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-228">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="36b42-229">'Get-AzOperationalInsightsSavedSearchResult' (別名 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="36b42-229">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="36b42-230">'Get-AzOperationalInsightsSearchResult' (別名 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="36b42-230">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="36b42-231">'Get-AzOperationalInsightsLinkTarget' (別名 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="36b42-231">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="36b42-232">已新增 'Set-AzOperationalInsightsWorkspace' 和 'New-AzOperationalInsightsWorkspace' 的參數</span><span class="sxs-lookup"><span data-stu-id="36b42-232">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="36b42-233">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-233">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="36b42-234">已針對叢集和連結服務建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-234">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-235">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-235">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-236">Azure Site Recovery 已將保護 Azure 鄰近放置群組虛擬機器的支援新增至 Azure 提供者。</span><span class="sxs-lookup"><span data-stu-id="36b42-236">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="36b42-237">Azure Site Recovery 已將區域的支援新增至區域複本。</span><span class="sxs-lookup"><span data-stu-id="36b42-237">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="36b42-238">Azure 備份已新增適用於 Azure FileShare 復原點的長期保留支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-238">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="36b42-239">Azure 備份已將磁片排除屬性新增至 'Get-AzRecoveryServicesBackupItem' Cmdlet 輸出。</span><span class="sxs-lookup"><span data-stu-id="36b42-239">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="36b42-240">已針對站台復原服務新增保存庫認證檔的私人端點。</span><span class="sxs-lookup"><span data-stu-id="36b42-240">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-241">Az.Resources</span></span>
* <span data-ttu-id="36b42-242">已新增有關在建立新角色定義時檢視延遲的訊息警告</span><span class="sxs-lookup"><span data-stu-id="36b42-242">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="36b42-243">已變更原則 Cmdlet 以輸出強型別物件</span><span class="sxs-lookup"><span data-stu-id="36b42-243">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="36b42-244">已移除用於 'Get-AzResourceLock' Cmdlet 的 '-TenantLevel ' 參數 [#11335]</span><span class="sxs-lookup"><span data-stu-id="36b42-244">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="36b42-245">已修正 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span><span class="sxs-lookup"><span data-stu-id="36b42-245">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="36b42-246">已新增在資源群組範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="36b42-246">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="36b42-247">已新增在訂用帳戶範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="36b42-247">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="36b42-248">Alias:'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="36b42-248">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="36b42-249">已覆寫 'New-AzDeployment' 和 'New-AzResourceGroupDeployment' 的 '-WhatIf' 和 '-Confirm' 參數，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="36b42-249">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="36b42-250">已在部署 Cmdlet 中新增 'ApiVersion' 參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="36b42-250">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="36b42-251">已新增為部署失敗顯示已改善錯誤訊息的功能</span><span class="sxs-lookup"><span data-stu-id="36b42-251">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="36b42-252">已新增針對部署失敗記錄的 correlationId</span><span class="sxs-lookup"><span data-stu-id="36b42-252">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="36b42-253">已將 'error' 屬性新增至部署指令碼輸出</span><span class="sxs-lookup"><span data-stu-id="36b42-253">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="36b42-254">已將 nuget Microsoft.Azure.Management.ResourceManager 更新為 '3.7.1-preview'</span><span class="sxs-lookup"><span data-stu-id="36b42-254">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="36b42-255">當 DeploymentValidateResult 中的 Error 屬性變更為唯讀時，已從 nuget 3.7.1-preview 中移除特定測試案例</span><span class="sxs-lookup"><span data-stu-id="36b42-255">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="36b42-256">已從 SDK ResourceManager 3.7.1-preview 引進 GenericResourceExpanded</span><span class="sxs-lookup"><span data-stu-id="36b42-256">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="36b42-257">已針對用於部署的所有 Get Cmdlet 以及下列 Cmdlet 新增標籤支援：</span><span class="sxs-lookup"><span data-stu-id="36b42-257">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="36b42-258">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="36b42-258">'New-AzDeployment'</span></span>
    - <span data-ttu-id="36b42-259">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="36b42-259">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="36b42-260">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="36b42-260">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="36b42-261">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="36b42-261">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36b42-262">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36b42-262">Az.ServiceFabric</span></span>
* <span data-ttu-id="36b42-263">已修正下列錯誤 (bug)：使用 --SecretIdentifier 新增憑證時取得錯誤憑證指紋</span><span class="sxs-lookup"><span data-stu-id="36b42-263">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-264">Az.Sql</span></span>
* <span data-ttu-id="36b42-265">增強下列項目的效能：</span><span class="sxs-lookup"><span data-stu-id="36b42-265">Enhance performance of:</span></span>
    - <span data-ttu-id="36b42-266">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="36b42-266">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="36b42-267">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="36b42-267">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="36b42-268">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="36b42-268">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="36b42-269">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="36b42-269">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="36b42-270">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="36b42-270">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="36b42-271">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="36b42-271">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="36b42-272">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="36b42-272">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="36b42-273">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="36b42-273">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="36b42-274">已從 Cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' 移除 'RetentionDays' 參數的用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="36b42-274">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="36b42-275">在 Vnet 中對儲存體帳戶進行稽核時，修正在建立儲存體 Blob 資料參與者角色時發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="36b42-275">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-276">Az.Storage</span></span>
* <span data-ttu-id="36b42-277">已新增 '-AsJob' 以取得/列出帳戶 Cmdlet 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36b42-277">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="36b42-278">使用 KeyvaultEncryption 更新儲存體帳戶以支援金鑰自動輪替時，使 KeyVersion 成為選用項目</span><span class="sxs-lookup"><span data-stu-id="36b42-278">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="36b42-279">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36b42-279">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="36b42-280">已修正由於管道無法移除 Azure 檔案目錄的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-280">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="36b42-281">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="36b42-281">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="36b42-282">已修正 [#9880]：變更 NetWorkRule DefaultAction 值定義以符合 Swagger。</span><span class="sxs-lookup"><span data-stu-id="36b42-282">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="36b42-283">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="36b42-283">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="36b42-284">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="36b42-284">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="36b42-285">已修正 [#11624]：新增 NetworkRules 時跳過重複的規則，以避免伺服器失敗</span><span class="sxs-lookup"><span data-stu-id="36b42-285">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="36b42-286">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="36b42-286">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="36b42-287">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.7</span><span class="sxs-lookup"><span data-stu-id="36b42-287">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="36b42-288">已新增警告訊息，以在清單 DataLake Gen2 項目中只傳回部分項目時，提醒使用者再次與 ContinuationToken 一起列出</span><span class="sxs-lookup"><span data-stu-id="36b42-288">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="36b42-289">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="36b42-289">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="36b42-290">已支援使用 Azure Files Active Directory 網域服務驗證來建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="36b42-290">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="36b42-291">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36b42-291">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="36b42-292">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36b42-292">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="36b42-293">支援新增或列出儲存體帳戶的 Kerberos 金鑰</span><span class="sxs-lookup"><span data-stu-id="36b42-293">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="36b42-294">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="36b42-294">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="36b42-295">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="36b42-295">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="36b42-296">支援容錯移轉儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="36b42-296">Supported failover Storage account</span></span>
    - <span data-ttu-id="36b42-297">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="36b42-297">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="36b42-298">已更新 'Get-AzStorageBlobCopyState' 的說明</span><span class="sxs-lookup"><span data-stu-id="36b42-298">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="36b42-299">已更新 'Get-AzStorageFileCopyState' 和 'Start-AzStorageBlobCopy' 的說明</span><span class="sxs-lookup"><span data-stu-id="36b42-299">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="36b42-300">已將儲存體用戶端程式庫 v12 整合到佇列和檔案 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-300">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="36b42-301">已將輸出類型從 CloudFile 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="36b42-301">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="36b42-302">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="36b42-302">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="36b42-303">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="36b42-303">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="36b42-304">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="36b42-304">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="36b42-305">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="36b42-305">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="36b42-306">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="36b42-306">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="36b42-307">已將輸出類型從 CloudFileDirectory 變更為 AzureStorageFileDirectory，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="36b42-307">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="36b42-308">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="36b42-308">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="36b42-309">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="36b42-309">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="36b42-310">已將輸出類型從 CloudFileShare 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="36b42-310">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="36b42-311">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="36b42-311">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="36b42-312">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="36b42-312">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="36b42-313">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="36b42-313">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="36b42-314">已將輸出類型從 FileShareProperties 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="36b42-314">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="36b42-315">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="36b42-315">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="36b42-316">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="36b42-316">Az.TrafficManager</span></span>
* <span data-ttu-id="36b42-317">已修正 'DisableAzureTrafficManagerEndpoint' 詳細資訊輸出中不正確的設定檔名稱</span><span class="sxs-lookup"><span data-stu-id="36b42-317">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-318">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-318">Az.Websites</span></span>
* <span data-ttu-id="36b42-319">已修正 'Update-AzWebAppAccessRestrictionConfig' 說明上的錯字。</span><span class="sxs-lookup"><span data-stu-id="36b42-319">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="36b42-320">3.8.0 - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="36b42-320">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="36b42-321">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="36b42-321">Highlights since the last release</span></span>
* <span data-ttu-id="36b42-322">Az.Storage 支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="36b42-322">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36b42-323">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-323">Az.Accounts</span></span>
* <span data-ttu-id="36b42-324">更新 'Resolve-AzError' 中的 Azure PowerShell 問卷 URL [#11507]</span><span class="sxs-lookup"><span data-stu-id="36b42-324">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36b42-325">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36b42-325">Az.ApiManagement</span></span>
* <span data-ttu-id="36b42-326">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="36b42-326">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="36b42-327">'Set-AzApiManagementGroup' 已更新文件以指定 GroupId 參數</span><span class="sxs-lookup"><span data-stu-id="36b42-327">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="36b42-328">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36b42-328">Az.Cdn</span></span>
* <span data-ttu-id="36b42-329">已修正 ChinaCDN 相關的定價 SKU 顯示</span><span class="sxs-lookup"><span data-stu-id="36b42-329">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36b42-330">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36b42-330">Az.CognitiveServices</span></span>
* <span data-ttu-id="36b42-331">支援身分識別、加密、UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="36b42-331">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-332">Az.Compute</span></span>
* <span data-ttu-id="36b42-333">已新增 'Set-AzVmssOrchestrationServiceState' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b42-333">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="36b42-334">具有 -InstanceView 的 'Get-AzVmss' 會顯示 OrchestrationService 狀態。</span><span class="sxs-lookup"><span data-stu-id="36b42-334">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36b42-335">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36b42-335">Az.IotHub</span></span>
* <span data-ttu-id="36b42-336">管理 IoT 裝置對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="36b42-336">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="36b42-337">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="36b42-337">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="36b42-338">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="36b42-338">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="36b42-339">已新增 Cmdlet，可在 IoT 中樞的裝置上叫用直接方法。</span><span class="sxs-lookup"><span data-stu-id="36b42-339">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="36b42-340">管理 IoT 裝置模組對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="36b42-340">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="36b42-341">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="36b42-341">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="36b42-342">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="36b42-342">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="36b42-343">大規模管理 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="36b42-343">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="36b42-344">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="36b42-344">New cmdlets are:</span></span>
    - <span data-ttu-id="36b42-345">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="36b42-345">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="36b42-346">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="36b42-346">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="36b42-347">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="36b42-347">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="36b42-348">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="36b42-348">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="36b42-349">已新增 Cmdlet，叫用 IoT 中樞的邊緣模組方法。</span><span class="sxs-lookup"><span data-stu-id="36b42-349">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36b42-350">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36b42-350">Az.KeyVault</span></span>
* <span data-ttu-id="36b42-351">已新增可在保存庫上啟用虛刪除和清除保護的新 Cmdlet 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="36b42-351">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="36b42-352">已將支援新增至 Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="36b42-352">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="36b42-353">已修正 'Remove-AzKeyVaultManagedStorageSasDefinition' 範例中的錯誤 [#11479]</span><span class="sxs-lookup"><span data-stu-id="36b42-353">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="36b42-354">已將支援新增至私人端點</span><span class="sxs-lookup"><span data-stu-id="36b42-354">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="36b42-355">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="36b42-355">Az.Maintenance</span></span>
* <span data-ttu-id="36b42-356">發行用於 GA 的維護 Cmdlet 版本</span><span class="sxs-lookup"><span data-stu-id="36b42-356">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36b42-357">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-357">Az.Monitor</span></span>
* <span data-ttu-id="36b42-358">已新增私人連結範圍的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-358">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="36b42-359">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="36b42-359">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="36b42-360">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="36b42-360">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="36b42-361">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="36b42-361">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="36b42-362">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="36b42-362">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="36b42-363">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="36b42-363">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="36b42-364">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="36b42-364">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="36b42-365">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="36b42-365">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-366">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-366">Az.Network</span></span>
* <span data-ttu-id="36b42-367">已更新 Cmdlet，可在私人 IP 上啟用虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="36b42-367">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="36b42-368">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="36b42-368">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="36b42-369">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="36b42-369">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="36b42-370">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="36b42-370">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="36b42-371">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="36b42-371">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="36b42-372">已更新 Cmdlet，可啟用以 FQDN 為基礎的 LocalNetworkGateways 和 VpnSites</span><span class="sxs-lookup"><span data-stu-id="36b42-372">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="36b42-373">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="36b42-373">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="36b42-374">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="36b42-374">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="36b42-375">已在 ExpressRouteCircuitConnectionConfig 中新增對 IPv6 位址系列的支援 (全球適用)</span><span class="sxs-lookup"><span data-stu-id="36b42-375">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="36b42-376">已新增 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="36b42-376">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="36b42-377">允許設定所有現有屬性，包括 IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="36b42-377">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="36b42-378">已更新 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="36b42-378">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="36b42-379">已新增另一個選擇性參數 AddressPrefixType 來指定位址首碼的位址系列</span><span class="sxs-lookup"><span data-stu-id="36b42-379">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="36b42-380">已更新 Cmdlet，可啟用虛擬網路閘道連線上的 DPD 逾時設定。</span><span class="sxs-lookup"><span data-stu-id="36b42-380">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="36b42-381">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-381">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="36b42-382">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-382">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36b42-383">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-383">Az.PolicyInsights</span></span>
* <span data-ttu-id="36b42-384">已新增用於觸發原則合規性掃描的 'Start-AzPolicyComplianceScan' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-384">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="36b42-385">已將原則定義、設定定義和指派版本新增至 'Get-AzPolicyState' 輸出</span><span class="sxs-lookup"><span data-stu-id="36b42-385">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36b42-386">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36b42-386">Az.ServiceFabric</span></span>
* <span data-ttu-id="36b42-387">已改善 'New-AzServiceFabricCluster' 範例的程式碼格式設定和可用性</span><span class="sxs-lookup"><span data-stu-id="36b42-387">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-388">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-388">Az.Sql</span></span>
* <span data-ttu-id="36b42-389">已新增 'Get-AzSqlInstanceOperation' 和 'Stop-AzSqlInstanceOperation' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-389">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="36b42-390">支援對 VNet 中的儲存體帳戶進行稽核。</span><span class="sxs-lookup"><span data-stu-id="36b42-390">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-391">Az.Storage</span></span>
* <span data-ttu-id="36b42-392">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="36b42-392">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="36b42-393">建立/更新儲存體帳戶時，支援新的 SkuName StandardGZRS、StandardRAGZRS</span><span class="sxs-lookup"><span data-stu-id="36b42-393">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="36b42-394">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36b42-394">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="36b42-395">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36b42-395">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="36b42-396">支援 DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="36b42-396">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="36b42-397">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="36b42-397">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="36b42-398">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="36b42-398">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="36b42-399">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="36b42-399">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="36b42-400">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="36b42-400">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="36b42-401">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="36b42-401">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="36b42-402">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="36b42-402">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="36b42-403">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="36b42-403">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="36b42-404">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="36b42-404">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="36b42-405">0.10.0-preview - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="36b42-405">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="36b42-406">一般</span><span class="sxs-lookup"><span data-stu-id="36b42-406">General</span></span>
* <span data-ttu-id="36b42-407">Az 模組現已在 Azure Stack Hub 中提供預覽。</span><span class="sxs-lookup"><span data-stu-id="36b42-407">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="36b42-408">此模組具有 Linux 和 macOs 的跨平台相容性。</span><span class="sxs-lookup"><span data-stu-id="36b42-408">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="36b42-409">Azure Stack Hub 現在支援使用 Az 模組的 PowerShell Core，如需詳細資訊，請參閱[這裡](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="36b42-409">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="36b42-410">Az 模組支援 2019-03-01-hybrid 設定檔：</span><span class="sxs-lookup"><span data-stu-id="36b42-410">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="36b42-411">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="36b42-411">Az.Billing</span></span>
  - <span data-ttu-id="36b42-412">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-412">Az.Compute</span></span>
  - <span data-ttu-id="36b42-413">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="36b42-413">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="36b42-414">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36b42-414">Az.EventHub</span></span>
  - <span data-ttu-id="36b42-415">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36b42-415">Az.IotHub</span></span>
  - <span data-ttu-id="36b42-416">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36b42-416">Az.KeyVault</span></span>
  - <span data-ttu-id="36b42-417">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-417">Az.Monitor</span></span>
  - <span data-ttu-id="36b42-418">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-418">Az.Network</span></span>
  - <span data-ttu-id="36b42-419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-419">Az.Resources</span></span>
  - <span data-ttu-id="36b42-420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-420">Az.Storage</span></span>
  - <span data-ttu-id="36b42-421">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-421">Az.Websites</span></span>
* <span data-ttu-id="36b42-422">已引進三個可搭配 Azure Stack Hub 且適用於 az 的新 PowerShell 模組，包括 Az.Databox、Az.IotHub 和 Az. EventHub</span><span class="sxs-lookup"><span data-stu-id="36b42-422">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="36b42-423">命令維持不變，但有次要變更，例如將 AzureRM 變更為 Az</span><span class="sxs-lookup"><span data-stu-id="36b42-423">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="36b42-424">您可以在[這裡](https://aka.ms/InstallASHPowerShell)找到 Azure Stack Hub 的 PowerShell 文件更新連結</span><span class="sxs-lookup"><span data-stu-id="36b42-424">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="36b42-425">3.7.0 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="36b42-425">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36b42-426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-426">Az.Accounts</span></span>
* <span data-ttu-id="36b42-427">已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]</span><span class="sxs-lookup"><span data-stu-id="36b42-427">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-428">Az.Compute</span></span>
* <span data-ttu-id="36b42-429">已將下列參數新增至 'New-AzDiskConfig' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-429">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="36b42-430">DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="36b42-430">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="36b42-431">允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。</span><span class="sxs-lookup"><span data-stu-id="36b42-431">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="36b42-432">已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。</span><span class="sxs-lookup"><span data-stu-id="36b42-432">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="36b42-433">[#11354]</span><span class="sxs-lookup"><span data-stu-id="36b42-433">[#11354]</span></span>
* <span data-ttu-id="36b42-434">已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-434">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="36b42-435">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="36b42-435">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="36b42-436">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="36b42-436">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="36b42-437">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="36b42-437">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="36b42-438">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="36b42-438">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="36b42-439">已修正說明文件範例中的錯誤</span><span class="sxs-lookup"><span data-stu-id="36b42-439">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="36b42-440">以表格格式顯示 VM PowerState 的確切字串值。</span><span class="sxs-lookup"><span data-stu-id="36b42-440">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="36b42-441">'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。</span><span class="sxs-lookup"><span data-stu-id="36b42-441">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="36b42-442">[#11257]</span><span class="sxs-lookup"><span data-stu-id="36b42-442">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-443">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-443">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-444">已將 ADF .Net SDK 版本更新為 4.8.0</span><span class="sxs-lookup"><span data-stu-id="36b42-444">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="36b42-445">已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行</span><span class="sxs-lookup"><span data-stu-id="36b42-445">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36b42-446">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-446">Az.DataLakeStore</span></span>
* <span data-ttu-id="36b42-447">已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述</span><span class="sxs-lookup"><span data-stu-id="36b42-447">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="36b42-448">已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項</span><span class="sxs-lookup"><span data-stu-id="36b42-448">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36b42-449">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36b42-449">Az.HDInsight</span></span>
* <span data-ttu-id="36b42-450">支援在建立叢集時指定支援的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="36b42-450">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36b42-451">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36b42-451">Az.IotHub</span></span>
* <span data-ttu-id="36b42-452">已新增管理每一部裝置的分散式設定支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-452">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="36b42-453">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="36b42-453">New Cmdlets are:</span></span>
    - <span data-ttu-id="36b42-454">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="36b42-454">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="36b42-455">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="36b42-455">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36b42-456">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36b42-456">Az.KeyVault</span></span>
* <span data-ttu-id="36b42-457">已將中斷性變更屬性新增至 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="36b42-457">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36b42-458">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-458">Az.Monitor</span></span>
* <span data-ttu-id="36b42-459">已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件</span><span class="sxs-lookup"><span data-stu-id="36b42-459">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-460">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-460">Az.Network</span></span>
* <span data-ttu-id="36b42-461">已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections</span><span class="sxs-lookup"><span data-stu-id="36b42-461">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="36b42-462">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="36b42-462">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="36b42-463">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="36b42-463">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="36b42-464">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="36b42-464">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="36b42-465">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="36b42-465">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="36b42-466">已移除 SQL 管理 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="36b42-466">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36b42-467">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-467">Az.PolicyInsights</span></span>
* <span data-ttu-id="36b42-468">改善錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="36b42-468">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-469">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-470">Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。</span><span class="sxs-lookup"><span data-stu-id="36b42-470">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="36b42-471">已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視</span><span class="sxs-lookup"><span data-stu-id="36b42-471">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="36b42-472">Azure 備份已新增針對失敗項目重試原則更新的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-472">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="36b42-473">Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-473">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="36b42-474">Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-474">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="36b42-475">Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-475">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-476">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-476">Az.Resources</span></span>
* <span data-ttu-id="36b42-477">已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="36b42-477">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="36b42-478">已新增對於錯誤案例的 correlationId 記錄</span><span class="sxs-lookup"><span data-stu-id="36b42-478">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="36b42-479">小型文件變更為 'Get-AzResourceLock'。</span><span class="sxs-lookup"><span data-stu-id="36b42-479">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="36b42-480">已新增範例。</span><span class="sxs-lookup"><span data-stu-id="36b42-480">Added example.</span></span>
* <span data-ttu-id="36b42-481">已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]</span><span class="sxs-lookup"><span data-stu-id="36b42-481">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="36b42-482">已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-482">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-483">Az.Sql</span></span>
* <span data-ttu-id="36b42-484">已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="36b42-484">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="36b42-485">已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="36b42-485">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="36b42-486">已儲存在資料庫中分類資料行時的敏感度等級。</span><span class="sxs-lookup"><span data-stu-id="36b42-486">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="36b42-487">Az.Support</span><span class="sxs-lookup"><span data-stu-id="36b42-487">Az.Support</span></span>
* <span data-ttu-id="36b42-488">'Az.Support' 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="36b42-488">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-489">Az.Websites</span></span>
* <span data-ttu-id="36b42-490">已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-490">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="36b42-491">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="36b42-491">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="36b42-492">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="36b42-492">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="36b42-493">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="36b42-493">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="36b42-494">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="36b42-494">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="36b42-495">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="36b42-495">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36b42-496">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-496">Az.Accounts</span></span>
* <span data-ttu-id="36b42-497">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="36b42-497">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="36b42-498">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="36b42-498">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="36b42-499">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="36b42-499">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36b42-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36b42-500">Az.ApiManagement</span></span>
* <span data-ttu-id="36b42-501">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="36b42-501">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="36b42-502">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="36b42-502">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="36b42-503">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-503">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="36b42-504">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="36b42-504">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36b42-505">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-505">Az.DataLakeStore</span></span>
* <span data-ttu-id="36b42-506">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="36b42-506">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36b42-507">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36b42-507">Az.IotHub</span></span>
* <span data-ttu-id="36b42-508">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-508">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="36b42-509">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="36b42-509">New Cmdlets are:</span></span>
    - <span data-ttu-id="36b42-510">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36b42-510">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="36b42-511">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36b42-511">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="36b42-512">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36b42-512">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="36b42-513">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36b42-513">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="36b42-514">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-514">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="36b42-515">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="36b42-515">New Cmdlets are:</span></span>
    - <span data-ttu-id="36b42-516">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="36b42-516">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="36b42-517">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="36b42-517">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="36b42-518">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="36b42-518">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="36b42-519">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="36b42-519">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="36b42-520">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="36b42-520">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="36b42-521">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="36b42-521">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="36b42-522">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-522">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="36b42-523">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="36b42-523">New Cmdlets are:</span></span>
    - <span data-ttu-id="36b42-524">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="36b42-524">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="36b42-525">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="36b42-525">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="36b42-526">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-526">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36b42-527">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-527">Az.Monitor</span></span>
* <span data-ttu-id="36b42-528">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="36b42-528">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-529">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-529">Az.Network</span></span>
* <span data-ttu-id="36b42-530">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="36b42-530">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="36b42-531">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="36b42-531">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="36b42-532">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="36b42-532">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="36b42-533">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="36b42-533">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-534">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-534">Az.Resources</span></span>
* <span data-ttu-id="36b42-535">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="36b42-535">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="36b42-536">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="36b42-536">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="36b42-537">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="36b42-537">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="36b42-538">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="36b42-538">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="36b42-539">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="36b42-539">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="36b42-540">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="36b42-540">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="36b42-541">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="36b42-541">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="36b42-542">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="36b42-542">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="36b42-543">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="36b42-543">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="36b42-544">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="36b42-544">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="36b42-545">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="36b42-545">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="36b42-546">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-546">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="36b42-547">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="36b42-547">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="36b42-548">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="36b42-548">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-549">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-549">Az.Sql</span></span>
* <span data-ttu-id="36b42-550">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="36b42-550">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="36b42-551">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-551">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="36b42-552">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="36b42-552">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="36b42-553">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="36b42-553">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="36b42-554">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="36b42-554">Remove an LTR backup</span></span>
    - <span data-ttu-id="36b42-555">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="36b42-555">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="36b42-556">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="36b42-556">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="36b42-557">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="36b42-557">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="36b42-558">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="36b42-558">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-559">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-559">Az.Storage</span></span>
* <span data-ttu-id="36b42-560">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="36b42-560">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="36b42-561">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="36b42-561">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="36b42-562">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="36b42-562">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="36b42-563">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="36b42-563">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="36b42-564">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="36b42-564">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-565">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-565">Az.Websites</span></span>
* <span data-ttu-id="36b42-566">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="36b42-566">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="36b42-567">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-567">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="36b42-568">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="36b42-568">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="36b42-569">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="36b42-569">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="36b42-570">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-570">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="36b42-571">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="36b42-571">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="36b42-572">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="36b42-572">Highlights since the last major release</span></span>
* <span data-ttu-id="36b42-573">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="36b42-573">Updated client side telemetry.</span></span>
* <span data-ttu-id="36b42-574">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="36b42-574">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="36b42-575">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b42-575">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36b42-576">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-576">Az.Accounts</span></span>
* <span data-ttu-id="36b42-577">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="36b42-577">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36b42-578">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36b42-578">Az.Automation</span></span>
* <span data-ttu-id="36b42-579">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="36b42-579">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36b42-580">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36b42-580">Az.CognitiveServices</span></span>
* <span data-ttu-id="36b42-581">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="36b42-581">Updated SDK to 7.0</span></span>
* <span data-ttu-id="36b42-582">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="36b42-582">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-583">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-583">Az.Compute</span></span>
* <span data-ttu-id="36b42-584">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="36b42-584">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="36b42-585">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36b42-585">Az.FrontDoor</span></span>
* <span data-ttu-id="36b42-586">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="36b42-586">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36b42-587">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36b42-587">Az.IotHub</span></span>
* <span data-ttu-id="36b42-588">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-588">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="36b42-589">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="36b42-589">New Cmdlets are:</span></span>
    - <span data-ttu-id="36b42-590">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36b42-590">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="36b42-591">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36b42-591">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="36b42-592">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36b42-592">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="36b42-593">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36b42-593">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36b42-594">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36b42-594">Az.KeyVault</span></span>
* <span data-ttu-id="36b42-595">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="36b42-595">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36b42-596">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-596">Az.Monitor</span></span>
* <span data-ttu-id="36b42-597">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="36b42-597">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="36b42-598">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="36b42-598">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="36b42-599">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="36b42-599">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-600">Az.Network</span></span>
* <span data-ttu-id="36b42-601">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="36b42-601">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="36b42-602">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="36b42-602">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="36b42-603">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="36b42-603">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="36b42-604">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="36b42-604">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="36b42-605">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b42-605">No new cmdlets are added.</span></span> <span data-ttu-id="36b42-606">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="36b42-606">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-607">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-607">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-608">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-608">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-609">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-609">Az.Resources</span></span>
* <span data-ttu-id="36b42-610">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-610">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="36b42-611">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="36b42-611">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="36b42-612">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="36b42-612">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="36b42-613">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="36b42-613">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="36b42-614">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="36b42-614">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="36b42-615">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="36b42-615">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="36b42-616">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="36b42-616">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="36b42-617">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="36b42-617">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-618">Az.Sql</span></span>
* <span data-ttu-id="36b42-619">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-619">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="36b42-620">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-620">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="36b42-621">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="36b42-621">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="36b42-622">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="36b42-622">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="36b42-623">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-623">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="36b42-624">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="36b42-624">Az.StorageSync</span></span>
* <span data-ttu-id="36b42-625">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="36b42-625">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="36b42-626">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="36b42-626">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="36b42-627">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="36b42-627">Highlights since the last major release</span></span>
* <span data-ttu-id="36b42-628">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="36b42-628">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="36b42-629">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="36b42-629">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36b42-630">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-630">Az.Accounts</span></span>
* <span data-ttu-id="36b42-631">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="36b42-631">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="36b42-632">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="36b42-632">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36b42-633">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36b42-633">Az.ApiManagement</span></span>
* <span data-ttu-id="36b42-634">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="36b42-634">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="36b42-635">**New-AzApiManagementProduct**\* 和 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="36b42-635">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="36b42-636">https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="36b42-636">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="36b42-637">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="36b42-637">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-638">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-638">Az.Compute</span></span>
* <span data-ttu-id="36b42-639">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="36b42-639">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="36b42-640">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-640">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="36b42-641">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-641">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="36b42-642">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-642">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="36b42-643">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b42-643">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-644">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-644">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-645">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="36b42-645">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="36b42-646">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="36b42-646">Az.DeploymentManager</span></span>
* <span data-ttu-id="36b42-647">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="36b42-647">Adds LIST operations for resources</span></span>
* <span data-ttu-id="36b42-648">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="36b42-648">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36b42-649">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36b42-649">Az.HDInsight</span></span>
* <span data-ttu-id="36b42-650">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="36b42-650">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36b42-651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36b42-651">Az.KeyVault</span></span>
* <span data-ttu-id="36b42-652">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="36b42-652">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-653">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-653">Az.Network</span></span>
* <span data-ttu-id="36b42-654">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="36b42-654">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="36b42-655">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="36b42-655">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="36b42-656">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-656">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="36b42-657">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="36b42-657">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="36b42-658">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="36b42-658">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="36b42-659">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="36b42-659">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="36b42-660">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="36b42-660">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="36b42-661">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-661">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="36b42-662">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-662">New cmdlets added:</span></span>
        - <span data-ttu-id="36b42-663">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="36b42-663">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="36b42-664">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-664">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="36b42-665">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="36b42-665">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="36b42-666">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-666">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36b42-667">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-667">Az.PolicyInsights</span></span>
* <span data-ttu-id="36b42-668">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="36b42-668">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="36b42-669">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="36b42-669">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="36b42-670">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="36b42-670">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="36b42-671">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="36b42-671">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-672">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-673">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="36b42-673">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="36b42-674">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-674">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-675">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-675">Az.Resources</span></span>
* <span data-ttu-id="36b42-676">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="36b42-676">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="36b42-677">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="36b42-677">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-678">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-678">Az.Sql</span></span>
<span data-ttu-id="36b42-679">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="36b42-679">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-680">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-680">Az.Storage</span></span>
* <span data-ttu-id="36b42-681">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="36b42-681">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="36b42-682">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36b42-682">New-AzStorageAccount</span></span>
* <span data-ttu-id="36b42-683">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="36b42-683">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="36b42-684">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="36b42-684">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-685">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-685">Az.Websites</span></span>
* <span data-ttu-id="36b42-686">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="36b42-686">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="36b42-687">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-687">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="36b42-688">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="36b42-688">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36b42-689">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-689">Az.Accounts</span></span>
* <span data-ttu-id="36b42-690">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="36b42-690">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="36b42-691">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36b42-691">Az.Cdn</span></span>
* <span data-ttu-id="36b42-692">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="36b42-692">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-693">Az.Compute</span></span>
* <span data-ttu-id="36b42-694">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b42-694">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="36b42-695">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="36b42-695">Az.ContainerInstance</span></span>
* <span data-ttu-id="36b42-696">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="36b42-696">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="36b42-697">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="36b42-697">Az.DataBoxEdge</span></span>
* <span data-ttu-id="36b42-698">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="36b42-698">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="36b42-699">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="36b42-699">Get the Edge Storage Container</span></span>
* <span data-ttu-id="36b42-700">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="36b42-700">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="36b42-701">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="36b42-701">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="36b42-702">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="36b42-702">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="36b42-703">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="36b42-703">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="36b42-704">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="36b42-704">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="36b42-705">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="36b42-705">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="36b42-706">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36b42-706">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="36b42-707">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="36b42-707">Get the Edge Storage Account</span></span>
* <span data-ttu-id="36b42-708">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36b42-708">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="36b42-709">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="36b42-709">Create new Edge Storage Account</span></span>
* <span data-ttu-id="36b42-710">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36b42-710">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="36b42-711">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="36b42-711">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="36b42-712">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="36b42-712">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="36b42-713">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="36b42-713">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="36b42-714">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="36b42-714">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="36b42-715">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="36b42-715">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-716">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-716">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-717">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="36b42-717">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="36b42-718">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="36b42-718">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="36b42-719">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="36b42-719">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="36b42-720">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="36b42-720">Az.DevTestLabs</span></span>
* <span data-ttu-id="36b42-721">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="36b42-721">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36b42-722">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36b42-722">Az.EventHub</span></span>
* <span data-ttu-id="36b42-723">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="36b42-723">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36b42-724">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36b42-724">Az.HDInsight</span></span>
* <span data-ttu-id="36b42-725">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="36b42-725">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="36b42-726">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="36b42-726">Az.MachineLearning</span></span>
* <span data-ttu-id="36b42-727">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-727">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="36b42-728">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="36b42-728">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="36b42-729">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="36b42-729">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="36b42-730">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="36b42-730">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="36b42-731">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="36b42-731">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="36b42-732">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="36b42-732">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="36b42-733">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="36b42-733">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="36b42-734">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="36b42-734">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-735">Az.Network</span></span>
* <span data-ttu-id="36b42-736">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="36b42-736">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-737">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-737">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-738">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="36b42-738">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="36b42-739">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="36b42-739">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="36b42-740">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="36b42-740">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="36b42-741">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="36b42-741">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-742">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-742">Az.Resources</span></span>
* <span data-ttu-id="36b42-743">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="36b42-743">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-744">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-744">Az.Sql</span></span>
* <span data-ttu-id="36b42-745">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="36b42-745">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="36b42-746">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="36b42-746">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="36b42-747">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="36b42-747">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="36b42-748">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="36b42-748">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-749">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-749">Az.Storage</span></span>
* <span data-ttu-id="36b42-750">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="36b42-750">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="36b42-751">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="36b42-751">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="36b42-752">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="36b42-752">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="36b42-753">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36b42-753">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="36b42-754">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="36b42-754">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="36b42-755">一般</span><span class="sxs-lookup"><span data-stu-id="36b42-755">General</span></span>
* <span data-ttu-id="36b42-756">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="36b42-756">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36b42-757">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-757">Az.Accounts</span></span>
* <span data-ttu-id="36b42-758">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="36b42-758">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="36b42-759">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="36b42-759">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="36b42-760">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36b42-760">Az.Batch</span></span>
* <span data-ttu-id="36b42-761">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="36b42-761">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-762">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-762">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-763">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="36b42-763">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="36b42-764">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36b42-764">Az.FrontDoor</span></span>
* <span data-ttu-id="36b42-765">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="36b42-765">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="36b42-766">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="36b42-766">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="36b42-767">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="36b42-767">Az.HealthcareApis</span></span>
* <span data-ttu-id="36b42-768">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="36b42-768">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36b42-769">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36b42-769">Az.KeyVault</span></span>
* <span data-ttu-id="36b42-770">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="36b42-770">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="36b42-771">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="36b42-771">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="36b42-772">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-772">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36b42-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-773">Az.Monitor</span></span>
* <span data-ttu-id="36b42-774">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="36b42-774">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="36b42-775">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="36b42-775">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="36b42-776">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="36b42-776">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-777">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-777">Az.Network</span></span>
* <span data-ttu-id="36b42-778">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="36b42-778">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-779">Az.Resources</span></span>
* <span data-ttu-id="36b42-780">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="36b42-780">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="36b42-781">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-781">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-782">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-782">Az.Sql</span></span>
* <span data-ttu-id="36b42-783">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="36b42-783">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-784">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-784">Az.Storage</span></span>
* <span data-ttu-id="36b42-785">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="36b42-785">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="36b42-786">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="36b42-786">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="36b42-787">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="36b42-787">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="36b42-788">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="36b42-788">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="36b42-789">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="36b42-789">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="36b42-790">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="36b42-790">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="36b42-791">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="36b42-791">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="36b42-792">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="36b42-792">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="36b42-793">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="36b42-793">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="36b42-794">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="36b42-794">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="36b42-795">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="36b42-795">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="36b42-796">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="36b42-796">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="36b42-797">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="36b42-797">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="36b42-798">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="36b42-798">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="36b42-799">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="36b42-799">Highlights since the last major release</span></span>
* <span data-ttu-id="36b42-800">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="36b42-800">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="36b42-801">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="36b42-801">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-802">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-802">Az.Compute</span></span>
* <span data-ttu-id="36b42-803">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="36b42-803">VM Reapply feature</span></span>
    - <span data-ttu-id="36b42-804">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-804">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="36b42-805">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="36b42-805">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="36b42-806">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36b42-806">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="36b42-807">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="36b42-807">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="36b42-808">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="36b42-808">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="36b42-809">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-809">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="36b42-810">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="36b42-810">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="36b42-811">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-811">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="36b42-812">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-812">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="36b42-813">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-813">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="36b42-814">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="36b42-814">Az.DataBoxEdge</span></span>
* <span data-ttu-id="36b42-815">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="36b42-815">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="36b42-816">取得訂單</span><span class="sxs-lookup"><span data-stu-id="36b42-816">Get the Order</span></span>
* <span data-ttu-id="36b42-817">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="36b42-817">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="36b42-818">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="36b42-818">Create new Order</span></span>
* <span data-ttu-id="36b42-819">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="36b42-819">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="36b42-820">移除訂單</span><span class="sxs-lookup"><span data-stu-id="36b42-820">Remove the Order</span></span>
* <span data-ttu-id="36b42-821">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="36b42-821">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="36b42-822">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="36b42-822">Now creates Local Share</span></span>
* <span data-ttu-id="36b42-823">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="36b42-823">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="36b42-824">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="36b42-824">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="36b42-825">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="36b42-825">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="36b42-826">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="36b42-826">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="36b42-827">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="36b42-827">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="36b42-828">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="36b42-828">Gets the information about Triggers</span></span>
* <span data-ttu-id="36b42-829">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="36b42-829">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="36b42-830">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="36b42-830">Create new Triggers</span></span>
* <span data-ttu-id="36b42-831">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="36b42-831">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="36b42-832">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="36b42-832">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-833">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-833">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-834">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="36b42-834">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="36b42-835">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="36b42-835">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36b42-836">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-836">Az.DataLakeStore</span></span>
* <span data-ttu-id="36b42-837">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="36b42-837">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36b42-838">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36b42-838">Az.EventHub</span></span>
* <span data-ttu-id="36b42-839">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="36b42-839">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="36b42-840">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36b42-840">Az.FrontDoor</span></span>
* <span data-ttu-id="36b42-841">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="36b42-841">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="36b42-842">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="36b42-842">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="36b42-843">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="36b42-843">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="36b42-844">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="36b42-844">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-845">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-845">Az.Network</span></span>
* <span data-ttu-id="36b42-846">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="36b42-846">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="36b42-847">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="36b42-847">Az.PrivateDns</span></span>
* <span data-ttu-id="36b42-848">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="36b42-848">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-849">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-849">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-850">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="36b42-850">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="36b42-851">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="36b42-851">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="36b42-852">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="36b42-852">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="36b42-853">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="36b42-853">Az.RedisCache</span></span>
* <span data-ttu-id="36b42-854">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="36b42-854">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="36b42-855">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="36b42-855">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="36b42-856">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="36b42-856">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-857">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-857">Az.Resources</span></span>
- <span data-ttu-id="36b42-858">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="36b42-858">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="36b42-859">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="36b42-859">Updated create policy definition help example</span></span>
- <span data-ttu-id="36b42-860">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="36b42-860">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="36b42-861">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="36b42-861">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="36b42-862">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="36b42-862">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-863">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-863">Az.Sql</span></span>
* <span data-ttu-id="36b42-864">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-864">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="36b42-865">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="36b42-865">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="36b42-866">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="36b42-866">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="36b42-867">一般</span><span class="sxs-lookup"><span data-stu-id="36b42-867">General</span></span>
* <span data-ttu-id="36b42-868">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="36b42-868">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36b42-869">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-869">Az.Accounts</span></span>
* <span data-ttu-id="36b42-870">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="36b42-870">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="36b42-871">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="36b42-871">Az.Advisor</span></span>
* <span data-ttu-id="36b42-872">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="36b42-872">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="36b42-873">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36b42-873">Az.Batch</span></span>
* <span data-ttu-id="36b42-874">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="36b42-874">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="36b42-875">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="36b42-875">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="36b42-876">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="36b42-876">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="36b42-877">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="36b42-877">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="36b42-878">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="36b42-878">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="36b42-879">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="36b42-879">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="36b42-880">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="36b42-880">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="36b42-881">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="36b42-881">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="36b42-882">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="36b42-882">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="36b42-883">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="36b42-883">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="36b42-884">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="36b42-884">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="36b42-885">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="36b42-885">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="36b42-886">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="36b42-886">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="36b42-887">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="36b42-887">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="36b42-888">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="36b42-888">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="36b42-889">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="36b42-889">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="36b42-890">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="36b42-890">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="36b42-891">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="36b42-891">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="36b42-892">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="36b42-892">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="36b42-893">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="36b42-893">This operation is no longer supported.</span></span>
* <span data-ttu-id="36b42-894">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="36b42-894">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="36b42-895">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="36b42-895">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="36b42-896">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="36b42-896">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="36b42-897">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="36b42-897">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="36b42-898">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="36b42-898">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="36b42-899">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="36b42-899">New non-verified images are also now returned.</span></span> <span data-ttu-id="36b42-900">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="36b42-900">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="36b42-901">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="36b42-901">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="36b42-902">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="36b42-902">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="36b42-903">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="36b42-903">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="36b42-904">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="36b42-904">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="36b42-905">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="36b42-905">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="36b42-906">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="36b42-906">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="36b42-907">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="36b42-907">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="36b42-908">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="36b42-908">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="36b42-909">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="36b42-909">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="36b42-910">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36b42-910">Az.Cdn</span></span>
* <span data-ttu-id="36b42-911">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="36b42-911">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="36b42-912">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="36b42-912">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-913">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-913">Az.Compute</span></span>
* <span data-ttu-id="36b42-914">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="36b42-914">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="36b42-915">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="36b42-915">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="36b42-916">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="36b42-916">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="36b42-917">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-917">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="36b42-918">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-918">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="36b42-919">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="36b42-919">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="36b42-920">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-920">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="36b42-921">重大變更</span><span class="sxs-lookup"><span data-stu-id="36b42-921">Breaking changes</span></span>
    - <span data-ttu-id="36b42-922">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="36b42-922">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="36b42-923">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="36b42-923">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-924">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-924">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-925">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="36b42-925">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36b42-926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-926">Az.DataLakeStore</span></span>
* <span data-ttu-id="36b42-927">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="36b42-927">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="36b42-928">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="36b42-928">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="36b42-929">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="36b42-929">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="36b42-930">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="36b42-930">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="36b42-931">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="36b42-931">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="36b42-932">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="36b42-932">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="36b42-933">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36b42-933">Az.FrontDoor</span></span>
* <span data-ttu-id="36b42-934">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="36b42-934">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36b42-935">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36b42-935">Az.HDInsight</span></span>
* <span data-ttu-id="36b42-936">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="36b42-936">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="36b42-937">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="36b42-937">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="36b42-938">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="36b42-938">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="36b42-939">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-939">Removed five cmdlets:</span></span>
    - <span data-ttu-id="36b42-940">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="36b42-940">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="36b42-941">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="36b42-941">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="36b42-942">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="36b42-942">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="36b42-943">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="36b42-943">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="36b42-944">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="36b42-944">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="36b42-945">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-945">Added three cmdlets:</span></span>
    - <span data-ttu-id="36b42-946">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="36b42-946">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="36b42-947">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="36b42-947">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="36b42-948">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="36b42-948">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="36b42-949">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="36b42-949">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="36b42-950">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="36b42-950">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="36b42-951">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="36b42-951">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="36b42-952">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="36b42-952">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="36b42-953">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="36b42-953">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="36b42-954">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="36b42-954">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="36b42-955">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="36b42-955">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="36b42-956">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="36b42-956">Added some scenario test cases.</span></span>
* <span data-ttu-id="36b42-957">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="36b42-957">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36b42-958">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36b42-958">Az.IotHub</span></span>
* <span data-ttu-id="36b42-959">重大變更：</span><span class="sxs-lookup"><span data-stu-id="36b42-959">Breaking changes:</span></span>
    - <span data-ttu-id="36b42-960">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="36b42-960">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="36b42-961">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="36b42-961">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="36b42-962">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="36b42-962">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="36b42-963">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="36b42-963">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="36b42-964">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="36b42-964">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="36b42-965">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="36b42-965">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="36b42-966">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="36b42-966">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="36b42-967">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="36b42-967">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="36b42-968">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="36b42-968">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="36b42-969">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="36b42-969">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="36b42-970">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="36b42-970">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="36b42-971">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="36b42-971">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-972">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-972">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-973">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="36b42-973">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="36b42-974">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="36b42-974">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="36b42-975">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="36b42-975">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="36b42-976">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="36b42-976">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="36b42-977">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="36b42-977">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="36b42-978">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="36b42-978">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="36b42-979">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="36b42-979">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="36b42-980">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-980">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="36b42-981">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="36b42-981">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-982">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-982">Az.Resources</span></span>
* <span data-ttu-id="36b42-983">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="36b42-983">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-984">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-984">Az.Network</span></span>
* <span data-ttu-id="36b42-985">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="36b42-985">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="36b42-986">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-986">Updated cmdlet:</span></span>
        - <span data-ttu-id="36b42-987">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-987">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36b42-988">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-988">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36b42-989">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-989">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36b42-990">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-990">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36b42-991">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-991">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="36b42-992">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="36b42-992">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="36b42-993">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-993">New cmdlet:</span></span>
        - <span data-ttu-id="36b42-994">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="36b42-994">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="36b42-995">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="36b42-995">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="36b42-996">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="36b42-996">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="36b42-997">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="36b42-997">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="36b42-998">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="36b42-998">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="36b42-999">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="36b42-999">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="36b42-1000">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="36b42-1000">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="36b42-1001">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1001">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="36b42-1002">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1002">New cmdlets added:</span></span>
        - <span data-ttu-id="36b42-1003">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="36b42-1003">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="36b42-1004">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="36b42-1004">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="36b42-1005">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="36b42-1005">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="36b42-1006">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="36b42-1006">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="36b42-1007">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36b42-1007">Set-AzVirtualHub</span></span>
* <span data-ttu-id="36b42-1008">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1008">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="36b42-1009">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1009">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="36b42-1010">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="36b42-1010">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="36b42-1011">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="36b42-1011">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="36b42-1012">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="36b42-1012">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="36b42-1013">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="36b42-1013">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="36b42-1014">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1014">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="36b42-1015">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1015">New cmdlets added:</span></span>
        - <span data-ttu-id="36b42-1016">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-1016">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="36b42-1017">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1017">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="36b42-1018">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="36b42-1018">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="36b42-1019">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="36b42-1019">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="36b42-1020">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="36b42-1020">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="36b42-1021">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="36b42-1021">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="36b42-1022">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="36b42-1022">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="36b42-1023">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1023">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="36b42-1024">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1024">New cmdlets added:</span></span>
        - <span data-ttu-id="36b42-1025">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="36b42-1025">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="36b42-1026">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="36b42-1026">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="36b42-1027">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="36b42-1027">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="36b42-1028">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="36b42-1028">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="36b42-1029">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="36b42-1029">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="36b42-1030">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="36b42-1030">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="36b42-1031">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1031">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="36b42-1032">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="36b42-1032">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="36b42-1033">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1033">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="36b42-1034">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="36b42-1034">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="36b42-1035">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1035">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="36b42-1036">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1036">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="36b42-1037">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="36b42-1037">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="36b42-1038">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="36b42-1038">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="36b42-1039">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="36b42-1039">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="36b42-1040">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="36b42-1040">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="36b42-1041">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1041">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="36b42-1042">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1042">New cmdlets added:</span></span>
        - <span data-ttu-id="36b42-1043">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="36b42-1043">New-AzIpGroup</span></span>
        - <span data-ttu-id="36b42-1044">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="36b42-1044">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="36b42-1045">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="36b42-1045">Get-AzIpGroup</span></span>
        - <span data-ttu-id="36b42-1046">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="36b42-1046">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36b42-1047">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36b42-1047">Az.ServiceFabric</span></span>
* <span data-ttu-id="36b42-1048">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="36b42-1048">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-1049">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-1049">Az.Sql</span></span>
* <span data-ttu-id="36b42-1050">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-1050">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="36b42-1051">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b42-1051">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="36b42-1052">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="36b42-1052">Removed deprecated aliases:</span></span>
* <span data-ttu-id="36b42-1053">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="36b42-1053">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="36b42-1054">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="36b42-1054">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="36b42-1055">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1055">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="36b42-1056">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="36b42-1056">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="36b42-1057">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1057">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="36b42-1058">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="36b42-1058">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-1059">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-1059">Az.Storage</span></span>
* <span data-ttu-id="36b42-1060">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="36b42-1060">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="36b42-1061">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36b42-1061">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="36b42-1062">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36b42-1062">Set-AzStorageAccount</span></span>
* <span data-ttu-id="36b42-1063">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="36b42-1063">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="36b42-1064">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="36b42-1064">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="36b42-1065">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="36b42-1065">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="36b42-1066">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="36b42-1066">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="36b42-1067">一般</span><span class="sxs-lookup"><span data-stu-id="36b42-1067">General</span></span>
* <span data-ttu-id="36b42-1068">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="36b42-1068">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36b42-1069">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-1069">Az.Accounts</span></span>
* <span data-ttu-id="36b42-1070">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="36b42-1070">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36b42-1071">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36b42-1071">Az.ApiManagement</span></span>
* <span data-ttu-id="36b42-1072">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1072">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="36b42-1073">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1073">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36b42-1074">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36b42-1074">Az.Automation</span></span>
* <span data-ttu-id="36b42-1075">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b42-1075">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="36b42-1076">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36b42-1076">Az.Batch</span></span>
* <span data-ttu-id="36b42-1077">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="36b42-1077">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-1078">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-1078">Az.Compute</span></span>
* <span data-ttu-id="36b42-1079">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="36b42-1079">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="36b42-1080">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="36b42-1080">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="36b42-1081">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="36b42-1081">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="36b42-1082">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="36b42-1082">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-1083">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-1083">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-1084">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="36b42-1084">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="36b42-1085">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="36b42-1085">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="36b42-1086">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="36b42-1086">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36b42-1087">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-1087">Az.DataLakeStore</span></span>
* <span data-ttu-id="36b42-1088">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="36b42-1088">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="36b42-1089">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="36b42-1089">Az.HealthcareApis</span></span>
* <span data-ttu-id="36b42-1090">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="36b42-1090">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="36b42-1091">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="36b42-1091">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="36b42-1092">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="36b42-1092">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="36b42-1093">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="36b42-1093">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36b42-1094">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36b42-1094">Az.IotHub</span></span>
* <span data-ttu-id="36b42-1095">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="36b42-1095">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="36b42-1096">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="36b42-1096">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36b42-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-1097">Az.Monitor</span></span>
* <span data-ttu-id="36b42-1098">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="36b42-1098">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="36b42-1099">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="36b42-1099">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="36b42-1100">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="36b42-1100">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="36b42-1101">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="36b42-1101">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-1102">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-1102">Az.Network</span></span>
* <span data-ttu-id="36b42-1103">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="36b42-1103">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="36b42-1104">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1104">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="36b42-1105">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1105">New cmdlets added:</span></span>
        - <span data-ttu-id="36b42-1106">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="36b42-1106">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="36b42-1107">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-1107">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="36b42-1108">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1108">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="36b42-1109">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1109">Updated cmdlets:</span></span>
        - <span data-ttu-id="36b42-1110">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1110">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="36b42-1111">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1111">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="36b42-1112">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1112">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="36b42-1113">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="36b42-1113">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="36b42-1114">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="36b42-1114">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="36b42-1115">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="36b42-1115">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="36b42-1116">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="36b42-1116">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="36b42-1117">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="36b42-1117">Az.RedisCache</span></span>
* <span data-ttu-id="36b42-1118">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="36b42-1118">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-1119">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-1119">Az.Sql</span></span>
* <span data-ttu-id="36b42-1120">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1120">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-1121">Az.Storage</span></span>
* <span data-ttu-id="36b42-1122">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="36b42-1122">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="36b42-1123">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="36b42-1123">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="36b42-1124">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="36b42-1124">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="36b42-1125">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="36b42-1125">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="36b42-1126">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36b42-1126">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="36b42-1127">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="36b42-1127">Az.StorageSync</span></span>
* <span data-ttu-id="36b42-1128">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="36b42-1128">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-1129">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-1129">Az.Websites</span></span>
* <span data-ttu-id="36b42-1130">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="36b42-1130">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="36b42-1131">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="36b42-1131">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="36b42-1132">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36b42-1132">Az.ApiManagement</span></span>
* <span data-ttu-id="36b42-1133">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="36b42-1133">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="36b42-1134">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="36b42-1134">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="36b42-1135">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="36b42-1135">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36b42-1136">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36b42-1136">Az.Automation</span></span>
* <span data-ttu-id="36b42-1137">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="36b42-1137">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="36b42-1138">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="36b42-1138">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="36b42-1139">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="36b42-1139">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-1140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-1140">Az.Compute</span></span>
* <span data-ttu-id="36b42-1141">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="36b42-1141">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="36b42-1142">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="36b42-1142">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="36b42-1143">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="36b42-1143">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="36b42-1144">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="36b42-1144">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="36b42-1145">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="36b42-1145">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="36b42-1146">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="36b42-1146">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="36b42-1147">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="36b42-1147">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="36b42-1148">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="36b42-1148">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="36b42-1149">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="36b42-1149">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-1150">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-1150">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-1151">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="36b42-1151">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="36b42-1152">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="36b42-1152">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36b42-1153">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36b42-1153">Az.HDInsight</span></span>
* <span data-ttu-id="36b42-1154">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="36b42-1154">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36b42-1155">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36b42-1155">Az.IotHub</span></span>
* <span data-ttu-id="36b42-1156">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-1156">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="36b42-1157">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-1157">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="36b42-1158">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="36b42-1158">New cmdlets are:</span></span>
    - <span data-ttu-id="36b42-1159">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="36b42-1159">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="36b42-1160">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="36b42-1160">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="36b42-1161">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="36b42-1161">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="36b42-1162">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="36b42-1162">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36b42-1163">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-1163">Az.Monitor</span></span>
* <span data-ttu-id="36b42-1164">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="36b42-1164">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="36b42-1165">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="36b42-1165">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="36b42-1166">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="36b42-1166">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="36b42-1167">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="36b42-1167">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="36b42-1168">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="36b42-1168">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="36b42-1169">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="36b42-1169">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="36b42-1170">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="36b42-1170">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="36b42-1171">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="36b42-1171">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="36b42-1172">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="36b42-1172">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="36b42-1173">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="36b42-1173">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="36b42-1174">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="36b42-1174">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="36b42-1175">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="36b42-1175">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="36b42-1176">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="36b42-1176">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="36b42-1177">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="36b42-1177">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="36b42-1178">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="36b42-1178">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="36b42-1179">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="36b42-1179">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="36b42-1180">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="36b42-1180">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="36b42-1181">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="36b42-1181">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="36b42-1182">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="36b42-1182">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="36b42-1183">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="36b42-1183">Overall improved help files</span></span>
* <span data-ttu-id="36b42-1184">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="36b42-1184">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-1185">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-1185">Az.Network</span></span>
* <span data-ttu-id="36b42-1186">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="36b42-1186">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="36b42-1187">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="36b42-1187">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="36b42-1188">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="36b42-1188">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="36b42-1189">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="36b42-1189">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="36b42-1190">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="36b42-1190">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="36b42-1191">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="36b42-1191">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="36b42-1192">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="36b42-1192">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="36b42-1193">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="36b42-1193">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="36b42-1194">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="36b42-1194">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="36b42-1195">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="36b42-1195">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="36b42-1196">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="36b42-1196">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="36b42-1197">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="36b42-1197">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="36b42-1198">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1198">New cmdlets</span></span>
        - <span data-ttu-id="36b42-1199">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="36b42-1199">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="36b42-1200">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-1200">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="36b42-1201">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1201">Updated cmdlet:</span></span>
        - <span data-ttu-id="36b42-1202">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="36b42-1202">New-VpnSite</span></span>
        - <span data-ttu-id="36b42-1203">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="36b42-1203">Update-VpnSite</span></span>
        - <span data-ttu-id="36b42-1204">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-1204">New-VpnConnection</span></span>
        - <span data-ttu-id="36b42-1205">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-1205">Update-VpnConnection</span></span>
* <span data-ttu-id="36b42-1206">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1206">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-1207">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-1207">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-1208">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="36b42-1208">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="36b42-1209">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="36b42-1209">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-1210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-1210">Az.Resources</span></span>
* <span data-ttu-id="36b42-1211">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="36b42-1211">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36b42-1212">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36b42-1212">Az.ServiceFabric</span></span>
* <span data-ttu-id="36b42-1213">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="36b42-1213">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="36b42-1214">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="36b42-1214">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="36b42-1215">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="36b42-1215">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="36b42-1216">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="36b42-1216">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="36b42-1217">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="36b42-1217">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="36b42-1218">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="36b42-1218">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="36b42-1219">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="36b42-1219">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="36b42-1220">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="36b42-1220">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="36b42-1221">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="36b42-1221">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="36b42-1222">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="36b42-1222">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="36b42-1223">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="36b42-1223">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="36b42-1224">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="36b42-1224">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="36b42-1225">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="36b42-1225">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="36b42-1226">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="36b42-1226">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="36b42-1227">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="36b42-1227">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="36b42-1228">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="36b42-1228">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="36b42-1229">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="36b42-1229">Az.SignalR</span></span>
* <span data-ttu-id="36b42-1230">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1230">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-1231">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-1231">Az.Sql</span></span>
* <span data-ttu-id="36b42-1232">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="36b42-1232">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="36b42-1233">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="36b42-1233">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="36b42-1234">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="36b42-1234">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="36b42-1235">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="36b42-1235">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="36b42-1236">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="36b42-1236">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-1237">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-1237">Az.Storage</span></span>
* <span data-ttu-id="36b42-1238">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="36b42-1238">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="36b42-1239">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="36b42-1239">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="36b42-1240">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="36b42-1240">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="36b42-1241">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="36b42-1241">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="36b42-1242">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="36b42-1242">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="36b42-1243">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="36b42-1243">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="36b42-1244">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="36b42-1244">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="36b42-1245">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="36b42-1245">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="36b42-1246">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="36b42-1246">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="36b42-1247">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="36b42-1247">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="36b42-1248">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="36b42-1248">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-1249">Az.Websites</span></span>
* <span data-ttu-id="36b42-1250">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1250">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="36b42-1251">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="36b42-1251">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="36b42-1252">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="36b42-1252">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="36b42-1253">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="36b42-1253">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="36b42-1254">一般</span><span class="sxs-lookup"><span data-stu-id="36b42-1254">General</span></span>
* <span data-ttu-id="36b42-1255">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1255">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36b42-1256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-1256">Az.Accounts</span></span>
* <span data-ttu-id="36b42-1257">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="36b42-1257">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="36b42-1258">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="36b42-1258">Az.Aks</span></span>
* <span data-ttu-id="36b42-1259">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1259">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="36b42-1260">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="36b42-1260">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36b42-1261">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36b42-1261">Az.ApiManagement</span></span>
* <span data-ttu-id="36b42-1262">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1262">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="36b42-1263">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="36b42-1263">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="36b42-1264">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-1264">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="36b42-1265">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="36b42-1265">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="36b42-1266">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="36b42-1266">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="36b42-1267">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36b42-1267">Az.Batch</span></span>
* <span data-ttu-id="36b42-1268">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="36b42-1268">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="36b42-1269">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36b42-1269">Az.Cdn</span></span>
* <span data-ttu-id="36b42-1270">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="36b42-1270">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-1271">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-1271">Az.Compute</span></span>
* <span data-ttu-id="36b42-1272">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1272">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="36b42-1273">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="36b42-1273">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="36b42-1274">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="36b42-1274">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="36b42-1275">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="36b42-1275">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="36b42-1276">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="36b42-1276">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="36b42-1277">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="36b42-1277">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="36b42-1278">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="36b42-1278">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="36b42-1279">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="36b42-1279">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-1280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-1280">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-1281">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="36b42-1281">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="36b42-1282">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="36b42-1282">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="36b42-1283">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="36b42-1283">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="36b42-1284">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="36b42-1284">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36b42-1285">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-1285">Az.DataLakeStore</span></span>
* <span data-ttu-id="36b42-1286">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="36b42-1286">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36b42-1287">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36b42-1287">Az.EventHub</span></span>
* <span data-ttu-id="36b42-1288">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1288">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="36b42-1289">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="36b42-1289">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="36b42-1290">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1290">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="36b42-1291">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="36b42-1291">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="36b42-1292">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="36b42-1292">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="36b42-1293">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1293">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36b42-1294">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-1294">Az.Monitor</span></span>
* <span data-ttu-id="36b42-1295">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="36b42-1295">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-1296">Az.Network</span></span>
* <span data-ttu-id="36b42-1297">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1297">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="36b42-1298">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="36b42-1298">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="36b42-1299">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="36b42-1299">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="36b42-1300">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1300">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="36b42-1301">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="36b42-1301">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="36b42-1302">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="36b42-1302">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="36b42-1303">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="36b42-1303">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36b42-1304">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-1304">Az.OperationalInsights</span></span>
* <span data-ttu-id="36b42-1305">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="36b42-1305">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="36b42-1306">新增了範例</span><span class="sxs-lookup"><span data-stu-id="36b42-1306">Added example</span></span>
    - <span data-ttu-id="36b42-1307">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="36b42-1307">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="36b42-1308">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="36b42-1308">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="36b42-1309">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="36b42-1309">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-1310">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-1310">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-1311">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="36b42-1311">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-1312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-1312">Az.Resources</span></span>
* <span data-ttu-id="36b42-1313">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1313">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="36b42-1314">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1314">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="36b42-1315">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="36b42-1315">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="36b42-1316">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="36b42-1316">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="36b42-1317">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="36b42-1317">Az.ServiceBus</span></span>
* <span data-ttu-id="36b42-1318">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="36b42-1318">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="36b42-1319">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="36b42-1319">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="36b42-1320">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="36b42-1320">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36b42-1321">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36b42-1321">Az.ServiceFabric</span></span>
* <span data-ttu-id="36b42-1322">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="36b42-1322">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="36b42-1323">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="36b42-1323">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="36b42-1324">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="36b42-1324">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="36b42-1325">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="36b42-1325">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="36b42-1326">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="36b42-1326">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="36b42-1327">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1327">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-1328">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-1328">Az.Sql</span></span>
* <span data-ttu-id="36b42-1329">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="36b42-1329">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-1330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-1330">Az.Storage</span></span>
* <span data-ttu-id="36b42-1331">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="36b42-1331">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="36b42-1332">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="36b42-1332">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="36b42-1333">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="36b42-1333">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="36b42-1334">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="36b42-1334">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="36b42-1335">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="36b42-1335">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="36b42-1336">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="36b42-1336">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-1337">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-1337">Az.Websites</span></span>
* <span data-ttu-id="36b42-1338">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="36b42-1338">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="36b42-1339">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="36b42-1339">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36b42-1340">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-1340">Az.Accounts</span></span>
* <span data-ttu-id="36b42-1341">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="36b42-1341">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="36b42-1342">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-1342">Az.ApplicationInsights</span></span>
* <span data-ttu-id="36b42-1343">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="36b42-1343">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36b42-1344">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36b42-1344">Az.Automation</span></span>
* <span data-ttu-id="36b42-1345">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="36b42-1345">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36b42-1346">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36b42-1346">Az.CognitiveServices</span></span>
* <span data-ttu-id="36b42-1347">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-1347">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-1348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-1348">Az.Compute</span></span>
* <span data-ttu-id="36b42-1349">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="36b42-1349">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="36b42-1350">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="36b42-1350">Az.ContainerRegistry</span></span>
* <span data-ttu-id="36b42-1351">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="36b42-1351">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="36b42-1352">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="36b42-1352">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-1353">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-1353">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-1354">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="36b42-1354">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="36b42-1355">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="36b42-1355">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36b42-1356">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36b42-1356">Az.EventHub</span></span>
* <span data-ttu-id="36b42-1357">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="36b42-1357">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="36b42-1358">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="36b42-1358">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36b42-1359">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36b42-1359">Az.KeyVault</span></span>
* <span data-ttu-id="36b42-1360">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1360">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="36b42-1361">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="36b42-1361">Az.LogicApp</span></span>
* <span data-ttu-id="36b42-1362">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="36b42-1362">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="36b42-1363">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="36b42-1363">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="36b42-1364">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="36b42-1364">Az.ManagedServices</span></span>
* <span data-ttu-id="36b42-1365">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1365">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-1366">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-1366">Az.Network</span></span>
* <span data-ttu-id="36b42-1367">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1367">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="36b42-1368">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1368">New cmdlets</span></span>
        - <span data-ttu-id="36b42-1369">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36b42-1369">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="36b42-1370">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="36b42-1370">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="36b42-1371">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-1371">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36b42-1372">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-1372">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36b42-1373">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-1373">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36b42-1374">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-1374">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36b42-1375">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="36b42-1375">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="36b42-1376">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="36b42-1376">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="36b42-1377">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="36b42-1377">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="36b42-1378">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1378">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="36b42-1379">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="36b42-1379">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="36b42-1380">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="36b42-1380">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="36b42-1381">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="36b42-1381">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="36b42-1382">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="36b42-1382">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="36b42-1383">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1383">Updated cmdlets</span></span>
        - <span data-ttu-id="36b42-1384">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1384">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="36b42-1385">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1385">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="36b42-1386">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1386">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="36b42-1387">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="36b42-1387">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="36b42-1388">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="36b42-1388">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="36b42-1389">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1389">Updated cmdlet:</span></span>
        - <span data-ttu-id="36b42-1390">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1390">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="36b42-1391">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1391">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="36b42-1392">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1392">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="36b42-1393">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="36b42-1393">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="36b42-1394">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="36b42-1394">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="36b42-1395">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="36b42-1395">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36b42-1396">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-1396">Az.OperationalInsights</span></span>
* <span data-ttu-id="36b42-1397">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="36b42-1397">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="36b42-1398">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="36b42-1398">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-1399">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-1399">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-1400">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="36b42-1400">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="36b42-1401">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="36b42-1401">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="36b42-1402">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="36b42-1402">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="36b42-1403">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="36b42-1403">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="36b42-1404">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="36b42-1404">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="36b42-1405">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="36b42-1405">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="36b42-1406">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="36b42-1406">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="36b42-1407">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="36b42-1407">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="36b42-1408">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="36b42-1408">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="36b42-1409">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="36b42-1409">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-1410">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-1410">Az.Resources</span></span>
- <span data-ttu-id="36b42-1411">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1411">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="36b42-1412">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="36b42-1412">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="36b42-1413">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="36b42-1413">Az.ServiceBus</span></span>
* <span data-ttu-id="36b42-1414">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="36b42-1414">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="36b42-1415">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="36b42-1415">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-1416">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-1416">Az.Sql</span></span>
* <span data-ttu-id="36b42-1417">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="36b42-1417">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="36b42-1418">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1418">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="36b42-1419">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="36b42-1419">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-1420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-1420">Az.Storage</span></span>
* <span data-ttu-id="36b42-1421">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="36b42-1421">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="36b42-1422">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="36b42-1422">Az.StorageSync</span></span>
* <span data-ttu-id="36b42-1423">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b42-1423">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="36b42-1424">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="36b42-1424">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-1425">Az.Websites</span></span>
* <span data-ttu-id="36b42-1426">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="36b42-1426">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="36b42-1427">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="36b42-1427">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="36b42-1428">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="36b42-1428">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="36b42-1429">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="36b42-1429">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36b42-1430">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-1430">Az.Accounts</span></span>
* <span data-ttu-id="36b42-1431">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1431">Add support for profile cmdlets</span></span>
* <span data-ttu-id="36b42-1432">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1432">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="36b42-1433">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1433">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="36b42-1434">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="36b42-1434">Az.Advisor</span></span>
* <span data-ttu-id="36b42-1435">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="36b42-1435">GA release of Az.Advisor</span></span>
* <span data-ttu-id="36b42-1436">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="36b42-1436">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36b42-1437">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36b42-1437">Az.ApiManagement</span></span>
* <span data-ttu-id="36b42-1438">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1438">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="36b42-1439">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="36b42-1439">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="36b42-1440">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1440">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="36b42-1441">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1441">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="36b42-1442">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1442">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="36b42-1443">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="36b42-1443">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="36b42-1444">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1444">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36b42-1445">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36b42-1445">Az.Automation</span></span>
* <span data-ttu-id="36b42-1446">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="36b42-1446">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-1447">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-1447">Az.Compute</span></span>
* <span data-ttu-id="36b42-1448">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1448">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-1449">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-1449">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-1450">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="36b42-1450">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="36b42-1451">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="36b42-1451">Az.EventGrid</span></span>
* <span data-ttu-id="36b42-1452">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="36b42-1452">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36b42-1453">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36b42-1453">Az.IotHub</span></span>
* <span data-ttu-id="36b42-1454">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-1454">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-1455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-1455">Az.Network</span></span>
* <span data-ttu-id="36b42-1456">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="36b42-1456">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="36b42-1457">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="36b42-1457">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36b42-1458">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-1458">Az.PolicyInsights</span></span>
* <span data-ttu-id="36b42-1459">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1459">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="36b42-1460">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="36b42-1460">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36b42-1461">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-1461">Az.OperationalInsights</span></span>
* <span data-ttu-id="36b42-1462">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="36b42-1462">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-1463">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-1463">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-1464">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="36b42-1464">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-1465">Az.Resources</span></span>
    - <span data-ttu-id="36b42-1466">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="36b42-1466">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="36b42-1467">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1467">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="36b42-1468">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="36b42-1468">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="36b42-1469">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="36b42-1469">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="36b42-1470">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="36b42-1470">Az.ServiceBus</span></span>
* <span data-ttu-id="36b42-1471">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="36b42-1471">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-1472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-1472">Az.Sql</span></span>
* <span data-ttu-id="36b42-1473">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="36b42-1473">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="36b42-1474">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="36b42-1474">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="36b42-1475">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="36b42-1475">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="36b42-1476">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="36b42-1476">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="36b42-1477">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="36b42-1477">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="36b42-1478">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="36b42-1478">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="36b42-1479">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="36b42-1479">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="36b42-1480">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="36b42-1480">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="36b42-1481">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="36b42-1481">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-1482">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-1482">Az.Storage</span></span>
* <span data-ttu-id="36b42-1483">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="36b42-1483">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="36b42-1484">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="36b42-1484">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="36b42-1485">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="36b42-1485">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="36b42-1486">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="36b42-1486">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="36b42-1487">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="36b42-1487">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="36b42-1488">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36b42-1488">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="36b42-1489">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36b42-1489">Set-AzStorageAccount</span></span>
* <span data-ttu-id="36b42-1490">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="36b42-1490">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="36b42-1491">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="36b42-1491">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="36b42-1492">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="36b42-1492">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="36b42-1493">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="36b42-1493">Az.StorageSync</span></span>
* <span data-ttu-id="36b42-1494">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="36b42-1494">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="36b42-1495">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="36b42-1495">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36b42-1496">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-1496">Az.Accounts</span></span>
* <span data-ttu-id="36b42-1497">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="36b42-1497">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="36b42-1498">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="36b42-1498">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="36b42-1499">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1499">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="36b42-1500">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="36b42-1500">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="36b42-1501">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="36b42-1501">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-1502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-1502">Az.Compute</span></span>
* <span data-ttu-id="36b42-1503">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="36b42-1503">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="36b42-1504">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="36b42-1504">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="36b42-1505">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="36b42-1505">Az.Dns</span></span>
* <span data-ttu-id="36b42-1506">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="36b42-1506">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="36b42-1507">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="36b42-1507">Az.EventGrid</span></span>
* <span data-ttu-id="36b42-1508">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="36b42-1508">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="36b42-1509">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1509">New cmdlets:</span></span>
    - <span data-ttu-id="36b42-1510">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="36b42-1510">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="36b42-1511">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="36b42-1511">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="36b42-1512">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="36b42-1512">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="36b42-1513">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="36b42-1513">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="36b42-1514">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="36b42-1514">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="36b42-1515">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="36b42-1515">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="36b42-1516">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="36b42-1516">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="36b42-1517">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="36b42-1517">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="36b42-1518">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="36b42-1518">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="36b42-1519">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="36b42-1519">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="36b42-1520">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="36b42-1520">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="36b42-1521">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="36b42-1521">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="36b42-1522">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="36b42-1522">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="36b42-1523">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="36b42-1523">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="36b42-1524">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="36b42-1524">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="36b42-1525">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="36b42-1525">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="36b42-1526">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1526">Updated cmdlets:</span></span>
    - <span data-ttu-id="36b42-1527">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="36b42-1527">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="36b42-1528">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="36b42-1528">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="36b42-1529">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="36b42-1529">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="36b42-1530">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="36b42-1530">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="36b42-1531">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="36b42-1531">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="36b42-1532">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="36b42-1532">Event subscription expiration date,</span></span>
            - <span data-ttu-id="36b42-1533">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="36b42-1533">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="36b42-1534">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="36b42-1534">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="36b42-1535">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="36b42-1535">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="36b42-1536">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="36b42-1536">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="36b42-1537">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="36b42-1537">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="36b42-1538">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="36b42-1538">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="36b42-1539">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="36b42-1539">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="36b42-1540">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="36b42-1540">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="36b42-1541">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36b42-1541">Az.FrontDoor</span></span>
* <span data-ttu-id="36b42-1542">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="36b42-1542">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="36b42-1543">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="36b42-1543">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="36b42-1544">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="36b42-1544">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="36b42-1545">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="36b42-1545">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-1546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-1546">Az.Network</span></span>
* <span data-ttu-id="36b42-1547">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1547">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="36b42-1548">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1548">New cmdlets</span></span>
        - <span data-ttu-id="36b42-1549">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="36b42-1549">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="36b42-1550">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="36b42-1550">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="36b42-1551">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1551">New cmdlets</span></span>
        - <span data-ttu-id="36b42-1552">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="36b42-1552">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="36b42-1553">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="36b42-1553">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="36b42-1554">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1554">New cmdlets</span></span>
        - <span data-ttu-id="36b42-1555">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="36b42-1555">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="36b42-1556">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="36b42-1556">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="36b42-1557">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="36b42-1557">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="36b42-1558">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1558">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="36b42-1559">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-1559">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="36b42-1560">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36b42-1560">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="36b42-1561">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1561">New cmdlets</span></span>
        - <span data-ttu-id="36b42-1562">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36b42-1562">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="36b42-1563">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36b42-1563">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="36b42-1564">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36b42-1564">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="36b42-1565">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="36b42-1565">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="36b42-1566">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="36b42-1566">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="36b42-1567">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="36b42-1567">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="36b42-1568">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="36b42-1568">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="36b42-1569">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="36b42-1569">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="36b42-1570">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="36b42-1570">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="36b42-1571">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="36b42-1571">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="36b42-1572">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="36b42-1572">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="36b42-1573">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="36b42-1573">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="36b42-1574">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1574">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="36b42-1575">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="36b42-1575">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="36b42-1576">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="36b42-1576">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="36b42-1577">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1577">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="36b42-1578">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="36b42-1578">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="36b42-1579">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1579">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="36b42-1580">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1580">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="36b42-1581">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="36b42-1581">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="36b42-1582">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="36b42-1582">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="36b42-1583">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="36b42-1583">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="36b42-1584">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="36b42-1584">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="36b42-1585">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="36b42-1585">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="36b42-1586">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="36b42-1586">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="36b42-1587">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="36b42-1587">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="36b42-1588">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="36b42-1588">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36b42-1589">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-1589">Az.OperationalInsights</span></span>
* <span data-ttu-id="36b42-1590">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="36b42-1590">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-1591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-1591">Az.Resources</span></span>
* <span data-ttu-id="36b42-1592">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="36b42-1592">Support for additional Template Export options</span></span>
    - <span data-ttu-id="36b42-1593">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="36b42-1593">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="36b42-1594">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="36b42-1594">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="36b42-1595">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="36b42-1595">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36b42-1596">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36b42-1596">Az.ServiceFabric</span></span>
* <span data-ttu-id="36b42-1597">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1597">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-1598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-1598">Az.Sql</span></span>
* <span data-ttu-id="36b42-1599">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="36b42-1599">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="36b42-1600">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="36b42-1600">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="36b42-1601">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="36b42-1601">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="36b42-1602">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="36b42-1602">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="36b42-1603">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="36b42-1603">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="36b42-1604">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="36b42-1604">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="36b42-1605">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="36b42-1605">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="36b42-1606">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="36b42-1606">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-1607">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-1607">Az.Storage</span></span>
* <span data-ttu-id="36b42-1608">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="36b42-1608">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="36b42-1609">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36b42-1609">New-AzStorageAccount</span></span>
* <span data-ttu-id="36b42-1610">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="36b42-1610">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="36b42-1611">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="36b42-1611">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-1612">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-1612">Az.Websites</span></span>
* <span data-ttu-id="36b42-1613">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="36b42-1613">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="36b42-1614">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="36b42-1614">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="36b42-1615">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="36b42-1615">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="36b42-1616">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36b42-1616">Az.Cdn</span></span>
* <span data-ttu-id="36b42-1617">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="36b42-1617">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-1618">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-1618">Az.Compute</span></span>
* <span data-ttu-id="36b42-1619">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="36b42-1619">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="36b42-1620">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="36b42-1620">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36b42-1621">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36b42-1621">Az.EventHub</span></span>
* <span data-ttu-id="36b42-1622">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="36b42-1622">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="36b42-1623">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b42-1623">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-1624">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-1624">Az.Network</span></span>
* <span data-ttu-id="36b42-1625">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="36b42-1625">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="36b42-1626">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="36b42-1626">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36b42-1627">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-1627">Az.PolicyInsights</span></span>
* <span data-ttu-id="36b42-1628">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1628">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-1629">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-1629">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-1630">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="36b42-1630">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="36b42-1631">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="36b42-1631">Az.ServiceBus</span></span>
* <span data-ttu-id="36b42-1632">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b42-1632">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36b42-1633">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36b42-1633">Az.ServiceFabric</span></span>
* <span data-ttu-id="36b42-1634">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="36b42-1634">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="36b42-1635">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="36b42-1635">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-1636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-1636">Az.Sql</span></span>
* <span data-ttu-id="36b42-1637">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="36b42-1637">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="36b42-1638">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1638">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="36b42-1639">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="36b42-1639">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="36b42-1640">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="36b42-1640">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-1641">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-1641">Az.Websites</span></span>
* <span data-ttu-id="36b42-1642">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1642">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="36b42-1643">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="36b42-1643">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="36b42-1644">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36b42-1644">Az.ApiManagement</span></span>
* <span data-ttu-id="36b42-1645">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="36b42-1645">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="36b42-1646">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="36b42-1646">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="36b42-1647">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="36b42-1647">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="36b42-1648">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="36b42-1648">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="36b42-1649">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="36b42-1649">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="36b42-1650">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="36b42-1650">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="36b42-1651">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="36b42-1651">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="36b42-1652">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="36b42-1652">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="36b42-1653">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="36b42-1653">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="36b42-1654">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="36b42-1654">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="36b42-1655">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="36b42-1655">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="36b42-1656">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="36b42-1656">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="36b42-1657">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="36b42-1657">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="36b42-1658">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="36b42-1658">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="36b42-1659">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="36b42-1659">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="36b42-1660">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="36b42-1660">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="36b42-1661">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="36b42-1661">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="36b42-1662">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="36b42-1662">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="36b42-1663">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="36b42-1663">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="36b42-1664">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="36b42-1664">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="36b42-1665">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="36b42-1665">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="36b42-1666">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="36b42-1666">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="36b42-1667">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="36b42-1667">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="36b42-1668">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="36b42-1668">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="36b42-1669">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1669">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="36b42-1670">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1670">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="36b42-1671">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="36b42-1671">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="36b42-1672">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="36b42-1672">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="36b42-1673">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-1673">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="36b42-1674">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="36b42-1674">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="36b42-1675">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="36b42-1675">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="36b42-1676">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="36b42-1676">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="36b42-1677">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="36b42-1677">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="36b42-1678">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="36b42-1678">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="36b42-1679">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="36b42-1679">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="36b42-1680">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="36b42-1680">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="36b42-1681">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="36b42-1681">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="36b42-1682">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="36b42-1682">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="36b42-1683">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="36b42-1683">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="36b42-1684">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="36b42-1684">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="36b42-1685">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="36b42-1685">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="36b42-1686">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="36b42-1686">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="36b42-1687">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="36b42-1687">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="36b42-1688">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="36b42-1688">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="36b42-1689">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="36b42-1689">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="36b42-1690">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="36b42-1690">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="36b42-1691">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="36b42-1691">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="36b42-1692">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="36b42-1692">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="36b42-1693">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="36b42-1693">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="36b42-1694">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="36b42-1694">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="36b42-1695">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="36b42-1695">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="36b42-1696">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="36b42-1696">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="36b42-1697">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="36b42-1697">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="36b42-1698">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="36b42-1698">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="36b42-1699">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="36b42-1699">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="36b42-1700">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="36b42-1700">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="36b42-1701">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="36b42-1701">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="36b42-1702">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="36b42-1702">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="36b42-1703">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="36b42-1703">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="36b42-1704">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-1704">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="36b42-1705">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="36b42-1705">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="36b42-1706">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="36b42-1706">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="36b42-1707">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="36b42-1707">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="36b42-1708">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-1708">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="36b42-1709">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="36b42-1709">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="36b42-1710">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="36b42-1710">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="36b42-1711">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="36b42-1711">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="36b42-1712">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="36b42-1712">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="36b42-1713">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="36b42-1713">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="36b42-1714">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="36b42-1714">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="36b42-1715">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="36b42-1715">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="36b42-1716">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="36b42-1716">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="36b42-1717">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="36b42-1717">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="36b42-1718">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="36b42-1718">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="36b42-1719">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="36b42-1719">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="36b42-1720">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="36b42-1720">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="36b42-1721">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="36b42-1721">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36b42-1722">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36b42-1722">Az.Automation</span></span>
* <span data-ttu-id="36b42-1723">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="36b42-1723">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="36b42-1724">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1724">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="36b42-1725">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1725">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="36b42-1726">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="36b42-1726">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="36b42-1727">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1727">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="36b42-1728">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="36b42-1728">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="36b42-1729">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="36b42-1729">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-1730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-1730">Az.Compute</span></span>
* <span data-ttu-id="36b42-1731">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b42-1731">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="36b42-1732">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="36b42-1732">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36b42-1733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-1733">Az.DataLakeStore</span></span>
* <span data-ttu-id="36b42-1734">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="36b42-1734">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36b42-1735">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-1735">Az.Monitor</span></span>
* <span data-ttu-id="36b42-1736">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="36b42-1736">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-1737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-1737">Az.Network</span></span>
* <span data-ttu-id="36b42-1738">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="36b42-1738">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="36b42-1739">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1739">Updated cmdlet:</span></span>
        - <span data-ttu-id="36b42-1740">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="36b42-1740">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="36b42-1741">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="36b42-1741">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-1742">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-1742">Az.Resources</span></span>
* <span data-ttu-id="36b42-1743">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="36b42-1743">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-1744">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-1744">Az.Sql</span></span>
* <span data-ttu-id="36b42-1745">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="36b42-1745">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="36b42-1746">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="36b42-1746">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36b42-1747">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-1747">Az.Accounts</span></span>
* <span data-ttu-id="36b42-1748">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1748">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36b42-1749">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36b42-1749">Az.CognitiveServices</span></span>
* <span data-ttu-id="36b42-1750">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="36b42-1750">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="36b42-1751">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="36b42-1751">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-1752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-1752">Az.Compute</span></span>
* <span data-ttu-id="36b42-1753">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="36b42-1753">Proximity placement group feature.</span></span>
    - <span data-ttu-id="36b42-1754">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="36b42-1754">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="36b42-1755">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1755">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="36b42-1756">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="36b42-1756">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="36b42-1757">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="36b42-1757">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="36b42-1758">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36b42-1758">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="36b42-1759">重大變更</span><span class="sxs-lookup"><span data-stu-id="36b42-1759">Breaking changes</span></span>
    - <span data-ttu-id="36b42-1760">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="36b42-1760">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="36b42-1761">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="36b42-1761">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="36b42-1762">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="36b42-1762">Az.DeploymentManager</span></span>
* <span data-ttu-id="36b42-1763">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1763">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="36b42-1764">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="36b42-1764">Az.Dns</span></span>
* <span data-ttu-id="36b42-1765">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="36b42-1765">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="36b42-1766">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="36b42-1766">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="36b42-1767">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="36b42-1767">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="36b42-1768">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36b42-1768">Az.FrontDoor</span></span>
* <span data-ttu-id="36b42-1769">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1769">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="36b42-1770">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="36b42-1770">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="36b42-1771">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36b42-1771">Az.HDInsight</span></span>
* <span data-ttu-id="36b42-1772">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-1772">Removed two cmdlets:</span></span>
    - <span data-ttu-id="36b42-1773">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="36b42-1773">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="36b42-1774">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="36b42-1774">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="36b42-1775">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="36b42-1775">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="36b42-1776">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="36b42-1776">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="36b42-1777">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="36b42-1777">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="36b42-1778">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="36b42-1778">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36b42-1779">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-1779">Az.Monitor</span></span>
* <span data-ttu-id="36b42-1780">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="36b42-1780">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="36b42-1781">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="36b42-1781">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="36b42-1782">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="36b42-1782">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="36b42-1783">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="36b42-1783">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="36b42-1784">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="36b42-1784">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="36b42-1785">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="36b42-1785">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="36b42-1786">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="36b42-1786">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="36b42-1787">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="36b42-1787">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="36b42-1788">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="36b42-1788">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="36b42-1789">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="36b42-1789">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="36b42-1790">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="36b42-1790">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="36b42-1791">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="36b42-1791">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="36b42-1792">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="36b42-1792">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="36b42-1793">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1793">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-1794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-1794">Az.Network</span></span>
* <span data-ttu-id="36b42-1795">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1795">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="36b42-1796">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1796">New cmdlets</span></span>
        - <span data-ttu-id="36b42-1797">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="36b42-1797">New-AzNatGateway</span></span>
        - <span data-ttu-id="36b42-1798">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="36b42-1798">Get-AzNatGateway</span></span>
        - <span data-ttu-id="36b42-1799">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="36b42-1799">Set-AzNatGateway</span></span>
        - <span data-ttu-id="36b42-1800">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="36b42-1800">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="36b42-1801">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1801">Updated cmdlets</span></span>
        - <span data-ttu-id="36b42-1802">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="36b42-1802">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="36b42-1803">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="36b42-1803">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="36b42-1804">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="36b42-1804">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="36b42-1805">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="36b42-1805">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="36b42-1806">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="36b42-1806">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36b42-1807">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-1807">Az.PolicyInsights</span></span>
* <span data-ttu-id="36b42-1808">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="36b42-1808">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="36b42-1809">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="36b42-1809">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="36b42-1810">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="36b42-1810">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-1811">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-1811">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-1812">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="36b42-1812">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="36b42-1813">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="36b42-1813">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="36b42-1814">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="36b42-1814">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="36b42-1815">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="36b42-1815">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="36b42-1816">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="36b42-1816">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="36b42-1817">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="36b42-1817">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="36b42-1818">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="36b42-1818">Az.Relay</span></span>
* <span data-ttu-id="36b42-1819">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="36b42-1819">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="36b42-1820">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="36b42-1820">Az.ServiceBus</span></span>
* <span data-ttu-id="36b42-1821">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1821">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-1822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-1822">Az.Storage</span></span>
* <span data-ttu-id="36b42-1823">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="36b42-1823">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="36b42-1824">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="36b42-1824">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="36b42-1825">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="36b42-1825">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="36b42-1826">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36b42-1826">New-AzStorageAccount</span></span>
* <span data-ttu-id="36b42-1827">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="36b42-1827">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="36b42-1828">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36b42-1828">New-AzStorageAccount</span></span>
    - <span data-ttu-id="36b42-1829">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36b42-1829">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="36b42-1830">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36b42-1830">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-1831">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-1831">Az.Websites</span></span>
* <span data-ttu-id="36b42-1832">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="36b42-1832">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="36b42-1833">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="36b42-1833">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="36b42-1834">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="36b42-1834">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="36b42-1835">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="36b42-1835">Highlights since the last major release</span></span>
* <span data-ttu-id="36b42-1836">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="36b42-1836">General availability of `Az` module</span></span>
* <span data-ttu-id="36b42-1837">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="36b42-1837">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="36b42-1838">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="36b42-1838">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="36b42-1839">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1839">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="36b42-1840">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="36b42-1840">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="36b42-1841">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1841">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="36b42-1842">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1842">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36b42-1843">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-1843">Az.Accounts</span></span>
* <span data-ttu-id="36b42-1844">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="36b42-1844">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="36b42-1845">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36b42-1845">Az.Batch</span></span>
* <span data-ttu-id="36b42-1846">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1846">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="36b42-1847">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36b42-1847">Az.Cdn</span></span>
* <span data-ttu-id="36b42-1848">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1848">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36b42-1849">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36b42-1849">Az.CognitiveServices</span></span>
* <span data-ttu-id="36b42-1850">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1850">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-1851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-1851">Az.Compute</span></span>
* <span data-ttu-id="36b42-1852">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1852">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="36b42-1853">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="36b42-1854">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="36b42-1854">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-1855">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-1855">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-1856">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="36b42-1856">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36b42-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-1857">Az.DataLakeStore</span></span>
* <span data-ttu-id="36b42-1858">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="36b42-1859">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="36b42-1859">Az.EventGrid</span></span>
* <span data-ttu-id="36b42-1860">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b42-1860">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36b42-1861">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36b42-1861">Az.EventHub</span></span>
* <span data-ttu-id="36b42-1862">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1862">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36b42-1863">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36b42-1863">Az.HDInsight</span></span>
* <span data-ttu-id="36b42-1864">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1864">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36b42-1865">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36b42-1865">Az.IotHub</span></span>
* <span data-ttu-id="36b42-1866">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1866">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36b42-1867">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36b42-1867">Az.KeyVault</span></span>
* <span data-ttu-id="36b42-1868">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1868">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="36b42-1869">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="36b42-1869">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="36b42-1870">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="36b42-1870">Az.MachineLearning</span></span>
* <span data-ttu-id="36b42-1871">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1871">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="36b42-1872">Az.Media</span><span class="sxs-lookup"><span data-stu-id="36b42-1872">Az.Media</span></span>
* <span data-ttu-id="36b42-1873">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1873">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36b42-1874">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-1874">Az.Monitor</span></span>
  * <span data-ttu-id="36b42-1875">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1875">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="36b42-1876">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="36b42-1876">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="36b42-1877">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="36b42-1877">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="36b42-1878">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="36b42-1878">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="36b42-1879">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="36b42-1879">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="36b42-1880">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="36b42-1880">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="36b42-1881">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="36b42-1881">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-1882">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-1882">Az.Network</span></span>
* <span data-ttu-id="36b42-1883">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1883">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="36b42-1884">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="36b42-1884">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="36b42-1885">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="36b42-1885">Az.NotificationHubs</span></span>
* <span data-ttu-id="36b42-1886">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1886">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36b42-1887">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-1887">Az.OperationalInsights</span></span>
* <span data-ttu-id="36b42-1888">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1888">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="36b42-1889">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="36b42-1889">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="36b42-1890">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-1891">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-1891">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-1892">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="36b42-1893">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="36b42-1893">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="36b42-1894">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="36b42-1894">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="36b42-1895">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="36b42-1895">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="36b42-1896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="36b42-1896">Az.RedisCache</span></span>
* <span data-ttu-id="36b42-1897">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-1898">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-1898">Az.Resources</span></span>
* <span data-ttu-id="36b42-1899">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="36b42-1899">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-1900">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-1900">Az.Sql</span></span>
* <span data-ttu-id="36b42-1901">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="36b42-1901">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="36b42-1902">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1902">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="36b42-1903">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="36b42-1903">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="36b42-1904">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="36b42-1904">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="36b42-1905">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="36b42-1905">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="36b42-1906">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="36b42-1906">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="36b42-1907">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="36b42-1907">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-1908">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-1908">Az.Websites</span></span>
* <span data-ttu-id="36b42-1909">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="36b42-1909">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="36b42-1910">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-1910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="36b42-1911">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="36b42-1911">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="36b42-1912">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="36b42-1912">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="36b42-1913">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="36b42-1913">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="36b42-1914">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="36b42-1914">Highlights since the last major release</span></span>
* <span data-ttu-id="36b42-1915">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="36b42-1915">General availability of `Az` module</span></span>
* <span data-ttu-id="36b42-1916">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="36b42-1916">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="36b42-1917">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="36b42-1917">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="36b42-1918">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1918">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="36b42-1919">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="36b42-1919">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="36b42-1920">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1920">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="36b42-1921">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1921">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36b42-1922">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-1922">Az.Accounts</span></span>
* <span data-ttu-id="36b42-1923">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="36b42-1923">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="36b42-1924">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="36b42-1924">Az.AnalysisServices</span></span>
* <span data-ttu-id="36b42-1925">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="36b42-1925">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="36b42-1926">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="36b42-1926">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36b42-1927">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36b42-1927">Az.Automation</span></span>
* <span data-ttu-id="36b42-1928">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="36b42-1928">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="36b42-1929">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="36b42-1929">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="36b42-1930">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="36b42-1930">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-1931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-1931">Az.Compute</span></span>
* <span data-ttu-id="36b42-1932">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-1932">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="36b42-1933">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="36b42-1933">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="36b42-1934">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="36b42-1934">Az.ContainerInstance</span></span>
* <span data-ttu-id="36b42-1935">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="36b42-1935">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-1936">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-1936">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-1937">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="36b42-1937">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="36b42-1938">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b42-1938">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-1939">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-1939">Az.Resources</span></span>
* <span data-ttu-id="36b42-1940">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="36b42-1940">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="36b42-1941">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="36b42-1941">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="36b42-1942">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="36b42-1942">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="36b42-1943">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="36b42-1943">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="36b42-1944">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="36b42-1944">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="36b42-1945">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="36b42-1945">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-1946">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-1946">Az.Sql</span></span>
* <span data-ttu-id="36b42-1947">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="36b42-1947">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-1948">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-1948">Az.Storage</span></span>
* <span data-ttu-id="36b42-1949">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="36b42-1949">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="36b42-1950">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="36b42-1950">New-AzStorageContext</span></span>
* <span data-ttu-id="36b42-1951">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="36b42-1951">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="36b42-1952">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="36b42-1952">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="36b42-1953">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="36b42-1953">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="36b42-1954">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="36b42-1954">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="36b42-1955">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="36b42-1955">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="36b42-1956">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1956">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="36b42-1957">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="36b42-1957">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="36b42-1958">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="36b42-1958">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="36b42-1959">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="36b42-1959">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="36b42-1960">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="36b42-1960">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="36b42-1961">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="36b42-1961">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="36b42-1962">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="36b42-1962">Highlights since the last major release</span></span>
* <span data-ttu-id="36b42-1963">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="36b42-1963">General availability of `Az` module</span></span>
* <span data-ttu-id="36b42-1964">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="36b42-1964">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="36b42-1965">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="36b42-1965">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="36b42-1966">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1966">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="36b42-1967">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="36b42-1967">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="36b42-1968">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1968">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="36b42-1969">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-1969">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36b42-1970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36b42-1970">Az.Automation</span></span>
* <span data-ttu-id="36b42-1971">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="36b42-1971">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="36b42-1972">動態分組</span><span class="sxs-lookup"><span data-stu-id="36b42-1972">Dynamic grouping</span></span>
    * <span data-ttu-id="36b42-1973">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="36b42-1973">Pre-Post script</span></span>
    * <span data-ttu-id="36b42-1974">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="36b42-1974">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-1975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-1975">Az.Compute</span></span>
* <span data-ttu-id="36b42-1976">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-1976">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="36b42-1977">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="36b42-1977">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36b42-1978">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36b42-1978">Az.KeyVault</span></span>
* <span data-ttu-id="36b42-1979">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1979">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-1980">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-1980">Az.Network</span></span>
* <span data-ttu-id="36b42-1981">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1981">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="36b42-1982">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="36b42-1982">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-1983">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-1983">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-1984">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="36b42-1984">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="36b42-1985">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1985">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-1986">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-1986">Az.Resources</span></span>
* <span data-ttu-id="36b42-1987">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="36b42-1987">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="36b42-1988">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="36b42-1988">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-1989">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-1989">Az.Sql</span></span>
* <span data-ttu-id="36b42-1990">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="36b42-1990">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-1991">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-1991">Az.Storage</span></span>
* <span data-ttu-id="36b42-1992">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="36b42-1992">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="36b42-1993">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="36b42-1993">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="36b42-1994">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="36b42-1994">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="36b42-1995">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="36b42-1995">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="36b42-1996">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="36b42-1996">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="36b42-1997">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="36b42-1997">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="36b42-1998">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="36b42-1998">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-1999">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-1999">Az.Websites</span></span>
* <span data-ttu-id="36b42-2000">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="36b42-2000">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="36b42-2001">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="36b42-2001">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36b42-2002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-2002">Az.Accounts</span></span>
* <span data-ttu-id="36b42-2003">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2003">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="36b42-2004">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="36b42-2004">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36b42-2005">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36b42-2005">Az.Automation</span></span>
* <span data-ttu-id="36b42-2006">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2006">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="36b42-2007">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="36b42-2007">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="36b42-2008">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="36b42-2008">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="36b42-2009">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36b42-2009">Az.Cdn</span></span>
* <span data-ttu-id="36b42-2010">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2010">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-2011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-2011">Az.Compute</span></span>
* <span data-ttu-id="36b42-2012">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="36b42-2012">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-2013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-2013">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-2014">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="36b42-2014">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="36b42-2015">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="36b42-2015">Az.LogicApp</span></span>
* <span data-ttu-id="36b42-2016">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="36b42-2016">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-2017">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-2017">Az.Network</span></span>
* <span data-ttu-id="36b42-2018">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="36b42-2018">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-2019">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-2019">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-2020">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-2020">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="36b42-2021">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="36b42-2021">SDK Update</span></span>
* <span data-ttu-id="36b42-2022">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="36b42-2022">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="36b42-2023">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="36b42-2023">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-2024">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-2024">Az.Resources</span></span>
* <span data-ttu-id="36b42-2025">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2025">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="36b42-2026">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="36b42-2026">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="36b42-2027">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2027">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="36b42-2028">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="36b42-2028">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="36b42-2029">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2029">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="36b42-2030">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="36b42-2030">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-2031">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-2031">Az.Sql</span></span>
* <span data-ttu-id="36b42-2032">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="36b42-2032">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="36b42-2033">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="36b42-2033">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-2034">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-2034">Az.Storage</span></span>
* <span data-ttu-id="36b42-2035">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36b42-2035">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="36b42-2036">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="36b42-2036">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="36b42-2037">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="36b42-2037">Az.AnalysisServices</span></span>
* <span data-ttu-id="36b42-2038">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2038">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36b42-2039">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36b42-2039">Az.Automation</span></span>
* <span data-ttu-id="36b42-2040">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="36b42-2040">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="36b42-2041">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2041">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="36b42-2042">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="36b42-2042">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36b42-2043">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36b42-2043">Az.CognitiveServices</span></span>
* <span data-ttu-id="36b42-2044">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="36b42-2044">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-2045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-2045">Az.Compute</span></span>
* <span data-ttu-id="36b42-2046">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2046">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="36b42-2047">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="36b42-2047">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="36b42-2048">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2048">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="36b42-2049">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="36b42-2049">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36b42-2050">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-2050">Az.DataLakeStore</span></span>
* <span data-ttu-id="36b42-2051">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2051">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36b42-2052">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36b42-2052">Az.EventHub</span></span>
* <span data-ttu-id="36b42-2053">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="36b42-2053">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36b42-2054">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36b42-2054">Az.KeyVault</span></span>
* <span data-ttu-id="36b42-2055">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="36b42-2055">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="36b42-2056">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="36b42-2056">Az.LogicApp</span></span>
* <span data-ttu-id="36b42-2057">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="36b42-2057">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="36b42-2058">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="36b42-2058">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="36b42-2059">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2059">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="36b42-2060">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="36b42-2060">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="36b42-2061">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="36b42-2061">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="36b42-2062">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="36b42-2062">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="36b42-2063">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="36b42-2063">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="36b42-2064">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2064">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="36b42-2065">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="36b42-2065">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="36b42-2066">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="36b42-2066">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="36b42-2067">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="36b42-2067">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="36b42-2068">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="36b42-2068">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="36b42-2069">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="36b42-2069">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36b42-2070">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-2070">Az.Monitor</span></span>
* <span data-ttu-id="36b42-2071">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="36b42-2071">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-2072">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-2072">Az.Network</span></span>
* <span data-ttu-id="36b42-2073">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="36b42-2073">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36b42-2074">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-2074">Az.OperationalInsights</span></span>
* <span data-ttu-id="36b42-2075">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-2075">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="36b42-2076">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="36b42-2076">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="36b42-2077">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="36b42-2077">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-2078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-2078">Az.Resources</span></span>
* <span data-ttu-id="36b42-2079">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2079">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="36b42-2080">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2080">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="36b42-2081">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2081">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="36b42-2082">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="36b42-2082">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-2083">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-2083">Az.Sql</span></span>
* <span data-ttu-id="36b42-2084">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="36b42-2084">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="36b42-2085">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="36b42-2085">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-2086">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-2086">Az.Websites</span></span>
* <span data-ttu-id="36b42-2087">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="36b42-2087">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="36b42-2088">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="36b42-2088">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36b42-2089">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-2089">Az.Accounts</span></span>
* <span data-ttu-id="36b42-2090">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="36b42-2090">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="36b42-2091">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="36b42-2091">Az.AnalysisServices</span></span>
<span data-ttu-id="36b42-2092">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="36b42-2092">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-2093">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-2093">Az.Compute</span></span>
* <span data-ttu-id="36b42-2094">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-2094">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="36b42-2095">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="36b42-2095">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="36b42-2096">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="36b42-2096">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-2097">Az.RecoveryServices</span></span>
<span data-ttu-id="36b42-2098">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="36b42-2098">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-2099">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-2099">Az.Resources</span></span>
* <span data-ttu-id="36b42-2100">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="36b42-2100">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="36b42-2101">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="36b42-2101">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="36b42-2102">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2102">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="36b42-2103">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="36b42-2103">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-2104">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-2104">Az.Sql</span></span>
* <span data-ttu-id="36b42-2105">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="36b42-2105">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="36b42-2106">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2106">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="36b42-2107">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="36b42-2107">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="36b42-2108">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="36b42-2108">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36b42-2109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-2109">Az.Accounts</span></span>
* <span data-ttu-id="36b42-2110">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="36b42-2110">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="36b42-2111">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="36b42-2111">Az.AnalysisServices</span></span>
* <span data-ttu-id="36b42-2112">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="36b42-2112">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-2113">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-2113">Az.RecoveryServices</span></span>
* <span data-ttu-id="36b42-2114">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="36b42-2114">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="36b42-2115">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="36b42-2115">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36b42-2116">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-2116">Az.Accounts</span></span>
* <span data-ttu-id="36b42-2117">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="36b42-2117">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="36b42-2118">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="36b42-2118">Update incorrect online help URLs</span></span>
* <span data-ttu-id="36b42-2119">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="36b42-2119">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="36b42-2120">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="36b42-2120">Az.Aks</span></span>
* <span data-ttu-id="36b42-2121">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="36b42-2121">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36b42-2122">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36b42-2122">Az.Automation</span></span>
* <span data-ttu-id="36b42-2123">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-2123">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="36b42-2124">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="36b42-2124">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="36b42-2125">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36b42-2125">Az.Cdn</span></span>
* <span data-ttu-id="36b42-2126">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="36b42-2126">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-2127">Az.Compute</span></span>
* <span data-ttu-id="36b42-2128">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2128">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="36b42-2129">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36b42-2129">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="36b42-2130">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="36b42-2130">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="36b42-2131">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="36b42-2131">Az.ContainerRegistry</span></span>
* <span data-ttu-id="36b42-2132">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="36b42-2132">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36b42-2133">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36b42-2133">Az.DataFactory</span></span>
* <span data-ttu-id="36b42-2134">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="36b42-2134">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36b42-2135">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-2135">Az.DataLakeStore</span></span>
* <span data-ttu-id="36b42-2136">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2136">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="36b42-2137">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="36b42-2137">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="36b42-2138">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="36b42-2138">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36b42-2139">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36b42-2139">Az.IotHub</span></span>
* <span data-ttu-id="36b42-2140">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b42-2140">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36b42-2141">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36b42-2141">Az.KeyVault</span></span>
* <span data-ttu-id="36b42-2142">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="36b42-2142">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-2143">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-2143">Az.Network</span></span>
* <span data-ttu-id="36b42-2144">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="36b42-2144">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-2145">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-2145">Az.Resources</span></span>
* <span data-ttu-id="36b42-2146">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="36b42-2146">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="36b42-2147">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2147">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="36b42-2148">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="36b42-2148">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="36b42-2149">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2149">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="36b42-2150">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2150">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="36b42-2151">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2151">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="36b42-2152">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="36b42-2152">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36b42-2153">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36b42-2153">Az.ServiceFabric</span></span>
* <span data-ttu-id="36b42-2154">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="36b42-2154">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="36b42-2155">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="36b42-2155">Fix some error messages.</span></span>
* <span data-ttu-id="36b42-2156">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="36b42-2156">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="36b42-2157">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="36b42-2157">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="36b42-2158">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="36b42-2158">Az.SignalR</span></span>
* <span data-ttu-id="36b42-2159">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="36b42-2159">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-2160">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-2160">Az.Sql</span></span>
* <span data-ttu-id="36b42-2161">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="36b42-2161">Update incorrect online help URLs</span></span>
* <span data-ttu-id="36b42-2162">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="36b42-2162">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="36b42-2163">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2163">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="36b42-2164">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="36b42-2164">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-2165">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-2165">Az.Storage</span></span>
* <span data-ttu-id="36b42-2166">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="36b42-2166">Update incorrect online help URLs</span></span>
* <span data-ttu-id="36b42-2167">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="36b42-2167">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="36b42-2168">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="36b42-2168">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="36b42-2169">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="36b42-2169">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="36b42-2170">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="36b42-2170">Az.TrafficManager</span></span>
* <span data-ttu-id="36b42-2171">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="36b42-2171">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-2172">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-2172">Az.Websites</span></span>
* <span data-ttu-id="36b42-2173">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="36b42-2173">Update incorrect online help URLs</span></span>
* <span data-ttu-id="36b42-2174">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="36b42-2174">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="36b42-2175">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="36b42-2175">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="36b42-2176">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="36b42-2176">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36b42-2177">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-2177">Az.Accounts</span></span>
* <span data-ttu-id="36b42-2178">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="36b42-2178">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-2179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-2179">Az.Compute</span></span>
* <span data-ttu-id="36b42-2180">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="36b42-2180">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="36b42-2181">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="36b42-2181">Updated the description of ID in help files</span></span>
* <span data-ttu-id="36b42-2182">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2182">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36b42-2183">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-2183">Az.DataLakeStore</span></span>
* <span data-ttu-id="36b42-2184">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="36b42-2184">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="36b42-2185">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="36b42-2185">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="36b42-2186">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="36b42-2186">Az.EventGrid</span></span>
* <span data-ttu-id="36b42-2187">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="36b42-2187">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="36b42-2188">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="36b42-2188">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="36b42-2189">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="36b42-2189">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="36b42-2190">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="36b42-2190">Event Time-To-Live,</span></span>
        - <span data-ttu-id="36b42-2191">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="36b42-2191">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="36b42-2192">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="36b42-2192">Dead letter endpoint.</span></span>
    - <span data-ttu-id="36b42-2193">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="36b42-2193">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="36b42-2194">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="36b42-2194">Event Time-To-Live,</span></span>
        - <span data-ttu-id="36b42-2195">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="36b42-2195">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="36b42-2196">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="36b42-2196">Dead letter endpoint.</span></span>
* <span data-ttu-id="36b42-2197">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="36b42-2197">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="36b42-2198">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="36b42-2198">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36b42-2199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36b42-2199">Az.IotHub</span></span>
* <span data-ttu-id="36b42-2200">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="36b42-2200">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="36b42-2201">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="36b42-2201">Az.LogicApp</span></span>
* <span data-ttu-id="36b42-2202">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="36b42-2202">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-2203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-2203">Az.Resources</span></span>
* <span data-ttu-id="36b42-2204">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2204">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="36b42-2205">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="36b42-2205">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="36b42-2206">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="36b42-2206">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="36b42-2207">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="36b42-2207">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="36b42-2208">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="36b42-2208">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="36b42-2209">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="36b42-2209">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="36b42-2210">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="36b42-2210">Az.SignalR</span></span>
* <span data-ttu-id="36b42-2211">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2211">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-2212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-2212">Az.Sql</span></span>
* <span data-ttu-id="36b42-2213">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="36b42-2213">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36b42-2214">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-2214">Az.Storage</span></span>
* <span data-ttu-id="36b42-2215">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="36b42-2215">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="36b42-2216">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="36b42-2216">New-AzStorageContext</span></span>
* <span data-ttu-id="36b42-2217">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="36b42-2217">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="36b42-2218">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="36b42-2218">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-2219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-2219">Az.Websites</span></span>
* <span data-ttu-id="36b42-2220">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="36b42-2220">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="36b42-2221">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2221">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="36b42-2222">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="36b42-2222">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="36b42-2223">一般</span><span class="sxs-lookup"><span data-stu-id="36b42-2223">General</span></span>

- <span data-ttu-id="36b42-2224">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="36b42-2224">General Availability of Az Module</span></span>
- <span data-ttu-id="36b42-2225">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="36b42-2225">Online help for each module</span></span>
- <span data-ttu-id="36b42-2226">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="36b42-2226">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="36b42-2227">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2227">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="36b42-2228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-2228">Az.Accounts</span></span>
- <span data-ttu-id="36b42-2229">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="36b42-2229">Changed from Az.Profile</span></span>
- <span data-ttu-id="36b42-2230">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="36b42-2230">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="36b42-2231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36b42-2231">Az.ApiManagement</span></span>
- <span data-ttu-id="36b42-2232">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="36b42-2232">Fixes for #7002</span></span>
- <span data-ttu-id="36b42-2233">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2233">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="36b42-2234">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36b42-2234">Az.Batch</span></span>
- <span data-ttu-id="36b42-2235">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="36b42-2235">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="36b42-2236">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="36b42-2236">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="36b42-2237">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2237">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="36b42-2238">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="36b42-2238">Az.Billing</span></span>
- <span data-ttu-id="36b42-2239">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2239">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="36b42-2240">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="36b42-2240">Az.CognitivServices</span></span>
- <span data-ttu-id="36b42-2241">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="36b42-2241">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="36b42-2242">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="36b42-2242">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="36b42-2243">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="36b42-2243">Az.ContainerInstance</span></span>
- <span data-ttu-id="36b42-2244">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="36b42-2244">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="36b42-2245">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="36b42-2245">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="36b42-2246">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2246">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="36b42-2247">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-2247">Az.DataLakeStore</span></span>
- <span data-ttu-id="36b42-2248">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2248">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="36b42-2249">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36b42-2249">Az.Monitor</span></span>
- <span data-ttu-id="36b42-2250">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2250">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="36b42-2251">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36b42-2251">Az.KeyVault</span></span>
- <span data-ttu-id="36b42-2252">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="36b42-2252">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="36b42-2253">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="36b42-2253">Az.MachineLearning</span></span>
- <span data-ttu-id="36b42-2254">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2254">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="36b42-2255">Az.Media</span><span class="sxs-lookup"><span data-stu-id="36b42-2255">Az.Media</span></span>
- <span data-ttu-id="36b42-2256">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="36b42-2256">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="36b42-2257">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-2257">Az.Network</span></span>
<span data-ttu-id="36b42-2258">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-2258">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="36b42-2259">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="36b42-2259">New cmdlets added:</span></span>
        - <span data-ttu-id="36b42-2260">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="36b42-2260">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="36b42-2261">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="36b42-2261">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="36b42-2262">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="36b42-2262">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="36b42-2263">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="36b42-2263">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="36b42-2264">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="36b42-2264">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="36b42-2265">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="36b42-2265">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="36b42-2266">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="36b42-2266">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="36b42-2267">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="36b42-2267">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="36b42-2268">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="36b42-2268">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="36b42-2269">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36b42-2269">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="36b42-2270">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="36b42-2270">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="36b42-2271">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="36b42-2271">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="36b42-2272">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-2272">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="36b42-2273">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-2273">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="36b42-2274">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-2274">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="36b42-2275">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2275">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="36b42-2276">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="36b42-2276">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="36b42-2277">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="36b42-2277">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="36b42-2278">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="36b42-2278">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="36b42-2279">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2279">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="36b42-2280">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2280">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="36b42-2281">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-2281">Az.OperationalInsights</span></span>
- <span data-ttu-id="36b42-2282">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2282">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="36b42-2283">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="36b42-2283">Az.Profile</span></span>
- <span data-ttu-id="36b42-2284">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36b42-2284">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-2285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-2285">Az.RecoveryServices</span></span>
- <span data-ttu-id="36b42-2286">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="36b42-2287">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-2287">Az.Resources</span></span>
- <span data-ttu-id="36b42-2288">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2288">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="36b42-2289">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36b42-2289">Az.ServiceFabric</span></span>
- <span data-ttu-id="36b42-2290">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="36b42-2290">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="36b42-2291">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2291">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="36b42-2292">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="36b42-2292">Az.SIgnalR</span></span>
- <span data-ttu-id="36b42-2293">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="36b42-2293">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="36b42-2294">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-2294">Az.Sql</span></span>
- <span data-ttu-id="36b42-2295">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="36b42-2295">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="36b42-2296">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="36b42-2296">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="36b42-2297">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2297">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="36b42-2298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-2298">Az.Storage</span></span>
- <span data-ttu-id="36b42-2299">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2299">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="36b42-2300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-2300">Az.Websites</span></span>
- <span data-ttu-id="36b42-2301">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36b42-2301">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="36b42-2302">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="36b42-2302">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="36b42-2303">一般</span><span class="sxs-lookup"><span data-stu-id="36b42-2303">General</span></span>

* <span data-ttu-id="36b42-2304">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="36b42-2304">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="36b42-2305">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-2305">Az.Compute</span></span>

* <span data-ttu-id="36b42-2306">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="36b42-2306">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="36b42-2307">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-2307">Az.DataLakeStore</span></span>

* <span data-ttu-id="36b42-2308">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="36b42-2308">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="36b42-2309">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36b42-2309">Az.FrontDoor</span></span>

* <span data-ttu-id="36b42-2310">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="36b42-2310">Fixed some broken links</span></span>
    - <span data-ttu-id="36b42-2311">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="36b42-2311">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="36b42-2312">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="36b42-2312">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="36b42-2313">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36b42-2313">Az.RecoveryServices</span></span>

* <span data-ttu-id="36b42-2314">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="36b42-2314">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="36b42-2315">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="36b42-2315">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="36b42-2316">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-2316">Az.Resources</span></span>

* <span data-ttu-id="36b42-2317">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="36b42-2317">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="36b42-2318">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="36b42-2318">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="36b42-2319">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-2319">Az.Sql</span></span>

* <span data-ttu-id="36b42-2320">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="36b42-2320">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="36b42-2321">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2321">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="36b42-2322">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="36b42-2322">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="36b42-2323">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-2323">Az.Storage</span></span>

* <span data-ttu-id="36b42-2324">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="36b42-2324">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="36b42-2325">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="36b42-2325">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="36b42-2326">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="36b42-2326">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="36b42-2327">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="36b42-2327">Support Static Website configuration</span></span>
    - <span data-ttu-id="36b42-2328">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="36b42-2328">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="36b42-2329">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="36b42-2329">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="36b42-2330">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-2330">Az.Websites</span></span>

* <span data-ttu-id="36b42-2331">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36b42-2331">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="36b42-2332">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="36b42-2332">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="36b42-2333">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="36b42-2333">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="36b42-2334">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="36b42-2334">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="36b42-2335">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36b42-2335">Az.ApiManagement</span></span>
* <span data-ttu-id="36b42-2336">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="36b42-2336">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="36b42-2337">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36b42-2337">Az.Automation</span></span>
* <span data-ttu-id="36b42-2338">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2338">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="36b42-2339">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2339">Added Update Management cmdlets</span></span>
* <span data-ttu-id="36b42-2340">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2340">Added Source Control cmdlets</span></span>
* <span data-ttu-id="36b42-2341">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2341">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="36b42-2342">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="36b42-2342">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="36b42-2343">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-2343">Az.Compute</span></span>
* <span data-ttu-id="36b42-2344">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2344">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="36b42-2345">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="36b42-2345">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="36b42-2346">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="36b42-2346">Az.ContainerInstance</span></span>
* <span data-ttu-id="36b42-2347">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="36b42-2347">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="36b42-2348">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="36b42-2348">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="36b42-2349">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="36b42-2349">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="36b42-2350">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-2350">Az.Network</span></span>
* <span data-ttu-id="36b42-2351">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="36b42-2351">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="36b42-2352">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="36b42-2352">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="36b42-2353">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="36b42-2353">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="36b42-2354">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2354">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="36b42-2355">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="36b42-2355">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="36b42-2356">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="36b42-2356">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="36b42-2357">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="36b42-2357">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="36b42-2358">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="36b42-2358">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="36b42-2359">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="36b42-2359">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="36b42-2360">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="36b42-2360">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="36b42-2361">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="36b42-2361">Az.Relay</span></span>
* <span data-ttu-id="36b42-2362">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="36b42-2362">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="36b42-2363">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-2363">Az.Resources</span></span>
* <span data-ttu-id="36b42-2364">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="36b42-2364">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="36b42-2365">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="36b42-2365">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="36b42-2366">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="36b42-2366">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="36b42-2367">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36b42-2367">Az.ServiceFabric</span></span>
* <span data-ttu-id="36b42-2368">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="36b42-2368">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="36b42-2369">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-2369">Az.Sql</span></span>
* <span data-ttu-id="36b42-2370">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2370">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="36b42-2371">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="36b42-2371">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="36b42-2372">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="36b42-2372">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="36b42-2373">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="36b42-2373">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="36b42-2374">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="36b42-2374">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="36b42-2375">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="36b42-2375">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="36b42-2376">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="36b42-2376">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="36b42-2377">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="36b42-2377">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="36b42-2378">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="36b42-2378">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="36b42-2379">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="36b42-2379">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="36b42-2380">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="36b42-2380">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="36b42-2381">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="36b42-2381">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="36b42-2382">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="36b42-2382">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="36b42-2383">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="36b42-2383">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="36b42-2384">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="36b42-2384">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="36b42-2385">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="36b42-2385">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="36b42-2386">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2386">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="36b42-2387">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="36b42-2387">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="36b42-2388">一般</span><span class="sxs-lookup"><span data-stu-id="36b42-2388">General</span></span>
* <span data-ttu-id="36b42-2389">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="36b42-2389">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="36b42-2390">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="36b42-2390">Az.Profile</span></span>
* <span data-ttu-id="36b42-2391">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="36b42-2391">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="36b42-2392">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="36b42-2392">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="36b42-2393">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="36b42-2393">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="36b42-2394">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="36b42-2394">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="36b42-2395">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2395">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="36b42-2396">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2396">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="36b42-2397">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2397">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="36b42-2398">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36b42-2398">Az.CognitiveServices</span></span>
* <span data-ttu-id="36b42-2399">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="36b42-2399">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-2400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-2400">Az.Compute</span></span>
* <span data-ttu-id="36b42-2401">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2401">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="36b42-2402">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="36b42-2402">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="36b42-2403">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="36b42-2403">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36b42-2404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-2404">Az.DataLakeStore</span></span>
* <span data-ttu-id="36b42-2405">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="36b42-2405">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="36b42-2406">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="36b42-2406">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="36b42-2407">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="36b42-2407">Az.Insights</span></span>
* <span data-ttu-id="36b42-2408">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="36b42-2408">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="36b42-2409">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="36b42-2409">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="36b42-2410">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="36b42-2410">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="36b42-2411">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="36b42-2411">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-2412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-2412">Az.Network</span></span>
* <span data-ttu-id="36b42-2413">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="36b42-2413">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="36b42-2414">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="36b42-2414">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="36b42-2415">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="36b42-2415">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="36b42-2416">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="36b42-2416">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="36b42-2417">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="36b42-2417">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="36b42-2418">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="36b42-2418">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="36b42-2419">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="36b42-2419">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36b42-2420">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36b42-2420">Az.PolicyInsights</span></span>
* <span data-ttu-id="36b42-2421">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2421">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-2422">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-2422">Az.Resources</span></span>
* <span data-ttu-id="36b42-2423">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="36b42-2423">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="36b42-2424">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="36b42-2424">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="36b42-2425">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="36b42-2425">Az.ServiceBus</span></span>
* <span data-ttu-id="36b42-2426">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="36b42-2426">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36b42-2427">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36b42-2427">Az.ServiceFabric</span></span>
* <span data-ttu-id="36b42-2428">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="36b42-2428">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="36b42-2429">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="36b42-2429">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="36b42-2430">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="36b42-2430">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="36b42-2431">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="36b42-2431">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="36b42-2432">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="36b42-2432">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="36b42-2433">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="36b42-2433">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="36b42-2434">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="36b42-2434">Az.Profile</span></span>
* <span data-ttu-id="36b42-2435">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2435">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="36b42-2436">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="36b42-2436">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-2437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-2437">Az.Compute</span></span>
* <span data-ttu-id="36b42-2438">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="36b42-2438">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="36b42-2439">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b42-2439">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36b42-2440">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36b42-2440">Az.DataLakeStore</span></span>
* <span data-ttu-id="36b42-2441">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="36b42-2441">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="36b42-2442">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="36b42-2442">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="36b42-2443">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="36b42-2443">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="36b42-2444">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="36b42-2444">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="36b42-2445">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="36b42-2445">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-2446">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-2446">Az.Network</span></span>
* <span data-ttu-id="36b42-2447">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="36b42-2447">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="36b42-2448">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b42-2448">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-2449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-2449">Az.Resources</span></span>
* <span data-ttu-id="36b42-2450">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="36b42-2450">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="36b42-2451">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="36b42-2451">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="36b42-2452">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="36b42-2452">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="36b42-2453">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="36b42-2453">Azure.Storage</span></span>
* <span data-ttu-id="36b42-2454">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2454">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="36b42-2455">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="36b42-2455">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="36b42-2456">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="36b42-2456">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="36b42-2457">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="36b42-2457">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="36b42-2458">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="36b42-2458">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36b42-2459">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36b42-2459">Az.CognitiveServices</span></span>
* <span data-ttu-id="36b42-2460">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="36b42-2460">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36b42-2461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36b42-2461">Az.Compute</span></span>
* <span data-ttu-id="36b42-2462">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="36b42-2462">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="36b42-2463">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="36b42-2463">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="36b42-2464">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="36b42-2464">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="36b42-2465">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="36b42-2465">Az.DataFactoryV2</span></span>
* <span data-ttu-id="36b42-2466">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="36b42-2466">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36b42-2467">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36b42-2467">Az.Network</span></span>
* <span data-ttu-id="36b42-2468">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="36b42-2468">Added NetworkProfile functionality.</span></span> <span data-ttu-id="36b42-2469">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2469">new cmdlets added</span></span>
    - <span data-ttu-id="36b42-2470">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="36b42-2470">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="36b42-2471">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="36b42-2471">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="36b42-2472">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="36b42-2472">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="36b42-2473">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="36b42-2473">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="36b42-2474">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-2474">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="36b42-2475">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="36b42-2475">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="36b42-2476">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="36b42-2476">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="36b42-2477">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2477">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="36b42-2478">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b42-2478">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="36b42-2479">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="36b42-2479">Az.RedisCache</span></span>
* <span data-ttu-id="36b42-2480">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="36b42-2480">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="36b42-2481">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="36b42-2481">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="36b42-2482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36b42-2482">Az.Resources</span></span>
* <span data-ttu-id="36b42-2483">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="36b42-2483">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="36b42-2484">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="36b42-2484">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="36b42-2485">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36b42-2485">Az.Sql</span></span>
* <span data-ttu-id="36b42-2486">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="36b42-2486">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36b42-2487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36b42-2487">Az.Websites</span></span>
* <span data-ttu-id="36b42-2488">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="36b42-2488">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="36b42-2489">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="36b42-2489">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="36b42-2490">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="36b42-2490">0.2.0 - September 2018</span></span>
 <span data-ttu-id="36b42-2491">初始版本</span><span class="sxs-lookup"><span data-stu-id="36b42-2491">Initial Release</span></span>
