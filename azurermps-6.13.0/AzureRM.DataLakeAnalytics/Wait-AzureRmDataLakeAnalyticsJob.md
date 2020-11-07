---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/wait-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 302129506c516cd0f2864210d5323b83fb54e0df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624406"
---
# <span data-ttu-id="59448-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="59448-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="59448-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59448-102">SYNOPSIS</span></span>
<span data-ttu-id="59448-103">等待工作完成。</span><span class="sxs-lookup"><span data-stu-id="59448-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59448-104">句法</span><span class="sxs-lookup"><span data-stu-id="59448-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59448-105">說明</span><span class="sxs-lookup"><span data-stu-id="59448-105">DESCRIPTION</span></span>
<span data-ttu-id="59448-106">**AzureRmDataLakeAnalyticsJob** Cmdlet 會等待 Azure Data Lake Analytics 作業完成。</span><span class="sxs-lookup"><span data-stu-id="59448-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="59448-107">示例</span><span class="sxs-lookup"><span data-stu-id="59448-107">EXAMPLES</span></span>

### <span data-ttu-id="59448-108">範例1：等候作業完成</span><span class="sxs-lookup"><span data-stu-id="59448-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="59448-109">下列命令會等待具有指定識別碼的作業完成。</span><span class="sxs-lookup"><span data-stu-id="59448-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="59448-110">參數</span><span class="sxs-lookup"><span data-stu-id="59448-110">PARAMETERS</span></span>

### <span data-ttu-id="59448-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="59448-111">-Account</span></span>
<span data-ttu-id="59448-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="59448-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="59448-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59448-113">-DefaultProfile</span></span>
<span data-ttu-id="59448-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="59448-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59448-115">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="59448-115">-JobId</span></span>
<span data-ttu-id="59448-116">指定要等候之作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="59448-116">Specifies the ID of the job for which to wait.</span></span>

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

### <span data-ttu-id="59448-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="59448-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="59448-118">指定在退出等待操作前要等待的秒數。</span><span class="sxs-lookup"><span data-stu-id="59448-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

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

### <span data-ttu-id="59448-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="59448-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="59448-120">指定每次檢查作業狀態之間經過的秒數。</span><span class="sxs-lookup"><span data-stu-id="59448-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

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

### <span data-ttu-id="59448-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59448-121">CommonParameters</span></span>
<span data-ttu-id="59448-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59448-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59448-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59448-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59448-124">輸入</span><span class="sxs-lookup"><span data-stu-id="59448-124">INPUTS</span></span>

### <span data-ttu-id="59448-125">System.object</span><span class="sxs-lookup"><span data-stu-id="59448-125">System.String</span></span>

### <span data-ttu-id="59448-126">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="59448-126">System.Guid</span></span>

### <span data-ttu-id="59448-127">System.object</span><span class="sxs-lookup"><span data-stu-id="59448-127">System.Int32</span></span>

## <span data-ttu-id="59448-128">輸出</span><span class="sxs-lookup"><span data-stu-id="59448-128">OUTPUTS</span></span>

### <span data-ttu-id="59448-129">[DataLake. JobInformation]。</span><span class="sxs-lookup"><span data-stu-id="59448-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="59448-130">筆記</span><span class="sxs-lookup"><span data-stu-id="59448-130">NOTES</span></span>

## <span data-ttu-id="59448-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="59448-131">RELATED LINKS</span></span>

[<span data-ttu-id="59448-132">AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="59448-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="59448-133">停止 AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="59448-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="59448-134">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="59448-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)


