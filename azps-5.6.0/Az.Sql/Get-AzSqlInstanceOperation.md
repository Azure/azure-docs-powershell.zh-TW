---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: c51ee87ccde0a6be22612033a2fb4c0a4ea3ad2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914286"
---
# <span data-ttu-id="4eef9-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="4eef9-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="4eef9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4eef9-102">SYNOPSIS</span></span>
<span data-ttu-id="4eef9-103">執行 SQL 受管理實例的操作。</span><span class="sxs-lookup"><span data-stu-id="4eef9-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="4eef9-104">語法</span><span class="sxs-lookup"><span data-stu-id="4eef9-104">SYNTAX</span></span>

### <span data-ttu-id="4eef9-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4eef9-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <String>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eef9-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eef9-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4eef9-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eef9-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eef9-108">描述</span><span class="sxs-lookup"><span data-stu-id="4eef9-108">DESCRIPTION</span></span>
<span data-ttu-id="4eef9-109">此Get-AzSqlInstanceOperation Cmdlet 會獲得 SQL 受管理實例上作業的資訊。</span><span class="sxs-lookup"><span data-stu-id="4eef9-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="4eef9-110">您可以查看受管理實例上的所有作業，或提供作業名稱來查看特定作業。</span><span class="sxs-lookup"><span data-stu-id="4eef9-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="4eef9-111">例子</span><span class="sxs-lookup"><span data-stu-id="4eef9-111">EXAMPLES</span></span>

### <span data-ttu-id="4eef9-112">範例 1：取得所有實例的運算</span><span class="sxs-lookup"><span data-stu-id="4eef9-112">Example 1: Get all instance's operations</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/79f2c91b-0080-4c14-b9b4-d9991c6e82dd
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 79f2c91b-0080-4c14-b9b4-d9991c6e82dd
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:19:53 AM
State                   : Cancelled
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="4eef9-113">此命令會獲得 SQL 管理實例的所有作業。</span><span class="sxs-lookup"><span data-stu-id="4eef9-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="4eef9-114">範例 2：取得特定作業</span><span class="sxs-lookup"><span data-stu-id="4eef9-114">Example 2: Get a specific operation</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="4eef9-115">此命令在 SQL 受管理實例上會使用名稱為 '5870c6d8-6703-4b27-8ae4-687b4ca7caea'的作業。</span><span class="sxs-lookup"><span data-stu-id="4eef9-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="4eef9-116">範例 3：使用作業資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4eef9-116">Example 3: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="4eef9-117">此命令會使用 id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers 執行 /Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'。</span><span class="sxs-lookup"><span data-stu-id="4eef9-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="4eef9-118">參數</span><span class="sxs-lookup"><span data-stu-id="4eef9-118">PARAMETERS</span></span>

### <span data-ttu-id="4eef9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eef9-119">-DefaultProfile</span></span>
<span data-ttu-id="4eef9-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4eef9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eef9-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="4eef9-121">-ManagedInstanceName</span></span>
<span data-ttu-id="4eef9-122">實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="4eef9-122">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eef9-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="4eef9-123">-Name</span></span>
<span data-ttu-id="4eef9-124">作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="4eef9-124">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: OperationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eef9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eef9-125">-ResourceGroupName</span></span>
<span data-ttu-id="4eef9-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4eef9-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eef9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4eef9-127">-ResourceId</span></span>
<span data-ttu-id="4eef9-128">受管理的實例作業資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4eef9-128">The managed instance operation resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByManagedInstanceOperationResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eef9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eef9-129">CommonParameters</span></span>
<span data-ttu-id="4eef9-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4eef9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eef9-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4eef9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eef9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="4eef9-132">INPUTS</span></span>

### <span data-ttu-id="4eef9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4eef9-133">System.String</span></span>

## <span data-ttu-id="4eef9-134">輸出</span><span class="sxs-lookup"><span data-stu-id="4eef9-134">OUTPUTS</span></span>

### <span data-ttu-id="4eef9-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="4eef9-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="4eef9-136">筆記</span><span class="sxs-lookup"><span data-stu-id="4eef9-136">NOTES</span></span>

## <span data-ttu-id="4eef9-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="4eef9-137">RELATED LINKS</span></span>
