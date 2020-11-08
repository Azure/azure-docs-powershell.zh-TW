---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: e69cffe6955a5bf19636dd519c0906be64ce4413
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129789"
---
# <span data-ttu-id="e9bc8-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="e9bc8-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="e9bc8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="e9bc8-103">啟動執行建議索引作業的工作流程。</span><span class="sxs-lookup"><span data-stu-id="e9bc8-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="e9bc8-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9bc8-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9bc8-105">說明</span><span class="sxs-lookup"><span data-stu-id="e9bc8-105">DESCRIPTION</span></span>
<span data-ttu-id="e9bc8-106">**Start AzSqlDatabaseExecuteIndexRecommendation** Cmdlet 會啟動工作流程，以針對 Azure SQL 資料庫執行建議的索引作業。</span><span class="sxs-lookup"><span data-stu-id="e9bc8-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="e9bc8-107">示例</span><span class="sxs-lookup"><span data-stu-id="e9bc8-107">EXAMPLES</span></span>

### <span data-ttu-id="e9bc8-108">範例1：執行索引建議</span><span class="sxs-lookup"><span data-stu-id="e9bc8-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="e9bc8-109">這個命令會執行索引建議。</span><span class="sxs-lookup"><span data-stu-id="e9bc8-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="e9bc8-110">參數</span><span class="sxs-lookup"><span data-stu-id="e9bc8-110">PARAMETERS</span></span>

### <span data-ttu-id="e9bc8-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e9bc8-111">-DatabaseName</span></span>
<span data-ttu-id="e9bc8-112">指定此 Cmdlet 啟動工作流程的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e9bc8-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="e9bc8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9bc8-113">-DefaultProfile</span></span>
<span data-ttu-id="e9bc8-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e9bc8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9bc8-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="e9bc8-115">-IndexRecommendationName</span></span>
<span data-ttu-id="e9bc8-116">指定此 Cmdlet 執行之索引建議的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9bc8-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="e9bc8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9bc8-117">-ResourceGroupName</span></span>
<span data-ttu-id="e9bc8-118">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9bc8-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e9bc8-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e9bc8-119">-ServerName</span></span>
<span data-ttu-id="e9bc8-120">指定主持此 Cmdlet 啟動工作流程之資料庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="e9bc8-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="e9bc8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9bc8-121">CommonParameters</span></span>
<span data-ttu-id="e9bc8-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9bc8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9bc8-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e9bc8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9bc8-124">輸入</span><span class="sxs-lookup"><span data-stu-id="e9bc8-124">INPUTS</span></span>

### <span data-ttu-id="e9bc8-125">System.object</span><span class="sxs-lookup"><span data-stu-id="e9bc8-125">System.String</span></span>

## <span data-ttu-id="e9bc8-126">輸出</span><span class="sxs-lookup"><span data-stu-id="e9bc8-126">OUTPUTS</span></span>

### <span data-ttu-id="e9bc8-127">IndexRecommendation （.Sql）命令</span><span class="sxs-lookup"><span data-stu-id="e9bc8-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="e9bc8-128">筆記</span><span class="sxs-lookup"><span data-stu-id="e9bc8-128">NOTES</span></span>

## <span data-ttu-id="e9bc8-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9bc8-129">RELATED LINKS</span></span>

[<span data-ttu-id="e9bc8-130">AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="e9bc8-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="e9bc8-131">停止 AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="e9bc8-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="e9bc8-132">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="e9bc8-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

