---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: a9e3f5f8305733329f7ff9e34eadde151d873c6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915829"
---
# <span data-ttu-id="a3faa-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="a3faa-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="a3faa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a3faa-102">SYNOPSIS</span></span>
<span data-ttu-id="a3faa-103">移除組群資源。</span><span class="sxs-lookup"><span data-stu-id="a3faa-103">Remove cluster resource.</span></span>

## <span data-ttu-id="a3faa-104">語法</span><span class="sxs-lookup"><span data-stu-id="a3faa-104">SYNTAX</span></span>

### <span data-ttu-id="a3faa-105">ByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="a3faa-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3faa-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a3faa-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3faa-107">ById</span><span class="sxs-lookup"><span data-stu-id="a3faa-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3faa-108">描述</span><span class="sxs-lookup"><span data-stu-id="a3faa-108">DESCRIPTION</span></span>
<span data-ttu-id="a3faa-109">移除集區後，也會移除該組集中下的節點類型。</span><span class="sxs-lookup"><span data-stu-id="a3faa-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="a3faa-110">例子</span><span class="sxs-lookup"><span data-stu-id="a3faa-110">EXAMPLES</span></span>

### <span data-ttu-id="a3faa-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a3faa-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="a3faa-112">移除組。</span><span class="sxs-lookup"><span data-stu-id="a3faa-112">Remove cluster.</span></span>

### <span data-ttu-id="a3faa-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="a3faa-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="a3faa-114">使用管線移除集區。</span><span class="sxs-lookup"><span data-stu-id="a3faa-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="a3faa-115">參數</span><span class="sxs-lookup"><span data-stu-id="a3faa-115">PARAMETERS</span></span>

### <span data-ttu-id="a3faa-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3faa-116">-AsJob</span></span>
<span data-ttu-id="a3faa-117">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="a3faa-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a3faa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3faa-118">-DefaultProfile</span></span>
<span data-ttu-id="a3faa-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3faa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3faa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3faa-120">-InputObject</span></span>
<span data-ttu-id="a3faa-121">Managed Cluster 資源</span><span class="sxs-lookup"><span data-stu-id="a3faa-121">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3faa-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a3faa-122">-Name</span></span>
<span data-ttu-id="a3faa-123">指定組名。</span><span class="sxs-lookup"><span data-stu-id="a3faa-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3faa-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3faa-124">-PassThru</span></span>
<span data-ttu-id="a3faa-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="a3faa-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a3faa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3faa-126">-ResourceGroupName</span></span>
<span data-ttu-id="a3faa-127">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3faa-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3faa-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3faa-128">-ResourceId</span></span>
<span data-ttu-id="a3faa-129">Managed Cluster 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a3faa-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3faa-130">-確認</span><span class="sxs-lookup"><span data-stu-id="a3faa-130">-Confirm</span></span>
<span data-ttu-id="a3faa-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a3faa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3faa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3faa-132">-WhatIf</span></span>
<span data-ttu-id="a3faa-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3faa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3faa-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3faa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3faa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3faa-135">CommonParameters</span></span>
<span data-ttu-id="a3faa-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a3faa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3faa-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3faa-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3faa-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a3faa-138">INPUTS</span></span>

### <span data-ttu-id="a3faa-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a3faa-139">System.String</span></span>

## <span data-ttu-id="a3faa-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a3faa-140">OUTPUTS</span></span>

### <span data-ttu-id="a3faa-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3faa-141">System.Boolean</span></span>

## <span data-ttu-id="a3faa-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a3faa-142">NOTES</span></span>

## <span data-ttu-id="a3faa-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3faa-143">RELATED LINKS</span></span>
