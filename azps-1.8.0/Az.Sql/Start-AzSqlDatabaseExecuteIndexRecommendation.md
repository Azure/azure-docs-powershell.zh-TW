---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 1ab1e223ec173cf5727011956f52979026159594
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399510"
---
# <span data-ttu-id="79d09-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="79d09-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="79d09-102">簡介</span><span class="sxs-lookup"><span data-stu-id="79d09-102">SYNOPSIS</span></span>
<span data-ttu-id="79d09-103">啟動執行建議索引作業的工作流程。</span><span class="sxs-lookup"><span data-stu-id="79d09-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="79d09-104">語法</span><span class="sxs-lookup"><span data-stu-id="79d09-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79d09-105">描述</span><span class="sxs-lookup"><span data-stu-id="79d09-105">DESCRIPTION</span></span>
<span data-ttu-id="79d09-106">**Start-AzSqlDatabaseExecuteIndexRecommendation** Cmdlet 會啟動工作流程，針對 Azure SQL Database 執行建議的索引作業。</span><span class="sxs-lookup"><span data-stu-id="79d09-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="79d09-107">例子</span><span class="sxs-lookup"><span data-stu-id="79d09-107">EXAMPLES</span></span>

### <span data-ttu-id="79d09-108">範例 1：執行索引建議</span><span class="sxs-lookup"><span data-stu-id="79d09-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="79d09-109">此命令會執行索引建議。</span><span class="sxs-lookup"><span data-stu-id="79d09-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="79d09-110">參數</span><span class="sxs-lookup"><span data-stu-id="79d09-110">PARAMETERS</span></span>

### <span data-ttu-id="79d09-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="79d09-111">-DatabaseName</span></span>
<span data-ttu-id="79d09-112">指定此 Cmdlet 啟動工作流程的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="79d09-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="79d09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79d09-113">-DefaultProfile</span></span>
<span data-ttu-id="79d09-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="79d09-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79d09-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="79d09-115">-IndexRecommendationName</span></span>
<span data-ttu-id="79d09-116">指定此 Cmdlet 執行之索引建議的名稱。</span><span class="sxs-lookup"><span data-stu-id="79d09-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="79d09-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79d09-117">-ResourceGroupName</span></span>
<span data-ttu-id="79d09-118">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="79d09-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="79d09-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="79d09-119">-ServerName</span></span>
<span data-ttu-id="79d09-120">指定主管此 Cmdlet 啟動工作流程之資料庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="79d09-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="79d09-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d09-121">CommonParameters</span></span>
<span data-ttu-id="79d09-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="79d09-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d09-123">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79d09-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d09-124">輸入</span><span class="sxs-lookup"><span data-stu-id="79d09-124">INPUTS</span></span>

### <span data-ttu-id="79d09-125">System.String</span><span class="sxs-lookup"><span data-stu-id="79d09-125">System.String</span></span>

## <span data-ttu-id="79d09-126">輸出</span><span class="sxs-lookup"><span data-stu-id="79d09-126">OUTPUTS</span></span>

### <span data-ttu-id="79d09-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="79d09-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="79d09-128">筆記</span><span class="sxs-lookup"><span data-stu-id="79d09-128">NOTES</span></span>

## <span data-ttu-id="79d09-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="79d09-129">RELATED LINKS</span></span>


[<span data-ttu-id="79d09-130">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="79d09-130">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="79d09-131">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="79d09-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


