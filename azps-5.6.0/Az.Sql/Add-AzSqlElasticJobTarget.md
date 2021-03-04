---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: 3a5c9284da784324b6b0887b836189c58077faa7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904305"
---
# <span data-ttu-id="32105-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="32105-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="32105-102">簡介</span><span class="sxs-lookup"><span data-stu-id="32105-102">SYNOPSIS</span></span>
<span data-ttu-id="32105-103">新增目標至目標群組</span><span class="sxs-lookup"><span data-stu-id="32105-103">Adds a target to a target group</span></span>

## <span data-ttu-id="32105-104">語法</span><span class="sxs-lookup"><span data-stu-id="32105-104">SYNTAX</span></span>

### <span data-ttu-id="32105-105">SqlDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="32105-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32105-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="32105-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32105-107">SqlS本圖</span><span class="sxs-lookup"><span data-stu-id="32105-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32105-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="32105-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32105-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="32105-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32105-110">SqlS本MapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="32105-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32105-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="32105-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32105-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="32105-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32105-113">SqlS本MapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="32105-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32105-114">描述</span><span class="sxs-lookup"><span data-stu-id="32105-114">DESCRIPTION</span></span>
<span data-ttu-id="32105-115">Cmdlet Add-AzSqlElasticJobTarget新增目標資源至目標群組</span><span class="sxs-lookup"><span data-stu-id="32105-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="32105-116">例子</span><span class="sxs-lookup"><span data-stu-id="32105-116">EXAMPLES</span></span>

### <span data-ttu-id="32105-117">範例 1：新增伺服器目標</span><span class="sxs-lookup"><span data-stu-id="32105-117">Example 1: Add a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="32105-118">範例 2：新增資料庫目標</span><span class="sxs-lookup"><span data-stu-id="32105-118">Example 2: Add a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="32105-119">範例 3：新增彈性資料庫目標</span><span class="sxs-lookup"><span data-stu-id="32105-119">Example 3: Add an elastic pool target</span></span>
```powershell
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="32105-120">範例 4：新增 s一線地圖目標</span><span class="sxs-lookup"><span data-stu-id="32105-120">Example 4: Add a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="32105-121">將目標 (伺服器、資料庫資料庫、資料庫和 s一體圖) 新到目標群組</span><span class="sxs-lookup"><span data-stu-id="32105-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="32105-122">參數</span><span class="sxs-lookup"><span data-stu-id="32105-122">PARAMETERS</span></span>

### <span data-ttu-id="32105-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="32105-123">-AgentName</span></span>
<span data-ttu-id="32105-124">代理人名稱。</span><span class="sxs-lookup"><span data-stu-id="32105-124">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32105-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="32105-125">-AgentServerName</span></span>
<span data-ttu-id="32105-126">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="32105-126">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32105-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="32105-127">-DatabaseName</span></span>
<span data-ttu-id="32105-128">資料庫目標名稱</span><span class="sxs-lookup"><span data-stu-id="32105-128">Database Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32105-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32105-129">-DefaultProfile</span></span>
<span data-ttu-id="32105-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="32105-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32105-131">-PoolPoolName</span><span class="sxs-lookup"><span data-stu-id="32105-131">-ElasticPoolName</span></span>
<span data-ttu-id="32105-132">集中資料庫目標名稱</span><span class="sxs-lookup"><span data-stu-id="32105-132">Elastic Pool Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlServerOrElasticPoolUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32105-133">-排除</span><span class="sxs-lookup"><span data-stu-id="32105-133">-Exclude</span></span>
<span data-ttu-id="32105-134">排除目標。</span><span class="sxs-lookup"><span data-stu-id="32105-134">Excludes a target.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32105-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="32105-135">-ParentObject</span></span>
<span data-ttu-id="32105-136">目標群組物件。</span><span class="sxs-lookup"><span data-stu-id="32105-136">The target group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32105-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="32105-137">-ParentResourceId</span></span>
<span data-ttu-id="32105-138">目標群組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="32105-138">The target group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32105-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="32105-139">-RefreshCredentialName</span></span>
<span data-ttu-id="32105-140">重新更新認證名稱</span><span class="sxs-lookup"><span data-stu-id="32105-140">Refresh Credential Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlShardMap, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32105-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32105-141">-ResourceGroupName</span></span>
<span data-ttu-id="32105-142">資源組名</span><span class="sxs-lookup"><span data-stu-id="32105-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32105-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="32105-143">-ServerName</span></span>
<span data-ttu-id="32105-144">伺服器目標名稱</span><span class="sxs-lookup"><span data-stu-id="32105-144">Server Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32105-145">-S有圖元名稱</span><span class="sxs-lookup"><span data-stu-id="32105-145">-ShardMapName</span></span>
<span data-ttu-id="32105-146">S一線地圖目標名稱</span><span class="sxs-lookup"><span data-stu-id="32105-146">Shard Map Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlShardMap, SqlShardMapUsingParentObject, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32105-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="32105-147">-TargetGroupName</span></span>
<span data-ttu-id="32105-148">目標群組名。</span><span class="sxs-lookup"><span data-stu-id="32105-148">The target group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32105-149">-確認</span><span class="sxs-lookup"><span data-stu-id="32105-149">-Confirm</span></span>
<span data-ttu-id="32105-150">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="32105-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32105-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32105-151">-WhatIf</span></span>
<span data-ttu-id="32105-152">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32105-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32105-153">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32105-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32105-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32105-154">CommonParameters</span></span>
<span data-ttu-id="32105-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="32105-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32105-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32105-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32105-157">輸入</span><span class="sxs-lookup"><span data-stu-id="32105-157">INPUTS</span></span>

### <span data-ttu-id="32105-158">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="32105-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="32105-159">輸出</span><span class="sxs-lookup"><span data-stu-id="32105-159">OUTPUTS</span></span>

### <span data-ttu-id="32105-160">Microsoft.Azure.management.sql.models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="32105-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="32105-161">筆記</span><span class="sxs-lookup"><span data-stu-id="32105-161">NOTES</span></span>

## <span data-ttu-id="32105-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="32105-162">RELATED LINKS</span></span>
