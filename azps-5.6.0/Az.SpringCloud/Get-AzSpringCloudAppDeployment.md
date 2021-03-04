---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: b4b68f654c78da0dc2341966e3f9efaac397e504
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902749"
---
# <span data-ttu-id="3e282-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="3e282-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="3e282-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3e282-102">SYNOPSIS</span></span>
<span data-ttu-id="3e282-103">取得部署及其屬性。</span><span class="sxs-lookup"><span data-stu-id="3e282-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="3e282-104">語法</span><span class="sxs-lookup"><span data-stu-id="3e282-104">SYNTAX</span></span>

### <span data-ttu-id="3e282-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="3e282-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e282-106">獲取</span><span class="sxs-lookup"><span data-stu-id="3e282-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e282-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3e282-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e282-108">清單</span><span class="sxs-lookup"><span data-stu-id="3e282-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3e282-109">描述</span><span class="sxs-lookup"><span data-stu-id="3e282-109">DESCRIPTION</span></span>
<span data-ttu-id="3e282-110">取得部署及其屬性。</span><span class="sxs-lookup"><span data-stu-id="3e282-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="3e282-111">例子</span><span class="sxs-lookup"><span data-stu-id="3e282-111">EXAMPLES</span></span>

### <span data-ttu-id="3e282-112">範例 1：取得 Spring Cloud App Deploymeng by name。</span><span class="sxs-lookup"><span data-stu-id="3e282-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
Active                               : False
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-6bd6f87954-nl2wl}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : <default>
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="3e282-113">取得以名稱命名的 Spring Cloud App Deploymeng。</span><span class="sxs-lookup"><span data-stu-id="3e282-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="3e282-114">範例 2：列出在給定之春雲 App 下的所有部署。</span><span class="sxs-lookup"><span data-stu-id="3e282-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="3e282-115">列出在給定之春雲應用程式下的所有部署。</span><span class="sxs-lookup"><span data-stu-id="3e282-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="3e282-116">參數</span><span class="sxs-lookup"><span data-stu-id="3e282-116">PARAMETERS</span></span>

### <span data-ttu-id="3e282-117">-AppName</span><span class="sxs-lookup"><span data-stu-id="3e282-117">-AppName</span></span>
<span data-ttu-id="3e282-118">應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e282-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e282-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e282-119">-DefaultProfile</span></span>
<span data-ttu-id="3e282-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e282-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e282-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e282-121">-InputObject</span></span>
<span data-ttu-id="3e282-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3e282-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3e282-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e282-123">-Name</span></span>
<span data-ttu-id="3e282-124">部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e282-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e282-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e282-125">-ResourceGroupName</span></span>
<span data-ttu-id="3e282-126">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3e282-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3e282-127">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="3e282-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e282-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3e282-128">-ServiceName</span></span>
<span data-ttu-id="3e282-129">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e282-129">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e282-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e282-130">-SubscriptionId</span></span>
<span data-ttu-id="3e282-131">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e282-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3e282-132">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3e282-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3e282-133">-版本</span><span class="sxs-lookup"><span data-stu-id="3e282-133">-Version</span></span>
<span data-ttu-id="3e282-134">要列出的部署版本</span><span class="sxs-lookup"><span data-stu-id="3e282-134">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e282-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e282-135">CommonParameters</span></span>
<span data-ttu-id="3e282-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3e282-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e282-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e282-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e282-138">輸入</span><span class="sxs-lookup"><span data-stu-id="3e282-138">INPUTS</span></span>

### <span data-ttu-id="3e282-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="3e282-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="3e282-140">輸出</span><span class="sxs-lookup"><span data-stu-id="3e282-140">OUTPUTS</span></span>

### <span data-ttu-id="3e282-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="3e282-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="3e282-142">筆記</span><span class="sxs-lookup"><span data-stu-id="3e282-142">NOTES</span></span>

<span data-ttu-id="3e282-143">別名</span><span class="sxs-lookup"><span data-stu-id="3e282-143">ALIASES</span></span>

<span data-ttu-id="3e282-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3e282-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3e282-145">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3e282-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e282-146">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3e282-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3e282-147">INPUTOBJECT： <ISpringCloudIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3e282-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3e282-148">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e282-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="3e282-149">`[BindingName <String>]`：裝訂資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e282-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="3e282-150">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e282-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="3e282-151">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e282-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="3e282-152">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e282-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="3e282-153">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="3e282-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3e282-154">`[Location <String>]`：地區</span><span class="sxs-lookup"><span data-stu-id="3e282-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="3e282-155">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3e282-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3e282-156">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="3e282-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3e282-157">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e282-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="3e282-158">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e282-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="3e282-159">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3e282-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3e282-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e282-160">RELATED LINKS</span></span>

