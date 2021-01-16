---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: 7dc07f1064837b710c246e4aafb4ceb008019e4e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274619"
---
# <span data-ttu-id="cc35a-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="cc35a-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="cc35a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc35a-102">SYNOPSIS</span></span>
<span data-ttu-id="cc35a-103">傳回成員資料庫或中心資料庫同步處理架構的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cc35a-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="cc35a-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc35a-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc35a-105">說明</span><span class="sxs-lookup"><span data-stu-id="cc35a-105">DESCRIPTION</span></span>
<span data-ttu-id="cc35a-106">**AzSqlSyncSchema** Cmdlet 會傳回成員資料庫或中心資料庫同步處理架構的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cc35a-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="cc35a-107">示例</span><span class="sxs-lookup"><span data-stu-id="cc35a-107">EXAMPLES</span></span>

### <span data-ttu-id="cc35a-108">範例1：取得中心資料庫的同步處理架構</span><span class="sxs-lookup"><span data-stu-id="cc35a-108">Example 1: Get the sync schema for a hub database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="cc35a-109">這個命令會在同步處理群組 syncGroup01 中取得中心資料庫的同步處理架構。</span><span class="sxs-lookup"><span data-stu-id="cc35a-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="cc35a-110">範例2：取得中心資料庫的同步處理架構，並展開資料表</span><span class="sxs-lookup"><span data-stu-id="cc35a-110">Example 2: Get the sync schema for a hub database, and expand Tables</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
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

<span data-ttu-id="cc35a-111">這個命令會在 [同步處理群組 syncGroup01] 和 [展開表格] 屬性中取得中心資料庫的同步處理架構。</span><span class="sxs-lookup"><span data-stu-id="cc35a-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="cc35a-112">範例3：取得成員資料庫的同步處理架構</span><span class="sxs-lookup"><span data-stu-id="cc35a-112">Example 3: Get the sync schema for a member database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="cc35a-113">這個命令會在同步處理成員 syncMember01 中取得成員資料庫的同步處理架構。</span><span class="sxs-lookup"><span data-stu-id="cc35a-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="cc35a-114">參數</span><span class="sxs-lookup"><span data-stu-id="cc35a-114">PARAMETERS</span></span>

### <span data-ttu-id="cc35a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cc35a-115">-DatabaseName</span></span>
<span data-ttu-id="cc35a-116">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc35a-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="cc35a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc35a-117">-DefaultProfile</span></span>
<span data-ttu-id="cc35a-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cc35a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc35a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc35a-119">-ResourceGroupName</span></span>
<span data-ttu-id="cc35a-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc35a-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="cc35a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cc35a-121">-ServerName</span></span>
<span data-ttu-id="cc35a-122">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc35a-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="cc35a-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="cc35a-123">-SyncGroupName</span></span>
<span data-ttu-id="cc35a-124">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="cc35a-124">The sync group name.</span></span>

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

### <span data-ttu-id="cc35a-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="cc35a-125">-SyncMemberName</span></span>
<span data-ttu-id="cc35a-126">同步處理成員名稱。</span><span class="sxs-lookup"><span data-stu-id="cc35a-126">The sync member name.</span></span>

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

### <span data-ttu-id="cc35a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc35a-127">CommonParameters</span></span>
<span data-ttu-id="cc35a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc35a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc35a-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cc35a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc35a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="cc35a-130">INPUTS</span></span>

### <span data-ttu-id="cc35a-131">System.object</span><span class="sxs-lookup"><span data-stu-id="cc35a-131">System.String</span></span>

## <span data-ttu-id="cc35a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="cc35a-132">OUTPUTS</span></span>

### <span data-ttu-id="cc35a-133">AzureSqlSyncFullSchemaModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="cc35a-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="cc35a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="cc35a-134">NOTES</span></span>

## <span data-ttu-id="cc35a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc35a-135">RELATED LINKS</span></span>
