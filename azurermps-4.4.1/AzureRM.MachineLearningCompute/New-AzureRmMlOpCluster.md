---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 222813dc78b4dd7c0118b8146a75ca4d225ce83c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452480"
---
# <span data-ttu-id="4567e-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4567e-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="4567e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4567e-102">SYNOPSIS</span></span>
<span data-ttu-id="4567e-103">建立新的 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="4567e-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4567e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4567e-104">SYNTAX</span></span>

### <span data-ttu-id="4567e-105">從 OperationalizationCluster 實例定義建立新的 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="4567e-105">Create a new operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4567e-106">從 Cmdlet 輸入參數建立新的 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="4567e-106">Create a new operationalization cluster from cmdlet input parameters.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <String>]
 [-Description <String>] [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-GlobalServiceConfigurationAdditionalProperties <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4567e-107">說明</span><span class="sxs-lookup"><span data-stu-id="4567e-107">DESCRIPTION</span></span>
<span data-ttu-id="4567e-108">建立新的 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="4567e-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="4567e-109">這將會建立群集物件、容器服務（如有需要）、應用程式深入資訊，以及 azure 容器註冊。</span><span class="sxs-lookup"><span data-stu-id="4567e-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="4567e-110">示例</span><span class="sxs-lookup"><span data-stu-id="4567e-110">EXAMPLES</span></span>

### <span data-ttu-id="4567e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4567e-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="4567e-112">使用 azure 容器服務和 Kubernetes 作為 orchestrator 來建立新的 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="4567e-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="4567e-113">範例2</span><span class="sxs-lookup"><span data-stu-id="4567e-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="4567e-114">在本機建立新的 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="4567e-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="4567e-115">這會建立 azure 容器 registry、application insights 及儲存空間帳戶，但不會建立容器服務。</span><span class="sxs-lookup"><span data-stu-id="4567e-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="4567e-116">參數</span><span class="sxs-lookup"><span data-stu-id="4567e-116">PARAMETERS</span></span>

### <span data-ttu-id="4567e-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="4567e-117">-AgentCount</span></span>
<span data-ttu-id="4567e-118">ACS 群集中的代理節點數目。</span><span class="sxs-lookup"><span data-stu-id="4567e-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="4567e-119">-AgentVmSize</span></span>
<span data-ttu-id="4567e-120">ACS 群集中的代理節點數目。</span><span class="sxs-lookup"><span data-stu-id="4567e-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4567e-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="4567e-122">要使用之 azure 容器註冊表的 URI，而不是建立一個。</span><span class="sxs-lookup"><span data-stu-id="4567e-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4567e-123">-InputObject</span></span>
<span data-ttu-id="4567e-124">Operationalization 群集屬性。</span><span class="sxs-lookup"><span data-stu-id="4567e-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Create a new operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="4567e-125">-ClusterType</span></span>
<span data-ttu-id="4567e-126">Operationalization 群集類型。</span><span class="sxs-lookup"><span data-stu-id="4567e-126">The operationalization cluster type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-127">-確認</span><span class="sxs-lookup"><span data-stu-id="4567e-127">-Confirm</span></span>
<span data-ttu-id="4567e-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4567e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4567e-129">-描述</span><span class="sxs-lookup"><span data-stu-id="4567e-129">-Description</span></span>
<span data-ttu-id="4567e-130">ACS 群集中的主節點數目。</span><span class="sxs-lookup"><span data-stu-id="4567e-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="4567e-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="4567e-132">全域服務設定的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="4567e-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="4567e-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="4567e-134">用於更新的 ETag 設定。</span><span class="sxs-lookup"><span data-stu-id="4567e-134">The configuration ETag for updates.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-135">-位置</span><span class="sxs-lookup"><span data-stu-id="4567e-135">-Location</span></span>
<span data-ttu-id="4567e-136">Operationalization 群集的位置。</span><span class="sxs-lookup"><span data-stu-id="4567e-136">The operationalization cluster's location.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-137">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="4567e-137">-MasterCount</span></span>
<span data-ttu-id="4567e-138">ACS 群集中的主節點數目。</span><span class="sxs-lookup"><span data-stu-id="4567e-138">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="4567e-139">-Name</span></span>
<span data-ttu-id="4567e-140">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="4567e-140">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-141">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="4567e-141">-OrchestratorType</span></span>
<span data-ttu-id="4567e-142">ACS 群集的 orchestrator 類型。</span><span class="sxs-lookup"><span data-stu-id="4567e-142">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4567e-143">-ResourceGroupName</span></span>
<span data-ttu-id="4567e-144">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4567e-144">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-145">-ClientId</span><span class="sxs-lookup"><span data-stu-id="4567e-145">-ClientId</span></span>
<span data-ttu-id="4567e-146">ACS 群集的 orchestrator service principal id。</span><span class="sxs-lookup"><span data-stu-id="4567e-146">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-147">密碼</span><span class="sxs-lookup"><span data-stu-id="4567e-147">-Secret</span></span>
<span data-ttu-id="4567e-148">ACS 群集的 orchestrator service 主體密碼。</span><span class="sxs-lookup"><span data-stu-id="4567e-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-149">-SslCName</span><span class="sxs-lookup"><span data-stu-id="4567e-149">-SslCName</span></span>
<span data-ttu-id="4567e-150">SSL 憑證的 CName。</span><span class="sxs-lookup"><span data-stu-id="4567e-150">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-151">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="4567e-151">-SslCertificate</span></span>
<span data-ttu-id="4567e-152">PEM 格式的 SSL 憑證資料，以 base64 字串編碼。</span><span class="sxs-lookup"><span data-stu-id="4567e-152">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="4567e-153">-SslKey</span></span>
<span data-ttu-id="4567e-154">PEM 格式的 SSL 金鑰資料，以 base64 字串編碼。</span><span class="sxs-lookup"><span data-stu-id="4567e-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="4567e-155">-SslStatus</span></span>
<span data-ttu-id="4567e-156">SSL 狀態。</span><span class="sxs-lookup"><span data-stu-id="4567e-156">SSL status.</span></span>
<span data-ttu-id="4567e-157">可能的值為 [Enabled] 和 "Disabled"。</span><span class="sxs-lookup"><span data-stu-id="4567e-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4567e-158">-StorageAccount</span></span>
<span data-ttu-id="4567e-159">要使用的儲存空間帳戶 URI，而不是建立一個。</span><span class="sxs-lookup"><span data-stu-id="4567e-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567e-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4567e-160">-WhatIf</span></span>
<span data-ttu-id="4567e-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4567e-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4567e-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4567e-162">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="4567e-163">輸入</span><span class="sxs-lookup"><span data-stu-id="4567e-163">INPUTS</span></span>

### <span data-ttu-id="4567e-164">所有</span><span class="sxs-lookup"><span data-stu-id="4567e-164">None</span></span>


## <span data-ttu-id="4567e-165">輸出</span><span class="sxs-lookup"><span data-stu-id="4567e-165">OUTPUTS</span></span>

### <span data-ttu-id="4567e-166">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="4567e-166">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="4567e-167">筆記</span><span class="sxs-lookup"><span data-stu-id="4567e-167">NOTES</span></span>

## <span data-ttu-id="4567e-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="4567e-168">RELATED LINKS</span></span>

