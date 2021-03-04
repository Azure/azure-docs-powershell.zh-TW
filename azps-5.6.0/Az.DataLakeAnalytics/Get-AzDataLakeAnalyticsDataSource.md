---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 016c2520ee97f03c19a68eefebdc0319bacdb6e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916165"
---
# <span data-ttu-id="15dda-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="15dda-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="15dda-102">簡介</span><span class="sxs-lookup"><span data-stu-id="15dda-102">SYNOPSIS</span></span>
<span data-ttu-id="15dda-103">獲得 Data Lake Analytics 資料來源。</span><span class="sxs-lookup"><span data-stu-id="15dda-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="15dda-104">語法</span><span class="sxs-lookup"><span data-stu-id="15dda-104">SYNTAX</span></span>

### <span data-ttu-id="15dda-105">GetAllDataSources (預設) </span><span class="sxs-lookup"><span data-stu-id="15dda-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15dda-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="15dda-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15dda-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="15dda-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15dda-108">描述</span><span class="sxs-lookup"><span data-stu-id="15dda-108">DESCRIPTION</span></span>
<span data-ttu-id="15dda-109">**Get-AzDataLakeAnalyticsDataSource** Cmdlet 會取得 Azure Data Lake Analytics 資料來源。</span><span class="sxs-lookup"><span data-stu-id="15dda-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="15dda-110">例子</span><span class="sxs-lookup"><span data-stu-id="15dda-110">EXAMPLES</span></span>

### <span data-ttu-id="15dda-111">範例 1：從帳戶取得資料來源</span><span class="sxs-lookup"><span data-stu-id="15dda-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="15dda-112">此命令會從 Data Lake Analytics 帳戶獲得名為 ContosoAdls 的 Data Lake Store 資料來源。</span><span class="sxs-lookup"><span data-stu-id="15dda-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="15dda-113">範例 2：取得 Data Lake Analytics 帳戶中的 Data Lake Store 帳戶清單</span><span class="sxs-lookup"><span data-stu-id="15dda-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="15dda-114">此命令會從 Data Lake Analytics 帳戶獲得所有 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="15dda-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="15dda-115">參數</span><span class="sxs-lookup"><span data-stu-id="15dda-115">PARAMETERS</span></span>

### <span data-ttu-id="15dda-116">-帳戶</span><span class="sxs-lookup"><span data-stu-id="15dda-116">-Account</span></span>
<span data-ttu-id="15dda-117">指定此 Cmdlet 會獲得資料來源的 Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="15dda-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="15dda-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="15dda-118">-Blob</span></span>
<span data-ttu-id="15dda-119">指定 Azure Blob 儲存體資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="15dda-119">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="15dda-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="15dda-120">-DataLakeStore</span></span>
<span data-ttu-id="15dda-121">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="15dda-121">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="15dda-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15dda-122">-DefaultProfile</span></span>
<span data-ttu-id="15dda-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="15dda-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15dda-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15dda-124">-ResourceGroupName</span></span>
<span data-ttu-id="15dda-125">指定包含資料來源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="15dda-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="15dda-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15dda-126">CommonParameters</span></span>
<span data-ttu-id="15dda-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="15dda-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15dda-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="15dda-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15dda-129">輸入</span><span class="sxs-lookup"><span data-stu-id="15dda-129">INPUTS</span></span>

### <span data-ttu-id="15dda-130">System.String</span><span class="sxs-lookup"><span data-stu-id="15dda-130">System.String</span></span>

## <span data-ttu-id="15dda-131">輸出</span><span class="sxs-lookup"><span data-stu-id="15dda-131">OUTPUTS</span></span>

### <span data-ttu-id="15dda-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="15dda-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="15dda-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="15dda-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="15dda-134">Microsoft.Azure.Commands.DataLakeAnalytics.models.AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="15dda-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="15dda-135">筆記</span><span class="sxs-lookup"><span data-stu-id="15dda-135">NOTES</span></span>

## <span data-ttu-id="15dda-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="15dda-136">RELATED LINKS</span></span>

[<span data-ttu-id="15dda-137">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="15dda-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="15dda-138">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="15dda-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="15dda-139">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="15dda-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


