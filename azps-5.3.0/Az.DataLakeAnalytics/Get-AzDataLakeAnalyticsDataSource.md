---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: e14e4c1b58b24cb8065681ae806789cd1252a0db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439375"
---
# <span data-ttu-id="8cfbe-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="8cfbe-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="8cfbe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8cfbe-102">SYNOPSIS</span></span>
<span data-ttu-id="8cfbe-103">取得資料 Lake Analytics 資料來源。</span><span class="sxs-lookup"><span data-stu-id="8cfbe-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="8cfbe-104">句法</span><span class="sxs-lookup"><span data-stu-id="8cfbe-104">SYNTAX</span></span>

### <span data-ttu-id="8cfbe-105">GetAllDataSources (預設) </span><span class="sxs-lookup"><span data-stu-id="8cfbe-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cfbe-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8cfbe-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cfbe-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8cfbe-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cfbe-108">說明</span><span class="sxs-lookup"><span data-stu-id="8cfbe-108">DESCRIPTION</span></span>
<span data-ttu-id="8cfbe-109">**AzDataLakeAnalyticsDataSource** Cmdlet 會取得 Azure Data Lake Analytics 資料來源。</span><span class="sxs-lookup"><span data-stu-id="8cfbe-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="8cfbe-110">示例</span><span class="sxs-lookup"><span data-stu-id="8cfbe-110">EXAMPLES</span></span>

### <span data-ttu-id="8cfbe-111">範例1：從帳戶取得資料來源</span><span class="sxs-lookup"><span data-stu-id="8cfbe-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="8cfbe-112">這個命令會從資料 Lake Analytics 帳戶取得名為 ContosoAdls 的 Data Lake Store 資料來源。</span><span class="sxs-lookup"><span data-stu-id="8cfbe-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="8cfbe-113">範例2：在 Data Lake Analytics 帳戶中取得資料 Lake Store 帳戶清單</span><span class="sxs-lookup"><span data-stu-id="8cfbe-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="8cfbe-114">這個命令會從資料 Lake Analytics 帳戶取得所有資料 Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="8cfbe-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="8cfbe-115">參數</span><span class="sxs-lookup"><span data-stu-id="8cfbe-115">PARAMETERS</span></span>

### <span data-ttu-id="8cfbe-116">-帳戶</span><span class="sxs-lookup"><span data-stu-id="8cfbe-116">-Account</span></span>
<span data-ttu-id="8cfbe-117">指定此 Cmdlet 取得資料來源的資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="8cfbe-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="8cfbe-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="8cfbe-118">-Blob</span></span>
<span data-ttu-id="8cfbe-119">指定 Azure Blob 儲存資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8cfbe-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cfbe-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8cfbe-120">-DataLakeStore</span></span>
<span data-ttu-id="8cfbe-121">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="8cfbe-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDataLakeStoreAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cfbe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cfbe-122">-DefaultProfile</span></span>
<span data-ttu-id="8cfbe-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8cfbe-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cfbe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cfbe-124">-ResourceGroupName</span></span>
<span data-ttu-id="8cfbe-125">指定包含資料來源的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8cfbe-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="8cfbe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cfbe-126">CommonParameters</span></span>
<span data-ttu-id="8cfbe-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8cfbe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cfbe-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8cfbe-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cfbe-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8cfbe-129">INPUTS</span></span>

### <span data-ttu-id="8cfbe-130">System.object</span><span class="sxs-lookup"><span data-stu-id="8cfbe-130">System.String</span></span>

## <span data-ttu-id="8cfbe-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8cfbe-131">OUTPUTS</span></span>

### <span data-ttu-id="8cfbe-132">PSStorageAccountInfo 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="8cfbe-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="8cfbe-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="8cfbe-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="8cfbe-134">AdlDataSource 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="8cfbe-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="8cfbe-135">筆記</span><span class="sxs-lookup"><span data-stu-id="8cfbe-135">NOTES</span></span>

## <span data-ttu-id="8cfbe-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="8cfbe-136">RELATED LINKS</span></span>

[<span data-ttu-id="8cfbe-137">附加 AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="8cfbe-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="8cfbe-138">移除-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="8cfbe-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="8cfbe-139">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="8cfbe-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


