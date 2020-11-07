---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 53bd361d67829fdf30741540f1435032067508e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792032"
---
# <span data-ttu-id="58ebc-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="58ebc-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="58ebc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="58ebc-103">刪除資料流程分析作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="58ebc-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="58ebc-104">句法</span><span class="sxs-lookup"><span data-stu-id="58ebc-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58ebc-105">說明</span><span class="sxs-lookup"><span data-stu-id="58ebc-105">DESCRIPTION</span></span>
<span data-ttu-id="58ebc-106">**AzStreamAnalyticsOutput** Cmdlet 會在 Azure 中非同步刪除資料流程分析作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="58ebc-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="58ebc-107">示例</span><span class="sxs-lookup"><span data-stu-id="58ebc-107">EXAMPLES</span></span>

### <span data-ttu-id="58ebc-108">範例1：移除作業的輸出</span><span class="sxs-lookup"><span data-stu-id="58ebc-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="58ebc-109">這個命令會移除作業 StreamingJob 中的輸出輸出。</span><span class="sxs-lookup"><span data-stu-id="58ebc-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="58ebc-110">參數</span><span class="sxs-lookup"><span data-stu-id="58ebc-110">PARAMETERS</span></span>

### <span data-ttu-id="58ebc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ebc-111">-DefaultProfile</span></span>
<span data-ttu-id="58ebc-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58ebc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58ebc-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="58ebc-113">-JobName</span></span>
<span data-ttu-id="58ebc-114">指定 Azure 資料流程分析輸出所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="58ebc-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="58ebc-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="58ebc-115">-Name</span></span>
<span data-ttu-id="58ebc-116">指定要移除之 Azure 資料流程分析輸出的名稱。</span><span class="sxs-lookup"><span data-stu-id="58ebc-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ebc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ebc-117">-ResourceGroupName</span></span>
<span data-ttu-id="58ebc-118">指定 Azure 資料流程分析輸出所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="58ebc-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="58ebc-119">-確認</span><span class="sxs-lookup"><span data-stu-id="58ebc-119">-Confirm</span></span>
<span data-ttu-id="58ebc-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58ebc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58ebc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58ebc-121">-WhatIf</span></span>
<span data-ttu-id="58ebc-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58ebc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58ebc-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58ebc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58ebc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ebc-124">CommonParameters</span></span>
<span data-ttu-id="58ebc-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58ebc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ebc-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58ebc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ebc-127">輸入</span><span class="sxs-lookup"><span data-stu-id="58ebc-127">INPUTS</span></span>

### <span data-ttu-id="58ebc-128">System.object</span><span class="sxs-lookup"><span data-stu-id="58ebc-128">System.String</span></span>

## <span data-ttu-id="58ebc-129">輸出</span><span class="sxs-lookup"><span data-stu-id="58ebc-129">OUTPUTS</span></span>

### <span data-ttu-id="58ebc-130">System.object</span><span class="sxs-lookup"><span data-stu-id="58ebc-130">System.Boolean</span></span>

## <span data-ttu-id="58ebc-131">筆記</span><span class="sxs-lookup"><span data-stu-id="58ebc-131">NOTES</span></span>

## <span data-ttu-id="58ebc-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="58ebc-132">RELATED LINKS</span></span>

[<span data-ttu-id="58ebc-133">AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="58ebc-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="58ebc-134">新-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="58ebc-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="58ebc-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="58ebc-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


