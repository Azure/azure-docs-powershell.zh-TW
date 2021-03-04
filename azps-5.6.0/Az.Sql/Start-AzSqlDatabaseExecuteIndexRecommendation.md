---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 74beb667ec01af4661c2f56daa6a3159d960622a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907997"
---
# <span data-ttu-id="4632a-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="4632a-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="4632a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4632a-102">SYNOPSIS</span></span>
<span data-ttu-id="4632a-103">啟動執行建議索引作業的工作流程。</span><span class="sxs-lookup"><span data-stu-id="4632a-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="4632a-104">語法</span><span class="sxs-lookup"><span data-stu-id="4632a-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4632a-105">描述</span><span class="sxs-lookup"><span data-stu-id="4632a-105">DESCRIPTION</span></span>
<span data-ttu-id="4632a-106">**Start-AzSqlDatabaseExecuteIndexRecommendation** Cmdlet 會啟動工作流程，針對 Azure SQL Database 執行建議的索引作業。</span><span class="sxs-lookup"><span data-stu-id="4632a-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="4632a-107">例子</span><span class="sxs-lookup"><span data-stu-id="4632a-107">EXAMPLES</span></span>

### <span data-ttu-id="4632a-108">範例 1：執行索引建議</span><span class="sxs-lookup"><span data-stu-id="4632a-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="4632a-109">此命令會執行索引建議。</span><span class="sxs-lookup"><span data-stu-id="4632a-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="4632a-110">參數</span><span class="sxs-lookup"><span data-stu-id="4632a-110">PARAMETERS</span></span>

### <span data-ttu-id="4632a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4632a-111">-DatabaseName</span></span>
<span data-ttu-id="4632a-112">指定此 Cmdlet 啟動工作流程的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="4632a-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="4632a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4632a-113">-DefaultProfile</span></span>
<span data-ttu-id="4632a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4632a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4632a-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="4632a-115">-IndexRecommendationName</span></span>
<span data-ttu-id="4632a-116">指定此 Cmdlet 執行之索引建議的名稱。</span><span class="sxs-lookup"><span data-stu-id="4632a-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="4632a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4632a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4632a-118">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4632a-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4632a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4632a-119">-ServerName</span></span>
<span data-ttu-id="4632a-120">指定主管此 Cmdlet 啟動工作流程之資料庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="4632a-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="4632a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4632a-121">CommonParameters</span></span>
<span data-ttu-id="4632a-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4632a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4632a-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4632a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4632a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="4632a-124">INPUTS</span></span>

### <span data-ttu-id="4632a-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4632a-125">System.String</span></span>

## <span data-ttu-id="4632a-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4632a-126">OUTPUTS</span></span>

### <span data-ttu-id="4632a-127">Microsoft.Azure.Commands.sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="4632a-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="4632a-128">筆記</span><span class="sxs-lookup"><span data-stu-id="4632a-128">NOTES</span></span>

## <span data-ttu-id="4632a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4632a-129">RELATED LINKS</span></span>

[<span data-ttu-id="4632a-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="4632a-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="4632a-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="4632a-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="4632a-132">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="4632a-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


