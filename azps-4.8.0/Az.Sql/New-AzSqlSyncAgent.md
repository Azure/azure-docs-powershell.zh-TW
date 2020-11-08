---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
ms.openlocfilehash: 4a4ce99eb30aaa959eabdc9c1385b567aef2b0fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129852"
---
# <span data-ttu-id="b8a6b-101">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b8a6b-101">New-AzSqlSyncAgent</span></span>

## <span data-ttu-id="b8a6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a6b-103">建立 Azure SQL 同步處理代理程式。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-103">Creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="b8a6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8a6b-104">SYNTAX</span></span>

### <span data-ttu-id="b8a6b-105">SyncDatabaseComponent (預設) </span><span class="sxs-lookup"><span data-stu-id="b8a6b-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8a6b-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="b8a6b-106">SyncDatabaseResourceID</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8a6b-107">說明</span><span class="sxs-lookup"><span data-stu-id="b8a6b-107">DESCRIPTION</span></span>
<span data-ttu-id="b8a6b-108">**AzSqlSyncAgent** Cmdlet 會建立 Azure SQL 同步處理代理程式。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-108">The **New-AzSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="b8a6b-109">示例</span><span class="sxs-lookup"><span data-stu-id="b8a6b-109">EXAMPLES</span></span>

### <span data-ttu-id="b8a6b-110">範例1：建立 Azure SQL server 的同步處理代理程式。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
-SyncDatabaseName "syncDatabaseName01" -SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 
Version                     : 4.2.0.0
IsUpToDate                  : True
ExpiryTime                  : 12/31/9999 11:59:59 PM
State                       : NeverConnected
```

<span data-ttu-id="b8a6b-111">這個命令會建立 Azure SQL server 的同步處理代理程式。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="b8a6b-112">參數</span><span class="sxs-lookup"><span data-stu-id="b8a6b-112">PARAMETERS</span></span>

### <span data-ttu-id="b8a6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a6b-113">-DefaultProfile</span></span>
<span data-ttu-id="b8a6b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b8a6b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8a6b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8a6b-115">-Name</span></span>
<span data-ttu-id="b8a6b-116">同步處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a6b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a6b-117">-ResourceGroupName</span></span>
<span data-ttu-id="b8a6b-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="b8a6b-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b8a6b-119">-ServerName</span></span>
<span data-ttu-id="b8a6b-120">同步處理常式所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="b8a6b-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b8a6b-121">-SyncDatabaseName</span></span>
<span data-ttu-id="b8a6b-122">用來儲存同步處理相關中繼資料的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-122">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a6b-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a6b-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="b8a6b-124">同步處理中繼資料資料庫所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a6b-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="b8a6b-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="b8a6b-126">同步處理中繼資料資料庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a6b-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="b8a6b-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="b8a6b-128">在其上託管同步處理中繼資料資料庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a6b-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b8a6b-129">-Confirm</span></span>
<span data-ttu-id="b8a6b-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8a6b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8a6b-131">-WhatIf</span></span>
<span data-ttu-id="b8a6b-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8a6b-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8a6b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a6b-134">CommonParameters</span></span>
<span data-ttu-id="b8a6b-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a6b-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b8a6b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a6b-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b8a6b-137">INPUTS</span></span>

### <span data-ttu-id="b8a6b-138">System.object</span><span class="sxs-lookup"><span data-stu-id="b8a6b-138">System.String</span></span>

## <span data-ttu-id="b8a6b-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b8a6b-139">OUTPUTS</span></span>

### <span data-ttu-id="b8a6b-140">AzureSqlSyncAgentModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="b8a6b-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="b8a6b-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b8a6b-141">NOTES</span></span>

## <span data-ttu-id="b8a6b-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8a6b-142">RELATED LINKS</span></span>

[<span data-ttu-id="b8a6b-143">移除-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b8a6b-143">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="b8a6b-144">AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b8a6b-144">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

