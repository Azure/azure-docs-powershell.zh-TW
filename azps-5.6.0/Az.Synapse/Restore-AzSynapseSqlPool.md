---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 3a9620a6b5fa68fc2d4e5baf647d8dc720d787a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913297"
---
# <span data-ttu-id="b90f4-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b90f4-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="b90f4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b90f4-102">SYNOPSIS</span></span>
<span data-ttu-id="b90f4-103">還原 Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b90f4-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b90f4-104">語法</span><span class="sxs-lookup"><span data-stu-id="b90f4-104">SYNTAX</span></span>

### <span data-ttu-id="b90f4-105">RestoreFromBackupIdNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b90f4-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b90f4-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b90f4-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b90f4-107">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b90f4-107">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b90f4-108">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b90f4-108">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b90f4-109">描述</span><span class="sxs-lookup"><span data-stu-id="b90f4-109">DESCRIPTION</span></span>
<span data-ttu-id="b90f4-110">**Restore-AzSynapseSqlPool** Cmdlet 會從任何 SQL 集區之備份或還原點還原 Azure Synapse Analytics SQL 集區。</span><span class="sxs-lookup"><span data-stu-id="b90f4-110">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="b90f4-111">還原的 SQL 資料庫會建立為新的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b90f4-111">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="b90f4-112">例子</span><span class="sxs-lookup"><span data-stu-id="b90f4-112">EXAMPLES</span></span>

### <span data-ttu-id="b90f4-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="b90f4-113">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="b90f4-114">此命令會從此訂閱中任何 SQL 集區的最新備份中還原，以建立 Azure Synapse Analytics SQL 集區。</span><span class="sxs-lookup"><span data-stu-id="b90f4-114">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="b90f4-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="b90f4-115">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="b90f4-116">此命令會利用此訂閱中任何 SQL 資料庫的還原點來復原或複製先前的狀態，以建立 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b90f4-116">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="b90f4-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="b90f4-117">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="b90f4-118">此命令會利用資源識別碼，從此訂閱中任何 SQL 集區的最新備份進行還原，以建立 Azure Synapse Analytics SQL 集區。</span><span class="sxs-lookup"><span data-stu-id="b90f4-118">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="b90f4-119">範例 4</span><span class="sxs-lookup"><span data-stu-id="b90f4-119">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="b90f4-120">此命令會利用此訂閱中任何 SQL 資料庫的還原點，以使用資源識別碼復原或複製先前狀態，以建立 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b90f4-120">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="b90f4-121">參數</span><span class="sxs-lookup"><span data-stu-id="b90f4-121">PARAMETERS</span></span>

### <span data-ttu-id="b90f4-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b90f4-122">-AsJob</span></span>
<span data-ttu-id="b90f4-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b90f4-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b90f4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b90f4-124">-DefaultProfile</span></span>
<span data-ttu-id="b90f4-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b90f4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b90f4-126">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="b90f4-126">-FromBackup</span></span>
<span data-ttu-id="b90f4-127">表示從此訂閱中任何 SQL 集區的最新備份進行還原。</span><span class="sxs-lookup"><span data-stu-id="b90f4-127">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

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

### <span data-ttu-id="b90f4-128">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="b90f4-128">-FromRestorePoint</span></span>
<span data-ttu-id="b90f4-129">表示利用此訂閱中任何 SQL 資料庫的還原點來復原或複製先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="b90f4-129">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

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

### <span data-ttu-id="b90f4-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="b90f4-130">-Name</span></span>
<span data-ttu-id="b90f4-131">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b90f4-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="b90f4-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="b90f4-132">-PerformanceLevel</span></span>
<span data-ttu-id="b90f4-133">要指派給 SQL 資料庫的 SQL 服務層級和績效等級。</span><span class="sxs-lookup"><span data-stu-id="b90f4-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="b90f4-134">例如，2000c。</span><span class="sxs-lookup"><span data-stu-id="b90f4-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="b90f4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b90f4-135">-ResourceGroupName</span></span>
<span data-ttu-id="b90f4-136">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b90f4-136">Resource group name.</span></span>

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

### <span data-ttu-id="b90f4-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b90f4-137">-ResourceId</span></span>
<span data-ttu-id="b90f4-138">要還原的資料庫資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b90f4-138">The resource ID of the database to restore.</span></span>

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

### <span data-ttu-id="b90f4-139">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="b90f4-139">-RestorePoint</span></span>
<span data-ttu-id="b90f4-140">要還原的快照時間。</span><span class="sxs-lookup"><span data-stu-id="b90f4-140">Snapshot time to restore.</span></span>

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

### <span data-ttu-id="b90f4-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b90f4-141">-WorkspaceName</span></span>
<span data-ttu-id="b90f4-142">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b90f4-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b90f4-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b90f4-143">-WorkspaceObject</span></span>
<span data-ttu-id="b90f4-144">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="b90f4-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b90f4-145">-確認</span><span class="sxs-lookup"><span data-stu-id="b90f4-145">-Confirm</span></span>
<span data-ttu-id="b90f4-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b90f4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b90f4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b90f4-147">-WhatIf</span></span>
<span data-ttu-id="b90f4-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b90f4-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b90f4-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b90f4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b90f4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b90f4-150">CommonParameters</span></span>
<span data-ttu-id="b90f4-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b90f4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b90f4-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b90f4-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b90f4-153">輸入</span><span class="sxs-lookup"><span data-stu-id="b90f4-153">INPUTS</span></span>

### <span data-ttu-id="b90f4-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b90f4-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b90f4-155">輸出</span><span class="sxs-lookup"><span data-stu-id="b90f4-155">OUTPUTS</span></span>

### <span data-ttu-id="b90f4-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b90f4-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="b90f4-157">筆記</span><span class="sxs-lookup"><span data-stu-id="b90f4-157">NOTES</span></span>

## <span data-ttu-id="b90f4-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="b90f4-158">RELATED LINKS</span></span>
