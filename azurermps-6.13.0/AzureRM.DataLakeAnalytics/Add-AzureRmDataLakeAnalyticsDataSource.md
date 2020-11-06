---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/add-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 6c33492dcf6fd596c5d958851263275841fdbc9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447384"
---
# <span data-ttu-id="da757-101">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="da757-101">Add-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="da757-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da757-102">SYNOPSIS</span></span>
<span data-ttu-id="da757-103">將資料來源新增至 Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="da757-103">Adds a data source to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da757-104">句法</span><span class="sxs-lookup"><span data-stu-id="da757-104">SYNTAX</span></span>

### <span data-ttu-id="da757-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="da757-105">AddDataLakeStorageAccount</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da757-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="da757-106">AddBlobStorageAccount</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da757-107">說明</span><span class="sxs-lookup"><span data-stu-id="da757-107">DESCRIPTION</span></span>
<span data-ttu-id="da757-108">**載入 AzureRmDataLakeAnalyticsDataSource** Cmdlet 會將資料來源新增至 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="da757-108">The **Add-AzureRmDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="da757-109">示例</span><span class="sxs-lookup"><span data-stu-id="da757-109">EXAMPLES</span></span>

### <span data-ttu-id="da757-110">範例1：新增資料來源至帳戶</span><span class="sxs-lookup"><span data-stu-id="da757-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="da757-111">這個命令會將 Data Lake Store 資料來源新增到 Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="da757-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="da757-112">參數</span><span class="sxs-lookup"><span data-stu-id="da757-112">PARAMETERS</span></span>

### <span data-ttu-id="da757-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="da757-113">-AccessKey</span></span>
<span data-ttu-id="da757-114">指定要新增之 Azure Blob 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="da757-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da757-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="da757-115">-Account</span></span>
<span data-ttu-id="da757-116">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="da757-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="da757-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="da757-117">-Blob</span></span>
<span data-ttu-id="da757-118">指定要新增之 Azure Blob 儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="da757-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da757-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="da757-119">-DataLakeStore</span></span>
<span data-ttu-id="da757-120">指定要新增之 Azure Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="da757-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da757-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da757-121">-DefaultProfile</span></span>
<span data-ttu-id="da757-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="da757-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da757-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da757-123">-ResourceGroupName</span></span>
<span data-ttu-id="da757-124">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="da757-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da757-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da757-125">CommonParameters</span></span>
<span data-ttu-id="da757-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da757-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da757-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="da757-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da757-128">輸入</span><span class="sxs-lookup"><span data-stu-id="da757-128">INPUTS</span></span>

### <span data-ttu-id="da757-129">System.object</span><span class="sxs-lookup"><span data-stu-id="da757-129">System.String</span></span>

## <span data-ttu-id="da757-130">輸出</span><span class="sxs-lookup"><span data-stu-id="da757-130">OUTPUTS</span></span>

### <span data-ttu-id="da757-131">System.object</span><span class="sxs-lookup"><span data-stu-id="da757-131">System.Object</span></span>

## <span data-ttu-id="da757-132">筆記</span><span class="sxs-lookup"><span data-stu-id="da757-132">NOTES</span></span>

## <span data-ttu-id="da757-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="da757-133">RELATED LINKS</span></span>

[<span data-ttu-id="da757-134">移除-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="da757-134">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="da757-135">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="da757-135">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


