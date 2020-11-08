---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 8bfcb3a96ee8db53a6a869a01441739ee9c503bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140437"
---
# <span data-ttu-id="a5d0c-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="a5d0c-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="a5d0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d0c-103">建立 Kusto 群集資料庫 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="a5d0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5d0c-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5d0c-105">說明</span><span class="sxs-lookup"><span data-stu-id="a5d0c-105">DESCRIPTION</span></span>
<span data-ttu-id="a5d0c-106">建立 Kusto 群集資料庫 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="a5d0c-107">示例</span><span class="sxs-lookup"><span data-stu-id="a5d0c-107">EXAMPLES</span></span>

### <span data-ttu-id="a5d0c-108">範例1：建立 Kusto 群集資料庫 principalAssignment</span><span class="sxs-lookup"><span data-stu-id="a5d0c-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="a5d0c-109">上述命令會建立 Kusto 群集資料庫 principalAssignment</span><span class="sxs-lookup"><span data-stu-id="a5d0c-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="a5d0c-110">參數</span><span class="sxs-lookup"><span data-stu-id="a5d0c-110">PARAMETERS</span></span>

### <span data-ttu-id="a5d0c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5d0c-111">-AsJob</span></span>
<span data-ttu-id="a5d0c-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="a5d0c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a5d0c-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a5d0c-113">-ClusterName</span></span>
<span data-ttu-id="a5d0c-114">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="a5d0c-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a5d0c-115">-DatabaseName</span></span>
<span data-ttu-id="a5d0c-116">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="a5d0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d0c-117">-DefaultProfile</span></span>
<span data-ttu-id="a5d0c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5d0c-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a5d0c-119">-NoWait</span></span>
<span data-ttu-id="a5d0c-120">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="a5d0c-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a5d0c-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="a5d0c-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="a5d0c-122">Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="a5d0c-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="a5d0c-123">-PrincipalId</span></span>
<span data-ttu-id="a5d0c-124">指派給資料庫主體的主要 ID。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="a5d0c-125">它可以是使用者的電子郵件、[應用程式識別碼] 或 [安全性群組名稱]。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="a5d0c-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="a5d0c-126">-PrincipalType</span></span>
<span data-ttu-id="a5d0c-127">主體類型。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-127">Principal type.</span></span>

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

### <span data-ttu-id="a5d0c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d0c-128">-ResourceGroupName</span></span>
<span data-ttu-id="a5d0c-129">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a5d0c-130">-角色</span><span class="sxs-lookup"><span data-stu-id="a5d0c-130">-Role</span></span>
<span data-ttu-id="a5d0c-131">資料庫主體角色。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-131">Database principal role.</span></span>

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

### <span data-ttu-id="a5d0c-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5d0c-132">-SubscriptionId</span></span>
<span data-ttu-id="a5d0c-133">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a5d0c-134">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a5d0c-135">-TenantId</span><span class="sxs-lookup"><span data-stu-id="a5d0c-135">-TenantId</span></span>
<span data-ttu-id="a5d0c-136">主體的租使用者識別碼</span><span class="sxs-lookup"><span data-stu-id="a5d0c-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="a5d0c-137">-確認</span><span class="sxs-lookup"><span data-stu-id="a5d0c-137">-Confirm</span></span>
<span data-ttu-id="a5d0c-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d0c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d0c-139">-WhatIf</span></span>
<span data-ttu-id="a5d0c-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d0c-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d0c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d0c-142">CommonParameters</span></span>
<span data-ttu-id="a5d0c-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d0c-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d0c-145">輸入</span><span class="sxs-lookup"><span data-stu-id="a5d0c-145">INPUTS</span></span>

## <span data-ttu-id="a5d0c-146">輸出</span><span class="sxs-lookup"><span data-stu-id="a5d0c-146">OUTPUTS</span></span>

### <span data-ttu-id="a5d0c-147">IDatabasePrincipalAssignment （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="a5d0c-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="a5d0c-148">筆記</span><span class="sxs-lookup"><span data-stu-id="a5d0c-148">NOTES</span></span>

<span data-ttu-id="a5d0c-149">別名</span><span class="sxs-lookup"><span data-stu-id="a5d0c-149">ALIASES</span></span>

## <span data-ttu-id="a5d0c-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5d0c-150">RELATED LINKS</span></span>

