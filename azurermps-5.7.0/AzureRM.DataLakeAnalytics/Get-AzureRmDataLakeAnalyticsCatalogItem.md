---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b7a608e4bed6e68f06660f10f2ef72effb6ad18b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623986"
---
# <span data-ttu-id="93b67-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="93b67-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="93b67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93b67-102">SYNOPSIS</span></span>
<span data-ttu-id="93b67-103">取得資料 Lake Analytics 目錄專案或專案類型。</span><span class="sxs-lookup"><span data-stu-id="93b67-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93b67-104">句法</span><span class="sxs-lookup"><span data-stu-id="93b67-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93b67-105">說明</span><span class="sxs-lookup"><span data-stu-id="93b67-105">DESCRIPTION</span></span>
<span data-ttu-id="93b67-106">**AzureRmDataLakeAnalyticsCatalogItem** 會取得指定的 Azure Data Lake Analytics 目錄專案，或取得指定類型的目錄專案。</span><span class="sxs-lookup"><span data-stu-id="93b67-106">The **Get-AzureRmDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="93b67-107">示例</span><span class="sxs-lookup"><span data-stu-id="93b67-107">EXAMPLES</span></span>

### <span data-ttu-id="93b67-108">範例1：取得指定的資料庫</span><span class="sxs-lookup"><span data-stu-id="93b67-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="93b67-109">這個命令會取得指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="93b67-109">This command gets the specified database.</span></span>

### <span data-ttu-id="93b67-110">範例2：在指定的資料庫和架構中取得表格</span><span class="sxs-lookup"><span data-stu-id="93b67-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="93b67-111">這個命令會取得指定資料庫中的資料表清單。</span><span class="sxs-lookup"><span data-stu-id="93b67-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="93b67-112">參數</span><span class="sxs-lookup"><span data-stu-id="93b67-112">PARAMETERS</span></span>

### <span data-ttu-id="93b67-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="93b67-113">-Account</span></span>
<span data-ttu-id="93b67-114">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="93b67-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93b67-115">-DefaultProfile</span></span>
<span data-ttu-id="93b67-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="93b67-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93b67-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="93b67-117">-ItemType</span></span>
<span data-ttu-id="93b67-118">指定 (s) 回遷或列出之專案的目錄專案類型。</span><span class="sxs-lookup"><span data-stu-id="93b67-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="93b67-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="93b67-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93b67-120">資料</span><span class="sxs-lookup"><span data-stu-id="93b67-120">Database</span></span>
- <span data-ttu-id="93b67-121">構架</span><span class="sxs-lookup"><span data-stu-id="93b67-121">Schema</span></span>
- <span data-ttu-id="93b67-122">元件</span><span class="sxs-lookup"><span data-stu-id="93b67-122">Assembly</span></span>
- <span data-ttu-id="93b67-123">張</span><span class="sxs-lookup"><span data-stu-id="93b67-123">Table</span></span>
- <span data-ttu-id="93b67-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="93b67-124">TableValuedFunction</span></span>
- <span data-ttu-id="93b67-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="93b67-125">TableStatistics</span></span>
- <span data-ttu-id="93b67-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="93b67-126">ExternalDataSource</span></span>
- <span data-ttu-id="93b67-127">視圖</span><span class="sxs-lookup"><span data-stu-id="93b67-127">View</span></span>
- <span data-ttu-id="93b67-128">過程</span><span class="sxs-lookup"><span data-stu-id="93b67-128">Procedure</span></span>
- <span data-ttu-id="93b67-129">秘訣</span><span class="sxs-lookup"><span data-stu-id="93b67-129">Secret</span></span>
- <span data-ttu-id="93b67-130">身份</span><span class="sxs-lookup"><span data-stu-id="93b67-130">Credential</span></span>
- <span data-ttu-id="93b67-131">類型</span><span class="sxs-lookup"><span data-stu-id="93b67-131">Types</span></span>
- <span data-ttu-id="93b67-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="93b67-132">TablePartition</span></span>

```yaml
Type: CatalogItemType
Parameter Sets: (All)
Aliases: 
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b67-133">-Path</span><span class="sxs-lookup"><span data-stu-id="93b67-133">-Path</span></span>
<span data-ttu-id="93b67-134">指定要檢索之專案的多部分路徑，或物件的父專案至清單。</span><span class="sxs-lookup"><span data-stu-id="93b67-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="93b67-135">路徑的各個部分應以句點 ( ) 。</span><span class="sxs-lookup"><span data-stu-id="93b67-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b67-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b67-136">CommonParameters</span></span>
<span data-ttu-id="93b67-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93b67-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b67-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="93b67-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b67-139">輸入</span><span class="sxs-lookup"><span data-stu-id="93b67-139">INPUTS</span></span>

### <span data-ttu-id="93b67-140">所有</span><span class="sxs-lookup"><span data-stu-id="93b67-140">None</span></span>
<span data-ttu-id="93b67-141">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="93b67-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93b67-142">輸出</span><span class="sxs-lookup"><span data-stu-id="93b67-142">OUTPUTS</span></span>

### <span data-ttu-id="93b67-143">CatalogItem</span><span class="sxs-lookup"><span data-stu-id="93b67-143">CatalogItem</span></span>
<span data-ttu-id="93b67-144">指定的目錄專案。</span><span class="sxs-lookup"><span data-stu-id="93b67-144">The specified catalog item.</span></span>

### <span data-ttu-id="93b67-145">清單<CatalogItem></span><span class="sxs-lookup"><span data-stu-id="93b67-145">List<CatalogItem></span></span>
<span data-ttu-id="93b67-146">指定的目錄專案在其對應容器下方的清單。</span><span class="sxs-lookup"><span data-stu-id="93b67-146">The list of the specified catalog items underneath their corresponding container.</span></span>

## <span data-ttu-id="93b67-147">筆記</span><span class="sxs-lookup"><span data-stu-id="93b67-147">NOTES</span></span>

## <span data-ttu-id="93b67-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="93b67-148">RELATED LINKS</span></span>

[<span data-ttu-id="93b67-149">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="93b67-149">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


