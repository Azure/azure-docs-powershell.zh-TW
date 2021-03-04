---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: ce69f6b087a7ed61f415e3d6a649f757bb10178f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913078"
---
# <span data-ttu-id="2f924-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2f924-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="2f924-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2f924-102">SYNOPSIS</span></span>
<span data-ttu-id="2f924-103">移除 Azure SQL 資料庫同步組。</span><span class="sxs-lookup"><span data-stu-id="2f924-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="2f924-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f924-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f924-105">描述</span><span class="sxs-lookup"><span data-stu-id="2f924-105">DESCRIPTION</span></span>
<span data-ttu-id="2f924-106">**Remove-AzSqlSyncGroup** Cmdlet 會移除 Azure SQL 資料庫同步組。</span><span class="sxs-lookup"><span data-stu-id="2f924-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="2f924-107">例子</span><span class="sxs-lookup"><span data-stu-id="2f924-107">EXAMPLES</span></span>

### <span data-ttu-id="2f924-108">範例 1：移除同步群組</span><span class="sxs-lookup"><span data-stu-id="2f924-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="2f924-109">此命令會移除名為 syncGroup01 的 Azure SQL 資料庫同步組。</span><span class="sxs-lookup"><span data-stu-id="2f924-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="2f924-110">參數</span><span class="sxs-lookup"><span data-stu-id="2f924-110">PARAMETERS</span></span>

### <span data-ttu-id="2f924-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f924-111">-DatabaseName</span></span>
<span data-ttu-id="2f924-112">Azure SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f924-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f924-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f924-113">-DefaultProfile</span></span>
<span data-ttu-id="2f924-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2f924-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f924-115">-強制</span><span class="sxs-lookup"><span data-stu-id="2f924-115">-Force</span></span>
<span data-ttu-id="2f924-116">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="2f924-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2f924-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f924-117">-Name</span></span>
<span data-ttu-id="2f924-118">同步組名。</span><span class="sxs-lookup"><span data-stu-id="2f924-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f924-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f924-119">-PassThru</span></span>
<span data-ttu-id="2f924-120">定義是否返回已移除的同步群組</span><span class="sxs-lookup"><span data-stu-id="2f924-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="2f924-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f924-121">-ResourceGroupName</span></span>
<span data-ttu-id="2f924-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f924-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f924-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f924-123">-ServerName</span></span>
<span data-ttu-id="2f924-124">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f924-124">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f924-125">-確認</span><span class="sxs-lookup"><span data-stu-id="2f924-125">-Confirm</span></span>
<span data-ttu-id="2f924-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2f924-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f924-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f924-127">-WhatIf</span></span>
<span data-ttu-id="2f924-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f924-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f924-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f924-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f924-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f924-130">CommonParameters</span></span>
<span data-ttu-id="2f924-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2f924-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f924-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f924-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f924-133">輸入</span><span class="sxs-lookup"><span data-stu-id="2f924-133">INPUTS</span></span>

### <span data-ttu-id="2f924-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2f924-134">System.String</span></span>

## <span data-ttu-id="2f924-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2f924-135">OUTPUTS</span></span>

### <span data-ttu-id="2f924-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="2f924-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="2f924-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2f924-137">NOTES</span></span>

## <span data-ttu-id="2f924-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f924-138">RELATED LINKS</span></span>

[<span data-ttu-id="2f924-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2f924-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="2f924-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2f924-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="2f924-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2f924-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

