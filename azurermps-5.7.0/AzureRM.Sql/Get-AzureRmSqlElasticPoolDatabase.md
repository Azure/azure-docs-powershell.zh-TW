---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: 3068b3a406414eb7302d76d5d053658dcf0e6245
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624277"
---
# <span data-ttu-id="220a3-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="220a3-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="220a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="220a3-102">SYNOPSIS</span></span>
<span data-ttu-id="220a3-103">在彈性池中取得彈性資料庫及其屬性值。</span><span class="sxs-lookup"><span data-stu-id="220a3-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="220a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="220a3-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="220a3-105">說明</span><span class="sxs-lookup"><span data-stu-id="220a3-105">DESCRIPTION</span></span>
<span data-ttu-id="220a3-106">**AzureRmSqlElasticPoolDatabase** Cmdlet 會在彈性池中取得彈性資料庫及其屬性值。</span><span class="sxs-lookup"><span data-stu-id="220a3-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="220a3-107">您可以在 Azure SQL Database 中指定彈性資料庫的名稱，只查看該資料庫的屬性值。</span><span class="sxs-lookup"><span data-stu-id="220a3-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="220a3-108">示例</span><span class="sxs-lookup"><span data-stu-id="220a3-108">EXAMPLES</span></span>

### <span data-ttu-id="220a3-109">範例1：取得彈性池中的所有資料庫</span><span class="sxs-lookup"><span data-stu-id="220a3-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="220a3-110">這個命令會取得一個名為 ElasticPool01 的彈性池中的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="220a3-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="220a3-111">參數</span><span class="sxs-lookup"><span data-stu-id="220a3-111">PARAMETERS</span></span>

### <span data-ttu-id="220a3-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="220a3-112">-DatabaseName</span></span>
<span data-ttu-id="220a3-113">指定此 Cmdlet 所取得之 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="220a3-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="220a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="220a3-114">-DefaultProfile</span></span>
<span data-ttu-id="220a3-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="220a3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="220a3-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="220a3-116">-ElasticPoolName</span></span>
<span data-ttu-id="220a3-117">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="220a3-117">Specifies the name of an elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="220a3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="220a3-118">-ResourceGroupName</span></span>
<span data-ttu-id="220a3-119">指定將彈性池指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="220a3-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="220a3-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="220a3-120">-ServerName</span></span>
<span data-ttu-id="220a3-121">指定包含彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="220a3-121">Specifies the name of a server that contains an elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="220a3-122">-確認</span><span class="sxs-lookup"><span data-stu-id="220a3-122">-Confirm</span></span>
<span data-ttu-id="220a3-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="220a3-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220a3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="220a3-124">-WhatIf</span></span>
<span data-ttu-id="220a3-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="220a3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="220a3-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="220a3-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220a3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="220a3-127">CommonParameters</span></span>
<span data-ttu-id="220a3-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="220a3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="220a3-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="220a3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="220a3-130">輸入</span><span class="sxs-lookup"><span data-stu-id="220a3-130">INPUTS</span></span>

### <span data-ttu-id="220a3-131">所有</span><span class="sxs-lookup"><span data-stu-id="220a3-131">None</span></span>
<span data-ttu-id="220a3-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="220a3-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="220a3-133">輸出</span><span class="sxs-lookup"><span data-stu-id="220a3-133">OUTPUTS</span></span>

### <span data-ttu-id="220a3-134">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="220a3-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="220a3-135">筆記</span><span class="sxs-lookup"><span data-stu-id="220a3-135">NOTES</span></span>

## <span data-ttu-id="220a3-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="220a3-136">RELATED LINKS</span></span>

[<span data-ttu-id="220a3-137">AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="220a3-137">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="220a3-138">AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="220a3-138">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="220a3-139">新-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="220a3-139">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="220a3-140">移除-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="220a3-140">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="220a3-141">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="220a3-141">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)
