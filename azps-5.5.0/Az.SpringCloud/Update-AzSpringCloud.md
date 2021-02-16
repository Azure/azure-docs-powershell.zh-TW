---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 361ba47486d7cc506e918ea279129110306e415f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133507"
---
# <span data-ttu-id="12e85-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="12e85-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="12e85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12e85-102">SYNOPSIS</span></span>
<span data-ttu-id="12e85-103">更新退出服務的操作。</span><span class="sxs-lookup"><span data-stu-id="12e85-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="12e85-104">句法</span><span class="sxs-lookup"><span data-stu-id="12e85-104">SYNTAX</span></span>

### <span data-ttu-id="12e85-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="12e85-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12e85-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="12e85-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="12e85-107">說明</span><span class="sxs-lookup"><span data-stu-id="12e85-107">DESCRIPTION</span></span>
<span data-ttu-id="12e85-108">更新退出服務的操作。</span><span class="sxs-lookup"><span data-stu-id="12e85-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="12e85-109">示例</span><span class="sxs-lookup"><span data-stu-id="12e85-109">EXAMPLES</span></span>

### <span data-ttu-id="12e85-110">範例1：依名稱更新彈簧雲端服務。</span><span class="sxs-lookup"><span data-stu-id="12e85-110">Example 1: Update Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="12e85-111">依名稱更新彈簧雲端服務。</span><span class="sxs-lookup"><span data-stu-id="12e85-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="12e85-112">範例2：從管道更新彈簧雲端服務。</span><span class="sxs-lookup"><span data-stu-id="12e85-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Update-AzSpringCloud
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="12e85-113">從管道更新彈簧雲端服務。</span><span class="sxs-lookup"><span data-stu-id="12e85-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="12e85-114">參數</span><span class="sxs-lookup"><span data-stu-id="12e85-114">PARAMETERS</span></span>

### <span data-ttu-id="12e85-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12e85-115">-AsJob</span></span>
<span data-ttu-id="12e85-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="12e85-116">Run the command as a job</span></span>

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

### <span data-ttu-id="12e85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e85-117">-DefaultProfile</span></span>
<span data-ttu-id="12e85-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12e85-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e85-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="12e85-119">-GitPropertyUri</span></span>
<span data-ttu-id="12e85-120">儲存庫的 URI</span><span class="sxs-lookup"><span data-stu-id="12e85-120">URI of the repository</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e85-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12e85-121">-InputObject</span></span>
<span data-ttu-id="12e85-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="12e85-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12e85-123">-位置</span><span class="sxs-lookup"><span data-stu-id="12e85-123">-Location</span></span>
<span data-ttu-id="12e85-124">資源的地理位置。</span><span class="sxs-lookup"><span data-stu-id="12e85-124">The GEO location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e85-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="12e85-125">-Name</span></span>
<span data-ttu-id="12e85-126">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e85-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e85-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="12e85-127">-NoWait</span></span>
<span data-ttu-id="12e85-128">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="12e85-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="12e85-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e85-129">-ResourceGroupName</span></span>
<span data-ttu-id="12e85-130">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e85-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="12e85-131">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="12e85-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e85-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="12e85-132">-SkuName</span></span>
<span data-ttu-id="12e85-133">Sku 名稱</span><span class="sxs-lookup"><span data-stu-id="12e85-133">Name of the Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e85-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="12e85-134">-SkuTier</span></span>
<span data-ttu-id="12e85-135">Sku 的層級</span><span class="sxs-lookup"><span data-stu-id="12e85-135">Tier of the Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e85-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12e85-136">-SubscriptionId</span></span>
<span data-ttu-id="12e85-137">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="12e85-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="12e85-138">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="12e85-138">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e85-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="12e85-139">-Tag</span></span>
<span data-ttu-id="12e85-140">服務的標記，是描述資源之鍵值對的清單。</span><span class="sxs-lookup"><span data-stu-id="12e85-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e85-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="12e85-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="12e85-142">目標應用程式洞察力工具金鑰</span><span class="sxs-lookup"><span data-stu-id="12e85-142">Target application insight instrumentation key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e85-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="12e85-143">-TraceEnabled</span></span>
<span data-ttu-id="12e85-144">指出是否啟用追蹤功能</span><span class="sxs-lookup"><span data-stu-id="12e85-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="12e85-145">-確認</span><span class="sxs-lookup"><span data-stu-id="12e85-145">-Confirm</span></span>
<span data-ttu-id="12e85-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12e85-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e85-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12e85-147">-WhatIf</span></span>
<span data-ttu-id="12e85-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12e85-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12e85-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12e85-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e85-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e85-150">CommonParameters</span></span>
<span data-ttu-id="12e85-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12e85-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e85-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="12e85-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e85-153">輸入</span><span class="sxs-lookup"><span data-stu-id="12e85-153">INPUTS</span></span>

### <span data-ttu-id="12e85-154">ISpringCloudIdentity （SpringCloud）的</span><span class="sxs-lookup"><span data-stu-id="12e85-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="12e85-155">輸出</span><span class="sxs-lookup"><span data-stu-id="12e85-155">OUTPUTS</span></span>

### <span data-ttu-id="12e85-156">IServiceResource （SpringCloud）。 Api20200701。</span><span class="sxs-lookup"><span data-stu-id="12e85-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="12e85-157">筆記</span><span class="sxs-lookup"><span data-stu-id="12e85-157">NOTES</span></span>

<span data-ttu-id="12e85-158">別名</span><span class="sxs-lookup"><span data-stu-id="12e85-158">ALIASES</span></span>

<span data-ttu-id="12e85-159">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="12e85-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12e85-160">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="12e85-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12e85-161">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="12e85-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12e85-162">INPUTOBJECT <ISpringCloudIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="12e85-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12e85-163">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e85-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="12e85-164">`[BindingName <String>]`：系結資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e85-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="12e85-165">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e85-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="12e85-166">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e85-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="12e85-167">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e85-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="12e85-168">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="12e85-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12e85-169">`[Location <String>]`：區域</span><span class="sxs-lookup"><span data-stu-id="12e85-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="12e85-170">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e85-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="12e85-171">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="12e85-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="12e85-172">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e85-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="12e85-173">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="12e85-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="12e85-174">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="12e85-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="12e85-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="12e85-175">RELATED LINKS</span></span>

