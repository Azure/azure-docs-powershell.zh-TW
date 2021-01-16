---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: cdf50079a08a4ac021e78e210ae574aa978674fe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285895"
---
# <span data-ttu-id="ba019-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="ba019-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="ba019-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba019-102">SYNOPSIS</span></span>
<span data-ttu-id="ba019-103">將目標新增至目標群組</span><span class="sxs-lookup"><span data-stu-id="ba019-103">Adds a target to a target group</span></span>

## <span data-ttu-id="ba019-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba019-104">SYNTAX</span></span>

### <span data-ttu-id="ba019-105">SqlDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="ba019-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba019-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="ba019-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba019-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="ba019-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba019-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ba019-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba019-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ba019-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba019-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ba019-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba019-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ba019-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba019-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ba019-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba019-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ba019-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba019-114">說明</span><span class="sxs-lookup"><span data-stu-id="ba019-114">DESCRIPTION</span></span>
<span data-ttu-id="ba019-115">Add-AzSqlElasticJobTarget Cmdlet 會將目標資源新增至目標群組</span><span class="sxs-lookup"><span data-stu-id="ba019-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="ba019-116">示例</span><span class="sxs-lookup"><span data-stu-id="ba019-116">EXAMPLES</span></span>

### <span data-ttu-id="ba019-117">範例1：新增伺服器目標</span><span class="sxs-lookup"><span data-stu-id="ba019-117">Example 1: Add a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="ba019-118">範例2：新增資料庫目標</span><span class="sxs-lookup"><span data-stu-id="ba019-118">Example 2: Add a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="ba019-119">範例3：新增彈性池目標</span><span class="sxs-lookup"><span data-stu-id="ba019-119">Example 3: Add an elastic pool target</span></span>
```powershell
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="ba019-120">範例4：新增 shard 地圖目標</span><span class="sxs-lookup"><span data-stu-id="ba019-120">Example 4: Add a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="ba019-121">將目標 (伺服器、彈性 pool、database 及 shard map) 新增至目標群組</span><span class="sxs-lookup"><span data-stu-id="ba019-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="ba019-122">參數</span><span class="sxs-lookup"><span data-stu-id="ba019-122">PARAMETERS</span></span>

### <span data-ttu-id="ba019-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="ba019-123">-AgentName</span></span>
<span data-ttu-id="ba019-124">[代理程式名稱]。</span><span class="sxs-lookup"><span data-stu-id="ba019-124">The agent name.</span></span>

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

### <span data-ttu-id="ba019-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="ba019-125">-AgentServerName</span></span>
<span data-ttu-id="ba019-126">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ba019-126">The server name.</span></span>

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

### <span data-ttu-id="ba019-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba019-127">-DatabaseName</span></span>
<span data-ttu-id="ba019-128">資料庫目標名稱</span><span class="sxs-lookup"><span data-stu-id="ba019-128">Database Target Name</span></span>

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

### <span data-ttu-id="ba019-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba019-129">-DefaultProfile</span></span>
<span data-ttu-id="ba019-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba019-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba019-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ba019-131">-ElasticPoolName</span></span>
<span data-ttu-id="ba019-132">彈性池目標名稱</span><span class="sxs-lookup"><span data-stu-id="ba019-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="ba019-133">-排除</span><span class="sxs-lookup"><span data-stu-id="ba019-133">-Exclude</span></span>
<span data-ttu-id="ba019-134">排除目標。</span><span class="sxs-lookup"><span data-stu-id="ba019-134">Excludes a target.</span></span>

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

### <span data-ttu-id="ba019-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ba019-135">-ParentObject</span></span>
<span data-ttu-id="ba019-136">目標群組物件。</span><span class="sxs-lookup"><span data-stu-id="ba019-136">The target group object.</span></span>

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

### <span data-ttu-id="ba019-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ba019-137">-ParentResourceId</span></span>
<span data-ttu-id="ba019-138">[目標群組資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="ba019-138">The target group resource id.</span></span>

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

### <span data-ttu-id="ba019-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="ba019-139">-RefreshCredentialName</span></span>
<span data-ttu-id="ba019-140">重新整理認證名稱</span><span class="sxs-lookup"><span data-stu-id="ba019-140">Refresh Credential Name</span></span>

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

### <span data-ttu-id="ba019-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba019-141">-ResourceGroupName</span></span>
<span data-ttu-id="ba019-142">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ba019-142">Resource Group Name</span></span>

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

### <span data-ttu-id="ba019-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ba019-143">-ServerName</span></span>
<span data-ttu-id="ba019-144">伺服器目標名稱</span><span class="sxs-lookup"><span data-stu-id="ba019-144">Server Target Name</span></span>

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

### <span data-ttu-id="ba019-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="ba019-145">-ShardMapName</span></span>
<span data-ttu-id="ba019-146">Shard 地圖目標名稱</span><span class="sxs-lookup"><span data-stu-id="ba019-146">Shard Map Target Name</span></span>

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

### <span data-ttu-id="ba019-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="ba019-147">-TargetGroupName</span></span>
<span data-ttu-id="ba019-148">目標群組名。</span><span class="sxs-lookup"><span data-stu-id="ba019-148">The target group name.</span></span>

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

### <span data-ttu-id="ba019-149">-確認</span><span class="sxs-lookup"><span data-stu-id="ba019-149">-Confirm</span></span>
<span data-ttu-id="ba019-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ba019-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba019-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba019-151">-WhatIf</span></span>
<span data-ttu-id="ba019-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba019-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba019-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba019-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba019-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba019-154">CommonParameters</span></span>
<span data-ttu-id="ba019-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba019-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba019-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ba019-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba019-157">輸入</span><span class="sxs-lookup"><span data-stu-id="ba019-157">INPUTS</span></span>

### <span data-ttu-id="ba019-158">AzureSqlElasticJobTargetGroupModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="ba019-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="ba019-159">輸出</span><span class="sxs-lookup"><span data-stu-id="ba019-159">OUTPUTS</span></span>

### <span data-ttu-id="ba019-160">JobTarget 中的 [.Sql]</span><span class="sxs-lookup"><span data-stu-id="ba019-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="ba019-161">筆記</span><span class="sxs-lookup"><span data-stu-id="ba019-161">NOTES</span></span>

## <span data-ttu-id="ba019-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba019-162">RELATED LINKS</span></span>
