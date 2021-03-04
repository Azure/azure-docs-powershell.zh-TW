---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
ms.openlocfilehash: 2433ffa7c1a016af4d3268162587d6b901b30ae9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910813"
---
# <span data-ttu-id="c5c54-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="c5c54-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="c5c54-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c5c54-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c54-103">在私人雲端中建立或更新集區</span><span class="sxs-lookup"><span data-stu-id="c5c54-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="c5c54-104">語法</span><span class="sxs-lookup"><span data-stu-id="c5c54-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c5c54-105">描述</span><span class="sxs-lookup"><span data-stu-id="c5c54-105">DESCRIPTION</span></span>
<span data-ttu-id="c5c54-106">在私人雲端中建立或更新集區</span><span class="sxs-lookup"><span data-stu-id="c5c54-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="c5c54-107">例子</span><span class="sxs-lookup"><span data-stu-id="c5c54-107">EXAMPLES</span></span>

### <span data-ttu-id="c5c54-108">範例 1：建立集區</span><span class="sxs-lookup"><span data-stu-id="c5c54-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="c5c54-109">建立集區</span><span class="sxs-lookup"><span data-stu-id="c5c54-109">Create cluster</span></span>

## <span data-ttu-id="c5c54-110">參數</span><span class="sxs-lookup"><span data-stu-id="c5c54-110">PARAMETERS</span></span>

### <span data-ttu-id="c5c54-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5c54-111">-AsJob</span></span>
<span data-ttu-id="c5c54-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="c5c54-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c5c54-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="c5c54-113">-ClusterSize</span></span>
<span data-ttu-id="c5c54-114">組大小</span><span class="sxs-lookup"><span data-stu-id="c5c54-114">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5c54-115">-DefaultProfile</span></span>
<span data-ttu-id="c5c54-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5c54-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c54-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c5c54-117">-Name</span></span>
<span data-ttu-id="c5c54-118">專用雲端中的組名</span><span class="sxs-lookup"><span data-stu-id="c5c54-118">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c54-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c5c54-119">-NoWait</span></span>
<span data-ttu-id="c5c54-120">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="c5c54-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c5c54-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="c5c54-121">-PrivateCloudName</span></span>
<span data-ttu-id="c5c54-122">私人雲端的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5c54-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="c5c54-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5c54-123">-ResourceGroupName</span></span>
<span data-ttu-id="c5c54-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5c54-124">The name of the resource group.</span></span>
<span data-ttu-id="c5c54-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c5c54-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c5c54-126">-SKUName</span><span class="sxs-lookup"><span data-stu-id="c5c54-126">-SkuName</span></span>
<span data-ttu-id="c5c54-127">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5c54-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="c5c54-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c5c54-128">-SubscriptionId</span></span>
<span data-ttu-id="c5c54-129">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5c54-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c54-130">-確認</span><span class="sxs-lookup"><span data-stu-id="c5c54-130">-Confirm</span></span>
<span data-ttu-id="c5c54-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c5c54-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5c54-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5c54-132">-WhatIf</span></span>
<span data-ttu-id="c5c54-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c5c54-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5c54-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c5c54-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5c54-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c54-135">CommonParameters</span></span>
<span data-ttu-id="c5c54-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c5c54-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c54-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5c54-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c54-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c5c54-138">INPUTS</span></span>

## <span data-ttu-id="c5c54-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c5c54-139">OUTPUTS</span></span>

### <span data-ttu-id="c5c54-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="c5c54-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="c5c54-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c5c54-141">NOTES</span></span>

<span data-ttu-id="c5c54-142">別名</span><span class="sxs-lookup"><span data-stu-id="c5c54-142">ALIASES</span></span>

## <span data-ttu-id="c5c54-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5c54-143">RELATED LINKS</span></span>

