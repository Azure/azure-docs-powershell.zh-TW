---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130727"
---
# <span data-ttu-id="11049-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="11049-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="11049-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11049-102">SYNOPSIS</span></span>
<span data-ttu-id="11049-103">從節點類型重新開機特定節點。</span><span class="sxs-lookup"><span data-stu-id="11049-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="11049-104">句法</span><span class="sxs-lookup"><span data-stu-id="11049-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11049-105">說明</span><span class="sxs-lookup"><span data-stu-id="11049-105">DESCRIPTION</span></span>
<span data-ttu-id="11049-106">從節點類型重新開機特定節點。</span><span class="sxs-lookup"><span data-stu-id="11049-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="11049-107">它會在重新開機 vm 之前停用服務結構節點，然後在它們返回之後再次啟用它們。</span><span class="sxs-lookup"><span data-stu-id="11049-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="11049-108">如果這是在主要節點類型上完成，可能需要一段時間，因為它可能不會同時重新開機所有節點。</span><span class="sxs-lookup"><span data-stu-id="11049-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="11049-109">Use-ForceRestart 會強制執行作業，即使服務結構無法停用節點，但使用時請小心，因為如果狀態工作負荷在節點上執行，可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="11049-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="11049-110">示例</span><span class="sxs-lookup"><span data-stu-id="11049-110">EXAMPLES</span></span>

### <span data-ttu-id="11049-111">範例1</span><span class="sxs-lookup"><span data-stu-id="11049-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="11049-112">重新開機節點類型上的節點0和3。</span><span class="sxs-lookup"><span data-stu-id="11049-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="11049-113">參數</span><span class="sxs-lookup"><span data-stu-id="11049-113">PARAMETERS</span></span>

### <span data-ttu-id="11049-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11049-114">-AsJob</span></span>
<span data-ttu-id="11049-115">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="11049-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="11049-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="11049-116">-ClusterName</span></span>
<span data-ttu-id="11049-117">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="11049-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="11049-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11049-118">-DefaultProfile</span></span>
<span data-ttu-id="11049-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11049-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11049-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="11049-120">-ForceRestart</span></span>
<span data-ttu-id="11049-121">使用這個標誌，即使服務結構無法停用節點，也會強制該節點重新開機。</span><span class="sxs-lookup"><span data-stu-id="11049-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="11049-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="11049-122">-Name</span></span>
<span data-ttu-id="11049-123">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="11049-123">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="11049-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="11049-124">-NodeName</span></span>
<span data-ttu-id="11049-125">操作的節點名稱清單。</span><span class="sxs-lookup"><span data-stu-id="11049-125">List of node names for the operation.</span></span>

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

### <span data-ttu-id="11049-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11049-126">-PassThru</span></span>
<span data-ttu-id="11049-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="11049-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="11049-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11049-128">-ResourceGroupName</span></span>
<span data-ttu-id="11049-129">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="11049-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="11049-130">-確認</span><span class="sxs-lookup"><span data-stu-id="11049-130">-Confirm</span></span>
<span data-ttu-id="11049-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11049-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11049-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11049-132">-WhatIf</span></span>
<span data-ttu-id="11049-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11049-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11049-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11049-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11049-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11049-135">CommonParameters</span></span>
<span data-ttu-id="11049-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11049-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11049-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="11049-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11049-138">輸入</span><span class="sxs-lookup"><span data-stu-id="11049-138">INPUTS</span></span>

### <span data-ttu-id="11049-139">System.object</span><span class="sxs-lookup"><span data-stu-id="11049-139">System.String</span></span>

## <span data-ttu-id="11049-140">輸出</span><span class="sxs-lookup"><span data-stu-id="11049-140">OUTPUTS</span></span>

### <span data-ttu-id="11049-141">System.object</span><span class="sxs-lookup"><span data-stu-id="11049-141">System.Boolean</span></span>

## <span data-ttu-id="11049-142">筆記</span><span class="sxs-lookup"><span data-stu-id="11049-142">NOTES</span></span>

## <span data-ttu-id="11049-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="11049-143">RELATED LINKS</span></span>
