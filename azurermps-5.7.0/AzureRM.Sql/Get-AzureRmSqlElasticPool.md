---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
ms.openlocfilehash: f06481984ef478a6bf3af51de1796855c265c2c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450457"
---
# <span data-ttu-id="fbfde-101">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fbfde-101">Get-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="fbfde-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fbfde-102">SYNOPSIS</span></span>
<span data-ttu-id="fbfde-103">在 Azure SQL 資料庫中取得彈性池及其屬性值。</span><span class="sxs-lookup"><span data-stu-id="fbfde-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbfde-104">句法</span><span class="sxs-lookup"><span data-stu-id="fbfde-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbfde-105">說明</span><span class="sxs-lookup"><span data-stu-id="fbfde-105">DESCRIPTION</span></span>
<span data-ttu-id="fbfde-106">**AzureRmSqlElasticPool** Cmdlet 會取得彈性池及其屬性值。</span><span class="sxs-lookup"><span data-stu-id="fbfde-106">The **Get-AzureRmSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="fbfde-107">指定現有彈性池的名稱，只查看該池的屬性值。</span><span class="sxs-lookup"><span data-stu-id="fbfde-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="fbfde-108">示例</span><span class="sxs-lookup"><span data-stu-id="fbfde-108">EXAMPLES</span></span>

### <span data-ttu-id="fbfde-109">範例1：取得所有彈性池</span><span class="sxs-lookup"><span data-stu-id="fbfde-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="fbfde-110">這個命令會取得伺服器上名為 Server01 的所有彈性池。</span><span class="sxs-lookup"><span data-stu-id="fbfde-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="fbfde-111">範例2：取得特定彈性池</span><span class="sxs-lookup"><span data-stu-id="fbfde-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="fbfde-112">這個命令會在名為 Server01 的伺服器上取得名為 ElasticPool0127 的彈性池。</span><span class="sxs-lookup"><span data-stu-id="fbfde-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="fbfde-113">範例3：取得 Azure SQL 彈性資料庫池的度量單位</span><span class="sxs-lookup"><span data-stu-id="fbfde-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-Metrics -TimeGrain 0:5:0
DimensionName  : 
DimensionValue : 
Name           : cpu_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : physical_data_read_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : log_write_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : dtu_consumption_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : storage_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent
```

<span data-ttu-id="fbfde-114">這個命令會傳回一個名為 ElasticPool01 的 Azure SQL 彈性資料庫池的指標。</span><span class="sxs-lookup"><span data-stu-id="fbfde-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

## <span data-ttu-id="fbfde-115">參數</span><span class="sxs-lookup"><span data-stu-id="fbfde-115">PARAMETERS</span></span>

### <span data-ttu-id="fbfde-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbfde-116">-DefaultProfile</span></span>
<span data-ttu-id="fbfde-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fbfde-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbfde-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fbfde-118">-ElasticPoolName</span></span>
<span data-ttu-id="fbfde-119">指定此 Cmdlet 取得之彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbfde-119">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbfde-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbfde-120">-ResourceGroupName</span></span>
<span data-ttu-id="fbfde-121">指定包含此 Cmdlet 所取得彈性池之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbfde-121">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fbfde-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fbfde-122">-ServerName</span></span>
<span data-ttu-id="fbfde-123">指定包含此 Cmdlet 所取得彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="fbfde-123">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fbfde-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbfde-124">CommonParameters</span></span>
<span data-ttu-id="fbfde-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fbfde-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbfde-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fbfde-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbfde-127">輸入</span><span class="sxs-lookup"><span data-stu-id="fbfde-127">INPUTS</span></span>

### <span data-ttu-id="fbfde-128">所有</span><span class="sxs-lookup"><span data-stu-id="fbfde-128">None</span></span>
<span data-ttu-id="fbfde-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="fbfde-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fbfde-130">輸出</span><span class="sxs-lookup"><span data-stu-id="fbfde-130">OUTPUTS</span></span>

### <span data-ttu-id="fbfde-131">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="fbfde-131">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="fbfde-132">筆記</span><span class="sxs-lookup"><span data-stu-id="fbfde-132">NOTES</span></span>

## <span data-ttu-id="fbfde-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="fbfde-133">RELATED LINKS</span></span>

[<span data-ttu-id="fbfde-134">新-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fbfde-134">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="fbfde-135">移除-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fbfde-135">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="fbfde-136">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fbfde-136">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


