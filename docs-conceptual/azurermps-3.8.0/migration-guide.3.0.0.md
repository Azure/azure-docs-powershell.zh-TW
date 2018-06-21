# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a><span data-ttu-id="d15b8-101">Microsoft Azure PowerShell 3.0.0 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="d15b8-101">Breaking changes for Microsoft Azure PowerShell 3.0.0.</span></span>

<span data-ttu-id="d15b8-102">本文件為 Microsoft Azure PowerShell Cmdlet 的客戶提供重大變更通知和移轉指南。</span><span class="sxs-lookup"><span data-stu-id="d15b8-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="d15b8-103">每一節都會說明促成重大變更的原因和阻力最小的移轉路徑。</span><span class="sxs-lookup"><span data-stu-id="d15b8-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span>  <span data-ttu-id="d15b8-104">如需深入了解內容，請參閱與每次變更相關聯的提取要求。</span><span class="sxs-lookup"><span data-stu-id="d15b8-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="d15b8-105">目錄</span><span class="sxs-lookup"><span data-stu-id="d15b8-105">Table of Contents</span></span>
1. [<span data-ttu-id="d15b8-106">Data Lake Store Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="d15b8-106">Breaking changes to Data Lake Store cmdlets</span></span>](#breaking-changes-to-data-lake-store-cmdlets)
2. [<span data-ttu-id="d15b8-107">ApiManagement Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="d15b8-107">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
3. [<span data-ttu-id="d15b8-108">Network Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="d15b8-108">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a><span data-ttu-id="d15b8-109">Data Lake Store Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="d15b8-109">Breaking changes to Data Lake Store cmdlets</span></span>

<span data-ttu-id="d15b8-110">受到此版本 ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)) 影響的 Cmdlet 如下：</span><span class="sxs-lookup"><span data-stu-id="d15b8-110">The following cmdlets were affected this release ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span></span>

<span data-ttu-id="d15b8-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span><span class="sxs-lookup"><span data-stu-id="d15b8-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span></span>
- <span data-ttu-id="d15b8-112">此 Cmdlet 已移除，並以 ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)`` 加以取代。</span><span class="sxs-lookup"><span data-stu-id="d15b8-112">This cmdlet was removed and replaced with ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>
- <span data-ttu-id="d15b8-113">舊的 Cmdlet 會傳回代表存取控制清單 (ACL) 的複雜物件。</span><span class="sxs-lookup"><span data-stu-id="d15b8-113">The old cmdlet returned a complex object representing the access control list (ACL).</span></span> <span data-ttu-id="d15b8-114">新的 Cmdlet 會傳回所選路徑 ACL 中的簡易項目清單。</span><span class="sxs-lookup"><span data-stu-id="d15b8-114">The new cmdlet returns a simple list of entries in the chosen path's ACL.</span></span>

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="d15b8-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="d15b8-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="d15b8-116">此 Cmdlet 會取代舊的 ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)`` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d15b8-116">This cmdlet replaces the old cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span></span>
- <span data-ttu-id="d15b8-117">這個新的 Cmdlet 會傳回所選路徑 ACL 中的簡易項目清單 (類型為 ``DataLakeStoreItemAce[]``)。</span><span class="sxs-lookup"><span data-stu-id="d15b8-117">This new cmdlet returns a simple list of entries in the chosen path's ACL, with type ``DataLakeStoreItemAce[]``.</span></span>
- <span data-ttu-id="d15b8-118">此 Cmdlet 的輸出可以傳遞至下列 Cmdlet 的 ``-Acl`` 參數中：</span><span class="sxs-lookup"><span data-stu-id="d15b8-118">The output of this cmdlet can be passed in to the ``-Acl`` parameter of the following cmdlets:</span></span>
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="d15b8-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**、**Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)****Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="d15b8-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="d15b8-120">這些 Cmdlet 現在會接受 ``-Acl`` 參數的 ``DataLakeStoreItemAce[]``。</span><span class="sxs-lookup"><span data-stu-id="d15b8-120">These cmdlets now accept ``DataLakeStoreItemAce[]`` for the ``-Acl`` parameter.</span></span>
- <span data-ttu-id="d15b8-121">``DataLakeStoreItemAce[]`` 會由 ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)`` 傳回。</span><span class="sxs-lookup"><span data-stu-id="d15b8-121">``DataLakeStoreItemAce[]`` is returned by ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="d15b8-122">ApiManagement Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="d15b8-122">Breaking changes to ApiManagement cmdlets</span></span>

<span data-ttu-id="d15b8-123">受到此版本 ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)) 影響的 Cmdlet 如下：</span><span class="sxs-lookup"><span data-stu-id="d15b8-123">The following cmdlets were affected this release ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span></span>

<span data-ttu-id="d15b8-124">**New-AzureRmApiManagementVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="d15b8-124">**New-AzureRmApiManagementVirtualNetwork**</span></span>
- <span data-ttu-id="d15b8-125">參考虛擬網路的必要參數從要求 SubnetName 和 SubnetResourceId 變更為 VnetId (格式為 ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``)</span><span class="sxs-lookup"><span data-stu-id="d15b8-125">The required parameters to reference a virtual network changed from requiring SubnetName and VnetId to SubnetResourceId in format ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span></span>

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

<span data-ttu-id="d15b8-126">**取代 Set-AzureRmApiManagementVirtualNetworks Cmdlet**</span><span class="sxs-lookup"><span data-stu-id="d15b8-126">**Deprecating Cmdlet Set-AzureRmApiManagementVirtualNetworks**</span></span>
- <span data-ttu-id="d15b8-127">此 Cmdlet 將受到取代，因為有多個方法可用來設定與 ApiManagement 部署相關聯的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="d15b8-127">The Cmdlet is getting deprecated as there was more than one way to Set Virtual Network associated to ApiManagement deployment.</span></span>

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="d15b8-128">Network Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="d15b8-128">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="d15b8-129">受到此版本 ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)) 影響的 Cmdlet 如下：</span><span class="sxs-lookup"><span data-stu-id="d15b8-129">The following cmdlets were affected this release ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span></span>

<span data-ttu-id="d15b8-130">**New-AzureRmVirtualNetworkGateway**</span><span class="sxs-lookup"><span data-stu-id="d15b8-130">**New-AzureRmVirtualNetworkGateway**</span></span>
- <span data-ttu-id="d15b8-131">已移除變更內容的描述 ``:- Bool parameter:-ActiveActive``，並新增 ``SwitchParameter:-EnableActiveActiveFeature``，以啟用新建虛擬網路閘道上的 Active-Active 功能。</span><span class="sxs-lookup"><span data-stu-id="d15b8-131">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and ``SwitchParameter:-EnableActiveActiveFeature`` is added for enabling Active-Active feature on newly creating virtual network gateway.</span></span>

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

<span data-ttu-id="d15b8-132">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d15b8-132">Set-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="d15b8-133">已移除變更內容的描述 ``:- Bool parameter:-ActiveActive``，並新增 2 個 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature``，以啟用和停用虛擬網路閘道上的 Active-Active 功能。</span><span class="sxs-lookup"><span data-stu-id="d15b8-133">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` are added for enabling and disabling Active-Active feature on virtual network gateway.</span></span>

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