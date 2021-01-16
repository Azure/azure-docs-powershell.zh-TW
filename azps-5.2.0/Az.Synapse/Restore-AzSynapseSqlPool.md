---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 7fbc6cedf039cca33d0a30b39a21f9cdcb350b61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276492"
---
# <span data-ttu-id="7e362-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7e362-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="7e362-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e362-102">SYNOPSIS</span></span>
<span data-ttu-id="7e362-103">還原 Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="7e362-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7e362-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e362-104">SYNTAX</span></span>

### <span data-ttu-id="7e362-105">RestoreFromBackupIdByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7e362-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e362-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e362-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e362-107">RestoreFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e362-107">RestoreFromBackupNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e362-108">RestoreFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e362-108">RestoreFromBackupNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-BackupResourceGroupName <String>] -BackupWorkspaceName <String> -BackupSqlPoolName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e362-109">RestoreFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e362-109">RestoreFromBackupInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e362-110">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e362-110">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e362-111">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e362-111">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String> [-RestorePoint <DateTime>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e362-112">RestoreFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e362-112">RestoreFromRestorePointNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e362-113">RestoreFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e362-113">RestoreFromRestorePointNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e362-114">RestoreFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e362-114">RestoreFromRestorePointInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e362-115">說明</span><span class="sxs-lookup"><span data-stu-id="7e362-115">DESCRIPTION</span></span>
<span data-ttu-id="7e362-116">**Restore-AzSynapseSqlPool** Cmdlet 會從任何 SQL 池中的備份或還原點還原 Azure SYNAPSE 分析 SQL 池。</span><span class="sxs-lookup"><span data-stu-id="7e362-116">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="7e362-117">已還原的 SQL pool 是以新的 SQL pool 建立。</span><span class="sxs-lookup"><span data-stu-id="7e362-117">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="7e362-118">示例</span><span class="sxs-lookup"><span data-stu-id="7e362-118">EXAMPLES</span></span>

### <span data-ttu-id="7e362-119">範例1</span><span class="sxs-lookup"><span data-stu-id="7e362-119">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="7e362-120">這個命令會透過從此訂閱中的任何 SQL pool 最近的備份進行還原，來建立 Azure Synapse 分析 SQL 池。</span><span class="sxs-lookup"><span data-stu-id="7e362-120">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="7e362-121">範例2</span><span class="sxs-lookup"><span data-stu-id="7e362-121">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="7e362-122">這個命令會利用此訂閱中的任何 SQL 池中的還原點來建立 Azure Synapse Analytics SQL pool，以從先前的狀態進行復原或複製。</span><span class="sxs-lookup"><span data-stu-id="7e362-122">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="7e362-123">範例3</span><span class="sxs-lookup"><span data-stu-id="7e362-123">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="7e362-124">這個命令會透過使用資源識別碼在此訂閱中的任何 SQL pool 的最新備份中還原，來建立 Azure Synapse 分析 SQL pool。</span><span class="sxs-lookup"><span data-stu-id="7e362-124">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="7e362-125">範例4</span><span class="sxs-lookup"><span data-stu-id="7e362-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="7e362-126">這個命令會利用此訂閱中的任何 SQL 池中的還原點來建立 Azure Synapse Analytics SQL pool，以使用資源識別碼來復原或複製先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="7e362-126">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="7e362-127">參數</span><span class="sxs-lookup"><span data-stu-id="7e362-127">PARAMETERS</span></span>

### <span data-ttu-id="7e362-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e362-128">-AsJob</span></span>
<span data-ttu-id="7e362-129">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e362-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e362-130">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e362-130">-BackupResourceGroupName</span></span>
<span data-ttu-id="7e362-131">要建立的 bakcup SQL pool 物件的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7e362-131">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-132">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="7e362-132">-BackupResourceId</span></span>
<span data-ttu-id="7e362-133">要還原的備份 SQL pool 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e362-133">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-134">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="7e362-134">-BackupSqlPoolName</span></span>
<span data-ttu-id="7e362-135">要建立的 bakcup SQL pool 物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e362-135">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-136">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="7e362-136">-BackupSqlPoolObject</span></span>
<span data-ttu-id="7e362-137">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="7e362-137">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-138">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7e362-138">-BackupWorkspaceName</span></span>
<span data-ttu-id="7e362-139">要建立的 bakcup SQL pool 物件的 Synapse 工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="7e362-139">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e362-140">-DefaultProfile</span></span>
<span data-ttu-id="7e362-141">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e362-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e362-142">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="7e362-142">-FromBackup</span></span>
<span data-ttu-id="7e362-143">指示要從此訂閱中的任何 SQL pool 最近的備份中還原。</span><span class="sxs-lookup"><span data-stu-id="7e362-143">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-144">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="7e362-144">-FromRestorePoint</span></span>
<span data-ttu-id="7e362-145">指示要利用此訂閱中任何 SQL pool 的還原點來復原或複製先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="7e362-145">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e362-146">-Name</span></span>
<span data-ttu-id="7e362-147">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e362-147">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="7e362-148">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="7e362-148">-PerformanceLevel</span></span>
<span data-ttu-id="7e362-149">要指派給 SQL pool 的 SQL 服務層級和效能等級。</span><span class="sxs-lookup"><span data-stu-id="7e362-149">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="7e362-150">例如，DW2000c。</span><span class="sxs-lookup"><span data-stu-id="7e362-150">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e362-151">-ResourceGroupName</span></span>
<span data-ttu-id="7e362-152">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7e362-152">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-153">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="7e362-153">-RestorePoint</span></span>
<span data-ttu-id="7e362-154">要還原的快照時間。</span><span class="sxs-lookup"><span data-stu-id="7e362-154">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-155">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e362-155">-SourceResourceGroupName</span></span>
<span data-ttu-id="7e362-156">要從中建立來源 SQL pool 物件的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7e362-156">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="7e362-157">-SourceResourceId</span></span>
<span data-ttu-id="7e362-158">要從中建立來源 SQL pool 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e362-158">The resource identifier of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="7e362-159">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="7e362-159">-SourceSqlPoolName</span></span>
<span data-ttu-id="7e362-160">要建立來源 SQL pool 物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e362-160">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-161">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="7e362-161">-SourceSqlPoolObject</span></span>
<span data-ttu-id="7e362-162">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="7e362-162">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-163">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7e362-163">-SourceWorkspaceName</span></span>
<span data-ttu-id="7e362-164">要從中建立來源 SQL pool 物件的 Synapse 工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="7e362-164">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e362-165">-Tag</span></span>
<span data-ttu-id="7e362-166">與資源相關聯之標記的字串字典。</span><span class="sxs-lookup"><span data-stu-id="7e362-166">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7e362-167">-WorkspaceName</span></span>
<span data-ttu-id="7e362-168">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e362-168">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-169">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7e362-169">-WorkspaceObject</span></span>
<span data-ttu-id="7e362-170">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="7e362-170">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e362-171">-確認</span><span class="sxs-lookup"><span data-stu-id="7e362-171">-Confirm</span></span>
<span data-ttu-id="7e362-172">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7e362-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e362-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e362-173">-WhatIf</span></span>
<span data-ttu-id="7e362-174">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7e362-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e362-175">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e362-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e362-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e362-176">CommonParameters</span></span>
<span data-ttu-id="7e362-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e362-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e362-178">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7e362-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e362-179">輸入</span><span class="sxs-lookup"><span data-stu-id="7e362-179">INPUTS</span></span>

### <span data-ttu-id="7e362-180">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="7e362-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7e362-181">輸出</span><span class="sxs-lookup"><span data-stu-id="7e362-181">OUTPUTS</span></span>

### <span data-ttu-id="7e362-182">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="7e362-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7e362-183">筆記</span><span class="sxs-lookup"><span data-stu-id="7e362-183">NOTES</span></span>

## <span data-ttu-id="7e362-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e362-184">RELATED LINKS</span></span>
