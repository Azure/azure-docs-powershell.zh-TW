---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: febf0ecb24be1b419353142805c9f91e0c771de5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902826"
---
# <span data-ttu-id="8ebac-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8ebac-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="8ebac-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8ebac-102">SYNOPSIS</span></span>
<span data-ttu-id="8ebac-103">更新服務結構應用程式。</span><span class="sxs-lookup"><span data-stu-id="8ebac-103">Update a service fabric application.</span></span> <span data-ttu-id="8ebac-104">這可讓您更新應用程式參數和/或升級應用程式類型版本，以觸發應用程式升級。</span><span class="sxs-lookup"><span data-stu-id="8ebac-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span> <span data-ttu-id="8ebac-105">僅支援 ARM 部署的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8ebac-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="8ebac-106">語法</span><span class="sxs-lookup"><span data-stu-id="8ebac-106">SYNTAX</span></span>

### <span data-ttu-id="8ebac-107">ByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="8ebac-107">ByResourceGroup (Default)</span></span>
```
Update-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-ForceRestart] [-UpgradeReplicaSetCheckTimeoutSec <Int32>]
 [-FailureAction <FailureAction>] [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ebac-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8ebac-108">ByResourceId</span></span>
```
Update-AzServiceFabricApplication [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>]
 [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-ForceRestart]
 [-UpgradeReplicaSetCheckTimeoutSec <Int32>] [-FailureAction <FailureAction>]
 [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ebac-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8ebac-109">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ebac-110">描述</span><span class="sxs-lookup"><span data-stu-id="8ebac-110">DESCRIPTION</span></span>
<span data-ttu-id="8ebac-111">此 Cmdlet 可用來更新應用程式參數，並升級應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="8ebac-111">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="8ebac-112">更新參數只會變更 ARM 端中的模型，只有在使用新類型版本時，該命令會觸發應用程式升級。</span><span class="sxs-lookup"><span data-stu-id="8ebac-112">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="8ebac-113">指定的類型版本應該已在使用 **New-AzServiceFabricApplicationTypeVersion** 的組集中建立。</span><span class="sxs-lookup"><span data-stu-id="8ebac-113">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="8ebac-114">例子</span><span class="sxs-lookup"><span data-stu-id="8ebac-114">EXAMPLES</span></span>

### <span data-ttu-id="8ebac-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="8ebac-115">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="8ebac-116">此範例會啟動應用程式升級，將類型版本更新為使用 **New-AzServiceFabricApplicationTypeVersion** 所建立之"v2"。</span><span class="sxs-lookup"><span data-stu-id="8ebac-116">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="8ebac-117">使用的應用程式參數應在應用程式清單中定義。</span><span class="sxs-lookup"><span data-stu-id="8ebac-117">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="8ebac-118">範例 2</span><span class="sxs-lookup"><span data-stu-id="8ebac-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="8ebac-119">此範例會更新應用程式的節點限制最小和最大數目。</span><span class="sxs-lookup"><span data-stu-id="8ebac-119">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="8ebac-120">範例 3</span><span class="sxs-lookup"><span data-stu-id="8ebac-120">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="8ebac-121">此範例會啟動應用程式升級，將類型版本更新為"v2"，並設定一些升級政策參數，這些參數會從目前的升級生效。</span><span class="sxs-lookup"><span data-stu-id="8ebac-121">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="8ebac-122">範例 4</span><span class="sxs-lookup"><span data-stu-id="8ebac-122">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="8ebac-123">此範例會更新應用程式參數，但只有在下一版升級至應用程式之前，這些變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="8ebac-123">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="8ebac-124">參數</span><span class="sxs-lookup"><span data-stu-id="8ebac-124">PARAMETERS</span></span>

### <span data-ttu-id="8ebac-125">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="8ebac-125">-ApplicationParameter</span></span>
<span data-ttu-id="8ebac-126">將應用程式參數指定為金鑰/值組。</span><span class="sxs-lookup"><span data-stu-id="8ebac-126">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="8ebac-127">這些參數必須存在於應用程式清單中。</span><span class="sxs-lookup"><span data-stu-id="8ebac-127">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-128">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8ebac-128">-ApplicationTypeVersion</span></span>
<span data-ttu-id="8ebac-129">指定應用程式類型版本</span><span class="sxs-lookup"><span data-stu-id="8ebac-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-130">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8ebac-130">-ClusterName</span></span>
<span data-ttu-id="8ebac-131">指定組名。</span><span class="sxs-lookup"><span data-stu-id="8ebac-131">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-132">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="8ebac-132">-ConsiderWarningAsError</span></span>
<span data-ttu-id="8ebac-133">指出是否要在健康狀態評估期間將警告健康狀態事件視為錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="8ebac-133">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ebac-134">-DefaultProfile</span></span>
<span data-ttu-id="8ebac-135">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ebac-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="8ebac-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="8ebac-137">指定每個服務健康情況政策所允許的無説明分割百分比上限，以用於受監控升級的預設服務類型。</span><span class="sxs-lookup"><span data-stu-id="8ebac-137">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="8ebac-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="8ebac-139">指定每個服務健康情況政策所允許的無説明複本百分比上限，以用於受監控升級的預設服務類型。</span><span class="sxs-lookup"><span data-stu-id="8ebac-139">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="8ebac-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="8ebac-141">指定健康情況政策所允許的未説明服務的最大百分比，以用於受監控升級的預設服務類型。</span><span class="sxs-lookup"><span data-stu-id="8ebac-141">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-142">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="8ebac-142">-FailureAction</span></span>
<span data-ttu-id="8ebac-143">指定受監控升級失敗時要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="8ebac-143">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="8ebac-144">此參數可接受的值為回收或手動。</span><span class="sxs-lookup"><span data-stu-id="8ebac-144">The acceptable values for this parameter are Rollback or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.FailureAction
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:
Accepted values: Rollback, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-145">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="8ebac-145">-ForceRestart</span></span>
<span data-ttu-id="8ebac-146">表示即使升級為只進行組配置的變更，服務主機也重新開機。</span><span class="sxs-lookup"><span data-stu-id="8ebac-146">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-147">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="8ebac-147">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="8ebac-148">指定工期 ，以碼錶示，如果先前的健康情況檢查失敗，服務布會在此之後重試健康情況檢查。</span><span class="sxs-lookup"><span data-stu-id="8ebac-148">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-149">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="8ebac-149">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="8ebac-150">指定 Service Fabric 等待的持續時間 ，以秒為秒，以確認應用程式是否穩定，再移往下一個升級網域或完成升級。</span><span class="sxs-lookup"><span data-stu-id="8ebac-150">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="8ebac-151">此等待持續時間可防止在執行健康情況檢查之後，未發現健康情況變更。</span><span class="sxs-lookup"><span data-stu-id="8ebac-151">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-152">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="8ebac-152">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="8ebac-153">指定 Service Fabric 在升級網域上完成升級後，先執行初始健康狀態檢查的工期 ，以秒為秒。</span><span class="sxs-lookup"><span data-stu-id="8ebac-153">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ebac-154">-InputObject</span></span>
<span data-ttu-id="8ebac-155">應用程式資源。</span><span class="sxs-lookup"><span data-stu-id="8ebac-155">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-156">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="8ebac-156">-MaximumNodeCount</span></span>
<span data-ttu-id="8ebac-157">指定要放置應用程式的節點數目上限</span><span class="sxs-lookup"><span data-stu-id="8ebac-157">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-158">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="8ebac-158">-MinimumNodeCount</span></span>
<span data-ttu-id="8ebac-159">指定 Service 準備此應用程式容量的節點數目</span><span class="sxs-lookup"><span data-stu-id="8ebac-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-160">-名稱</span><span class="sxs-lookup"><span data-stu-id="8ebac-160">-Name</span></span>
<span data-ttu-id="8ebac-161">指定應用程式的名稱</span><span class="sxs-lookup"><span data-stu-id="8ebac-161">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ebac-162">-ResourceGroupName</span></span>
<span data-ttu-id="8ebac-163">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ebac-163">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ebac-164">-ResourceId</span></span>
<span data-ttu-id="8ebac-165">應用程式的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="8ebac-165">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-166">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="8ebac-166">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="8ebac-167">指定健康情況政策的地圖，以下列格式做為雜湊表格，做為不同的服務類型：@ {"ServiceTypeName" ：" "MaxPercentUnhealthyPartitionsPerService，MaxPercentUnhealthyReplicasPerPartition，MaxPercentUnhealthyServices"}。</span><span class="sxs-lookup"><span data-stu-id="8ebac-167">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="8ebac-168">例如：@{ "ServiceTypeName01" = "5，10，5";"ServiceTypeName02" = "5，5，5" }</span><span class="sxs-lookup"><span data-stu-id="8ebac-168">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-169">-不健康DeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="8ebac-169">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="8ebac-170">指定在組群的應用程式健康情況狀態發生錯誤之前，部署在組群節點上之應用程式實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="8ebac-170">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-171">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="8ebac-171">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="8ebac-172">指定服務結構升級單一升級網域所花的時間上限 ，以秒為秒。</span><span class="sxs-lookup"><span data-stu-id="8ebac-172">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="8ebac-173">過了此期間之後，升級會失敗。</span><span class="sxs-lookup"><span data-stu-id="8ebac-173">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-174">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="8ebac-174">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="8ebac-175">指定 Service Fabric 等待服務重新設置至安全狀態的時間上限 ，如果尚未進入安全狀態，則服務結構會繼續進行升級。</span><span class="sxs-lookup"><span data-stu-id="8ebac-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-176">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="8ebac-176">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="8ebac-177">指定 Service Fabric 在整個升級期間所花的時間上限 ，以秒為秒。</span><span class="sxs-lookup"><span data-stu-id="8ebac-177">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="8ebac-178">過了此期間之後，升級會失敗。</span><span class="sxs-lookup"><span data-stu-id="8ebac-178">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebac-179">-確認</span><span class="sxs-lookup"><span data-stu-id="8ebac-179">-Confirm</span></span>
<span data-ttu-id="8ebac-180">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8ebac-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ebac-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ebac-181">-WhatIf</span></span>
<span data-ttu-id="8ebac-182">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ebac-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ebac-183">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ebac-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ebac-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ebac-184">CommonParameters</span></span>
<span data-ttu-id="8ebac-185">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8ebac-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ebac-186">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ebac-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ebac-187">輸入</span><span class="sxs-lookup"><span data-stu-id="8ebac-187">INPUTS</span></span>

### <span data-ttu-id="8ebac-188">System.String</span><span class="sxs-lookup"><span data-stu-id="8ebac-188">System.String</span></span>

### <span data-ttu-id="8ebac-189">Microsoft.Azure.Commands.ServiceFabric.models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="8ebac-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="8ebac-190">輸出</span><span class="sxs-lookup"><span data-stu-id="8ebac-190">OUTPUTS</span></span>

### <span data-ttu-id="8ebac-191">Microsoft.Azure.Commands.ServiceFabric.models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="8ebac-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="8ebac-192">筆記</span><span class="sxs-lookup"><span data-stu-id="8ebac-192">NOTES</span></span>

## <span data-ttu-id="8ebac-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ebac-193">RELATED LINKS</span></span>
