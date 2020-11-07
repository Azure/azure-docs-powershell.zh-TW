---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: d4cb344f63b871f55668c4de7205ada80ff04f35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624653"
---
# <span data-ttu-id="90bef-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="90bef-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="90bef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90bef-102">SYNOPSIS</span></span>
<span data-ttu-id="90bef-103">停止執行建議索引作業的工作流程。</span><span class="sxs-lookup"><span data-stu-id="90bef-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90bef-104">句法</span><span class="sxs-lookup"><span data-stu-id="90bef-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90bef-105">說明</span><span class="sxs-lookup"><span data-stu-id="90bef-105">DESCRIPTION</span></span>
<span data-ttu-id="90bef-106">**AzureRmSqlDatabaseExecuteIndexRecommendation** Cmdlet 會停止執行建議的索引作業的工作流程。</span><span class="sxs-lookup"><span data-stu-id="90bef-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="90bef-107">示例</span><span class="sxs-lookup"><span data-stu-id="90bef-107">EXAMPLES</span></span>

### <span data-ttu-id="90bef-108">範例1：停止執行索引建議</span><span class="sxs-lookup"><span data-stu-id="90bef-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="90bef-109">這個命令會停止執行索引建議。</span><span class="sxs-lookup"><span data-stu-id="90bef-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="90bef-110">參數</span><span class="sxs-lookup"><span data-stu-id="90bef-110">PARAMETERS</span></span>

### <span data-ttu-id="90bef-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="90bef-111">-DatabaseName</span></span>
<span data-ttu-id="90bef-112">指定此 Cmdlet 停止工作流程之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="90bef-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90bef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90bef-113">-DefaultProfile</span></span>
<span data-ttu-id="90bef-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="90bef-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90bef-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="90bef-115">-IndexRecommendationName</span></span>
<span data-ttu-id="90bef-116">指定此 Cmdlet 停止的索引建議名稱。</span><span class="sxs-lookup"><span data-stu-id="90bef-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90bef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90bef-117">-ResourceGroupName</span></span>
<span data-ttu-id="90bef-118">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90bef-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="90bef-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="90bef-119">-ServerName</span></span>
<span data-ttu-id="90bef-120">指定主持此 Cmdlet 停止工作流程之資料庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="90bef-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90bef-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90bef-121">CommonParameters</span></span>
<span data-ttu-id="90bef-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90bef-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90bef-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90bef-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90bef-124">輸入</span><span class="sxs-lookup"><span data-stu-id="90bef-124">INPUTS</span></span>

### <span data-ttu-id="90bef-125">所有</span><span class="sxs-lookup"><span data-stu-id="90bef-125">None</span></span>
<span data-ttu-id="90bef-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="90bef-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="90bef-127">輸出</span><span class="sxs-lookup"><span data-stu-id="90bef-127">OUTPUTS</span></span>

## <span data-ttu-id="90bef-128">筆記</span><span class="sxs-lookup"><span data-stu-id="90bef-128">NOTES</span></span>

## <span data-ttu-id="90bef-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="90bef-129">RELATED LINKS</span></span>

[<span data-ttu-id="90bef-130">AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="90bef-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="90bef-131">開始-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="90bef-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="90bef-132">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="90bef-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


