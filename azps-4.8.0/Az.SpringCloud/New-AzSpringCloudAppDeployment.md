---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 0669371f589722e3da18e554df98dbf7d193ccc8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129872"
---
# <span data-ttu-id="6c5f4-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="6c5f4-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="6c5f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c5f4-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5f4-103">建立新部署或更新現有的部署。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="6c5f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c5f4-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6c5f4-105">說明</span><span class="sxs-lookup"><span data-stu-id="6c5f4-105">DESCRIPTION</span></span>
<span data-ttu-id="6c5f4-106">建立新部署或更新現有的部署。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="6c5f4-107">示例</span><span class="sxs-lookup"><span data-stu-id="6c5f4-107">EXAMPLES</span></span>

### <span data-ttu-id="6c5f4-108">範例1：範例1：建立彈簧雲端部署。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
```powershell
PS C:\> New-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rp -name spring-cloud-service -AppName gateway -DeploymentName default

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

<span data-ttu-id="6c5f4-109">建立彈簧雲端部署。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="6c5f4-110">參數</span><span class="sxs-lookup"><span data-stu-id="6c5f4-110">PARAMETERS</span></span>

### <span data-ttu-id="6c5f4-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="6c5f4-111">-AppName</span></span>
<span data-ttu-id="6c5f4-112">App 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-112">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c5f4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c5f4-113">-AsJob</span></span>
<span data-ttu-id="6c5f4-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="6c5f4-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6c5f4-115">-Cpu</span><span class="sxs-lookup"><span data-stu-id="6c5f4-115">-Cpu</span></span>
<span data-ttu-id="6c5f4-116">所需的 CPU</span><span class="sxs-lookup"><span data-stu-id="6c5f4-116">Required CPU</span></span>

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

### <span data-ttu-id="6c5f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5f4-117">-DefaultProfile</span></span>
<span data-ttu-id="6c5f4-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c5f4-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="6c5f4-119">-EnvironmentVariable</span></span>
<span data-ttu-id="6c5f4-120">環境變數集合</span><span class="sxs-lookup"><span data-stu-id="6c5f4-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="6c5f4-121">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="6c5f4-121">-InstanceCount</span></span>
<span data-ttu-id="6c5f4-122">實例計數</span><span class="sxs-lookup"><span data-stu-id="6c5f4-122">Instance count</span></span>

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

### <span data-ttu-id="6c5f4-123">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="6c5f4-123">-JvmOption</span></span>
<span data-ttu-id="6c5f4-124">JVM 參數</span><span class="sxs-lookup"><span data-stu-id="6c5f4-124">JVM parameter</span></span>

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

### <span data-ttu-id="6c5f4-125">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="6c5f4-125">-MemoryInGb</span></span>
<span data-ttu-id="6c5f4-126">所需的記憶體大小（GB）</span><span class="sxs-lookup"><span data-stu-id="6c5f4-126">Required Memory size in GB</span></span>

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

### <span data-ttu-id="6c5f4-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c5f4-127">-Name</span></span>
<span data-ttu-id="6c5f4-128">部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-128">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c5f4-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6c5f4-129">-NoWait</span></span>
<span data-ttu-id="6c5f4-130">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="6c5f4-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6c5f4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c5f4-131">-ResourceGroupName</span></span>
<span data-ttu-id="6c5f4-132">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-132">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6c5f4-133">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c5f4-134">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="6c5f4-134">-RuntimeVersion</span></span>
<span data-ttu-id="6c5f4-135">執行時間版本</span><span class="sxs-lookup"><span data-stu-id="6c5f4-135">Runtime version</span></span>

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

### <span data-ttu-id="6c5f4-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6c5f4-136">-ServiceName</span></span>
<span data-ttu-id="6c5f4-137">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-137">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c5f4-138">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="6c5f4-138">-SourceArtifactSelector</span></span>
<span data-ttu-id="6c5f4-139">要用於多模組專案部署的專案選擇器。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-139">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="6c5f4-140">這應該 bethe 目的模組/專案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-140">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="6c5f4-141">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="6c5f4-141">-SourceRelativePath</span></span>
<span data-ttu-id="6c5f4-142">儲存來源的儲存空間相對路徑</span><span class="sxs-lookup"><span data-stu-id="6c5f4-142">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="6c5f4-143">-SourceType</span><span class="sxs-lookup"><span data-stu-id="6c5f4-143">-SourceType</span></span>
<span data-ttu-id="6c5f4-144">上傳來源的類型</span><span class="sxs-lookup"><span data-stu-id="6c5f4-144">Type of the source uploaded</span></span>

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

### <span data-ttu-id="6c5f4-145">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="6c5f4-145">-SourceVersion</span></span>
<span data-ttu-id="6c5f4-146">來源的版本</span><span class="sxs-lookup"><span data-stu-id="6c5f4-146">Version of the source</span></span>

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

### <span data-ttu-id="6c5f4-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c5f4-147">-SubscriptionId</span></span>
<span data-ttu-id="6c5f4-148">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-148">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6c5f4-149">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-149">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c5f4-150">-確認</span><span class="sxs-lookup"><span data-stu-id="6c5f4-150">-Confirm</span></span>
<span data-ttu-id="6c5f4-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c5f4-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c5f4-152">-WhatIf</span></span>
<span data-ttu-id="6c5f4-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c5f4-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c5f4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5f4-155">CommonParameters</span></span>
<span data-ttu-id="6c5f4-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5f4-157">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5f4-158">輸入</span><span class="sxs-lookup"><span data-stu-id="6c5f4-158">INPUTS</span></span>

## <span data-ttu-id="6c5f4-159">輸出</span><span class="sxs-lookup"><span data-stu-id="6c5f4-159">OUTPUTS</span></span>

### <span data-ttu-id="6c5f4-160">IDeploymentResource （SpringCloud）。 Api20190501Preview。</span><span class="sxs-lookup"><span data-stu-id="6c5f4-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="6c5f4-161">筆記</span><span class="sxs-lookup"><span data-stu-id="6c5f4-161">NOTES</span></span>

<span data-ttu-id="6c5f4-162">別名</span><span class="sxs-lookup"><span data-stu-id="6c5f4-162">ALIASES</span></span>

## <span data-ttu-id="6c5f4-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c5f4-163">RELATED LINKS</span></span>
