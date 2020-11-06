---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
ms.openlocfilehash: e40510745ea7de39df4e15d0b1be7516d0fb33ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452683"
---
# <span data-ttu-id="7053c-101">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7053c-101">Get-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="7053c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7053c-102">SYNOPSIS</span></span>
<span data-ttu-id="7053c-103">在 Azure SQL 資料庫中取得彈性池及其屬性值。</span><span class="sxs-lookup"><span data-stu-id="7053c-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7053c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7053c-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7053c-105">說明</span><span class="sxs-lookup"><span data-stu-id="7053c-105">DESCRIPTION</span></span>
<span data-ttu-id="7053c-106">**AzureRmSqlElasticPool** Cmdlet 會取得彈性池及其屬性值。</span><span class="sxs-lookup"><span data-stu-id="7053c-106">The **Get-AzureRmSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="7053c-107">指定現有彈性池的名稱，只查看該池的屬性值。</span><span class="sxs-lookup"><span data-stu-id="7053c-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="7053c-108">示例</span><span class="sxs-lookup"><span data-stu-id="7053c-108">EXAMPLES</span></span>

### <span data-ttu-id="7053c-109">範例1：取得所有彈性池</span><span class="sxs-lookup"><span data-stu-id="7053c-109">Example 1: Get all elastic pools</span></span>
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

<span data-ttu-id="7053c-110">這個命令會取得伺服器上名為 Server01 的所有彈性池。</span><span class="sxs-lookup"><span data-stu-id="7053c-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="7053c-111">範例2：取得特定彈性池</span><span class="sxs-lookup"><span data-stu-id="7053c-111">Example 2: Get a specific elastic pool</span></span>
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

<span data-ttu-id="7053c-112">這個命令會在名為 Server01 的伺服器上取得名為 ElasticPool0127 的彈性池。</span><span class="sxs-lookup"><span data-stu-id="7053c-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="7053c-113">範例3：取得 Azure SQL 彈性資料庫池的度量單位</span><span class="sxs-lookup"><span data-stu-id="7053c-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
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

<span data-ttu-id="7053c-114">這個命令會傳回一個名為 ElasticPool01 的 Azure SQL 彈性資料庫池的指標。</span><span class="sxs-lookup"><span data-stu-id="7053c-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

## <span data-ttu-id="7053c-115">參數</span><span class="sxs-lookup"><span data-stu-id="7053c-115">PARAMETERS</span></span>

### <span data-ttu-id="7053c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7053c-116">-DefaultProfile</span></span>
<span data-ttu-id="7053c-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7053c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7053c-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7053c-118">-ElasticPoolName</span></span>
<span data-ttu-id="7053c-119">指定此 Cmdlet 取得之彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="7053c-119">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7053c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7053c-120">-ResourceGroupName</span></span>
<span data-ttu-id="7053c-121">指定包含此 Cmdlet 所取得彈性池之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7053c-121">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7053c-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7053c-122">-ServerName</span></span>
<span data-ttu-id="7053c-123">指定包含此 Cmdlet 所取得彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="7053c-123">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7053c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7053c-124">CommonParameters</span></span>
<span data-ttu-id="7053c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7053c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7053c-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7053c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7053c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="7053c-127">INPUTS</span></span>

### <span data-ttu-id="7053c-128">System.object</span><span class="sxs-lookup"><span data-stu-id="7053c-128">System.String</span></span>

## <span data-ttu-id="7053c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="7053c-129">OUTPUTS</span></span>

### <span data-ttu-id="7053c-130">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="7053c-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="7053c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="7053c-131">NOTES</span></span>

## <span data-ttu-id="7053c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="7053c-132">RELATED LINKS</span></span>

[<span data-ttu-id="7053c-133">新-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7053c-133">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="7053c-134">移除-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7053c-134">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="7053c-135">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7053c-135">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

