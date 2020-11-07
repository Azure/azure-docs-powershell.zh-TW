---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 9904699d95429e029f330e5c3ca3e5957eb4c35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623629"
---
# <span data-ttu-id="b6986-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b6986-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="b6986-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6986-102">SYNOPSIS</span></span>
<span data-ttu-id="b6986-103">刪除資料流程分析作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="b6986-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6986-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6986-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6986-105">說明</span><span class="sxs-lookup"><span data-stu-id="b6986-105">DESCRIPTION</span></span>
<span data-ttu-id="b6986-106">**AzureRmStreamAnalyticsOutput** Cmdlet 會在 Azure 中非同步刪除資料流程分析作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="b6986-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="b6986-107">示例</span><span class="sxs-lookup"><span data-stu-id="b6986-107">EXAMPLES</span></span>

### <span data-ttu-id="b6986-108">範例1：移除作業的輸出</span><span class="sxs-lookup"><span data-stu-id="b6986-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="b6986-109">這個命令會移除作業 StreamingJob 中的輸出輸出。</span><span class="sxs-lookup"><span data-stu-id="b6986-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="b6986-110">參數</span><span class="sxs-lookup"><span data-stu-id="b6986-110">PARAMETERS</span></span>

### <span data-ttu-id="b6986-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="b6986-111">-JobName</span></span>
<span data-ttu-id="b6986-112">指定 Azure 資料流程分析輸出所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6986-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="b6986-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6986-113">-Name</span></span>
<span data-ttu-id="b6986-114">指定要移除之 Azure 資料流程分析輸出的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6986-114">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="b6986-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6986-115">-ResourceGroupName</span></span>
<span data-ttu-id="b6986-116">指定 Azure 資料流程分析輸出所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6986-116">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="b6986-117">-確認</span><span class="sxs-lookup"><span data-stu-id="b6986-117">-Confirm</span></span>
<span data-ttu-id="b6986-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b6986-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6986-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6986-119">-WhatIf</span></span>
<span data-ttu-id="b6986-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6986-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6986-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6986-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6986-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6986-122">-DefaultProfile</span></span>
<span data-ttu-id="b6986-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6986-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6986-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6986-124">CommonParameters</span></span>
<span data-ttu-id="b6986-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6986-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6986-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b6986-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6986-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b6986-127">INPUTS</span></span>

## <span data-ttu-id="b6986-128">輸出</span><span class="sxs-lookup"><span data-stu-id="b6986-128">OUTPUTS</span></span>

### <span data-ttu-id="b6986-129">System.object</span><span class="sxs-lookup"><span data-stu-id="b6986-129">System.Object</span></span>

## <span data-ttu-id="b6986-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b6986-130">NOTES</span></span>

## <span data-ttu-id="b6986-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6986-131">RELATED LINKS</span></span>

[<span data-ttu-id="b6986-132">AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b6986-132">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="b6986-133">新-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b6986-133">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="b6986-134">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b6986-134">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


