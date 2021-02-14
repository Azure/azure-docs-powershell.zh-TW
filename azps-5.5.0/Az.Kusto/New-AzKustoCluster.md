---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b868633f0217b2048f0a83641f678e9c092d21c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142991"
---
# <span data-ttu-id="8708d-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="8708d-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="8708d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8708d-102">SYNOPSIS</span></span>
<span data-ttu-id="8708d-103">建立或更新 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="8708d-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="8708d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8708d-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8708d-105">說明</span><span class="sxs-lookup"><span data-stu-id="8708d-105">DESCRIPTION</span></span>
<span data-ttu-id="8708d-106">建立或更新 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="8708d-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="8708d-107">示例</span><span class="sxs-lookup"><span data-stu-id="8708d-107">EXAMPLES</span></span>

### <span data-ttu-id="8708d-108">範例1：建立新的 Kusto 群集</span><span class="sxs-lookup"><span data-stu-id="8708d-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="8708d-109">上述命令會在資源群組 "testrg" 中建立名為 "testnewkustocluster" 的新 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="8708d-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="8708d-110">參數</span><span class="sxs-lookup"><span data-stu-id="8708d-110">PARAMETERS</span></span>

### <span data-ttu-id="8708d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8708d-111">-AsJob</span></span>
<span data-ttu-id="8708d-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="8708d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="8708d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8708d-113">-DefaultProfile</span></span>
<span data-ttu-id="8708d-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8708d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8708d-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="8708d-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="8708d-116">布林值，指出群集的磁片是否已加密。</span><span class="sxs-lookup"><span data-stu-id="8708d-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="8708d-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="8708d-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="8708d-118">指示是否已啟用雙加密的布林值。</span><span class="sxs-lookup"><span data-stu-id="8708d-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="8708d-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="8708d-119">-EnablePurge</span></span>
<span data-ttu-id="8708d-120">指示是否已啟用清除作業的布林值。</span><span class="sxs-lookup"><span data-stu-id="8708d-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="8708d-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="8708d-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="8708d-122">指示是否已啟用流式攝取的布林值。</span><span class="sxs-lookup"><span data-stu-id="8708d-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="8708d-123">-EngineType</span><span class="sxs-lookup"><span data-stu-id="8708d-123">-EngineType</span></span>
<span data-ttu-id="8708d-124">引擎類型</span><span class="sxs-lookup"><span data-stu-id="8708d-124">The engine type</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EngineType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8708d-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8708d-125">-IdentityType</span></span>
<span data-ttu-id="8708d-126">所使用的 managed 身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="8708d-126">The type of managed identity used.</span></span>
<span data-ttu-id="8708d-127">類型 "SystemAssigned，UserAssigned" 包括隱式建立的身分識別和一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="8708d-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="8708d-128">類型 "None" 將移除所有身分識別。</span><span class="sxs-lookup"><span data-stu-id="8708d-128">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="8708d-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8708d-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="8708d-130">與 Kusto 群集相關聯的使用者識別欄位表。</span><span class="sxs-lookup"><span data-stu-id="8708d-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="8708d-131">使用者身分識別字典金鑰參照會是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}」。</span><span class="sxs-lookup"><span data-stu-id="8708d-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="8708d-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="8708d-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="8708d-133">金鑰保存庫金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="8708d-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="8708d-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="8708d-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="8708d-135">金鑰保存庫的 Uri。</span><span class="sxs-lookup"><span data-stu-id="8708d-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="8708d-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="8708d-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="8708d-137">金鑰保存庫金鑰的版本。</span><span class="sxs-lookup"><span data-stu-id="8708d-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="8708d-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="8708d-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="8708d-139">使用者指派身分識別 (ARM 資源識別碼) 具有金鑰存取權。</span><span class="sxs-lookup"><span data-stu-id="8708d-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="8708d-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="8708d-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="8708d-141">語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="8708d-141">The list of language extensions.</span></span>
<span data-ttu-id="8708d-142">若要建立，請參閱 LANGUAGEEXTENSIONVALUE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="8708d-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8708d-143">-位置</span><span class="sxs-lookup"><span data-stu-id="8708d-143">-Location</span></span>
<span data-ttu-id="8708d-144">資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="8708d-144">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="8708d-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="8708d-145">-Name</span></span>
<span data-ttu-id="8708d-146">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="8708d-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="8708d-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8708d-147">-NoWait</span></span>
<span data-ttu-id="8708d-148">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="8708d-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8708d-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="8708d-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="8708d-150">指示是否已啟用 [已優化自動縮放] 功能的布林值。</span><span class="sxs-lookup"><span data-stu-id="8708d-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="8708d-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="8708d-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="8708d-152">允許的最大實例數。</span><span class="sxs-lookup"><span data-stu-id="8708d-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="8708d-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="8708d-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="8708d-154">允許的最小實例數。</span><span class="sxs-lookup"><span data-stu-id="8708d-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="8708d-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="8708d-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="8708d-156">定義的範本版本，實例1。</span><span class="sxs-lookup"><span data-stu-id="8708d-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="8708d-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8708d-157">-ResourceGroupName</span></span>
<span data-ttu-id="8708d-158">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8708d-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="8708d-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="8708d-159">-SkuCapacity</span></span>
<span data-ttu-id="8708d-160">群集的實例數。</span><span class="sxs-lookup"><span data-stu-id="8708d-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="8708d-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8708d-161">-SkuName</span></span>
<span data-ttu-id="8708d-162">SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="8708d-162">SKU name.</span></span>

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

### <span data-ttu-id="8708d-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8708d-163">-SkuTier</span></span>
<span data-ttu-id="8708d-164">SKU 層。</span><span class="sxs-lookup"><span data-stu-id="8708d-164">SKU tier.</span></span>

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

### <span data-ttu-id="8708d-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8708d-165">-SubscriptionId</span></span>
<span data-ttu-id="8708d-166">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="8708d-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8708d-167">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8708d-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8708d-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="8708d-168">-Tag</span></span>
<span data-ttu-id="8708d-169">資源標記。</span><span class="sxs-lookup"><span data-stu-id="8708d-169">Resource tags.</span></span>

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

### <span data-ttu-id="8708d-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="8708d-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="8708d-171">群集的外部租使用者。</span><span class="sxs-lookup"><span data-stu-id="8708d-171">The cluster's external tenants.</span></span>
<span data-ttu-id="8708d-172">若要建立，請參閱 TRUSTEDEXTERNALTENANT 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="8708d-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8708d-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="8708d-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="8708d-174">資料管理的服務公用 IP 位址資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8708d-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="8708d-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="8708d-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="8708d-176">引擎服務的公用 IP 位址資源 id。</span><span class="sxs-lookup"><span data-stu-id="8708d-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="8708d-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="8708d-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="8708d-178">子網資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8708d-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="8708d-179">-Zone</span><span class="sxs-lookup"><span data-stu-id="8708d-179">-Zone</span></span>
<span data-ttu-id="8708d-180">群集的可用性區域。</span><span class="sxs-lookup"><span data-stu-id="8708d-180">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="8708d-181">-確認</span><span class="sxs-lookup"><span data-stu-id="8708d-181">-Confirm</span></span>
<span data-ttu-id="8708d-182">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8708d-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8708d-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8708d-183">-WhatIf</span></span>
<span data-ttu-id="8708d-184">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8708d-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8708d-185">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8708d-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8708d-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8708d-186">CommonParameters</span></span>
<span data-ttu-id="8708d-187">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8708d-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8708d-188">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8708d-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8708d-189">輸入</span><span class="sxs-lookup"><span data-stu-id="8708d-189">INPUTS</span></span>

## <span data-ttu-id="8708d-190">輸出</span><span class="sxs-lookup"><span data-stu-id="8708d-190">OUTPUTS</span></span>

### <span data-ttu-id="8708d-191">ICluster （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="8708d-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="8708d-192">筆記</span><span class="sxs-lookup"><span data-stu-id="8708d-192">NOTES</span></span>

<span data-ttu-id="8708d-193">別名</span><span class="sxs-lookup"><span data-stu-id="8708d-193">ALIASES</span></span>

<span data-ttu-id="8708d-194">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8708d-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8708d-195">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8708d-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8708d-196">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8708d-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8708d-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >：語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="8708d-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="8708d-198">`[Name <LanguageExtensionName?>]`：語言副檔名名稱。</span><span class="sxs-lookup"><span data-stu-id="8708d-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="8708d-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >：群集的外部租使用者。</span><span class="sxs-lookup"><span data-stu-id="8708d-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="8708d-200">`[Value <String>]`：代表外部租使用者的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8708d-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="8708d-201">相關連結</span><span class="sxs-lookup"><span data-stu-id="8708d-201">RELATED LINKS</span></span>

