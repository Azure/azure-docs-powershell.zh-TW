# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a>Microsoft Azure PowerShell 3.0.0 的重大變更。

本文件為 Microsoft Azure PowerShell Cmdlet 的客戶提供重大變更通知和移轉指南。  每一節都會說明促成重大變更的原因和阻力最小的移轉路徑。  如需深入了解內容，請參閱與每次變更相關聯的提取要求。

## <a name="table-of-contents"></a>目錄
1. [Data Lake Store Cmdlet 的重大變更](#breaking-changes-to-data-lake-store-cmdlets)
2. [ApiManagement Cmdlet 的重大變更](#breaking-changes-to-apimanagement-cmdlets)
3. [Network Cmdlet 的重大變更](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a>Data Lake Store Cmdlet 的重大變更

受到此版本 ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)) 影響的 Cmdlet 如下：

**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**
- 此 Cmdlet 已移除，並以 ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)`` 加以取代。
- 舊的 Cmdlet 會傳回代表存取控制清單 (ACL) 的複雜物件。 新的 Cmdlet 會傳回所選路徑 ACL 中的簡易項目清單。

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**
- 此 Cmdlet 會取代舊的 ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)`` Cmdlet。
- 這個新的 Cmdlet 會傳回所選路徑 ACL 中的簡易項目清單 (類型為 ``DataLakeStoreItemAce[]``)。
- 此 Cmdlet 的輸出可以傳遞至下列 Cmdlet 的 ``-Acl`` 參數中：
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**、**Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)****Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**
- 這些 Cmdlet 現在會接受 ``-Acl`` 參數的 ``DataLakeStoreItemAce[]``。
- ``DataLakeStoreItemAce[]`` 會由 ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)`` 傳回。

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>ApiManagement Cmdlet 的重大變更

受到此版本 ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)) 影響的 Cmdlet 如下：

**New-AzureRmApiManagementVirtualNetwork**
- 參考虛擬網路的必要參數從要求 SubnetName 和 SubnetResourceId 變更為 VnetId (格式為 ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``)

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

**取代 Set-AzureRmApiManagementVirtualNetworks Cmdlet**
- 此 Cmdlet 將受到取代，因為有多個方法可用來設定與 ApiManagement 部署相關聯的虛擬網路。

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a>Network Cmdlet 的重大變更

受到此版本 ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)) 影響的 Cmdlet 如下：

**New-AzureRmVirtualNetworkGateway**
- 已移除變更內容的描述 ``:- Bool parameter:-ActiveActive``，並新增 ``SwitchParameter:-EnableActiveActiveFeature``，以啟用新建虛擬網路閘道上的 Active-Active 功能。

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

Set-AzureRmVirtualNetworkGateway
- 已移除變更內容的描述 ``:- Bool parameter:-ActiveActive``，並新增 2 個 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature``，以啟用和停用虛擬網路閘道上的 Active-Active 功能。

```powershell
# Old
# Sample of how the cmdlet was previously called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $true
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $false  

# New
# Sample of how the cmdlet should now be called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -EnableActiveActiveFeature
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -DisableActiveActiveFeature
```