---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/update-azurermmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: 042c857efde915847e8ad809e84c91ddaa103b66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449073"
---
# <span data-ttu-id="9cb34-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="9cb34-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="9cb34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9cb34-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb34-103">在 operationalization 群集的系統服務上開始更新。</span><span class="sxs-lookup"><span data-stu-id="9cb34-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cb34-104">句法</span><span class="sxs-lookup"><span data-stu-id="9cb34-104">SYNTAX</span></span>

### <span data-ttu-id="9cb34-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9cb34-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb34-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="9cb34-106">StartUpdateWithInputObject</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb34-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="9cb34-107">StartUpdateWithResourceId</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cb34-108">說明</span><span class="sxs-lookup"><span data-stu-id="9cb34-108">DESCRIPTION</span></span>
<span data-ttu-id="9cb34-109">系統服務可以獨立于 operationalization 群集進行更新。</span><span class="sxs-lookup"><span data-stu-id="9cb34-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="9cb34-110">若要在系統服務上開始更新，請使用此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9cb34-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="9cb34-111">如果沒有可用的更新，更新仍會啟動並成功返回。</span><span class="sxs-lookup"><span data-stu-id="9cb34-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="9cb34-112">更新完成之後，就會報告它開始、完成及是否成功。</span><span class="sxs-lookup"><span data-stu-id="9cb34-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="9cb34-113">示例</span><span class="sxs-lookup"><span data-stu-id="9cb34-113">EXAMPLES</span></span>

### <span data-ttu-id="9cb34-114">範例1</span><span class="sxs-lookup"><span data-stu-id="9cb34-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="9cb34-115">在指定的群集上啟動系統服務更新。</span><span class="sxs-lookup"><span data-stu-id="9cb34-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="9cb34-116">參數</span><span class="sxs-lookup"><span data-stu-id="9cb34-116">PARAMETERS</span></span>

### <span data-ttu-id="9cb34-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb34-117">-DefaultProfile</span></span>
<span data-ttu-id="9cb34-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9cb34-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cb34-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cb34-119">-InputObject</span></span>
<span data-ttu-id="9cb34-120">Operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="9cb34-120">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="9cb34-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9cb34-121">-Name</span></span>
<span data-ttu-id="9cb34-122">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cb34-122">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="9cb34-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb34-123">-ResourceGroupName</span></span>
<span data-ttu-id="9cb34-124">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cb34-124">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="9cb34-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cb34-125">-ResourceId</span></span>
<span data-ttu-id="9cb34-126">Operationalization 群集的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="9cb34-126">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="9cb34-127">-確認</span><span class="sxs-lookup"><span data-stu-id="9cb34-127">-Confirm</span></span>
<span data-ttu-id="9cb34-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9cb34-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cb34-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb34-129">-WhatIf</span></span>
<span data-ttu-id="9cb34-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9cb34-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cb34-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9cb34-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cb34-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb34-132">CommonParameters</span></span>
<span data-ttu-id="9cb34-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9cb34-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb34-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9cb34-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb34-135">輸入</span><span class="sxs-lookup"><span data-stu-id="9cb34-135">INPUTS</span></span>

### <span data-ttu-id="9cb34-136">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="9cb34-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="9cb34-137">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9cb34-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9cb34-138">System.object</span><span class="sxs-lookup"><span data-stu-id="9cb34-138">System.String</span></span>

## <span data-ttu-id="9cb34-139">輸出</span><span class="sxs-lookup"><span data-stu-id="9cb34-139">OUTPUTS</span></span>

### <span data-ttu-id="9cb34-140">PSUpdateSystemServicesResponse 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="9cb34-140">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="9cb34-141">筆記</span><span class="sxs-lookup"><span data-stu-id="9cb34-141">NOTES</span></span>

## <span data-ttu-id="9cb34-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cb34-142">RELATED LINKS</span></span>
