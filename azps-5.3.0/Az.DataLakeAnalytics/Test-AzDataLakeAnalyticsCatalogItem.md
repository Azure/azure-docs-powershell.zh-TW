---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439360"
---
# <span data-ttu-id="2be7c-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="2be7c-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="2be7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2be7c-102">SYNOPSIS</span></span>
<span data-ttu-id="2be7c-103">檢查是否存在目錄專案。</span><span class="sxs-lookup"><span data-stu-id="2be7c-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="2be7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2be7c-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2be7c-105">說明</span><span class="sxs-lookup"><span data-stu-id="2be7c-105">DESCRIPTION</span></span>
<span data-ttu-id="2be7c-106">**Test AzDataLakeAnalyticsCatalogItem** Cmdlet 會檢查 Azure Data Lake Analytics 目錄專案是否存在。</span><span class="sxs-lookup"><span data-stu-id="2be7c-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="2be7c-107">示例</span><span class="sxs-lookup"><span data-stu-id="2be7c-107">EXAMPLES</span></span>

### <span data-ttu-id="2be7c-108">範例1：測試目錄專案是否存在</span><span class="sxs-lookup"><span data-stu-id="2be7c-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="2be7c-109">這個命令會測試指定的架構專案是否存在。</span><span class="sxs-lookup"><span data-stu-id="2be7c-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="2be7c-110">參數</span><span class="sxs-lookup"><span data-stu-id="2be7c-110">PARAMETERS</span></span>

### <span data-ttu-id="2be7c-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="2be7c-111">-Account</span></span>
<span data-ttu-id="2be7c-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2be7c-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="2be7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be7c-113">-DefaultProfile</span></span>
<span data-ttu-id="2be7c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2be7c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2be7c-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="2be7c-115">-ItemType</span></span>
<span data-ttu-id="2be7c-116">指定要檢查之專案的目錄專案類型。</span><span class="sxs-lookup"><span data-stu-id="2be7c-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="2be7c-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2be7c-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2be7c-118">資料</span><span class="sxs-lookup"><span data-stu-id="2be7c-118">Database</span></span>
- <span data-ttu-id="2be7c-119">構架</span><span class="sxs-lookup"><span data-stu-id="2be7c-119">Schema</span></span>
- <span data-ttu-id="2be7c-120">元件</span><span class="sxs-lookup"><span data-stu-id="2be7c-120">Assembly</span></span>
- <span data-ttu-id="2be7c-121">張</span><span class="sxs-lookup"><span data-stu-id="2be7c-121">Table</span></span>
- <span data-ttu-id="2be7c-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="2be7c-122">TablePartition</span></span>
- <span data-ttu-id="2be7c-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="2be7c-123">TableValuedFunction</span></span>
- <span data-ttu-id="2be7c-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="2be7c-124">TableStatistics</span></span>
- <span data-ttu-id="2be7c-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="2be7c-125">ExternalDataSource</span></span>
- <span data-ttu-id="2be7c-126">視圖</span><span class="sxs-lookup"><span data-stu-id="2be7c-126">View</span></span>
- <span data-ttu-id="2be7c-127">過程</span><span class="sxs-lookup"><span data-stu-id="2be7c-127">Procedure</span></span>
- <span data-ttu-id="2be7c-128">秘訣</span><span class="sxs-lookup"><span data-stu-id="2be7c-128">Secret</span></span>
- <span data-ttu-id="2be7c-129">身份</span><span class="sxs-lookup"><span data-stu-id="2be7c-129">Credential</span></span>
- <span data-ttu-id="2be7c-130">類型</span><span class="sxs-lookup"><span data-stu-id="2be7c-130">Types</span></span>

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

### <span data-ttu-id="2be7c-131">-Path</span><span class="sxs-lookup"><span data-stu-id="2be7c-131">-Path</span></span>
<span data-ttu-id="2be7c-132">指定要取得的專案路徑，或專案至清單的父專案路徑。</span><span class="sxs-lookup"><span data-stu-id="2be7c-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="2be7c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be7c-133">CommonParameters</span></span>
<span data-ttu-id="2be7c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2be7c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be7c-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2be7c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be7c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="2be7c-136">INPUTS</span></span>

### <span data-ttu-id="2be7c-137">System.object</span><span class="sxs-lookup"><span data-stu-id="2be7c-137">System.String</span></span>

### <span data-ttu-id="2be7c-138">DataLakeAnalyticsEnums + CatalogItemType （DataLakeAnalytics）。</span><span class="sxs-lookup"><span data-stu-id="2be7c-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="2be7c-139">CatalogPathInstance 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="2be7c-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="2be7c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="2be7c-140">OUTPUTS</span></span>

### <span data-ttu-id="2be7c-141">System.object</span><span class="sxs-lookup"><span data-stu-id="2be7c-141">System.Boolean</span></span>

## <span data-ttu-id="2be7c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="2be7c-142">NOTES</span></span>

## <span data-ttu-id="2be7c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="2be7c-143">RELATED LINKS</span></span>

[<span data-ttu-id="2be7c-144">AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="2be7c-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


