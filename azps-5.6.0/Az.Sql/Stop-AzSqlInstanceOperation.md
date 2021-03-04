---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c72ed4167e08988070d12b686363240e2b47014a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904817"
---
# <span data-ttu-id="870c1-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="870c1-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="870c1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="870c1-102">SYNOPSIS</span></span>
<span data-ttu-id="870c1-103">停止 SQL 受管理實例的作業。</span><span class="sxs-lookup"><span data-stu-id="870c1-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="870c1-104">語法</span><span class="sxs-lookup"><span data-stu-id="870c1-104">SYNTAX</span></span>

### <span data-ttu-id="870c1-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="870c1-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="870c1-106">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="870c1-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="870c1-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="870c1-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="870c1-108">描述</span><span class="sxs-lookup"><span data-stu-id="870c1-108">DESCRIPTION</span></span>
<span data-ttu-id="870c1-109">Cmdlet Stop-AzSqlInstanceOperation SQL 受管理實例上提供的作業名稱停止作業。</span><span class="sxs-lookup"><span data-stu-id="870c1-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="870c1-110">例子</span><span class="sxs-lookup"><span data-stu-id="870c1-110">EXAMPLES</span></span>

### <span data-ttu-id="870c1-111">範例 1：取得特定作業</span><span class="sxs-lookup"><span data-stu-id="870c1-111">Example 1: Get a specific operation</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name d0f5bef5-e2b1-4ef8-bb42-2e54073874f9

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:49:53 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="870c1-112">此命令會停止在 SQL 受管理實例上名稱為 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' 的作業。</span><span class="sxs-lookup"><span data-stu-id="870c1-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="870c1-113">範例 2：使用作業資源識別碼</span><span class="sxs-lookup"><span data-stu-id="870c1-113">Example 2: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 4253bf58-34f1-4499-80c6-198d94c659f7
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/4253bf58-34f1-4499-80c6-198d94c659f7
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 4253bf58-34f1-4499-80c6-198d94c659f7
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:47:32 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="870c1-114">此命令會停止使用資源識別碼 $managedInstanceOperation.Id。</span><span class="sxs-lookup"><span data-stu-id="870c1-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="870c1-115">範例 3：使用工作物件</span><span class="sxs-lookup"><span data-stu-id="870c1-115">Example 3: Using operation object</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name b15a2b78-c42c-4e00-bf87-7ef4737552dc
PS C:\> Stop-AzSqlInstanceOperation -InputObject $managedInstanceOperation

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/b15a2b78-c42c-4e00-bf87-7ef4737552dc
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : b15a2b78-c42c-4e00-bf87-7ef4737552dc
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:44:57 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="870c1-116">此命令會停止使用物件或物件$managedInstanceOperation。</span><span class="sxs-lookup"><span data-stu-id="870c1-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="870c1-117">參數</span><span class="sxs-lookup"><span data-stu-id="870c1-117">PARAMETERS</span></span>

### <span data-ttu-id="870c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="870c1-118">-DefaultProfile</span></span>
<span data-ttu-id="870c1-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="870c1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="870c1-120">-強制</span><span class="sxs-lookup"><span data-stu-id="870c1-120">-Force</span></span>
<span data-ttu-id="870c1-121">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="870c1-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="870c1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="870c1-122">-InputObject</span></span>
<span data-ttu-id="870c1-123">要取消的作業</span><span class="sxs-lookup"><span data-stu-id="870c1-123">The operation to cancel</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel
Parameter Sets: StopByInputObjectParameterSet
Aliases: SqlInstanceOperation

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="870c1-124">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="870c1-124">-ManagedInstanceName</span></span>
<span data-ttu-id="870c1-125">實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="870c1-125">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870c1-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="870c1-126">-Name</span></span>
<span data-ttu-id="870c1-127">作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="870c1-127">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases: OperationName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870c1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="870c1-128">-ResourceGroupName</span></span>
<span data-ttu-id="870c1-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="870c1-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870c1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="870c1-130">-ResourceId</span></span>
<span data-ttu-id="870c1-131">要停止之工作物件的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="870c1-131">The resource id of operation object to stop</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="870c1-132">-確認</span><span class="sxs-lookup"><span data-stu-id="870c1-132">-Confirm</span></span>
<span data-ttu-id="870c1-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="870c1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="870c1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="870c1-134">-WhatIf</span></span>
<span data-ttu-id="870c1-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="870c1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="870c1-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="870c1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="870c1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="870c1-137">CommonParameters</span></span>
<span data-ttu-id="870c1-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="870c1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="870c1-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="870c1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="870c1-140">輸入</span><span class="sxs-lookup"><span data-stu-id="870c1-140">INPUTS</span></span>

### <span data-ttu-id="870c1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="870c1-141">System.String</span></span>

### <span data-ttu-id="870c1-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="870c1-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="870c1-143">輸出</span><span class="sxs-lookup"><span data-stu-id="870c1-143">OUTPUTS</span></span>

### <span data-ttu-id="870c1-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="870c1-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="870c1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="870c1-145">NOTES</span></span>

## <span data-ttu-id="870c1-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="870c1-146">RELATED LINKS</span></span>
