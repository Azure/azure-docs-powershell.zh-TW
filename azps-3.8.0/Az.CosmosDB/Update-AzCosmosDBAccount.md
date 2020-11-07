---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: a31df71a1242f4f4e9eb01a37d31eb54ec874a99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956494"
---
# <span data-ttu-id="74d4d-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="74d4d-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="74d4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="74d4d-103">更新 CosmosDB 帳戶屬性。</span><span class="sxs-lookup"><span data-stu-id="74d4d-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="74d4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="74d4d-104">SYNTAX</span></span>

### <span data-ttu-id="74d4d-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="74d4d-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74d4d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74d4d-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74d4d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74d4d-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74d4d-108">說明</span><span class="sxs-lookup"><span data-stu-id="74d4d-108">DESCRIPTION</span></span>
<span data-ttu-id="74d4d-109">更新 CosmosDB 帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="74d4d-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="74d4d-110">無法使用其他屬性來更新帳戶區域 simulataneously。</span><span class="sxs-lookup"><span data-stu-id="74d4d-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="74d4d-111">示例</span><span class="sxs-lookup"><span data-stu-id="74d4d-111">EXAMPLES</span></span>

### <span data-ttu-id="74d4d-112">範例1</span><span class="sxs-lookup"><span data-stu-id="74d4d-112">Example 1</span></span>
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

<span data-ttu-id="74d4d-113">已將 DefaultConsistencyLevel 更新為「強勁」、啟用 AutomaticFailover、啟用 MultipleWriteLocations，並啟用 VirtualNetwork 的 CosmosDB 帳戶具有名稱 accountName。</span><span class="sxs-lookup"><span data-stu-id="74d4d-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="74d4d-114">參數</span><span class="sxs-lookup"><span data-stu-id="74d4d-114">PARAMETERS</span></span>

### <span data-ttu-id="74d4d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74d4d-115">-AsJob</span></span>
<span data-ttu-id="74d4d-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="74d4d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74d4d-117">-確認</span><span class="sxs-lookup"><span data-stu-id="74d4d-117">-Confirm</span></span>
<span data-ttu-id="74d4d-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74d4d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74d4d-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="74d4d-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="74d4d-120">Cosmos DB 資料庫帳戶的預設一致性等級。</span><span class="sxs-lookup"><span data-stu-id="74d4d-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="74d4d-121">已接受的值： BoundedStaleness、ConsistentPrefix、最終、會話、強</span><span class="sxs-lookup"><span data-stu-id="74d4d-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="74d4d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d4d-122">-DefaultProfile</span></span>
<span data-ttu-id="74d4d-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74d4d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74d4d-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="74d4d-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="74d4d-125">在中繼資料資源 (資料庫、容器、透過帳戶金鑰) 的輸送量中停用寫入作業</span><span class="sxs-lookup"><span data-stu-id="74d4d-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="74d4d-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="74d4d-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="74d4d-127">在由於中斷而無法使用區域的極少事件中，啟用寫入區域的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="74d4d-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="74d4d-128">自動容錯移轉會針對該帳戶產生新的寫入區域，並根據針對該帳戶所設定的容錯移轉優先順序來選取。</span><span class="sxs-lookup"><span data-stu-id="74d4d-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="74d4d-129">已接受的值： false、true</span><span class="sxs-lookup"><span data-stu-id="74d4d-129">Accepted values: false, true</span></span>

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

### <span data-ttu-id="74d4d-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="74d4d-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="74d4d-131">啟用多個寫位置。</span><span class="sxs-lookup"><span data-stu-id="74d4d-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="74d4d-132">已接受的值： false、true</span><span class="sxs-lookup"><span data-stu-id="74d4d-132">Accepted values: false, true</span></span>

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

### <span data-ttu-id="74d4d-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="74d4d-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="74d4d-134">在 Cosmos DB 資料庫帳戶上啟用虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="74d4d-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="74d4d-135">已接受的值： false、true</span><span class="sxs-lookup"><span data-stu-id="74d4d-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="74d4d-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74d4d-136">-InputObject</span></span>
<span data-ttu-id="74d4d-137">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="74d4d-137">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74d4d-138">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="74d4d-138">-IpRangeFilter</span></span>
<span data-ttu-id="74d4d-139">防火牆支援。</span><span class="sxs-lookup"><span data-stu-id="74d4d-139">Firewall support.</span></span>
<span data-ttu-id="74d4d-140">指定 CIDR 形式的 IP 位址或 IP 位址範圍集合，以作為指定資料庫帳戶的允許用戶端 Ip 清單</span><span class="sxs-lookup"><span data-stu-id="74d4d-140">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="74d4d-141">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="74d4d-141">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="74d4d-142">在與限制失效的一致性搭配使用時，此值代表 timespan) 容許的過期 (時間量。</span><span class="sxs-lookup"><span data-stu-id="74d4d-142">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="74d4d-143">此值的接受範圍是5-86400。</span><span class="sxs-lookup"><span data-stu-id="74d4d-143">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="74d4d-144">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="74d4d-144">-MaxStalenessPrefix</span></span>
<span data-ttu-id="74d4d-145">在與限制失效的一致性搭配使用時，此值代表容許的過時要求數量。</span><span class="sxs-lookup"><span data-stu-id="74d4d-145">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="74d4d-146">此值的接受範圍為 1-2147483647。</span><span class="sxs-lookup"><span data-stu-id="74d4d-146">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="74d4d-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="74d4d-147">-Name</span></span>
<span data-ttu-id="74d4d-148">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="74d4d-148">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="74d4d-149">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="74d4d-149">-PublicNetworkAccess</span></span>
<span data-ttu-id="74d4d-150">此伺服器是否允許公用端點存取。</span><span class="sxs-lookup"><span data-stu-id="74d4d-150">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="74d4d-151">可能的值包括：「已啟用」、「已停用」</span><span class="sxs-lookup"><span data-stu-id="74d4d-151">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="74d4d-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74d4d-152">-ResourceGroupName</span></span>
<span data-ttu-id="74d4d-153">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="74d4d-153">Name of resource group.</span></span>

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

### <span data-ttu-id="74d4d-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74d4d-154">-ResourceId</span></span>
<span data-ttu-id="74d4d-155">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="74d4d-155">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="74d4d-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="74d4d-156">-Tag</span></span>
<span data-ttu-id="74d4d-157">以鍵值對的方式將標記 Hashtable 組成。</span><span class="sxs-lookup"><span data-stu-id="74d4d-157">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="74d4d-158">使用空字串清除現有標記。</span><span class="sxs-lookup"><span data-stu-id="74d4d-158">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="74d4d-159">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="74d4d-159">-VirtualNetworkRule</span></span>
<span data-ttu-id="74d4d-160">虛擬網路 ACL 的字串值陣列。</span><span class="sxs-lookup"><span data-stu-id="74d4d-160">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="74d4d-161">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="74d4d-161">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="74d4d-162">虛擬網路的 PSVirtualNetworkRuleObjects 陣列。</span><span class="sxs-lookup"><span data-stu-id="74d4d-162">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74d4d-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74d4d-163">-WhatIf</span></span>
<span data-ttu-id="74d4d-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74d4d-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74d4d-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74d4d-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74d4d-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d4d-166">CommonParameters</span></span>
<span data-ttu-id="74d4d-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74d4d-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d4d-168">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="74d4d-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d4d-169">輸入</span><span class="sxs-lookup"><span data-stu-id="74d4d-169">INPUTS</span></span>

### <span data-ttu-id="74d4d-170">PSCorsRule [] 的 CosmosDB []</span><span class="sxs-lookup"><span data-stu-id="74d4d-170">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="74d4d-171">輸出</span><span class="sxs-lookup"><span data-stu-id="74d4d-171">OUTPUTS</span></span>

### <span data-ttu-id="74d4d-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="74d4d-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="74d4d-173">筆記</span><span class="sxs-lookup"><span data-stu-id="74d4d-173">NOTES</span></span>

## <span data-ttu-id="74d4d-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="74d4d-174">RELATED LINKS</span></span>
