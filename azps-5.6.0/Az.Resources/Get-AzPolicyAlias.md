---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azpolicyalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
ms.openlocfilehash: cc77008f4aa8cb170dc86f0b7d9847fe40e87254
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912621"
---
# <span data-ttu-id="2bc45-101">Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="2bc45-101">Get-AzPolicyAlias</span></span>

## <span data-ttu-id="2bc45-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2bc45-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc45-103">Get-AzPolicyAlias會取及輸出已定義別名且符合指定參數值的 Azure 提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="2bc45-103">Get-AzPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="2bc45-104">如果沒有提供參數，將會輸出包含別名的所有提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="2bc45-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="2bc45-105">-ListAvailable 切換器會列出所有符合的資源類型，包括沒有別名的資源類型，以修改此行為。</span><span class="sxs-lookup"><span data-stu-id="2bc45-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

## <span data-ttu-id="2bc45-106">語法</span><span class="sxs-lookup"><span data-stu-id="2bc45-106">SYNTAX</span></span>

```
Get-AzPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bc45-107">描述</span><span class="sxs-lookup"><span data-stu-id="2bc45-107">DESCRIPTION</span></span>
<span data-ttu-id="2bc45-108">**Get-AzPolicyAlias Cmdlet** 會取得一個策略別名清單。</span><span class="sxs-lookup"><span data-stu-id="2bc45-108">The **Get-AzPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="2bc45-109">Azure Policy 會使用策略別名來參照資源類型屬性。</span><span class="sxs-lookup"><span data-stu-id="2bc45-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="2bc45-110">提供的參數可比對資源類型或別名的各種屬性，以限制清單中專案。</span><span class="sxs-lookup"><span data-stu-id="2bc45-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="2bc45-111">如果目標字串包含目標字串，使用不區分大小寫的比較，指定相符值會相符。</span><span class="sxs-lookup"><span data-stu-id="2bc45-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="2bc45-112">例子</span><span class="sxs-lookup"><span data-stu-id="2bc45-112">EXAMPLES</span></span>

### <span data-ttu-id="2bc45-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="2bc45-113">Example 1</span></span>
```powershell
PS C:\> Get-AzPolicyAlias

Namespace                     ResourceType                                   Aliases
---------                     ------------                                   -------
Microsoft.AnalysisServices    servers                                        {Microsoft.AnalysisServices/servers/state, Microsoft.AnalysisServices/s...
Microsoft.Authorization       roleAssignments                                {Microsoft.Authorization/roleAssignments/roleDefinitionId, Microsoft.Au...
Microsoft.Authorization       roleDefinitions                                {Microsoft.Authorization/roleDefinitions/type, Microsoft.Authorization/...

...                           ...                                            ...

Microsoft.Web                 hostingEnvironments                            {Microsoft.Web/hostingEnvironments/clusterSettings[*].name, Microsoft.W...
Microsoft.Web                 sites/config                                   {Microsoft.Web/sites/config/httpLoggingEnabled, Microsoft.Web/sites/con...
Microsoft.GuestConfiguration  guestConfigurationAssignments                  {Microsoft.GuestConfiguration/guestConfigurationAssignments/complianceS...


PS C:\>
```

<span data-ttu-id="2bc45-114">列出具有別名的所有提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="2bc45-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="2bc45-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="2bc45-115">Example 2</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ListAvailable

Namespace                                ResourceType                                                        Aliases
---------                                ------------                                                        -------

...                                      ...                                                                 ...

Microsoft.AlertsManagement               operations                                                          {}
Microsoft.AnalysisServices               servers                                                             {Microsoft.AnalysisServices/servers/sta...
Microsoft.AnalysisServices               locations                                                           {}

...                                      ...                                                                 ...


PS C:\>
```

<span data-ttu-id="2bc45-116">列出所有提供者資源類型，包括沒有別名的提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="2bc45-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="2bc45-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="2bc45-117">Example 3</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...
Microsoft.Compute disks                              {Microsoft.Compute/imagePublisher, Microsoft.Compute/imageOffer, Microsoft.Compute/imageSku, Mi...


PS C:\>
```

<span data-ttu-id="2bc45-118">列出命名空間符合 'compute' 且包含別名的所有提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="2bc45-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="2bc45-119">範例 4</span><span class="sxs-lookup"><span data-stu-id="2bc45-119">Example 4</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual'

Namespace         ResourceType                           Aliases
---------         ------------                           -------
Microsoft.Compute virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Micro...
Microsoft.Compute virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualM...
Microsoft.Compute virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleS...
Microsoft.Compute virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/...
Microsoft.Network virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGateway...
Microsoft.Network virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetworks...
Microsoft.Network virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql     servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers/vi...


PS C:\>
```

<span data-ttu-id="2bc45-120">列出資源類型符合"虛擬"且包含別名的所有提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="2bc45-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="2bc45-121">範例 5</span><span class="sxs-lookup"><span data-stu-id="2bc45-121">Example 5</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual' -ListAvailable

Namespace                    ResourceType                                               Aliases
---------                    ------------                                               -------

...                          ...                                                        ...

Microsoft.KeyVault           locations/deleteVirtualNetworkOrSubnets                    {}
Microsoft.Network            virtualNetworks                                            {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id,...
Microsoft.Network            virtualNetworkGateways                                     {Microsoft.Network/virtualNetworkGateways/sku.name, Microsof...
Microsoft.Network            locations/virtualNetworkAvailableEndpointServices          {}

...                          ...                                                        ...


PS C:\>
```

<span data-ttu-id="2bc45-122">列出資源類型符合'虛擬'的所有提供者資源類型，包括沒有別名的提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="2bc45-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="2bc45-123">範例 6</span><span class="sxs-lookup"><span data-stu-id="2bc45-123">Example 6</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute' -ResourceTypeMatch 'virtual'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...


PS C:\>
```

<span data-ttu-id="2bc45-124">列出命名空間符合 'compute' 的所有提供者資源類型，而資源類型符合'虛擬'且包含別名。</span><span class="sxs-lookup"><span data-stu-id="2bc45-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="2bc45-125">注意：-命名空間Match 和 -ResourceTypeMatch 提供獨佔比對，而其他則包含。</span><span class="sxs-lookup"><span data-stu-id="2bc45-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="2bc45-126">範例 7</span><span class="sxs-lookup"><span data-stu-id="2bc45-126">Example 7</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="2bc45-127">列出所有包含符合"虛擬」別名的提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="2bc45-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="2bc45-128">範例 8</span><span class="sxs-lookup"><span data-stu-id="2bc45-128">Example 8</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual' -PathMatch 'network'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    networkInterfaces                      {Microsoft.Network/networkInterfaces/ipconfigurations[*].subnet.id, Microsoft.Network/ne...
Microsoft.Network    networkSecurityGroups                  {Microsoft.Network/networkSecurityGroups/securityRules[*].protocol, Microsoft.Network/ne...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="2bc45-129">列出所有包含別名符合'虛擬'或路徑符合'網路'的別名的提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="2bc45-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="2bc45-130">範例 9</span><span class="sxs-lookup"><span data-stu-id="2bc45-130">Example 9</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ApiVersionMatch 'alpha'

Namespace          ResourceType        Aliases
---------          ------------        -------
Microsoft.Cache    Redis               {Microsoft.Cache/Redis/sku.name, Microsoft.Cache/Redis/sku.family, Microsoft.Cache/Redis/sku.capacity, Micros...
Microsoft.Cache    Redis/firewallrules {Microsoft.Cache/Redis/firewallrules/startIP, Microsoft.Cache/Redis/firewallrules/endIP}
Microsoft.Security alerts              {Microsoft.Security/alerts/state}
Microsoft.Security pricings            {Microsoft.Security/pricings/pricingTier}
Microsoft.Security complianceResults   {Microsoft.Security/complianceResults/resourceStatus}


PS C:\>
```

<span data-ttu-id="2bc45-131">列出具有 Alpha api 版本或包含 Alpha api 版本別名的所有提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="2bc45-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="2bc45-132">參數</span><span class="sxs-lookup"><span data-stu-id="2bc45-132">PARAMETERS</span></span>

### <span data-ttu-id="2bc45-133">-AliasMatch</span><span class="sxs-lookup"><span data-stu-id="2bc45-133">-AliasMatch</span></span>
<span data-ttu-id="2bc45-134">包含名稱符合此值之別名的輸出專案。</span><span class="sxs-lookup"><span data-stu-id="2bc45-134">Includes in the output items with aliases whose name matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Alias

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc45-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2bc45-135">-ApiVersion</span></span>
<span data-ttu-id="2bc45-136">設定時，表示要使用資源提供者 API 的版本。</span><span class="sxs-lookup"><span data-stu-id="2bc45-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="2bc45-137">如果未指定，API 版本會自動判斷為最新可用。</span><span class="sxs-lookup"><span data-stu-id="2bc45-137">If not specified, the API version is automatically determined as the latest available.</span></span>


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

### <span data-ttu-id="2bc45-138">-ApiVersionMatch</span><span class="sxs-lookup"><span data-stu-id="2bc45-138">-ApiVersionMatch</span></span>
<span data-ttu-id="2bc45-139">包含資源類型或別名具有比對 api 版本的輸出專案。</span><span class="sxs-lookup"><span data-stu-id="2bc45-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>


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

### <span data-ttu-id="2bc45-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc45-140">-DefaultProfile</span></span>
<span data-ttu-id="2bc45-141">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bc45-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2bc45-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="2bc45-142">-ListAvailable</span></span>
<span data-ttu-id="2bc45-143">包含包含或不含別名的輸出比對專案。</span><span class="sxs-lookup"><span data-stu-id="2bc45-143">Includes in the output matching items with and without aliases.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: ShowAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc45-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="2bc45-144">-LocationMatch</span></span>
<span data-ttu-id="2bc45-145">包含資源類型具有比對位置的輸出專案。</span><span class="sxs-lookup"><span data-stu-id="2bc45-145">Includes in the output items whose resource types have a matching location.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc45-146">-命名空間Match</span><span class="sxs-lookup"><span data-stu-id="2bc45-146">-NamespaceMatch</span></span>
<span data-ttu-id="2bc45-147">將輸出限制于命名空間符合此值的專案。</span><span class="sxs-lookup"><span data-stu-id="2bc45-147">Limits the output to items whose namespace matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, Namespace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc45-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="2bc45-148">-PathMatch</span></span>
<span data-ttu-id="2bc45-149">包含包含符合此值之路徑之別名的輸出專案。</span><span class="sxs-lookup"><span data-stu-id="2bc45-149">Includes in the output items with aliases containing a path that matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc45-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="2bc45-150">-Pre</span></span>
<span data-ttu-id="2bc45-151">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="2bc45-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>


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

### <span data-ttu-id="2bc45-152">-ResourceTypeMatch</span><span class="sxs-lookup"><span data-stu-id="2bc45-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="2bc45-153">將輸出限制于資源類型符合此值的專案。</span><span class="sxs-lookup"><span data-stu-id="2bc45-153">Limits the output to items whose resource type matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceType, Resource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc45-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc45-154">CommonParameters</span></span>
<span data-ttu-id="2bc45-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2bc45-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc45-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2bc45-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc45-157">輸入</span><span class="sxs-lookup"><span data-stu-id="2bc45-157">INPUTS</span></span>

### <span data-ttu-id="2bc45-158">沒有</span><span class="sxs-lookup"><span data-stu-id="2bc45-158">None</span></span>

## <span data-ttu-id="2bc45-159">輸出</span><span class="sxs-lookup"><span data-stu-id="2bc45-159">OUTPUTS</span></span>

### <span data-ttu-id="2bc45-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span><span class="sxs-lookup"><span data-stu-id="2bc45-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="2bc45-161">筆記</span><span class="sxs-lookup"><span data-stu-id="2bc45-161">NOTES</span></span>

* <span data-ttu-id="2bc45-162">若要展開 Aliases 或其他任何屬性，請將輸出移至 `select -ExpandProperty <property>` 。</span><span class="sxs-lookup"><span data-stu-id="2bc45-162">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="2bc45-163">例如： `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="2bc45-163">For example: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="2bc45-164">其他屬性可在輸出中使用，並可以輸出到的管道顯示 `Format-List` 。</span><span class="sxs-lookup"><span data-stu-id="2bc45-164">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="2bc45-165">例如： `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="2bc45-165">For example: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="2bc45-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bc45-166">RELATED LINKS</span></span>
