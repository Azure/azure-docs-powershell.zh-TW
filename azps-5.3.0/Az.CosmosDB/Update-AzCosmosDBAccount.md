---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446004"
---
# <span data-ttu-id="1522f-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="1522f-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="1522f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1522f-102">SYNOPSIS</span></span>
<span data-ttu-id="1522f-103">更新 CosmosDB 帳戶屬性。</span><span class="sxs-lookup"><span data-stu-id="1522f-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="1522f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1522f-104">SYNTAX</span></span>

### <span data-ttu-id="1522f-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1522f-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1522f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1522f-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1522f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1522f-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1522f-108">說明</span><span class="sxs-lookup"><span data-stu-id="1522f-108">DESCRIPTION</span></span>
<span data-ttu-id="1522f-109">更新 CosmosDB 帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="1522f-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="1522f-110">無法使用其他屬性來更新帳戶區域 simulataneously。</span><span class="sxs-lookup"><span data-stu-id="1522f-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="1522f-111">示例</span><span class="sxs-lookup"><span data-stu-id="1522f-111">EXAMPLES</span></span>

### <span data-ttu-id="1522f-112">範例1</span><span class="sxs-lookup"><span data-stu-id="1522f-112">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name accountName -DefaultConsistencyLevel "Strong" -EnableAutomaticFailover 1 -EnableMultipleWriteLocations 1 -EnableVirtualNetwork 1

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : True
EnableAutomaticFailover       : True
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {accountName-eastus}
ReadLocations                 : {accountName-eastus}
FailoverPolicies              : {accountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : True
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/accountName
Name                          : accountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="1522f-113">已將 DefaultConsistencyLevel 更新為「強勁」、啟用 AutomaticFailover、啟用 MultipleWriteLocations，並啟用 VirtualNetwork 的 CosmosDB 帳戶具有名稱 accountName。</span><span class="sxs-lookup"><span data-stu-id="1522f-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="1522f-114">參數</span><span class="sxs-lookup"><span data-stu-id="1522f-114">PARAMETERS</span></span>

### <span data-ttu-id="1522f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1522f-115">-AsJob</span></span>
<span data-ttu-id="1522f-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1522f-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-117">-確認</span><span class="sxs-lookup"><span data-stu-id="1522f-117">-Confirm</span></span>
<span data-ttu-id="1522f-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1522f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="1522f-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="1522f-120">Cosmos DB 資料庫帳戶的預設一致性等級。</span><span class="sxs-lookup"><span data-stu-id="1522f-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="1522f-121">已接受的值： BoundedStaleness、ConsistentPrefix、最終、會話、強</span><span class="sxs-lookup"><span data-stu-id="1522f-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1522f-122">-DefaultProfile</span></span>
<span data-ttu-id="1522f-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1522f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="1522f-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="1522f-125">在中繼資料資源 (資料庫、容器、透過帳戶金鑰) 的輸送量中停用寫入作業</span><span class="sxs-lookup"><span data-stu-id="1522f-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="1522f-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="1522f-127">[Bool]，表示該帳戶是否已啟用 AnalyticalStorage。</span><span class="sxs-lookup"><span data-stu-id="1522f-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="1522f-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="1522f-129">在由於中斷而無法使用區域的極少事件中，啟用寫入區域的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="1522f-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="1522f-130">自動容錯移轉會針對該帳戶產生新的寫入區域，並根據針對該帳戶所設定的容錯移轉優先順序來選取。</span><span class="sxs-lookup"><span data-stu-id="1522f-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="1522f-131">已接受的值： false、true</span><span class="sxs-lookup"><span data-stu-id="1522f-131">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="1522f-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="1522f-133">啟用多個寫位置。</span><span class="sxs-lookup"><span data-stu-id="1522f-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="1522f-134">已接受的值： false、true</span><span class="sxs-lookup"><span data-stu-id="1522f-134">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1522f-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="1522f-136">在 Cosmos DB 資料庫帳戶上啟用虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="1522f-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="1522f-137">已接受的值： false、true</span><span class="sxs-lookup"><span data-stu-id="1522f-137">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1522f-138">-InputObject</span></span>
<span data-ttu-id="1522f-139">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="1522f-139">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="1522f-140">-IpRule</span></span>
<span data-ttu-id="1522f-141">防火牆支援。</span><span class="sxs-lookup"><span data-stu-id="1522f-141">Firewall support.</span></span> <span data-ttu-id="1522f-142">指定 CIDR 格式的 IP 位址或 IP 位址範圍的集合，以作為指定資料庫帳戶的允許用戶端 Ip 清單。</span><span class="sxs-lookup"><span data-stu-id="1522f-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="1522f-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="1522f-144">KeyVault 的 URI</span><span class="sxs-lookup"><span data-stu-id="1522f-144">URI of the KeyVault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1522f-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="1522f-146">在與限制失效的一致性搭配使用時，此值代表 timespan) 容許的過期 (時間量。</span><span class="sxs-lookup"><span data-stu-id="1522f-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="1522f-147">此值的接受範圍是5-86400。</span><span class="sxs-lookup"><span data-stu-id="1522f-147">Accepted range for this value is 5-86400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="1522f-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="1522f-149">在與限制失效的一致性搭配使用時，此值代表容許的過時要求數量。</span><span class="sxs-lookup"><span data-stu-id="1522f-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="1522f-150">此值的接受範圍為 1-2147483647。</span><span class="sxs-lookup"><span data-stu-id="1522f-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-151">-名稱</span><span class="sxs-lookup"><span data-stu-id="1522f-151">-Name</span></span>
<span data-ttu-id="1522f-152">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1522f-152">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="1522f-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="1522f-154">此伺服器是否允許公用端點存取。</span><span class="sxs-lookup"><span data-stu-id="1522f-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="1522f-155">可能的值包括：「已啟用」、「已停用」</span><span class="sxs-lookup"><span data-stu-id="1522f-155">Possible values include: 'Enabled', 'Disabled'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1522f-156">-ResourceGroupName</span></span>
<span data-ttu-id="1522f-157">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1522f-157">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1522f-158">-ResourceId</span></span>
<span data-ttu-id="1522f-159">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="1522f-159">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="1522f-160">-Tag</span></span>
<span data-ttu-id="1522f-161">以鍵值對的方式將標記 Hashtable 組成。</span><span class="sxs-lookup"><span data-stu-id="1522f-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="1522f-162">使用空字串清除現有標記。</span><span class="sxs-lookup"><span data-stu-id="1522f-162">Use empty string to clear existing tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-163">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1522f-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="1522f-164">虛擬網路 ACL 的字串值陣列。</span><span class="sxs-lookup"><span data-stu-id="1522f-164">Array of string values of ACL's for virtual network.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="1522f-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="1522f-166">虛擬網路的 PSVirtualNetworkRuleObjects 陣列。</span><span class="sxs-lookup"><span data-stu-id="1522f-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1522f-167">-WhatIf</span></span>
<span data-ttu-id="1522f-168">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1522f-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1522f-169">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1522f-169">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1522f-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1522f-170">CommonParameters</span></span>
<span data-ttu-id="1522f-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1522f-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1522f-172">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1522f-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1522f-173">輸入</span><span class="sxs-lookup"><span data-stu-id="1522f-173">INPUTS</span></span>

### <span data-ttu-id="1522f-174">PSCorsRule [] 的 CosmosDB []</span><span class="sxs-lookup"><span data-stu-id="1522f-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="1522f-175">輸出</span><span class="sxs-lookup"><span data-stu-id="1522f-175">OUTPUTS</span></span>

### <span data-ttu-id="1522f-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1522f-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="1522f-177">筆記</span><span class="sxs-lookup"><span data-stu-id="1522f-177">NOTES</span></span>

## <span data-ttu-id="1522f-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="1522f-178">RELATED LINKS</span></span>
