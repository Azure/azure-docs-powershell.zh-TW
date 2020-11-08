---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: d676958948b9197a64a08646e837287299107bfa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129249"
---
# <span data-ttu-id="593ec-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="593ec-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="593ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="593ec-102">SYNOPSIS</span></span>
<span data-ttu-id="593ec-103">移除 [群集資源]。</span><span class="sxs-lookup"><span data-stu-id="593ec-103">Remove cluster resource.</span></span>

## <span data-ttu-id="593ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="593ec-104">SYNTAX</span></span>

### <span data-ttu-id="593ec-105">ByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="593ec-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="593ec-106">ByName</span><span class="sxs-lookup"><span data-stu-id="593ec-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="593ec-107">ById</span><span class="sxs-lookup"><span data-stu-id="593ec-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="593ec-108">說明</span><span class="sxs-lookup"><span data-stu-id="593ec-108">DESCRIPTION</span></span>
<span data-ttu-id="593ec-109">移除群集這會在群集底下移除節點類型。</span><span class="sxs-lookup"><span data-stu-id="593ec-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="593ec-110">示例</span><span class="sxs-lookup"><span data-stu-id="593ec-110">EXAMPLES</span></span>

### <span data-ttu-id="593ec-111">範例1</span><span class="sxs-lookup"><span data-stu-id="593ec-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="593ec-112">移除群集。</span><span class="sxs-lookup"><span data-stu-id="593ec-112">Remove cluster.</span></span>

### <span data-ttu-id="593ec-113">範例2</span><span class="sxs-lookup"><span data-stu-id="593ec-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="593ec-114">使用管道移除群集。</span><span class="sxs-lookup"><span data-stu-id="593ec-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="593ec-115">參數</span><span class="sxs-lookup"><span data-stu-id="593ec-115">PARAMETERS</span></span>

### <span data-ttu-id="593ec-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="593ec-116">-AsJob</span></span>
<span data-ttu-id="593ec-117">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="593ec-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="593ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="593ec-118">-DefaultProfile</span></span>
<span data-ttu-id="593ec-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="593ec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="593ec-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="593ec-120">-InputObject</span></span>
<span data-ttu-id="593ec-121">受管理的群集資源</span><span class="sxs-lookup"><span data-stu-id="593ec-121">Managed Cluster resource</span></span>

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

### <span data-ttu-id="593ec-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="593ec-122">-Name</span></span>
<span data-ttu-id="593ec-123">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="593ec-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="593ec-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="593ec-124">-PassThru</span></span>
<span data-ttu-id="593ec-125">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="593ec-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="593ec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="593ec-126">-ResourceGroupName</span></span>
<span data-ttu-id="593ec-127">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="593ec-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="593ec-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="593ec-128">-ResourceId</span></span>
<span data-ttu-id="593ec-129">受管理的群集資源識別碼</span><span class="sxs-lookup"><span data-stu-id="593ec-129">Managed Cluster resource id</span></span>

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

### <span data-ttu-id="593ec-130">-確認</span><span class="sxs-lookup"><span data-stu-id="593ec-130">-Confirm</span></span>
<span data-ttu-id="593ec-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="593ec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="593ec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="593ec-132">-WhatIf</span></span>
<span data-ttu-id="593ec-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="593ec-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="593ec-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="593ec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="593ec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="593ec-135">CommonParameters</span></span>
<span data-ttu-id="593ec-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="593ec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="593ec-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="593ec-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="593ec-138">輸入</span><span class="sxs-lookup"><span data-stu-id="593ec-138">INPUTS</span></span>

### <span data-ttu-id="593ec-139">System.object</span><span class="sxs-lookup"><span data-stu-id="593ec-139">System.String</span></span>

## <span data-ttu-id="593ec-140">輸出</span><span class="sxs-lookup"><span data-stu-id="593ec-140">OUTPUTS</span></span>

### <span data-ttu-id="593ec-141">System.object</span><span class="sxs-lookup"><span data-stu-id="593ec-141">System.Boolean</span></span>

## <span data-ttu-id="593ec-142">筆記</span><span class="sxs-lookup"><span data-stu-id="593ec-142">NOTES</span></span>

## <span data-ttu-id="593ec-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="593ec-143">RELATED LINKS</span></span>