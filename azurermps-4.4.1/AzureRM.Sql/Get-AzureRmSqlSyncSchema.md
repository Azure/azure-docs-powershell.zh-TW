---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
ms.openlocfilehash: ef66de2b12cf0ea723540c392a296d2d1c482505
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446633"
---
# <span data-ttu-id="26db8-101">Get-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="26db8-101">Get-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="26db8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26db8-102">SYNOPSIS</span></span>
<span data-ttu-id="26db8-103">傳回成員資料庫或中心資料庫同步處理架構的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26db8-103">Returns information about the sync schema of a member database or a hub database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26db8-104">句法</span><span class="sxs-lookup"><span data-stu-id="26db8-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26db8-105">說明</span><span class="sxs-lookup"><span data-stu-id="26db8-105">DESCRIPTION</span></span>
<span data-ttu-id="26db8-106">**AzureRmSqlSyncSchema** Cmdlet 會傳回成員資料庫或中心資料庫同步處理架構的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26db8-106">The **Get-AzureRmSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="26db8-107">示例</span><span class="sxs-lookup"><span data-stu-id="26db8-107">EXAMPLES</span></span>

### <span data-ttu-id="26db8-108">範例1.1：取得中心資料庫的同步處理架構</span><span class="sxs-lookup"><span data-stu-id="26db8-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="26db8-109">這個命令會在同步處理群組 syncGroup01 中取得中心資料庫的同步處理架構。</span><span class="sxs-lookup"><span data-stu-id="26db8-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="26db8-110">範例1.2：取得中心資料庫的同步處理架構，以及展開資料表</span><span class="sxs-lookup"><span data-stu-id="26db8-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
Columns    : {column1, column2}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_1
QuotedName : [dbo].[Table_1]

Columns    : {column2, column4}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_2
QuotedName : [dbo].[Table_2]
```

<span data-ttu-id="26db8-111">這個命令會在 [同步處理群組 syncGroup01] 和 [展開表格] 屬性中取得中心資料庫的同步處理架構。</span><span class="sxs-lookup"><span data-stu-id="26db8-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="26db8-112">範例2：取得成員資料庫的同步處理架構</span><span class="sxs-lookup"><span data-stu-id="26db8-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="26db8-113">這個命令會在同步處理成員 syncMember01 中取得成員資料庫的同步處理架構。</span><span class="sxs-lookup"><span data-stu-id="26db8-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="26db8-114">參數</span><span class="sxs-lookup"><span data-stu-id="26db8-114">PARAMETERS</span></span>

### <span data-ttu-id="26db8-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="26db8-115">-DatabaseName</span></span>
<span data-ttu-id="26db8-116">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="26db8-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="26db8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26db8-117">-ResourceGroupName</span></span>
<span data-ttu-id="26db8-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26db8-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="26db8-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="26db8-119">-ServerName</span></span>
<span data-ttu-id="26db8-120">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="26db8-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="26db8-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="26db8-121">-SyncGroupName</span></span>
<span data-ttu-id="26db8-122">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="26db8-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26db8-123">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="26db8-123">-SyncMemberName</span></span>
<span data-ttu-id="26db8-124">同步處理成員名稱。</span><span class="sxs-lookup"><span data-stu-id="26db8-124">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26db8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26db8-125">-DefaultProfile</span></span>
<span data-ttu-id="26db8-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26db8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26db8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26db8-127">CommonParameters</span></span>
<span data-ttu-id="26db8-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26db8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26db8-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26db8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26db8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="26db8-130">INPUTS</span></span>

## <span data-ttu-id="26db8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="26db8-131">OUTPUTS</span></span>

### <span data-ttu-id="26db8-132">AzureSqlSyncFullSchemaModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="26db8-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

### <span data-ttu-id="26db8-133">資料表： DataSync. AzureSqlSyncFullSchemaTableModel （.Sql）</span><span class="sxs-lookup"><span data-stu-id="26db8-133">Tables: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaTableModel</span></span>

### <span data-ttu-id="26db8-134">[欄]： AzureSqlSyncFullSchemaColumnModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="26db8-134">Columns: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaColumnModel</span></span>

## <span data-ttu-id="26db8-135">筆記</span><span class="sxs-lookup"><span data-stu-id="26db8-135">NOTES</span></span>

## <span data-ttu-id="26db8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="26db8-136">RELATED LINKS</span></span>

