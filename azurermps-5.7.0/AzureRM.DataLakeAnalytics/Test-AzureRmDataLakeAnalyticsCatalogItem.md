---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: deb93fb17c2c739dcf377665f8b2f604a2fb4847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448691"
---
# <span data-ttu-id="4ced1-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="4ced1-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="4ced1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ced1-102">SYNOPSIS</span></span>
<span data-ttu-id="4ced1-103">檢查是否存在目錄專案。</span><span class="sxs-lookup"><span data-stu-id="4ced1-103">Checks for the existence of a catalog item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ced1-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ced1-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ced1-105">說明</span><span class="sxs-lookup"><span data-stu-id="4ced1-105">DESCRIPTION</span></span>
<span data-ttu-id="4ced1-106">**Test AzureRmDataLakeAnalyticsCatalogItem** Cmdlet 會檢查 Azure Data Lake Analytics 目錄專案是否存在。</span><span class="sxs-lookup"><span data-stu-id="4ced1-106">The **Test-AzureRmDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="4ced1-107">示例</span><span class="sxs-lookup"><span data-stu-id="4ced1-107">EXAMPLES</span></span>

### <span data-ttu-id="4ced1-108">範例1：測試目錄專案是否存在</span><span class="sxs-lookup"><span data-stu-id="4ced1-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="4ced1-109">這個命令會測試指定的架構專案是否存在。</span><span class="sxs-lookup"><span data-stu-id="4ced1-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="4ced1-110">參數</span><span class="sxs-lookup"><span data-stu-id="4ced1-110">PARAMETERS</span></span>

### <span data-ttu-id="4ced1-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="4ced1-111">-Account</span></span>
<span data-ttu-id="4ced1-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4ced1-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4ced1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ced1-113">-DefaultProfile</span></span>
<span data-ttu-id="4ced1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4ced1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ced1-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="4ced1-115">-ItemType</span></span>
<span data-ttu-id="4ced1-116">指定要檢查之專案的目錄專案類型。</span><span class="sxs-lookup"><span data-stu-id="4ced1-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="4ced1-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4ced1-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4ced1-118">資料</span><span class="sxs-lookup"><span data-stu-id="4ced1-118">Database</span></span>
- <span data-ttu-id="4ced1-119">構架</span><span class="sxs-lookup"><span data-stu-id="4ced1-119">Schema</span></span>
- <span data-ttu-id="4ced1-120">元件</span><span class="sxs-lookup"><span data-stu-id="4ced1-120">Assembly</span></span>
- <span data-ttu-id="4ced1-121">張</span><span class="sxs-lookup"><span data-stu-id="4ced1-121">Table</span></span>
- <span data-ttu-id="4ced1-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="4ced1-122">TablePartition</span></span>
- <span data-ttu-id="4ced1-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="4ced1-123">TableValuedFunction</span></span>
- <span data-ttu-id="4ced1-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="4ced1-124">TableStatistics</span></span>
- <span data-ttu-id="4ced1-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="4ced1-125">ExternalDataSource</span></span>
- <span data-ttu-id="4ced1-126">視圖</span><span class="sxs-lookup"><span data-stu-id="4ced1-126">View</span></span>
- <span data-ttu-id="4ced1-127">過程</span><span class="sxs-lookup"><span data-stu-id="4ced1-127">Procedure</span></span>
- <span data-ttu-id="4ced1-128">秘訣</span><span class="sxs-lookup"><span data-stu-id="4ced1-128">Secret</span></span>
- <span data-ttu-id="4ced1-129">身份</span><span class="sxs-lookup"><span data-stu-id="4ced1-129">Credential</span></span>
- <span data-ttu-id="4ced1-130">類型</span><span class="sxs-lookup"><span data-stu-id="4ced1-130">Types</span></span>

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

### <span data-ttu-id="4ced1-131">-Path</span><span class="sxs-lookup"><span data-stu-id="4ced1-131">-Path</span></span>
<span data-ttu-id="4ced1-132">指定要取得的專案路徑，或專案至清單的父專案路徑。</span><span class="sxs-lookup"><span data-stu-id="4ced1-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ced1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ced1-133">CommonParameters</span></span>
<span data-ttu-id="4ced1-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ced1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ced1-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ced1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ced1-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4ced1-136">INPUTS</span></span>

### <span data-ttu-id="4ced1-137">所有</span><span class="sxs-lookup"><span data-stu-id="4ced1-137">None</span></span>
<span data-ttu-id="4ced1-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4ced1-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ced1-139">輸出</span><span class="sxs-lookup"><span data-stu-id="4ced1-139">OUTPUTS</span></span>

### <span data-ttu-id="4ced1-140">bool</span><span class="sxs-lookup"><span data-stu-id="4ced1-140">bool</span></span>
<span data-ttu-id="4ced1-141">True 或 false，表示指定的目錄專案是否存在。</span><span class="sxs-lookup"><span data-stu-id="4ced1-141">True or false indicating if the specified catalog item exists or not.</span></span>

## <span data-ttu-id="4ced1-142">筆記</span><span class="sxs-lookup"><span data-stu-id="4ced1-142">NOTES</span></span>

## <span data-ttu-id="4ced1-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ced1-143">RELATED LINKS</span></span>

[<span data-ttu-id="4ced1-144">AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="4ced1-144">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Get-AzureRmDataLakeAnalyticsCatalogItem.md)


