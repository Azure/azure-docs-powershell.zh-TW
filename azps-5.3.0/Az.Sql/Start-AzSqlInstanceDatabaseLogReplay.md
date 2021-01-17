---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 61a87f61efaa889af830cc7bdaa44bcf0b7fc698
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437020"
---
# <span data-ttu-id="ff0f0-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="ff0f0-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="ff0f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff0f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ff0f0-103">使用指定的參數開機記錄重播服務。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="ff0f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff0f0-104">SYNTAX</span></span>

### <span data-ttu-id="ff0f0-105">LogReplayInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="ff0f0-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff0f0-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="ff0f0-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff0f0-107">說明</span><span class="sxs-lookup"><span data-stu-id="ff0f0-107">DESCRIPTION</span></span>
<span data-ttu-id="ff0f0-108">**Start-AzSqlInstanceDatabaseLogReplay** Cmdlet 會開機記錄重播服務的開始。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="ff0f0-109">示例</span><span class="sxs-lookup"><span data-stu-id="ff0f0-109">EXAMPLES</span></span>

### <span data-ttu-id="ff0f0-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ff0f0-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="ff0f0-111">這個命令會建立新的 managed 資料庫，並開始從指定的容器還原備份，直到 last_backup .bak 還原為止。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="ff0f0-112">範例2</span><span class="sxs-lookup"><span data-stu-id="ff0f0-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="ff0f0-113">這個命令會建立新的 managed 資料庫，並開始從指定的容器還原備份，直到使用上次備份所需的 Complete-AzSqlInstanceDatabaseLogReplay 呼叫為止。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="ff0f0-114">參數</span><span class="sxs-lookup"><span data-stu-id="ff0f0-114">PARAMETERS</span></span>

### <span data-ttu-id="ff0f0-115">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="ff0f0-115">-AutoCompleteRestore</span></span>
<span data-ttu-id="ff0f0-116">指示符是否在完成後自動完成還原。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-116">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="ff0f0-117">-排序規則</span><span class="sxs-lookup"><span data-stu-id="ff0f0-117">-Collation</span></span>
<span data-ttu-id="ff0f0-118">要使用之實例資料庫的排序規則。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-118">The collation of the instance database to use.</span></span>

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

### <span data-ttu-id="ff0f0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0f0-119">-DefaultProfile</span></span>
<span data-ttu-id="ff0f0-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff0f0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff0f0-121">-InputObject</span></span>
<span data-ttu-id="ff0f0-122">實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-122">The instance database object.</span></span>

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

### <span data-ttu-id="ff0f0-123">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ff0f0-123">-InstanceName</span></span>
<span data-ttu-id="ff0f0-124">實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-124">The name of the instance.</span></span>

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

### <span data-ttu-id="ff0f0-125">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="ff0f0-125">-LastBackupName</span></span>
<span data-ttu-id="ff0f0-126">要還原之最後一個備份檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-126">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="ff0f0-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff0f0-127">-Name</span></span>
<span data-ttu-id="ff0f0-128">實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-128">The name of the instance database.</span></span>

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

### <span data-ttu-id="ff0f0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff0f0-129">-PassThru</span></span>
<span data-ttu-id="ff0f0-130">定義是否要傳回同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-130">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="ff0f0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff0f0-131">-ResourceGroupName</span></span>
<span data-ttu-id="ff0f0-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="ff0f0-133">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="ff0f0-133">-StorageContainerSasToken</span></span>
<span data-ttu-id="ff0f0-134">儲存容器 Sas 權杖。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-134">The storage container Sas token.</span></span>

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

### <span data-ttu-id="ff0f0-135">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="ff0f0-135">-StorageContainerUri</span></span>
<span data-ttu-id="ff0f0-136">儲存容器 URI。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-136">The storage container URI.</span></span>

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

### <span data-ttu-id="ff0f0-137">-確認</span><span class="sxs-lookup"><span data-stu-id="ff0f0-137">-Confirm</span></span>
<span data-ttu-id="ff0f0-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff0f0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff0f0-139">-WhatIf</span></span>
<span data-ttu-id="ff0f0-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff0f0-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff0f0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0f0-142">CommonParameters</span></span>
<span data-ttu-id="ff0f0-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0f0-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ff0f0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0f0-145">輸入</span><span class="sxs-lookup"><span data-stu-id="ff0f0-145">INPUTS</span></span>

### <span data-ttu-id="ff0f0-146">System.object</span><span class="sxs-lookup"><span data-stu-id="ff0f0-146">System.String</span></span>

### <span data-ttu-id="ff0f0-147">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="ff0f0-147">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="ff0f0-148">輸出</span><span class="sxs-lookup"><span data-stu-id="ff0f0-148">OUTPUTS</span></span>

### <span data-ttu-id="ff0f0-149">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="ff0f0-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="ff0f0-150">筆記</span><span class="sxs-lookup"><span data-stu-id="ff0f0-150">NOTES</span></span>

## <span data-ttu-id="ff0f0-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff0f0-151">RELATED LINKS</span></span>
