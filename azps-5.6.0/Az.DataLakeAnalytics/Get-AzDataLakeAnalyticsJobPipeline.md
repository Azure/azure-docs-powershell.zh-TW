---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 9e925e1bd118a9ac5f676ee666cb945f22d1ffac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911130"
---
# <span data-ttu-id="e22d1-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="e22d1-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="e22d1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e22d1-102">SYNOPSIS</span></span>
<span data-ttu-id="e22d1-103">獲得 Data Lake Analytics Job 管道或管線。</span><span class="sxs-lookup"><span data-stu-id="e22d1-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="e22d1-104">語法</span><span class="sxs-lookup"><span data-stu-id="e22d1-104">SYNTAX</span></span>

### <span data-ttu-id="e22d1-105">GetAllInAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="e22d1-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e22d1-106">GetByS0ificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="e22d1-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e22d1-107">描述</span><span class="sxs-lookup"><span data-stu-id="e22d1-107">DESCRIPTION</span></span>
<span data-ttu-id="e22d1-108">**Get-AzDataLakeAnalyticsJobPipeline 會** 取得指定的 Azure Data Lake Analytics Job 管道或管線清單。</span><span class="sxs-lookup"><span data-stu-id="e22d1-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="e22d1-109">例子</span><span class="sxs-lookup"><span data-stu-id="e22d1-109">EXAMPLES</span></span>

### <span data-ttu-id="e22d1-110">範例 1：取得指定的管線</span><span class="sxs-lookup"><span data-stu-id="e22d1-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="e22d1-111">此命令會獲得在帳戶 'contocbdla'中具有 id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' 的指定管線。</span><span class="sxs-lookup"><span data-stu-id="e22d1-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="e22d1-112">範例 2：取得帳戶中所有管線的清單</span><span class="sxs-lookup"><span data-stu-id="e22d1-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="e22d1-113">此命令會獲得帳戶 "contola" 中所有管線的清單</span><span class="sxs-lookup"><span data-stu-id="e22d1-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="e22d1-114">參數</span><span class="sxs-lookup"><span data-stu-id="e22d1-114">PARAMETERS</span></span>

### <span data-ttu-id="e22d1-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e22d1-115">-Account</span></span>
<span data-ttu-id="e22d1-116">資料湖分析帳戶名稱的名稱，其下想要取回工作管道。</span><span class="sxs-lookup"><span data-stu-id="e22d1-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="e22d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e22d1-117">-DefaultProfile</span></span>
<span data-ttu-id="e22d1-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e22d1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e22d1-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="e22d1-119">-PipelineId</span></span>
<span data-ttu-id="e22d1-120">要退貨資訊的特定工作管道識別碼。</span><span class="sxs-lookup"><span data-stu-id="e22d1-120">ID of the specific job pipeline to return information for.</span></span>

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

### <span data-ttu-id="e22d1-121">-提交之後</span><span class="sxs-lookup"><span data-stu-id="e22d1-121">-SubmittedAfter</span></span>
<span data-ttu-id="e22d1-122">選擇性篩選，會 () 指定時間後提交的工作管道。</span><span class="sxs-lookup"><span data-stu-id="e22d1-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="e22d1-123">-提交Before</span><span class="sxs-lookup"><span data-stu-id="e22d1-123">-SubmittedBefore</span></span>
<span data-ttu-id="e22d1-124">選擇性篩選，可 () 特定時間之前提交的工作管道。</span><span class="sxs-lookup"><span data-stu-id="e22d1-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="e22d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e22d1-125">CommonParameters</span></span>
<span data-ttu-id="e22d1-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e22d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e22d1-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e22d1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e22d1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e22d1-128">INPUTS</span></span>

### <span data-ttu-id="e22d1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e22d1-129">System.String</span></span>

### <span data-ttu-id="e22d1-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e22d1-130">System.Guid</span></span>

### <span data-ttu-id="e22d1-131">System.Nullable'1[[System.DateTimeOffset， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e22d1-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e22d1-132">輸出</span><span class="sxs-lookup"><span data-stu-id="e22d1-132">OUTPUTS</span></span>

### <span data-ttu-id="e22d1-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="e22d1-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="e22d1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e22d1-134">NOTES</span></span>

## <span data-ttu-id="e22d1-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="e22d1-135">RELATED LINKS</span></span>
