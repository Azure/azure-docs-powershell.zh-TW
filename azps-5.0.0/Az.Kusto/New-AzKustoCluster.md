---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b8b6c11da622b7fa0ee67dc418f2055dd72c1d13
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140442"
---
# <span data-ttu-id="1ae24-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="1ae24-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="1ae24-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ae24-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae24-103">建立或更新 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="1ae24-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="1ae24-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ae24-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1ae24-105">說明</span><span class="sxs-lookup"><span data-stu-id="1ae24-105">DESCRIPTION</span></span>
<span data-ttu-id="1ae24-106">建立或更新 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="1ae24-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="1ae24-107">示例</span><span class="sxs-lookup"><span data-stu-id="1ae24-107">EXAMPLES</span></span>

### <span data-ttu-id="1ae24-108">範例1：建立新的 Kusto 群集</span><span class="sxs-lookup"><span data-stu-id="1ae24-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="1ae24-109">上述命令會在資源群組 "testrg" 中建立名為 "testnewkustocluster" 的新 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="1ae24-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="1ae24-110">參數</span><span class="sxs-lookup"><span data-stu-id="1ae24-110">PARAMETERS</span></span>

### <span data-ttu-id="1ae24-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ae24-111">-AsJob</span></span>
<span data-ttu-id="1ae24-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="1ae24-112">Run the command as a job</span></span>

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

### <span data-ttu-id="1ae24-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae24-113">-DefaultProfile</span></span>
<span data-ttu-id="1ae24-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ae24-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="1ae24-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="1ae24-116">布林值，指出群集的磁片是否已加密。</span><span class="sxs-lookup"><span data-stu-id="1ae24-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="1ae24-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="1ae24-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="1ae24-118">指示是否已啟用雙加密的布林值。</span><span class="sxs-lookup"><span data-stu-id="1ae24-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="1ae24-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="1ae24-119">-EnablePurge</span></span>
<span data-ttu-id="1ae24-120">指示是否已啟用清除作業的布林值。</span><span class="sxs-lookup"><span data-stu-id="1ae24-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="1ae24-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="1ae24-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="1ae24-122">指示是否已啟用流式攝取的布林值。</span><span class="sxs-lookup"><span data-stu-id="1ae24-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="1ae24-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="1ae24-123">-IdentityType</span></span>
<span data-ttu-id="1ae24-124">身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="1ae24-124">The identity type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-125">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1ae24-125">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="1ae24-126">與 Kusto 群集相關聯的使用者識別欄位表。</span><span class="sxs-lookup"><span data-stu-id="1ae24-126">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="1ae24-127">使用者身分識別字典金鑰參照會是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}」。</span><span class="sxs-lookup"><span data-stu-id="1ae24-127">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-128">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="1ae24-128">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="1ae24-129">金鑰保存庫金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae24-129">The name of the key vault key.</span></span>

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

### <span data-ttu-id="1ae24-130">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="1ae24-130">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="1ae24-131">金鑰保存庫的 Uri。</span><span class="sxs-lookup"><span data-stu-id="1ae24-131">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="1ae24-132">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="1ae24-132">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="1ae24-133">金鑰保存庫金鑰的版本。</span><span class="sxs-lookup"><span data-stu-id="1ae24-133">The version of the key vault key.</span></span>

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

### <span data-ttu-id="1ae24-134">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="1ae24-134">-LanguageExtensionValue</span></span>
<span data-ttu-id="1ae24-135">語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="1ae24-135">The list of language extensions.</span></span>
<span data-ttu-id="1ae24-136">若要建立，請參閱 LANGUAGEEXTENSIONVALUE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="1ae24-136">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-137">-位置</span><span class="sxs-lookup"><span data-stu-id="1ae24-137">-Location</span></span>
<span data-ttu-id="1ae24-138">資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="1ae24-138">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ae24-139">-Name</span></span>
<span data-ttu-id="1ae24-140">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae24-140">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-141">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1ae24-141">-NoWait</span></span>
<span data-ttu-id="1ae24-142">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="1ae24-142">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1ae24-143">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="1ae24-143">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="1ae24-144">指示是否已啟用 [已優化自動縮放] 功能的布林值。</span><span class="sxs-lookup"><span data-stu-id="1ae24-144">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="1ae24-145">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="1ae24-145">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="1ae24-146">允許的最大實例數。</span><span class="sxs-lookup"><span data-stu-id="1ae24-146">Maximum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-147">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="1ae24-147">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="1ae24-148">允許的最小實例數。</span><span class="sxs-lookup"><span data-stu-id="1ae24-148">Minimum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-149">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="1ae24-149">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="1ae24-150">定義的範本版本，實例1。</span><span class="sxs-lookup"><span data-stu-id="1ae24-150">The version of the template defined, for instance 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae24-151">-ResourceGroupName</span></span>
<span data-ttu-id="1ae24-152">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae24-152">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-153">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="1ae24-153">-SkuCapacity</span></span>
<span data-ttu-id="1ae24-154">群集的實例數。</span><span class="sxs-lookup"><span data-stu-id="1ae24-154">The number of instances of the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-155">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1ae24-155">-SkuName</span></span>
<span data-ttu-id="1ae24-156">SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae24-156">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-157">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="1ae24-157">-SkuTier</span></span>
<span data-ttu-id="1ae24-158">SKU 層。</span><span class="sxs-lookup"><span data-stu-id="1ae24-158">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ae24-159">-SubscriptionId</span></span>
<span data-ttu-id="1ae24-160">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="1ae24-160">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1ae24-161">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="1ae24-161">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="1ae24-162">-Tag</span></span>
<span data-ttu-id="1ae24-163">資源標記。</span><span class="sxs-lookup"><span data-stu-id="1ae24-163">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-164">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="1ae24-164">-TrustedExternalTenant</span></span>
<span data-ttu-id="1ae24-165">群集的外部租使用者。</span><span class="sxs-lookup"><span data-stu-id="1ae24-165">The cluster's external tenants.</span></span>
<span data-ttu-id="1ae24-166">若要建立，請參閱 TRUSTEDEXTERNALTENANT 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="1ae24-166">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="1ae24-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="1ae24-168">資料管理的服務公用 IP 位址資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ae24-168">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="1ae24-169">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="1ae24-169">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="1ae24-170">引擎服務的公用 IP 位址資源 id。</span><span class="sxs-lookup"><span data-stu-id="1ae24-170">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="1ae24-171">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="1ae24-171">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="1ae24-172">子網資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ae24-172">The subnet resource id.</span></span>

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

### <span data-ttu-id="1ae24-173">-Zone</span><span class="sxs-lookup"><span data-stu-id="1ae24-173">-Zone</span></span>
<span data-ttu-id="1ae24-174">群集的可用性區域。</span><span class="sxs-lookup"><span data-stu-id="1ae24-174">The availability zones of the cluster.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae24-175">-確認</span><span class="sxs-lookup"><span data-stu-id="1ae24-175">-Confirm</span></span>
<span data-ttu-id="1ae24-176">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1ae24-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ae24-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ae24-177">-WhatIf</span></span>
<span data-ttu-id="1ae24-178">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ae24-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ae24-179">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ae24-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ae24-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae24-180">CommonParameters</span></span>
<span data-ttu-id="1ae24-181">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ae24-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae24-182">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1ae24-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae24-183">輸入</span><span class="sxs-lookup"><span data-stu-id="1ae24-183">INPUTS</span></span>

## <span data-ttu-id="1ae24-184">輸出</span><span class="sxs-lookup"><span data-stu-id="1ae24-184">OUTPUTS</span></span>

### <span data-ttu-id="1ae24-185">ICluster （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="1ae24-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="1ae24-186">筆記</span><span class="sxs-lookup"><span data-stu-id="1ae24-186">NOTES</span></span>

<span data-ttu-id="1ae24-187">別名</span><span class="sxs-lookup"><span data-stu-id="1ae24-187">ALIASES</span></span>

<span data-ttu-id="1ae24-188">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="1ae24-188">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ae24-189">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="1ae24-189">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ae24-190">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="1ae24-190">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ae24-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >：語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="1ae24-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="1ae24-192">`[Name <LanguageExtensionName?>]`：語言副檔名名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae24-192">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="1ae24-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >：群集的外部租使用者。</span><span class="sxs-lookup"><span data-stu-id="1ae24-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="1ae24-194">`[Value <String>]`：代表外部租使用者的 GUID。</span><span class="sxs-lookup"><span data-stu-id="1ae24-194">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="1ae24-195">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ae24-195">RELATED LINKS</span></span>

