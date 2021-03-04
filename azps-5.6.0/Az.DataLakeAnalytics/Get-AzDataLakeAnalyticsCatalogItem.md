---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 738820c4c06fd32862def36ec76983968e99efb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914025"
---
# <span data-ttu-id="21ded-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="21ded-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="21ded-102">簡介</span><span class="sxs-lookup"><span data-stu-id="21ded-102">SYNOPSIS</span></span>
<span data-ttu-id="21ded-103">獲得 Data Lake Analytics 型錄專案或專案類型。</span><span class="sxs-lookup"><span data-stu-id="21ded-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="21ded-104">語法</span><span class="sxs-lookup"><span data-stu-id="21ded-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21ded-105">描述</span><span class="sxs-lookup"><span data-stu-id="21ded-105">DESCRIPTION</span></span>
<span data-ttu-id="21ded-106">**Get-AzDataLakeAnalyticsCatalogItem 會** 取得指定的 Azure Data Lake Analytics 型錄專案，或取得指定類型的目錄專案。</span><span class="sxs-lookup"><span data-stu-id="21ded-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="21ded-107">例子</span><span class="sxs-lookup"><span data-stu-id="21ded-107">EXAMPLES</span></span>

### <span data-ttu-id="21ded-108">範例 1：取得指定的資料庫</span><span class="sxs-lookup"><span data-stu-id="21ded-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="21ded-109">此命令會獲得指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="21ded-109">This command gets the specified database.</span></span>

### <span data-ttu-id="21ded-110">範例 2：取得指定資料庫和架構的資料表</span><span class="sxs-lookup"><span data-stu-id="21ded-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="21ded-111">此命令會獲得指定資料庫中的資料表清單。</span><span class="sxs-lookup"><span data-stu-id="21ded-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="21ded-112">參數</span><span class="sxs-lookup"><span data-stu-id="21ded-112">PARAMETERS</span></span>

### <span data-ttu-id="21ded-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="21ded-113">-Account</span></span>
<span data-ttu-id="21ded-114">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="21ded-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ded-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ded-115">-DefaultProfile</span></span>
<span data-ttu-id="21ded-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="21ded-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21ded-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="21ded-117">-ItemType</span></span>
<span data-ttu-id="21ded-118">指定要抓取或列出 (專案的) 專案類型。</span><span class="sxs-lookup"><span data-stu-id="21ded-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="21ded-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="21ded-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="21ded-120">資料庫</span><span class="sxs-lookup"><span data-stu-id="21ded-120">Database</span></span>
- <span data-ttu-id="21ded-121">模式</span><span class="sxs-lookup"><span data-stu-id="21ded-121">Schema</span></span>
- <span data-ttu-id="21ded-122">裝配</span><span class="sxs-lookup"><span data-stu-id="21ded-122">Assembly</span></span>
- <span data-ttu-id="21ded-123">表</span><span class="sxs-lookup"><span data-stu-id="21ded-123">Table</span></span>
- <span data-ttu-id="21ded-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="21ded-124">TableValuedFunction</span></span>
- <span data-ttu-id="21ded-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="21ded-125">TableStatistics</span></span>
- <span data-ttu-id="21ded-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="21ded-126">ExternalDataSource</span></span>
- <span data-ttu-id="21ded-127">視圖</span><span class="sxs-lookup"><span data-stu-id="21ded-127">View</span></span>
- <span data-ttu-id="21ded-128">程式</span><span class="sxs-lookup"><span data-stu-id="21ded-128">Procedure</span></span>
- <span data-ttu-id="21ded-129">秘密</span><span class="sxs-lookup"><span data-stu-id="21ded-129">Secret</span></span>
- <span data-ttu-id="21ded-130">憑據</span><span class="sxs-lookup"><span data-stu-id="21ded-130">Credential</span></span>
- <span data-ttu-id="21ded-131">類型</span><span class="sxs-lookup"><span data-stu-id="21ded-131">Types</span></span>
- <span data-ttu-id="21ded-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="21ded-132">TablePartition</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ded-133">-路徑</span><span class="sxs-lookup"><span data-stu-id="21ded-133">-Path</span></span>
<span data-ttu-id="21ded-134">指定要取回之專案或要清單之專案的父專案的多部分路徑。</span><span class="sxs-lookup"><span data-stu-id="21ded-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="21ded-135">路徑的各個部分應該以 (.) 分隔。</span><span class="sxs-lookup"><span data-stu-id="21ded-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ded-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ded-136">CommonParameters</span></span>
<span data-ttu-id="21ded-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="21ded-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ded-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="21ded-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ded-139">輸入</span><span class="sxs-lookup"><span data-stu-id="21ded-139">INPUTS</span></span>

### <span data-ttu-id="21ded-140">System.String</span><span class="sxs-lookup"><span data-stu-id="21ded-140">System.String</span></span>

### <span data-ttu-id="21ded-141">Microsoft.Azure.Commands.DataLakeAnalytics.models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="21ded-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="21ded-142">Microsoft.Azure.Commands.DataLakeAnalytics.models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="21ded-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="21ded-143">輸出</span><span class="sxs-lookup"><span data-stu-id="21ded-143">OUTPUTS</span></span>

### <span data-ttu-id="21ded-144">Microsoft.Azure.management.DataLake.Analytics.models.CatalogItem</span><span class="sxs-lookup"><span data-stu-id="21ded-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="21ded-145">筆記</span><span class="sxs-lookup"><span data-stu-id="21ded-145">NOTES</span></span>

## <span data-ttu-id="21ded-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="21ded-146">RELATED LINKS</span></span>

[<span data-ttu-id="21ded-147">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="21ded-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


