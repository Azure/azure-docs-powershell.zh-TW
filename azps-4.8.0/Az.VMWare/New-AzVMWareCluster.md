---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
ms.openlocfilehash: f2ed1813859f92624696eef7fa4f881f3eba1628
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128406"
---
# <span data-ttu-id="58df7-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="58df7-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="58df7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58df7-102">SYNOPSIS</span></span>
<span data-ttu-id="58df7-103">在私有雲端建立或更新群集</span><span class="sxs-lookup"><span data-stu-id="58df7-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="58df7-104">句法</span><span class="sxs-lookup"><span data-stu-id="58df7-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="58df7-105">說明</span><span class="sxs-lookup"><span data-stu-id="58df7-105">DESCRIPTION</span></span>
<span data-ttu-id="58df7-106">在私有雲端建立或更新群集</span><span class="sxs-lookup"><span data-stu-id="58df7-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="58df7-107">示例</span><span class="sxs-lookup"><span data-stu-id="58df7-107">EXAMPLES</span></span>

### <span data-ttu-id="58df7-108">範例1：建立群集</span><span class="sxs-lookup"><span data-stu-id="58df7-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="58df7-109">建立群集</span><span class="sxs-lookup"><span data-stu-id="58df7-109">Create cluster</span></span>

## <span data-ttu-id="58df7-110">參數</span><span class="sxs-lookup"><span data-stu-id="58df7-110">PARAMETERS</span></span>

### <span data-ttu-id="58df7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58df7-111">-AsJob</span></span>
<span data-ttu-id="58df7-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="58df7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="58df7-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="58df7-113">-ClusterSize</span></span>
<span data-ttu-id="58df7-114">群集大小</span><span class="sxs-lookup"><span data-stu-id="58df7-114">The cluster size</span></span>

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

### <span data-ttu-id="58df7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58df7-115">-DefaultProfile</span></span>
<span data-ttu-id="58df7-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58df7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58df7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="58df7-117">-Name</span></span>
<span data-ttu-id="58df7-118">私人雲端中的群集名稱</span><span class="sxs-lookup"><span data-stu-id="58df7-118">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="58df7-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="58df7-119">-NoWait</span></span>
<span data-ttu-id="58df7-120">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="58df7-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="58df7-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="58df7-121">-PrivateCloudName</span></span>
<span data-ttu-id="58df7-122">私有雲端的名稱。</span><span class="sxs-lookup"><span data-stu-id="58df7-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="58df7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58df7-123">-ResourceGroupName</span></span>
<span data-ttu-id="58df7-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="58df7-124">The name of the resource group.</span></span>
<span data-ttu-id="58df7-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="58df7-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="58df7-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="58df7-126">-SkuName</span></span>
<span data-ttu-id="58df7-127">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="58df7-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="58df7-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58df7-128">-SubscriptionId</span></span>
<span data-ttu-id="58df7-129">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="58df7-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="58df7-130">-確認</span><span class="sxs-lookup"><span data-stu-id="58df7-130">-Confirm</span></span>
<span data-ttu-id="58df7-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58df7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58df7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58df7-132">-WhatIf</span></span>
<span data-ttu-id="58df7-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58df7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58df7-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58df7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58df7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58df7-135">CommonParameters</span></span>
<span data-ttu-id="58df7-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58df7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58df7-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="58df7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58df7-138">輸入</span><span class="sxs-lookup"><span data-stu-id="58df7-138">INPUTS</span></span>

## <span data-ttu-id="58df7-139">輸出</span><span class="sxs-lookup"><span data-stu-id="58df7-139">OUTPUTS</span></span>

### <span data-ttu-id="58df7-140">ICluster 中的 Api20200320 （）。</span><span class="sxs-lookup"><span data-stu-id="58df7-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="58df7-141">筆記</span><span class="sxs-lookup"><span data-stu-id="58df7-141">NOTES</span></span>

<span data-ttu-id="58df7-142">別名</span><span class="sxs-lookup"><span data-stu-id="58df7-142">ALIASES</span></span>

## <span data-ttu-id="58df7-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="58df7-143">RELATED LINKS</span></span>

