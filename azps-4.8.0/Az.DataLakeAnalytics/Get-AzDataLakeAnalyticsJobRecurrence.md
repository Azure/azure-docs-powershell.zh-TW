---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: d571eb887069aa5c28029dfa98ab022c1d82fc88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971144"
---
# <span data-ttu-id="9ad13-101">Get-AzDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="9ad13-101">Get-AzDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="9ad13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ad13-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad13-103">取得資料 Lake Analytics 作業週期或重複執行。</span><span class="sxs-lookup"><span data-stu-id="9ad13-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

## <span data-ttu-id="9ad13-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ad13-104">SYNTAX</span></span>

### <span data-ttu-id="9ad13-105">GetAllInAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="9ad13-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ad13-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="9ad13-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ad13-107">說明</span><span class="sxs-lookup"><span data-stu-id="9ad13-107">DESCRIPTION</span></span>
<span data-ttu-id="9ad13-108">**AzDataLakeAnalyticsJobRecurrence** 會取得指定的 Azure Data Lake Analytics 作業週期或定期清單。</span><span class="sxs-lookup"><span data-stu-id="9ad13-108">The **Get-AzDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="9ad13-109">示例</span><span class="sxs-lookup"><span data-stu-id="9ad13-109">EXAMPLES</span></span>

### <span data-ttu-id="9ad13-110">範例1：取得指定的週期</span><span class="sxs-lookup"><span data-stu-id="9ad13-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="9ad13-111">此命令會取得帳戶 "contosoadla" 中 id 為「83cb7ad2-3523-4b82-b909-d478b0d8aea3」的指定作業週期。</span><span class="sxs-lookup"><span data-stu-id="9ad13-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="9ad13-112">範例2：取得帳戶中所有定期作業的清單</span><span class="sxs-lookup"><span data-stu-id="9ad13-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="9ad13-113">這個命令會取得帳戶 "contosoadla" 中所有週期性清單</span><span class="sxs-lookup"><span data-stu-id="9ad13-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="9ad13-114">參數</span><span class="sxs-lookup"><span data-stu-id="9ad13-114">PARAMETERS</span></span>

### <span data-ttu-id="9ad13-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="9ad13-115">-Account</span></span>
<span data-ttu-id="9ad13-116">要在其中檢索作業週期之資料 Lake Analytics 帳戶名稱的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ad13-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="9ad13-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad13-117">-DefaultProfile</span></span>
<span data-ttu-id="9ad13-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9ad13-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ad13-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="9ad13-119">-RecurrenceId</span></span>
<span data-ttu-id="9ad13-120">針對其傳回信息的特定作業週期識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ad13-120">ID of the specific job recurrence to return information for.</span></span>

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

### <span data-ttu-id="9ad13-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="9ad13-121">-SubmittedAfter</span></span>
<span data-ttu-id="9ad13-122">會傳回作業週期 () 只會在指定的時間之後提交的選用篩選。</span><span class="sxs-lookup"><span data-stu-id="9ad13-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="9ad13-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="9ad13-123">-SubmittedBefore</span></span>
<span data-ttu-id="9ad13-124">會傳回作業週期 () 只會在指定的時間前提交的選用篩選。</span><span class="sxs-lookup"><span data-stu-id="9ad13-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="9ad13-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad13-125">CommonParameters</span></span>
<span data-ttu-id="9ad13-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ad13-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad13-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9ad13-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad13-128">輸入</span><span class="sxs-lookup"><span data-stu-id="9ad13-128">INPUTS</span></span>

### <span data-ttu-id="9ad13-129">System.object</span><span class="sxs-lookup"><span data-stu-id="9ad13-129">System.String</span></span>

### <span data-ttu-id="9ad13-130">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="9ad13-130">System.Guid</span></span>

### <span data-ttu-id="9ad13-131">"CoreLib" 1 [（System.object，System.object，，版本 = 4.0.0.0，Culture = 中立，</span><span class="sxs-lookup"><span data-stu-id="9ad13-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9ad13-132">輸出</span><span class="sxs-lookup"><span data-stu-id="9ad13-132">OUTPUTS</span></span>

### <span data-ttu-id="9ad13-133">PSJobRecurrenceInformation 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="9ad13-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="9ad13-134">筆記</span><span class="sxs-lookup"><span data-stu-id="9ad13-134">NOTES</span></span>

## <span data-ttu-id="9ad13-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ad13-135">RELATED LINKS</span></span>
