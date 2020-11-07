---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: b9f008d610729d1f1bc73affbb5b8f3eae04ecdd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965705"
---
# <span data-ttu-id="cfa6b-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="cfa6b-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="cfa6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cfa6b-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa6b-103">取得 SQL managed 實例的操作。</span><span class="sxs-lookup"><span data-stu-id="cfa6b-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="cfa6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="cfa6b-104">SYNTAX</span></span>

### <span data-ttu-id="cfa6b-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cfa6b-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <Guid>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfa6b-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfa6b-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cfa6b-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfa6b-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfa6b-108">說明</span><span class="sxs-lookup"><span data-stu-id="cfa6b-108">DESCRIPTION</span></span>
<span data-ttu-id="cfa6b-109">Get-AzSqlInstanceOperation Cmdlet 會取得有關 SQL managed 實例上操作的資訊。</span><span class="sxs-lookup"><span data-stu-id="cfa6b-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="cfa6b-110">您可以透過提供作業名稱來查看受管理實例上的所有操作，或查看特定的操作。</span><span class="sxs-lookup"><span data-stu-id="cfa6b-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="cfa6b-111">示例</span><span class="sxs-lookup"><span data-stu-id="cfa6b-111">EXAMPLES</span></span>

### <span data-ttu-id="cfa6b-112">範例1：取得所有實例的操作</span><span class="sxs-lookup"><span data-stu-id="cfa6b-112">Example 1: Get all instance's operations</span></span>
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
```

<span data-ttu-id="cfa6b-113">這個命令會取得 SQL managed 實例的所有操作。</span><span class="sxs-lookup"><span data-stu-id="cfa6b-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="cfa6b-114">範例2：取得特定的操作</span><span class="sxs-lookup"><span data-stu-id="cfa6b-114">Example 2: Get a specific operation</span></span>
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
```

<span data-ttu-id="cfa6b-115">這個命令會在 SQL managed 實例上取得名稱為 "5870c6d8-6703-4b27-8ae4-687b4ca7caea" 的運算。</span><span class="sxs-lookup"><span data-stu-id="cfa6b-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="cfa6b-116">範例3：使用作業資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cfa6b-116">Example 3: Using operation resource id</span></span>
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
```

<span data-ttu-id="cfa6b-117">此命令會取得 id 為 "/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea" 的操作。</span><span class="sxs-lookup"><span data-stu-id="cfa6b-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="cfa6b-118">參數</span><span class="sxs-lookup"><span data-stu-id="cfa6b-118">PARAMETERS</span></span>

### <span data-ttu-id="cfa6b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa6b-119">-DefaultProfile</span></span>
<span data-ttu-id="cfa6b-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cfa6b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfa6b-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="cfa6b-121">-ManagedInstanceName</span></span>
<span data-ttu-id="cfa6b-122">實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfa6b-122">The name of the instance.</span></span>

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

### <span data-ttu-id="cfa6b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="cfa6b-123">-Name</span></span>
<span data-ttu-id="cfa6b-124">作業名稱。</span><span class="sxs-lookup"><span data-stu-id="cfa6b-124">The name of the operation.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DefaultParameterSet
Aliases: OperationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa6b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfa6b-125">-ResourceGroupName</span></span>
<span data-ttu-id="cfa6b-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfa6b-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="cfa6b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfa6b-127">-ResourceId</span></span>
<span data-ttu-id="cfa6b-128">Managed instance 操作資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cfa6b-128">The managed instance operation resource identifier.</span></span>

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

### <span data-ttu-id="cfa6b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa6b-129">CommonParameters</span></span>
<span data-ttu-id="cfa6b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cfa6b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa6b-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cfa6b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa6b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="cfa6b-132">INPUTS</span></span>

### <span data-ttu-id="cfa6b-133">System.object</span><span class="sxs-lookup"><span data-stu-id="cfa6b-133">System.String</span></span>

## <span data-ttu-id="cfa6b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="cfa6b-134">OUTPUTS</span></span>

### <span data-ttu-id="cfa6b-135">AzureSqlManagedInstanceOperationModel 中的 [ManagedInstanceOperation]</span><span class="sxs-lookup"><span data-stu-id="cfa6b-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="cfa6b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="cfa6b-136">NOTES</span></span>

## <span data-ttu-id="cfa6b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="cfa6b-137">RELATED LINKS</span></span>
