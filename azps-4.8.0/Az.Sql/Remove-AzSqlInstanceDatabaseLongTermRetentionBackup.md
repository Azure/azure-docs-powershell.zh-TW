---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127255"
---
# <span data-ttu-id="af459-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="af459-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="af459-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af459-102">SYNOPSIS</span></span>
<span data-ttu-id="af459-103">刪除長期保留備份。</span><span class="sxs-lookup"><span data-stu-id="af459-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="af459-104">句法</span><span class="sxs-lookup"><span data-stu-id="af459-104">SYNTAX</span></span>

### <span data-ttu-id="af459-105">RemoveBackupDefault (預設) </span><span class="sxs-lookup"><span data-stu-id="af459-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af459-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="af459-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af459-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="af459-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af459-108">說明</span><span class="sxs-lookup"><span data-stu-id="af459-108">DESCRIPTION</span></span>
<span data-ttu-id="af459-109">**AzSqlInstanceDatabaseLongTermRetentionBackup** Cmdlet 會刪除指定的備份。</span><span class="sxs-lookup"><span data-stu-id="af459-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="af459-110">示例</span><span class="sxs-lookup"><span data-stu-id="af459-110">EXAMPLES</span></span>

### <span data-ttu-id="af459-111">範例1</span><span class="sxs-lookup"><span data-stu-id="af459-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="af459-112">刪除名稱為15be823c-7e2c-49d8-819f-a3fdcad92215 的備份; 132268250550000000</span><span class="sxs-lookup"><span data-stu-id="af459-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="af459-113">參數</span><span class="sxs-lookup"><span data-stu-id="af459-113">PARAMETERS</span></span>

### <span data-ttu-id="af459-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="af459-114">-BackupName</span></span>
<span data-ttu-id="af459-115">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="af459-115">The name of the backup.</span></span>

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

### <span data-ttu-id="af459-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="af459-116">-DatabaseName</span></span>
<span data-ttu-id="af459-117">備份所在之受管理資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="af459-117">The name of the Managed Database the backup is from.</span></span>

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

### <span data-ttu-id="af459-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af459-118">-DefaultProfile</span></span>
<span data-ttu-id="af459-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af459-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af459-120">-Force</span><span class="sxs-lookup"><span data-stu-id="af459-120">-Force</span></span>
<span data-ttu-id="af459-121">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="af459-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="af459-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af459-122">-InputObject</span></span>
<span data-ttu-id="af459-123">要移除的資料庫長期保留備份物件。</span><span class="sxs-lookup"><span data-stu-id="af459-123">The Database Long Term Retention Backup object to remove.</span></span>

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

### <span data-ttu-id="af459-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="af459-124">-InstanceName</span></span>
<span data-ttu-id="af459-125">備份所在之受管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="af459-125">The name of the Managed Instance the backup is under.</span></span>

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

### <span data-ttu-id="af459-126">-位置</span><span class="sxs-lookup"><span data-stu-id="af459-126">-Location</span></span>
<span data-ttu-id="af459-127">備份來源管理實例的位置。</span><span class="sxs-lookup"><span data-stu-id="af459-127">The location of the backups' source Managed Instance.</span></span>

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

### <span data-ttu-id="af459-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af459-128">-ResourceGroupName</span></span>
<span data-ttu-id="af459-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="af459-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="af459-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af459-130">-ResourceId</span></span>
<span data-ttu-id="af459-131">要移除之 [長期保留] 備份的 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="af459-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="af459-132">-確認</span><span class="sxs-lookup"><span data-stu-id="af459-132">-Confirm</span></span>
<span data-ttu-id="af459-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="af459-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af459-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af459-134">-WhatIf</span></span>
<span data-ttu-id="af459-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af459-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af459-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af459-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af459-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af459-137">CommonParameters</span></span>
<span data-ttu-id="af459-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af459-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af459-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="af459-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af459-140">輸入</span><span class="sxs-lookup"><span data-stu-id="af459-140">INPUTS</span></span>

### <span data-ttu-id="af459-141">AzureSqlManagedDatabaseLongTermRetentionBackupModel 中的 [ManagedDatabaseBackup]</span><span class="sxs-lookup"><span data-stu-id="af459-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="af459-142">System.object</span><span class="sxs-lookup"><span data-stu-id="af459-142">System.String</span></span>

## <span data-ttu-id="af459-143">輸出</span><span class="sxs-lookup"><span data-stu-id="af459-143">OUTPUTS</span></span>

### <span data-ttu-id="af459-144">AzureSqlManagedDatabaseLongTermRetentionBackupModel 中的 [ManagedDatabaseBackup]</span><span class="sxs-lookup"><span data-stu-id="af459-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="af459-145">筆記</span><span class="sxs-lookup"><span data-stu-id="af459-145">NOTES</span></span>

## <span data-ttu-id="af459-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="af459-146">RELATED LINKS</span></span>

[<span data-ttu-id="af459-147">AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="af459-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="af459-148">AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="af459-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="af459-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="af459-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="af459-150">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="af459-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)