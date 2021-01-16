---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 39324dc0f85ca4d6f9c3498fae92c340e2113dad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277244"
---
# <span data-ttu-id="43237-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="43237-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="43237-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43237-102">SYNOPSIS</span></span>
<span data-ttu-id="43237-103">取得服務及其屬性。</span><span class="sxs-lookup"><span data-stu-id="43237-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="43237-104">句法</span><span class="sxs-lookup"><span data-stu-id="43237-104">SYNTAX</span></span>

### <span data-ttu-id="43237-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="43237-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43237-106">獲取</span><span class="sxs-lookup"><span data-stu-id="43237-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43237-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43237-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43237-108">List1</span><span class="sxs-lookup"><span data-stu-id="43237-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="43237-109">說明</span><span class="sxs-lookup"><span data-stu-id="43237-109">DESCRIPTION</span></span>
<span data-ttu-id="43237-110">取得服務及其屬性。</span><span class="sxs-lookup"><span data-stu-id="43237-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="43237-111">示例</span><span class="sxs-lookup"><span data-stu-id="43237-111">EXAMPLES</span></span>

### <span data-ttu-id="43237-112">範例1：透過名稱取得彈簧雲端服務</span><span class="sxs-lookup"><span data-stu-id="43237-112">Example 1: Get Spring Cloud Service by name</span></span>
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

<span data-ttu-id="43237-113">依名稱取得春季雲端服務</span><span class="sxs-lookup"><span data-stu-id="43237-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="43237-114">範例2：列出 [資源] 群組底下的所有彈簧雲端服務。</span><span class="sxs-lookup"><span data-stu-id="43237-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="43237-115">列出 [資源] 群組底下的所有彈簧雲端服務。</span><span class="sxs-lookup"><span data-stu-id="43237-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="43237-116">參數</span><span class="sxs-lookup"><span data-stu-id="43237-116">PARAMETERS</span></span>

### <span data-ttu-id="43237-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43237-117">-DefaultProfile</span></span>
<span data-ttu-id="43237-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43237-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43237-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43237-119">-InputObject</span></span>
<span data-ttu-id="43237-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="43237-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43237-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="43237-121">-Name</span></span>
<span data-ttu-id="43237-122">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43237-122">The name of the Service resource.</span></span>

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

### <span data-ttu-id="43237-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43237-123">-ResourceGroupName</span></span>
<span data-ttu-id="43237-124">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="43237-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="43237-125">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="43237-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="43237-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43237-126">-SubscriptionId</span></span>
<span data-ttu-id="43237-127">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="43237-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="43237-128">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="43237-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="43237-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43237-129">CommonParameters</span></span>
<span data-ttu-id="43237-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43237-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43237-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="43237-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43237-132">輸入</span><span class="sxs-lookup"><span data-stu-id="43237-132">INPUTS</span></span>

### <span data-ttu-id="43237-133">ISpringCloudIdentity （SpringCloud）的</span><span class="sxs-lookup"><span data-stu-id="43237-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="43237-134">輸出</span><span class="sxs-lookup"><span data-stu-id="43237-134">OUTPUTS</span></span>

### <span data-ttu-id="43237-135">IServiceResource （SpringCloud）。 Api20200701。</span><span class="sxs-lookup"><span data-stu-id="43237-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="43237-136">筆記</span><span class="sxs-lookup"><span data-stu-id="43237-136">NOTES</span></span>

<span data-ttu-id="43237-137">別名</span><span class="sxs-lookup"><span data-stu-id="43237-137">ALIASES</span></span>

<span data-ttu-id="43237-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="43237-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43237-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="43237-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43237-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="43237-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43237-141">INPUTOBJECT <ISpringCloudIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="43237-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43237-142">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43237-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="43237-143">`[BindingName <String>]`：系結資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43237-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="43237-144">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43237-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="43237-145">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43237-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="43237-146">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43237-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="43237-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="43237-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43237-148">`[Location <String>]`：區域</span><span class="sxs-lookup"><span data-stu-id="43237-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="43237-149">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="43237-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="43237-150">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="43237-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="43237-151">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43237-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="43237-152">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="43237-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="43237-153">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="43237-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="43237-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="43237-154">RELATED LINKS</span></span>

