---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 2205c241625f0bfdc2be21cda34c5bc3d6d07c12
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917625"
---
# <span data-ttu-id="7e38a-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7e38a-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="7e38a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7e38a-102">SYNOPSIS</span></span>
<span data-ttu-id="7e38a-103">獲得伺服器或資料庫的建議索引作業。</span><span class="sxs-lookup"><span data-stu-id="7e38a-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="7e38a-104">語法</span><span class="sxs-lookup"><span data-stu-id="7e38a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e38a-105">描述</span><span class="sxs-lookup"><span data-stu-id="7e38a-105">DESCRIPTION</span></span>
<span data-ttu-id="7e38a-106">**Get-AzSqlDatabaseIndexRecommendation** Cmdlet 會取得 Azure SQL Database 伺服器或資料庫的建議索引作業。</span><span class="sxs-lookup"><span data-stu-id="7e38a-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="7e38a-107">例子</span><span class="sxs-lookup"><span data-stu-id="7e38a-107">EXAMPLES</span></span>

### <span data-ttu-id="7e38a-108">範例 1：取得伺服器上所有資料庫的索引建議</span><span class="sxs-lookup"><span data-stu-id="7e38a-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="7e38a-109">此命令會針對伺服器伺服器01 上的所有資料庫，會返回索引建議。</span><span class="sxs-lookup"><span data-stu-id="7e38a-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="7e38a-110">範例 2：取得特定資料庫的索引建議</span><span class="sxs-lookup"><span data-stu-id="7e38a-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="7e38a-111">此命令會針對特定資料庫返回索引建議。</span><span class="sxs-lookup"><span data-stu-id="7e38a-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="7e38a-112">範例 3：按名稱取得單一索引建議</span><span class="sxs-lookup"><span data-stu-id="7e38a-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="7e38a-113">此命令會按名稱返回單一索引建議。</span><span class="sxs-lookup"><span data-stu-id="7e38a-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="7e38a-114">參數</span><span class="sxs-lookup"><span data-stu-id="7e38a-114">PARAMETERS</span></span>

### <span data-ttu-id="7e38a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e38a-115">-DatabaseName</span></span>
<span data-ttu-id="7e38a-116">指定此 Cmdlet 會提供索引建議的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="7e38a-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="7e38a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e38a-117">-DefaultProfile</span></span>
<span data-ttu-id="7e38a-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7e38a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e38a-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="7e38a-119">-IndexRecommendationName</span></span>
<span data-ttu-id="7e38a-120">指定此 Cmdlet 獲得之索引建議的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e38a-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7e38a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e38a-121">-ResourceGroupName</span></span>
<span data-ttu-id="7e38a-122">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7e38a-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="7e38a-123">此 Cmdlet 會針對此伺服器所託管的資料庫，提供索引建議。</span><span class="sxs-lookup"><span data-stu-id="7e38a-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="7e38a-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7e38a-124">-ServerName</span></span>
<span data-ttu-id="7e38a-125">指定主管此 Cmdlet 會提供索引建議之資料庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="7e38a-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="7e38a-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="7e38a-126">-TableName</span></span>
<span data-ttu-id="7e38a-127">指定 Azure SQL 資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e38a-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="7e38a-128">-確認</span><span class="sxs-lookup"><span data-stu-id="7e38a-128">-Confirm</span></span>
<span data-ttu-id="7e38a-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7e38a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e38a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e38a-130">-WhatIf</span></span>
<span data-ttu-id="7e38a-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7e38a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e38a-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e38a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e38a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e38a-133">CommonParameters</span></span>
<span data-ttu-id="7e38a-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7e38a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e38a-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e38a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e38a-136">輸入</span><span class="sxs-lookup"><span data-stu-id="7e38a-136">INPUTS</span></span>

### <span data-ttu-id="7e38a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="7e38a-137">System.String</span></span>

## <span data-ttu-id="7e38a-138">輸出</span><span class="sxs-lookup"><span data-stu-id="7e38a-138">OUTPUTS</span></span>

### <span data-ttu-id="7e38a-139">Microsoft.Azure.Commands.sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7e38a-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="7e38a-140">筆記</span><span class="sxs-lookup"><span data-stu-id="7e38a-140">NOTES</span></span>

## <span data-ttu-id="7e38a-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e38a-141">RELATED LINKS</span></span>

[<span data-ttu-id="7e38a-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7e38a-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="7e38a-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7e38a-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
