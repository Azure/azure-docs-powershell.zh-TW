---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 186b93c23de78bddcfb88946fbd19becee8ae938
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902753"
---
# <span data-ttu-id="e0fc5-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="e0fc5-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="e0fc5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e0fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="e0fc5-103">取得服務及其屬性。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="e0fc5-104">語法</span><span class="sxs-lookup"><span data-stu-id="e0fc5-104">SYNTAX</span></span>

### <span data-ttu-id="e0fc5-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="e0fc5-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e0fc5-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e0fc5-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e0fc5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e0fc5-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e0fc5-108">清單1</span><span class="sxs-lookup"><span data-stu-id="e0fc5-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0fc5-109">描述</span><span class="sxs-lookup"><span data-stu-id="e0fc5-109">DESCRIPTION</span></span>
<span data-ttu-id="e0fc5-110">取得服務及其屬性。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="e0fc5-111">例子</span><span class="sxs-lookup"><span data-stu-id="e0fc5-111">EXAMPLES</span></span>

### <span data-ttu-id="e0fc5-112">範例 1：按名稱取得 Spring Cloud Service</span><span class="sxs-lookup"><span data-stu-id="e0fc5-112">Example 1: Get Spring Cloud Service by name</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
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

<span data-ttu-id="e0fc5-113">以名稱取得春雲服務</span><span class="sxs-lookup"><span data-stu-id="e0fc5-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="e0fc5-114">範例 2：在資源群組下列出所有春雲服務。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="e0fc5-115">在資源群組下列出所有春意雲服務。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="e0fc5-116">參數</span><span class="sxs-lookup"><span data-stu-id="e0fc5-116">PARAMETERS</span></span>

### <span data-ttu-id="e0fc5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0fc5-117">-DefaultProfile</span></span>
<span data-ttu-id="e0fc5-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0fc5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0fc5-119">-InputObject</span></span>
<span data-ttu-id="e0fc5-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0fc5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0fc5-121">-Name</span></span>
<span data-ttu-id="e0fc5-122">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0fc5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0fc5-123">-ResourceGroupName</span></span>
<span data-ttu-id="e0fc5-124">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e0fc5-125">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0fc5-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0fc5-126">-SubscriptionId</span></span>
<span data-ttu-id="e0fc5-127">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e0fc5-128">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0fc5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0fc5-129">CommonParameters</span></span>
<span data-ttu-id="e0fc5-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0fc5-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0fc5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0fc5-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e0fc5-132">INPUTS</span></span>

### <span data-ttu-id="e0fc5-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="e0fc5-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="e0fc5-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e0fc5-134">OUTPUTS</span></span>

### <span data-ttu-id="e0fc5-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="e0fc5-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="e0fc5-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e0fc5-136">NOTES</span></span>

<span data-ttu-id="e0fc5-137">別名</span><span class="sxs-lookup"><span data-stu-id="e0fc5-137">ALIASES</span></span>

<span data-ttu-id="e0fc5-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e0fc5-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0fc5-139">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0fc5-140">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0fc5-141">INPUTOBJECT： <ISpringCloudIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e0fc5-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e0fc5-142">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="e0fc5-143">`[BindingName <String>]`：裝訂資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="e0fc5-144">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="e0fc5-145">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="e0fc5-146">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="e0fc5-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="e0fc5-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e0fc5-148">`[Location <String>]`：地區</span><span class="sxs-lookup"><span data-stu-id="e0fc5-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="e0fc5-149">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e0fc5-150">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e0fc5-151">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="e0fc5-152">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="e0fc5-153">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e0fc5-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e0fc5-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0fc5-154">RELATED LINKS</span></span>

