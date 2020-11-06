---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 93e64c4a64eecbe66fc3f9b2923ade65405a05a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444572"
---
# <span data-ttu-id="3bc1c-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="3bc1c-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="3bc1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3bc1c-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc1c-103">取得資料 Lake Analytics 資料來源。</span><span class="sxs-lookup"><span data-stu-id="3bc1c-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bc1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3bc1c-104">SYNTAX</span></span>

### <span data-ttu-id="3bc1c-105">GetAllDataSources (預設) </span><span class="sxs-lookup"><span data-stu-id="3bc1c-105">GetAllDataSources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc1c-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3bc1c-106">GetDataLakeStoreAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc1c-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3bc1c-107">GetBlobStorageAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bc1c-108">說明</span><span class="sxs-lookup"><span data-stu-id="3bc1c-108">DESCRIPTION</span></span>
<span data-ttu-id="3bc1c-109">**AzureRmDataLakeAnalyticsDataSource** Cmdlet 會取得 Azure Data Lake Analytics 資料來源。</span><span class="sxs-lookup"><span data-stu-id="3bc1c-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="3bc1c-110">示例</span><span class="sxs-lookup"><span data-stu-id="3bc1c-110">EXAMPLES</span></span>

### <span data-ttu-id="3bc1c-111">範例1：從帳戶取得資料來源</span><span class="sxs-lookup"><span data-stu-id="3bc1c-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="3bc1c-112">這個命令會從資料 Lake Analytics 帳戶取得名為 ContosoAdls 的 Data Lake Store 資料來源。</span><span class="sxs-lookup"><span data-stu-id="3bc1c-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="3bc1c-113">範例2：在 Data Lake Analytics 帳戶中取得資料 Lake Store 帳戶清單</span><span class="sxs-lookup"><span data-stu-id="3bc1c-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="3bc1c-114">這個命令會從資料 Lake Analytics 帳戶取得所有資料 Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="3bc1c-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="3bc1c-115">參數</span><span class="sxs-lookup"><span data-stu-id="3bc1c-115">PARAMETERS</span></span>

### <span data-ttu-id="3bc1c-116">-帳戶</span><span class="sxs-lookup"><span data-stu-id="3bc1c-116">-Account</span></span>
<span data-ttu-id="3bc1c-117">指定此 Cmdlet 取得資料來源的資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="3bc1c-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="3bc1c-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="3bc1c-118">-Blob</span></span>
<span data-ttu-id="3bc1c-119">指定 Azure Blob 儲存資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bc1c-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc1c-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3bc1c-120">-DataLakeStore</span></span>
<span data-ttu-id="3bc1c-121">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bc1c-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: GetDataLakeStoreAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc1c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc1c-122">-DefaultProfile</span></span>
<span data-ttu-id="3bc1c-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3bc1c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3bc1c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc1c-124">-ResourceGroupName</span></span>
<span data-ttu-id="3bc1c-125">指定包含資料來源的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3bc1c-125">Specifies the resource group name that contains the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc1c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc1c-126">CommonParameters</span></span>
<span data-ttu-id="3bc1c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3bc1c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc1c-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3bc1c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc1c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3bc1c-129">INPUTS</span></span>

### <span data-ttu-id="3bc1c-130">所有</span><span class="sxs-lookup"><span data-stu-id="3bc1c-130">None</span></span>
<span data-ttu-id="3bc1c-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3bc1c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3bc1c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="3bc1c-132">OUTPUTS</span></span>

### <span data-ttu-id="3bc1c-133">PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="3bc1c-133">PSStorageAccountInfo</span></span>
<span data-ttu-id="3bc1c-134">指定的 Azure 儲存空間帳戶詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3bc1c-134">The specified Azure Storage account details.</span></span>

### <span data-ttu-id="3bc1c-135">PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="3bc1c-135">PSDataLakeStoreAccountInfo</span></span>
<span data-ttu-id="3bc1c-136">指定的資料 Lake Store 帳戶詳細資料</span><span class="sxs-lookup"><span data-stu-id="3bc1c-136">The specified Data Lake Store account details</span></span>

### <span data-ttu-id="3bc1c-137">清單<AdlDataSource></span><span class="sxs-lookup"><span data-stu-id="3bc1c-137">List<AdlDataSource></span></span>
<span data-ttu-id="3bc1c-138">指定資料 Lake Analytics 帳戶中的 Azure 儲存空間帳戶和 Data Lake Store 帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="3bc1c-138">The list of both Azure Storage accounts and Data Lake Store accounts in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="3bc1c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="3bc1c-139">NOTES</span></span>

## <span data-ttu-id="3bc1c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bc1c-140">RELATED LINKS</span></span>

[<span data-ttu-id="3bc1c-141">附加 AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="3bc1c-141">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="3bc1c-142">移除-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="3bc1c-142">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="3bc1c-143">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="3bc1c-143">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


