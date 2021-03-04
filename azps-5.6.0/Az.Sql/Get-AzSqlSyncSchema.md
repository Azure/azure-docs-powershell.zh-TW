---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: e32f693b5f0bfc114f3ac40a4fc5761ec3a3ca70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914257"
---
# <span data-ttu-id="96b52-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="96b52-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="96b52-102">簡介</span><span class="sxs-lookup"><span data-stu-id="96b52-102">SYNOPSIS</span></span>
<span data-ttu-id="96b52-103">會返回成員資料庫或中樞資料庫的同步架構相關資訊。</span><span class="sxs-lookup"><span data-stu-id="96b52-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="96b52-104">語法</span><span class="sxs-lookup"><span data-stu-id="96b52-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96b52-105">描述</span><span class="sxs-lookup"><span data-stu-id="96b52-105">DESCRIPTION</span></span>
<span data-ttu-id="96b52-106">**Get-AzSqlSyncSchema Cmdlet** 會返回成員資料庫或中樞資料庫的同步架構相關資訊。</span><span class="sxs-lookup"><span data-stu-id="96b52-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="96b52-107">例子</span><span class="sxs-lookup"><span data-stu-id="96b52-107">EXAMPLES</span></span>

### <span data-ttu-id="96b52-108">範例 1：取得中樞資料庫的同步架構</span><span class="sxs-lookup"><span data-stu-id="96b52-108">Example 1: Get the sync schema for a hub database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="96b52-109">此命令會獲得同步群組同步組同步組01 中中樞資料庫的同步架構。</span><span class="sxs-lookup"><span data-stu-id="96b52-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="96b52-110">範例 2：取得中樞資料庫的同步架構，然後展開資料表</span><span class="sxs-lookup"><span data-stu-id="96b52-110">Example 2: Get the sync schema for a hub database, and expand Tables</span></span>
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

<span data-ttu-id="96b52-111">此命令會針對同步群組 SyncGroup01 中的中樞資料庫，獲得同步架構架構，並展開資料表屬性。</span><span class="sxs-lookup"><span data-stu-id="96b52-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="96b52-112">範例 3：取得成員資料庫的同步架構</span><span class="sxs-lookup"><span data-stu-id="96b52-112">Example 3: Get the sync schema for a member database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="96b52-113">此命令會獲得同步成員 SyncMember01 中成員資料庫的同步架構。</span><span class="sxs-lookup"><span data-stu-id="96b52-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="96b52-114">參數</span><span class="sxs-lookup"><span data-stu-id="96b52-114">PARAMETERS</span></span>

### <span data-ttu-id="96b52-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="96b52-115">-DatabaseName</span></span>
<span data-ttu-id="96b52-116">Azure SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="96b52-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="96b52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b52-117">-DefaultProfile</span></span>
<span data-ttu-id="96b52-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="96b52-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96b52-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96b52-119">-ResourceGroupName</span></span>
<span data-ttu-id="96b52-120">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="96b52-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="96b52-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="96b52-121">-ServerName</span></span>
<span data-ttu-id="96b52-122">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="96b52-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="96b52-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="96b52-123">-SyncGroupName</span></span>
<span data-ttu-id="96b52-124">同步組名。</span><span class="sxs-lookup"><span data-stu-id="96b52-124">The sync group name.</span></span>

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

### <span data-ttu-id="96b52-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="96b52-125">-SyncMemberName</span></span>
<span data-ttu-id="96b52-126">同步成員名稱。</span><span class="sxs-lookup"><span data-stu-id="96b52-126">The sync member name.</span></span>

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

### <span data-ttu-id="96b52-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b52-127">CommonParameters</span></span>
<span data-ttu-id="96b52-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="96b52-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b52-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96b52-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b52-130">輸入</span><span class="sxs-lookup"><span data-stu-id="96b52-130">INPUTS</span></span>

### <span data-ttu-id="96b52-131">System.String</span><span class="sxs-lookup"><span data-stu-id="96b52-131">System.String</span></span>

## <span data-ttu-id="96b52-132">輸出</span><span class="sxs-lookup"><span data-stu-id="96b52-132">OUTPUTS</span></span>

### <span data-ttu-id="96b52-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="96b52-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="96b52-134">筆記</span><span class="sxs-lookup"><span data-stu-id="96b52-134">NOTES</span></span>

## <span data-ttu-id="96b52-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="96b52-135">RELATED LINKS</span></span>
