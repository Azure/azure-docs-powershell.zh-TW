---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 4cb97982ed3649502bcf11ce471cef0231ae3058
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905798"
---
# <span data-ttu-id="352f0-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="352f0-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="352f0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="352f0-102">SYNOPSIS</span></span>
<span data-ttu-id="352f0-103">獲得備份的短期保留政策。</span><span class="sxs-lookup"><span data-stu-id="352f0-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="352f0-104">語法</span><span class="sxs-lookup"><span data-stu-id="352f0-104">SYNTAX</span></span>

### <span data-ttu-id="352f0-105">PolicyByResourceServerDatabaseSet (預設) </span><span class="sxs-lookup"><span data-stu-id="352f0-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="352f0-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="352f0-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="352f0-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="352f0-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="352f0-108">描述</span><span class="sxs-lookup"><span data-stu-id="352f0-108">DESCRIPTION</span></span>
<span data-ttu-id="352f0-109">**Get-AzSqlDatabaseBackupShortTermRetentionPolidlet** 會取得註冊至此資料庫的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="352f0-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="352f0-110">此為時間點還原備份的保留期間 ，以天數表示。</span><span class="sxs-lookup"><span data-stu-id="352f0-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="352f0-111">例子</span><span class="sxs-lookup"><span data-stu-id="352f0-111">EXAMPLES</span></span>

### <span data-ttu-id="352f0-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="352f0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="352f0-113">此命令會獲得資料庫01 的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="352f0-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="352f0-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="352f0-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="352f0-115">此命令會透過資料庫物件的管道，獲得資料庫01 的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="352f0-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="352f0-116">參數</span><span class="sxs-lookup"><span data-stu-id="352f0-116">PARAMETERS</span></span>

### <span data-ttu-id="352f0-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="352f0-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="352f0-118">要取得其策略的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="352f0-118">The database object to get the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="352f0-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="352f0-119">-DatabaseName</span></span>
<span data-ttu-id="352f0-120">要使用的 Azure SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="352f0-120">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="352f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="352f0-121">-DefaultProfile</span></span>
<span data-ttu-id="352f0-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="352f0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="352f0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="352f0-123">-ResourceGroupName</span></span>
<span data-ttu-id="352f0-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="352f0-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="352f0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="352f0-125">-ResourceId</span></span>
<span data-ttu-id="352f0-126">短期保留政策資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="352f0-126">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="352f0-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="352f0-127">-ServerName</span></span>
<span data-ttu-id="352f0-128">資料庫位於中的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="352f0-128">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="352f0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="352f0-129">CommonParameters</span></span>
<span data-ttu-id="352f0-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="352f0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="352f0-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="352f0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="352f0-132">輸入</span><span class="sxs-lookup"><span data-stu-id="352f0-132">INPUTS</span></span>

### <span data-ttu-id="352f0-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="352f0-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="352f0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="352f0-134">System.String</span></span>

## <span data-ttu-id="352f0-135">輸出</span><span class="sxs-lookup"><span data-stu-id="352f0-135">OUTPUTS</span></span>

### <span data-ttu-id="352f0-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="352f0-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="352f0-137">筆記</span><span class="sxs-lookup"><span data-stu-id="352f0-137">NOTES</span></span>

## <span data-ttu-id="352f0-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="352f0-138">RELATED LINKS</span></span>
