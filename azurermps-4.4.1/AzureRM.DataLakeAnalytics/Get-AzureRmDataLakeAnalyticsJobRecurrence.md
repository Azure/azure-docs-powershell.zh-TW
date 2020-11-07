---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: cfc5d0999ed9c77e38b83eee99eabbd19dd1e493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626310"
---
# <span data-ttu-id="a6339-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="a6339-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="a6339-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6339-102">SYNOPSIS</span></span>
<span data-ttu-id="a6339-103">取得資料 Lake Analytics 作業週期或重複執行。</span><span class="sxs-lookup"><span data-stu-id="a6339-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6339-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6339-104">SYNTAX</span></span>

### <span data-ttu-id="a6339-105">所有帳戶 (預設) </span><span class="sxs-lookup"><span data-stu-id="a6339-105">All In Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6339-106">特定作業週期</span><span class="sxs-lookup"><span data-stu-id="a6339-106">Specific Job Recurrence</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6339-107">說明</span><span class="sxs-lookup"><span data-stu-id="a6339-107">DESCRIPTION</span></span>
<span data-ttu-id="a6339-108">**AzureRmDataLakeAnalyticsJobRecurrence** 會取得指定的 Azure Data Lake Analytics 作業週期或定期清單。</span><span class="sxs-lookup"><span data-stu-id="a6339-108">The **Get-AzureRmDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="a6339-109">示例</span><span class="sxs-lookup"><span data-stu-id="a6339-109">EXAMPLES</span></span>

### <span data-ttu-id="a6339-110">範例1：取得指定的週期</span><span class="sxs-lookup"><span data-stu-id="a6339-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="a6339-111">此命令會取得帳戶 "contosoadla" 中 id 為「83cb7ad2-3523-4b82-b909-d478b0d8aea3」的指定作業週期。</span><span class="sxs-lookup"><span data-stu-id="a6339-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="a6339-112">範例2：取得帳戶中所有定期作業的清單</span><span class="sxs-lookup"><span data-stu-id="a6339-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="a6339-113">這個命令會取得帳戶 "contosoadla" 中所有週期性清單</span><span class="sxs-lookup"><span data-stu-id="a6339-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="a6339-114">參數</span><span class="sxs-lookup"><span data-stu-id="a6339-114">PARAMETERS</span></span>

### <span data-ttu-id="a6339-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a6339-115">-Account</span></span>
<span data-ttu-id="a6339-116">要在其中檢索作業週期之資料 Lake Analytics 帳戶名稱的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6339-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="a6339-117">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="a6339-117">-RecurrenceId</span></span>
<span data-ttu-id="a6339-118">針對其傳回信息的特定作業週期識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6339-118">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific Job Recurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6339-119">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="a6339-119">-SubmittedAfter</span></span>
<span data-ttu-id="a6339-120">會傳回作業週期 () 只會在指定的時間之後提交的選用篩選。</span><span class="sxs-lookup"><span data-stu-id="a6339-120">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="a6339-121">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="a6339-121">-SubmittedBefore</span></span>
<span data-ttu-id="a6339-122">會傳回作業週期 () 只會在指定的時間前提交的選用篩選。</span><span class="sxs-lookup"><span data-stu-id="a6339-122">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="a6339-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6339-123">-DefaultProfile</span></span>
<span data-ttu-id="a6339-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6339-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6339-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6339-125">CommonParameters</span></span>
<span data-ttu-id="a6339-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6339-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6339-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6339-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6339-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a6339-128">INPUTS</span></span>

### <span data-ttu-id="a6339-129">System.object</span><span class="sxs-lookup"><span data-stu-id="a6339-129">System.String</span></span>
<span data-ttu-id="a6339-130">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="a6339-130">System.Guid</span></span>

## <span data-ttu-id="a6339-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a6339-131">OUTPUTS</span></span>

### <span data-ttu-id="a6339-132">PSJobRecurrenceInformation 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="a6339-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="a6339-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a6339-133">NOTES</span></span>

## <span data-ttu-id="a6339-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6339-134">RELATED LINKS</span></span>
