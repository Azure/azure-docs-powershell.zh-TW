---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: a0848ffc888b4812a28198749417d0b0894a5d98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626011"
---
# <span data-ttu-id="e96a6-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e96a6-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="e96a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e96a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e96a6-103">取消作業。</span><span class="sxs-lookup"><span data-stu-id="e96a6-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e96a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="e96a6-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e96a6-105">說明</span><span class="sxs-lookup"><span data-stu-id="e96a6-105">DESCRIPTION</span></span>
<span data-ttu-id="e96a6-106">**AzureRmDataLakeAnalyticsJob** Cmdlet 會取消 Azure Data Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="e96a6-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="e96a6-107">示例</span><span class="sxs-lookup"><span data-stu-id="e96a6-107">EXAMPLES</span></span>

### <span data-ttu-id="e96a6-108">範例1：取消作業</span><span class="sxs-lookup"><span data-stu-id="e96a6-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="e96a6-109">這個命令會取消具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="e96a6-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="e96a6-110">參數</span><span class="sxs-lookup"><span data-stu-id="e96a6-110">PARAMETERS</span></span>

### <span data-ttu-id="e96a6-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e96a6-111">-Account</span></span>
<span data-ttu-id="e96a6-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e96a6-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e96a6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e96a6-113">-Force</span></span>
<span data-ttu-id="e96a6-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e96a6-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96a6-115">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="e96a6-115">-JobId</span></span>
<span data-ttu-id="e96a6-116">指定要取消的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="e96a6-116">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="e96a6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e96a6-117">-PassThru</span></span>
<span data-ttu-id="e96a6-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e96a6-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e96a6-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e96a6-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96a6-120">-確認</span><span class="sxs-lookup"><span data-stu-id="e96a6-120">-Confirm</span></span>
<span data-ttu-id="e96a6-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e96a6-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96a6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e96a6-122">-WhatIf</span></span>
<span data-ttu-id="e96a6-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e96a6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e96a6-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e96a6-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96a6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e96a6-125">-DefaultProfile</span></span>
<span data-ttu-id="e96a6-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e96a6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e96a6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e96a6-127">CommonParameters</span></span>
<span data-ttu-id="e96a6-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e96a6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e96a6-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e96a6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e96a6-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e96a6-130">INPUTS</span></span>

### <span data-ttu-id="e96a6-131">Guid</span><span class="sxs-lookup"><span data-stu-id="e96a6-131">Guid</span></span>
<span data-ttu-id="e96a6-132">形參 "JobId" 接受管線中 "Guid" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e96a6-132">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="e96a6-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e96a6-133">OUTPUTS</span></span>

### <span data-ttu-id="e96a6-134">bool</span><span class="sxs-lookup"><span data-stu-id="e96a6-134">bool</span></span>
<span data-ttu-id="e96a6-135">如果已指定 PassThru，則會在作業完成時傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e96a6-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="e96a6-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e96a6-136">NOTES</span></span>

## <span data-ttu-id="e96a6-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e96a6-137">RELATED LINKS</span></span>

[<span data-ttu-id="e96a6-138">AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e96a6-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="e96a6-139">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e96a6-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="e96a6-140">稍候-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e96a6-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


