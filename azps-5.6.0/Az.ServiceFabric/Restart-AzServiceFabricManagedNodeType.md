---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 8b68175be91b3669c42a67259f5095b567e7905e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915797"
---
# <span data-ttu-id="3faba-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3faba-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="3faba-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3faba-102">SYNOPSIS</span></span>
<span data-ttu-id="3faba-103">從節點類型重新開機特定節點。</span><span class="sxs-lookup"><span data-stu-id="3faba-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="3faba-104">語法</span><span class="sxs-lookup"><span data-stu-id="3faba-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3faba-105">描述</span><span class="sxs-lookup"><span data-stu-id="3faba-105">DESCRIPTION</span></span>
<span data-ttu-id="3faba-106">從節點類型重新開機特定節點。</span><span class="sxs-lookup"><span data-stu-id="3faba-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="3faba-107">在重新開機 vm 之前，它會停用服務結構節點，並再次啟用它們一旦恢復使用。</span><span class="sxs-lookup"><span data-stu-id="3faba-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="3faba-108">如果是在主要節點類型上完成此工作，可能需要一些時間，因為可能不會同時重新開機所有節點。</span><span class="sxs-lookup"><span data-stu-id="3faba-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="3faba-109">即使服務結構無法停用節點，使用 -ForceRestart 還是會強制執行作業，但請小心使用，因為如果節點上執行有狀態的工作量，可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="3faba-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="3faba-110">例子</span><span class="sxs-lookup"><span data-stu-id="3faba-110">EXAMPLES</span></span>

### <span data-ttu-id="3faba-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="3faba-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="3faba-112">在節點類型上重新開機節點 0 和 3。</span><span class="sxs-lookup"><span data-stu-id="3faba-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="3faba-113">參數</span><span class="sxs-lookup"><span data-stu-id="3faba-113">PARAMETERS</span></span>

### <span data-ttu-id="3faba-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3faba-114">-AsJob</span></span>
<span data-ttu-id="3faba-115">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="3faba-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3faba-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3faba-116">-ClusterName</span></span>
<span data-ttu-id="3faba-117">指定組名。</span><span class="sxs-lookup"><span data-stu-id="3faba-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3faba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3faba-118">-DefaultProfile</span></span>
<span data-ttu-id="3faba-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3faba-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3faba-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="3faba-120">-ForceRestart</span></span>
<span data-ttu-id="3faba-121">使用此旗標會強制節點重新開機，即使服務結構無法停用節點。</span><span class="sxs-lookup"><span data-stu-id="3faba-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="3faba-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="3faba-122">-Name</span></span>
<span data-ttu-id="3faba-123">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="3faba-123">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3faba-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="3faba-124">-NodeName</span></span>
<span data-ttu-id="3faba-125">作業的節點名稱清單。</span><span class="sxs-lookup"><span data-stu-id="3faba-125">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3faba-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3faba-126">-PassThru</span></span>
<span data-ttu-id="3faba-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="3faba-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="3faba-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3faba-128">-ResourceGroupName</span></span>
<span data-ttu-id="3faba-129">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3faba-129">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3faba-130">-確認</span><span class="sxs-lookup"><span data-stu-id="3faba-130">-Confirm</span></span>
<span data-ttu-id="3faba-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3faba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3faba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3faba-132">-WhatIf</span></span>
<span data-ttu-id="3faba-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3faba-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3faba-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3faba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3faba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3faba-135">CommonParameters</span></span>
<span data-ttu-id="3faba-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3faba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3faba-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3faba-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3faba-138">輸入</span><span class="sxs-lookup"><span data-stu-id="3faba-138">INPUTS</span></span>

### <span data-ttu-id="3faba-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3faba-139">System.String</span></span>

## <span data-ttu-id="3faba-140">輸出</span><span class="sxs-lookup"><span data-stu-id="3faba-140">OUTPUTS</span></span>

### <span data-ttu-id="3faba-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3faba-141">System.Boolean</span></span>

## <span data-ttu-id="3faba-142">筆記</span><span class="sxs-lookup"><span data-stu-id="3faba-142">NOTES</span></span>

## <span data-ttu-id="3faba-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="3faba-143">RELATED LINKS</span></span>
