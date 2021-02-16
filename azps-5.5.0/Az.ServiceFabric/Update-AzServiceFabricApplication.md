---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: e53ed405c9a03e7a9ec7a7c3694a44d513a1a1ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133555"
---
# <span data-ttu-id="c140a-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c140a-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="c140a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c140a-102">SYNOPSIS</span></span>
<span data-ttu-id="c140a-103">更新服務結構應用程式。</span><span class="sxs-lookup"><span data-stu-id="c140a-103">Update a service fabric application.</span></span> <span data-ttu-id="c140a-104">這可讓您更新應用程式參數和/或升級應用程式類型版本，這將會觸發應用程式升級。</span><span class="sxs-lookup"><span data-stu-id="c140a-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span> <span data-ttu-id="c140a-105">僅支援 ARM 部署的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c140a-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="c140a-106">句法</span><span class="sxs-lookup"><span data-stu-id="c140a-106">SYNTAX</span></span>

### <span data-ttu-id="c140a-107">ByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="c140a-107">ByResourceGroup (Default)</span></span>
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

### <span data-ttu-id="c140a-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c140a-108">ByResourceId</span></span>
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

### <span data-ttu-id="c140a-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c140a-109">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c140a-110">說明</span><span class="sxs-lookup"><span data-stu-id="c140a-110">DESCRIPTION</span></span>
<span data-ttu-id="c140a-111">這個 Cmdlet 可用來更新應用程式參數，並升級應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="c140a-111">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="c140a-112">更新參數只會在 ARM 端變更模型，只要使用新的類型版本，命令就會觸發應用程式升級。</span><span class="sxs-lookup"><span data-stu-id="c140a-112">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="c140a-113">指定的類型版本應該已經在群集中使用 **新的-AzServiceFabricApplicationTypeVersion** 建立。</span><span class="sxs-lookup"><span data-stu-id="c140a-113">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="c140a-114">示例</span><span class="sxs-lookup"><span data-stu-id="c140a-114">EXAMPLES</span></span>

### <span data-ttu-id="c140a-115">範例1</span><span class="sxs-lookup"><span data-stu-id="c140a-115">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="c140a-116">這個範例會啟動應用程式升級，以將類型版本更新為使用 **新的 AzServiceFabricApplicationTypeVersion** 建立的 "v2"。</span><span class="sxs-lookup"><span data-stu-id="c140a-116">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="c140a-117">所使用的應用程式參數應該在應用程式資訊清單中定義。</span><span class="sxs-lookup"><span data-stu-id="c140a-117">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="c140a-118">範例2</span><span class="sxs-lookup"><span data-stu-id="c140a-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="c140a-119">這個範例會更新應用程式的最小和最大節點限制數。</span><span class="sxs-lookup"><span data-stu-id="c140a-119">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="c140a-120">範例3</span><span class="sxs-lookup"><span data-stu-id="c140a-120">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="c140a-121">這個範例會啟動應用程式升級，以將類型版本更新為 "v2"，同時也會設定從目前升級生效的一些升級原則參數。</span><span class="sxs-lookup"><span data-stu-id="c140a-121">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="c140a-122">範例4</span><span class="sxs-lookup"><span data-stu-id="c140a-122">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="c140a-123">這個範例會更新應用程式參數，但只有在下一次升級到應用程式版本之後，才會生效這些變更。</span><span class="sxs-lookup"><span data-stu-id="c140a-123">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="c140a-124">參數</span><span class="sxs-lookup"><span data-stu-id="c140a-124">PARAMETERS</span></span>

### <span data-ttu-id="c140a-125">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="c140a-125">-ApplicationParameter</span></span>
<span data-ttu-id="c140a-126">將應用程式參數指定為鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="c140a-126">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="c140a-127">這些參數必須存在於應用程式資訊清單中。</span><span class="sxs-lookup"><span data-stu-id="c140a-127">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="c140a-128">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c140a-128">-ApplicationTypeVersion</span></span>
<span data-ttu-id="c140a-129">指定應用程式類型版本</span><span class="sxs-lookup"><span data-stu-id="c140a-129">Specify the application type version</span></span>

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

### <span data-ttu-id="c140a-130">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c140a-130">-ClusterName</span></span>
<span data-ttu-id="c140a-131">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="c140a-131">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c140a-132">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="c140a-132">-ConsiderWarningAsError</span></span>
<span data-ttu-id="c140a-133">指出是否要在健康評估期間將警告健康情況事件視為錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="c140a-133">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

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

### <span data-ttu-id="c140a-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c140a-134">-DefaultProfile</span></span>
<span data-ttu-id="c140a-135">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c140a-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c140a-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="c140a-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="c140a-137">指定要用於受監視升級之預設服務類型的健康原則所允許的每個服務的 unhelthy 分區最大百分比。</span><span class="sxs-lookup"><span data-stu-id="c140a-137">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="c140a-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="c140a-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="c140a-139">指定要用於受監視升級之預設服務類型的健康原則所允許的每個服務的 unhelthy 副本最大百分比。</span><span class="sxs-lookup"><span data-stu-id="c140a-139">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="c140a-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="c140a-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="c140a-141">指定要用於受監視升級之預設服務類型的健康原則所允許的最大 unhelthy 服務百分比。</span><span class="sxs-lookup"><span data-stu-id="c140a-141">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="c140a-142">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="c140a-142">-FailureAction</span></span>
<span data-ttu-id="c140a-143">指定受監視升級失敗時要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="c140a-143">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="c140a-144">此參數可接受的值為 [復原] 或 [手動]。</span><span class="sxs-lookup"><span data-stu-id="c140a-144">The acceptable values for this parameter are Rollback or Manual.</span></span>

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

### <span data-ttu-id="c140a-145">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="c140a-145">-ForceRestart</span></span>
<span data-ttu-id="c140a-146">表示服務主機會重新開機，即使升級是僅限設定的變更。</span><span class="sxs-lookup"><span data-stu-id="c140a-146">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

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

### <span data-ttu-id="c140a-147">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="c140a-147">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="c140a-148">指定當前一個健康情況檢查失敗時，服務結構會自動重試健康情況檢查之後的持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c140a-148">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

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

### <span data-ttu-id="c140a-149">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="c140a-149">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="c140a-150">指定服務結構等待的持續時間（以秒為單位），以便在移至下一個升級網域或完成升級前，確認應用程式是否穩定。</span><span class="sxs-lookup"><span data-stu-id="c140a-150">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="c140a-151">在執行狀況檢查之後，此等待持續時間可避免健康情況的未檢測變更。</span><span class="sxs-lookup"><span data-stu-id="c140a-151">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

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

### <span data-ttu-id="c140a-152">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="c140a-152">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="c140a-153">指定服務結構在完成升級網域升級後，執行初始健康情況檢查之前的持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c140a-153">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

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

### <span data-ttu-id="c140a-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c140a-154">-InputObject</span></span>
<span data-ttu-id="c140a-155">應用程式資源。</span><span class="sxs-lookup"><span data-stu-id="c140a-155">The application resource.</span></span>

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

### <span data-ttu-id="c140a-156">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="c140a-156">-MaximumNodeCount</span></span>
<span data-ttu-id="c140a-157">指定要放置應用程式的最大節點數</span><span class="sxs-lookup"><span data-stu-id="c140a-157">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="c140a-158">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="c140a-158">-MinimumNodeCount</span></span>
<span data-ttu-id="c140a-159">指定服務結構將針對此應用程式保留容量的最小節點數</span><span class="sxs-lookup"><span data-stu-id="c140a-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="c140a-160">-名稱</span><span class="sxs-lookup"><span data-stu-id="c140a-160">-Name</span></span>
<span data-ttu-id="c140a-161">指定應用程式的名稱</span><span class="sxs-lookup"><span data-stu-id="c140a-161">Specify the name of the application</span></span>

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

### <span data-ttu-id="c140a-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c140a-162">-ResourceGroupName</span></span>
<span data-ttu-id="c140a-163">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c140a-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c140a-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c140a-164">-ResourceId</span></span>
<span data-ttu-id="c140a-165">應用程式的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="c140a-165">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="c140a-166">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="c140a-166">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="c140a-167">以下列格式，指定要用於不同服務類型的健康原則對應為雜湊資料表： @ {"ServiceTypeName"： "MaxPercentUnhealthyPartitionsPerService，MaxPercentUnhealthyReplicasPerPartition，MaxPercentUnhealthyServices"}。</span><span class="sxs-lookup"><span data-stu-id="c140a-167">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="c140a-168">例如： @ {"ServiceTypeName01" = "5，10，5";"ServiceTypeName02" = "5，5，5"}</span><span class="sxs-lookup"><span data-stu-id="c140a-168">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

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

### <span data-ttu-id="c140a-169">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="c140a-169">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="c140a-170">指定在群集的 [應用程式健康狀態] 發生錯誤前，在叢集節點上部署之應用程式實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="c140a-170">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

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

### <span data-ttu-id="c140a-171">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="c140a-171">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="c140a-172">指定 Service Fabric 升級單一升級網域所需的最長時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c140a-172">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="c140a-173">此期間之後，升級就會失敗。</span><span class="sxs-lookup"><span data-stu-id="c140a-173">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="c140a-174">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="c140a-174">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="c140a-175">指定服務結構在服務結構繼續進行升級前，等待服務重新設定為安全狀態的最長時間（若尚未處於安全狀態）。</span><span class="sxs-lookup"><span data-stu-id="c140a-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

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

### <span data-ttu-id="c140a-176">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="c140a-176">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="c140a-177">指定服務結構在整個升級時所需的最長時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c140a-177">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="c140a-178">此期間之後，升級就會失敗。</span><span class="sxs-lookup"><span data-stu-id="c140a-178">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="c140a-179">-確認</span><span class="sxs-lookup"><span data-stu-id="c140a-179">-Confirm</span></span>
<span data-ttu-id="c140a-180">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c140a-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c140a-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c140a-181">-WhatIf</span></span>
<span data-ttu-id="c140a-182">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c140a-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c140a-183">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c140a-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c140a-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c140a-184">CommonParameters</span></span>
<span data-ttu-id="c140a-185">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c140a-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c140a-186">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c140a-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c140a-187">輸入</span><span class="sxs-lookup"><span data-stu-id="c140a-187">INPUTS</span></span>

### <span data-ttu-id="c140a-188">System.object</span><span class="sxs-lookup"><span data-stu-id="c140a-188">System.String</span></span>

### <span data-ttu-id="c140a-189">PSApplication 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="c140a-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="c140a-190">輸出</span><span class="sxs-lookup"><span data-stu-id="c140a-190">OUTPUTS</span></span>

### <span data-ttu-id="c140a-191">PSApplication 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="c140a-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="c140a-192">筆記</span><span class="sxs-lookup"><span data-stu-id="c140a-192">NOTES</span></span>

## <span data-ttu-id="c140a-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="c140a-193">RELATED LINKS</span></span>
