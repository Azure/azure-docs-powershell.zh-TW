---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: e361dc9a224649b7b1af38594145f14e24091d7a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141239"
---
# <span data-ttu-id="27a49-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="27a49-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="27a49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27a49-102">SYNOPSIS</span></span>
<span data-ttu-id="27a49-103">移除 Azure SQL Managed 資料庫實例。</span><span class="sxs-lookup"><span data-stu-id="27a49-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="27a49-104">句法</span><span class="sxs-lookup"><span data-stu-id="27a49-104">SYNTAX</span></span>

### <span data-ttu-id="27a49-105">RemoveInstanceFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="27a49-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27a49-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="27a49-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27a49-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="27a49-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27a49-108">說明</span><span class="sxs-lookup"><span data-stu-id="27a49-108">DESCRIPTION</span></span>
<span data-ttu-id="27a49-109">**AzSqlInstance** Cmdlet 會移除 Azure SQL Database Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="27a49-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="27a49-110">示例</span><span class="sxs-lookup"><span data-stu-id="27a49-110">EXAMPLES</span></span>

### <span data-ttu-id="27a49-111">範例1：移除實例</span><span class="sxs-lookup"><span data-stu-id="27a49-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="27a49-112">這個命令會移除名為 managedInstance1 的實例。</span><span class="sxs-lookup"><span data-stu-id="27a49-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="27a49-113">參數</span><span class="sxs-lookup"><span data-stu-id="27a49-113">PARAMETERS</span></span>

### <span data-ttu-id="27a49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a49-114">-DefaultProfile</span></span>
<span data-ttu-id="27a49-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="27a49-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27a49-116">-Force</span><span class="sxs-lookup"><span data-stu-id="27a49-116">-Force</span></span>
<span data-ttu-id="27a49-117">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="27a49-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="27a49-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27a49-118">-InputObject</span></span>
<span data-ttu-id="27a49-119">要移除的 AzureSqlManagedInstanceModel 物件</span><span class="sxs-lookup"><span data-stu-id="27a49-119">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="27a49-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="27a49-120">-Name</span></span>
<span data-ttu-id="27a49-121">SQL 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="27a49-121">SQL instance name.</span></span>

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

### <span data-ttu-id="27a49-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a49-122">-ResourceGroupName</span></span>
<span data-ttu-id="27a49-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="27a49-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="27a49-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27a49-124">-ResourceId</span></span>
<span data-ttu-id="27a49-125">要移除之實例物件的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="27a49-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="27a49-126">-確認</span><span class="sxs-lookup"><span data-stu-id="27a49-126">-Confirm</span></span>
<span data-ttu-id="27a49-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="27a49-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27a49-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27a49-128">-WhatIf</span></span>
<span data-ttu-id="27a49-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="27a49-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27a49-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27a49-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27a49-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a49-131">CommonParameters</span></span>
<span data-ttu-id="27a49-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27a49-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a49-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="27a49-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a49-134">輸入</span><span class="sxs-lookup"><span data-stu-id="27a49-134">INPUTS</span></span>

### <span data-ttu-id="27a49-135">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="27a49-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="27a49-136">System.object</span><span class="sxs-lookup"><span data-stu-id="27a49-136">System.String</span></span>

## <span data-ttu-id="27a49-137">輸出</span><span class="sxs-lookup"><span data-stu-id="27a49-137">OUTPUTS</span></span>

### <span data-ttu-id="27a49-138">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="27a49-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="27a49-139">筆記</span><span class="sxs-lookup"><span data-stu-id="27a49-139">NOTES</span></span>

## <span data-ttu-id="27a49-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="27a49-140">RELATED LINKS</span></span>
