---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 694b9811bf11454e232f1514b59b1b537e4720a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136120"
---
# <span data-ttu-id="64b67-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="64b67-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="64b67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64b67-102">SYNOPSIS</span></span>
<span data-ttu-id="64b67-103">建立 Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="64b67-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="64b67-104">句法</span><span class="sxs-lookup"><span data-stu-id="64b67-104">SYNTAX</span></span>

### <span data-ttu-id="64b67-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="64b67-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64b67-106">CreateFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b67-106">CreateFromBackupIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64b67-107">CreateFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b67-107">CreateFromBackupIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64b67-108">CreateFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b67-108">CreateFromBackupNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64b67-109">CreateFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b67-109">CreateFromBackupNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64b67-110">CreateFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b67-110">CreateFromBackupInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64b67-111">CreateFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b67-111">CreateFromRestorePointIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64b67-112">CreateFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b67-112">CreateFromRestorePointIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64b67-113">CreateFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b67-113">CreateFromRestorePointNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64b67-114">CreateFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b67-114">CreateFromRestorePointNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64b67-115">CreateFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b67-115">CreateFromRestorePointInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64b67-116">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b67-116">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64b67-117">說明</span><span class="sxs-lookup"><span data-stu-id="64b67-117">DESCRIPTION</span></span>
<span data-ttu-id="64b67-118">**AzSynapseSqlPool** Cmdlet 會建立 Azure SYNAPSE 分析 SQL pool。</span><span class="sxs-lookup"><span data-stu-id="64b67-118">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="64b67-119">示例</span><span class="sxs-lookup"><span data-stu-id="64b67-119">EXAMPLES</span></span>

### <span data-ttu-id="64b67-120">範例1</span><span class="sxs-lookup"><span data-stu-id="64b67-120">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="64b67-121">這個命令會建立 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="64b67-121">This command creates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="64b67-122">範例2</span><span class="sxs-lookup"><span data-stu-id="64b67-122">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="64b67-123">這個命令會透過從此訂閱中的任何 SQL pool 最近的備份進行還原，來建立 Azure Synapse 分析 SQL 池。</span><span class="sxs-lookup"><span data-stu-id="64b67-123">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="64b67-124">範例3</span><span class="sxs-lookup"><span data-stu-id="64b67-124">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="64b67-125">這個命令會利用此訂閱中的任何 SQL 池中的還原點來建立 Azure Synapse Analytics SQL pool，以從先前的狀態進行復原或複製。</span><span class="sxs-lookup"><span data-stu-id="64b67-125">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="64b67-126">範例4</span><span class="sxs-lookup"><span data-stu-id="64b67-126">Example 4</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="64b67-127">這個命令會透過使用資源識別碼在此訂閱中的任何 SQL pool 的最新備份中還原，來建立 Azure Synapse 分析 SQL pool。</span><span class="sxs-lookup"><span data-stu-id="64b67-127">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="64b67-128">範例5</span><span class="sxs-lookup"><span data-stu-id="64b67-128">Example 5</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws |  New-AzSynapseSqlPool -FromRestorePoint -Name dwsql0554 -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/mandywtest/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="64b67-129">這個命令會利用此訂閱中的任何 SQL 池中的還原點來建立 Azure Synapse Analytics SQL pool，以使用資源識別碼來復原或複製先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="64b67-129">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="64b67-130">參數</span><span class="sxs-lookup"><span data-stu-id="64b67-130">PARAMETERS</span></span>

### <span data-ttu-id="64b67-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64b67-131">-AsJob</span></span>
<span data-ttu-id="64b67-132">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="64b67-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64b67-133">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b67-133">-BackupResourceGroupName</span></span>
<span data-ttu-id="64b67-134">要建立的 bakcup SQL pool 物件的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="64b67-134">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-135">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="64b67-135">-BackupResourceId</span></span>
<span data-ttu-id="64b67-136">要還原的備份 SQL pool 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="64b67-136">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-137">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="64b67-137">-BackupSqlPoolName</span></span>
<span data-ttu-id="64b67-138">要建立的 bakcup SQL pool 物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="64b67-138">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-139">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="64b67-139">-BackupSqlPoolObject</span></span>
<span data-ttu-id="64b67-140">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="64b67-140">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-141">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="64b67-141">-BackupWorkspaceName</span></span>
<span data-ttu-id="64b67-142">要建立的 bakcup SQL pool 物件的 Synapse 工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="64b67-142">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-143">-排序規則</span><span class="sxs-lookup"><span data-stu-id="64b67-143">-Collation</span></span>
<span data-ttu-id="64b67-144">排序規則定義排序與比較資料的規則，且無法在建立 SQL 池之後進行變更。</span><span class="sxs-lookup"><span data-stu-id="64b67-144">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="64b67-145">預設的排序規則為 [SQL_Latin1_General_CP1_CI_AS]。</span><span class="sxs-lookup"><span data-stu-id="64b67-145">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b67-146">-DefaultProfile</span></span>
<span data-ttu-id="64b67-147">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="64b67-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64b67-148">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="64b67-148">-FromBackup</span></span>
<span data-ttu-id="64b67-149">指示要從此訂閱中的任何 SQL pool 最近的備份中還原。</span><span class="sxs-lookup"><span data-stu-id="64b67-149">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-150">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="64b67-150">-FromRestorePoint</span></span>
<span data-ttu-id="64b67-151">指示要利用此訂閱中任何 SQL pool 的還原點來復原或複製先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="64b67-151">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-152">-名稱</span><span class="sxs-lookup"><span data-stu-id="64b67-152">-Name</span></span>
<span data-ttu-id="64b67-153">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="64b67-153">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="64b67-154">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="64b67-154">-PerformanceLevel</span></span>
<span data-ttu-id="64b67-155">要指派給 SQL pool 的 SQL 服務層級和效能等級。</span><span class="sxs-lookup"><span data-stu-id="64b67-155">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="64b67-156">例如，DW2000c。</span><span class="sxs-lookup"><span data-stu-id="64b67-156">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b67-157">-ResourceGroupName</span></span>
<span data-ttu-id="64b67-158">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="64b67-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-159">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="64b67-159">-RestorePoint</span></span>
<span data-ttu-id="64b67-160">要還原的快照時間。</span><span class="sxs-lookup"><span data-stu-id="64b67-160">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-161">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b67-161">-SourceResourceGroupName</span></span>
<span data-ttu-id="64b67-162">要從中建立來源 SQL pool 物件的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="64b67-162">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-163">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="64b67-163">-SourceResourceId</span></span>
<span data-ttu-id="64b67-164">要從中建立來源 SQL pool 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="64b67-164">The resource identifier of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-165">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="64b67-165">-SourceSqlPoolName</span></span>
<span data-ttu-id="64b67-166">要建立來源 SQL pool 物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="64b67-166">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-167">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="64b67-167">-SourceSqlPoolObject</span></span>
<span data-ttu-id="64b67-168">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="64b67-168">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-169">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="64b67-169">-SourceWorkspaceName</span></span>
<span data-ttu-id="64b67-170">要從中建立來源 SQL pool 物件的 Synapse 工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="64b67-170">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="64b67-171">-Tag</span></span>
<span data-ttu-id="64b67-172">與資源相關聯之標記的字串字典。</span><span class="sxs-lookup"><span data-stu-id="64b67-172">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="64b67-173">-版本</span><span class="sxs-lookup"><span data-stu-id="64b67-173">-Version</span></span>
<span data-ttu-id="64b67-174">Synapse SQL pool 的版本。</span><span class="sxs-lookup"><span data-stu-id="64b67-174">Version of Synapse SQL pool.</span></span> <span data-ttu-id="64b67-175">例如，2或3。</span><span class="sxs-lookup"><span data-stu-id="64b67-175">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-176">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="64b67-176">-WorkspaceName</span></span>
<span data-ttu-id="64b67-177">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="64b67-177">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-178">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="64b67-178">-WorkspaceObject</span></span>
<span data-ttu-id="64b67-179">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="64b67-179">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64b67-180">-確認</span><span class="sxs-lookup"><span data-stu-id="64b67-180">-Confirm</span></span>
<span data-ttu-id="64b67-181">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="64b67-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64b67-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64b67-182">-WhatIf</span></span>
<span data-ttu-id="64b67-183">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64b67-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64b67-184">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64b67-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64b67-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b67-185">CommonParameters</span></span>
<span data-ttu-id="64b67-186">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64b67-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b67-187">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="64b67-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b67-188">輸入</span><span class="sxs-lookup"><span data-stu-id="64b67-188">INPUTS</span></span>

### <span data-ttu-id="64b67-189">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="64b67-189">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="64b67-190">輸出</span><span class="sxs-lookup"><span data-stu-id="64b67-190">OUTPUTS</span></span>

### <span data-ttu-id="64b67-191">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="64b67-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="64b67-192">筆記</span><span class="sxs-lookup"><span data-stu-id="64b67-192">NOTES</span></span>

## <span data-ttu-id="64b67-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="64b67-193">RELATED LINKS</span></span>
