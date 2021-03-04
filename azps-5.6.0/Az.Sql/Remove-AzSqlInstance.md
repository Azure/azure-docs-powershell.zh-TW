---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: a8985d77ba1bbf33e49f353ad39d287f7bd3979b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902710"
---
# <span data-ttu-id="cb3bb-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb3bb-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="cb3bb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cb3bb-102">SYNOPSIS</span></span>
<span data-ttu-id="cb3bb-103">移除 Azure SQL Managed 資料庫實例。</span><span class="sxs-lookup"><span data-stu-id="cb3bb-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="cb3bb-104">語法</span><span class="sxs-lookup"><span data-stu-id="cb3bb-104">SYNTAX</span></span>

### <span data-ttu-id="cb3bb-105">RemoveInstanceFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="cb3bb-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb3bb-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="cb3bb-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb3bb-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="cb3bb-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb3bb-108">描述</span><span class="sxs-lookup"><span data-stu-id="cb3bb-108">DESCRIPTION</span></span>
<span data-ttu-id="cb3bb-109">**Remove-AzSqlInstance Cmdlet** 會移除 Azure SQL Database Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="cb3bb-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="cb3bb-110">例子</span><span class="sxs-lookup"><span data-stu-id="cb3bb-110">EXAMPLES</span></span>

### <span data-ttu-id="cb3bb-111">範例 1：移除實例</span><span class="sxs-lookup"><span data-stu-id="cb3bb-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cb3bb-112">此命令會移除名為 managedInstance1 的實例。</span><span class="sxs-lookup"><span data-stu-id="cb3bb-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="cb3bb-113">參數</span><span class="sxs-lookup"><span data-stu-id="cb3bb-113">PARAMETERS</span></span>

### <span data-ttu-id="cb3bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb3bb-114">-DefaultProfile</span></span>
<span data-ttu-id="cb3bb-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb3bb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb3bb-116">-強制</span><span class="sxs-lookup"><span data-stu-id="cb3bb-116">-Force</span></span>
<span data-ttu-id="cb3bb-117">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="cb3bb-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="cb3bb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb3bb-118">-InputObject</span></span>
<span data-ttu-id="cb3bb-119">要移除的 AzureSqlManagedInstanceModel 物件</span><span class="sxs-lookup"><span data-stu-id="cb3bb-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb3bb-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb3bb-120">-Name</span></span>
<span data-ttu-id="cb3bb-121">SQL 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="cb3bb-121">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb3bb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb3bb-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb3bb-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb3bb-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb3bb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb3bb-124">-ResourceId</span></span>
<span data-ttu-id="cb3bb-125">要移除的實例物件資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cb3bb-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb3bb-126">-確認</span><span class="sxs-lookup"><span data-stu-id="cb3bb-126">-Confirm</span></span>
<span data-ttu-id="cb3bb-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cb3bb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb3bb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb3bb-128">-WhatIf</span></span>
<span data-ttu-id="cb3bb-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb3bb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb3bb-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb3bb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb3bb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb3bb-131">CommonParameters</span></span>
<span data-ttu-id="cb3bb-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cb3bb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb3bb-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb3bb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb3bb-134">輸入</span><span class="sxs-lookup"><span data-stu-id="cb3bb-134">INPUTS</span></span>

### <span data-ttu-id="cb3bb-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="cb3bb-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="cb3bb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="cb3bb-136">System.String</span></span>

## <span data-ttu-id="cb3bb-137">輸出</span><span class="sxs-lookup"><span data-stu-id="cb3bb-137">OUTPUTS</span></span>

### <span data-ttu-id="cb3bb-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="cb3bb-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="cb3bb-139">筆記</span><span class="sxs-lookup"><span data-stu-id="cb3bb-139">NOTES</span></span>

## <span data-ttu-id="cb3bb-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb3bb-140">RELATED LINKS</span></span>
