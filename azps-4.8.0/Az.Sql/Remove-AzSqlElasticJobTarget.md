---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 4bd797528b3656364594f28f72d2b9ce2f7fdfaa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127254"
---
# <span data-ttu-id="f4c99-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="f4c99-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="f4c99-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4c99-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c99-103">從目標群組中移除目標</span><span class="sxs-lookup"><span data-stu-id="f4c99-103">Removes the target from the target group</span></span>

## <span data-ttu-id="f4c99-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4c99-104">SYNTAX</span></span>

### <span data-ttu-id="f4c99-105">SqlDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="f4c99-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4c99-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="f4c99-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4c99-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="f4c99-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4c99-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f4c99-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4c99-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f4c99-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4c99-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f4c99-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4c99-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f4c99-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4c99-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f4c99-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4c99-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f4c99-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4c99-114">說明</span><span class="sxs-lookup"><span data-stu-id="f4c99-114">DESCRIPTION</span></span>
<span data-ttu-id="f4c99-115">Remove-AzSqlElasticJobTarget Cmdlet 會將目標資源移除至目標群組</span><span class="sxs-lookup"><span data-stu-id="f4c99-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="f4c99-116">示例</span><span class="sxs-lookup"><span data-stu-id="f4c99-116">EXAMPLES</span></span>

### <span data-ttu-id="f4c99-117">範例1：移除伺服器目標</span><span class="sxs-lookup"><span data-stu-id="f4c99-117">Example 1: Remove a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="f4c99-118">範例2：移除資料庫目標</span><span class="sxs-lookup"><span data-stu-id="f4c99-118">Example 2: Remove a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="f4c99-119">範例3：移除彈性池目標</span><span class="sxs-lookup"><span data-stu-id="f4c99-119">Example 3: Remove an elastic pool target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="f4c99-120">範例4：移除 shard 對應目標</span><span class="sxs-lookup"><span data-stu-id="f4c99-120">Example 4: Remove a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="f4c99-121">從目標群組移除目標 (伺服器、彈性 pool、database 及 shard map) </span><span class="sxs-lookup"><span data-stu-id="f4c99-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="f4c99-122">參數</span><span class="sxs-lookup"><span data-stu-id="f4c99-122">PARAMETERS</span></span>

### <span data-ttu-id="f4c99-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f4c99-123">-AgentName</span></span>
<span data-ttu-id="f4c99-124">SQL 資料庫代理程式名稱。</span><span class="sxs-lookup"><span data-stu-id="f4c99-124">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="f4c99-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="f4c99-125">-AgentServerName</span></span>
<span data-ttu-id="f4c99-126">SQL 資料庫代理伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f4c99-126">SQL Database Agent Server Name.</span></span>

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

### <span data-ttu-id="f4c99-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4c99-127">-DatabaseName</span></span>
<span data-ttu-id="f4c99-128">資料庫目標名稱</span><span class="sxs-lookup"><span data-stu-id="f4c99-128">Database Target Name</span></span>

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

### <span data-ttu-id="f4c99-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4c99-129">-DefaultProfile</span></span>
<span data-ttu-id="f4c99-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4c99-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4c99-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f4c99-131">-ElasticPoolName</span></span>
<span data-ttu-id="f4c99-132">彈性池目標名稱</span><span class="sxs-lookup"><span data-stu-id="f4c99-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="f4c99-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f4c99-133">-ParentObject</span></span>
<span data-ttu-id="f4c99-134">目標群組物件。</span><span class="sxs-lookup"><span data-stu-id="f4c99-134">The target group object.</span></span>

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

### <span data-ttu-id="f4c99-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f4c99-135">-ParentResourceId</span></span>
<span data-ttu-id="f4c99-136">[目標群組資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f4c99-136">The target group resource id.</span></span>

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

### <span data-ttu-id="f4c99-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="f4c99-137">-RefreshCredentialName</span></span>
<span data-ttu-id="f4c99-138">重新整理認證名稱</span><span class="sxs-lookup"><span data-stu-id="f4c99-138">Refresh Credential Name</span></span>

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

### <span data-ttu-id="f4c99-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4c99-139">-ResourceGroupName</span></span>
<span data-ttu-id="f4c99-140">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f4c99-140">Resource Group Name</span></span>

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

### <span data-ttu-id="f4c99-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f4c99-141">-ServerName</span></span>
<span data-ttu-id="f4c99-142">伺服器目標名稱</span><span class="sxs-lookup"><span data-stu-id="f4c99-142">Server Target Name</span></span>

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

### <span data-ttu-id="f4c99-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="f4c99-143">-ShardMapName</span></span>
<span data-ttu-id="f4c99-144">Shard 地圖目標名稱</span><span class="sxs-lookup"><span data-stu-id="f4c99-144">Shard Map Target Name</span></span>

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

### <span data-ttu-id="f4c99-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="f4c99-145">-TargetGroupName</span></span>
<span data-ttu-id="f4c99-146">SQL 資料庫代理程式名稱。</span><span class="sxs-lookup"><span data-stu-id="f4c99-146">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="f4c99-147">-確認</span><span class="sxs-lookup"><span data-stu-id="f4c99-147">-Confirm</span></span>
<span data-ttu-id="f4c99-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4c99-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4c99-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4c99-149">-WhatIf</span></span>
<span data-ttu-id="f4c99-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4c99-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4c99-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4c99-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4c99-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c99-152">CommonParameters</span></span>
<span data-ttu-id="f4c99-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4c99-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c99-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f4c99-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c99-155">輸入</span><span class="sxs-lookup"><span data-stu-id="f4c99-155">INPUTS</span></span>

### <span data-ttu-id="f4c99-156">AzureSqlElasticJobTargetGroupModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="f4c99-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="f4c99-157">輸出</span><span class="sxs-lookup"><span data-stu-id="f4c99-157">OUTPUTS</span></span>

### <span data-ttu-id="f4c99-158">JobTarget 中的 [.Sql]</span><span class="sxs-lookup"><span data-stu-id="f4c99-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="f4c99-159">筆記</span><span class="sxs-lookup"><span data-stu-id="f4c99-159">NOTES</span></span>

## <span data-ttu-id="f4c99-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4c99-160">RELATED LINKS</span></span>
