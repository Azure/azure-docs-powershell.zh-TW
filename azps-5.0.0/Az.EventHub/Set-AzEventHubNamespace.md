---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: f13a92bef4bfbafc67beec6d99cf02d8d1d63c31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138881"
---
# <span data-ttu-id="8e268-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="8e268-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="8e268-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e268-102">SYNOPSIS</span></span>
<span data-ttu-id="8e268-103">更新指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="8e268-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="8e268-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e268-104">SYNTAX</span></span>

### <span data-ttu-id="8e268-105">NamespaceParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8e268-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-Identity] [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e268-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e268-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity]
 [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e268-107">IdentityUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e268-107">IdentityUpdateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e268-108">說明</span><span class="sxs-lookup"><span data-stu-id="8e268-108">DESCRIPTION</span></span>
<span data-ttu-id="8e268-109">Set-AzEventHubNamespace Cmdlet 會更新指定事件中樞命名空間的屬性。</span><span class="sxs-lookup"><span data-stu-id="8e268-109">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="8e268-110">示例</span><span class="sxs-lookup"><span data-stu-id="8e268-110">EXAMPLES</span></span>

### <span data-ttu-id="8e268-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8e268-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="8e268-112">更新要建立之命名空間 MyNamespaceName 的標記 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="8e268-112">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="8e268-113">範例2</span><span class="sxs-lookup"><span data-stu-id="8e268-113">Example 2</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10 

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="8e268-114">\` \` 使用 AutoInflate = Enabled 和 MaximumThroughputUnits = 10 更新命名空間 MyNamespaceName 的狀態</span><span class="sxs-lookup"><span data-stu-id="8e268-114">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

### <span data-ttu-id="8e268-115">範例3</span><span class="sxs-lookup"><span data-stu-id="8e268-115">Example 3</span></span>

<span data-ttu-id="8e268-116">更新指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="8e268-116">Updates the specified Event Hubs namespace.</span></span> <span data-ttu-id="8e268-117"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="8e268-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzEventHubNamespace -Location 'WestUS' -Name MyNamespaceName -ResourceGroupName MyResourceGroupName -SkuName Basic
```

### <span data-ttu-id="8e268-118">範例5：在群集中使用 [管理身分識別] 建立及更新命名空間</span><span class="sxs-lookup"><span data-stu-id="8e268-118">Example 5: Creating and updating Namespace with Manage Identity in a cluster</span></span> 
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
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
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
PS C:\> $getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
$key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperty @(@($key.Name, $keyvault.VaultUri,""))

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

## <span data-ttu-id="8e268-119">參數</span><span class="sxs-lookup"><span data-stu-id="8e268-119">PARAMETERS</span></span>

### <span data-ttu-id="8e268-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e268-120">-DefaultProfile</span></span>
<span data-ttu-id="8e268-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e268-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e268-122">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="8e268-122">-EnableAutoInflate</span></span>
<span data-ttu-id="8e268-123">指出是否已啟用 AutoInflate</span><span class="sxs-lookup"><span data-stu-id="8e268-123">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e268-124">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="8e268-124">-EnableKafka</span></span>
<span data-ttu-id="8e268-125">啟用或停用命名空間的 Kafka</span><span class="sxs-lookup"><span data-stu-id="8e268-125">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="8e268-126">身分識別</span><span class="sxs-lookup"><span data-stu-id="8e268-126">-Identity</span></span>
<span data-ttu-id="8e268-127">啟用或停用命名空間的身分識別</span><span class="sxs-lookup"><span data-stu-id="8e268-127">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="8e268-128">-IdentityUserDefined</span><span class="sxs-lookup"><span data-stu-id="8e268-128">-IdentityUserDefined</span></span>
<span data-ttu-id="8e268-129">使用者定義的身分識別或無</span><span class="sxs-lookup"><span data-stu-id="8e268-129">User defined Identity or None</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e268-130">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="8e268-130">-KeyProperty</span></span>
<span data-ttu-id="8e268-131">索引鍵屬性清單，@ ( @ (KeyName、KeyVaultUri、Keyversion) 、@ (KeyName、KeyVaultUri、Keyversion) # A5</span><span class="sxs-lookup"><span data-stu-id="8e268-131">List of Key Properties, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String[]]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e268-132">-KeySource</span><span class="sxs-lookup"><span data-stu-id="8e268-132">-KeySource</span></span>
<span data-ttu-id="8e268-133">金鑰來源</span><span class="sxs-lookup"><span data-stu-id="8e268-133">Key Source</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e268-134">-位置</span><span class="sxs-lookup"><span data-stu-id="8e268-134">-Location</span></span>
<span data-ttu-id="8e268-135">EventHub 命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="8e268-135">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="8e268-136">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="8e268-136">-MaximumThroughputUnits</span></span>
<span data-ttu-id="8e268-137">啟用 AutoInflate 時的輸送量單位上限，值應該在0到20輸送量單位內。</span><span class="sxs-lookup"><span data-stu-id="8e268-137">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e268-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e268-138">-Name</span></span>
<span data-ttu-id="8e268-139">EventHub 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="8e268-139">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="8e268-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e268-140">-ResourceGroupName</span></span>
<span data-ttu-id="8e268-141">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8e268-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="8e268-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="8e268-142">-SkuCapacity</span></span>
<span data-ttu-id="8e268-143">Eventhub 輸送量單位。</span><span class="sxs-lookup"><span data-stu-id="8e268-143">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="8e268-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8e268-144">-SkuName</span></span>
<span data-ttu-id="8e268-145">命名空間 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="8e268-145">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="8e268-146">-State</span><span class="sxs-lookup"><span data-stu-id="8e268-146">-State</span></span>
<span data-ttu-id="8e268-147">停用/啟用命名空間。</span><span class="sxs-lookup"><span data-stu-id="8e268-147">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e268-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="8e268-148">-Tag</span></span>
<span data-ttu-id="8e268-149">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="8e268-149">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e268-150">-確認</span><span class="sxs-lookup"><span data-stu-id="8e268-150">-Confirm</span></span>
<span data-ttu-id="8e268-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e268-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e268-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e268-152">-WhatIf</span></span>
<span data-ttu-id="8e268-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e268-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e268-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e268-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e268-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e268-155">CommonParameters</span></span>
<span data-ttu-id="8e268-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e268-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e268-157">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8e268-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e268-158">輸入</span><span class="sxs-lookup"><span data-stu-id="8e268-158">INPUTS</span></span>

### <span data-ttu-id="8e268-159">System.object</span><span class="sxs-lookup"><span data-stu-id="8e268-159">System.String</span></span>

### <span data-ttu-id="8e268-160">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8e268-160">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="8e268-161">"NamespaceState" 1 [[1.4.3.0]、[]、[]、[Culture = 中性]、[PublicKeyToken = null]]。</span><span class="sxs-lookup"><span data-stu-id="8e268-161">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8e268-162">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8e268-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8e268-163">輸出</span><span class="sxs-lookup"><span data-stu-id="8e268-163">OUTPUTS</span></span>

### <span data-ttu-id="8e268-164">PSNamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e268-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="8e268-165">筆記</span><span class="sxs-lookup"><span data-stu-id="8e268-165">NOTES</span></span>

## <span data-ttu-id="8e268-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e268-166">RELATED LINKS</span></span>