---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: 7abc847bebf5baeea1bf12db6d930bd2daa34d7f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902081"
---
# <span data-ttu-id="933b3-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="933b3-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="933b3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="933b3-102">SYNOPSIS</span></span>
<span data-ttu-id="933b3-103">建立事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="933b3-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="933b3-104">語法</span><span class="sxs-lookup"><span data-stu-id="933b3-104">SYNTAX</span></span>

### <span data-ttu-id="933b3-105">命名空間ParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="933b3-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-ZoneRedundant]
 [[-ClusterARMId] <String>] [-Identity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="933b3-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="933b3-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-ZoneRedundant] [[-ClusterARMId] <String>] [-Identity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="933b3-107">描述</span><span class="sxs-lookup"><span data-stu-id="933b3-107">DESCRIPTION</span></span>
<span data-ttu-id="933b3-108">此New-AzEventHubNamespace Cmdlet 會建立類型為事件中樞的新命名空間。</span><span class="sxs-lookup"><span data-stu-id="933b3-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="933b3-109">例子</span><span class="sxs-lookup"><span data-stu-id="933b3-109">EXAMPLES</span></span>
### <span data-ttu-id="933b3-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="933b3-110">Example 1</span></span>                                           
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

<span data-ttu-id="933b3-111">在資源群組 MyResourceGroupName 的指定地理位置 MyLocation 中建立事件中樞命名空間 \` \` \` \` \` MyNamespaceName。 \`</span><span class="sxs-lookup"><span data-stu-id="933b3-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="933b3-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="933b3-112">Example 2</span></span>
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

<span data-ttu-id="933b3-113">在指定的地理位置 MyLocation 中建立事件中樞命名空間 \` MyNamespaceName，資源群組 \` \` \` \` MyResourceGroupName 和 \` AutoInflate 會以 MaximumThroughputUnits 10 啟用。</span><span class="sxs-lookup"><span data-stu-id="933b3-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="933b3-114">範例 3：啟用 Kafka 的命名空間</span><span class="sxs-lookup"><span data-stu-id="933b3-114">Example 3: Kafka enabled namespace</span></span>
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

<span data-ttu-id="933b3-115">在啟用 Kafka 和 AutoInflate 的資源群組 MyResourceGroupName 中，于指定的地理位置 MyLocation 中建立事件中樞命名空間 \` \` \` \` \` \` MyNamespaceName。</span><span class="sxs-lookup"><span data-stu-id="933b3-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="933b3-116">範例 4：ZoneRedundant 啟用命名空間</span><span class="sxs-lookup"><span data-stu-id="933b3-116">Example 4: ZoneRedundant enabled namespace</span></span>
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

<span data-ttu-id="933b3-117">在啟用 Kafka 和 AutoInflate 的資源群組 MyResourceGroupName 中，于指定的地理位置 MyLocation 中建立事件中樞命名空間 \` \` \` \` \` \` MyNamespaceName。</span><span class="sxs-lookup"><span data-stu-id="933b3-117">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="933b3-118">範例 5：在組集中使用管理身分識別建立命名空間</span><span class="sxs-lookup"><span data-stu-id="933b3-118">Example 5: Creating Namespace with Manage Identity in a cluster</span></span> 
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

## <span data-ttu-id="933b3-119">參數</span><span class="sxs-lookup"><span data-stu-id="933b3-119">PARAMETERS</span></span>

### <span data-ttu-id="933b3-120">-ClusterARMId</span><span class="sxs-lookup"><span data-stu-id="933b3-120">-ClusterARMId</span></span>
<span data-ttu-id="933b3-121">要建立命名空間的組群 ARM 識別碼</span><span class="sxs-lookup"><span data-stu-id="933b3-121">ARM ID of Cluster where namespace is to be created</span></span>

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

### <span data-ttu-id="933b3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="933b3-122">-DefaultProfile</span></span>
<span data-ttu-id="933b3-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="933b3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="933b3-124">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="933b3-124">-EnableAutoInflate</span></span>
<span data-ttu-id="933b3-125">表示是否已啟用 AutoInflate</span><span class="sxs-lookup"><span data-stu-id="933b3-125">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="933b3-126">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="933b3-126">-EnableKafka</span></span>
<span data-ttu-id="933b3-127">啟用或停用 Kafka 的命名空間</span><span class="sxs-lookup"><span data-stu-id="933b3-127">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="933b3-128">-身分識別</span><span class="sxs-lookup"><span data-stu-id="933b3-128">-Identity</span></span>
<span data-ttu-id="933b3-129">啟用或停用命名空間的身分識別</span><span class="sxs-lookup"><span data-stu-id="933b3-129">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="933b3-130">-位置</span><span class="sxs-lookup"><span data-stu-id="933b3-130">-Location</span></span>
<span data-ttu-id="933b3-131">EventHub 命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="933b3-131">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="933b3-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="933b3-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="933b3-133">啟用 AutoInflate 時，輸送量單位的上限，值應在 0 到 20 個輸送量單位內。</span><span class="sxs-lookup"><span data-stu-id="933b3-133">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="933b3-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="933b3-134">-Name</span></span>
<span data-ttu-id="933b3-135">EventHub 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="933b3-135">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="933b3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="933b3-136">-ResourceGroupName</span></span>
<span data-ttu-id="933b3-137">資源組名</span><span class="sxs-lookup"><span data-stu-id="933b3-137">Resource Group Name</span></span>

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

### <span data-ttu-id="933b3-138">-Sku以</span><span class="sxs-lookup"><span data-stu-id="933b3-138">-SkuCapacity</span></span>
<span data-ttu-id="933b3-139">Eventhub 輸送量單位。</span><span class="sxs-lookup"><span data-stu-id="933b3-139">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="933b3-140">-SKUName</span><span class="sxs-lookup"><span data-stu-id="933b3-140">-SkuName</span></span>
<span data-ttu-id="933b3-141">命名空間 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="933b3-141">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="933b3-142">-標記</span><span class="sxs-lookup"><span data-stu-id="933b3-142">-Tag</span></span>
<span data-ttu-id="933b3-143">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="933b3-143">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="933b3-144">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="933b3-144">-ZoneRedundant</span></span>
<span data-ttu-id="933b3-145">啟用或停用命名空間的區域多餘的功能</span><span class="sxs-lookup"><span data-stu-id="933b3-145">enabling or disabling Zone Redundant for namespace</span></span>

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

### <span data-ttu-id="933b3-146">-確認</span><span class="sxs-lookup"><span data-stu-id="933b3-146">-Confirm</span></span>
<span data-ttu-id="933b3-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="933b3-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="933b3-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="933b3-148">-WhatIf</span></span>
<span data-ttu-id="933b3-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="933b3-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="933b3-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="933b3-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="933b3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933b3-151">CommonParameters</span></span>
<span data-ttu-id="933b3-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="933b3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="933b3-153">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="933b3-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933b3-154">輸入</span><span class="sxs-lookup"><span data-stu-id="933b3-154">INPUTS</span></span>

### <span data-ttu-id="933b3-155">System.String</span><span class="sxs-lookup"><span data-stu-id="933b3-155">System.String</span></span>

### <span data-ttu-id="933b3-156">System.Nullable'1[[System.Int32， mscorlib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="933b3-156">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="933b3-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="933b3-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="933b3-158">輸出</span><span class="sxs-lookup"><span data-stu-id="933b3-158">OUTPUTS</span></span>

### <span data-ttu-id="933b3-159">Microsoft.Azure.Commands.EventHub.models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="933b3-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="933b3-160">筆記</span><span class="sxs-lookup"><span data-stu-id="933b3-160">NOTES</span></span>

## <span data-ttu-id="933b3-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="933b3-161">RELATED LINKS</span></span>
