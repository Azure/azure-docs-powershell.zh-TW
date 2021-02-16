---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: ba31f4d7c81392a30f4f8b9073d967b2a57cfab7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133499"
---
# <span data-ttu-id="69be5-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="69be5-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="69be5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69be5-102">SYNOPSIS</span></span>
<span data-ttu-id="69be5-103">更新現有部署的操作。</span><span class="sxs-lookup"><span data-stu-id="69be5-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="69be5-104">句法</span><span class="sxs-lookup"><span data-stu-id="69be5-104">SYNTAX</span></span>

### <span data-ttu-id="69be5-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="69be5-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="69be5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="69be5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69be5-107">說明</span><span class="sxs-lookup"><span data-stu-id="69be5-107">DESCRIPTION</span></span>
<span data-ttu-id="69be5-108">更新現有部署的操作。</span><span class="sxs-lookup"><span data-stu-id="69be5-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="69be5-109">示例</span><span class="sxs-lookup"><span data-stu-id="69be5-109">EXAMPLES</span></span>

### <span data-ttu-id="69be5-110">範例1：依名稱更新彈簧雲端部署。</span><span class="sxs-lookup"><span data-stu-id="69be5-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="69be5-111">依名稱更新彈簧雲端部署。</span><span class="sxs-lookup"><span data-stu-id="69be5-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="69be5-112">範例2：從管道更新彈簧雲端部署。</span><span class="sxs-lookup"><span data-stu-id="69be5-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="69be5-113">從管道更新彈簧雲端部署。</span><span class="sxs-lookup"><span data-stu-id="69be5-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="69be5-114">參數</span><span class="sxs-lookup"><span data-stu-id="69be5-114">PARAMETERS</span></span>

### <span data-ttu-id="69be5-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="69be5-115">-AppName</span></span>
<span data-ttu-id="69be5-116">App 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="69be5-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="69be5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69be5-117">-AsJob</span></span>
<span data-ttu-id="69be5-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="69be5-118">Run the command as a job</span></span>

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

### <span data-ttu-id="69be5-119">-Cpu</span><span class="sxs-lookup"><span data-stu-id="69be5-119">-Cpu</span></span>
<span data-ttu-id="69be5-120">所需的 CPU</span><span class="sxs-lookup"><span data-stu-id="69be5-120">Required CPU</span></span>

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

### <span data-ttu-id="69be5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69be5-121">-DefaultProfile</span></span>
<span data-ttu-id="69be5-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69be5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69be5-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="69be5-123">-EnvironmentVariable</span></span>
<span data-ttu-id="69be5-124">環境變數集合</span><span class="sxs-lookup"><span data-stu-id="69be5-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="69be5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69be5-125">-InputObject</span></span>
<span data-ttu-id="69be5-126">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="69be5-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="69be5-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="69be5-127">-JvmOption</span></span>
<span data-ttu-id="69be5-128">JVM 參數</span><span class="sxs-lookup"><span data-stu-id="69be5-128">JVM parameter</span></span>

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

### <span data-ttu-id="69be5-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="69be5-129">-MemoryInGb</span></span>
<span data-ttu-id="69be5-130">所需的記憶體大小（GB）</span><span class="sxs-lookup"><span data-stu-id="69be5-130">Required Memory size in GB</span></span>

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

### <span data-ttu-id="69be5-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="69be5-131">-Name</span></span>
<span data-ttu-id="69be5-132">部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="69be5-132">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="69be5-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="69be5-133">-NoWait</span></span>
<span data-ttu-id="69be5-134">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="69be5-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="69be5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69be5-135">-ResourceGroupName</span></span>
<span data-ttu-id="69be5-136">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="69be5-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="69be5-137">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="69be5-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="69be5-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="69be5-138">-RuntimeVersion</span></span>
<span data-ttu-id="69be5-139">執行時間版本</span><span class="sxs-lookup"><span data-stu-id="69be5-139">Runtime version</span></span>

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

### <span data-ttu-id="69be5-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="69be5-140">-ServiceName</span></span>
<span data-ttu-id="69be5-141">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="69be5-141">The name of the Service resource.</span></span>

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

### <span data-ttu-id="69be5-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="69be5-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="69be5-143">要用於多模組專案部署的專案選擇器。</span><span class="sxs-lookup"><span data-stu-id="69be5-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="69be5-144">這應該 bethe 目的模組/專案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="69be5-144">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="69be5-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="69be5-145">-SourceRelativePath</span></span>
<span data-ttu-id="69be5-146">儲存來源的儲存空間相對路徑</span><span class="sxs-lookup"><span data-stu-id="69be5-146">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="69be5-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="69be5-147">-SourceType</span></span>
<span data-ttu-id="69be5-148">上傳來源的類型</span><span class="sxs-lookup"><span data-stu-id="69be5-148">Type of the source uploaded</span></span>

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

### <span data-ttu-id="69be5-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="69be5-149">-SourceVersion</span></span>
<span data-ttu-id="69be5-150">來源的版本</span><span class="sxs-lookup"><span data-stu-id="69be5-150">Version of the source</span></span>

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

### <span data-ttu-id="69be5-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69be5-151">-SubscriptionId</span></span>
<span data-ttu-id="69be5-152">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="69be5-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="69be5-153">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="69be5-153">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="69be5-154">-確認</span><span class="sxs-lookup"><span data-stu-id="69be5-154">-Confirm</span></span>
<span data-ttu-id="69be5-155">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="69be5-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69be5-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69be5-156">-WhatIf</span></span>
<span data-ttu-id="69be5-157">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69be5-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69be5-158">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69be5-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69be5-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69be5-159">CommonParameters</span></span>
<span data-ttu-id="69be5-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69be5-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69be5-161">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="69be5-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69be5-162">輸入</span><span class="sxs-lookup"><span data-stu-id="69be5-162">INPUTS</span></span>

### <span data-ttu-id="69be5-163">ISpringCloudIdentity （SpringCloud）的</span><span class="sxs-lookup"><span data-stu-id="69be5-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="69be5-164">輸出</span><span class="sxs-lookup"><span data-stu-id="69be5-164">OUTPUTS</span></span>

### <span data-ttu-id="69be5-165">IDeploymentResource （SpringCloud）。 Api20200701。</span><span class="sxs-lookup"><span data-stu-id="69be5-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="69be5-166">筆記</span><span class="sxs-lookup"><span data-stu-id="69be5-166">NOTES</span></span>

<span data-ttu-id="69be5-167">別名</span><span class="sxs-lookup"><span data-stu-id="69be5-167">ALIASES</span></span>

<span data-ttu-id="69be5-168">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="69be5-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="69be5-169">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="69be5-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="69be5-170">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="69be5-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="69be5-171">INPUTOBJECT <ISpringCloudIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="69be5-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="69be5-172">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="69be5-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="69be5-173">`[BindingName <String>]`：系結資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="69be5-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="69be5-174">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="69be5-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="69be5-175">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="69be5-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="69be5-176">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="69be5-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="69be5-177">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="69be5-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="69be5-178">`[Location <String>]`：區域</span><span class="sxs-lookup"><span data-stu-id="69be5-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="69be5-179">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="69be5-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="69be5-180">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="69be5-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="69be5-181">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="69be5-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="69be5-182">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="69be5-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="69be5-183">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="69be5-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="69be5-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="69be5-184">RELATED LINKS</span></span>

