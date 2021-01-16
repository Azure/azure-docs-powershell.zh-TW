---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 9dd14e1f8b61978575501700346157d7c22c0111
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285716"
---
# <span data-ttu-id="d5be6-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d5be6-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="d5be6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5be6-102">SYNOPSIS</span></span>
<span data-ttu-id="d5be6-103">取得伺服器或資料庫的建議索引作業。</span><span class="sxs-lookup"><span data-stu-id="d5be6-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="d5be6-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5be6-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5be6-105">說明</span><span class="sxs-lookup"><span data-stu-id="d5be6-105">DESCRIPTION</span></span>
<span data-ttu-id="d5be6-106">**AzSqlDatabaseIndexRecommendation** Cmdlet 會取得 Azure SQL 資料庫伺服器或資料庫的建議索引作業。</span><span class="sxs-lookup"><span data-stu-id="d5be6-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="d5be6-107">示例</span><span class="sxs-lookup"><span data-stu-id="d5be6-107">EXAMPLES</span></span>

### <span data-ttu-id="d5be6-108">範例1：取得伺服器上所有資料庫的索引建議</span><span class="sxs-lookup"><span data-stu-id="d5be6-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="d5be6-109">這個命令會針對伺服器 server01 上的所有資料庫傳回索引建議。</span><span class="sxs-lookup"><span data-stu-id="d5be6-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="d5be6-110">範例2：取得特定資料庫的索引建議</span><span class="sxs-lookup"><span data-stu-id="d5be6-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="d5be6-111">這個命令會傳回特定資料庫的索引建議。</span><span class="sxs-lookup"><span data-stu-id="d5be6-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="d5be6-112">範例3：依名稱取得單一索引建議</span><span class="sxs-lookup"><span data-stu-id="d5be6-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="d5be6-113">這個命令會依名稱傳回單一索引建議。</span><span class="sxs-lookup"><span data-stu-id="d5be6-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="d5be6-114">參數</span><span class="sxs-lookup"><span data-stu-id="d5be6-114">PARAMETERS</span></span>

### <span data-ttu-id="d5be6-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d5be6-115">-DatabaseName</span></span>
<span data-ttu-id="d5be6-116">指定此 Cmdlet 取得索引建議之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5be6-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5be6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5be6-117">-DefaultProfile</span></span>
<span data-ttu-id="d5be6-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d5be6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5be6-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="d5be6-119">-IndexRecommendationName</span></span>
<span data-ttu-id="d5be6-120">指定此 Cmdlet 所取得之索引建議的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5be6-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5be6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5be6-121">-ResourceGroupName</span></span>
<span data-ttu-id="d5be6-122">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5be6-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="d5be6-123">這個 Cmdlet 會取得此伺服器託管之資料庫的索引建議。</span><span class="sxs-lookup"><span data-stu-id="d5be6-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="d5be6-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d5be6-124">-ServerName</span></span>
<span data-ttu-id="d5be6-125">指定主持此 Cmdlet 之資料庫的伺服器，以取得索引建議。</span><span class="sxs-lookup"><span data-stu-id="d5be6-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5be6-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="d5be6-126">-TableName</span></span>
<span data-ttu-id="d5be6-127">指定 Azure SQL 資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5be6-127">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5be6-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d5be6-128">-Confirm</span></span>
<span data-ttu-id="d5be6-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d5be6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5be6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5be6-130">-WhatIf</span></span>
<span data-ttu-id="d5be6-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d5be6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5be6-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5be6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5be6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5be6-133">CommonParameters</span></span>
<span data-ttu-id="d5be6-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5be6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5be6-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d5be6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5be6-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d5be6-136">INPUTS</span></span>

### <span data-ttu-id="d5be6-137">System.object</span><span class="sxs-lookup"><span data-stu-id="d5be6-137">System.String</span></span>

## <span data-ttu-id="d5be6-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d5be6-138">OUTPUTS</span></span>

### <span data-ttu-id="d5be6-139">IndexRecommendation （.Sql）命令</span><span class="sxs-lookup"><span data-stu-id="d5be6-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="d5be6-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d5be6-140">NOTES</span></span>

## <span data-ttu-id="d5be6-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5be6-141">RELATED LINKS</span></span>

[<span data-ttu-id="d5be6-142">開始-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d5be6-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="d5be6-143">停止 AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d5be6-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
