---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 283a7963d7dcf278f203385bd790bd19cadc9d7c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138082"
---
# <span data-ttu-id="4f034-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4f034-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="4f034-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f034-102">SYNOPSIS</span></span>
<span data-ttu-id="4f034-103">移除 [Azure SQL 資料庫容錯移轉] 群組。</span><span class="sxs-lookup"><span data-stu-id="4f034-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="4f034-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f034-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f034-105">說明</span><span class="sxs-lookup"><span data-stu-id="4f034-105">DESCRIPTION</span></span>
<span data-ttu-id="4f034-106">這個命令會移除具有指定名稱的容錯移轉群組，並將所有資料庫與複製關聯保持不變。</span><span class="sxs-lookup"><span data-stu-id="4f034-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="4f034-107">將會從 DNS 登出偵聽程式端點。</span><span class="sxs-lookup"><span data-stu-id="4f034-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="4f034-108">應使用容錯移轉群組的主要伺服器來執行命令。</span><span class="sxs-lookup"><span data-stu-id="4f034-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="4f034-109">示例</span><span class="sxs-lookup"><span data-stu-id="4f034-109">EXAMPLES</span></span>

### <span data-ttu-id="4f034-110">範例1</span><span class="sxs-lookup"><span data-stu-id="4f034-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="4f034-111">移除容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="4f034-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="4f034-112">參數</span><span class="sxs-lookup"><span data-stu-id="4f034-112">PARAMETERS</span></span>

### <span data-ttu-id="4f034-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f034-113">-DefaultProfile</span></span>
<span data-ttu-id="4f034-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4f034-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f034-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="4f034-115">-FailoverGroupName</span></span>
<span data-ttu-id="4f034-116">要移除之 Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f034-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="4f034-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4f034-117">-Force</span></span>
<span data-ttu-id="4f034-118">跳過確認訊息以執行動作。</span><span class="sxs-lookup"><span data-stu-id="4f034-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="4f034-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f034-119">-ResourceGroupName</span></span>
<span data-ttu-id="4f034-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f034-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="4f034-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4f034-121">-ServerName</span></span>
<span data-ttu-id="4f034-122">容錯移轉群組之主要 Azure SQL Database 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f034-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="4f034-123">-確認</span><span class="sxs-lookup"><span data-stu-id="4f034-123">-Confirm</span></span>
<span data-ttu-id="4f034-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4f034-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f034-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f034-125">-WhatIf</span></span>
<span data-ttu-id="4f034-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4f034-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f034-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f034-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f034-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f034-128">CommonParameters</span></span>
<span data-ttu-id="4f034-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f034-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f034-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4f034-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f034-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4f034-131">INPUTS</span></span>

### <span data-ttu-id="4f034-132">System.object</span><span class="sxs-lookup"><span data-stu-id="4f034-132">System.String</span></span>

## <span data-ttu-id="4f034-133">輸出</span><span class="sxs-lookup"><span data-stu-id="4f034-133">OUTPUTS</span></span>

### <span data-ttu-id="4f034-134">AzureSqlFailoverGroupModel 中的 [FailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="4f034-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="4f034-135">筆記</span><span class="sxs-lookup"><span data-stu-id="4f034-135">NOTES</span></span>

## <span data-ttu-id="4f034-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f034-136">RELATED LINKS</span></span>

[<span data-ttu-id="4f034-137">新-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4f034-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4f034-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4f034-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4f034-139">AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4f034-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4f034-140">附加 AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4f034-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="4f034-141">移除-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4f034-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="4f034-142">切換 AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4f034-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4f034-143">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="4f034-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
