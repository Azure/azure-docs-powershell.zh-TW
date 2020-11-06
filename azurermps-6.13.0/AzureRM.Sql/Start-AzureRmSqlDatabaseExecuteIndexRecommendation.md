---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: c61f1bd988410b696eddd12162958333022dd892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448175"
---
# <span data-ttu-id="d4dfc-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d4dfc-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="d4dfc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="d4dfc-103">啟動執行建議索引作業的工作流程。</span><span class="sxs-lookup"><span data-stu-id="d4dfc-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4dfc-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4dfc-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4dfc-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="d4dfc-106">**Start AzureRmSqlDatabaseExecuteIndexRecommendation** Cmdlet 會啟動工作流程，以針對 Azure SQL 資料庫執行建議的索引作業。</span><span class="sxs-lookup"><span data-stu-id="d4dfc-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="d4dfc-107">示例</span><span class="sxs-lookup"><span data-stu-id="d4dfc-107">EXAMPLES</span></span>

### <span data-ttu-id="d4dfc-108">範例1：執行索引建議</span><span class="sxs-lookup"><span data-stu-id="d4dfc-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="d4dfc-109">這個命令會執行索引建議。</span><span class="sxs-lookup"><span data-stu-id="d4dfc-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="d4dfc-110">參數</span><span class="sxs-lookup"><span data-stu-id="d4dfc-110">PARAMETERS</span></span>

### <span data-ttu-id="d4dfc-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d4dfc-111">-DatabaseName</span></span>
<span data-ttu-id="d4dfc-112">指定此 Cmdlet 啟動工作流程的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="d4dfc-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="d4dfc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4dfc-113">-DefaultProfile</span></span>
<span data-ttu-id="d4dfc-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d4dfc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4dfc-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="d4dfc-115">-IndexRecommendationName</span></span>
<span data-ttu-id="d4dfc-116">指定此 Cmdlet 執行之索引建議的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4dfc-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="d4dfc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4dfc-117">-ResourceGroupName</span></span>
<span data-ttu-id="d4dfc-118">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4dfc-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d4dfc-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d4dfc-119">-ServerName</span></span>
<span data-ttu-id="d4dfc-120">指定主持此 Cmdlet 啟動工作流程之資料庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="d4dfc-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="d4dfc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4dfc-121">CommonParameters</span></span>
<span data-ttu-id="d4dfc-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4dfc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4dfc-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4dfc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4dfc-124">輸入</span><span class="sxs-lookup"><span data-stu-id="d4dfc-124">INPUTS</span></span>

### <span data-ttu-id="d4dfc-125">System.object</span><span class="sxs-lookup"><span data-stu-id="d4dfc-125">System.String</span></span>

## <span data-ttu-id="d4dfc-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d4dfc-126">OUTPUTS</span></span>

### <span data-ttu-id="d4dfc-127">IndexRecommendation （.Sql）命令</span><span class="sxs-lookup"><span data-stu-id="d4dfc-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="d4dfc-128">筆記</span><span class="sxs-lookup"><span data-stu-id="d4dfc-128">NOTES</span></span>

## <span data-ttu-id="d4dfc-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4dfc-129">RELATED LINKS</span></span>

[<span data-ttu-id="d4dfc-130">AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="d4dfc-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="d4dfc-131">停止 AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d4dfc-131">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="d4dfc-132">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="d4dfc-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


