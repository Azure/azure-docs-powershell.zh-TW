---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 8f2a0cd576c3fe7f184d3f016f6666aa8749b5c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129490"
---
# <span data-ttu-id="a51cd-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="a51cd-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="a51cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a51cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a51cd-103">建立 Kusto 群集 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="a51cd-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="a51cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="a51cd-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a51cd-105">說明</span><span class="sxs-lookup"><span data-stu-id="a51cd-105">DESCRIPTION</span></span>
<span data-ttu-id="a51cd-106">建立 Kusto 群集 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="a51cd-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="a51cd-107">示例</span><span class="sxs-lookup"><span data-stu-id="a51cd-107">EXAMPLES</span></span>

### <span data-ttu-id="a51cd-108">範例1：建立 Kusto 群集 principalAssignment</span><span class="sxs-lookup"><span data-stu-id="a51cd-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="a51cd-109">上述命令會建立 Kusto 群集 principalAssignment</span><span class="sxs-lookup"><span data-stu-id="a51cd-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="a51cd-110">參數</span><span class="sxs-lookup"><span data-stu-id="a51cd-110">PARAMETERS</span></span>

### <span data-ttu-id="a51cd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a51cd-111">-AsJob</span></span>
<span data-ttu-id="a51cd-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="a51cd-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a51cd-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a51cd-113">-ClusterName</span></span>
<span data-ttu-id="a51cd-114">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a51cd-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="a51cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a51cd-115">-DefaultProfile</span></span>
<span data-ttu-id="a51cd-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a51cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a51cd-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a51cd-117">-NoWait</span></span>
<span data-ttu-id="a51cd-118">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="a51cd-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a51cd-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="a51cd-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="a51cd-120">Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a51cd-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="a51cd-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="a51cd-121">-PrincipalId</span></span>
<span data-ttu-id="a51cd-122">指派給群集主體的主要 ID。</span><span class="sxs-lookup"><span data-stu-id="a51cd-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="a51cd-123">它可以是使用者的電子郵件、[應用程式識別碼] 或 [安全性群組名稱]。</span><span class="sxs-lookup"><span data-stu-id="a51cd-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="a51cd-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="a51cd-124">-PrincipalType</span></span>
<span data-ttu-id="a51cd-125">主體類型。</span><span class="sxs-lookup"><span data-stu-id="a51cd-125">Principal type.</span></span>

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

### <span data-ttu-id="a51cd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a51cd-126">-ResourceGroupName</span></span>
<span data-ttu-id="a51cd-127">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a51cd-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a51cd-128">-角色</span><span class="sxs-lookup"><span data-stu-id="a51cd-128">-Role</span></span>
<span data-ttu-id="a51cd-129">群集主要角色。</span><span class="sxs-lookup"><span data-stu-id="a51cd-129">Cluster principal role.</span></span>

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

### <span data-ttu-id="a51cd-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a51cd-130">-SubscriptionId</span></span>
<span data-ttu-id="a51cd-131">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a51cd-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a51cd-132">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a51cd-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a51cd-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="a51cd-133">-TenantId</span></span>
<span data-ttu-id="a51cd-134">主體的租使用者識別碼</span><span class="sxs-lookup"><span data-stu-id="a51cd-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="a51cd-135">-確認</span><span class="sxs-lookup"><span data-stu-id="a51cd-135">-Confirm</span></span>
<span data-ttu-id="a51cd-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a51cd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a51cd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a51cd-137">-WhatIf</span></span>
<span data-ttu-id="a51cd-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a51cd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a51cd-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a51cd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a51cd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a51cd-140">CommonParameters</span></span>
<span data-ttu-id="a51cd-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a51cd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a51cd-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a51cd-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a51cd-143">輸入</span><span class="sxs-lookup"><span data-stu-id="a51cd-143">INPUTS</span></span>

## <span data-ttu-id="a51cd-144">輸出</span><span class="sxs-lookup"><span data-stu-id="a51cd-144">OUTPUTS</span></span>

### <span data-ttu-id="a51cd-145">IClusterPrincipalAssignment （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="a51cd-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="a51cd-146">筆記</span><span class="sxs-lookup"><span data-stu-id="a51cd-146">NOTES</span></span>

<span data-ttu-id="a51cd-147">別名</span><span class="sxs-lookup"><span data-stu-id="a51cd-147">ALIASES</span></span>

## <span data-ttu-id="a51cd-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a51cd-148">RELATED LINKS</span></span>
