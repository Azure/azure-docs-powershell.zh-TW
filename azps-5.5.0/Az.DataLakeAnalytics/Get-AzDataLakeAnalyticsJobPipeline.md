---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 1d13d1b6e55831c972457c5a6a5aadc427ecb3a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129479"
---
# <span data-ttu-id="abca0-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="abca0-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="abca0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="abca0-102">SYNOPSIS</span></span>
<span data-ttu-id="abca0-103">取得資料 Lake Analytics 作業管道或管線。</span><span class="sxs-lookup"><span data-stu-id="abca0-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="abca0-104">句法</span><span class="sxs-lookup"><span data-stu-id="abca0-104">SYNTAX</span></span>

### <span data-ttu-id="abca0-105">GetAllInAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="abca0-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abca0-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="abca0-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abca0-107">說明</span><span class="sxs-lookup"><span data-stu-id="abca0-107">DESCRIPTION</span></span>
<span data-ttu-id="abca0-108">**AzDataLakeAnalyticsJobPipeline** 會取得指定的 Azure Data Lake Analytics 作業管道或管線清單。</span><span class="sxs-lookup"><span data-stu-id="abca0-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="abca0-109">示例</span><span class="sxs-lookup"><span data-stu-id="abca0-109">EXAMPLES</span></span>

### <span data-ttu-id="abca0-110">範例1：取得指定的管線</span><span class="sxs-lookup"><span data-stu-id="abca0-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="abca0-111">此命令會取得帳戶 "contosoadla" 中 id 為 "83cb7ad2-3523-4b82-b909-d478b0d8aea3" 的指定管線。</span><span class="sxs-lookup"><span data-stu-id="abca0-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="abca0-112">範例2：取得帳戶中所有管線的清單</span><span class="sxs-lookup"><span data-stu-id="abca0-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="abca0-113">這個命令會取得帳戶 "contosoadla" 中所有管線的清單</span><span class="sxs-lookup"><span data-stu-id="abca0-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="abca0-114">參數</span><span class="sxs-lookup"><span data-stu-id="abca0-114">PARAMETERS</span></span>

### <span data-ttu-id="abca0-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="abca0-115">-Account</span></span>
<span data-ttu-id="abca0-116">要在其中檢索作業管線的資料 Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="abca0-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="abca0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abca0-117">-DefaultProfile</span></span>
<span data-ttu-id="abca0-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="abca0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abca0-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="abca0-119">-PipelineId</span></span>
<span data-ttu-id="abca0-120">要傳回信息之特定作業管線的識別碼。</span><span class="sxs-lookup"><span data-stu-id="abca0-120">ID of the specific job pipeline to return information for.</span></span>

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

### <span data-ttu-id="abca0-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="abca0-121">-SubmittedAfter</span></span>
<span data-ttu-id="abca0-122">會傳回作業管道 (s 的選用篩選，只) 在指定的時間之後提交。</span><span class="sxs-lookup"><span data-stu-id="abca0-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="abca0-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="abca0-123">-SubmittedBefore</span></span>
<span data-ttu-id="abca0-124">會傳回作業管線 (s 的選用篩選，) 只會在指定的時間前提交。</span><span class="sxs-lookup"><span data-stu-id="abca0-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="abca0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abca0-125">CommonParameters</span></span>
<span data-ttu-id="abca0-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="abca0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abca0-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="abca0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abca0-128">輸入</span><span class="sxs-lookup"><span data-stu-id="abca0-128">INPUTS</span></span>

### <span data-ttu-id="abca0-129">System.object</span><span class="sxs-lookup"><span data-stu-id="abca0-129">System.String</span></span>

### <span data-ttu-id="abca0-130">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="abca0-130">System.Guid</span></span>

### <span data-ttu-id="abca0-131">"CoreLib" 1 [（System.object，System.object，，版本 = 4.0.0.0，Culture = 中立，</span><span class="sxs-lookup"><span data-stu-id="abca0-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="abca0-132">輸出</span><span class="sxs-lookup"><span data-stu-id="abca0-132">OUTPUTS</span></span>

### <span data-ttu-id="abca0-133">PSJobPipelineInformation 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="abca0-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="abca0-134">筆記</span><span class="sxs-lookup"><span data-stu-id="abca0-134">NOTES</span></span>

## <span data-ttu-id="abca0-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="abca0-135">RELATED LINKS</span></span>
