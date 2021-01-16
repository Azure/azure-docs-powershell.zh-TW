---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285644"
---
# <span data-ttu-id="4a223-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="4a223-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="4a223-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a223-102">SYNOPSIS</span></span>
<span data-ttu-id="4a223-103">傳回 Azure SQL 資料庫同步處理群組的記錄。</span><span class="sxs-lookup"><span data-stu-id="4a223-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="4a223-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a223-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a223-105">說明</span><span class="sxs-lookup"><span data-stu-id="4a223-105">DESCRIPTION</span></span>
<span data-ttu-id="4a223-106">**AzSqlSyncGroupLog** Cmdlet 會傳回 Azure SQL 資料庫同步處理群組的記錄。</span><span class="sxs-lookup"><span data-stu-id="4a223-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="4a223-107">示例</span><span class="sxs-lookup"><span data-stu-id="4a223-107">EXAMPLES</span></span>

### <span data-ttu-id="4a223-108">範例1：取得 Azure SQL 同步處理群組的記錄</span><span class="sxs-lookup"><span data-stu-id="4a223-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="4a223-109">這個命令會取得 Azure SQL 同步處理群組的記錄。</span><span class="sxs-lookup"><span data-stu-id="4a223-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="4a223-110">參數</span><span class="sxs-lookup"><span data-stu-id="4a223-110">PARAMETERS</span></span>

### <span data-ttu-id="4a223-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a223-111">-DatabaseName</span></span>
<span data-ttu-id="4a223-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a223-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="4a223-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a223-113">-DefaultProfile</span></span>
<span data-ttu-id="4a223-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4a223-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a223-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4a223-115">-EndTime</span></span>
<span data-ttu-id="4a223-116">要查詢的記錄結束時間。</span><span class="sxs-lookup"><span data-stu-id="4a223-116">The end time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a223-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="4a223-117">-LogLevel</span></span>
<span data-ttu-id="4a223-118">要查詢的記錄類型。</span><span class="sxs-lookup"><span data-stu-id="4a223-118">The type of the logs to query.</span></span>
<span data-ttu-id="4a223-119">有效值為： "Error"、"Warning"、"Success" 和 "All"。</span><span class="sxs-lookup"><span data-stu-id="4a223-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a223-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a223-120">-ResourceGroupName</span></span>
<span data-ttu-id="4a223-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a223-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a223-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4a223-122">-ServerName</span></span>
<span data-ttu-id="4a223-123">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a223-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="4a223-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4a223-124">-StartTime</span></span>
<span data-ttu-id="4a223-125">要查詢之記錄的開始時間。</span><span class="sxs-lookup"><span data-stu-id="4a223-125">The start time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a223-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4a223-126">-SyncGroupName</span></span>
<span data-ttu-id="4a223-127">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="4a223-127">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a223-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a223-128">CommonParameters</span></span>
<span data-ttu-id="4a223-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a223-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a223-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4a223-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a223-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4a223-131">INPUTS</span></span>

### <span data-ttu-id="4a223-132">System.object</span><span class="sxs-lookup"><span data-stu-id="4a223-132">System.String</span></span>

## <span data-ttu-id="4a223-133">輸出</span><span class="sxs-lookup"><span data-stu-id="4a223-133">OUTPUTS</span></span>

### <span data-ttu-id="4a223-134">AzureSqlSyncGroupLogModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="4a223-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="4a223-135">筆記</span><span class="sxs-lookup"><span data-stu-id="4a223-135">NOTES</span></span>

## <span data-ttu-id="4a223-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a223-136">RELATED LINKS</span></span>
