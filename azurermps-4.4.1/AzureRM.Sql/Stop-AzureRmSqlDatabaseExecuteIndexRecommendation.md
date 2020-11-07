---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 4fef918efd69d1ef5506efb70f1db94903845a8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625654"
---
# <span data-ttu-id="cb0bf-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="cb0bf-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="cb0bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb0bf-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0bf-103">停止執行建議索引作業的工作流程。</span><span class="sxs-lookup"><span data-stu-id="cb0bf-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb0bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb0bf-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb0bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb0bf-105">DESCRIPTION</span></span>
<span data-ttu-id="cb0bf-106">**AzureRmSqlDatabaseExecuteIndexRecommendation** Cmdlet 會停止執行建議的索引作業的工作流程。</span><span class="sxs-lookup"><span data-stu-id="cb0bf-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="cb0bf-107">示例</span><span class="sxs-lookup"><span data-stu-id="cb0bf-107">EXAMPLES</span></span>

### <span data-ttu-id="cb0bf-108">範例1：停止執行索引建議</span><span class="sxs-lookup"><span data-stu-id="cb0bf-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="cb0bf-109">這個命令會停止執行索引建議。</span><span class="sxs-lookup"><span data-stu-id="cb0bf-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="cb0bf-110">參數</span><span class="sxs-lookup"><span data-stu-id="cb0bf-110">PARAMETERS</span></span>

### <span data-ttu-id="cb0bf-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cb0bf-111">-DatabaseName</span></span>
<span data-ttu-id="cb0bf-112">指定此 Cmdlet 停止工作流程之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb0bf-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="cb0bf-113">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="cb0bf-113">-IndexRecommendationName</span></span>
<span data-ttu-id="cb0bf-114">指定此 Cmdlet 停止的索引建議名稱。</span><span class="sxs-lookup"><span data-stu-id="cb0bf-114">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="cb0bf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb0bf-115">-ResourceGroupName</span></span>
<span data-ttu-id="cb0bf-116">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb0bf-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="cb0bf-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb0bf-117">-ServerName</span></span>
<span data-ttu-id="cb0bf-118">指定主持此 Cmdlet 停止工作流程之資料庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="cb0bf-118">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="cb0bf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb0bf-119">-DefaultProfile</span></span>
<span data-ttu-id="cb0bf-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb0bf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb0bf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0bf-121">CommonParameters</span></span>
<span data-ttu-id="cb0bf-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb0bf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0bf-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb0bf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0bf-124">輸入</span><span class="sxs-lookup"><span data-stu-id="cb0bf-124">INPUTS</span></span>

## <span data-ttu-id="cb0bf-125">輸出</span><span class="sxs-lookup"><span data-stu-id="cb0bf-125">OUTPUTS</span></span>

## <span data-ttu-id="cb0bf-126">筆記</span><span class="sxs-lookup"><span data-stu-id="cb0bf-126">NOTES</span></span>

## <span data-ttu-id="cb0bf-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb0bf-127">RELATED LINKS</span></span>

[<span data-ttu-id="cb0bf-128">AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="cb0bf-128">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="cb0bf-129">開始-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="cb0bf-129">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="cb0bf-130">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="cb0bf-130">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


