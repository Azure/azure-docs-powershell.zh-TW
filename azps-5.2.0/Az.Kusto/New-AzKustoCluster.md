---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b8b6c11da622b7fa0ee67dc418f2055dd72c1d13
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281636"
---
# <span data-ttu-id="7bd00-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="7bd00-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="7bd00-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7bd00-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd00-103">建立或更新 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="7bd00-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="7bd00-104">句法</span><span class="sxs-lookup"><span data-stu-id="7bd00-104">SYNTAX</span></span>

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

## <span data-ttu-id="7bd00-105">說明</span><span class="sxs-lookup"><span data-stu-id="7bd00-105">DESCRIPTION</span></span>
<span data-ttu-id="7bd00-106">建立或更新 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="7bd00-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="7bd00-107">示例</span><span class="sxs-lookup"><span data-stu-id="7bd00-107">EXAMPLES</span></span>

### <span data-ttu-id="7bd00-108">範例1：建立新的 Kusto 群集</span><span class="sxs-lookup"><span data-stu-id="7bd00-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="7bd00-109">上述命令會在資源群組 "testrg" 中建立名為 "testnewkustocluster" 的新 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="7bd00-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="7bd00-110">參數</span><span class="sxs-lookup"><span data-stu-id="7bd00-110">PARAMETERS</span></span>

### <span data-ttu-id="7bd00-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bd00-111">-AsJob</span></span>
<span data-ttu-id="7bd00-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="7bd00-112">Run the command as a job</span></span>

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

### <span data-ttu-id="7bd00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd00-113">-DefaultProfile</span></span>
<span data-ttu-id="7bd00-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7bd00-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bd00-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="7bd00-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="7bd00-116">布林值，指出群集的磁片是否已加密。</span><span class="sxs-lookup"><span data-stu-id="7bd00-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="7bd00-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="7bd00-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="7bd00-118">指示是否已啟用雙加密的布林值。</span><span class="sxs-lookup"><span data-stu-id="7bd00-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="7bd00-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="7bd00-119">-EnablePurge</span></span>
<span data-ttu-id="7bd00-120">指示是否已啟用清除作業的布林值。</span><span class="sxs-lookup"><span data-stu-id="7bd00-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="7bd00-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="7bd00-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="7bd00-122">指示是否已啟用流式攝取的布林值。</span><span class="sxs-lookup"><span data-stu-id="7bd00-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="7bd00-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7bd00-123">-IdentityType</span></span>
<span data-ttu-id="7bd00-124">身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="7bd00-124">The identity type.</span></span>

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

### <span data-ttu-id="7bd00-125">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7bd00-125">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="7bd00-126">與 Kusto 群集相關聯的使用者識別欄位表。</span><span class="sxs-lookup"><span data-stu-id="7bd00-126">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="7bd00-127">使用者身分識別字典金鑰參照會是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}」。</span><span class="sxs-lookup"><span data-stu-id="7bd00-127">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="7bd00-128">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="7bd00-128">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="7bd00-129">金鑰保存庫金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd00-129">The name of the key vault key.</span></span>

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

### <span data-ttu-id="7bd00-130">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="7bd00-130">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="7bd00-131">金鑰保存庫的 Uri。</span><span class="sxs-lookup"><span data-stu-id="7bd00-131">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="7bd00-132">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="7bd00-132">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="7bd00-133">金鑰保存庫金鑰的版本。</span><span class="sxs-lookup"><span data-stu-id="7bd00-133">The version of the key vault key.</span></span>

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

### <span data-ttu-id="7bd00-134">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="7bd00-134">-LanguageExtensionValue</span></span>
<span data-ttu-id="7bd00-135">語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="7bd00-135">The list of language extensions.</span></span>
<span data-ttu-id="7bd00-136">若要建立，請參閱 LANGUAGEEXTENSIONVALUE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="7bd00-136">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="7bd00-137">-位置</span><span class="sxs-lookup"><span data-stu-id="7bd00-137">-Location</span></span>
<span data-ttu-id="7bd00-138">資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="7bd00-138">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="7bd00-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="7bd00-139">-Name</span></span>
<span data-ttu-id="7bd00-140">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd00-140">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7bd00-141">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7bd00-141">-NoWait</span></span>
<span data-ttu-id="7bd00-142">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="7bd00-142">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7bd00-143">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="7bd00-143">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="7bd00-144">指示是否已啟用 [已優化自動縮放] 功能的布林值。</span><span class="sxs-lookup"><span data-stu-id="7bd00-144">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="7bd00-145">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="7bd00-145">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="7bd00-146">允許的最大實例數。</span><span class="sxs-lookup"><span data-stu-id="7bd00-146">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="7bd00-147">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="7bd00-147">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="7bd00-148">允許的最小實例數。</span><span class="sxs-lookup"><span data-stu-id="7bd00-148">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="7bd00-149">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="7bd00-149">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="7bd00-150">定義的範本版本，實例1。</span><span class="sxs-lookup"><span data-stu-id="7bd00-150">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="7bd00-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd00-151">-ResourceGroupName</span></span>
<span data-ttu-id="7bd00-152">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd00-152">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7bd00-153">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7bd00-153">-SkuCapacity</span></span>
<span data-ttu-id="7bd00-154">群集的實例數。</span><span class="sxs-lookup"><span data-stu-id="7bd00-154">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="7bd00-155">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7bd00-155">-SkuName</span></span>
<span data-ttu-id="7bd00-156">SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd00-156">SKU name.</span></span>

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

### <span data-ttu-id="7bd00-157">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="7bd00-157">-SkuTier</span></span>
<span data-ttu-id="7bd00-158">SKU 層。</span><span class="sxs-lookup"><span data-stu-id="7bd00-158">SKU tier.</span></span>

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

### <span data-ttu-id="7bd00-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7bd00-159">-SubscriptionId</span></span>
<span data-ttu-id="7bd00-160">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="7bd00-160">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7bd00-161">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="7bd00-161">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7bd00-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="7bd00-162">-Tag</span></span>
<span data-ttu-id="7bd00-163">資源標記。</span><span class="sxs-lookup"><span data-stu-id="7bd00-163">Resource tags.</span></span>

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

### <span data-ttu-id="7bd00-164">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="7bd00-164">-TrustedExternalTenant</span></span>
<span data-ttu-id="7bd00-165">群集的外部租使用者。</span><span class="sxs-lookup"><span data-stu-id="7bd00-165">The cluster's external tenants.</span></span>
<span data-ttu-id="7bd00-166">若要建立，請參閱 TRUSTEDEXTERNALTENANT 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="7bd00-166">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7bd00-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="7bd00-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="7bd00-168">資料管理的服務公用 IP 位址資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bd00-168">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="7bd00-169">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="7bd00-169">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="7bd00-170">引擎服務的公用 IP 位址資源 id。</span><span class="sxs-lookup"><span data-stu-id="7bd00-170">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="7bd00-171">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="7bd00-171">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="7bd00-172">子網資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bd00-172">The subnet resource id.</span></span>

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

### <span data-ttu-id="7bd00-173">-Zone</span><span class="sxs-lookup"><span data-stu-id="7bd00-173">-Zone</span></span>
<span data-ttu-id="7bd00-174">群集的可用性區域。</span><span class="sxs-lookup"><span data-stu-id="7bd00-174">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="7bd00-175">-確認</span><span class="sxs-lookup"><span data-stu-id="7bd00-175">-Confirm</span></span>
<span data-ttu-id="7bd00-176">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7bd00-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bd00-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bd00-177">-WhatIf</span></span>
<span data-ttu-id="7bd00-178">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7bd00-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bd00-179">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7bd00-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bd00-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd00-180">CommonParameters</span></span>
<span data-ttu-id="7bd00-181">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7bd00-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd00-182">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7bd00-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd00-183">輸入</span><span class="sxs-lookup"><span data-stu-id="7bd00-183">INPUTS</span></span>

## <span data-ttu-id="7bd00-184">輸出</span><span class="sxs-lookup"><span data-stu-id="7bd00-184">OUTPUTS</span></span>

### <span data-ttu-id="7bd00-185">ICluster （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="7bd00-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="7bd00-186">筆記</span><span class="sxs-lookup"><span data-stu-id="7bd00-186">NOTES</span></span>

<span data-ttu-id="7bd00-187">別名</span><span class="sxs-lookup"><span data-stu-id="7bd00-187">ALIASES</span></span>

<span data-ttu-id="7bd00-188">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="7bd00-188">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7bd00-189">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="7bd00-189">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7bd00-190">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="7bd00-190">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7bd00-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >：語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="7bd00-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="7bd00-192">`[Name <LanguageExtensionName?>]`：語言副檔名名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd00-192">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="7bd00-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >：群集的外部租使用者。</span><span class="sxs-lookup"><span data-stu-id="7bd00-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="7bd00-194">`[Value <String>]`：代表外部租使用者的 GUID。</span><span class="sxs-lookup"><span data-stu-id="7bd00-194">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="7bd00-195">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bd00-195">RELATED LINKS</span></span>

