---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 9fd729a85babf1440516c52f0e7737f4c0d0d281
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906594"
---
# <span data-ttu-id="11bcf-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="11bcf-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="11bcf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="11bcf-103">建立 Kusto cluster 資料庫主體Assignment。</span><span class="sxs-lookup"><span data-stu-id="11bcf-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="11bcf-104">語法</span><span class="sxs-lookup"><span data-stu-id="11bcf-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="11bcf-105">描述</span><span class="sxs-lookup"><span data-stu-id="11bcf-105">DESCRIPTION</span></span>
<span data-ttu-id="11bcf-106">建立 Kusto cluster 資料庫主體Assignment。</span><span class="sxs-lookup"><span data-stu-id="11bcf-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="11bcf-107">例子</span><span class="sxs-lookup"><span data-stu-id="11bcf-107">EXAMPLES</span></span>

### <span data-ttu-id="11bcf-108">範例 1：建立 Kusto cluster 資料庫主體Assignment</span><span class="sxs-lookup"><span data-stu-id="11bcf-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="11bcf-109">上述命令會建立 Kusto cluster 資料庫主體Assignment</span><span class="sxs-lookup"><span data-stu-id="11bcf-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="11bcf-110">參數</span><span class="sxs-lookup"><span data-stu-id="11bcf-110">PARAMETERS</span></span>

### <span data-ttu-id="11bcf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11bcf-111">-AsJob</span></span>
<span data-ttu-id="11bcf-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="11bcf-112">Run the command as a job</span></span>

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

### <span data-ttu-id="11bcf-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="11bcf-113">-ClusterName</span></span>
<span data-ttu-id="11bcf-114">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="11bcf-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="11bcf-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="11bcf-115">-DatabaseName</span></span>
<span data-ttu-id="11bcf-116">Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="11bcf-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="11bcf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11bcf-117">-DefaultProfile</span></span>
<span data-ttu-id="11bcf-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="11bcf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11bcf-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="11bcf-119">-NoWait</span></span>
<span data-ttu-id="11bcf-120">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="11bcf-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="11bcf-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="11bcf-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="11bcf-122">Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="11bcf-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="11bcf-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="11bcf-123">-PrincipalId</span></span>
<span data-ttu-id="11bcf-124">指派給資料庫主體的主要識別碼。</span><span class="sxs-lookup"><span data-stu-id="11bcf-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="11bcf-125">它可以是使用者電子郵件、應用程式識別碼或安全性群組名。</span><span class="sxs-lookup"><span data-stu-id="11bcf-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="11bcf-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="11bcf-126">-PrincipalType</span></span>
<span data-ttu-id="11bcf-127">主體類型。</span><span class="sxs-lookup"><span data-stu-id="11bcf-127">Principal type.</span></span>

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

### <span data-ttu-id="11bcf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11bcf-128">-ResourceGroupName</span></span>
<span data-ttu-id="11bcf-129">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="11bcf-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="11bcf-130">-角色</span><span class="sxs-lookup"><span data-stu-id="11bcf-130">-Role</span></span>
<span data-ttu-id="11bcf-131">資料庫主體角色。</span><span class="sxs-lookup"><span data-stu-id="11bcf-131">Database principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DatabasePrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bcf-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11bcf-132">-SubscriptionId</span></span>
<span data-ttu-id="11bcf-133">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="11bcf-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="11bcf-134">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="11bcf-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="11bcf-135">-TenantId</span><span class="sxs-lookup"><span data-stu-id="11bcf-135">-TenantId</span></span>
<span data-ttu-id="11bcf-136">主體的租使用者識別碼</span><span class="sxs-lookup"><span data-stu-id="11bcf-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="11bcf-137">-確認</span><span class="sxs-lookup"><span data-stu-id="11bcf-137">-Confirm</span></span>
<span data-ttu-id="11bcf-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="11bcf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11bcf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11bcf-139">-WhatIf</span></span>
<span data-ttu-id="11bcf-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11bcf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11bcf-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11bcf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11bcf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11bcf-142">CommonParameters</span></span>
<span data-ttu-id="11bcf-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11bcf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11bcf-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11bcf-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11bcf-145">輸入</span><span class="sxs-lookup"><span data-stu-id="11bcf-145">INPUTS</span></span>

## <span data-ttu-id="11bcf-146">輸出</span><span class="sxs-lookup"><span data-stu-id="11bcf-146">OUTPUTS</span></span>

### <span data-ttu-id="11bcf-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="11bcf-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="11bcf-148">筆記</span><span class="sxs-lookup"><span data-stu-id="11bcf-148">NOTES</span></span>

<span data-ttu-id="11bcf-149">別名</span><span class="sxs-lookup"><span data-stu-id="11bcf-149">ALIASES</span></span>

## <span data-ttu-id="11bcf-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="11bcf-150">RELATED LINKS</span></span>

