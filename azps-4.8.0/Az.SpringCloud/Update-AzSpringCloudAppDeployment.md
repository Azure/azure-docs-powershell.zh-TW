---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f19383959e2a342555c7a741524e687b7bac37a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129228"
---
# <span data-ttu-id="329c2-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="329c2-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="329c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="329c2-102">SYNOPSIS</span></span>
<span data-ttu-id="329c2-103">更新現有部署的操作。</span><span class="sxs-lookup"><span data-stu-id="329c2-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="329c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="329c2-104">SYNTAX</span></span>

### <span data-ttu-id="329c2-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="329c2-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="329c2-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="329c2-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="329c2-107">說明</span><span class="sxs-lookup"><span data-stu-id="329c2-107">DESCRIPTION</span></span>
<span data-ttu-id="329c2-108">更新現有部署的操作。</span><span class="sxs-lookup"><span data-stu-id="329c2-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="329c2-109">示例</span><span class="sxs-lookup"><span data-stu-id="329c2-109">EXAMPLES</span></span>

### <span data-ttu-id="329c2-110">範例1：依名稱更新彈簧雲端部署。</span><span class="sxs-lookup"><span data-stu-id="329c2-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="329c2-111">依名稱更新彈簧雲端部署。</span><span class="sxs-lookup"><span data-stu-id="329c2-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="329c2-112">範例2：從管道更新彈簧雲端部署。</span><span class="sxs-lookup"><span data-stu-id="329c2-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="329c2-113">從管道更新彈簧雲端部署。</span><span class="sxs-lookup"><span data-stu-id="329c2-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="329c2-114">參數</span><span class="sxs-lookup"><span data-stu-id="329c2-114">PARAMETERS</span></span>

### <span data-ttu-id="329c2-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="329c2-115">-AppName</span></span>
<span data-ttu-id="329c2-116">App 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="329c2-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="329c2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="329c2-117">-AsJob</span></span>
<span data-ttu-id="329c2-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="329c2-118">Run the command as a job</span></span>

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

### <span data-ttu-id="329c2-119">-Cpu</span><span class="sxs-lookup"><span data-stu-id="329c2-119">-Cpu</span></span>
<span data-ttu-id="329c2-120">所需的 CPU</span><span class="sxs-lookup"><span data-stu-id="329c2-120">Required CPU</span></span>

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

### <span data-ttu-id="329c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="329c2-121">-DefaultProfile</span></span>
<span data-ttu-id="329c2-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="329c2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="329c2-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="329c2-123">-EnvironmentVariable</span></span>
<span data-ttu-id="329c2-124">環境變數集合</span><span class="sxs-lookup"><span data-stu-id="329c2-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="329c2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="329c2-125">-InputObject</span></span>
<span data-ttu-id="329c2-126">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="329c2-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="329c2-127">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="329c2-127">-InstanceCount</span></span>
<span data-ttu-id="329c2-128">實例計數</span><span class="sxs-lookup"><span data-stu-id="329c2-128">Instance count</span></span>

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

### <span data-ttu-id="329c2-129">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="329c2-129">-JvmOption</span></span>
<span data-ttu-id="329c2-130">JVM 參數</span><span class="sxs-lookup"><span data-stu-id="329c2-130">JVM parameter</span></span>

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

### <span data-ttu-id="329c2-131">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="329c2-131">-MemoryInGb</span></span>
<span data-ttu-id="329c2-132">所需的記憶體大小（GB）</span><span class="sxs-lookup"><span data-stu-id="329c2-132">Required Memory size in GB</span></span>

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

### <span data-ttu-id="329c2-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="329c2-133">-Name</span></span>
<span data-ttu-id="329c2-134">部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="329c2-134">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="329c2-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="329c2-135">-NoWait</span></span>
<span data-ttu-id="329c2-136">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="329c2-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="329c2-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="329c2-137">-ResourceGroupName</span></span>
<span data-ttu-id="329c2-138">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="329c2-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="329c2-139">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="329c2-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="329c2-140">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="329c2-140">-RuntimeVersion</span></span>
<span data-ttu-id="329c2-141">執行時間版本</span><span class="sxs-lookup"><span data-stu-id="329c2-141">Runtime version</span></span>

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

### <span data-ttu-id="329c2-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="329c2-142">-ServiceName</span></span>
<span data-ttu-id="329c2-143">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="329c2-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="329c2-144">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="329c2-144">-SourceArtifactSelector</span></span>
<span data-ttu-id="329c2-145">要用於多模組專案部署的專案選擇器。</span><span class="sxs-lookup"><span data-stu-id="329c2-145">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="329c2-146">這應該 bethe 目的模組/專案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="329c2-146">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="329c2-147">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="329c2-147">-SourceRelativePath</span></span>
<span data-ttu-id="329c2-148">儲存來源的儲存空間相對路徑</span><span class="sxs-lookup"><span data-stu-id="329c2-148">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="329c2-149">-SourceType</span><span class="sxs-lookup"><span data-stu-id="329c2-149">-SourceType</span></span>
<span data-ttu-id="329c2-150">上傳來源的類型</span><span class="sxs-lookup"><span data-stu-id="329c2-150">Type of the source uploaded</span></span>

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

### <span data-ttu-id="329c2-151">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="329c2-151">-SourceVersion</span></span>
<span data-ttu-id="329c2-152">來源的版本</span><span class="sxs-lookup"><span data-stu-id="329c2-152">Version of the source</span></span>

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

### <span data-ttu-id="329c2-153">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="329c2-153">-SubscriptionId</span></span>
<span data-ttu-id="329c2-154">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="329c2-154">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="329c2-155">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="329c2-155">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="329c2-156">-確認</span><span class="sxs-lookup"><span data-stu-id="329c2-156">-Confirm</span></span>
<span data-ttu-id="329c2-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="329c2-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="329c2-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="329c2-158">-WhatIf</span></span>
<span data-ttu-id="329c2-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="329c2-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="329c2-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="329c2-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="329c2-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="329c2-161">CommonParameters</span></span>
<span data-ttu-id="329c2-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="329c2-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="329c2-163">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="329c2-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="329c2-164">輸入</span><span class="sxs-lookup"><span data-stu-id="329c2-164">INPUTS</span></span>

### <span data-ttu-id="329c2-165">ISpringCloudIdentity （SpringCloud）的</span><span class="sxs-lookup"><span data-stu-id="329c2-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="329c2-166">輸出</span><span class="sxs-lookup"><span data-stu-id="329c2-166">OUTPUTS</span></span>

### <span data-ttu-id="329c2-167">IDeploymentResource （SpringCloud）。 Api20190501Preview。</span><span class="sxs-lookup"><span data-stu-id="329c2-167">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="329c2-168">筆記</span><span class="sxs-lookup"><span data-stu-id="329c2-168">NOTES</span></span>

<span data-ttu-id="329c2-169">別名</span><span class="sxs-lookup"><span data-stu-id="329c2-169">ALIASES</span></span>

<span data-ttu-id="329c2-170">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="329c2-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="329c2-171">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="329c2-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="329c2-172">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="329c2-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="329c2-173">INPUTOBJECT <ISpringCloudIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="329c2-173">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="329c2-174">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="329c2-174">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="329c2-175">`[BindingName <String>]`：系結資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="329c2-175">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="329c2-176">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="329c2-176">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="329c2-177">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="329c2-177">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="329c2-178">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="329c2-178">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="329c2-179">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="329c2-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="329c2-180">`[Location <String>]`：區域</span><span class="sxs-lookup"><span data-stu-id="329c2-180">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="329c2-181">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="329c2-181">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="329c2-182">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="329c2-182">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="329c2-183">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="329c2-183">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="329c2-184">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="329c2-184">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="329c2-185">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="329c2-185">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="329c2-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="329c2-186">RELATED LINKS</span></span>

