---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284304"
---
# <span data-ttu-id="562de-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="562de-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="562de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="562de-102">SYNOPSIS</span></span>
<span data-ttu-id="562de-103">取得資料 Lake Analytics 目錄專案或專案類型。</span><span class="sxs-lookup"><span data-stu-id="562de-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="562de-104">句法</span><span class="sxs-lookup"><span data-stu-id="562de-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="562de-105">說明</span><span class="sxs-lookup"><span data-stu-id="562de-105">DESCRIPTION</span></span>
<span data-ttu-id="562de-106">**AzDataLakeAnalyticsCatalogItem** 會取得指定的 Azure Data Lake Analytics 目錄專案，或取得指定類型的目錄專案。</span><span class="sxs-lookup"><span data-stu-id="562de-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="562de-107">示例</span><span class="sxs-lookup"><span data-stu-id="562de-107">EXAMPLES</span></span>

### <span data-ttu-id="562de-108">範例1：取得指定的資料庫</span><span class="sxs-lookup"><span data-stu-id="562de-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="562de-109">這個命令會取得指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="562de-109">This command gets the specified database.</span></span>

### <span data-ttu-id="562de-110">範例2：在指定的資料庫和架構中取得表格</span><span class="sxs-lookup"><span data-stu-id="562de-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="562de-111">這個命令會取得指定資料庫中的資料表清單。</span><span class="sxs-lookup"><span data-stu-id="562de-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="562de-112">參數</span><span class="sxs-lookup"><span data-stu-id="562de-112">PARAMETERS</span></span>

### <span data-ttu-id="562de-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="562de-113">-Account</span></span>
<span data-ttu-id="562de-114">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="562de-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="562de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="562de-115">-DefaultProfile</span></span>
<span data-ttu-id="562de-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="562de-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="562de-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="562de-117">-ItemType</span></span>
<span data-ttu-id="562de-118">指定 (s) 回遷或列出之專案的目錄專案類型。</span><span class="sxs-lookup"><span data-stu-id="562de-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="562de-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="562de-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="562de-120">資料</span><span class="sxs-lookup"><span data-stu-id="562de-120">Database</span></span>
- <span data-ttu-id="562de-121">構架</span><span class="sxs-lookup"><span data-stu-id="562de-121">Schema</span></span>
- <span data-ttu-id="562de-122">元件</span><span class="sxs-lookup"><span data-stu-id="562de-122">Assembly</span></span>
- <span data-ttu-id="562de-123">張</span><span class="sxs-lookup"><span data-stu-id="562de-123">Table</span></span>
- <span data-ttu-id="562de-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="562de-124">TableValuedFunction</span></span>
- <span data-ttu-id="562de-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="562de-125">TableStatistics</span></span>
- <span data-ttu-id="562de-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="562de-126">ExternalDataSource</span></span>
- <span data-ttu-id="562de-127">視圖</span><span class="sxs-lookup"><span data-stu-id="562de-127">View</span></span>
- <span data-ttu-id="562de-128">過程</span><span class="sxs-lookup"><span data-stu-id="562de-128">Procedure</span></span>
- <span data-ttu-id="562de-129">秘訣</span><span class="sxs-lookup"><span data-stu-id="562de-129">Secret</span></span>
- <span data-ttu-id="562de-130">身份</span><span class="sxs-lookup"><span data-stu-id="562de-130">Credential</span></span>
- <span data-ttu-id="562de-131">類型</span><span class="sxs-lookup"><span data-stu-id="562de-131">Types</span></span>
- <span data-ttu-id="562de-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="562de-132">TablePartition</span></span>

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

### <span data-ttu-id="562de-133">-Path</span><span class="sxs-lookup"><span data-stu-id="562de-133">-Path</span></span>
<span data-ttu-id="562de-134">指定要檢索之專案的多部分路徑，或物件的父專案至清單。</span><span class="sxs-lookup"><span data-stu-id="562de-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="562de-135">路徑的各個部分應以句點 ( ) 。</span><span class="sxs-lookup"><span data-stu-id="562de-135">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="562de-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="562de-136">CommonParameters</span></span>
<span data-ttu-id="562de-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="562de-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="562de-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="562de-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="562de-139">輸入</span><span class="sxs-lookup"><span data-stu-id="562de-139">INPUTS</span></span>

### <span data-ttu-id="562de-140">System.object</span><span class="sxs-lookup"><span data-stu-id="562de-140">System.String</span></span>

### <span data-ttu-id="562de-141">DataLakeAnalyticsEnums + CatalogItemType （DataLakeAnalytics）。</span><span class="sxs-lookup"><span data-stu-id="562de-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="562de-142">CatalogPathInstance 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="562de-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="562de-143">輸出</span><span class="sxs-lookup"><span data-stu-id="562de-143">OUTPUTS</span></span>

### <span data-ttu-id="562de-144">[DataLake. CatalogItem]。</span><span class="sxs-lookup"><span data-stu-id="562de-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="562de-145">筆記</span><span class="sxs-lookup"><span data-stu-id="562de-145">NOTES</span></span>

## <span data-ttu-id="562de-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="562de-146">RELATED LINKS</span></span>

[<span data-ttu-id="562de-147">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="562de-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


