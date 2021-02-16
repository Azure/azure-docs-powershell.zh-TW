---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: a51fffe36102b05121e52054103357bd26f56d51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133239"
---
# <span data-ttu-id="0f2d6-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="0f2d6-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="0f2d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0f2d6-102">SYNOPSIS</span></span>
<span data-ttu-id="0f2d6-103">建立事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="0f2d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="0f2d6-104">SYNTAX</span></span>

### <span data-ttu-id="0f2d6-105">NamespaceParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0f2d6-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-ZoneRedundant]
 [[-ClusterARMId] <String>] [-Identity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f2d6-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f2d6-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-ZoneRedundant] [[-ClusterARMId] <String>] [-Identity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f2d6-107">說明</span><span class="sxs-lookup"><span data-stu-id="0f2d6-107">DESCRIPTION</span></span>
<span data-ttu-id="0f2d6-108">New-AzEventHubNamespace Cmdlet 會建立一個類型事件中樞的新命名空間。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="0f2d6-109">示例</span><span class="sxs-lookup"><span data-stu-id="0f2d6-109">EXAMPLES</span></span>
### <span data-ttu-id="0f2d6-110">範例1</span><span class="sxs-lookup"><span data-stu-id="0f2d6-110">Example 1</span></span>                                           
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/14/2020 9:02:16 PM
UpdatedAt                     : 6/14/2020 9:03:04 PM
ServiceBusEndpoint            : https://testingnew2018.servicebus.windows.net:443/
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : False
MaximumThroughputUnits        : 0
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="0f2d6-111">\` \` \` \` 在 [資源群組 MyResourceGroupName] 中，在指定的地理位置 MyLocation 中 \` \` 建立事件中心命名空間 MyNamespaceName。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0f2d6-112">範例2</span><span class="sxs-lookup"><span data-stu-id="0f2d6-112">Example 2</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="0f2d6-113">在 \` MyNamespaceName \` 的 [ \` \` 資源群組] MyResourceGroupName 中， \` \` 以及 MaximumThroughputUnits 10 啟用 AutoInflate，在指定的地理位置 MyLocation 中建立事件中心命名空間。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="0f2d6-114">範例3： Kafka 啟用的命名空間</span><span class="sxs-lookup"><span data-stu-id="0f2d6-114">Example 3: Kafka enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="0f2d6-115">\` \` \` \` 在 \` \` 已啟用 Kafka 和 AutoInflate 的 [資源群組] MyResourceGroupName 中，在指定的地理位置 MyLocation 中建立事件中心命名空間 MyNamespaceName。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="0f2d6-116">範例4： ZoneRedundant 啟用的命名空間</span><span class="sxs-lookup"><span data-stu-id="0f2d6-116">Example 4: ZoneRedundant enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -ZoneRedundant

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : True
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="0f2d6-117">\` \` \` \` 在 \` \` 已啟用 Kafka 和 AutoInflate 的 [資源群組] MyResourceGroupName 中，在指定的地理位置 MyLocation 中建立事件中心命名空間 MyNamespaceName。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-117">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="0f2d6-118">範例5：在群集中建立具有管理身分識別的命名空間</span><span class="sxs-lookup"><span data-stu-id="0f2d6-118">Example 5: Creating Namespace with Manage Identity in a cluster</span></span> 
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation --EnableAutoInflate -MaximumThroughputUnits 12 -EnableKafka -ZoneRedundant -Identity

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 12
ZoneRedundant                 : True
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity.PrincipalId          : ##########
Identity.TenantId             : ##########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :


# Get created namespace
PS C:\>$getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
PS C:\> $key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperties @(@($key.Name, $keyvault.VaultUri,""))

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
ServiceBusEndpoint            : #########
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          : #########
Identity.TenantId             : #########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          : MicrosoftKeyVault
Encryption.KeyVaultProperties : {testkey, https://myvaultname.vault.azure.net, }
```

## <span data-ttu-id="0f2d6-119">參數</span><span class="sxs-lookup"><span data-stu-id="0f2d6-119">PARAMETERS</span></span>

### <span data-ttu-id="0f2d6-120">-ClusterARMId</span><span class="sxs-lookup"><span data-stu-id="0f2d6-120">-ClusterARMId</span></span>
<span data-ttu-id="0f2d6-121">要建立命名空間之群集的 ARM 識別碼</span><span class="sxs-lookup"><span data-stu-id="0f2d6-121">ARM ID of Cluster where namespace is to be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f2d6-122">-DefaultProfile</span></span>
<span data-ttu-id="0f2d6-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f2d6-124">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="0f2d6-124">-EnableAutoInflate</span></span>
<span data-ttu-id="0f2d6-125">指出是否已啟用 AutoInflate</span><span class="sxs-lookup"><span data-stu-id="0f2d6-125">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d6-126">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="0f2d6-126">-EnableKafka</span></span>
<span data-ttu-id="0f2d6-127">啟用或停用命名空間的 Kafka</span><span class="sxs-lookup"><span data-stu-id="0f2d6-127">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="0f2d6-128">身分識別</span><span class="sxs-lookup"><span data-stu-id="0f2d6-128">-Identity</span></span>
<span data-ttu-id="0f2d6-129">啟用或停用命名空間的身分識別</span><span class="sxs-lookup"><span data-stu-id="0f2d6-129">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="0f2d6-130">-位置</span><span class="sxs-lookup"><span data-stu-id="0f2d6-130">-Location</span></span>
<span data-ttu-id="0f2d6-131">EventHub 命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-131">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d6-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="0f2d6-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="0f2d6-133">啟用 AutoInflate 時的輸送量單位上限，值應該在0到20輸送量單位內。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-133">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d6-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="0f2d6-134">-Name</span></span>
<span data-ttu-id="0f2d6-135">EventHub 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-135">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f2d6-136">-ResourceGroupName</span></span>
<span data-ttu-id="0f2d6-137">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="0f2d6-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d6-138">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="0f2d6-138">-SkuCapacity</span></span>
<span data-ttu-id="0f2d6-139">Eventhub 輸送量單位。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-139">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d6-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0f2d6-140">-SkuName</span></span>
<span data-ttu-id="0f2d6-141">命名空間 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-141">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d6-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="0f2d6-142">-Tag</span></span>
<span data-ttu-id="0f2d6-143">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-143">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d6-144">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="0f2d6-144">-ZoneRedundant</span></span>
<span data-ttu-id="0f2d6-145">啟用或停用命名空間的區域冗余</span><span class="sxs-lookup"><span data-stu-id="0f2d6-145">enabling or disabling Zone Redundant for namespace</span></span>

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

### <span data-ttu-id="0f2d6-146">-確認</span><span class="sxs-lookup"><span data-stu-id="0f2d6-146">-Confirm</span></span>
<span data-ttu-id="0f2d6-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f2d6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f2d6-148">-WhatIf</span></span>
<span data-ttu-id="0f2d6-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f2d6-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f2d6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f2d6-151">CommonParameters</span></span>
<span data-ttu-id="0f2d6-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f2d6-153">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0f2d6-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f2d6-154">輸入</span><span class="sxs-lookup"><span data-stu-id="0f2d6-154">INPUTS</span></span>

### <span data-ttu-id="0f2d6-155">System.object</span><span class="sxs-lookup"><span data-stu-id="0f2d6-155">System.String</span></span>

### <span data-ttu-id="0f2d6-156">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0f2d6-156">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0f2d6-157">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0f2d6-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0f2d6-158">輸出</span><span class="sxs-lookup"><span data-stu-id="0f2d6-158">OUTPUTS</span></span>

### <span data-ttu-id="0f2d6-159">PSNamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="0f2d6-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="0f2d6-160">筆記</span><span class="sxs-lookup"><span data-stu-id="0f2d6-160">NOTES</span></span>

## <span data-ttu-id="0f2d6-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f2d6-161">RELATED LINKS</span></span>
