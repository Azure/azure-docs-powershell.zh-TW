---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: ccdcf55b61b57b54848f3310d7366bb76e0f6805
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913038"
---
# <span data-ttu-id="086f9-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="086f9-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="086f9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="086f9-102">SYNOPSIS</span></span>
<span data-ttu-id="086f9-103">設定備份短期保留政策。</span><span class="sxs-lookup"><span data-stu-id="086f9-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="086f9-104">語法</span><span class="sxs-lookup"><span data-stu-id="086f9-104">SYNTAX</span></span>

### <span data-ttu-id="086f9-105">PolicyByResourceServerDatabaseSet (預設) </span><span class="sxs-lookup"><span data-stu-id="086f9-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="086f9-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="086f9-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="086f9-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="086f9-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="086f9-108">描述</span><span class="sxs-lookup"><span data-stu-id="086f9-108">DESCRIPTION</span></span>
<span data-ttu-id="086f9-109">**Set-AzSqlDatabaseBackupShortTermRetentionPolidlet** 會在此資料庫中註冊短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="086f9-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="086f9-110">此為時間點還原備份的保留期間 ，以天數表示。</span><span class="sxs-lookup"><span data-stu-id="086f9-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="086f9-111">例子</span><span class="sxs-lookup"><span data-stu-id="086f9-111">EXAMPLES</span></span>

### <span data-ttu-id="086f9-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="086f9-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="086f9-113">此命令將資料庫01 的短期保留政策設定為 35 天。</span><span class="sxs-lookup"><span data-stu-id="086f9-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="086f9-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="086f9-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="086f9-115">此命令會透過資料庫物件的管道將資料庫01 的短期保留政策設定為 35 天。</span><span class="sxs-lookup"><span data-stu-id="086f9-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="086f9-116">參數</span><span class="sxs-lookup"><span data-stu-id="086f9-116">PARAMETERS</span></span>

### <span data-ttu-id="086f9-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="086f9-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="086f9-118">要取得其策略的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="086f9-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="086f9-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="086f9-119">-DatabaseName</span></span>
<span data-ttu-id="086f9-120">要使用的 Azure SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="086f9-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="086f9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="086f9-121">-DefaultProfile</span></span>
<span data-ttu-id="086f9-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="086f9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="086f9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="086f9-123">-ResourceGroupName</span></span>
<span data-ttu-id="086f9-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="086f9-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="086f9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="086f9-125">-ResourceId</span></span>
<span data-ttu-id="086f9-126">短期保留政策資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="086f9-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="086f9-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="086f9-127">-RetentionDays</span></span>
<span data-ttu-id="086f9-128">備份保留設定 ，以天數表示。</span><span class="sxs-lookup"><span data-stu-id="086f9-128">The backup retention setting, in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="086f9-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="086f9-129">-ServerName</span></span>
<span data-ttu-id="086f9-130">資料庫位於中的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="086f9-130">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="086f9-131">-確認</span><span class="sxs-lookup"><span data-stu-id="086f9-131">-Confirm</span></span>
<span data-ttu-id="086f9-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="086f9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="086f9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="086f9-133">-WhatIf</span></span>
<span data-ttu-id="086f9-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="086f9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="086f9-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="086f9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="086f9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="086f9-136">CommonParameters</span></span>
<span data-ttu-id="086f9-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="086f9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="086f9-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="086f9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="086f9-139">輸入</span><span class="sxs-lookup"><span data-stu-id="086f9-139">INPUTS</span></span>

### <span data-ttu-id="086f9-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="086f9-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="086f9-141">System.String</span><span class="sxs-lookup"><span data-stu-id="086f9-141">System.String</span></span>

## <span data-ttu-id="086f9-142">輸出</span><span class="sxs-lookup"><span data-stu-id="086f9-142">OUTPUTS</span></span>

### <span data-ttu-id="086f9-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="086f9-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="086f9-144">筆記</span><span class="sxs-lookup"><span data-stu-id="086f9-144">NOTES</span></span>

## <span data-ttu-id="086f9-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="086f9-145">RELATED LINKS</span></span>
