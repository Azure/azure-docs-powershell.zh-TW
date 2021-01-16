---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 93c4c5c1fa269414b80001f9fd24f1a79c5ed4de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275915"
---
# <span data-ttu-id="f50f4-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f50f4-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="f50f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f50f4-102">SYNOPSIS</span></span>
<span data-ttu-id="f50f4-103">設定 [備份短期保留原則]。</span><span class="sxs-lookup"><span data-stu-id="f50f4-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="f50f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="f50f4-104">SYNTAX</span></span>

### <span data-ttu-id="f50f4-105">PolicyByResourceInstanceDatabaseSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f50f4-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f50f4-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f50f4-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f50f4-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f50f4-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f50f4-108">說明</span><span class="sxs-lookup"><span data-stu-id="f50f4-108">DESCRIPTION</span></span>
<span data-ttu-id="f50f4-109">**AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** Cmdlet 會取得已登錄至此資料庫的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="f50f4-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="f50f4-110">原則是在時間點還原備份的保留期間（以天數為單位）。</span><span class="sxs-lookup"><span data-stu-id="f50f4-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="f50f4-111">示例</span><span class="sxs-lookup"><span data-stu-id="f50f4-111">EXAMPLES</span></span>

### <span data-ttu-id="f50f4-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f50f4-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="f50f4-113">這個命令會將 database01 至35天的短期保留原則設定為。</span><span class="sxs-lookup"><span data-stu-id="f50f4-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="f50f4-114">範例2</span><span class="sxs-lookup"><span data-stu-id="f50f4-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="f50f4-115">這個命令會透過 database01 到資料庫物件中的 [管道]，來設定到35天的短期限保留原則。</span><span class="sxs-lookup"><span data-stu-id="f50f4-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="f50f4-116">範例3</span><span class="sxs-lookup"><span data-stu-id="f50f4-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 8
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 8

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 8
```

<span data-ttu-id="f50f4-117">這個命令會在已刪除的資料庫物件中，為以 [DB1] 命名的所有已刪除資料庫設定短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="f50f4-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="f50f4-118">注意：您只能減少已刪除資料庫的保留期間。</span><span class="sxs-lookup"><span data-stu-id="f50f4-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="f50f4-119">參數</span><span class="sxs-lookup"><span data-stu-id="f50f4-119">PARAMETERS</span></span>

### <span data-ttu-id="f50f4-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f50f4-120">-DatabaseName</span></span>
<span data-ttu-id="f50f4-121">要為其檢索備份之 Azure SQL 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f50f4-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f50f4-122">-DefaultProfile</span></span>
<span data-ttu-id="f50f4-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f50f4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f50f4-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="f50f4-124">-DeletionDate</span></span>
<span data-ttu-id="f50f4-125">要為其檢索備份的 Azure SQL 實例資料庫的刪除日期，以毫秒為單位 (（例如 2016-02-23T00：21： 22.847 Z) </span><span class="sxs-lookup"><span data-stu-id="f50f4-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f50f4-126">-InputObject</span></span>
<span data-ttu-id="f50f4-127">要取得/設定原則的即時或刪除資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="f50f4-127">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f50f4-128">-InstanceName</span></span>
<span data-ttu-id="f50f4-129">資料庫所在之 Azure SQL 託管實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="f50f4-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f50f4-130">-ResourceGroupName</span></span>
<span data-ttu-id="f50f4-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f50f4-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f50f4-132">-ResourceId</span></span>
<span data-ttu-id="f50f4-133">短期保留原則資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f50f4-133">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="f50f4-134">-RetentionDays</span></span>
<span data-ttu-id="f50f4-135">備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="f50f4-135">Days of backup retention.</span></span>

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

### <span data-ttu-id="f50f4-136">-確認</span><span class="sxs-lookup"><span data-stu-id="f50f4-136">-Confirm</span></span>
<span data-ttu-id="f50f4-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f50f4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f50f4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f50f4-138">-WhatIf</span></span>
<span data-ttu-id="f50f4-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f50f4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f50f4-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f50f4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f50f4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f50f4-141">CommonParameters</span></span>
<span data-ttu-id="f50f4-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f50f4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f50f4-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f50f4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f50f4-144">輸入</span><span class="sxs-lookup"><span data-stu-id="f50f4-144">INPUTS</span></span>

### <span data-ttu-id="f50f4-145">AzureSqlManagedDatabaseBaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="f50f4-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="f50f4-146">System.object</span><span class="sxs-lookup"><span data-stu-id="f50f4-146">System.String</span></span>

## <span data-ttu-id="f50f4-147">輸出</span><span class="sxs-lookup"><span data-stu-id="f50f4-147">OUTPUTS</span></span>

### <span data-ttu-id="f50f4-148">AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel 中的 [ManagedDatabaseBackup]</span><span class="sxs-lookup"><span data-stu-id="f50f4-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="f50f4-149">筆記</span><span class="sxs-lookup"><span data-stu-id="f50f4-149">NOTES</span></span>

## <span data-ttu-id="f50f4-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="f50f4-150">RELATED LINKS</span></span>
