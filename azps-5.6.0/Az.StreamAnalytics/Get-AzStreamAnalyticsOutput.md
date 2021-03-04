---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 1f959f96b02296d4cc25cca06ae6c95bdef98af7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907386"
---
# <span data-ttu-id="31227-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="31227-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="31227-102">簡介</span><span class="sxs-lookup"><span data-stu-id="31227-102">SYNOPSIS</span></span>
<span data-ttu-id="31227-103">獲得指定 Stream Analytics 工作或輸出中定義的輸出。</span><span class="sxs-lookup"><span data-stu-id="31227-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="31227-104">語法</span><span class="sxs-lookup"><span data-stu-id="31227-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31227-105">描述</span><span class="sxs-lookup"><span data-stu-id="31227-105">DESCRIPTION</span></span>
<span data-ttu-id="31227-106">**Get-AzStreamAnalyticsOutput** Cmdlet 會列出指定 Stream Analytics 工作定義的所有輸出，或取得特定輸出的資訊。</span><span class="sxs-lookup"><span data-stu-id="31227-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="31227-107">例子</span><span class="sxs-lookup"><span data-stu-id="31227-107">EXAMPLES</span></span>

### <span data-ttu-id="31227-108">範例 1：取得有關工作輸出的資訊</span><span class="sxs-lookup"><span data-stu-id="31227-108">Example 1: Get information about job outputs</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="31227-109">此命令會返回有關在 Job StreamingJob 上定義之輸出的資訊。</span><span class="sxs-lookup"><span data-stu-id="31227-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="31227-110">範例 2：取得特定工作輸出的資訊</span><span class="sxs-lookup"><span data-stu-id="31227-110">Example 2: Get information about a specific job output</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="31227-111">此命令會返回有關在 Job StreamingJob 上定義之輸出之輸出的資訊。</span><span class="sxs-lookup"><span data-stu-id="31227-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="31227-112">參數</span><span class="sxs-lookup"><span data-stu-id="31227-112">PARAMETERS</span></span>

### <span data-ttu-id="31227-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31227-113">-DefaultProfile</span></span>
<span data-ttu-id="31227-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="31227-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31227-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="31227-115">-JobName</span></span>
<span data-ttu-id="31227-116">指定 Azure Stream Analytics 輸出所屬的 Azure Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="31227-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="31227-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="31227-117">-Name</span></span>
<span data-ttu-id="31227-118">指定要取回的 Azure Stream Analytics 輸出名稱。</span><span class="sxs-lookup"><span data-stu-id="31227-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31227-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31227-119">-ResourceGroupName</span></span>
<span data-ttu-id="31227-120">指定 Azure Stream Analytics 輸出所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="31227-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="31227-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31227-121">CommonParameters</span></span>
<span data-ttu-id="31227-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="31227-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31227-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="31227-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31227-124">輸入</span><span class="sxs-lookup"><span data-stu-id="31227-124">INPUTS</span></span>

### <span data-ttu-id="31227-125">System.String</span><span class="sxs-lookup"><span data-stu-id="31227-125">System.String</span></span>

## <span data-ttu-id="31227-126">輸出</span><span class="sxs-lookup"><span data-stu-id="31227-126">OUTPUTS</span></span>

### <span data-ttu-id="31227-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="31227-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="31227-128">筆記</span><span class="sxs-lookup"><span data-stu-id="31227-128">NOTES</span></span>

## <span data-ttu-id="31227-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="31227-129">RELATED LINKS</span></span>

[<span data-ttu-id="31227-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="31227-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="31227-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="31227-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="31227-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="31227-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


