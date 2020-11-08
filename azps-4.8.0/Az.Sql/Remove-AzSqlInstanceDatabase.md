---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: a496bd4ba68d9d62bdfe65dc293c68377b7d3aa6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129847"
---
# <span data-ttu-id="ce246-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ce246-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="ce246-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce246-102">SYNOPSIS</span></span>
<span data-ttu-id="ce246-103">移除 Azure SQL Managed 實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="ce246-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="ce246-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce246-104">SYNTAX</span></span>

### <span data-ttu-id="ce246-105">RemoveInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="ce246-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce246-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="ce246-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce246-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="ce246-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce246-108">說明</span><span class="sxs-lookup"><span data-stu-id="ce246-108">DESCRIPTION</span></span>
<span data-ttu-id="ce246-109">**AzSqlInstanceDatabase** Cmdlet 會移除 Azure SQL Managed 實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="ce246-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="ce246-110">示例</span><span class="sxs-lookup"><span data-stu-id="ce246-110">EXAMPLES</span></span>

### <span data-ttu-id="ce246-111">範例1：從實例中移除資料庫</span><span class="sxs-lookup"><span data-stu-id="ce246-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ce246-112">這個命令會從實例 managedInstance1 中移除名為 Database01 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="ce246-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="ce246-113">參數</span><span class="sxs-lookup"><span data-stu-id="ce246-113">PARAMETERS</span></span>

### <span data-ttu-id="ce246-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce246-114">-DefaultProfile</span></span>
<span data-ttu-id="ce246-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce246-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce246-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ce246-116">-Force</span></span>
<span data-ttu-id="ce246-117">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="ce246-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ce246-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce246-118">-InputObject</span></span>
<span data-ttu-id="ce246-119">要移除的實例資料庫物件</span><span class="sxs-lookup"><span data-stu-id="ce246-119">The Instance Database object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce246-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ce246-120">-InstanceName</span></span>
<span data-ttu-id="ce246-121">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="ce246-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce246-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce246-122">-Name</span></span>
<span data-ttu-id="ce246-123">要移除之 Azure SQL 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce246-123">The name of the Azure SQL Instance Database to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce246-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce246-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce246-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce246-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce246-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce246-126">-ResourceId</span></span>
<span data-ttu-id="ce246-127">要移除之實例資料庫物件的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ce246-127">The resource id of Instance Database object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce246-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ce246-128">-Confirm</span></span>
<span data-ttu-id="ce246-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce246-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce246-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce246-130">-WhatIf</span></span>
<span data-ttu-id="ce246-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce246-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce246-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce246-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce246-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce246-133">CommonParameters</span></span>
<span data-ttu-id="ce246-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce246-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce246-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ce246-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce246-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ce246-136">INPUTS</span></span>

### <span data-ttu-id="ce246-137">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="ce246-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="ce246-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ce246-138">System.String</span></span>

## <span data-ttu-id="ce246-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ce246-139">OUTPUTS</span></span>

### <span data-ttu-id="ce246-140">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="ce246-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="ce246-141">筆記</span><span class="sxs-lookup"><span data-stu-id="ce246-141">NOTES</span></span>

## <span data-ttu-id="ce246-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce246-142">RELATED LINKS</span></span>