---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: 66e03a171e0140dc9f84ad0a9161bf0af5af9b4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614653"
---
# <span data-ttu-id="fecc8-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fecc8-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="fecc8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fecc8-102">SYNOPSIS</span></span>
<span data-ttu-id="fecc8-103">更新 Azure SQL 資料庫同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="fecc8-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="fecc8-104">句法</span><span class="sxs-lookup"><span data-stu-id="fecc8-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fecc8-105">說明</span><span class="sxs-lookup"><span data-stu-id="fecc8-105">DESCRIPTION</span></span>
<span data-ttu-id="fecc8-106">**AzSqlSyncGroup** Cmdlet 會修改 Azure SQL 資料庫同步處理群組的屬性。</span><span class="sxs-lookup"><span data-stu-id="fecc8-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="fecc8-107">示例</span><span class="sxs-lookup"><span data-stu-id="fecc8-107">EXAMPLES</span></span>

### <span data-ttu-id="fecc8-108">範例1：更新 Azure SQL 資料庫的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="fecc8-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="fecc8-109">這個命令會更新 Azure SQL 資料庫的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="fecc8-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="fecc8-110">「schema.js開啟」是本機磁片上的檔案。</span><span class="sxs-lookup"><span data-stu-id="fecc8-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="fecc8-111">它包含 json 格式的 shema 負載。</span><span class="sxs-lookup"><span data-stu-id="fecc8-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="fecc8-112">架構 json 的範例為： {"Tables"： [{"欄"： [{"QuotedName"： "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}，{"QuotedName"： "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}]，"QuotedName"： "MayQuotedTable1"}，{"欄"： [{"QuotedName"： "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}，{"QuotedName"： "b3ee3a7f-7614-4644-ad07"： "afa832620b4bManualTestsm4column2，" QuotedName "：" MayQuotedTable2 "}]，" MasterSyncMemberName "：" "}"</span><span class="sxs-lookup"><span data-stu-id="fecc8-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="fecc8-113">參數</span><span class="sxs-lookup"><span data-stu-id="fecc8-113">PARAMETERS</span></span>

### <span data-ttu-id="fecc8-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="fecc8-114">-DatabaseCredential</span></span>
<span data-ttu-id="fecc8-115">中心資料庫的 SQL 驗證認證。</span><span class="sxs-lookup"><span data-stu-id="fecc8-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="fecc8-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fecc8-116">-DatabaseName</span></span>
<span data-ttu-id="fecc8-117">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="fecc8-117">SQL Database name.</span></span>

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

### <span data-ttu-id="fecc8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fecc8-118">-DefaultProfile</span></span>
<span data-ttu-id="fecc8-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fecc8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fecc8-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="fecc8-120">-IntervalInSeconds</span></span>
<span data-ttu-id="fecc8-121">執行資料同步處理的頻率 (，以秒為單位) 。</span><span class="sxs-lookup"><span data-stu-id="fecc8-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="fecc8-122">預設值是-1，這表示不會啟用自動同步處理。</span><span class="sxs-lookup"><span data-stu-id="fecc8-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="fecc8-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="fecc8-123">-Name</span></span>
<span data-ttu-id="fecc8-124">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="fecc8-124">The sync group name.</span></span>

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

### <span data-ttu-id="fecc8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fecc8-125">-ResourceGroupName</span></span>
<span data-ttu-id="fecc8-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fecc8-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="fecc8-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="fecc8-127">-SchemaFile</span></span>
<span data-ttu-id="fecc8-128">架構檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="fecc8-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="fecc8-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fecc8-129">-ServerName</span></span>
<span data-ttu-id="fecc8-130">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fecc8-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="fecc8-131">-確認</span><span class="sxs-lookup"><span data-stu-id="fecc8-131">-Confirm</span></span>
<span data-ttu-id="fecc8-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fecc8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fecc8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fecc8-133">-WhatIf</span></span>
<span data-ttu-id="fecc8-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fecc8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fecc8-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fecc8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fecc8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fecc8-136">CommonParameters</span></span>
<span data-ttu-id="fecc8-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fecc8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fecc8-138">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fecc8-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fecc8-139">輸入</span><span class="sxs-lookup"><span data-stu-id="fecc8-139">INPUTS</span></span>

### <span data-ttu-id="fecc8-140">System.object</span><span class="sxs-lookup"><span data-stu-id="fecc8-140">System.String</span></span>

## <span data-ttu-id="fecc8-141">輸出</span><span class="sxs-lookup"><span data-stu-id="fecc8-141">OUTPUTS</span></span>

### <span data-ttu-id="fecc8-142">AzureSqlSyncGroupModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="fecc8-142">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="fecc8-143">筆記</span><span class="sxs-lookup"><span data-stu-id="fecc8-143">NOTES</span></span>

## <span data-ttu-id="fecc8-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="fecc8-144">RELATED LINKS</span></span>

[<span data-ttu-id="fecc8-145">新-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fecc8-145">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="fecc8-146">移除-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fecc8-146">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="fecc8-147">AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fecc8-147">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

