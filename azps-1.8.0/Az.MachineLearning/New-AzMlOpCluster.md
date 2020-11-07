---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
ms.openlocfilehash: 51c8beb396bb0795fa77431a256ddc38e4e8df38
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786946"
---
# <span data-ttu-id="f4321-101">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f4321-101">New-AzMlOpCluster</span></span>

## <span data-ttu-id="f4321-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4321-102">SYNOPSIS</span></span>
<span data-ttu-id="f4321-103">建立新的 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="f4321-103">Creates a new operationalization cluster.</span></span>

## <span data-ttu-id="f4321-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4321-104">SYNTAX</span></span>

### <span data-ttu-id="f4321-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="f4321-105">CreateWithInputObject</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4321-106">CreateWithParameters</span><span class="sxs-lookup"><span data-stu-id="f4321-106">CreateWithParameters</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4321-107">說明</span><span class="sxs-lookup"><span data-stu-id="f4321-107">DESCRIPTION</span></span>
<span data-ttu-id="f4321-108">建立新的 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="f4321-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="f4321-109">這將會建立群集物件、容器服務（如有需要）、應用程式深入資訊，以及 azure 容器註冊。</span><span class="sxs-lookup"><span data-stu-id="f4321-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="f4321-110">示例</span><span class="sxs-lookup"><span data-stu-id="f4321-110">EXAMPLES</span></span>

### <span data-ttu-id="f4321-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f4321-111">Example 1</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="f4321-112">使用 azure 容器服務和 Kubernetes 作為 orchestrator 來建立新的 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="f4321-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="f4321-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f4321-113">Example 2</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="f4321-114">在本機建立新的 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="f4321-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="f4321-115">這會建立 azure 容器 registry、application insights 及儲存空間帳戶，但不會建立容器服務。</span><span class="sxs-lookup"><span data-stu-id="f4321-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="f4321-116">參數</span><span class="sxs-lookup"><span data-stu-id="f4321-116">PARAMETERS</span></span>

### <span data-ttu-id="f4321-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="f4321-117">-AgentCount</span></span>
<span data-ttu-id="f4321-118">ACS 群集中的代理節點數目。</span><span class="sxs-lookup"><span data-stu-id="f4321-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="f4321-119">-AgentVmSize</span></span>
<span data-ttu-id="f4321-120">ACS 群集中的代理節點數目。</span><span class="sxs-lookup"><span data-stu-id="f4321-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f4321-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="f4321-122">要使用之 azure 容器註冊表的 URI，而不是建立一個。</span><span class="sxs-lookup"><span data-stu-id="f4321-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="f4321-123">-ClientId</span></span>
<span data-ttu-id="f4321-124">ACS 群集的 orchestrator service principal id。</span><span class="sxs-lookup"><span data-stu-id="f4321-124">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="f4321-125">-ClusterType</span></span>
<span data-ttu-id="f4321-126">Operationalization 群集類型。</span><span class="sxs-lookup"><span data-stu-id="f4321-126">The operationalization cluster type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4321-127">-DefaultProfile</span></span>
<span data-ttu-id="f4321-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4321-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4321-129">-描述</span><span class="sxs-lookup"><span data-stu-id="f4321-129">-Description</span></span>
<span data-ttu-id="f4321-130">ACS 群集中的主節點數目。</span><span class="sxs-lookup"><span data-stu-id="f4321-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="f4321-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="f4321-132">全域服務設定的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="f4321-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="f4321-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="f4321-134">用於更新的 ETag 設定。</span><span class="sxs-lookup"><span data-stu-id="f4321-134">The configuration ETag for updates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4321-135">-InputObject</span></span>
<span data-ttu-id="f4321-136">Operationalization 群集屬性。</span><span class="sxs-lookup"><span data-stu-id="f4321-136">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-137">-位置</span><span class="sxs-lookup"><span data-stu-id="f4321-137">-Location</span></span>
<span data-ttu-id="f4321-138">Operationalization 群集的位置。</span><span class="sxs-lookup"><span data-stu-id="f4321-138">The operationalization cluster's location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="f4321-139">-MasterCount</span></span>
<span data-ttu-id="f4321-140">ACS 群集中的主節點數目。</span><span class="sxs-lookup"><span data-stu-id="f4321-140">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4321-141">-Name</span></span>
<span data-ttu-id="f4321-142">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4321-142">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="f4321-143">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="f4321-143">-OrchestratorType</span></span>
<span data-ttu-id="f4321-144">ACS 群集的 orchestrator 類型。</span><span class="sxs-lookup"><span data-stu-id="f4321-144">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4321-145">-ResourceGroupName</span></span>
<span data-ttu-id="f4321-146">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4321-146">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="f4321-147">密碼</span><span class="sxs-lookup"><span data-stu-id="f4321-147">-Secret</span></span>
<span data-ttu-id="f4321-148">ACS 群集的 orchestrator service 主體密碼。</span><span class="sxs-lookup"><span data-stu-id="f4321-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="f4321-149">-SslCertificate</span></span>
<span data-ttu-id="f4321-150">PEM 格式的 SSL 憑證資料，以 base64 字串編碼。</span><span class="sxs-lookup"><span data-stu-id="f4321-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="f4321-151">-SslCName</span></span>
<span data-ttu-id="f4321-152">SSL 憑證的 CName。</span><span class="sxs-lookup"><span data-stu-id="f4321-152">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="f4321-153">-SslKey</span></span>
<span data-ttu-id="f4321-154">PEM 格式的 SSL 金鑰資料，以 base64 字串編碼。</span><span class="sxs-lookup"><span data-stu-id="f4321-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="f4321-155">-SslStatus</span></span>
<span data-ttu-id="f4321-156">SSL 狀態。</span><span class="sxs-lookup"><span data-stu-id="f4321-156">SSL status.</span></span>
<span data-ttu-id="f4321-157">可能的值為 [Enabled] 和 "Disabled"。</span><span class="sxs-lookup"><span data-stu-id="f4321-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4321-158">-StorageAccount</span></span>
<span data-ttu-id="f4321-159">要使用的儲存空間帳戶 URI，而不是建立一個。</span><span class="sxs-lookup"><span data-stu-id="f4321-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4321-160">-確認</span><span class="sxs-lookup"><span data-stu-id="f4321-160">-Confirm</span></span>
<span data-ttu-id="f4321-161">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4321-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4321-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4321-162">-WhatIf</span></span>
<span data-ttu-id="f4321-163">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4321-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4321-164">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4321-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4321-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4321-165">CommonParameters</span></span>
<span data-ttu-id="f4321-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4321-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4321-167">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4321-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4321-168">輸入</span><span class="sxs-lookup"><span data-stu-id="f4321-168">INPUTS</span></span>

### <span data-ttu-id="f4321-169">所有</span><span class="sxs-lookup"><span data-stu-id="f4321-169">None</span></span>

## <span data-ttu-id="f4321-170">輸出</span><span class="sxs-lookup"><span data-stu-id="f4321-170">OUTPUTS</span></span>

### <span data-ttu-id="f4321-171">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="f4321-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="f4321-172">筆記</span><span class="sxs-lookup"><span data-stu-id="f4321-172">NOTES</span></span>

## <span data-ttu-id="f4321-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4321-173">RELATED LINKS</span></span>
