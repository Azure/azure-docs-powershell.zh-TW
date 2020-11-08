---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3accf4b622f77edb0e3d0cea6fe67bbc1db9ff6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136689"
---
# <span data-ttu-id="332bd-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="332bd-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="332bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="332bd-102">SYNOPSIS</span></span>
<span data-ttu-id="332bd-103">取得部署及其屬性。</span><span class="sxs-lookup"><span data-stu-id="332bd-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="332bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="332bd-104">SYNTAX</span></span>

### <span data-ttu-id="332bd-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="332bd-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="332bd-106">獲取</span><span class="sxs-lookup"><span data-stu-id="332bd-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="332bd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="332bd-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="332bd-108">清單</span><span class="sxs-lookup"><span data-stu-id="332bd-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="332bd-109">說明</span><span class="sxs-lookup"><span data-stu-id="332bd-109">DESCRIPTION</span></span>
<span data-ttu-id="332bd-110">取得部署及其屬性。</span><span class="sxs-lookup"><span data-stu-id="332bd-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="332bd-111">示例</span><span class="sxs-lookup"><span data-stu-id="332bd-111">EXAMPLES</span></span>

### <span data-ttu-id="332bd-112">範例1：透過名稱取得彈簧雲端 App Deploymeng。</span><span class="sxs-lookup"><span data-stu-id="332bd-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="332bd-113">透過名稱取得春季雲端 App Deploymeng。</span><span class="sxs-lookup"><span data-stu-id="332bd-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="332bd-114">範例2：列出指定彈簧雲端 app 下的所有部署。</span><span class="sxs-lookup"><span data-stu-id="332bd-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="332bd-115">列出指定春季雲端 app 下的所有部署。</span><span class="sxs-lookup"><span data-stu-id="332bd-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="332bd-116">參數</span><span class="sxs-lookup"><span data-stu-id="332bd-116">PARAMETERS</span></span>

### <span data-ttu-id="332bd-117">-AppName</span><span class="sxs-lookup"><span data-stu-id="332bd-117">-AppName</span></span>
<span data-ttu-id="332bd-118">App 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="332bd-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="332bd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="332bd-119">-DefaultProfile</span></span>
<span data-ttu-id="332bd-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="332bd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="332bd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="332bd-121">-InputObject</span></span>
<span data-ttu-id="332bd-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="332bd-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="332bd-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="332bd-123">-Name</span></span>
<span data-ttu-id="332bd-124">部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="332bd-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="332bd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="332bd-125">-ResourceGroupName</span></span>
<span data-ttu-id="332bd-126">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="332bd-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="332bd-127">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="332bd-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="332bd-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="332bd-128">-ServiceName</span></span>
<span data-ttu-id="332bd-129">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="332bd-129">The name of the Service resource.</span></span>

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

### <span data-ttu-id="332bd-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="332bd-130">-SubscriptionId</span></span>
<span data-ttu-id="332bd-131">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="332bd-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="332bd-132">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="332bd-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="332bd-133">-版本</span><span class="sxs-lookup"><span data-stu-id="332bd-133">-Version</span></span>
<span data-ttu-id="332bd-134">要列出的部署版本</span><span class="sxs-lookup"><span data-stu-id="332bd-134">Version of the deployments to be listed</span></span>

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

### <span data-ttu-id="332bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="332bd-135">CommonParameters</span></span>
<span data-ttu-id="332bd-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="332bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="332bd-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="332bd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="332bd-138">輸入</span><span class="sxs-lookup"><span data-stu-id="332bd-138">INPUTS</span></span>

### <span data-ttu-id="332bd-139">ISpringCloudIdentity （SpringCloud）的</span><span class="sxs-lookup"><span data-stu-id="332bd-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="332bd-140">輸出</span><span class="sxs-lookup"><span data-stu-id="332bd-140">OUTPUTS</span></span>

### <span data-ttu-id="332bd-141">IDeploymentResource （SpringCloud）。 Api20200701。</span><span class="sxs-lookup"><span data-stu-id="332bd-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="332bd-142">筆記</span><span class="sxs-lookup"><span data-stu-id="332bd-142">NOTES</span></span>

<span data-ttu-id="332bd-143">別名</span><span class="sxs-lookup"><span data-stu-id="332bd-143">ALIASES</span></span>

<span data-ttu-id="332bd-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="332bd-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="332bd-145">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="332bd-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="332bd-146">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="332bd-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="332bd-147">INPUTOBJECT <ISpringCloudIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="332bd-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="332bd-148">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="332bd-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="332bd-149">`[BindingName <String>]`：系結資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="332bd-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="332bd-150">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="332bd-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="332bd-151">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="332bd-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="332bd-152">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="332bd-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="332bd-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="332bd-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="332bd-154">`[Location <String>]`：區域</span><span class="sxs-lookup"><span data-stu-id="332bd-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="332bd-155">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="332bd-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="332bd-156">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="332bd-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="332bd-157">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="332bd-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="332bd-158">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="332bd-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="332bd-159">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="332bd-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="332bd-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="332bd-160">RELATED LINKS</span></span>

