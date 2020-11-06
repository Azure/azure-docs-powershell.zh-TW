---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: b6c703b1c3373e4e0f1347d9bb2a9819ac1e5de6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449682"
---
# <span data-ttu-id="12677-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="12677-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="12677-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12677-102">SYNOPSIS</span></span>
<span data-ttu-id="12677-103">移除資料流程分析作業。</span><span class="sxs-lookup"><span data-stu-id="12677-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12677-104">句法</span><span class="sxs-lookup"><span data-stu-id="12677-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12677-105">說明</span><span class="sxs-lookup"><span data-stu-id="12677-105">DESCRIPTION</span></span>
<span data-ttu-id="12677-106">**AzureRmStreamAnalyticsJob** Cmdlet 會以非同步方式刪除 Azure 中的特定資料流程分析作業。</span><span class="sxs-lookup"><span data-stu-id="12677-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="12677-107">示例</span><span class="sxs-lookup"><span data-stu-id="12677-107">EXAMPLES</span></span>

### <span data-ttu-id="12677-108">範例1：移除作業</span><span class="sxs-lookup"><span data-stu-id="12677-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="12677-109">這個命令會移除作業 StreamingJob。</span><span class="sxs-lookup"><span data-stu-id="12677-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="12677-110">參數</span><span class="sxs-lookup"><span data-stu-id="12677-110">PARAMETERS</span></span>

### <span data-ttu-id="12677-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12677-111">-DefaultProfile</span></span>
<span data-ttu-id="12677-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12677-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12677-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="12677-113">-Name</span></span>
<span data-ttu-id="12677-114">指定要移除之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="12677-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12677-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12677-115">-ResourceGroupName</span></span>
<span data-ttu-id="12677-116">指定 Azure 資料流程分析作業所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="12677-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12677-117">-確認</span><span class="sxs-lookup"><span data-stu-id="12677-117">-Confirm</span></span>
<span data-ttu-id="12677-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12677-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12677-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12677-119">-WhatIf</span></span>
<span data-ttu-id="12677-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12677-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12677-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12677-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12677-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12677-122">CommonParameters</span></span>
<span data-ttu-id="12677-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12677-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12677-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12677-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12677-125">輸入</span><span class="sxs-lookup"><span data-stu-id="12677-125">INPUTS</span></span>

### <span data-ttu-id="12677-126">System.object</span><span class="sxs-lookup"><span data-stu-id="12677-126">System.String</span></span>

## <span data-ttu-id="12677-127">輸出</span><span class="sxs-lookup"><span data-stu-id="12677-127">OUTPUTS</span></span>

### <span data-ttu-id="12677-128">System.object</span><span class="sxs-lookup"><span data-stu-id="12677-128">System.Boolean</span></span>

## <span data-ttu-id="12677-129">筆記</span><span class="sxs-lookup"><span data-stu-id="12677-129">NOTES</span></span>

## <span data-ttu-id="12677-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="12677-130">RELATED LINKS</span></span>

[<span data-ttu-id="12677-131">AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="12677-131">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="12677-132">新-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="12677-132">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="12677-133">開始-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="12677-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="12677-134">停止 AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="12677-134">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


