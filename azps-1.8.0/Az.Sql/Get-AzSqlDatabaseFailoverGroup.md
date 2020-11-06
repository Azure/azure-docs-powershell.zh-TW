---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 430c4cc1318d53ebb2671b9fb1dd0cea8655898d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620482"
---
# <span data-ttu-id="a2d0c-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a2d0c-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="a2d0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d0c-103">取得或列出 Azure SQL Database 容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="a2d0c-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="a2d0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2d0c-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2d0c-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2d0c-105">DESCRIPTION</span></span>
<span data-ttu-id="a2d0c-106">取得特定的 Azure SQL Database 容錯移轉群組，或列出伺服器上的容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="a2d0c-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="a2d0c-107">[容錯移轉] 群組中的任何一個伺服器都可以用來執行命令。</span><span class="sxs-lookup"><span data-stu-id="a2d0c-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="a2d0c-108">傳回的值將反映特定伺服器相對於容錯移轉群組的狀態。</span><span class="sxs-lookup"><span data-stu-id="a2d0c-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="a2d0c-109">示例</span><span class="sxs-lookup"><span data-stu-id="a2d0c-109">EXAMPLES</span></span>

### <span data-ttu-id="a2d0c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a2d0c-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="a2d0c-111">列出伺服器上的所有容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="a2d0c-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="a2d0c-112">範例2</span><span class="sxs-lookup"><span data-stu-id="a2d0c-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="a2d0c-113">取得特定的容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="a2d0c-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="a2d0c-114">範例3</span><span class="sxs-lookup"><span data-stu-id="a2d0c-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="a2d0c-115">在以 "fg" 開頭的伺服器中取得所有容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="a2d0c-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="a2d0c-116">參數</span><span class="sxs-lookup"><span data-stu-id="a2d0c-116">PARAMETERS</span></span>

### <span data-ttu-id="a2d0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d0c-117">-DefaultProfile</span></span>
<span data-ttu-id="a2d0c-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a2d0c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2d0c-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d0c-119">-FailoverGroupName</span></span>
<span data-ttu-id="a2d0c-120">要檢索之 Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2d0c-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a2d0c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d0c-121">-ResourceGroupName</span></span>
<span data-ttu-id="a2d0c-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2d0c-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a2d0c-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a2d0c-123">-ServerName</span></span>
<span data-ttu-id="a2d0c-124">要從中檢索容錯移轉群組的 Azure SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a2d0c-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="a2d0c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d0c-125">CommonParameters</span></span>
<span data-ttu-id="a2d0c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2d0c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d0c-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a2d0c-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d0c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a2d0c-128">INPUTS</span></span>

### <span data-ttu-id="a2d0c-129">System.object</span><span class="sxs-lookup"><span data-stu-id="a2d0c-129">System.String</span></span>

## <span data-ttu-id="a2d0c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a2d0c-130">OUTPUTS</span></span>

### <span data-ttu-id="a2d0c-131">AzureSqlFailoverGroupModel 中的 [FailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="a2d0c-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="a2d0c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a2d0c-132">NOTES</span></span>

## <span data-ttu-id="a2d0c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2d0c-133">RELATED LINKS</span></span>

[<span data-ttu-id="a2d0c-134">新-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a2d0c-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a2d0c-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a2d0c-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a2d0c-136">附加 AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a2d0c-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="a2d0c-137">移除-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a2d0c-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="a2d0c-138">切換 AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a2d0c-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a2d0c-139">移除-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a2d0c-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a2d0c-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="a2d0c-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
