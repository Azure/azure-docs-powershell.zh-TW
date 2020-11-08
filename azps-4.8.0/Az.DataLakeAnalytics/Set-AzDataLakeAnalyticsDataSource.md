---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 0dd0dfb25959ed3a5753ae6bd19b0500d4742634
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136478"
---
# <span data-ttu-id="6a8a4-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6a8a4-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="6a8a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6a8a4-102">SYNOPSIS</span></span>
<span data-ttu-id="6a8a4-103">修改資料 Lake Analytics 帳戶的資料來源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6a8a4-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="6a8a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="6a8a4-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a8a4-105">說明</span><span class="sxs-lookup"><span data-stu-id="6a8a4-105">DESCRIPTION</span></span>
<span data-ttu-id="6a8a4-106">**AzDataLakeAnalyticsDataSource** Cmdlet 會修改 Azure Data Lake Analytics 帳戶的資料來源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6a8a4-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6a8a4-107">示例</span><span class="sxs-lookup"><span data-stu-id="6a8a4-107">EXAMPLES</span></span>

### <span data-ttu-id="6a8a4-108">範例1：變更資料來源的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="6a8a4-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="6a8a4-109">這個命令會變更針對 Azure Blob 儲存資料來源所儲存的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="6a8a4-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="6a8a4-110">參數</span><span class="sxs-lookup"><span data-stu-id="6a8a4-110">PARAMETERS</span></span>

### <span data-ttu-id="6a8a4-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="6a8a4-111">-AccessKey</span></span>
<span data-ttu-id="6a8a4-112">指定 Azure Blob 儲存資料來源的新便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="6a8a4-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a8a4-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="6a8a4-113">-Account</span></span>
<span data-ttu-id="6a8a4-114">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6a8a4-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="6a8a4-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="6a8a4-115">-Blob</span></span>
<span data-ttu-id="6a8a4-116">指定 Azure Blob 儲存資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a8a4-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a8a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a8a4-117">-DefaultProfile</span></span>
<span data-ttu-id="6a8a4-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6a8a4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a8a4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a8a4-119">-ResourceGroupName</span></span>
<span data-ttu-id="6a8a4-120">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6a8a4-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="6a8a4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a8a4-121">CommonParameters</span></span>
<span data-ttu-id="6a8a4-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6a8a4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a8a4-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6a8a4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a8a4-124">輸入</span><span class="sxs-lookup"><span data-stu-id="6a8a4-124">INPUTS</span></span>

### <span data-ttu-id="6a8a4-125">System.object</span><span class="sxs-lookup"><span data-stu-id="6a8a4-125">System.String</span></span>

## <span data-ttu-id="6a8a4-126">輸出</span><span class="sxs-lookup"><span data-stu-id="6a8a4-126">OUTPUTS</span></span>

### <span data-ttu-id="6a8a4-127">System.void</span><span class="sxs-lookup"><span data-stu-id="6a8a4-127">System.Void</span></span>

## <span data-ttu-id="6a8a4-128">筆記</span><span class="sxs-lookup"><span data-stu-id="6a8a4-128">NOTES</span></span>

## <span data-ttu-id="6a8a4-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a8a4-129">RELATED LINKS</span></span>

[<span data-ttu-id="6a8a4-130">附加 AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6a8a4-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="6a8a4-131">移除-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6a8a4-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

