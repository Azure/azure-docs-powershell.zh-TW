---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956706"
---
# <span data-ttu-id="5db4e-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="5db4e-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="5db4e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5db4e-102">SYNOPSIS</span></span>
<span data-ttu-id="5db4e-103">傳回 Azure SQL 資料庫同步處理群組的記錄。</span><span class="sxs-lookup"><span data-stu-id="5db4e-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="5db4e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5db4e-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5db4e-105">說明</span><span class="sxs-lookup"><span data-stu-id="5db4e-105">DESCRIPTION</span></span>
<span data-ttu-id="5db4e-106">**AzSqlSyncGroupLog** Cmdlet 會傳回 Azure SQL 資料庫同步處理群組的記錄。</span><span class="sxs-lookup"><span data-stu-id="5db4e-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="5db4e-107">示例</span><span class="sxs-lookup"><span data-stu-id="5db4e-107">EXAMPLES</span></span>

### <span data-ttu-id="5db4e-108">範例1：取得 Azure SQL 同步處理群組的記錄</span><span class="sxs-lookup"><span data-stu-id="5db4e-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="5db4e-109">這個命令會取得 Azure SQL 同步處理群組的記錄。</span><span class="sxs-lookup"><span data-stu-id="5db4e-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="5db4e-110">參數</span><span class="sxs-lookup"><span data-stu-id="5db4e-110">PARAMETERS</span></span>

### <span data-ttu-id="5db4e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5db4e-111">-DatabaseName</span></span>
<span data-ttu-id="5db4e-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5db4e-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="5db4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db4e-113">-DefaultProfile</span></span>
<span data-ttu-id="5db4e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5db4e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5db4e-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5db4e-115">-EndTime</span></span>
<span data-ttu-id="5db4e-116">要查詢的記錄結束時間。</span><span class="sxs-lookup"><span data-stu-id="5db4e-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="5db4e-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="5db4e-117">-LogLevel</span></span>
<span data-ttu-id="5db4e-118">要查詢的記錄類型。</span><span class="sxs-lookup"><span data-stu-id="5db4e-118">The type of the logs to query.</span></span>
<span data-ttu-id="5db4e-119">有效值為： "Error"、"Warning"、"Success" 和 "All"。</span><span class="sxs-lookup"><span data-stu-id="5db4e-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="5db4e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db4e-120">-ResourceGroupName</span></span>
<span data-ttu-id="5db4e-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5db4e-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="5db4e-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5db4e-122">-ServerName</span></span>
<span data-ttu-id="5db4e-123">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5db4e-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="5db4e-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5db4e-124">-StartTime</span></span>
<span data-ttu-id="5db4e-125">要查詢之記錄的開始時間。</span><span class="sxs-lookup"><span data-stu-id="5db4e-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="5db4e-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5db4e-126">-SyncGroupName</span></span>
<span data-ttu-id="5db4e-127">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="5db4e-127">The sync group name.</span></span>

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

### <span data-ttu-id="5db4e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db4e-128">CommonParameters</span></span>
<span data-ttu-id="5db4e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5db4e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db4e-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5db4e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db4e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="5db4e-131">INPUTS</span></span>

### <span data-ttu-id="5db4e-132">System.object</span><span class="sxs-lookup"><span data-stu-id="5db4e-132">System.String</span></span>

## <span data-ttu-id="5db4e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5db4e-133">OUTPUTS</span></span>

### <span data-ttu-id="5db4e-134">AzureSqlSyncGroupLogModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="5db4e-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="5db4e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5db4e-135">NOTES</span></span>

## <span data-ttu-id="5db4e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="5db4e-136">RELATED LINKS</span></span>
