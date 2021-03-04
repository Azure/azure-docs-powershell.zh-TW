---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: ce937cc6f7e4bc68592ed089a3028e2919fde29f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904818"
---
# <span data-ttu-id="6f7bf-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="6f7bf-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="6f7bf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6f7bf-102">SYNOPSIS</span></span>
<span data-ttu-id="6f7bf-103">以指定參數開機記錄重播服務。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="6f7bf-104">語法</span><span class="sxs-lookup"><span data-stu-id="6f7bf-104">SYNTAX</span></span>

### <span data-ttu-id="6f7bf-105">LogReplayInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="6f7bf-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f7bf-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="6f7bf-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6f7bf-107">描述</span><span class="sxs-lookup"><span data-stu-id="6f7bf-107">DESCRIPTION</span></span>
<span data-ttu-id="6f7bf-108">**Start-AzSqlInstanceDatabaseLogReplay** Cmdlet 會開機記錄重播服務。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="6f7bf-109">例子</span><span class="sxs-lookup"><span data-stu-id="6f7bf-109">EXAMPLES</span></span>

### <span data-ttu-id="6f7bf-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="6f7bf-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="6f7bf-111">此命令會建立新的受管理資料庫，並開始從給定容器還原備份，last_backup.bak 還原。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="6f7bf-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="6f7bf-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="6f7bf-113">此命令會建立新的受管理資料庫，並開始從給定容器還原備份，直到Complete-AzSqlInstanceDatabaseLogReplay最後一次要求備份時再重新叫用。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="6f7bf-114">參數</span><span class="sxs-lookup"><span data-stu-id="6f7bf-114">PARAMETERS</span></span>

### <span data-ttu-id="6f7bf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f7bf-115">-AsJob</span></span>
<span data-ttu-id="6f7bf-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6f7bf-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f7bf-117">-自動完成Restore</span><span class="sxs-lookup"><span data-stu-id="6f7bf-117">-AutoCompleteRestore</span></span>
<span data-ttu-id="6f7bf-118">完成時是否要自動完成還原的標記。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-118">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="6f7bf-119">-排序</span><span class="sxs-lookup"><span data-stu-id="6f7bf-119">-Collation</span></span>
<span data-ttu-id="6f7bf-120">這是要使用的實例資料庫的排序規則。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-120">The collation of the instance database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f7bf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f7bf-121">-DefaultProfile</span></span>
<span data-ttu-id="6f7bf-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f7bf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f7bf-123">-InputObject</span></span>
<span data-ttu-id="6f7bf-124">實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-124">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7bf-125">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6f7bf-125">-InstanceName</span></span>
<span data-ttu-id="6f7bf-126">實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-126">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7bf-127">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="6f7bf-127">-LastBackupName</span></span>
<span data-ttu-id="6f7bf-128">要還原的最後一個備份檔案名。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-128">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f7bf-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f7bf-129">-Name</span></span>
<span data-ttu-id="6f7bf-130">實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-130">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7bf-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f7bf-131">-PassThru</span></span>
<span data-ttu-id="6f7bf-132">定義是否返回同步組。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-132">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="6f7bf-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f7bf-133">-ResourceGroupName</span></span>
<span data-ttu-id="6f7bf-134">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7bf-135">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="6f7bf-135">-StorageContainerSasToken</span></span>
<span data-ttu-id="6f7bf-136">儲存容器 Sas 權杖。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-136">The storage container Sas token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasToken

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f7bf-137">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="6f7bf-137">-StorageContainerUri</span></span>
<span data-ttu-id="6f7bf-138">儲存容器 URI。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-138">The storage container URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Storage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f7bf-139">-確認</span><span class="sxs-lookup"><span data-stu-id="6f7bf-139">-Confirm</span></span>
<span data-ttu-id="6f7bf-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f7bf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f7bf-141">-WhatIf</span></span>
<span data-ttu-id="6f7bf-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f7bf-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f7bf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f7bf-144">CommonParameters</span></span>
<span data-ttu-id="6f7bf-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6f7bf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f7bf-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f7bf-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f7bf-147">輸入</span><span class="sxs-lookup"><span data-stu-id="6f7bf-147">INPUTS</span></span>

### <span data-ttu-id="6f7bf-148">System.String</span><span class="sxs-lookup"><span data-stu-id="6f7bf-148">System.String</span></span>

### <span data-ttu-id="6f7bf-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="6f7bf-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="6f7bf-150">輸出</span><span class="sxs-lookup"><span data-stu-id="6f7bf-150">OUTPUTS</span></span>

### <span data-ttu-id="6f7bf-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="6f7bf-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="6f7bf-152">筆記</span><span class="sxs-lookup"><span data-stu-id="6f7bf-152">NOTES</span></span>

## <span data-ttu-id="6f7bf-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f7bf-153">RELATED LINKS</span></span>
