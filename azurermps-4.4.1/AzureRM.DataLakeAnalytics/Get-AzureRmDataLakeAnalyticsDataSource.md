---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: b7f2c6f2077d0b7e9c7510f6984ada15a65d6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626312"
---
# <span data-ttu-id="c5e97-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="c5e97-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="c5e97-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5e97-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e97-103">取得資料 Lake Analytics 資料來源。</span><span class="sxs-lookup"><span data-stu-id="c5e97-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5e97-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5e97-104">SYNTAX</span></span>

### <span data-ttu-id="c5e97-105">列出所有資料來源 (預設) </span><span class="sxs-lookup"><span data-stu-id="c5e97-105">List all data sources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5e97-106">取得資料 Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="c5e97-106">Get a Data Lake Store account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5e97-107">取得 Blob 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="c5e97-107">Get a Blob storage account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5e97-108">說明</span><span class="sxs-lookup"><span data-stu-id="c5e97-108">DESCRIPTION</span></span>
<span data-ttu-id="c5e97-109">**AzureRmDataLakeAnalyticsDataSource** Cmdlet 會取得 Azure Data Lake Analytics 資料來源。</span><span class="sxs-lookup"><span data-stu-id="c5e97-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="c5e97-110">示例</span><span class="sxs-lookup"><span data-stu-id="c5e97-110">EXAMPLES</span></span>

### <span data-ttu-id="c5e97-111">範例1：從帳戶取得資料來源</span><span class="sxs-lookup"><span data-stu-id="c5e97-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="c5e97-112">這個命令會從資料 Lake Analytics 帳戶取得名為 ContosoAdls 的 Data Lake Store 資料來源。</span><span class="sxs-lookup"><span data-stu-id="c5e97-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="c5e97-113">範例2：在 Data Lake Analytics 帳戶中取得資料 Lake Store 帳戶清單</span><span class="sxs-lookup"><span data-stu-id="c5e97-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="c5e97-114">這個命令會從資料 Lake Analytics 帳戶取得所有資料 Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="c5e97-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="c5e97-115">參數</span><span class="sxs-lookup"><span data-stu-id="c5e97-115">PARAMETERS</span></span>

### <span data-ttu-id="c5e97-116">-帳戶</span><span class="sxs-lookup"><span data-stu-id="c5e97-116">-Account</span></span>
<span data-ttu-id="c5e97-117">指定此 Cmdlet 取得資料來源的資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="c5e97-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="c5e97-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="c5e97-118">-Blob</span></span>
<span data-ttu-id="c5e97-119">指定 Azure Blob 儲存資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5e97-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e97-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c5e97-120">-DataLakeStore</span></span>
<span data-ttu-id="c5e97-121">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5e97-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Data Lake Store account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e97-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e97-122">-ResourceGroupName</span></span>
<span data-ttu-id="c5e97-123">指定包含資料來源的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c5e97-123">Specifies the resource group name that contains the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e97-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e97-124">-DefaultProfile</span></span>
<span data-ttu-id="c5e97-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5e97-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5e97-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e97-126">CommonParameters</span></span>
<span data-ttu-id="c5e97-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5e97-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e97-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c5e97-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e97-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c5e97-129">INPUTS</span></span>

## <span data-ttu-id="c5e97-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c5e97-130">OUTPUTS</span></span>

### <span data-ttu-id="c5e97-131">PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="c5e97-131">PSStorageAccountInfo</span></span>
<span data-ttu-id="c5e97-132">指定的 Azure 儲存空間帳戶詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c5e97-132">The specified Azure Storage account details.</span></span>

### <span data-ttu-id="c5e97-133">PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="c5e97-133">PSDataLakeStoreAccountInfo</span></span>
<span data-ttu-id="c5e97-134">指定的資料 Lake Store 帳戶詳細資料</span><span class="sxs-lookup"><span data-stu-id="c5e97-134">The specified Data Lake Store account details</span></span>

### <span data-ttu-id="c5e97-135">清單<AdlDataSource></span><span class="sxs-lookup"><span data-stu-id="c5e97-135">List<AdlDataSource></span></span>
<span data-ttu-id="c5e97-136">指定資料 Lake Analytics 帳戶中的 Azure 儲存空間帳戶和 Data Lake Store 帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="c5e97-136">The list of both Azure Storage accounts and Data Lake Store accounts in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="c5e97-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c5e97-137">NOTES</span></span>

## <span data-ttu-id="c5e97-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5e97-138">RELATED LINKS</span></span>

[<span data-ttu-id="c5e97-139">附加 AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="c5e97-139">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="c5e97-140">移除-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="c5e97-140">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="c5e97-141">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="c5e97-141">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


