---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
ms.openlocfilehash: 0e673cd74d87cee990130c1fd58b9049eec9ff15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611893"
---
# <span data-ttu-id="49743-101">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="49743-101">Update-AzMlOpClusterSystemService</span></span>

## <span data-ttu-id="49743-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49743-102">SYNOPSIS</span></span>
<span data-ttu-id="49743-103">在 operationalization 群集的系統服務上開始更新。</span><span class="sxs-lookup"><span data-stu-id="49743-103">Starts an update on the operationalization cluster's system services.</span></span>

## <span data-ttu-id="49743-104">句法</span><span class="sxs-lookup"><span data-stu-id="49743-104">SYNTAX</span></span>

### <span data-ttu-id="49743-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="49743-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49743-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="49743-106">StartUpdateWithInputObject</span></span>
```
Update-AzMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49743-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="49743-107">StartUpdateWithResourceId</span></span>
```
Update-AzMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49743-108">說明</span><span class="sxs-lookup"><span data-stu-id="49743-108">DESCRIPTION</span></span>
<span data-ttu-id="49743-109">系統服務可以獨立于 operationalization 群集進行更新。</span><span class="sxs-lookup"><span data-stu-id="49743-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="49743-110">若要在系統服務上開始更新，請使用此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49743-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="49743-111">如果沒有可用的更新，更新仍會啟動並成功返回。</span><span class="sxs-lookup"><span data-stu-id="49743-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="49743-112">更新完成之後，就會報告它開始、完成及是否成功。</span><span class="sxs-lookup"><span data-stu-id="49743-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="49743-113">示例</span><span class="sxs-lookup"><span data-stu-id="49743-113">EXAMPLES</span></span>

### <span data-ttu-id="49743-114">範例1</span><span class="sxs-lookup"><span data-stu-id="49743-114">Example 1</span></span>
```
PS C:\> Update-AzMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="49743-115">在指定的群集上啟動系統服務更新。</span><span class="sxs-lookup"><span data-stu-id="49743-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="49743-116">參數</span><span class="sxs-lookup"><span data-stu-id="49743-116">PARAMETERS</span></span>

### <span data-ttu-id="49743-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49743-117">-DefaultProfile</span></span>
<span data-ttu-id="49743-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49743-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49743-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49743-119">-InputObject</span></span>
<span data-ttu-id="49743-120">Operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="49743-120">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49743-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="49743-121">-Name</span></span>
<span data-ttu-id="49743-122">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="49743-122">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49743-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49743-123">-ResourceGroupName</span></span>
<span data-ttu-id="49743-124">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="49743-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49743-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49743-125">-ResourceId</span></span>
<span data-ttu-id="49743-126">Operationalization 群集的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="49743-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49743-127">-確認</span><span class="sxs-lookup"><span data-stu-id="49743-127">-Confirm</span></span>
<span data-ttu-id="49743-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="49743-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49743-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49743-129">-WhatIf</span></span>
<span data-ttu-id="49743-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49743-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49743-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49743-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49743-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49743-132">CommonParameters</span></span>
<span data-ttu-id="49743-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49743-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49743-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49743-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49743-135">輸入</span><span class="sxs-lookup"><span data-stu-id="49743-135">INPUTS</span></span>

### <span data-ttu-id="49743-136">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="49743-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="49743-137">System.object</span><span class="sxs-lookup"><span data-stu-id="49743-137">System.String</span></span>

## <span data-ttu-id="49743-138">輸出</span><span class="sxs-lookup"><span data-stu-id="49743-138">OUTPUTS</span></span>

### <span data-ttu-id="49743-139">PSUpdateSystemServicesResponse 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="49743-139">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="49743-140">筆記</span><span class="sxs-lookup"><span data-stu-id="49743-140">NOTES</span></span>

## <span data-ttu-id="49743-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="49743-141">RELATED LINKS</span></span>
