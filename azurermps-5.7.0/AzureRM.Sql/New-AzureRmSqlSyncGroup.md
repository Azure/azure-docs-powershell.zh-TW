---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 65ac7bb4a63fa8519bd8f0b0c006209d5f171833
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450437"
---
# <span data-ttu-id="3fc38-101">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3fc38-101">New-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="3fc38-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fc38-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc38-103">建立 Azure SQL 資料庫同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="3fc38-103">Creates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fc38-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fc38-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3fc38-105">說明</span><span class="sxs-lookup"><span data-stu-id="3fc38-105">DESCRIPTION</span></span>
<span data-ttu-id="3fc38-106">**新的-AzureRmSqlSyncGroup** Cmdlet 會建立 Azure SQL 資料庫同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="3fc38-106">The **New-AzureRmSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="3fc38-107">示例</span><span class="sxs-lookup"><span data-stu-id="3fc38-107">EXAMPLES</span></span>

### <span data-ttu-id="3fc38-108">範例1：建立 Azure SQL 資料庫的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="3fc38-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
-DatabaseCredential $credential -IntervalInSeconds 100 -SyncDatabaseServerName "syncDatabaseServer01" -SyncDatabaseName "syncDatabaseName01"
-SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" -Schema ".\schema.json" | Format-List
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

<span data-ttu-id="3fc38-109">這個命令會建立 Azure SQL 資料庫的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="3fc38-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="3fc38-110">「schema.js開啟」是本機磁片上的檔案。</span><span class="sxs-lookup"><span data-stu-id="3fc38-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="3fc38-111">它包含 json 格式的 shema 負載。</span><span class="sxs-lookup"><span data-stu-id="3fc38-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="3fc38-112">架構 json 的範例為： {"Tables"： [{"欄"： [{"QuotedName"： "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}，{"QuotedName"： "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}]，"QuotedName"： "MayQuotedTable1"}，{"欄"： [{"QuotedName"： "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}，{"QuotedName"： "b3ee3a7f-7614-4644-ad07"： "afa832620b4bManualTestsm4column2，" QuotedName "：" MayQuotedTable2 "}]，" MasterSyncMemberName "：" "}"</span><span class="sxs-lookup"><span data-stu-id="3fc38-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="3fc38-113">參數</span><span class="sxs-lookup"><span data-stu-id="3fc38-113">PARAMETERS</span></span>

### <span data-ttu-id="3fc38-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="3fc38-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="3fc38-115">在同步群組中解決中心與成員資料庫之間 confliction 的原則。</span><span class="sxs-lookup"><span data-stu-id="3fc38-115">The policy of resolving confliction between hub and member database in the sync group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="3fc38-116">-DatabaseCredential</span></span>
<span data-ttu-id="3fc38-117">中心資料庫的 SQL 驗證認證。</span><span class="sxs-lookup"><span data-stu-id="3fc38-117">The SQL authentication credential of the hub database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3fc38-118">-DatabaseName</span></span>
<span data-ttu-id="3fc38-119">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fc38-119">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fc38-120">-DefaultProfile</span></span>
<span data-ttu-id="3fc38-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3fc38-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3fc38-122">-IntervalInSeconds</span></span>
<span data-ttu-id="3fc38-123">執行資料同步處理的頻率 (，以秒為單位) 。</span><span class="sxs-lookup"><span data-stu-id="3fc38-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="3fc38-124">預設值是-1，這表示不會啟用自動同步處理。</span><span class="sxs-lookup"><span data-stu-id="3fc38-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="3fc38-125">-Name</span></span>
<span data-ttu-id="3fc38-126">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="3fc38-126">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fc38-127">-ResourceGroupName</span></span>
<span data-ttu-id="3fc38-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fc38-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="3fc38-129">-SchemaFile</span></span>
<span data-ttu-id="3fc38-130">架構檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="3fc38-130">The path of the schema file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3fc38-131">-ServerName</span></span>
<span data-ttu-id="3fc38-132">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fc38-132">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3fc38-133">-SyncDatabaseName</span></span>
<span data-ttu-id="3fc38-134">用來儲存同步處理相關中繼資料的資料庫。</span><span class="sxs-lookup"><span data-stu-id="3fc38-134">The database used to store sync related metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fc38-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="3fc38-136">同步處理中繼資料資料庫所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3fc38-136">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="3fc38-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="3fc38-138">在其上託管同步處理中繼資料資料庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="3fc38-138">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-139">-確認</span><span class="sxs-lookup"><span data-stu-id="3fc38-139">-Confirm</span></span>
<span data-ttu-id="3fc38-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3fc38-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fc38-141">-WhatIf</span></span>
<span data-ttu-id="3fc38-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3fc38-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fc38-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fc38-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc38-144">CommonParameters</span></span>
<span data-ttu-id="3fc38-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fc38-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc38-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3fc38-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc38-147">輸入</span><span class="sxs-lookup"><span data-stu-id="3fc38-147">INPUTS</span></span>

### <span data-ttu-id="3fc38-148">所有</span><span class="sxs-lookup"><span data-stu-id="3fc38-148">None</span></span>
<span data-ttu-id="3fc38-149">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3fc38-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3fc38-150">輸出</span><span class="sxs-lookup"><span data-stu-id="3fc38-150">OUTPUTS</span></span>

### <span data-ttu-id="3fc38-151">AzureSqlSyncGroupModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="3fc38-151">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="3fc38-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3fc38-152">NOTES</span></span>

## <span data-ttu-id="3fc38-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fc38-153">RELATED LINKS</span></span>

[<span data-ttu-id="3fc38-154">Set-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3fc38-154">Set-AzureRmSqlSyncGroup</span></span>](./Set-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="3fc38-155">移除-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3fc38-155">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="3fc38-156">AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3fc38-156">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

