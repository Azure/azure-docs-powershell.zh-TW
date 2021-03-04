---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 7b23bd6082fc79ff6096f496117c0ff6b63fd134
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905793"
---
# <span data-ttu-id="edc65-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="edc65-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="edc65-102">簡介</span><span class="sxs-lookup"><span data-stu-id="edc65-102">SYNOPSIS</span></span>
<span data-ttu-id="edc65-103">獲取或列出 Azure SQL 資料庫容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="edc65-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="edc65-104">語法</span><span class="sxs-lookup"><span data-stu-id="edc65-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edc65-105">描述</span><span class="sxs-lookup"><span data-stu-id="edc65-105">DESCRIPTION</span></span>
<span data-ttu-id="edc65-106">在伺服器上獲得特定的 Azure SQL 資料庫容錯移轉群組或列出容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="edc65-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="edc65-107">容錯移轉群組中的任一伺服器都可以用來執行命令。</span><span class="sxs-lookup"><span data-stu-id="edc65-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="edc65-108">所返回的值會反映指定伺服器與容錯移轉群組有關的狀態。</span><span class="sxs-lookup"><span data-stu-id="edc65-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="edc65-109">例子</span><span class="sxs-lookup"><span data-stu-id="edc65-109">EXAMPLES</span></span>

### <span data-ttu-id="edc65-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="edc65-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="edc65-111">列出伺服器上所有容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="edc65-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="edc65-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="edc65-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="edc65-113">取得特定的容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="edc65-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="edc65-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="edc65-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="edc65-115">取得伺服器中以 "fg" 開始的所有容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="edc65-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="edc65-116">參數</span><span class="sxs-lookup"><span data-stu-id="edc65-116">PARAMETERS</span></span>

### <span data-ttu-id="edc65-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc65-117">-DefaultProfile</span></span>
<span data-ttu-id="edc65-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="edc65-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edc65-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="edc65-119">-FailoverGroupName</span></span>
<span data-ttu-id="edc65-120">要取回的 Azure SQL 資料庫容錯移轉組名。</span><span class="sxs-lookup"><span data-stu-id="edc65-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edc65-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edc65-121">-ResourceGroupName</span></span>
<span data-ttu-id="edc65-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="edc65-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="edc65-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="edc65-123">-ServerName</span></span>
<span data-ttu-id="edc65-124">用於取回容錯移轉群組的 Azure SQL Database Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="edc65-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="edc65-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc65-125">CommonParameters</span></span>
<span data-ttu-id="edc65-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="edc65-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc65-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edc65-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc65-128">輸入</span><span class="sxs-lookup"><span data-stu-id="edc65-128">INPUTS</span></span>

### <span data-ttu-id="edc65-129">System.String</span><span class="sxs-lookup"><span data-stu-id="edc65-129">System.String</span></span>

## <span data-ttu-id="edc65-130">輸出</span><span class="sxs-lookup"><span data-stu-id="edc65-130">OUTPUTS</span></span>

### <span data-ttu-id="edc65-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="edc65-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="edc65-132">筆記</span><span class="sxs-lookup"><span data-stu-id="edc65-132">NOTES</span></span>

## <span data-ttu-id="edc65-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="edc65-133">RELATED LINKS</span></span>

[<span data-ttu-id="edc65-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="edc65-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="edc65-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="edc65-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="edc65-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="edc65-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="edc65-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="edc65-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="edc65-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="edc65-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="edc65-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="edc65-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="edc65-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="edc65-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
