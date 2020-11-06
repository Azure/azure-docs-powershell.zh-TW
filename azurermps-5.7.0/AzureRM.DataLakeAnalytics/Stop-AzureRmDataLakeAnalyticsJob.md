---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/stop-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 956e263f402a3b6cb78631f8337d46fc1effdd98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448692"
---
# <span data-ttu-id="6c60a-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6c60a-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="6c60a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c60a-102">SYNOPSIS</span></span>
<span data-ttu-id="6c60a-103">取消作業。</span><span class="sxs-lookup"><span data-stu-id="6c60a-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c60a-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c60a-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c60a-105">說明</span><span class="sxs-lookup"><span data-stu-id="6c60a-105">DESCRIPTION</span></span>
<span data-ttu-id="6c60a-106">**AzureRmDataLakeAnalyticsJob** Cmdlet 會取消 Azure Data Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="6c60a-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="6c60a-107">示例</span><span class="sxs-lookup"><span data-stu-id="6c60a-107">EXAMPLES</span></span>

### <span data-ttu-id="6c60a-108">範例1：取消作業</span><span class="sxs-lookup"><span data-stu-id="6c60a-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="6c60a-109">這個命令會取消具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="6c60a-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="6c60a-110">參數</span><span class="sxs-lookup"><span data-stu-id="6c60a-110">PARAMETERS</span></span>

### <span data-ttu-id="6c60a-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="6c60a-111">-Account</span></span>
<span data-ttu-id="6c60a-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6c60a-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c60a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c60a-113">-DefaultProfile</span></span>
<span data-ttu-id="6c60a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6c60a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c60a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6c60a-115">-Force</span></span>
<span data-ttu-id="6c60a-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6c60a-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c60a-117">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="6c60a-117">-JobId</span></span>
<span data-ttu-id="6c60a-118">指定要取消的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c60a-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c60a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c60a-119">-PassThru</span></span>
<span data-ttu-id="6c60a-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="6c60a-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6c60a-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="6c60a-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c60a-122">-確認</span><span class="sxs-lookup"><span data-stu-id="6c60a-122">-Confirm</span></span>
<span data-ttu-id="6c60a-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c60a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c60a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c60a-124">-WhatIf</span></span>
<span data-ttu-id="6c60a-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c60a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c60a-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c60a-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c60a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c60a-127">CommonParameters</span></span>
<span data-ttu-id="6c60a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c60a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c60a-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6c60a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c60a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6c60a-130">INPUTS</span></span>

### <span data-ttu-id="6c60a-131">Guid</span><span class="sxs-lookup"><span data-stu-id="6c60a-131">Guid</span></span>
<span data-ttu-id="6c60a-132">形參 "JobId" 接受管線中 "Guid" 類型的值</span><span class="sxs-lookup"><span data-stu-id="6c60a-132">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="6c60a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="6c60a-133">OUTPUTS</span></span>

### <span data-ttu-id="6c60a-134">bool</span><span class="sxs-lookup"><span data-stu-id="6c60a-134">bool</span></span>
<span data-ttu-id="6c60a-135">如果已指定 PassThru，則會在作業完成時傳回 true。</span><span class="sxs-lookup"><span data-stu-id="6c60a-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="6c60a-136">筆記</span><span class="sxs-lookup"><span data-stu-id="6c60a-136">NOTES</span></span>

## <span data-ttu-id="6c60a-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c60a-137">RELATED LINKS</span></span>

[<span data-ttu-id="6c60a-138">AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6c60a-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="6c60a-139">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6c60a-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="6c60a-140">稍候-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6c60a-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


