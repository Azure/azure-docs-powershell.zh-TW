---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: a3e1561feb470708420015bac1e2f0688f182896
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139164"
---
# <span data-ttu-id="f4efe-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="f4efe-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="f4efe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4efe-102">SYNOPSIS</span></span>
<span data-ttu-id="f4efe-103">更新 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="f4efe-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="f4efe-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4efe-104">SYNTAX</span></span>

### <span data-ttu-id="f4efe-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="f4efe-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f4efe-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f4efe-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f4efe-107">說明</span><span class="sxs-lookup"><span data-stu-id="f4efe-107">DESCRIPTION</span></span>
<span data-ttu-id="f4efe-108">更新 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="f4efe-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="f4efe-109">示例</span><span class="sxs-lookup"><span data-stu-id="f4efe-109">EXAMPLES</span></span>

### <span data-ttu-id="f4efe-110">範例1：依名稱更新現有的群集</span><span class="sxs-lookup"><span data-stu-id="f4efe-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="f4efe-111">上述命令會更新在資源群組 "testrg" 中找到的 Kusto 群集 "testnewkustocluster" 的 sku。</span><span class="sxs-lookup"><span data-stu-id="f4efe-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="f4efe-112">範例2：依名稱更新現有的群集</span><span class="sxs-lookup"><span data-stu-id="f4efe-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="f4efe-113">上述命令會使用客戶管理金鑰更新在資源群組 "testrg" 中找到的群集 "testnewkustocluster"。</span><span class="sxs-lookup"><span data-stu-id="f4efe-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="f4efe-114">參數</span><span class="sxs-lookup"><span data-stu-id="f4efe-114">PARAMETERS</span></span>

### <span data-ttu-id="f4efe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4efe-115">-AsJob</span></span>
<span data-ttu-id="f4efe-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="f4efe-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f4efe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4efe-117">-DefaultProfile</span></span>
<span data-ttu-id="f4efe-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4efe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4efe-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f4efe-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="f4efe-120">布林值，指出群集的磁片是否已加密。</span><span class="sxs-lookup"><span data-stu-id="f4efe-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="f4efe-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="f4efe-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="f4efe-122">指示是否已啟用雙加密的布林值。</span><span class="sxs-lookup"><span data-stu-id="f4efe-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="f4efe-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="f4efe-123">-EnablePurge</span></span>
<span data-ttu-id="f4efe-124">指示是否已啟用清除作業的布林值。</span><span class="sxs-lookup"><span data-stu-id="f4efe-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="f4efe-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="f4efe-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="f4efe-126">指示是否已啟用流式攝取的布林值。</span><span class="sxs-lookup"><span data-stu-id="f4efe-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="f4efe-127">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f4efe-127">-IdentityType</span></span>
<span data-ttu-id="f4efe-128">身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="f4efe-128">The identity type.</span></span>

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

### <span data-ttu-id="f4efe-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f4efe-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="f4efe-130">與 Kusto 群集相關聯的使用者識別欄位表。</span><span class="sxs-lookup"><span data-stu-id="f4efe-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="f4efe-131">使用者身分識別字典金鑰參照會是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}」。</span><span class="sxs-lookup"><span data-stu-id="f4efe-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="f4efe-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4efe-132">-InputObject</span></span>
<span data-ttu-id="f4efe-133">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f4efe-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4efe-134">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="f4efe-134">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="f4efe-135">金鑰保存庫金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4efe-135">The name of the key vault key.</span></span>

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

### <span data-ttu-id="f4efe-136">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="f4efe-136">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="f4efe-137">金鑰保存庫的 Uri。</span><span class="sxs-lookup"><span data-stu-id="f4efe-137">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="f4efe-138">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f4efe-138">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="f4efe-139">金鑰保存庫金鑰的版本。</span><span class="sxs-lookup"><span data-stu-id="f4efe-139">The version of the key vault key.</span></span>

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

### <span data-ttu-id="f4efe-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="f4efe-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="f4efe-141">語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="f4efe-141">The list of language extensions.</span></span>
<span data-ttu-id="f4efe-142">若要建立，請參閱 LANGUAGEEXTENSIONVALUE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="f4efe-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="f4efe-143">-位置</span><span class="sxs-lookup"><span data-stu-id="f4efe-143">-Location</span></span>
<span data-ttu-id="f4efe-144">資源位置。</span><span class="sxs-lookup"><span data-stu-id="f4efe-144">Resource location.</span></span>

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

### <span data-ttu-id="f4efe-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4efe-145">-Name</span></span>
<span data-ttu-id="f4efe-146">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4efe-146">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4efe-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f4efe-147">-NoWait</span></span>
<span data-ttu-id="f4efe-148">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="f4efe-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f4efe-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="f4efe-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="f4efe-150">指示是否已啟用 [已優化自動縮放] 功能的布林值。</span><span class="sxs-lookup"><span data-stu-id="f4efe-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="f4efe-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="f4efe-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="f4efe-152">允許的最大實例數。</span><span class="sxs-lookup"><span data-stu-id="f4efe-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="f4efe-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="f4efe-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="f4efe-154">允許的最小實例數。</span><span class="sxs-lookup"><span data-stu-id="f4efe-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="f4efe-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="f4efe-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="f4efe-156">定義的範本版本，實例1。</span><span class="sxs-lookup"><span data-stu-id="f4efe-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="f4efe-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4efe-157">-ResourceGroupName</span></span>
<span data-ttu-id="f4efe-158">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4efe-158">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4efe-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f4efe-159">-SkuCapacity</span></span>
<span data-ttu-id="f4efe-160">群集的實例數。</span><span class="sxs-lookup"><span data-stu-id="f4efe-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="f4efe-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f4efe-161">-SkuName</span></span>
<span data-ttu-id="f4efe-162">SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="f4efe-162">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4efe-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f4efe-163">-SkuTier</span></span>
<span data-ttu-id="f4efe-164">SKU 層。</span><span class="sxs-lookup"><span data-stu-id="f4efe-164">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4efe-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4efe-165">-SubscriptionId</span></span>
<span data-ttu-id="f4efe-166">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f4efe-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f4efe-167">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f4efe-167">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4efe-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4efe-168">-Tag</span></span>
<span data-ttu-id="f4efe-169">資源標記。</span><span class="sxs-lookup"><span data-stu-id="f4efe-169">Resource tags.</span></span>

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

### <span data-ttu-id="f4efe-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="f4efe-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="f4efe-171">群集的外部租使用者。</span><span class="sxs-lookup"><span data-stu-id="f4efe-171">The cluster's external tenants.</span></span>
<span data-ttu-id="f4efe-172">若要建立，請參閱 TRUSTEDEXTERNALTENANT 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="f4efe-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f4efe-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="f4efe-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="f4efe-174">資料管理的服務公用 IP 位址資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4efe-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="f4efe-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="f4efe-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="f4efe-176">引擎服務的公用 IP 位址資源 id。</span><span class="sxs-lookup"><span data-stu-id="f4efe-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="f4efe-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="f4efe-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="f4efe-178">子網資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4efe-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="f4efe-179">-確認</span><span class="sxs-lookup"><span data-stu-id="f4efe-179">-Confirm</span></span>
<span data-ttu-id="f4efe-180">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4efe-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4efe-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4efe-181">-WhatIf</span></span>
<span data-ttu-id="f4efe-182">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4efe-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4efe-183">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4efe-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4efe-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4efe-184">CommonParameters</span></span>
<span data-ttu-id="f4efe-185">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4efe-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4efe-186">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f4efe-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4efe-187">輸入</span><span class="sxs-lookup"><span data-stu-id="f4efe-187">INPUTS</span></span>

### <span data-ttu-id="f4efe-188">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="f4efe-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f4efe-189">輸出</span><span class="sxs-lookup"><span data-stu-id="f4efe-189">OUTPUTS</span></span>

### <span data-ttu-id="f4efe-190">ICluster （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="f4efe-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="f4efe-191">筆記</span><span class="sxs-lookup"><span data-stu-id="f4efe-191">NOTES</span></span>

<span data-ttu-id="f4efe-192">別名</span><span class="sxs-lookup"><span data-stu-id="f4efe-192">ALIASES</span></span>

<span data-ttu-id="f4efe-193">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f4efe-193">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4efe-194">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f4efe-194">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4efe-195">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f4efe-195">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4efe-196">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f4efe-196">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f4efe-197">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4efe-197">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f4efe-198">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4efe-198">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f4efe-199">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4efe-199">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f4efe-200">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4efe-200">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f4efe-201">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f4efe-201">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f4efe-202">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="f4efe-202">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f4efe-203">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4efe-203">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f4efe-204">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4efe-204">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f4efe-205">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f4efe-205">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f4efe-206">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f4efe-206">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="f4efe-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >：語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="f4efe-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="f4efe-208">`[Name <LanguageExtensionName?>]`：語言副檔名名稱。</span><span class="sxs-lookup"><span data-stu-id="f4efe-208">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="f4efe-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >：群集的外部租使用者。</span><span class="sxs-lookup"><span data-stu-id="f4efe-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="f4efe-210">`[Value <String>]`：代表外部租使用者的 GUID。</span><span class="sxs-lookup"><span data-stu-id="f4efe-210">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="f4efe-211">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4efe-211">RELATED LINKS</span></span>

