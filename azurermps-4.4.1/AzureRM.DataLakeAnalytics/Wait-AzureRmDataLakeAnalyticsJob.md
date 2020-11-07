---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 672a992dd86fcbd95e17f0795147231b1b62cd5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625209"
---
# <span data-ttu-id="3e029-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3e029-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="3e029-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e029-102">SYNOPSIS</span></span>
<span data-ttu-id="3e029-103">等待工作完成。</span><span class="sxs-lookup"><span data-stu-id="3e029-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e029-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e029-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e029-105">說明</span><span class="sxs-lookup"><span data-stu-id="3e029-105">DESCRIPTION</span></span>
<span data-ttu-id="3e029-106">**AzureRmDataLakeAnalyticsJob** Cmdlet 會等待 Azure Data Lake Analytics 作業完成。</span><span class="sxs-lookup"><span data-stu-id="3e029-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="3e029-107">示例</span><span class="sxs-lookup"><span data-stu-id="3e029-107">EXAMPLES</span></span>

### <span data-ttu-id="3e029-108">範例1：等候作業完成</span><span class="sxs-lookup"><span data-stu-id="3e029-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="3e029-109">下列命令會等待具有指定識別碼的作業完成。</span><span class="sxs-lookup"><span data-stu-id="3e029-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="3e029-110">參數</span><span class="sxs-lookup"><span data-stu-id="3e029-110">PARAMETERS</span></span>

### <span data-ttu-id="3e029-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="3e029-111">-Account</span></span>
<span data-ttu-id="3e029-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3e029-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="3e029-113">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="3e029-113">-JobId</span></span>
<span data-ttu-id="3e029-114">指定要等候之作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e029-114">Specifies the ID of the job for which to wait.</span></span>

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

### <span data-ttu-id="3e029-115">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="3e029-115">-TimeoutInSeconds</span></span>
<span data-ttu-id="3e029-116">指定在退出等待操作前要等待的秒數。</span><span class="sxs-lookup"><span data-stu-id="3e029-116">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

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

### <span data-ttu-id="3e029-117">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3e029-117">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="3e029-118">指定每次檢查作業狀態之間經過的秒數。</span><span class="sxs-lookup"><span data-stu-id="3e029-118">Specify the number of seconds that elapse between each check of the job state.</span></span>

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

### <span data-ttu-id="3e029-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e029-119">-DefaultProfile</span></span>
<span data-ttu-id="3e029-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e029-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e029-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e029-121">CommonParameters</span></span>
<span data-ttu-id="3e029-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e029-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e029-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e029-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e029-124">輸入</span><span class="sxs-lookup"><span data-stu-id="3e029-124">INPUTS</span></span>

### <span data-ttu-id="3e029-125">Guid</span><span class="sxs-lookup"><span data-stu-id="3e029-125">Guid</span></span>
<span data-ttu-id="3e029-126">形參 "JobId" 接受管線中 "Guid" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3e029-126">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="3e029-127">輸出</span><span class="sxs-lookup"><span data-stu-id="3e029-127">OUTPUTS</span></span>

### <span data-ttu-id="3e029-128">JobInformation</span><span class="sxs-lookup"><span data-stu-id="3e029-128">JobInformation</span></span>
<span data-ttu-id="3e029-129">已完成作業的最終作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3e029-129">The final job details for the completed job.</span></span>

## <span data-ttu-id="3e029-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3e029-130">NOTES</span></span>

## <span data-ttu-id="3e029-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e029-131">RELATED LINKS</span></span>

[<span data-ttu-id="3e029-132">AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3e029-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="3e029-133">停止 AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3e029-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="3e029-134">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3e029-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)


