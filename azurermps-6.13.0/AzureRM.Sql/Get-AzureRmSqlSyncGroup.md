---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: bc4a547ec216cc4c88837f48eadc1c1e80c9087a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454531"
---
# <span data-ttu-id="501be-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="501be-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="501be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="501be-102">SYNOPSIS</span></span>
<span data-ttu-id="501be-103">傳回有關 Azure SQL 資料庫同步處理群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="501be-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="501be-104">句法</span><span class="sxs-lookup"><span data-stu-id="501be-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="501be-105">說明</span><span class="sxs-lookup"><span data-stu-id="501be-105">DESCRIPTION</span></span>
<span data-ttu-id="501be-106">**AzureRmSqlSyncGroup** Cmdlet 會傳回一或多個 Azure SQL 資料庫同步處理群組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="501be-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="501be-107">指定同步群組的名稱，只查看該同步群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="501be-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="501be-108">示例</span><span class="sxs-lookup"><span data-stu-id="501be-108">EXAMPLES</span></span>

### <span data-ttu-id="501be-109">範例1：取得指派給 Azure SQL 資料庫之 Azure SQL 同步處理群組的所有實例</span><span class="sxs-lookup"><span data-stu-id="501be-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
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

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="501be-110">這個命令會取得指派給 Azure SQL 資料庫的所有 Azure SQL 資料庫同步處理群組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="501be-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="501be-111">範例2：取得 Azure SQL 資料庫同步處理群組的相關資訊</span><span class="sxs-lookup"><span data-stu-id="501be-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="501be-112">此命令會取得名為 "SyncGroup01" 的 Azure SQL 資料庫同步處理群組的相關資訊</span><span class="sxs-lookup"><span data-stu-id="501be-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="501be-113">參數</span><span class="sxs-lookup"><span data-stu-id="501be-113">PARAMETERS</span></span>

### <span data-ttu-id="501be-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="501be-114">-DatabaseName</span></span>
<span data-ttu-id="501be-115">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="501be-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="501be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="501be-116">-DefaultProfile</span></span>
<span data-ttu-id="501be-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="501be-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="501be-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="501be-118">-Name</span></span>
<span data-ttu-id="501be-119">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="501be-119">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="501be-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="501be-120">-ResourceGroupName</span></span>
<span data-ttu-id="501be-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="501be-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="501be-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="501be-122">-ServerName</span></span>
<span data-ttu-id="501be-123">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="501be-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="501be-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="501be-124">CommonParameters</span></span>
<span data-ttu-id="501be-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="501be-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="501be-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="501be-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="501be-127">輸入</span><span class="sxs-lookup"><span data-stu-id="501be-127">INPUTS</span></span>

### <span data-ttu-id="501be-128">System.object</span><span class="sxs-lookup"><span data-stu-id="501be-128">System.String</span></span>

## <span data-ttu-id="501be-129">輸出</span><span class="sxs-lookup"><span data-stu-id="501be-129">OUTPUTS</span></span>

### <span data-ttu-id="501be-130">AzureSqlSyncGroupModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="501be-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="501be-131">筆記</span><span class="sxs-lookup"><span data-stu-id="501be-131">NOTES</span></span>

## <span data-ttu-id="501be-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="501be-132">RELATED LINKS</span></span>

[<span data-ttu-id="501be-133">新-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="501be-133">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="501be-134">更新-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="501be-134">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="501be-135">移除-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="501be-135">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

