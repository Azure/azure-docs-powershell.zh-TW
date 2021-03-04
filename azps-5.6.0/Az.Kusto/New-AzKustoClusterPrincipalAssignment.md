---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 738f0d4b4033dd7cccdc0fbabe94d2dfde9779c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903809"
---
# <span data-ttu-id="4ea7a-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="4ea7a-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="4ea7a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4ea7a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea7a-103">建立 Kusto cluster principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="4ea7a-104">語法</span><span class="sxs-lookup"><span data-stu-id="4ea7a-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4ea7a-105">描述</span><span class="sxs-lookup"><span data-stu-id="4ea7a-105">DESCRIPTION</span></span>
<span data-ttu-id="4ea7a-106">建立 Kusto cluster principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="4ea7a-107">例子</span><span class="sxs-lookup"><span data-stu-id="4ea7a-107">EXAMPLES</span></span>

### <span data-ttu-id="4ea7a-108">範例 1：建立 Kusto cluster principalAssignment</span><span class="sxs-lookup"><span data-stu-id="4ea7a-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="4ea7a-109">上述命令會建立一個 Kusto cluster principalAssignment</span><span class="sxs-lookup"><span data-stu-id="4ea7a-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="4ea7a-110">參數</span><span class="sxs-lookup"><span data-stu-id="4ea7a-110">PARAMETERS</span></span>

### <span data-ttu-id="4ea7a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ea7a-111">-AsJob</span></span>
<span data-ttu-id="4ea7a-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="4ea7a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="4ea7a-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4ea7a-113">-ClusterName</span></span>
<span data-ttu-id="4ea7a-114">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4ea7a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea7a-115">-DefaultProfile</span></span>
<span data-ttu-id="4ea7a-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ea7a-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4ea7a-117">-NoWait</span></span>
<span data-ttu-id="4ea7a-118">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="4ea7a-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4ea7a-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="4ea7a-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="4ea7a-120">Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="4ea7a-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="4ea7a-121">-PrincipalId</span></span>
<span data-ttu-id="4ea7a-122">指派給組主體的主要識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="4ea7a-123">它可以是使用者電子郵件、應用程式識別碼或安全性群組名。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-123">It can be a user email, application ID, or security group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea7a-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="4ea7a-124">-PrincipalType</span></span>
<span data-ttu-id="4ea7a-125">主體類型。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-125">Principal type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.PrincipalType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea7a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ea7a-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ea7a-127">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4ea7a-128">-角色</span><span class="sxs-lookup"><span data-stu-id="4ea7a-128">-Role</span></span>
<span data-ttu-id="4ea7a-129">集區主體角色。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-129">Cluster principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.ClusterPrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea7a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ea7a-130">-SubscriptionId</span></span>
<span data-ttu-id="4ea7a-131">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4ea7a-132">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4ea7a-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="4ea7a-133">-TenantId</span></span>
<span data-ttu-id="4ea7a-134">主體的租使用者識別碼</span><span class="sxs-lookup"><span data-stu-id="4ea7a-134">The tenant id of the principal</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea7a-135">-確認</span><span class="sxs-lookup"><span data-stu-id="4ea7a-135">-Confirm</span></span>
<span data-ttu-id="4ea7a-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ea7a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ea7a-137">-WhatIf</span></span>
<span data-ttu-id="4ea7a-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ea7a-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ea7a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea7a-140">CommonParameters</span></span>
<span data-ttu-id="4ea7a-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4ea7a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea7a-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ea7a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea7a-143">輸入</span><span class="sxs-lookup"><span data-stu-id="4ea7a-143">INPUTS</span></span>

## <span data-ttu-id="4ea7a-144">輸出</span><span class="sxs-lookup"><span data-stu-id="4ea7a-144">OUTPUTS</span></span>

### <span data-ttu-id="4ea7a-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="4ea7a-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="4ea7a-146">筆記</span><span class="sxs-lookup"><span data-stu-id="4ea7a-146">NOTES</span></span>

<span data-ttu-id="4ea7a-147">別名</span><span class="sxs-lookup"><span data-stu-id="4ea7a-147">ALIASES</span></span>

## <span data-ttu-id="4ea7a-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ea7a-148">RELATED LINKS</span></span>

