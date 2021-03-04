---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: c95b6a7a42327b7380e19ff333453f956797dcdc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916470"
---
# <span data-ttu-id="7d567-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7d567-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="7d567-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7d567-102">SYNOPSIS</span></span>
<span data-ttu-id="7d567-103">更新 Azure SQL 資料庫同步組。</span><span class="sxs-lookup"><span data-stu-id="7d567-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="7d567-104">語法</span><span class="sxs-lookup"><span data-stu-id="7d567-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-UsePrivateLinkConnection <Boolean>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d567-105">描述</span><span class="sxs-lookup"><span data-stu-id="7d567-105">DESCRIPTION</span></span>
<span data-ttu-id="7d567-106">**Update-AzSqlSyncGroup** Cmdlet 會修改 Azure SQL 資料庫同步組的屬性。</span><span class="sxs-lookup"><span data-stu-id="7d567-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="7d567-107">例子</span><span class="sxs-lookup"><span data-stu-id="7d567-107">EXAMPLES</span></span>

### <span data-ttu-id="7d567-108">範例 1：更新 Azure SQL Database 的同步組。</span><span class="sxs-lookup"><span data-stu-id="7d567-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
-DatabaseCredential $credential -IntervalInSeconds 100 -Schema ".\schema.json" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="7d567-109">此命令會更新 Azure SQL 資料庫的同步組。</span><span class="sxs-lookup"><span data-stu-id="7d567-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="7d567-110">「schema.js」是一個位於本地磁片中的檔案。</span><span class="sxs-lookup"><span data-stu-id="7d567-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="7d567-111">它包含 json 格式的架構負載。</span><span class="sxs-lookup"><span data-stu-id="7d567-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="7d567-112">架構 json 的範例為：{"Tables"： [{"Columns"： [{"QuotedName"： "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}， {"QuotedName"： "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}]， "QuotedName"： "MayQuotedTable1"}， {"Columns"： [{"QuotedName"： "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}， {"QuotedName"： "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}]， "QuotedName"： "MayQuotedTable2"}]， "MasterSyncMemberName"： Null }</span><span class="sxs-lookup"><span data-stu-id="7d567-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="7d567-113">參數</span><span class="sxs-lookup"><span data-stu-id="7d567-113">PARAMETERS</span></span>

### <span data-ttu-id="7d567-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="7d567-114">-DatabaseCredential</span></span>
<span data-ttu-id="7d567-115">中樞資料庫的 SQL 驗證認證。</span><span class="sxs-lookup"><span data-stu-id="7d567-115">The SQL authentication credential of the hub database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d567-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7d567-116">-DatabaseName</span></span>
<span data-ttu-id="7d567-117">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="7d567-117">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d567-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d567-118">-DefaultProfile</span></span>
<span data-ttu-id="7d567-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7d567-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d567-120">-IntervalIn以秒為單位</span><span class="sxs-lookup"><span data-stu-id="7d567-120">-IntervalInSeconds</span></span>
<span data-ttu-id="7d567-121">執行資料 (的頻率) 秒。</span><span class="sxs-lookup"><span data-stu-id="7d567-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="7d567-122">預設值為 -1，這表示未啟用自動同步處理。</span><span class="sxs-lookup"><span data-stu-id="7d567-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="7d567-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d567-123">-Name</span></span>
<span data-ttu-id="7d567-124">同步組名。</span><span class="sxs-lookup"><span data-stu-id="7d567-124">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d567-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d567-125">-ResourceGroupName</span></span>
<span data-ttu-id="7d567-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d567-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d567-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="7d567-127">-SchemaFile</span></span>
<span data-ttu-id="7d567-128">架構檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="7d567-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="7d567-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7d567-129">-ServerName</span></span>
<span data-ttu-id="7d567-130">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d567-130">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d567-131">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7d567-131">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="7d567-132">當連接到此同步群組的中樞時，是否要使用私人連結連接。</span><span class="sxs-lookup"><span data-stu-id="7d567-132">Whether to use a private link connection when connecting to the hub of this sync group.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d567-133">-確認</span><span class="sxs-lookup"><span data-stu-id="7d567-133">-Confirm</span></span>
<span data-ttu-id="7d567-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7d567-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d567-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d567-135">-WhatIf</span></span>
<span data-ttu-id="7d567-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d567-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d567-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d567-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d567-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d567-138">CommonParameters</span></span>
<span data-ttu-id="7d567-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7d567-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d567-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d567-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d567-141">輸入</span><span class="sxs-lookup"><span data-stu-id="7d567-141">INPUTS</span></span>

### <span data-ttu-id="7d567-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7d567-142">System.String</span></span>

## <span data-ttu-id="7d567-143">輸出</span><span class="sxs-lookup"><span data-stu-id="7d567-143">OUTPUTS</span></span>

### <span data-ttu-id="7d567-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="7d567-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="7d567-145">筆記</span><span class="sxs-lookup"><span data-stu-id="7d567-145">NOTES</span></span>

## <span data-ttu-id="7d567-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d567-146">RELATED LINKS</span></span>

[<span data-ttu-id="7d567-147">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7d567-147">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="7d567-148">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7d567-148">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="7d567-149">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7d567-149">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

