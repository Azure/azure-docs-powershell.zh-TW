---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: 751fa50a6c29c826fe707852efa661b78d1b9c33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915521"
---
# <span data-ttu-id="d4368-101">Get-AzDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="d4368-101">Get-AzDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="d4368-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d4368-102">SYNOPSIS</span></span>
<span data-ttu-id="d4368-103">獲得 Data Lake Analytics Job 週期或週期。</span><span class="sxs-lookup"><span data-stu-id="d4368-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

## <span data-ttu-id="d4368-104">語法</span><span class="sxs-lookup"><span data-stu-id="d4368-104">SYNTAX</span></span>

### <span data-ttu-id="d4368-105">GetAllInAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="d4368-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4368-106">GetByS0ificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="d4368-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4368-107">描述</span><span class="sxs-lookup"><span data-stu-id="d4368-107">DESCRIPTION</span></span>
<span data-ttu-id="d4368-108">**Get-AzDataLakeAnalyticsJobRecurrence 會** 取得指定的 Azure Data Lake Analytics Job 週期或週期清單。</span><span class="sxs-lookup"><span data-stu-id="d4368-108">The **Get-AzDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="d4368-109">例子</span><span class="sxs-lookup"><span data-stu-id="d4368-109">EXAMPLES</span></span>

### <span data-ttu-id="d4368-110">範例 1：取得指定的週期</span><span class="sxs-lookup"><span data-stu-id="d4368-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="d4368-111">此命令會獲得指定的工作週期，其帳戶 'contocbdla' 中的 id '83cb7ad2-3523-4b82-b909-d478b0d8aea3'。</span><span class="sxs-lookup"><span data-stu-id="d4368-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="d4368-112">範例 2：取得帳戶中所有週期的清單</span><span class="sxs-lookup"><span data-stu-id="d4368-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="d4368-113">此命令會獲得帳戶 "contola" 中所有週期的清單</span><span class="sxs-lookup"><span data-stu-id="d4368-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="d4368-114">參數</span><span class="sxs-lookup"><span data-stu-id="d4368-114">PARAMETERS</span></span>

### <span data-ttu-id="d4368-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="d4368-115">-Account</span></span>
<span data-ttu-id="d4368-116">資料湖分析帳戶名稱的名稱，其下想要取回工作週期。</span><span class="sxs-lookup"><span data-stu-id="d4368-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="d4368-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4368-117">-DefaultProfile</span></span>
<span data-ttu-id="d4368-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d4368-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4368-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="d4368-119">-RecurrenceId</span></span>
<span data-ttu-id="d4368-120">要退回資訊的特定工作週期識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4368-120">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobRecurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4368-121">-提交之後</span><span class="sxs-lookup"><span data-stu-id="d4368-121">-SubmittedAfter</span></span>
<span data-ttu-id="d4368-122">選擇性篩選，會 () 時間後提交的工作週期。</span><span class="sxs-lookup"><span data-stu-id="d4368-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="d4368-123">-提交Before</span><span class="sxs-lookup"><span data-stu-id="d4368-123">-SubmittedBefore</span></span>
<span data-ttu-id="d4368-124">選擇性篩選，會 () 特定時間之前提交的工作週期。</span><span class="sxs-lookup"><span data-stu-id="d4368-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="d4368-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4368-125">CommonParameters</span></span>
<span data-ttu-id="d4368-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d4368-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4368-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d4368-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4368-128">輸入</span><span class="sxs-lookup"><span data-stu-id="d4368-128">INPUTS</span></span>

### <span data-ttu-id="d4368-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d4368-129">System.String</span></span>

### <span data-ttu-id="d4368-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d4368-130">System.Guid</span></span>

### <span data-ttu-id="d4368-131">System.Nullable'1[[System.DateTimeOffset， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d4368-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d4368-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d4368-132">OUTPUTS</span></span>

### <span data-ttu-id="d4368-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="d4368-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="d4368-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d4368-134">NOTES</span></span>

## <span data-ttu-id="d4368-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4368-135">RELATED LINKS</span></span>
