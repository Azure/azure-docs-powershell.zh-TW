---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: de1f09fe6fd484345ebf4ebd7ae2a27d4640c694
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916700"
---
# <span data-ttu-id="4385d-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="4385d-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="4385d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4385d-102">SYNOPSIS</span></span>
<span data-ttu-id="4385d-103">建立新部署或更新即將離開的部署。</span><span class="sxs-lookup"><span data-stu-id="4385d-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="4385d-104">語法</span><span class="sxs-lookup"><span data-stu-id="4385d-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4385d-105">描述</span><span class="sxs-lookup"><span data-stu-id="4385d-105">DESCRIPTION</span></span>
<span data-ttu-id="4385d-106">建立新部署或更新即將離開的部署。</span><span class="sxs-lookup"><span data-stu-id="4385d-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="4385d-107">例子</span><span class="sxs-lookup"><span data-stu-id="4385d-107">EXAMPLES</span></span>

### <span data-ttu-id="4385d-108">範例 1：範例 1：建立春雲部署。</span><span class="sxs-lookup"><span data-stu-id="4385d-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
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

<span data-ttu-id="4385d-109">建立春假雲端部署。</span><span class="sxs-lookup"><span data-stu-id="4385d-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="4385d-110">參數</span><span class="sxs-lookup"><span data-stu-id="4385d-110">PARAMETERS</span></span>

### <span data-ttu-id="4385d-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="4385d-111">-AppName</span></span>
<span data-ttu-id="4385d-112">應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="4385d-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="4385d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4385d-113">-AsJob</span></span>
<span data-ttu-id="4385d-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="4385d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4385d-115">-Cpu</span><span class="sxs-lookup"><span data-stu-id="4385d-115">-Cpu</span></span>
<span data-ttu-id="4385d-116">必要的 CPU</span><span class="sxs-lookup"><span data-stu-id="4385d-116">Required CPU</span></span>

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

### <span data-ttu-id="4385d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4385d-117">-DefaultProfile</span></span>
<span data-ttu-id="4385d-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4385d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4385d-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="4385d-119">-EnvironmentVariable</span></span>
<span data-ttu-id="4385d-120">環境變數集合</span><span class="sxs-lookup"><span data-stu-id="4385d-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="4385d-121">-進一無二</span><span class="sxs-lookup"><span data-stu-id="4385d-121">-JvmOption</span></span>
<span data-ttu-id="4385d-122">PARAMETERM 參數</span><span class="sxs-lookup"><span data-stu-id="4385d-122">JVM parameter</span></span>

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

### <span data-ttu-id="4385d-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="4385d-123">-MemoryInGb</span></span>
<span data-ttu-id="4385d-124">所需的記憶體大小 ，以 GB 為單位</span><span class="sxs-lookup"><span data-stu-id="4385d-124">Required Memory size in GB</span></span>

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

### <span data-ttu-id="4385d-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="4385d-125">-Name</span></span>
<span data-ttu-id="4385d-126">部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="4385d-126">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="4385d-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4385d-127">-NoWait</span></span>
<span data-ttu-id="4385d-128">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="4385d-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4385d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4385d-129">-ResourceGroupName</span></span>
<span data-ttu-id="4385d-130">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4385d-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4385d-131">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="4385d-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4385d-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="4385d-132">-RuntimeVersion</span></span>
<span data-ttu-id="4385d-133">執行時間版本</span><span class="sxs-lookup"><span data-stu-id="4385d-133">Runtime version</span></span>

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

### <span data-ttu-id="4385d-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4385d-134">-ServiceName</span></span>
<span data-ttu-id="4385d-135">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="4385d-135">The name of the Service resource.</span></span>

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

### <span data-ttu-id="4385d-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="4385d-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="4385d-137">用於多模組專案部署之產品選取器。</span><span class="sxs-lookup"><span data-stu-id="4385d-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="4385d-138">這應該是目的模組/專案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="4385d-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="4385d-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="4385d-139">-SourceRelativePath</span></span>
<span data-ttu-id="4385d-140">儲存來源之儲存空間的相對路徑</span><span class="sxs-lookup"><span data-stu-id="4385d-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="4385d-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="4385d-141">-SourceType</span></span>
<span data-ttu-id="4385d-142">上傳的來源類型</span><span class="sxs-lookup"><span data-stu-id="4385d-142">Type of the source uploaded</span></span>

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

### <span data-ttu-id="4385d-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="4385d-143">-SourceVersion</span></span>
<span data-ttu-id="4385d-144">來源版本</span><span class="sxs-lookup"><span data-stu-id="4385d-144">Version of the source</span></span>

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

### <span data-ttu-id="4385d-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4385d-145">-SubscriptionId</span></span>
<span data-ttu-id="4385d-146">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="4385d-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4385d-147">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4385d-147">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4385d-148">-確認</span><span class="sxs-lookup"><span data-stu-id="4385d-148">-Confirm</span></span>
<span data-ttu-id="4385d-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4385d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4385d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4385d-150">-WhatIf</span></span>
<span data-ttu-id="4385d-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4385d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4385d-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4385d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4385d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4385d-153">CommonParameters</span></span>
<span data-ttu-id="4385d-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4385d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4385d-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4385d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4385d-156">輸入</span><span class="sxs-lookup"><span data-stu-id="4385d-156">INPUTS</span></span>

## <span data-ttu-id="4385d-157">輸出</span><span class="sxs-lookup"><span data-stu-id="4385d-157">OUTPUTS</span></span>

### <span data-ttu-id="4385d-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="4385d-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="4385d-159">筆記</span><span class="sxs-lookup"><span data-stu-id="4385d-159">NOTES</span></span>

<span data-ttu-id="4385d-160">別名</span><span class="sxs-lookup"><span data-stu-id="4385d-160">ALIASES</span></span>

## <span data-ttu-id="4385d-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="4385d-161">RELATED LINKS</span></span>

