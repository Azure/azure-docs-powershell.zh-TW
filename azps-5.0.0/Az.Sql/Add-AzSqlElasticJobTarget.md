---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: cdf50079a08a4ac021e78e210ae574aa978674fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136653"
---
# <span data-ttu-id="e3296-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="e3296-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="e3296-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3296-102">SYNOPSIS</span></span>
<span data-ttu-id="e3296-103">將目標新增至目標群組</span><span class="sxs-lookup"><span data-stu-id="e3296-103">Adds a target to a target group</span></span>

## <span data-ttu-id="e3296-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3296-104">SYNTAX</span></span>

### <span data-ttu-id="e3296-105">SqlDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="e3296-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3296-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="e3296-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3296-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="e3296-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3296-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="e3296-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3296-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="e3296-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3296-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="e3296-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3296-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e3296-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3296-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e3296-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3296-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e3296-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3296-114">說明</span><span class="sxs-lookup"><span data-stu-id="e3296-114">DESCRIPTION</span></span>
<span data-ttu-id="e3296-115">Add-AzSqlElasticJobTarget Cmdlet 會將目標資源新增至目標群組</span><span class="sxs-lookup"><span data-stu-id="e3296-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="e3296-116">示例</span><span class="sxs-lookup"><span data-stu-id="e3296-116">EXAMPLES</span></span>

### <span data-ttu-id="e3296-117">範例1：新增伺服器目標</span><span class="sxs-lookup"><span data-stu-id="e3296-117">Example 1: Add a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="e3296-118">範例2：新增資料庫目標</span><span class="sxs-lookup"><span data-stu-id="e3296-118">Example 2: Add a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="e3296-119">範例3：新增彈性池目標</span><span class="sxs-lookup"><span data-stu-id="e3296-119">Example 3: Add an elastic pool target</span></span>
```powershell
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="e3296-120">範例4：新增 shard 地圖目標</span><span class="sxs-lookup"><span data-stu-id="e3296-120">Example 4: Add a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="e3296-121">將目標 (伺服器、彈性 pool、database 及 shard map) 新增至目標群組</span><span class="sxs-lookup"><span data-stu-id="e3296-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="e3296-122">參數</span><span class="sxs-lookup"><span data-stu-id="e3296-122">PARAMETERS</span></span>

### <span data-ttu-id="e3296-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e3296-123">-AgentName</span></span>
<span data-ttu-id="e3296-124">[代理程式名稱]。</span><span class="sxs-lookup"><span data-stu-id="e3296-124">The agent name.</span></span>

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

### <span data-ttu-id="e3296-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="e3296-125">-AgentServerName</span></span>
<span data-ttu-id="e3296-126">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="e3296-126">The server name.</span></span>

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

### <span data-ttu-id="e3296-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e3296-127">-DatabaseName</span></span>
<span data-ttu-id="e3296-128">資料庫目標名稱</span><span class="sxs-lookup"><span data-stu-id="e3296-128">Database Target Name</span></span>

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

### <span data-ttu-id="e3296-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3296-129">-DefaultProfile</span></span>
<span data-ttu-id="e3296-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3296-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3296-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e3296-131">-ElasticPoolName</span></span>
<span data-ttu-id="e3296-132">彈性池目標名稱</span><span class="sxs-lookup"><span data-stu-id="e3296-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="e3296-133">-排除</span><span class="sxs-lookup"><span data-stu-id="e3296-133">-Exclude</span></span>
<span data-ttu-id="e3296-134">排除目標。</span><span class="sxs-lookup"><span data-stu-id="e3296-134">Excludes a target.</span></span>

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

### <span data-ttu-id="e3296-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e3296-135">-ParentObject</span></span>
<span data-ttu-id="e3296-136">目標群組物件。</span><span class="sxs-lookup"><span data-stu-id="e3296-136">The target group object.</span></span>

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

### <span data-ttu-id="e3296-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e3296-137">-ParentResourceId</span></span>
<span data-ttu-id="e3296-138">[目標群組資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e3296-138">The target group resource id.</span></span>

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

### <span data-ttu-id="e3296-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="e3296-139">-RefreshCredentialName</span></span>
<span data-ttu-id="e3296-140">重新整理認證名稱</span><span class="sxs-lookup"><span data-stu-id="e3296-140">Refresh Credential Name</span></span>

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

### <span data-ttu-id="e3296-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3296-141">-ResourceGroupName</span></span>
<span data-ttu-id="e3296-142">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e3296-142">Resource Group Name</span></span>

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

### <span data-ttu-id="e3296-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e3296-143">-ServerName</span></span>
<span data-ttu-id="e3296-144">伺服器目標名稱</span><span class="sxs-lookup"><span data-stu-id="e3296-144">Server Target Name</span></span>

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

### <span data-ttu-id="e3296-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="e3296-145">-ShardMapName</span></span>
<span data-ttu-id="e3296-146">Shard 地圖目標名稱</span><span class="sxs-lookup"><span data-stu-id="e3296-146">Shard Map Target Name</span></span>

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

### <span data-ttu-id="e3296-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="e3296-147">-TargetGroupName</span></span>
<span data-ttu-id="e3296-148">目標群組名。</span><span class="sxs-lookup"><span data-stu-id="e3296-148">The target group name.</span></span>

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

### <span data-ttu-id="e3296-149">-確認</span><span class="sxs-lookup"><span data-stu-id="e3296-149">-Confirm</span></span>
<span data-ttu-id="e3296-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3296-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3296-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3296-151">-WhatIf</span></span>
<span data-ttu-id="e3296-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3296-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3296-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3296-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3296-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3296-154">CommonParameters</span></span>
<span data-ttu-id="e3296-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3296-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3296-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e3296-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3296-157">輸入</span><span class="sxs-lookup"><span data-stu-id="e3296-157">INPUTS</span></span>

### <span data-ttu-id="e3296-158">AzureSqlElasticJobTargetGroupModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="e3296-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="e3296-159">輸出</span><span class="sxs-lookup"><span data-stu-id="e3296-159">OUTPUTS</span></span>

### <span data-ttu-id="e3296-160">JobTarget 中的 [.Sql]</span><span class="sxs-lookup"><span data-stu-id="e3296-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="e3296-161">筆記</span><span class="sxs-lookup"><span data-stu-id="e3296-161">NOTES</span></span>

## <span data-ttu-id="e3296-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3296-162">RELATED LINKS</span></span>
