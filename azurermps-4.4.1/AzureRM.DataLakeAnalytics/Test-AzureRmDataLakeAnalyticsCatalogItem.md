---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 249ef7ae66436d4bf82b3b038aa8b1201f68110e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624569"
---
# <span data-ttu-id="b796d-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="b796d-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="b796d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b796d-102">SYNOPSIS</span></span>
<span data-ttu-id="b796d-103">檢查是否存在目錄專案。</span><span class="sxs-lookup"><span data-stu-id="b796d-103">Checks for the existence of a catalog item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b796d-104">句法</span><span class="sxs-lookup"><span data-stu-id="b796d-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b796d-105">說明</span><span class="sxs-lookup"><span data-stu-id="b796d-105">DESCRIPTION</span></span>
<span data-ttu-id="b796d-106">**Test AzureRmDataLakeAnalyticsCatalogItem** Cmdlet 會檢查 Azure Data Lake Analytics 目錄專案是否存在。</span><span class="sxs-lookup"><span data-stu-id="b796d-106">The **Test-AzureRmDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="b796d-107">示例</span><span class="sxs-lookup"><span data-stu-id="b796d-107">EXAMPLES</span></span>

### <span data-ttu-id="b796d-108">範例1：測試目錄專案是否存在</span><span class="sxs-lookup"><span data-stu-id="b796d-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="b796d-109">這個命令會測試指定的架構專案是否存在。</span><span class="sxs-lookup"><span data-stu-id="b796d-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="b796d-110">參數</span><span class="sxs-lookup"><span data-stu-id="b796d-110">PARAMETERS</span></span>

### <span data-ttu-id="b796d-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="b796d-111">-Account</span></span>
<span data-ttu-id="b796d-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b796d-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="b796d-113">-ItemType</span><span class="sxs-lookup"><span data-stu-id="b796d-113">-ItemType</span></span>
<span data-ttu-id="b796d-114">指定要檢查之專案的目錄專案類型。</span><span class="sxs-lookup"><span data-stu-id="b796d-114">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="b796d-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b796d-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b796d-116">資料</span><span class="sxs-lookup"><span data-stu-id="b796d-116">Database</span></span>
- <span data-ttu-id="b796d-117">構架</span><span class="sxs-lookup"><span data-stu-id="b796d-117">Schema</span></span>
- <span data-ttu-id="b796d-118">元件</span><span class="sxs-lookup"><span data-stu-id="b796d-118">Assembly</span></span>
- <span data-ttu-id="b796d-119">張</span><span class="sxs-lookup"><span data-stu-id="b796d-119">Table</span></span>
- <span data-ttu-id="b796d-120">TablePartition</span><span class="sxs-lookup"><span data-stu-id="b796d-120">TablePartition</span></span>
- <span data-ttu-id="b796d-121">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="b796d-121">TableValuedFunction</span></span>
- <span data-ttu-id="b796d-122">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="b796d-122">TableStatistics</span></span>
- <span data-ttu-id="b796d-123">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="b796d-123">ExternalDataSource</span></span>
- <span data-ttu-id="b796d-124">視圖</span><span class="sxs-lookup"><span data-stu-id="b796d-124">View</span></span>
- <span data-ttu-id="b796d-125">過程</span><span class="sxs-lookup"><span data-stu-id="b796d-125">Procedure</span></span>
- <span data-ttu-id="b796d-126">秘訣</span><span class="sxs-lookup"><span data-stu-id="b796d-126">Secret</span></span>
- <span data-ttu-id="b796d-127">身份</span><span class="sxs-lookup"><span data-stu-id="b796d-127">Credential</span></span>
- <span data-ttu-id="b796d-128">類型</span><span class="sxs-lookup"><span data-stu-id="b796d-128">Types</span></span>

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

### <span data-ttu-id="b796d-129">-Path</span><span class="sxs-lookup"><span data-stu-id="b796d-129">-Path</span></span>
<span data-ttu-id="b796d-130">指定要取得的專案路徑，或專案至清單的父專案路徑。</span><span class="sxs-lookup"><span data-stu-id="b796d-130">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="b796d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b796d-131">-DefaultProfile</span></span>
<span data-ttu-id="b796d-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b796d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b796d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b796d-133">CommonParameters</span></span>
<span data-ttu-id="b796d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b796d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b796d-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b796d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b796d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b796d-136">INPUTS</span></span>

## <span data-ttu-id="b796d-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b796d-137">OUTPUTS</span></span>

### <span data-ttu-id="b796d-138">bool</span><span class="sxs-lookup"><span data-stu-id="b796d-138">bool</span></span>
<span data-ttu-id="b796d-139">True 或 false，表示指定的目錄專案是否存在。</span><span class="sxs-lookup"><span data-stu-id="b796d-139">True or false indicating if the specified catalog item exists or not.</span></span>

## <span data-ttu-id="b796d-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b796d-140">NOTES</span></span>

## <span data-ttu-id="b796d-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b796d-141">RELATED LINKS</span></span>

[<span data-ttu-id="b796d-142">AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="b796d-142">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Get-AzureRmDataLakeAnalyticsCatalogItem.md)


