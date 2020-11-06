---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
ms.openlocfilehash: f8a939dbaac0dadb52aff28b208f7fb69ef836df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452028"
---
# <span data-ttu-id="dabc1-101">Get-AzureRmSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="dabc1-101">Get-AzureRmSqlSyncGroupLog</span></span>

## <span data-ttu-id="dabc1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dabc1-102">SYNOPSIS</span></span>
<span data-ttu-id="dabc1-103">傳回 Azure SQL 資料庫同步處理群組的記錄。</span><span class="sxs-lookup"><span data-stu-id="dabc1-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dabc1-104">句法</span><span class="sxs-lookup"><span data-stu-id="dabc1-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dabc1-105">說明</span><span class="sxs-lookup"><span data-stu-id="dabc1-105">DESCRIPTION</span></span>
<span data-ttu-id="dabc1-106">**AzureRmSqlSyncGroupLog** Cmdlet 會傳回 Azure SQL 資料庫同步處理群組的記錄。</span><span class="sxs-lookup"><span data-stu-id="dabc1-106">The **Get-AzureRmSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="dabc1-107">示例</span><span class="sxs-lookup"><span data-stu-id="dabc1-107">EXAMPLES</span></span>

### <span data-ttu-id="dabc1-108">範例1：取得 Azure SQL 同步處理群組的記錄</span><span class="sxs-lookup"><span data-stu-id="dabc1-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="dabc1-109">這個命令會取得 Azure SQL 同步處理群組的記錄。</span><span class="sxs-lookup"><span data-stu-id="dabc1-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="dabc1-110">參數</span><span class="sxs-lookup"><span data-stu-id="dabc1-110">PARAMETERS</span></span>

### <span data-ttu-id="dabc1-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dabc1-111">-DatabaseName</span></span>
<span data-ttu-id="dabc1-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="dabc1-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="dabc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabc1-113">-DefaultProfile</span></span>
<span data-ttu-id="dabc1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dabc1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dabc1-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="dabc1-115">-EndTime</span></span>
<span data-ttu-id="dabc1-116">要查詢的記錄結束時間。</span><span class="sxs-lookup"><span data-stu-id="dabc1-116">The end time of the logs to query.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabc1-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="dabc1-117">-LogLevel</span></span>
<span data-ttu-id="dabc1-118">要查詢的記錄類型。</span><span class="sxs-lookup"><span data-stu-id="dabc1-118">The type of the logs to query.</span></span>
<span data-ttu-id="dabc1-119">有效值為： "Error"、"Warning"、"Success" 和 "All"。</span><span class="sxs-lookup"><span data-stu-id="dabc1-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabc1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dabc1-120">-ResourceGroupName</span></span>
<span data-ttu-id="dabc1-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dabc1-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="dabc1-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dabc1-122">-ServerName</span></span>
<span data-ttu-id="dabc1-123">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="dabc1-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="dabc1-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dabc1-124">-StartTime</span></span>
<span data-ttu-id="dabc1-125">要查詢之記錄的開始時間。</span><span class="sxs-lookup"><span data-stu-id="dabc1-125">The start time of the logs to query.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabc1-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="dabc1-126">-SyncGroupName</span></span>
<span data-ttu-id="dabc1-127">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="dabc1-127">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabc1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabc1-128">CommonParameters</span></span>
<span data-ttu-id="dabc1-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dabc1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabc1-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dabc1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabc1-131">輸入</span><span class="sxs-lookup"><span data-stu-id="dabc1-131">INPUTS</span></span>

### <span data-ttu-id="dabc1-132">所有</span><span class="sxs-lookup"><span data-stu-id="dabc1-132">None</span></span>
<span data-ttu-id="dabc1-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="dabc1-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dabc1-134">輸出</span><span class="sxs-lookup"><span data-stu-id="dabc1-134">OUTPUTS</span></span>

### <span data-ttu-id="dabc1-135">AzureSqlSyncGroupLogModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="dabc1-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="dabc1-136">筆記</span><span class="sxs-lookup"><span data-stu-id="dabc1-136">NOTES</span></span>

## <span data-ttu-id="dabc1-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="dabc1-137">RELATED LINKS</span></span>
