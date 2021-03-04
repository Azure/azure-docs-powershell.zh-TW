---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: d3faa342d1f54abe2433ec7de8ee1c3f910fa58d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905789"
---
# <span data-ttu-id="c24cf-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c24cf-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="c24cf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c24cf-102">SYNOPSIS</span></span>
<span data-ttu-id="c24cf-103">刪除長期保留備份。</span><span class="sxs-lookup"><span data-stu-id="c24cf-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="c24cf-104">語法</span><span class="sxs-lookup"><span data-stu-id="c24cf-104">SYNTAX</span></span>

### <span data-ttu-id="c24cf-105">RemoveBackupDefault (預設) </span><span class="sxs-lookup"><span data-stu-id="c24cf-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24cf-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="c24cf-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24cf-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="c24cf-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c24cf-108">描述</span><span class="sxs-lookup"><span data-stu-id="c24cf-108">DESCRIPTION</span></span>
<span data-ttu-id="c24cf-109">**Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** Cmdlet 會刪除指定的備份。</span><span class="sxs-lookup"><span data-stu-id="c24cf-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="c24cf-110">例子</span><span class="sxs-lookup"><span data-stu-id="c24cf-110">EXAMPLES</span></span>

### <span data-ttu-id="c24cf-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="c24cf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="c24cf-112">刪除名稱為 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250505000000 的備份</span><span class="sxs-lookup"><span data-stu-id="c24cf-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="c24cf-113">參數</span><span class="sxs-lookup"><span data-stu-id="c24cf-113">PARAMETERS</span></span>

### <span data-ttu-id="c24cf-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="c24cf-114">-BackupName</span></span>
<span data-ttu-id="c24cf-115">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="c24cf-115">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24cf-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c24cf-116">-DatabaseName</span></span>
<span data-ttu-id="c24cf-117">備份的受管理資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="c24cf-117">The name of the Managed Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24cf-118">-DefaultProfile</span></span>
<span data-ttu-id="c24cf-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c24cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c24cf-120">-強制</span><span class="sxs-lookup"><span data-stu-id="c24cf-120">-Force</span></span>
<span data-ttu-id="c24cf-121">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="c24cf-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24cf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c24cf-122">-InputObject</span></span>
<span data-ttu-id="c24cf-123">要移除的資料庫長期保留備份物件。</span><span class="sxs-lookup"><span data-stu-id="c24cf-123">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c24cf-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c24cf-124">-InstanceName</span></span>
<span data-ttu-id="c24cf-125">備份的受管理實例名稱位於下。</span><span class="sxs-lookup"><span data-stu-id="c24cf-125">The name of the Managed Instance the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24cf-126">-位置</span><span class="sxs-lookup"><span data-stu-id="c24cf-126">-Location</span></span>
<span data-ttu-id="c24cf-127">備份來源受管理實例的位置。</span><span class="sxs-lookup"><span data-stu-id="c24cf-127">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24cf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c24cf-128">-ResourceGroupName</span></span>
<span data-ttu-id="c24cf-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c24cf-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24cf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c24cf-130">-ResourceId</span></span>
<span data-ttu-id="c24cf-131">要移除之資料庫長期保留備份的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c24cf-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24cf-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c24cf-132">-Confirm</span></span>
<span data-ttu-id="c24cf-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c24cf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c24cf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c24cf-134">-WhatIf</span></span>
<span data-ttu-id="c24cf-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c24cf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c24cf-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c24cf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c24cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c24cf-137">CommonParameters</span></span>
<span data-ttu-id="c24cf-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c24cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c24cf-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c24cf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c24cf-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c24cf-140">INPUTS</span></span>

### <span data-ttu-id="c24cf-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="c24cf-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="c24cf-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c24cf-142">System.String</span></span>

## <span data-ttu-id="c24cf-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c24cf-143">OUTPUTS</span></span>

### <span data-ttu-id="c24cf-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="c24cf-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="c24cf-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c24cf-145">NOTES</span></span>

## <span data-ttu-id="c24cf-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="c24cf-146">RELATED LINKS</span></span>

[<span data-ttu-id="c24cf-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c24cf-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c24cf-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c24cf-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="c24cf-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c24cf-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="c24cf-150">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="c24cf-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)