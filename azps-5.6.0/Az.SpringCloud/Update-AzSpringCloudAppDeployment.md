---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 466bf2908cf1da940a369d2276dbf39106d60515
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915781"
---
# <span data-ttu-id="98f90-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="98f90-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="98f90-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98f90-102">SYNOPSIS</span></span>
<span data-ttu-id="98f90-103">更新即將離開部署的作業。</span><span class="sxs-lookup"><span data-stu-id="98f90-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="98f90-104">語法</span><span class="sxs-lookup"><span data-stu-id="98f90-104">SYNTAX</span></span>

### <span data-ttu-id="98f90-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="98f90-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="98f90-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="98f90-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="98f90-107">描述</span><span class="sxs-lookup"><span data-stu-id="98f90-107">DESCRIPTION</span></span>
<span data-ttu-id="98f90-108">更新即將離開部署的作業。</span><span class="sxs-lookup"><span data-stu-id="98f90-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="98f90-109">例子</span><span class="sxs-lookup"><span data-stu-id="98f90-109">EXAMPLES</span></span>

### <span data-ttu-id="98f90-110">範例 1：按名稱更新 Spring Cloud 部署。</span><span class="sxs-lookup"><span data-stu-id="98f90-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="98f90-111">按名稱更新春雲部署。</span><span class="sxs-lookup"><span data-stu-id="98f90-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="98f90-112">範例 2：從管道更新 Spring Cloud 部署。</span><span class="sxs-lookup"><span data-stu-id="98f90-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Update-AzSpringCloudAppDeployment -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="98f90-113">從管道更新春雲部署。</span><span class="sxs-lookup"><span data-stu-id="98f90-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="98f90-114">參數</span><span class="sxs-lookup"><span data-stu-id="98f90-114">PARAMETERS</span></span>

### <span data-ttu-id="98f90-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="98f90-115">-AppName</span></span>
<span data-ttu-id="98f90-116">應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="98f90-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="98f90-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98f90-117">-AsJob</span></span>
<span data-ttu-id="98f90-118">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="98f90-118">Run the command as a job</span></span>

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

### <span data-ttu-id="98f90-119">-Cpu</span><span class="sxs-lookup"><span data-stu-id="98f90-119">-Cpu</span></span>
<span data-ttu-id="98f90-120">必要的 CPU</span><span class="sxs-lookup"><span data-stu-id="98f90-120">Required CPU</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f90-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f90-121">-DefaultProfile</span></span>
<span data-ttu-id="98f90-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="98f90-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98f90-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="98f90-123">-EnvironmentVariable</span></span>
<span data-ttu-id="98f90-124">環境變數集合</span><span class="sxs-lookup"><span data-stu-id="98f90-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="98f90-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98f90-125">-InputObject</span></span>
<span data-ttu-id="98f90-126">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="98f90-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="98f90-127">-進一無二</span><span class="sxs-lookup"><span data-stu-id="98f90-127">-JvmOption</span></span>
<span data-ttu-id="98f90-128">PARAMETERM 參數</span><span class="sxs-lookup"><span data-stu-id="98f90-128">JVM parameter</span></span>

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

### <span data-ttu-id="98f90-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="98f90-129">-MemoryInGb</span></span>
<span data-ttu-id="98f90-130">所需的記憶體大小 ，以 GB 為單位</span><span class="sxs-lookup"><span data-stu-id="98f90-130">Required Memory size in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f90-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="98f90-131">-Name</span></span>
<span data-ttu-id="98f90-132">部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="98f90-132">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f90-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="98f90-133">-NoWait</span></span>
<span data-ttu-id="98f90-134">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="98f90-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="98f90-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f90-135">-ResourceGroupName</span></span>
<span data-ttu-id="98f90-136">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="98f90-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="98f90-137">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="98f90-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="98f90-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="98f90-138">-RuntimeVersion</span></span>
<span data-ttu-id="98f90-139">執行時間版本</span><span class="sxs-lookup"><span data-stu-id="98f90-139">Runtime version</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.RuntimeVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f90-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="98f90-140">-ServiceName</span></span>
<span data-ttu-id="98f90-141">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="98f90-141">The name of the Service resource.</span></span>

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

### <span data-ttu-id="98f90-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="98f90-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="98f90-143">用於多模組專案部署之產品選取器。</span><span class="sxs-lookup"><span data-stu-id="98f90-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="98f90-144">這應該是目的模組/專案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="98f90-144">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="98f90-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="98f90-145">-SourceRelativePath</span></span>
<span data-ttu-id="98f90-146">儲存來源之儲存空間的相對路徑</span><span class="sxs-lookup"><span data-stu-id="98f90-146">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="98f90-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="98f90-147">-SourceType</span></span>
<span data-ttu-id="98f90-148">上傳的來源類型</span><span class="sxs-lookup"><span data-stu-id="98f90-148">Type of the source uploaded</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.UserSourceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f90-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="98f90-149">-SourceVersion</span></span>
<span data-ttu-id="98f90-150">來源版本</span><span class="sxs-lookup"><span data-stu-id="98f90-150">Version of the source</span></span>

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

### <span data-ttu-id="98f90-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98f90-151">-SubscriptionId</span></span>
<span data-ttu-id="98f90-152">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="98f90-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="98f90-153">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="98f90-153">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="98f90-154">-確認</span><span class="sxs-lookup"><span data-stu-id="98f90-154">-Confirm</span></span>
<span data-ttu-id="98f90-155">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="98f90-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98f90-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98f90-156">-WhatIf</span></span>
<span data-ttu-id="98f90-157">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98f90-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98f90-158">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98f90-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98f90-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f90-159">CommonParameters</span></span>
<span data-ttu-id="98f90-160">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98f90-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f90-161">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98f90-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f90-162">輸入</span><span class="sxs-lookup"><span data-stu-id="98f90-162">INPUTS</span></span>

### <span data-ttu-id="98f90-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="98f90-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="98f90-164">輸出</span><span class="sxs-lookup"><span data-stu-id="98f90-164">OUTPUTS</span></span>

### <span data-ttu-id="98f90-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="98f90-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="98f90-166">筆記</span><span class="sxs-lookup"><span data-stu-id="98f90-166">NOTES</span></span>

<span data-ttu-id="98f90-167">別名</span><span class="sxs-lookup"><span data-stu-id="98f90-167">ALIASES</span></span>

<span data-ttu-id="98f90-168">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="98f90-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="98f90-169">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="98f90-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="98f90-170">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="98f90-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="98f90-171">INPUTOBJECT： <ISpringCloudIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="98f90-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="98f90-172">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="98f90-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="98f90-173">`[BindingName <String>]`：裝訂資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="98f90-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="98f90-174">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="98f90-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="98f90-175">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="98f90-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="98f90-176">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="98f90-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="98f90-177">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="98f90-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="98f90-178">`[Location <String>]`：地區</span><span class="sxs-lookup"><span data-stu-id="98f90-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="98f90-179">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="98f90-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="98f90-180">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="98f90-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="98f90-181">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="98f90-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="98f90-182">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="98f90-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="98f90-183">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="98f90-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="98f90-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="98f90-184">RELATED LINKS</span></span>

