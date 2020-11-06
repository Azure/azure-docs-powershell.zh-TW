---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: cbe72d14eac4864b784f31c4a800db09fc38b042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449075"
---
# <span data-ttu-id="c7f9f-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="c7f9f-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="c7f9f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7f9f-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f9f-103">設定 operationalization 群集的屬性。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7f9f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7f9f-104">SYNTAX</span></span>

### <span data-ttu-id="c7f9f-105">SetByIndividualParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="c7f9f-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7f9f-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c7f9f-106">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7f9f-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7f9f-107">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7f9f-108">說明</span><span class="sxs-lookup"><span data-stu-id="c7f9f-108">DESCRIPTION</span></span>
<span data-ttu-id="c7f9f-109">設定 operationalization 群集的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="c7f9f-110">因為它會在使用群集物件時設定所有屬性，所以必須傳遞完全有效的輸入物件。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="c7f9f-111">唯讀屬性將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="c7f9f-112">目前只有部分屬性可更新，如參數集中所示。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="c7f9f-113">示例</span><span class="sxs-lookup"><span data-stu-id="c7f9f-113">EXAMPLES</span></span>

### <span data-ttu-id="c7f9f-114">範例1</span><span class="sxs-lookup"><span data-stu-id="c7f9f-114">Example 1</span></span>
<span data-ttu-id="c7f9f-115">使用個別參數更新群集。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="c7f9f-116">範例2</span><span class="sxs-lookup"><span data-stu-id="c7f9f-116">Example 2</span></span>
<span data-ttu-id="c7f9f-117">使用輸入物件更新群集。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="c7f9f-118">參數</span><span class="sxs-lookup"><span data-stu-id="c7f9f-118">PARAMETERS</span></span>

### <span data-ttu-id="c7f9f-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="c7f9f-119">-AgentCount</span></span>
<span data-ttu-id="c7f9f-120">ACS 群集中的代理節點數目。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-120">The number of agent nodes in the ACS cluster.</span></span>

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

### <span data-ttu-id="c7f9f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f9f-121">-DefaultProfile</span></span>
<span data-ttu-id="c7f9f-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7f9f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7f9f-123">-InputObject</span></span>
<span data-ttu-id="c7f9f-124">Operationalization 群集屬性。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-124">The operationalization cluster properties.</span></span>

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

### <span data-ttu-id="c7f9f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7f9f-125">-Name</span></span>
<span data-ttu-id="c7f9f-126">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-126">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="c7f9f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7f9f-127">-ResourceGroupName</span></span>
<span data-ttu-id="c7f9f-128">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-128">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="c7f9f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7f9f-129">-ResourceId</span></span>
<span data-ttu-id="c7f9f-130">Operationalization 群集的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-130">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="c7f9f-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="c7f9f-131">-SslCertificate</span></span>
<span data-ttu-id="c7f9f-132">PEM 格式的 SSL 憑證資料。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-132">The SSL certificate data in PEM format.</span></span>

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

### <span data-ttu-id="c7f9f-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="c7f9f-133">-SslCName</span></span>
<span data-ttu-id="c7f9f-134">SSL 憑證的 CName。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-134">The CName for the SSL certificate.</span></span>

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

### <span data-ttu-id="c7f9f-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="c7f9f-135">-SslKey</span></span>
<span data-ttu-id="c7f9f-136">PEM 格式的 SSL 金鑰資料。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-136">The SSL key data in PEM format.</span></span>

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

### <span data-ttu-id="c7f9f-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="c7f9f-137">-SslStatus</span></span>
<span data-ttu-id="c7f9f-138">SSL 狀態。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-138">SSL status.</span></span>
<span data-ttu-id="c7f9f-139">可能的值為 [Enabled] 和 "Disabled"。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

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

### <span data-ttu-id="c7f9f-140">-確認</span><span class="sxs-lookup"><span data-stu-id="c7f9f-140">-Confirm</span></span>
<span data-ttu-id="c7f9f-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7f9f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7f9f-142">-WhatIf</span></span>
<span data-ttu-id="c7f9f-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7f9f-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7f9f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f9f-145">CommonParameters</span></span>
<span data-ttu-id="c7f9f-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f9f-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f9f-148">輸入</span><span class="sxs-lookup"><span data-stu-id="c7f9f-148">INPUTS</span></span>

### <span data-ttu-id="c7f9f-149">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="c7f9f-150">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c7f9f-150">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c7f9f-151">System.object</span><span class="sxs-lookup"><span data-stu-id="c7f9f-151">System.String</span></span>

### <span data-ttu-id="c7f9f-152">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c7f9f-152">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c7f9f-153">輸出</span><span class="sxs-lookup"><span data-stu-id="c7f9f-153">OUTPUTS</span></span>

### <span data-ttu-id="c7f9f-154">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="c7f9f-154">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="c7f9f-155">筆記</span><span class="sxs-lookup"><span data-stu-id="c7f9f-155">NOTES</span></span>

## <span data-ttu-id="c7f9f-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7f9f-156">RELATED LINKS</span></span>
