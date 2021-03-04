---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: f735dc3f213069c1ecf5bbae9d1d5cf24dda98a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902910"
---
# <span data-ttu-id="73cd2-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="73cd2-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="73cd2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="73cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="73cd2-103">等待工作完成。</span><span class="sxs-lookup"><span data-stu-id="73cd2-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="73cd2-104">語法</span><span class="sxs-lookup"><span data-stu-id="73cd2-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73cd2-105">描述</span><span class="sxs-lookup"><span data-stu-id="73cd2-105">DESCRIPTION</span></span>
<span data-ttu-id="73cd2-106">**Wait-AzDataLakeAnalyticsJob** Cmdlet 會等待 Azure Data Lake Analytics 工作完成。</span><span class="sxs-lookup"><span data-stu-id="73cd2-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="73cd2-107">例子</span><span class="sxs-lookup"><span data-stu-id="73cd2-107">EXAMPLES</span></span>

### <span data-ttu-id="73cd2-108">範例 1：等待工作完成</span><span class="sxs-lookup"><span data-stu-id="73cd2-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="73cd2-109">下列命令會等待具有指定識別碼的工作完成。</span><span class="sxs-lookup"><span data-stu-id="73cd2-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="73cd2-110">參數</span><span class="sxs-lookup"><span data-stu-id="73cd2-110">PARAMETERS</span></span>

### <span data-ttu-id="73cd2-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="73cd2-111">-Account</span></span>
<span data-ttu-id="73cd2-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="73cd2-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="73cd2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73cd2-113">-DefaultProfile</span></span>
<span data-ttu-id="73cd2-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="73cd2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73cd2-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="73cd2-115">-JobId</span></span>
<span data-ttu-id="73cd2-116">指定要等待的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="73cd2-116">Specifies the ID of the job for which to wait.</span></span>

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

### <span data-ttu-id="73cd2-117">-TimeoutIn用秒</span><span class="sxs-lookup"><span data-stu-id="73cd2-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="73cd2-118">指定在離開等待作業前要等候的秒數。</span><span class="sxs-lookup"><span data-stu-id="73cd2-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

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

### <span data-ttu-id="73cd2-119">-WaitIntervalIn用秒</span><span class="sxs-lookup"><span data-stu-id="73cd2-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="73cd2-120">指定每次檢查工作狀態之間經過的秒數。</span><span class="sxs-lookup"><span data-stu-id="73cd2-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

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

### <span data-ttu-id="73cd2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73cd2-121">CommonParameters</span></span>
<span data-ttu-id="73cd2-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="73cd2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73cd2-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="73cd2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73cd2-124">輸入</span><span class="sxs-lookup"><span data-stu-id="73cd2-124">INPUTS</span></span>

### <span data-ttu-id="73cd2-125">System.String</span><span class="sxs-lookup"><span data-stu-id="73cd2-125">System.String</span></span>

### <span data-ttu-id="73cd2-126">System.Guid</span><span class="sxs-lookup"><span data-stu-id="73cd2-126">System.Guid</span></span>

### <span data-ttu-id="73cd2-127">System.Int32</span><span class="sxs-lookup"><span data-stu-id="73cd2-127">System.Int32</span></span>

## <span data-ttu-id="73cd2-128">輸出</span><span class="sxs-lookup"><span data-stu-id="73cd2-128">OUTPUTS</span></span>

### <span data-ttu-id="73cd2-129">Microsoft.Azure.management.DataLake.Analytics.models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="73cd2-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="73cd2-130">筆記</span><span class="sxs-lookup"><span data-stu-id="73cd2-130">NOTES</span></span>

## <span data-ttu-id="73cd2-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="73cd2-131">RELATED LINKS</span></span>

[<span data-ttu-id="73cd2-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="73cd2-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="73cd2-133">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="73cd2-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="73cd2-134">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="73cd2-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)


