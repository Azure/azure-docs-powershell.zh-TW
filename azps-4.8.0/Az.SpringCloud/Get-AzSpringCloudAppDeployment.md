---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: d33f649d71a8fb3f4a112ac77937f37d867a24c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129884"
---
# <span data-ttu-id="bc10e-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="bc10e-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="bc10e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc10e-102">SYNOPSIS</span></span>
<span data-ttu-id="bc10e-103">取得部署及其屬性。</span><span class="sxs-lookup"><span data-stu-id="bc10e-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="bc10e-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc10e-104">SYNTAX</span></span>

### <span data-ttu-id="bc10e-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="bc10e-105">List (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bc10e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="bc10e-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bc10e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bc10e-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc10e-108">說明</span><span class="sxs-lookup"><span data-stu-id="bc10e-108">DESCRIPTION</span></span>
<span data-ttu-id="bc10e-109">取得部署及其屬性。</span><span class="sxs-lookup"><span data-stu-id="bc10e-109">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="bc10e-110">示例</span><span class="sxs-lookup"><span data-stu-id="bc10e-110">EXAMPLES</span></span>

### <span data-ttu-id="bc10e-111">範例1：透過名稱取得彈簧雲端 App Deploymeng。</span><span class="sxs-lookup"><span data-stu-id="bc10e-111">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="bc10e-112">透過名稱取得春季雲端 App Deploymeng。</span><span class="sxs-lookup"><span data-stu-id="bc10e-112">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="bc10e-113">範例2：列出指定彈簧雲端 app 下的所有部署。</span><span class="sxs-lookup"><span data-stu-id="bc10e-113">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="bc10e-114">列出指定春季雲端 app 下的所有部署。</span><span class="sxs-lookup"><span data-stu-id="bc10e-114">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="bc10e-115">參數</span><span class="sxs-lookup"><span data-stu-id="bc10e-115">PARAMETERS</span></span>

### <span data-ttu-id="bc10e-116">-AppName</span><span class="sxs-lookup"><span data-stu-id="bc10e-116">-AppName</span></span>
<span data-ttu-id="bc10e-117">App 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc10e-117">The name of the App resource.</span></span>

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

### <span data-ttu-id="bc10e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc10e-118">-DefaultProfile</span></span>
<span data-ttu-id="bc10e-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc10e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc10e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc10e-120">-InputObject</span></span>
<span data-ttu-id="bc10e-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="bc10e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bc10e-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc10e-122">-Name</span></span>
<span data-ttu-id="bc10e-123">部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc10e-123">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="bc10e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc10e-124">-ResourceGroupName</span></span>
<span data-ttu-id="bc10e-125">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc10e-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="bc10e-126">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="bc10e-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="bc10e-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bc10e-127">-ServiceName</span></span>
<span data-ttu-id="bc10e-128">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc10e-128">The name of the Service resource.</span></span>

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

### <span data-ttu-id="bc10e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc10e-129">-SubscriptionId</span></span>
<span data-ttu-id="bc10e-130">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="bc10e-130">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="bc10e-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="bc10e-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc10e-132">-版本</span><span class="sxs-lookup"><span data-stu-id="bc10e-132">-Version</span></span>
<span data-ttu-id="bc10e-133">要列出的部署版本</span><span class="sxs-lookup"><span data-stu-id="bc10e-133">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc10e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc10e-134">CommonParameters</span></span>
<span data-ttu-id="bc10e-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc10e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc10e-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bc10e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc10e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="bc10e-137">INPUTS</span></span>

### <span data-ttu-id="bc10e-138">ISpringCloudIdentity （SpringCloud）的</span><span class="sxs-lookup"><span data-stu-id="bc10e-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="bc10e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="bc10e-139">OUTPUTS</span></span>

### <span data-ttu-id="bc10e-140">IDeploymentResource （SpringCloud）。 Api20190501Preview。</span><span class="sxs-lookup"><span data-stu-id="bc10e-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="bc10e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="bc10e-141">NOTES</span></span>

<span data-ttu-id="bc10e-142">別名</span><span class="sxs-lookup"><span data-stu-id="bc10e-142">ALIASES</span></span>

<span data-ttu-id="bc10e-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="bc10e-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bc10e-144">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="bc10e-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc10e-145">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="bc10e-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bc10e-146">INPUTOBJECT <ISpringCloudIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="bc10e-146">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bc10e-147">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc10e-147">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="bc10e-148">`[BindingName <String>]`：系結資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc10e-148">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="bc10e-149">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc10e-149">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="bc10e-150">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc10e-150">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="bc10e-151">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc10e-151">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="bc10e-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="bc10e-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bc10e-153">`[Location <String>]`：區域</span><span class="sxs-lookup"><span data-stu-id="bc10e-153">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="bc10e-154">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc10e-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="bc10e-155">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="bc10e-155">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="bc10e-156">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc10e-156">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="bc10e-157">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="bc10e-157">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="bc10e-158">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="bc10e-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bc10e-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc10e-159">RELATED LINKS</span></span>

