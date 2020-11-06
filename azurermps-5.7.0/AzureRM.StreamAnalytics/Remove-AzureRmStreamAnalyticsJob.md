---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 64ebe431333914a907c515744501f4624a7977ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447568"
---
# <span data-ttu-id="722e6-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="722e6-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="722e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="722e6-102">SYNOPSIS</span></span>
<span data-ttu-id="722e6-103">移除資料流程分析作業。</span><span class="sxs-lookup"><span data-stu-id="722e6-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="722e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="722e6-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="722e6-105">說明</span><span class="sxs-lookup"><span data-stu-id="722e6-105">DESCRIPTION</span></span>
<span data-ttu-id="722e6-106">**AzureRmStreamAnalyticsJob** Cmdlet 會以非同步方式刪除 Azure 中的特定資料流程分析作業。</span><span class="sxs-lookup"><span data-stu-id="722e6-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="722e6-107">示例</span><span class="sxs-lookup"><span data-stu-id="722e6-107">EXAMPLES</span></span>

### <span data-ttu-id="722e6-108">範例1：移除作業</span><span class="sxs-lookup"><span data-stu-id="722e6-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="722e6-109">這個命令會移除作業 StreamingJob。</span><span class="sxs-lookup"><span data-stu-id="722e6-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="722e6-110">參數</span><span class="sxs-lookup"><span data-stu-id="722e6-110">PARAMETERS</span></span>

### <span data-ttu-id="722e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="722e6-111">-DefaultProfile</span></span>
<span data-ttu-id="722e6-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="722e6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="722e6-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="722e6-113">-Name</span></span>
<span data-ttu-id="722e6-114">指定要移除之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="722e6-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="722e6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="722e6-115">-ResourceGroupName</span></span>
<span data-ttu-id="722e6-116">指定 Azure 資料流程分析作業所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="722e6-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="722e6-117">-確認</span><span class="sxs-lookup"><span data-stu-id="722e6-117">-Confirm</span></span>
<span data-ttu-id="722e6-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="722e6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="722e6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="722e6-119">-WhatIf</span></span>
<span data-ttu-id="722e6-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="722e6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="722e6-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="722e6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="722e6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="722e6-122">CommonParameters</span></span>
<span data-ttu-id="722e6-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="722e6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="722e6-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="722e6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="722e6-125">輸入</span><span class="sxs-lookup"><span data-stu-id="722e6-125">INPUTS</span></span>

### <span data-ttu-id="722e6-126">所有</span><span class="sxs-lookup"><span data-stu-id="722e6-126">None</span></span>
<span data-ttu-id="722e6-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="722e6-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="722e6-128">輸出</span><span class="sxs-lookup"><span data-stu-id="722e6-128">OUTPUTS</span></span>

### <span data-ttu-id="722e6-129">System.object</span><span class="sxs-lookup"><span data-stu-id="722e6-129">System.Object</span></span>

## <span data-ttu-id="722e6-130">筆記</span><span class="sxs-lookup"><span data-stu-id="722e6-130">NOTES</span></span>

## <span data-ttu-id="722e6-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="722e6-131">RELATED LINKS</span></span>

[<span data-ttu-id="722e6-132">AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="722e6-132">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="722e6-133">新-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="722e6-133">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="722e6-134">開始-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="722e6-134">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="722e6-135">停止 AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="722e6-135">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


