---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2642a310e2a318498b3d170b463ac7e366bf5818
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903257"
---
# <span data-ttu-id="a7e3f-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="a7e3f-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="a7e3f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a7e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e3f-103">檢查目錄專案是否存在。</span><span class="sxs-lookup"><span data-stu-id="a7e3f-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="a7e3f-104">語法</span><span class="sxs-lookup"><span data-stu-id="a7e3f-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7e3f-105">描述</span><span class="sxs-lookup"><span data-stu-id="a7e3f-105">DESCRIPTION</span></span>
<span data-ttu-id="a7e3f-106">**Test-AzDataLakeAnalyticsCatalogItem** Cmdlet 會檢查 Azure Data Lake Analytics 目錄專案是否存在。</span><span class="sxs-lookup"><span data-stu-id="a7e3f-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="a7e3f-107">例子</span><span class="sxs-lookup"><span data-stu-id="a7e3f-107">EXAMPLES</span></span>

### <span data-ttu-id="a7e3f-108">範例 1：測試目錄專案是否存在</span><span class="sxs-lookup"><span data-stu-id="a7e3f-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="a7e3f-109">此命令會測試指定的架構專案是否存在。</span><span class="sxs-lookup"><span data-stu-id="a7e3f-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="a7e3f-110">參數</span><span class="sxs-lookup"><span data-stu-id="a7e3f-110">PARAMETERS</span></span>

### <span data-ttu-id="a7e3f-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a7e3f-111">-Account</span></span>
<span data-ttu-id="a7e3f-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a7e3f-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a7e3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e3f-113">-DefaultProfile</span></span>
<span data-ttu-id="a7e3f-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a7e3f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7e3f-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="a7e3f-115">-ItemType</span></span>
<span data-ttu-id="a7e3f-116">指定要檢查項目的型錄專案類型。</span><span class="sxs-lookup"><span data-stu-id="a7e3f-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="a7e3f-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a7e3f-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a7e3f-118">資料庫</span><span class="sxs-lookup"><span data-stu-id="a7e3f-118">Database</span></span>
- <span data-ttu-id="a7e3f-119">模式</span><span class="sxs-lookup"><span data-stu-id="a7e3f-119">Schema</span></span>
- <span data-ttu-id="a7e3f-120">裝配</span><span class="sxs-lookup"><span data-stu-id="a7e3f-120">Assembly</span></span>
- <span data-ttu-id="a7e3f-121">表</span><span class="sxs-lookup"><span data-stu-id="a7e3f-121">Table</span></span>
- <span data-ttu-id="a7e3f-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="a7e3f-122">TablePartition</span></span>
- <span data-ttu-id="a7e3f-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="a7e3f-123">TableValuedFunction</span></span>
- <span data-ttu-id="a7e3f-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="a7e3f-124">TableStatistics</span></span>
- <span data-ttu-id="a7e3f-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="a7e3f-125">ExternalDataSource</span></span>
- <span data-ttu-id="a7e3f-126">視圖</span><span class="sxs-lookup"><span data-stu-id="a7e3f-126">View</span></span>
- <span data-ttu-id="a7e3f-127">程式</span><span class="sxs-lookup"><span data-stu-id="a7e3f-127">Procedure</span></span>
- <span data-ttu-id="a7e3f-128">秘密</span><span class="sxs-lookup"><span data-stu-id="a7e3f-128">Secret</span></span>
- <span data-ttu-id="a7e3f-129">憑據</span><span class="sxs-lookup"><span data-stu-id="a7e3f-129">Credential</span></span>
- <span data-ttu-id="a7e3f-130">類型</span><span class="sxs-lookup"><span data-stu-id="a7e3f-130">Types</span></span>

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

### <span data-ttu-id="a7e3f-131">-路徑</span><span class="sxs-lookup"><span data-stu-id="a7e3f-131">-Path</span></span>
<span data-ttu-id="a7e3f-132">指定要抓取之專案的路徑，或要列出之專案之父專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="a7e3f-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7e3f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e3f-133">CommonParameters</span></span>
<span data-ttu-id="a7e3f-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a7e3f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e3f-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a7e3f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e3f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a7e3f-136">INPUTS</span></span>

### <span data-ttu-id="a7e3f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a7e3f-137">System.String</span></span>

### <span data-ttu-id="a7e3f-138">Microsoft.Azure.Commands.DataLakeAnalytics.models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="a7e3f-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="a7e3f-139">Microsoft.Azure.Commands.DataLakeAnalytics.models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="a7e3f-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="a7e3f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a7e3f-140">OUTPUTS</span></span>

### <span data-ttu-id="a7e3f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a7e3f-141">System.Boolean</span></span>

## <span data-ttu-id="a7e3f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a7e3f-142">NOTES</span></span>

## <span data-ttu-id="a7e3f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7e3f-143">RELATED LINKS</span></span>

[<span data-ttu-id="a7e3f-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="a7e3f-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


