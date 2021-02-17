---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 7f13b1a1a5daad4e7c97de962943bb859f6a09df
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399476"
---
# <span data-ttu-id="c323c-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c323c-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="c323c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c323c-102">SYNOPSIS</span></span>
<span data-ttu-id="c323c-103">停止執行建議索引作業的工作流程。</span><span class="sxs-lookup"><span data-stu-id="c323c-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="c323c-104">語法</span><span class="sxs-lookup"><span data-stu-id="c323c-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c323c-105">描述</span><span class="sxs-lookup"><span data-stu-id="c323c-105">DESCRIPTION</span></span>
<span data-ttu-id="c323c-106">**Stop-AzSqlDatabaseExecuteIndexRecommendation** Cmdlet 會停止執行建議索引作業的工作流程。</span><span class="sxs-lookup"><span data-stu-id="c323c-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="c323c-107">例子</span><span class="sxs-lookup"><span data-stu-id="c323c-107">EXAMPLES</span></span>

### <span data-ttu-id="c323c-108">範例 1：停止執行索引建議</span><span class="sxs-lookup"><span data-stu-id="c323c-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="c323c-109">此命令停止執行索引建議。</span><span class="sxs-lookup"><span data-stu-id="c323c-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="c323c-110">參數</span><span class="sxs-lookup"><span data-stu-id="c323c-110">PARAMETERS</span></span>

### <span data-ttu-id="c323c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c323c-111">-DatabaseName</span></span>
<span data-ttu-id="c323c-112">指定此 Cmdlet 停止工作流程的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="c323c-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="c323c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c323c-113">-DefaultProfile</span></span>
<span data-ttu-id="c323c-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c323c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c323c-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="c323c-115">-IndexRecommendationName</span></span>
<span data-ttu-id="c323c-116">指定此 Cmdlet 停止的索引建議名稱。</span><span class="sxs-lookup"><span data-stu-id="c323c-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="c323c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c323c-117">-ResourceGroupName</span></span>
<span data-ttu-id="c323c-118">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c323c-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c323c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c323c-119">-ServerName</span></span>
<span data-ttu-id="c323c-120">指定主管此 Cmdlet 停止工作流程之資料庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="c323c-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="c323c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c323c-121">CommonParameters</span></span>
<span data-ttu-id="c323c-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c323c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c323c-123">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c323c-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c323c-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c323c-124">INPUTS</span></span>

### <span data-ttu-id="c323c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c323c-125">System.String</span></span>

## <span data-ttu-id="c323c-126">輸出</span><span class="sxs-lookup"><span data-stu-id="c323c-126">OUTPUTS</span></span>

### <span data-ttu-id="c323c-127">Microsoft.Azure.Commands.sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c323c-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="c323c-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c323c-128">NOTES</span></span>

## <span data-ttu-id="c323c-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c323c-129">RELATED LINKS</span></span>


[<span data-ttu-id="c323c-130">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c323c-130">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="c323c-131">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="c323c-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


