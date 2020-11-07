---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/set-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
ms.openlocfilehash: 833b3456cd39e4589ceaf37e0c86fd654c250ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786921"
---
# <span data-ttu-id="277da-101">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="277da-101">Set-AzMlOpCluster</span></span>

## <span data-ttu-id="277da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="277da-102">SYNOPSIS</span></span>
<span data-ttu-id="277da-103">設定 operationalization 群集的屬性。</span><span class="sxs-lookup"><span data-stu-id="277da-103">Sets the properties of an operationalization cluster.</span></span>

## <span data-ttu-id="277da-104">句法</span><span class="sxs-lookup"><span data-stu-id="277da-104">SYNTAX</span></span>

### <span data-ttu-id="277da-105">SetByIndividualParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="277da-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="277da-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="277da-106">SetByInputObject</span></span>
```
Set-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="277da-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="277da-107">SetByResourceId</span></span>
```
Set-AzMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>] [-SslCertificate <String>]
 [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="277da-108">說明</span><span class="sxs-lookup"><span data-stu-id="277da-108">DESCRIPTION</span></span>
<span data-ttu-id="277da-109">設定 operationalization 群集的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="277da-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="277da-110">因為它會在使用群集物件時設定所有屬性，所以必須傳遞完全有效的輸入物件。</span><span class="sxs-lookup"><span data-stu-id="277da-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="277da-111">唯讀屬性將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="277da-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="277da-112">目前只有部分屬性可更新，如參數集中所示。</span><span class="sxs-lookup"><span data-stu-id="277da-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="277da-113">示例</span><span class="sxs-lookup"><span data-stu-id="277da-113">EXAMPLES</span></span>

### <span data-ttu-id="277da-114">範例1</span><span class="sxs-lookup"><span data-stu-id="277da-114">Example 1</span></span>
<span data-ttu-id="277da-115">使用個別參數更新群集。</span><span class="sxs-lookup"><span data-stu-id="277da-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="277da-116">範例2</span><span class="sxs-lookup"><span data-stu-id="277da-116">Example 2</span></span>
<span data-ttu-id="277da-117">使用輸入物件更新群集。</span><span class="sxs-lookup"><span data-stu-id="277da-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="277da-118">參數</span><span class="sxs-lookup"><span data-stu-id="277da-118">PARAMETERS</span></span>

### <span data-ttu-id="277da-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="277da-119">-AgentCount</span></span>
<span data-ttu-id="277da-120">ACS 群集中的代理節點數目。</span><span class="sxs-lookup"><span data-stu-id="277da-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277da-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="277da-121">-DefaultProfile</span></span>
<span data-ttu-id="277da-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="277da-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="277da-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="277da-123">-InputObject</span></span>
<span data-ttu-id="277da-124">Operationalization 群集屬性。</span><span class="sxs-lookup"><span data-stu-id="277da-124">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="277da-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="277da-125">-Name</span></span>
<span data-ttu-id="277da-126">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="277da-126">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="277da-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="277da-127">-ResourceGroupName</span></span>
<span data-ttu-id="277da-128">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="277da-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="277da-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="277da-129">-ResourceId</span></span>
<span data-ttu-id="277da-130">Operationalization 群集的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="277da-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277da-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="277da-131">-SslCertificate</span></span>
<span data-ttu-id="277da-132">PEM 格式的 SSL 憑證資料。</span><span class="sxs-lookup"><span data-stu-id="277da-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277da-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="277da-133">-SslCName</span></span>
<span data-ttu-id="277da-134">SSL 憑證的 CName。</span><span class="sxs-lookup"><span data-stu-id="277da-134">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277da-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="277da-135">-SslKey</span></span>
<span data-ttu-id="277da-136">PEM 格式的 SSL 金鑰資料。</span><span class="sxs-lookup"><span data-stu-id="277da-136">The SSL key data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277da-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="277da-137">-SslStatus</span></span>
<span data-ttu-id="277da-138">SSL 狀態。</span><span class="sxs-lookup"><span data-stu-id="277da-138">SSL status.</span></span>
<span data-ttu-id="277da-139">可能的值為 [Enabled] 和 "Disabled"。</span><span class="sxs-lookup"><span data-stu-id="277da-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277da-140">-確認</span><span class="sxs-lookup"><span data-stu-id="277da-140">-Confirm</span></span>
<span data-ttu-id="277da-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="277da-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="277da-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="277da-142">-WhatIf</span></span>
<span data-ttu-id="277da-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="277da-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="277da-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="277da-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="277da-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="277da-145">CommonParameters</span></span>
<span data-ttu-id="277da-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="277da-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="277da-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="277da-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="277da-148">輸入</span><span class="sxs-lookup"><span data-stu-id="277da-148">INPUTS</span></span>

### <span data-ttu-id="277da-149">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="277da-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="277da-150">System.object</span><span class="sxs-lookup"><span data-stu-id="277da-150">System.String</span></span>

### <span data-ttu-id="277da-151">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="277da-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="277da-152">輸出</span><span class="sxs-lookup"><span data-stu-id="277da-152">OUTPUTS</span></span>

### <span data-ttu-id="277da-153">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="277da-153">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="277da-154">筆記</span><span class="sxs-lookup"><span data-stu-id="277da-154">NOTES</span></span>

## <span data-ttu-id="277da-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="277da-155">RELATED LINKS</span></span>
