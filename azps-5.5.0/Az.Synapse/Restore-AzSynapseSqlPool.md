---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: fd83b97a7b95760d0ee2ce88295ed14c98a43ab3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130359"
---
# <span data-ttu-id="aa171-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="aa171-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="aa171-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa171-102">SYNOPSIS</span></span>
<span data-ttu-id="aa171-103">還原 Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="aa171-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="aa171-104">句法</span><span class="sxs-lookup"><span data-stu-id="aa171-104">SYNTAX</span></span>

### <span data-ttu-id="aa171-105">RestoreFromBackupIdByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="aa171-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa171-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa171-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa171-107">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa171-107">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa171-108">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa171-108">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa171-109">說明</span><span class="sxs-lookup"><span data-stu-id="aa171-109">DESCRIPTION</span></span>
<span data-ttu-id="aa171-110">**Restore-AzSynapseSqlPool** Cmdlet 會從任何 SQL 池中的備份或還原點還原 Azure SYNAPSE 分析 SQL 池。</span><span class="sxs-lookup"><span data-stu-id="aa171-110">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="aa171-111">已還原的 SQL pool 是以新的 SQL pool 建立。</span><span class="sxs-lookup"><span data-stu-id="aa171-111">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="aa171-112">示例</span><span class="sxs-lookup"><span data-stu-id="aa171-112">EXAMPLES</span></span>

### <span data-ttu-id="aa171-113">範例1</span><span class="sxs-lookup"><span data-stu-id="aa171-113">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="aa171-114">這個命令會透過從此訂閱中的任何 SQL pool 最近的備份進行還原，來建立 Azure Synapse 分析 SQL 池。</span><span class="sxs-lookup"><span data-stu-id="aa171-114">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="aa171-115">範例2</span><span class="sxs-lookup"><span data-stu-id="aa171-115">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="aa171-116">這個命令會利用此訂閱中的任何 SQL 池中的還原點來建立 Azure Synapse Analytics SQL pool，以從先前的狀態進行復原或複製。</span><span class="sxs-lookup"><span data-stu-id="aa171-116">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="aa171-117">範例3</span><span class="sxs-lookup"><span data-stu-id="aa171-117">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="aa171-118">這個命令會透過使用資源識別碼在此訂閱中的任何 SQL pool 的最新備份中還原，來建立 Azure Synapse 分析 SQL pool。</span><span class="sxs-lookup"><span data-stu-id="aa171-118">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="aa171-119">範例4</span><span class="sxs-lookup"><span data-stu-id="aa171-119">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="aa171-120">這個命令會利用此訂閱中的任何 SQL 池中的還原點來建立 Azure Synapse Analytics SQL pool，以使用資源識別碼來復原或複製先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="aa171-120">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="aa171-121">參數</span><span class="sxs-lookup"><span data-stu-id="aa171-121">PARAMETERS</span></span>

### <span data-ttu-id="aa171-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa171-122">-AsJob</span></span>
<span data-ttu-id="aa171-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="aa171-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa171-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa171-124">-DefaultProfile</span></span>
<span data-ttu-id="aa171-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa171-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa171-126">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="aa171-126">-FromBackup</span></span>
<span data-ttu-id="aa171-127">指示要從此訂閱中的任何 SQL pool 最近的備份中還原。</span><span class="sxs-lookup"><span data-stu-id="aa171-127">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa171-128">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="aa171-128">-FromRestorePoint</span></span>
<span data-ttu-id="aa171-129">指示要利用此訂閱中任何 SQL pool 的還原點來復原或複製先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="aa171-129">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa171-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="aa171-130">-Name</span></span>
<span data-ttu-id="aa171-131">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa171-131">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetSqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa171-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="aa171-132">-PerformanceLevel</span></span>
<span data-ttu-id="aa171-133">要指派給 SQL pool 的 SQL 服務層級和效能等級。</span><span class="sxs-lookup"><span data-stu-id="aa171-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="aa171-134">例如，DW2000c。</span><span class="sxs-lookup"><span data-stu-id="aa171-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa171-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa171-135">-ResourceGroupName</span></span>
<span data-ttu-id="aa171-136">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="aa171-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa171-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa171-137">-ResourceId</span></span>
<span data-ttu-id="aa171-138">要還原之資料庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa171-138">The resource ID of the database to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa171-139">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="aa171-139">-RestorePoint</span></span>
<span data-ttu-id="aa171-140">要還原的快照時間。</span><span class="sxs-lookup"><span data-stu-id="aa171-140">Snapshot time to restore.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases: PointInTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa171-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aa171-141">-WorkspaceName</span></span>
<span data-ttu-id="aa171-142">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa171-142">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa171-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="aa171-143">-WorkspaceObject</span></span>
<span data-ttu-id="aa171-144">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="aa171-144">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa171-145">-確認</span><span class="sxs-lookup"><span data-stu-id="aa171-145">-Confirm</span></span>
<span data-ttu-id="aa171-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aa171-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa171-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa171-147">-WhatIf</span></span>
<span data-ttu-id="aa171-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aa171-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa171-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aa171-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa171-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa171-150">CommonParameters</span></span>
<span data-ttu-id="aa171-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa171-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa171-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aa171-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa171-153">輸入</span><span class="sxs-lookup"><span data-stu-id="aa171-153">INPUTS</span></span>

### <span data-ttu-id="aa171-154">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="aa171-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="aa171-155">輸出</span><span class="sxs-lookup"><span data-stu-id="aa171-155">OUTPUTS</span></span>

### <span data-ttu-id="aa171-156">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="aa171-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="aa171-157">筆記</span><span class="sxs-lookup"><span data-stu-id="aa171-157">NOTES</span></span>

## <span data-ttu-id="aa171-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa171-158">RELATED LINKS</span></span>
