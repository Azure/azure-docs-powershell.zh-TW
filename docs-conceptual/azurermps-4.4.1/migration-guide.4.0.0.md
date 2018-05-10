# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a><span data-ttu-id="9bb5e-101">Microsoft Azure PowerShell 4.0.0 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-101">Breaking changes for Microsoft Azure PowerShell 4.0.0</span></span>

<span data-ttu-id="9bb5e-102">本文件為 Microsoft Azure PowerShell Cmdlet 的客戶提供重大變更通知和移轉指南。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="9bb5e-103">每一節都會說明促成重大變更的原因和阻力最小的移轉路徑。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="9bb5e-104">如需深入了解內容，請參閱與每次變更相關聯的提取要求。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="9bb5e-105">目錄</span><span class="sxs-lookup"><span data-stu-id="9bb5e-105">Table of Contents</span></span>

- [<span data-ttu-id="9bb5e-106">Compute Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-106">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="9bb5e-107">EventHub Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-107">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="9bb5e-108">Insights Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-108">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="9bb5e-109">Network Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-109">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="9bb5e-110">ServiceBus Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-110">Breaking changes to ServiceBus cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)
- [<span data-ttu-id="9bb5e-111">Sql Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-111">Breaking changes to Sql cmdlets</span></span>](#breaking-changes-to-sql-cmdlets)
- [<span data-ttu-id="9bb5e-112">Storage Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-112">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
- [<span data-ttu-id="9bb5e-113">Profile Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-113">Breaking Changes to Profile Cmdlets</span></span>](#breaking-changes-to-profile-cmdlets)
## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="9bb5e-114">Compute Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-114">Breaking changes to Compute cmdlets</span></span>

<span data-ttu-id="9bb5e-115">受到此版本影響的輸出類型如下：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-115">The following output types were affected this release:</span></span>

### <a name="psvirtualmachine"></a><span data-ttu-id="9bb5e-116">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9bb5e-116">PSVirtualMachine</span></span>
- <span data-ttu-id="9bb5e-117">`PSVirtualMachine` 物件的最上層屬性 `DataDiskNames` 和 `NetworkInterfaceIDs` 已從輸出類型中移除。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-117">Top level properties `DataDiskNames` and `NetworkInterfaceIDs` of nthe `PSVirtualMachine` object have been removed from the output type.</span></span> <span data-ttu-id="9bb5e-118">這些屬性已一律可在 `PSVirtualMachine` 物件的 `StorageProfile` 和 `NetworkProfile` 屬性中使用，並需要繼續透過存取方式取得。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-118">These properties have always been available in the `StorageProfile` and `NetworkProfile` properties of the `PSVirtualMachine` object and will be the way they will need to be accessed going forward.</span></span>
- <span data-ttu-id="9bb5e-119">這項變更會影響下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-119">This change affects the following cmdlets:</span></span>
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="9bb5e-120">EventHub Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-120">Breaking changes to EventHub cmdlets</span></span>

<span data-ttu-id="9bb5e-121">受到此版本影響的 Cmdlet 如下：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-121">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="9bb5e-122">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="9bb5e-122">Get-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="9bb5e-123">`ResourceGroupName` 屬性已從輸出類型 `NamespaceAttributes` 中移除</span><span class="sxs-lookup"><span data-stu-id="9bb5e-123">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="9bb5e-124">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="9bb5e-124">New-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="9bb5e-125">`ResourceGroupName` 屬性已從輸出類型 `NamespaceAttributes` 中移除</span><span class="sxs-lookup"><span data-stu-id="9bb5e-125">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="9bb5e-126">Insights Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-126">Breaking changes to Insights cmdlets</span></span>

<span data-ttu-id="9bb5e-127">受到此版本影響的 Cmdlet 如下：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-127">The following cmdlets were affected this release:</span></span>
    
### <a name="get-azurermusage"></a><span data-ttu-id="9bb5e-128">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="9bb5e-128">Get-AzureRmUsage</span></span>
- <span data-ttu-id="9bb5e-129">此 Cmdlet 已受到取代。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-129">This cmdlet has been deprecated.</span></span>

### <a name="remove-azurermalertrule"></a><span data-ttu-id="9bb5e-130">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="9bb5e-130">Remove-AzureRmAlertRule</span></span>
- <span data-ttu-id="9bb5e-131">此 Cmdlet 的輸出已從具有單一物件的清單變更為單一物件，此物件包含 requestId 和狀態碼。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-131">The output of this cmdlet has changed from a list with a single object to a single object; this object includes the requestId, and status code.</span></span>
    
```powershell
# Old  
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
if ($s1 -ne $null)
{
    $r = $s1(0).RequestId
    $s = $s1(0).StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogalertrule"></a><span data-ttu-id="9bb5e-132">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="9bb5e-132">Add-AzureRmLogAlertRule</span></span>
- <span data-ttu-id="9bb5e-133">此 Cmdlet 已受到取代。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-133">This cmdlet has been deprecated.</span></span>
    
### <a name="get-azurermalertrule"></a><span data-ttu-id="9bb5e-134">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="9bb5e-134">Get-AzureRmAlertRule</span></span>
- <span data-ttu-id="9bb5e-135">此 Cmdlet 輸出 (物件清單) 的每個元素會經過壓平合併，也就是並非以 `{ Id, Location, Name, Tags, Properties }` 結構傳回物件，而是以 `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}` 結構傳回物件，該結構是 Azure Resource 的所有屬性和最上層 AlertRuleResource 的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-135">Each element of the the output (a list of objects) of this cmdlet is flattened, i.e. instead of returning objects with the structure `{ Id, Location, Name, Tags, Properties }` it will return objects with the structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, which is all of the attributes of an Azure Resource plus all of the attributes of an AlertRuleResource at the top level.</span></span>
    
```powershell
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
      
    Write-Host $rules(0).Id
    Write-Host $rules(0).Properties.IsEnabled
    Write-Host $rules(0).Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
 
    Write-Host $rules(0).Id
      
    # Properties will remain for a while
    Write-Host $rules(0).Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules(0).IsEnabled
    Write-Host $rules(0).Condition
}
```
    
### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="9bb5e-136">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9bb5e-136">Get-AzureRmAutoscaleSetting</span></span>
- <span data-ttu-id="9bb5e-137">`AutoscaleSettingResourceName` 欄位會受到取代，因為它一律與 `Name` 欄位有相同的值。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-137">The `AutoscaleSettingResourceName` field is deprecated since it always has the same value as the `Name` field.</span></span>

```powershell
# Old  
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# There won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```
    
### <a name="remove-azurermlogprofile"></a><span data-ttu-id="9bb5e-138">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="9bb5e-138">Remove-AzureRmLogProfile</span></span>
- <span data-ttu-id="9bb5e-139">此 Cmdlet 的輸出將會從 `Boolean` 變更為物件，其中包含 `RequestId` 和 `StatusCode`</span><span class="sxs-lookup"><span data-stu-id="9bb5e-139">The output of this cmdlet will change from `Boolean` to and object containing `RequestId` and `StatusCode`</span></span>

```powershell
# Old  
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
if ($s1 -eq $true)
{
    Write-Host "Removed"
}
else
{
    Write-Host "Failed"
}

# New
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogprofile"></a><span data-ttu-id="9bb5e-140">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="9bb5e-140">Add-AzureRmLogProfile</span></span>
- <span data-ttu-id="9bb5e-141">此 Cmdlet 的輸出會變更為包含 requestId、狀態碼和已更新或新建立資源的物件</span><span class="sxs-lookup"><span data-stu-id="9bb5e-141">The output of this cmdlet will change from an object that includes the requestId, status code, and the updated or newly created resource</span></span>
    
```powershell
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a><span data-ttu-id="9bb5e-142">Set-AzureRmDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="9bb5e-142">Set-AzureRmDiagnosticSettings</span></span>
- <span data-ttu-id="9bb5e-143">此命令將重新命名為 `Update-AzureRmDiagnsoticSettings`</span><span class="sxs-lookup"><span data-stu-id="9bb5e-143">The command is going to be renamed to `Update-AzureRmDiagnsoticSettings`</span></span>

```powershell
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="9bb5e-144">Network Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-144">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="9bb5e-145">受到此版本影響的 Cmdlet 如下：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-145">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermvirtualnetworkgatewayconnection"></a><span data-ttu-id="9bb5e-146">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9bb5e-146">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="9bb5e-147">`EnableBgp` 參數已變更為採用 `boolean`，而不是採用 `string`</span><span class="sxs-lookup"><span data-stu-id="9bb5e-147">`EnableBgp` parameter has been changed to take a `boolean` instead of a `string`</span></span>

```powershell
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="9bb5e-148">ServiceBus Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-148">Breaking changes to ServiceBus cmdlets</span></span>

<span data-ttu-id="9bb5e-149">受到此版本影響的 Cmdlet 如下：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-149">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermservicebusnamespace"></a><span data-ttu-id="9bb5e-150">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9bb5e-150">Get-AzureRmServiceBusNamespace</span></span>
- <span data-ttu-id="9bb5e-151">`ResourceGroupName` 屬性已從輸出類型 `NamespaceAttributes` 中移除</span><span class="sxs-lookup"><span data-stu-id="9bb5e-151">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermservicebusnamespace"></a><span data-ttu-id="9bb5e-152">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9bb5e-152">New-AzureRmServiceBusNamespace</span></span>

- <span data-ttu-id="9bb5e-153">`ResourceGroupName` 屬性已從輸出類型 `NamespaceAttributes` 中移除</span><span class="sxs-lookup"><span data-stu-id="9bb5e-153">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-sql-cmdlets"></a><span data-ttu-id="9bb5e-154">Sql Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-154">Breaking changes to Sql cmdlets</span></span>

<span data-ttu-id="9bb5e-155">受到此版本影響的 Cmdlet 如下：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-155">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermsqldatabasefailovergroup"></a><span data-ttu-id="9bb5e-156">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9bb5e-156">New-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="9bb5e-157">`Tag` 參數已移除</span><span class="sxs-lookup"><span data-stu-id="9bb5e-157">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="9bb5e-158">`GracePeriodWithDataLossHour` 參數已重新命名為 `GracePeriodWithDataLossHours`</span><span class="sxs-lookup"><span data-stu-id="9bb5e-158">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a><span data-ttu-id="9bb5e-159">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9bb5e-159">Set-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="9bb5e-160">`Tag` 參數已移除</span><span class="sxs-lookup"><span data-stu-id="9bb5e-160">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="9bb5e-161">`GracePeriodWithDataLossHour` 參數已重新命名為 `GracePeriodWithDataLossHours`</span><span class="sxs-lookup"><span data-stu-id="9bb5e-161">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a><span data-ttu-id="9bb5e-162">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9bb5e-162">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>
- <span data-ttu-id="9bb5e-163">`Tag` 參數已移除</span><span class="sxs-lookup"><span data-stu-id="9bb5e-163">`Tag` parameter has been removed</span></span>

```powershell
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a><span data-ttu-id="9bb5e-164">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9bb5e-164">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>
- <span data-ttu-id="9bb5e-165">`Tag` 參數已移除</span><span class="sxs-lookup"><span data-stu-id="9bb5e-165">`Tag` parameter has been removed</span></span>

```powershell
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a><span data-ttu-id="9bb5e-166">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9bb5e-166">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="9bb5e-167">`PartnerResourceGroupName` 參數已移除</span><span class="sxs-lookup"><span data-stu-id="9bb5e-167">`PartnerResourceGroupName` parameter has been removed</span></span>
- <span data-ttu-id="9bb5e-168">`PartnerServerName` 參數已移除</span><span class="sxs-lookup"><span data-stu-id="9bb5e-168">`PartnerServerName` parameter has been removed</span></span>

```powershell
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a><span data-ttu-id="9bb5e-169">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9bb5e-169">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>
- <span data-ttu-id="9bb5e-170">`Usage_Anomaly` 值已不再是 `ExcludedDetectionType` 參數的有效值</span><span class="sxs-lookup"><span data-stu-id="9bb5e-170">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a><span data-ttu-id="9bb5e-171">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9bb5e-171">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
- <span data-ttu-id="9bb5e-172">`Usage_Anomaly` 值已不再是 `ExcludedDetectionType` 參數的有效值</span><span class="sxs-lookup"><span data-stu-id="9bb5e-172">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="9bb5e-173">Storage Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-173">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="9bb5e-174">受到此版本影響的輸出類型參數如下：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-174">The following output type properties were affected this release:</span></span>

### <a name="azurestorageblobicloudblobserviceclient"></a><span data-ttu-id="9bb5e-175">AzureStorageBlob.ICloudBlob.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="9bb5e-175">AzureStorageBlob.ICloudBlob.ServiceClient</span></span>
- <span data-ttu-id="9bb5e-176">下列屬性已從此類型中移除 (_注意_：這些屬性還是可以在 `DefaultRequestOptions` 屬性中找到):</span><span class="sxs-lookup"><span data-stu-id="9bb5e-176">The following properties were removed from this type (_note_: they can still be found in `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="9bb5e-177">這項變更會影響下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-177">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a><span data-ttu-id="9bb5e-178">AzureStorageContainer.CloudBlobContainer.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="9bb5e-178">AzureStorageContainer.CloudBlobContainer.ServiceClient</span></span>
- <span data-ttu-id="9bb5e-179">下列屬性已從此類型中移除 (_注意_：這些屬性還是可以在 `DefaultRequestOptions` 屬性中找到)：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-179">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="9bb5e-180">這項變更會影響下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-180">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a><span data-ttu-id="9bb5e-181">AzureStorageQueue.CloudQueue.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="9bb5e-181">AzureStorageQueue.CloudQueue.ServiceClient</span></span>
- <span data-ttu-id="9bb5e-182">下列屬性已從此類型中移除 (_注意_：這些屬性還是可以在 `DefaultRequestOptions` 屬性中找到)：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-182">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="9bb5e-183">這項變更會影響下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-183">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a><span data-ttu-id="9bb5e-184">AzureStorageTable.CloudTable.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="9bb5e-184">AzureStorageTable.CloudTable.ServiceClient</span></span>
- <span data-ttu-id="9bb5e-185">下列屬性已從此類型中移除 (_注意_：這些屬性還是可以在 `DefaultRequestOptions` 屬性中找到)：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-185">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="9bb5e-186">這項變更會影響下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9bb5e-186">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell
# Old
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.LocationMode       
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.RetryPolicy

# New
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.DefaultRequestOptions.LocationMode     
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.DefaultRequestOptions.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.DefaultRequestOptions.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.DefaultRequestOptions.RetryPolicy
```

## <a name="breaking-changes-to-profile-cmdlets"></a><span data-ttu-id="9bb5e-187">Profile Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-187">Breaking Changes to Profile Cmdlets</span></span>

<span data-ttu-id="9bb5e-188">下列 Cmdlet 與 Cmdlet 輸出類型已在此版本中變更。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-188">The following cmdlets and cmdlet output types were changed in this release.</span></span>

### <a name="add-azurermaccount-breaking-changes"></a><span data-ttu-id="9bb5e-189">Add-AzureRmAccount 重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-189">Add-AzureRmAccount breaking changes</span></span>

- <span data-ttu-id="9bb5e-190">```EnvironmentName``` 已移除，並以 ```Environment``` 加以取代，```Environment``` 現在會採用字串，而不是採用 ```AzureEnvironment``` 物件</span><span class="sxs-lookup"><span data-stu-id="9bb5e-190">```EnvironmentName``` parameter has been removed and replaced with ```Environment```, the ```Environment``` now takes a string and not an ```AzureEnvironment``` object</span></span>

```powershell
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a><span data-ttu-id="9bb5e-191">Select-AzureRmProfile 已重新命名為 Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="9bb5e-191">Select-AzureRmProfile was renamed to Import-AzureRmContext</span></span>

<span data-ttu-id="9bb5e-192">```Select-AzureRmProfile``` 已重新命名為 ```Import-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="9bb5e-192">```Select-AzureRmProfile``` was renamed to ```Import-AzureRmContext```</span></span>

```powershell
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a><span data-ttu-id="9bb5e-193">Save-AzureRmProfile 已重新命名為 Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="9bb5e-193">Save-AzureRmProfile was renamed to Save-AzureRmContext</span></span>

<span data-ttu-id="9bb5e-194">```Save-AzureRmProfile``` 已重新命名為 ```Save-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="9bb5e-194">```Save-AzureRmProfile``` was renamed to ```Save-AzureRmContext```</span></span>

```powershell
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a><span data-ttu-id="9bb5e-195">PSAzureContext 類型輸出的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-195">Breaking Changes to output PSAzureContext Type</span></span>

- <span data-ttu-id="9bb5e-196">```TokenCache``` 屬性已變更為實作 ```IAzureTokenCache``` 的類型，而不是實作 ```byte[]``` 的類型</span><span class="sxs-lookup"><span data-stu-id="9bb5e-196">The ```TokenCache``` property changed to a type that implements ```IAzureTokenCache``` instead of a ```byte[]```</span></span>

```powershell
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a><span data-ttu-id="9bb5e-197">PSAzureAccount 類型輸出的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-197">Breaking Changes to the output PSAzureAccount Type</span></span>

- <span data-ttu-id="9bb5e-198">```AccountType``` 屬性已變更為 ```Type```</span><span class="sxs-lookup"><span data-stu-id="9bb5e-198">The ```AccountType``` property was changed to ```Type```</span></span>

```powershell
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a><span data-ttu-id="9bb5e-199">PSAzureSubscription 類型輸出的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-199">Breaking Changes to the output PSAzureSubscription Type</span></span>
- <span data-ttu-id="9bb5e-200">```SubscriptionId``` 屬性已變更為 ```Id```</span><span class="sxs-lookup"><span data-stu-id="9bb5e-200">The ```SubscriptionId``` property was changed to ```Id```</span></span>

```powershell
# Old
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId

# New
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
```

- <span data-ttu-id="9bb5e-201">```SubscriptionName``` 屬性已變更為 ```Name```</span><span class="sxs-lookup"><span data-stu-id="9bb5e-201">The ```SubscriptionName``` property was changed to ```Name```</span></span>

```powershell
# Old
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionName
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionName
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName

# New
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Name
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Name
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
```

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a><span data-ttu-id="9bb5e-202">PSAzureTenant 類型輸出的重大變更</span><span class="sxs-lookup"><span data-stu-id="9bb5e-202">Breaking Changes to the output PSAzureTenant Type</span></span>

- <span data-ttu-id="9bb5e-203">```TenantId``` 屬性已變更為 ```Id```</span><span class="sxs-lookup"><span data-stu-id="9bb5e-203">The ```TenantId``` property was changed to ```Id```</span></span>

```powershell
# Old
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).TenantId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.TenantId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId

# New
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
```

- <span data-ttu-id="9bb5e-204">```Domain``` 屬性已變更為 ```Directory```</span><span class="sxs-lookup"><span data-stu-id="9bb5e-204">The ```Domain``` property was changed to ```Directory```</span></span>

```powershell
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
