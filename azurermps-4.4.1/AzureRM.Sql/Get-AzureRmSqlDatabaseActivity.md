---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: b37ae31c1f0dc6360743a863f0305fd5823cbb3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455579"
---
# <span data-ttu-id="fc929-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="fc929-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="fc929-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc929-102">SYNOPSIS</span></span>
<span data-ttu-id="fc929-103">取得移動彈性資料庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="fc929-103">Gets the status of moving elastic databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc929-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc929-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> -ElasticPoolName <String> -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc929-105">說明</span><span class="sxs-lookup"><span data-stu-id="fc929-105">DESCRIPTION</span></span>
<span data-ttu-id="fc929-106">**AzureRmSqlDatabaseActivity** Cmdlet 會取得彈性資料庫在 Azure SQL 資料庫中的彈性資料庫池中移動的狀態。</span><span class="sxs-lookup"><span data-stu-id="fc929-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of elastic databases moving into or out of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="fc929-107">示例</span><span class="sxs-lookup"><span data-stu-id="fc929-107">EXAMPLES</span></span>

### <span data-ttu-id="fc929-108">範例1：取得所有 SQL 資料庫實例的狀態</span><span class="sxs-lookup"><span data-stu-id="fc929-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="fc929-109">這個命令會傳回一個名為 ElasticPool01 的彈性池中所有 SQL 資料庫實例的操作狀態。</span><span class="sxs-lookup"><span data-stu-id="fc929-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="fc929-110">參數</span><span class="sxs-lookup"><span data-stu-id="fc929-110">PARAMETERS</span></span>

### <span data-ttu-id="fc929-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc929-111">-DatabaseName</span></span>
<span data-ttu-id="fc929-112">指定此 Cmdlet 取得狀態之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc929-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="fc929-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fc929-113">-ElasticPoolName</span></span>
<span data-ttu-id="fc929-114">指定此 Cmdlet 取得狀態的彈性資料庫池的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc929-114">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="fc929-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="fc929-115">-OperationId</span></span>
<span data-ttu-id="fc929-116">指定此 Cmdlet 取得的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc929-116">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc929-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc929-117">-ResourceGroupName</span></span>
<span data-ttu-id="fc929-118">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc929-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="fc929-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fc929-119">-ServerName</span></span>
<span data-ttu-id="fc929-120">指定主持彈性資料庫池之 Microsoft SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc929-120">Specifies the name of the Microsoft SQL Server that hosts the elastic database pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc929-121">-確認</span><span class="sxs-lookup"><span data-stu-id="fc929-121">-Confirm</span></span>
<span data-ttu-id="fc929-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fc929-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc929-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc929-123">-WhatIf</span></span>
<span data-ttu-id="fc929-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc929-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc929-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc929-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc929-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc929-126">-DefaultProfile</span></span>
<span data-ttu-id="fc929-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc929-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc929-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc929-128">CommonParameters</span></span>
<span data-ttu-id="fc929-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc929-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc929-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc929-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc929-131">輸入</span><span class="sxs-lookup"><span data-stu-id="fc929-131">INPUTS</span></span>

## <span data-ttu-id="fc929-132">輸出</span><span class="sxs-lookup"><span data-stu-id="fc929-132">OUTPUTS</span></span>

### <span data-ttu-id="fc929-133">AzureSqlDatabaseActivityModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="fc929-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="fc929-134">筆記</span><span class="sxs-lookup"><span data-stu-id="fc929-134">NOTES</span></span>

## <span data-ttu-id="fc929-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc929-135">RELATED LINKS</span></span>

