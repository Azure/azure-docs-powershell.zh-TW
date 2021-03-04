---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: adc3bc9c8d367da6f031f8847cee7ce48b3f9b43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904269"
---
# <span data-ttu-id="a6691-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a6691-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="a6691-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a6691-102">SYNOPSIS</span></span>
<span data-ttu-id="a6691-103">移除 Azure SQL 資料庫容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="a6691-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="a6691-104">語法</span><span class="sxs-lookup"><span data-stu-id="a6691-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6691-105">描述</span><span class="sxs-lookup"><span data-stu-id="a6691-105">DESCRIPTION</span></span>
<span data-ttu-id="a6691-106">此命令會移除具有指定名稱的容錯移轉群組，並保留所有資料庫和複製關係。</span><span class="sxs-lookup"><span data-stu-id="a6691-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="a6691-107">會從 DNS 取消註冊聆聽者端點。</span><span class="sxs-lookup"><span data-stu-id="a6691-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="a6691-108">容錯移轉群組的主伺服器應該用來執行命令。</span><span class="sxs-lookup"><span data-stu-id="a6691-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="a6691-109">例子</span><span class="sxs-lookup"><span data-stu-id="a6691-109">EXAMPLES</span></span>

### <span data-ttu-id="a6691-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="a6691-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="a6691-111">移除容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="a6691-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="a6691-112">參數</span><span class="sxs-lookup"><span data-stu-id="a6691-112">PARAMETERS</span></span>

### <span data-ttu-id="a6691-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6691-113">-DefaultProfile</span></span>
<span data-ttu-id="a6691-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a6691-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6691-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="a6691-115">-FailoverGroupName</span></span>
<span data-ttu-id="a6691-116">要移除的 Azure SQL 資料庫容錯移轉組名。</span><span class="sxs-lookup"><span data-stu-id="a6691-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="a6691-117">-強制</span><span class="sxs-lookup"><span data-stu-id="a6691-117">-Force</span></span>
<span data-ttu-id="a6691-118">跳過執行動作的確認訊息。</span><span class="sxs-lookup"><span data-stu-id="a6691-118">Skip confirmation message for performing the action.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6691-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6691-119">-ResourceGroupName</span></span>
<span data-ttu-id="a6691-120">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6691-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a6691-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a6691-121">-ServerName</span></span>
<span data-ttu-id="a6691-122">容錯移轉群組的主要 Azure SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a6691-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="a6691-123">-確認</span><span class="sxs-lookup"><span data-stu-id="a6691-123">-Confirm</span></span>
<span data-ttu-id="a6691-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a6691-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6691-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6691-125">-WhatIf</span></span>
<span data-ttu-id="a6691-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6691-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6691-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6691-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6691-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6691-128">CommonParameters</span></span>
<span data-ttu-id="a6691-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a6691-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6691-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6691-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6691-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a6691-131">INPUTS</span></span>

### <span data-ttu-id="a6691-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a6691-132">System.String</span></span>

## <span data-ttu-id="a6691-133">輸出</span><span class="sxs-lookup"><span data-stu-id="a6691-133">OUTPUTS</span></span>

### <span data-ttu-id="a6691-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="a6691-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="a6691-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a6691-135">NOTES</span></span>

## <span data-ttu-id="a6691-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6691-136">RELATED LINKS</span></span>

[<span data-ttu-id="a6691-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a6691-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a6691-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a6691-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a6691-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a6691-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a6691-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a6691-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="a6691-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a6691-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="a6691-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a6691-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a6691-143">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="a6691-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
