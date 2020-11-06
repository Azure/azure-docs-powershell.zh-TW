---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: c17a58cee2b5f13345997b97ce00792a8b9c9a0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453788"
---
# <span data-ttu-id="4a1a8-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="4a1a8-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="4a1a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a1a8-102">SYNOPSIS</span></span>
<span data-ttu-id="4a1a8-103">取得資料 Lake Analytics 作業管道或管線。</span><span class="sxs-lookup"><span data-stu-id="4a1a8-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a1a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a1a8-104">SYNTAX</span></span>

### <span data-ttu-id="4a1a8-105">GetAllInAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="4a1a8-105">GetAllInAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a1a8-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="4a1a8-106">GetBySpecificJobPipeline</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a1a8-107">說明</span><span class="sxs-lookup"><span data-stu-id="4a1a8-107">DESCRIPTION</span></span>
<span data-ttu-id="4a1a8-108">**AzureRmDataLakeAnalyticsJobPipeline** 會取得指定的 Azure Data Lake Analytics 作業管道或管線清單。</span><span class="sxs-lookup"><span data-stu-id="4a1a8-108">The **Get-AzureRmDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="4a1a8-109">示例</span><span class="sxs-lookup"><span data-stu-id="4a1a8-109">EXAMPLES</span></span>

### <span data-ttu-id="4a1a8-110">範例1：取得指定的管線</span><span class="sxs-lookup"><span data-stu-id="4a1a8-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="4a1a8-111">此命令會取得帳戶 "contosoadla" 中 id 為 "83cb7ad2-3523-4b82-b909-d478b0d8aea3" 的指定管線。</span><span class="sxs-lookup"><span data-stu-id="4a1a8-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="4a1a8-112">範例2：取得帳戶中所有管線的清單</span><span class="sxs-lookup"><span data-stu-id="4a1a8-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="4a1a8-113">這個命令會取得帳戶 "contosoadla" 中所有管線的清單</span><span class="sxs-lookup"><span data-stu-id="4a1a8-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="4a1a8-114">參數</span><span class="sxs-lookup"><span data-stu-id="4a1a8-114">PARAMETERS</span></span>

### <span data-ttu-id="4a1a8-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="4a1a8-115">-Account</span></span>
<span data-ttu-id="4a1a8-116">要在其中檢索作業管線的資料 Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4a1a8-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="4a1a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a1a8-117">-DefaultProfile</span></span>
<span data-ttu-id="4a1a8-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4a1a8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a1a8-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="4a1a8-119">-PipelineId</span></span>
<span data-ttu-id="4a1a8-120">要傳回信息之特定作業管線的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a1a8-120">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobPipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a1a8-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="4a1a8-121">-SubmittedAfter</span></span>
<span data-ttu-id="4a1a8-122">會傳回作業管道 (s 的選用篩選，只) 在指定的時間之後提交。</span><span class="sxs-lookup"><span data-stu-id="4a1a8-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a1a8-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="4a1a8-123">-SubmittedBefore</span></span>
<span data-ttu-id="4a1a8-124">會傳回作業管線 (s 的選用篩選，) 只會在指定的時間前提交。</span><span class="sxs-lookup"><span data-stu-id="4a1a8-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a1a8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a1a8-125">CommonParameters</span></span>
<span data-ttu-id="4a1a8-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a1a8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a1a8-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4a1a8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a1a8-128">輸入</span><span class="sxs-lookup"><span data-stu-id="4a1a8-128">INPUTS</span></span>

### <span data-ttu-id="4a1a8-129">System.object</span><span class="sxs-lookup"><span data-stu-id="4a1a8-129">System.String</span></span>

### <span data-ttu-id="4a1a8-130">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="4a1a8-130">System.Guid</span></span>

### <span data-ttu-id="4a1a8-131">System.object "1 [[System. DateTimeOffset，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4a1a8-131">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4a1a8-132">輸出</span><span class="sxs-lookup"><span data-stu-id="4a1a8-132">OUTPUTS</span></span>

### <span data-ttu-id="4a1a8-133">PSJobPipelineInformation 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="4a1a8-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="4a1a8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="4a1a8-134">NOTES</span></span>

## <span data-ttu-id="4a1a8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a1a8-135">RELATED LINKS</span></span>
