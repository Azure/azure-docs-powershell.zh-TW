---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: c52b0a9cafbb5a3e61af3a044ef834e499e88bc5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958752"
---
# <span data-ttu-id="eb419-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="eb419-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="eb419-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb419-102">SYNOPSIS</span></span>
<span data-ttu-id="eb419-103">刪除長期保留備份。</span><span class="sxs-lookup"><span data-stu-id="eb419-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="eb419-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb419-104">SYNTAX</span></span>

### <span data-ttu-id="eb419-105">RemoveBackupDefault (預設) </span><span class="sxs-lookup"><span data-stu-id="eb419-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb419-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="eb419-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb419-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb419-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb419-108">說明</span><span class="sxs-lookup"><span data-stu-id="eb419-108">DESCRIPTION</span></span>
<span data-ttu-id="eb419-109">**AzSqlInstanceDatabaseLongTermRetentionBackup** Cmdlet 會刪除指定的備份。</span><span class="sxs-lookup"><span data-stu-id="eb419-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="eb419-110">示例</span><span class="sxs-lookup"><span data-stu-id="eb419-110">EXAMPLES</span></span>

### <span data-ttu-id="eb419-111">範例1</span><span class="sxs-lookup"><span data-stu-id="eb419-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="eb419-112">刪除名稱為15be823c-7e2c-49d8-819f-a3fdcad92215 的備份; 132268250550000000</span><span class="sxs-lookup"><span data-stu-id="eb419-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="eb419-113">參數</span><span class="sxs-lookup"><span data-stu-id="eb419-113">PARAMETERS</span></span>

### <span data-ttu-id="eb419-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="eb419-114">-BackupName</span></span>
<span data-ttu-id="eb419-115">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb419-115">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb419-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb419-116">-DatabaseName</span></span>
<span data-ttu-id="eb419-117">備份所在之受管理資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb419-117">The name of the Managed Database the backup is from.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb419-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb419-118">-DefaultProfile</span></span>
<span data-ttu-id="eb419-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb419-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb419-120">-Force</span><span class="sxs-lookup"><span data-stu-id="eb419-120">-Force</span></span>
<span data-ttu-id="eb419-121">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="eb419-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb419-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb419-122">-InputObject</span></span>
<span data-ttu-id="eb419-123">要移除的資料庫長期保留備份物件。</span><span class="sxs-lookup"><span data-stu-id="eb419-123">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb419-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="eb419-124">-InstanceName</span></span>
<span data-ttu-id="eb419-125">備份所在之受管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb419-125">The name of the Managed Instance the backup is under.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb419-126">-位置</span><span class="sxs-lookup"><span data-stu-id="eb419-126">-Location</span></span>
<span data-ttu-id="eb419-127">備份來源管理實例的位置。</span><span class="sxs-lookup"><span data-stu-id="eb419-127">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb419-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb419-128">-ResourceGroupName</span></span>
<span data-ttu-id="eb419-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb419-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb419-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb419-130">-ResourceId</span></span>
<span data-ttu-id="eb419-131">要移除之 [長期保留] 備份的 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="eb419-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb419-132">-確認</span><span class="sxs-lookup"><span data-stu-id="eb419-132">-Confirm</span></span>
<span data-ttu-id="eb419-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eb419-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb419-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb419-134">-WhatIf</span></span>
<span data-ttu-id="eb419-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb419-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb419-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb419-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb419-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb419-137">CommonParameters</span></span>
<span data-ttu-id="eb419-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb419-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb419-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eb419-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb419-140">輸入</span><span class="sxs-lookup"><span data-stu-id="eb419-140">INPUTS</span></span>

### <span data-ttu-id="eb419-141">AzureSqlManagedDatabaseLongTermRetentionBackupModel 中的 [ManagedDatabaseBackup]</span><span class="sxs-lookup"><span data-stu-id="eb419-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="eb419-142">System.object</span><span class="sxs-lookup"><span data-stu-id="eb419-142">System.String</span></span>

## <span data-ttu-id="eb419-143">輸出</span><span class="sxs-lookup"><span data-stu-id="eb419-143">OUTPUTS</span></span>

### <span data-ttu-id="eb419-144">AzureSqlManagedDatabaseLongTermRetentionBackupModel 中的 [ManagedDatabaseBackup]</span><span class="sxs-lookup"><span data-stu-id="eb419-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="eb419-145">筆記</span><span class="sxs-lookup"><span data-stu-id="eb419-145">NOTES</span></span>

## <span data-ttu-id="eb419-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb419-146">RELATED LINKS</span></span>

[<span data-ttu-id="eb419-147">AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="eb419-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="eb419-148">AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="eb419-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="eb419-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="eb419-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="eb419-150">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="eb419-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)