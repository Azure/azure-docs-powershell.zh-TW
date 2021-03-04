---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
ms.openlocfilehash: b3cd900760821765d135810acaaafdeac45c0eb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916350"
---
# <span data-ttu-id="d90de-101">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="d90de-101">New-AzSqlSyncAgent</span></span>

## <span data-ttu-id="d90de-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d90de-102">SYNOPSIS</span></span>
<span data-ttu-id="d90de-103">建立 Azure SQL 同步代理程式。</span><span class="sxs-lookup"><span data-stu-id="d90de-103">Creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="d90de-104">語法</span><span class="sxs-lookup"><span data-stu-id="d90de-104">SYNTAX</span></span>

### <span data-ttu-id="d90de-105">SyncDatabaseComponent (預設) </span><span class="sxs-lookup"><span data-stu-id="d90de-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d90de-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="d90de-106">SyncDatabaseResourceID</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d90de-107">描述</span><span class="sxs-lookup"><span data-stu-id="d90de-107">DESCRIPTION</span></span>
<span data-ttu-id="d90de-108">**New-AzSqlSyncAgent** Cmdlet 會建立 Azure SQL 同步代理程式。</span><span class="sxs-lookup"><span data-stu-id="d90de-108">The **New-AzSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="d90de-109">例子</span><span class="sxs-lookup"><span data-stu-id="d90de-109">EXAMPLES</span></span>

### <span data-ttu-id="d90de-110">範例 1：為 Azure SQL 伺服器建立同步處理代理程式。</span><span class="sxs-lookup"><span data-stu-id="d90de-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
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

<span data-ttu-id="d90de-111">此命令會為 Azure SQL 伺服器建立同步處理代理程式。</span><span class="sxs-lookup"><span data-stu-id="d90de-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="d90de-112">參數</span><span class="sxs-lookup"><span data-stu-id="d90de-112">PARAMETERS</span></span>

### <span data-ttu-id="d90de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d90de-113">-DefaultProfile</span></span>
<span data-ttu-id="d90de-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d90de-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d90de-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d90de-115">-Name</span></span>
<span data-ttu-id="d90de-116">同步代理程式名稱。</span><span class="sxs-lookup"><span data-stu-id="d90de-116">The sync agent name.</span></span>

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

### <span data-ttu-id="d90de-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d90de-117">-ResourceGroupName</span></span>
<span data-ttu-id="d90de-118">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d90de-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="d90de-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d90de-119">-ServerName</span></span>
<span data-ttu-id="d90de-120">同步處理代理程式位於 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d90de-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="d90de-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d90de-121">-SyncDatabaseName</span></span>
<span data-ttu-id="d90de-122">用來儲存同步處理相關中繼資料的資料庫。</span><span class="sxs-lookup"><span data-stu-id="d90de-122">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="d90de-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d90de-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="d90de-124">同步中繼資料資料庫所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d90de-124">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="d90de-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="d90de-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="d90de-126">同步中繼資料資料庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d90de-126">The resource ID of  the sync metadata database.</span></span>

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

### <span data-ttu-id="d90de-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="d90de-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="d90de-128">託管同步處理中繼資料資料庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="d90de-128">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="d90de-129">-確認</span><span class="sxs-lookup"><span data-stu-id="d90de-129">-Confirm</span></span>
<span data-ttu-id="d90de-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d90de-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d90de-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d90de-131">-WhatIf</span></span>
<span data-ttu-id="d90de-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d90de-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d90de-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d90de-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d90de-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d90de-134">CommonParameters</span></span>
<span data-ttu-id="d90de-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d90de-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d90de-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d90de-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d90de-137">輸入</span><span class="sxs-lookup"><span data-stu-id="d90de-137">INPUTS</span></span>

### <span data-ttu-id="d90de-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d90de-138">System.String</span></span>

## <span data-ttu-id="d90de-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d90de-139">OUTPUTS</span></span>

### <span data-ttu-id="d90de-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="d90de-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="d90de-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d90de-141">NOTES</span></span>

## <span data-ttu-id="d90de-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d90de-142">RELATED LINKS</span></span>

[<span data-ttu-id="d90de-143">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="d90de-143">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="d90de-144">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="d90de-144">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

