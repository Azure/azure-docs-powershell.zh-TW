---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 258db8a7dc1d771b73ea4c4fa373b1861847b820
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625214"
---
# <span data-ttu-id="56343-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="56343-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="56343-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56343-102">SYNOPSIS</span></span>
<span data-ttu-id="56343-103">修改資料 Lake Analytics 帳戶的資料來源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="56343-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56343-104">句法</span><span class="sxs-lookup"><span data-stu-id="56343-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56343-105">說明</span><span class="sxs-lookup"><span data-stu-id="56343-105">DESCRIPTION</span></span>
<span data-ttu-id="56343-106">**AzureRmDataLakeAnalyticsDataSource** Cmdlet 會修改 Azure Data Lake Analytics 帳戶的資料來源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="56343-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="56343-107">示例</span><span class="sxs-lookup"><span data-stu-id="56343-107">EXAMPLES</span></span>

### <span data-ttu-id="56343-108">範例1：變更資料來源的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="56343-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="56343-109">這個命令會變更針對 Azure Blob 儲存資料來源所儲存的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="56343-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="56343-110">參數</span><span class="sxs-lookup"><span data-stu-id="56343-110">PARAMETERS</span></span>

### <span data-ttu-id="56343-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="56343-111">-AccessKey</span></span>
<span data-ttu-id="56343-112">指定 Azure Blob 儲存資料來源的新便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="56343-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="56343-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="56343-113">-Account</span></span>
<span data-ttu-id="56343-114">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="56343-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="56343-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="56343-115">-Blob</span></span>
<span data-ttu-id="56343-116">指定 Azure Blob 儲存資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="56343-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="56343-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56343-117">-ResourceGroupName</span></span>
<span data-ttu-id="56343-118">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="56343-118">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="56343-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56343-119">-DefaultProfile</span></span>
<span data-ttu-id="56343-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="56343-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56343-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56343-121">CommonParameters</span></span>
<span data-ttu-id="56343-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56343-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56343-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="56343-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56343-124">輸入</span><span class="sxs-lookup"><span data-stu-id="56343-124">INPUTS</span></span>

## <span data-ttu-id="56343-125">輸出</span><span class="sxs-lookup"><span data-stu-id="56343-125">OUTPUTS</span></span>

### <span data-ttu-id="56343-126">所有</span><span class="sxs-lookup"><span data-stu-id="56343-126">None</span></span>

## <span data-ttu-id="56343-127">筆記</span><span class="sxs-lookup"><span data-stu-id="56343-127">NOTES</span></span>

## <span data-ttu-id="56343-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="56343-128">RELATED LINKS</span></span>

[<span data-ttu-id="56343-129">附加 AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="56343-129">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="56343-130">移除-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="56343-130">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


