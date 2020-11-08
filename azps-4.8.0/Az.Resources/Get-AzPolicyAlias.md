---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
ms.openlocfilehash: b2881c735caae8f644676b1ee19cb0d80725c13a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135671"
---
# <span data-ttu-id="00681-101">Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="00681-101">Get-AzPolicyAlias</span></span>

## <span data-ttu-id="00681-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00681-102">SYNOPSIS</span></span>
<span data-ttu-id="00681-103">Get-AzPolicyAlias 檢索及輸出已定義別名並符合指定參數值的 Azure 提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="00681-103">Get-AzPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="00681-104">如果未提供任何參數，則會輸出包含別名的所有提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="00681-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="00681-105">-ListAvailable 開關會列出所有相符的資源類型，包括不含別名的那些資源類型來修改此行為。</span><span class="sxs-lookup"><span data-stu-id="00681-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

## <span data-ttu-id="00681-106">句法</span><span class="sxs-lookup"><span data-stu-id="00681-106">SYNTAX</span></span>

```
Get-AzPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00681-107">說明</span><span class="sxs-lookup"><span data-stu-id="00681-107">DESCRIPTION</span></span>
<span data-ttu-id="00681-108">**AzPolicyAlias** Cmdlet 會取得原則別名清單。</span><span class="sxs-lookup"><span data-stu-id="00681-108">The **Get-AzPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="00681-109">策略別名是由 Azure Policy 用來參照資源類型屬性。</span><span class="sxs-lookup"><span data-stu-id="00681-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="00681-110">提供的參數可根據資源類型或其別名的各種屬性來限制清單中的專案。</span><span class="sxs-lookup"><span data-stu-id="00681-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="00681-111">如果目標字串包含使用不區分大小寫的比較，則指定的 match 值會相符。</span><span class="sxs-lookup"><span data-stu-id="00681-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="00681-112">示例</span><span class="sxs-lookup"><span data-stu-id="00681-112">EXAMPLES</span></span>

### <span data-ttu-id="00681-113">範例1</span><span class="sxs-lookup"><span data-stu-id="00681-113">Example 1</span></span>
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

<span data-ttu-id="00681-114">列出具有別名的所有提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="00681-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="00681-115">範例2</span><span class="sxs-lookup"><span data-stu-id="00681-115">Example 2</span></span>
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

<span data-ttu-id="00681-116">列出所有提供者資源類型，包括不含別名的物件。</span><span class="sxs-lookup"><span data-stu-id="00681-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="00681-117">範例3</span><span class="sxs-lookup"><span data-stu-id="00681-117">Example 3</span></span>
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

<span data-ttu-id="00681-118">列出命名空間與「compute」相符且包含別名的所有提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="00681-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="00681-119">範例4</span><span class="sxs-lookup"><span data-stu-id="00681-119">Example 4</span></span>
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

<span data-ttu-id="00681-120">列出資源類型符合「virtual」且包含別名的所有提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="00681-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="00681-121">範例5</span><span class="sxs-lookup"><span data-stu-id="00681-121">Example 5</span></span>
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

<span data-ttu-id="00681-122">列出資源類型符合「virtual」的所有提供者資源類型，包括不含別名的服務。</span><span class="sxs-lookup"><span data-stu-id="00681-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="00681-123">範例6</span><span class="sxs-lookup"><span data-stu-id="00681-123">Example 6</span></span>
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

<span data-ttu-id="00681-124">列出其 namespace 與「compute」相符且資源類型符合「virtual」且包含別名的所有提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="00681-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="00681-125">注意：-NamespaceMatch 和-ResourceTypeMatch 提供專屬相符，而其他則是包含。</span><span class="sxs-lookup"><span data-stu-id="00681-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="00681-126">範例7</span><span class="sxs-lookup"><span data-stu-id="00681-126">Example 7</span></span>
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

<span data-ttu-id="00681-127">列出所有包含與「virtual」相符的別名的提供者資源類型。</span><span class="sxs-lookup"><span data-stu-id="00681-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="00681-128">範例8</span><span class="sxs-lookup"><span data-stu-id="00681-128">Example 8</span></span>
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

<span data-ttu-id="00681-129">列出所有包含與「virtual」相符的別名的提供者資源類型，或是與「網路」相符路徑的別名。</span><span class="sxs-lookup"><span data-stu-id="00681-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="00681-130">範例9</span><span class="sxs-lookup"><span data-stu-id="00681-130">Example 9</span></span>
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

<span data-ttu-id="00681-131">使用 Alpha api 版本列出所有提供者資源類型，或包含含 Alpha api 版本的別名。</span><span class="sxs-lookup"><span data-stu-id="00681-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="00681-132">參數</span><span class="sxs-lookup"><span data-stu-id="00681-132">PARAMETERS</span></span>

### <span data-ttu-id="00681-133">-AliasMatch</span><span class="sxs-lookup"><span data-stu-id="00681-133">-AliasMatch</span></span>
<span data-ttu-id="00681-134">在輸出專案中包含其名稱符合此值的別名。</span><span class="sxs-lookup"><span data-stu-id="00681-134">Includes in the output items with aliases whose name matches this value.</span></span>


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

### <span data-ttu-id="00681-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="00681-135">-ApiVersion</span></span>
<span data-ttu-id="00681-136">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="00681-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="00681-137">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="00681-137">If not specified, the API version is automatically determined as the latest available.</span></span>


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

### <span data-ttu-id="00681-138">-ApiVersionMatch</span><span class="sxs-lookup"><span data-stu-id="00681-138">-ApiVersionMatch</span></span>
<span data-ttu-id="00681-139">包含在其資源類型或別名具有相符 api 版本的輸出專案中。</span><span class="sxs-lookup"><span data-stu-id="00681-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>


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

### <span data-ttu-id="00681-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00681-140">-DefaultProfile</span></span>
<span data-ttu-id="00681-141">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="00681-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="00681-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="00681-142">-ListAvailable</span></span>
<span data-ttu-id="00681-143">包含在具有與不含別名的輸出相符專案中。</span><span class="sxs-lookup"><span data-stu-id="00681-143">Includes in the output matching items with and without aliases.</span></span>


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

### <span data-ttu-id="00681-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="00681-144">-LocationMatch</span></span>
<span data-ttu-id="00681-145">包含在其資源類型具有相符位置的輸出專案中。</span><span class="sxs-lookup"><span data-stu-id="00681-145">Includes in the output items whose resource types have a matching location.</span></span>


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

### <span data-ttu-id="00681-146">-NamespaceMatch</span><span class="sxs-lookup"><span data-stu-id="00681-146">-NamespaceMatch</span></span>
<span data-ttu-id="00681-147">將輸出限制為 namespace 與此值相符的專案。</span><span class="sxs-lookup"><span data-stu-id="00681-147">Limits the output to items whose namespace matches this value.</span></span>


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

### <span data-ttu-id="00681-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="00681-148">-PathMatch</span></span>
<span data-ttu-id="00681-149">包含在包含與此值相符之路徑之別名的輸出專案中。</span><span class="sxs-lookup"><span data-stu-id="00681-149">Includes in the output items with aliases containing a path that matches this value.</span></span>


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

### <span data-ttu-id="00681-150">-預先</span><span class="sxs-lookup"><span data-stu-id="00681-150">-Pre</span></span>
<span data-ttu-id="00681-151">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="00681-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>


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

### <span data-ttu-id="00681-152">-ResourceTypeMatch</span><span class="sxs-lookup"><span data-stu-id="00681-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="00681-153">將輸出限制為資源類型符合此值的專案。</span><span class="sxs-lookup"><span data-stu-id="00681-153">Limits the output to items whose resource type matches this value.</span></span>


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

### <span data-ttu-id="00681-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00681-154">CommonParameters</span></span>
<span data-ttu-id="00681-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00681-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00681-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="00681-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00681-157">輸入</span><span class="sxs-lookup"><span data-stu-id="00681-157">INPUTS</span></span>

### <span data-ttu-id="00681-158">所有</span><span class="sxs-lookup"><span data-stu-id="00681-158">None</span></span>

## <span data-ttu-id="00681-159">輸出</span><span class="sxs-lookup"><span data-stu-id="00681-159">OUTPUTS</span></span>

### <span data-ttu-id="00681-160">PsResourceProviderAlias 中的 [命令]</span><span class="sxs-lookup"><span data-stu-id="00681-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="00681-161">筆記</span><span class="sxs-lookup"><span data-stu-id="00681-161">NOTES</span></span>

* <span data-ttu-id="00681-162">若要展開別名或任何其他屬性，請將輸出管道 `select -ExpandProperty <property>` 。</span><span class="sxs-lookup"><span data-stu-id="00681-162">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="00681-163">例如： `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="00681-163">For example: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="00681-164">您可以在輸出中使用其他屬性，並透過將輸出輸送至來顯示 `Format-List` 。</span><span class="sxs-lookup"><span data-stu-id="00681-164">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="00681-165">例如： `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="00681-165">For example: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="00681-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="00681-166">RELATED LINKS</span></span>
