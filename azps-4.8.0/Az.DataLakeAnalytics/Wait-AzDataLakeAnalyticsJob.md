---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 047d0c7c9b141f10ee3f1be2ba1e739960f2e5bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127086"
---
# <span data-ttu-id="9f451-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9f451-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="9f451-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f451-102">SYNOPSIS</span></span>
<span data-ttu-id="9f451-103">等待工作完成。</span><span class="sxs-lookup"><span data-stu-id="9f451-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="9f451-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f451-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f451-105">說明</span><span class="sxs-lookup"><span data-stu-id="9f451-105">DESCRIPTION</span></span>
<span data-ttu-id="9f451-106">**AzDataLakeAnalyticsJob** Cmdlet 會等待 Azure Data Lake Analytics 作業完成。</span><span class="sxs-lookup"><span data-stu-id="9f451-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="9f451-107">示例</span><span class="sxs-lookup"><span data-stu-id="9f451-107">EXAMPLES</span></span>

### <span data-ttu-id="9f451-108">範例1：等候作業完成</span><span class="sxs-lookup"><span data-stu-id="9f451-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="9f451-109">下列命令會等待具有指定識別碼的作業完成。</span><span class="sxs-lookup"><span data-stu-id="9f451-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="9f451-110">參數</span><span class="sxs-lookup"><span data-stu-id="9f451-110">PARAMETERS</span></span>

### <span data-ttu-id="9f451-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="9f451-111">-Account</span></span>
<span data-ttu-id="9f451-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9f451-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="9f451-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f451-113">-DefaultProfile</span></span>
<span data-ttu-id="9f451-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9f451-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f451-115">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="9f451-115">-JobId</span></span>
<span data-ttu-id="9f451-116">指定要等候之作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9f451-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f451-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="9f451-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="9f451-118">指定在退出等待操作前要等待的秒數。</span><span class="sxs-lookup"><span data-stu-id="9f451-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f451-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9f451-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="9f451-120">指定每次檢查作業狀態之間經過的秒數。</span><span class="sxs-lookup"><span data-stu-id="9f451-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f451-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f451-121">CommonParameters</span></span>
<span data-ttu-id="9f451-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f451-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f451-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9f451-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f451-124">輸入</span><span class="sxs-lookup"><span data-stu-id="9f451-124">INPUTS</span></span>

### <span data-ttu-id="9f451-125">System.object</span><span class="sxs-lookup"><span data-stu-id="9f451-125">System.String</span></span>

### <span data-ttu-id="9f451-126">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="9f451-126">System.Guid</span></span>

### <span data-ttu-id="9f451-127">System.object</span><span class="sxs-lookup"><span data-stu-id="9f451-127">System.Int32</span></span>

## <span data-ttu-id="9f451-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9f451-128">OUTPUTS</span></span>

### <span data-ttu-id="9f451-129">[DataLake. JobInformation]。</span><span class="sxs-lookup"><span data-stu-id="9f451-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="9f451-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9f451-130">NOTES</span></span>

## <span data-ttu-id="9f451-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f451-131">RELATED LINKS</span></span>

[<span data-ttu-id="9f451-132">AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9f451-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="9f451-133">停止 AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9f451-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="9f451-134">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9f451-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)


