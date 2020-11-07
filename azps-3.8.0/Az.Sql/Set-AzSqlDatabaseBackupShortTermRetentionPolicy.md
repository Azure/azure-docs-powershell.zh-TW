---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d605262a76d27295761ce54d59d092a490da5abc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956901"
---
# <span data-ttu-id="5539e-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5539e-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="5539e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5539e-102">SYNOPSIS</span></span>
<span data-ttu-id="5539e-103">設定 [備份短期保留原則]。</span><span class="sxs-lookup"><span data-stu-id="5539e-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="5539e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5539e-104">SYNTAX</span></span>

### <span data-ttu-id="5539e-105">PolicyByResourceServerDatabaseSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5539e-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5539e-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5539e-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5539e-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5539e-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5539e-108">說明</span><span class="sxs-lookup"><span data-stu-id="5539e-108">DESCRIPTION</span></span>
<span data-ttu-id="5539e-109">**AzSqlDatabaseBackupShortTermRetentionPolicy** Cmdlet 會取得已登錄至此資料庫的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="5539e-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="5539e-110">原則是在時間點還原備份的保留期間（以天數為單位）。</span><span class="sxs-lookup"><span data-stu-id="5539e-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="5539e-111">示例</span><span class="sxs-lookup"><span data-stu-id="5539e-111">EXAMPLES</span></span>

### <span data-ttu-id="5539e-112">範例1</span><span class="sxs-lookup"><span data-stu-id="5539e-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="5539e-113">這個命令會將 database01 至35天的短期保留原則設定為。</span><span class="sxs-lookup"><span data-stu-id="5539e-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="5539e-114">範例2</span><span class="sxs-lookup"><span data-stu-id="5539e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="5539e-115">這個命令會透過 database01 到資料庫物件中的 [管道]，來設定到35天的短期限保留原則。</span><span class="sxs-lookup"><span data-stu-id="5539e-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="5539e-116">參數</span><span class="sxs-lookup"><span data-stu-id="5539e-116">PARAMETERS</span></span>

### <span data-ttu-id="5539e-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5539e-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="5539e-118">要取得原則的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="5539e-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="5539e-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5539e-119">-DatabaseName</span></span>
<span data-ttu-id="5539e-120">要使用之 Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5539e-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="5539e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5539e-121">-DefaultProfile</span></span>
<span data-ttu-id="5539e-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5539e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5539e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5539e-123">-ResourceGroupName</span></span>
<span data-ttu-id="5539e-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5539e-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="5539e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5539e-125">-ResourceId</span></span>
<span data-ttu-id="5539e-126">短期保留原則資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5539e-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="5539e-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="5539e-127">-RetentionDays</span></span>
<span data-ttu-id="5539e-128">[備份保留] 設定，以天為單位。</span><span class="sxs-lookup"><span data-stu-id="5539e-128">The backup retention setting, in days.</span></span>

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

### <span data-ttu-id="5539e-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5539e-129">-ServerName</span></span>
<span data-ttu-id="5539e-130">資料庫所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5539e-130">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="5539e-131">-確認</span><span class="sxs-lookup"><span data-stu-id="5539e-131">-Confirm</span></span>
<span data-ttu-id="5539e-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5539e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5539e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5539e-133">-WhatIf</span></span>
<span data-ttu-id="5539e-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5539e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5539e-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5539e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5539e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5539e-136">CommonParameters</span></span>
<span data-ttu-id="5539e-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5539e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5539e-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5539e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5539e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5539e-139">INPUTS</span></span>

### <span data-ttu-id="5539e-140">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="5539e-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="5539e-141">System.object</span><span class="sxs-lookup"><span data-stu-id="5539e-141">System.String</span></span>

## <span data-ttu-id="5539e-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5539e-142">OUTPUTS</span></span>

### <span data-ttu-id="5539e-143">AzureSqlDatabaseBackupShortTermRetentionPolicyModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="5539e-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="5539e-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5539e-144">NOTES</span></span>

## <span data-ttu-id="5539e-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="5539e-145">RELATED LINKS</span></span>
