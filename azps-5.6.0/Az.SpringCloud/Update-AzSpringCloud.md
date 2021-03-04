---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 9c9ec2f2a48d3bc94ef0e0ab72b5b2bf4edd9045
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915790"
---
# <span data-ttu-id="f6152-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="f6152-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="f6152-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f6152-102">SYNOPSIS</span></span>
<span data-ttu-id="f6152-103">更新離開服務的作業。</span><span class="sxs-lookup"><span data-stu-id="f6152-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="f6152-104">語法</span><span class="sxs-lookup"><span data-stu-id="f6152-104">SYNTAX</span></span>

### <span data-ttu-id="f6152-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="f6152-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f6152-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f6152-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f6152-107">描述</span><span class="sxs-lookup"><span data-stu-id="f6152-107">DESCRIPTION</span></span>
<span data-ttu-id="f6152-108">更新離開服務的作業。</span><span class="sxs-lookup"><span data-stu-id="f6152-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="f6152-109">例子</span><span class="sxs-lookup"><span data-stu-id="f6152-109">EXAMPLES</span></span>

### <span data-ttu-id="f6152-110">範例 1：按名稱更新 Spring Cloud Service。</span><span class="sxs-lookup"><span data-stu-id="f6152-110">Example 1: Update Spring Cloud Service by name.</span></span>
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

<span data-ttu-id="f6152-111">按名稱更新春雲服務。</span><span class="sxs-lookup"><span data-stu-id="f6152-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="f6152-112">範例 2：從管道更新 Spring Cloud Service。</span><span class="sxs-lookup"><span data-stu-id="f6152-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
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

<span data-ttu-id="f6152-113">從管道更新春雲服務。</span><span class="sxs-lookup"><span data-stu-id="f6152-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="f6152-114">參數</span><span class="sxs-lookup"><span data-stu-id="f6152-114">PARAMETERS</span></span>

### <span data-ttu-id="f6152-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6152-115">-AsJob</span></span>
<span data-ttu-id="f6152-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="f6152-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f6152-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6152-117">-DefaultProfile</span></span>
<span data-ttu-id="f6152-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6152-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6152-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="f6152-119">-GitPropertyUri</span></span>
<span data-ttu-id="f6152-120">存放庫的 URI</span><span class="sxs-lookup"><span data-stu-id="f6152-120">URI of the repository</span></span>

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

### <span data-ttu-id="f6152-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6152-121">-InputObject</span></span>
<span data-ttu-id="f6152-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f6152-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f6152-123">-位置</span><span class="sxs-lookup"><span data-stu-id="f6152-123">-Location</span></span>
<span data-ttu-id="f6152-124">資源的 GEO 位置。</span><span class="sxs-lookup"><span data-stu-id="f6152-124">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="f6152-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6152-125">-Name</span></span>
<span data-ttu-id="f6152-126">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6152-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="f6152-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f6152-127">-NoWait</span></span>
<span data-ttu-id="f6152-128">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="f6152-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f6152-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6152-129">-ResourceGroupName</span></span>
<span data-ttu-id="f6152-130">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f6152-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f6152-131">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="f6152-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f6152-132">-SKUName</span><span class="sxs-lookup"><span data-stu-id="f6152-132">-SkuName</span></span>
<span data-ttu-id="f6152-133">SKU 的名稱</span><span class="sxs-lookup"><span data-stu-id="f6152-133">Name of the Sku</span></span>

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

### <span data-ttu-id="f6152-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f6152-134">-SkuTier</span></span>
<span data-ttu-id="f6152-135">SKU 層級</span><span class="sxs-lookup"><span data-stu-id="f6152-135">Tier of the Sku</span></span>

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

### <span data-ttu-id="f6152-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6152-136">-SubscriptionId</span></span>
<span data-ttu-id="f6152-137">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6152-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f6152-138">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f6152-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f6152-139">-標記</span><span class="sxs-lookup"><span data-stu-id="f6152-139">-Tag</span></span>
<span data-ttu-id="f6152-140">服務標記，這是描述資源的金鑰值組清單。</span><span class="sxs-lookup"><span data-stu-id="f6152-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="f6152-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="f6152-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="f6152-142">目標應用程式深入資訊便捷鍵</span><span class="sxs-lookup"><span data-stu-id="f6152-142">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="f6152-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="f6152-143">-TraceEnabled</span></span>
<span data-ttu-id="f6152-144">指出是否啟用追蹤功能</span><span class="sxs-lookup"><span data-stu-id="f6152-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="f6152-145">-確認</span><span class="sxs-lookup"><span data-stu-id="f6152-145">-Confirm</span></span>
<span data-ttu-id="f6152-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f6152-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6152-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6152-147">-WhatIf</span></span>
<span data-ttu-id="f6152-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6152-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6152-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6152-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6152-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6152-150">CommonParameters</span></span>
<span data-ttu-id="f6152-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f6152-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6152-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6152-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6152-153">輸入</span><span class="sxs-lookup"><span data-stu-id="f6152-153">INPUTS</span></span>

### <span data-ttu-id="f6152-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="f6152-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="f6152-155">輸出</span><span class="sxs-lookup"><span data-stu-id="f6152-155">OUTPUTS</span></span>

### <span data-ttu-id="f6152-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="f6152-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="f6152-157">筆記</span><span class="sxs-lookup"><span data-stu-id="f6152-157">NOTES</span></span>

<span data-ttu-id="f6152-158">別名</span><span class="sxs-lookup"><span data-stu-id="f6152-158">ALIASES</span></span>

<span data-ttu-id="f6152-159">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f6152-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6152-160">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f6152-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6152-161">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f6152-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6152-162">INPUTOBJECT： <ISpringCloudIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f6152-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6152-163">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6152-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="f6152-164">`[BindingName <String>]`：裝訂資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6152-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="f6152-165">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6152-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="f6152-166">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6152-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="f6152-167">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6152-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="f6152-168">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="f6152-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6152-169">`[Location <String>]`：地區</span><span class="sxs-lookup"><span data-stu-id="f6152-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="f6152-170">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f6152-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f6152-171">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="f6152-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f6152-172">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6152-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="f6152-173">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6152-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="f6152-174">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f6152-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f6152-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6152-175">RELATED LINKS</span></span>

