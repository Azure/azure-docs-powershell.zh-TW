---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 26808bd3db72f8618505045b2b20f6d0b56806da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907389"
---
# <span data-ttu-id="d226b-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d226b-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="d226b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d226b-102">SYNOPSIS</span></span>
<span data-ttu-id="d226b-103">獲得 Stream Analytics 工作資訊。</span><span class="sxs-lookup"><span data-stu-id="d226b-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="d226b-104">語法</span><span class="sxs-lookup"><span data-stu-id="d226b-104">SYNTAX</span></span>

### <span data-ttu-id="d226b-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d226b-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d226b-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="d226b-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d226b-107">描述</span><span class="sxs-lookup"><span data-stu-id="d226b-107">DESCRIPTION</span></span>
<span data-ttu-id="d226b-108">**Get-AzStreamAnalyticsJob** Cmdlet 會列出 Azure 訂閱或指定資源群組中定義的所有 Stream Analytics 工作，或取得資源群組中特定工作的工作資訊。</span><span class="sxs-lookup"><span data-stu-id="d226b-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="d226b-109">例子</span><span class="sxs-lookup"><span data-stu-id="d226b-109">EXAMPLES</span></span>

### <span data-ttu-id="d226b-110">範例 1：取得訂閱中所有工作的資訊</span><span class="sxs-lookup"><span data-stu-id="d226b-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="d226b-111">此命令會返回 Azure 訂閱中所有 Stream Analytics 工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="d226b-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="d226b-112">範例 2：取得資源群組中所有工作的資訊</span><span class="sxs-lookup"><span data-stu-id="d226b-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="d226b-113">此命令會返回資源群組 StreamAnalytics-Default-West-US 中所有 Stream Analytics 工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="d226b-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="d226b-114">範例 3：取得資源群組中特定工作的資訊</span><span class="sxs-lookup"><span data-stu-id="d226b-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="d226b-115">此命令會返回資源群組 StreamAnalytics-Default-West-US 中 Stream Analytics 工作 StreamingJob 的資訊。</span><span class="sxs-lookup"><span data-stu-id="d226b-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="d226b-116">參數</span><span class="sxs-lookup"><span data-stu-id="d226b-116">PARAMETERS</span></span>

### <span data-ttu-id="d226b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d226b-117">-DefaultProfile</span></span>
<span data-ttu-id="d226b-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d226b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d226b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d226b-119">-Name</span></span>
<span data-ttu-id="d226b-120">指定要取回的 Azure Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="d226b-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d226b-121">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="d226b-121">-NoExpand</span></span>
<span data-ttu-id="d226b-122">表示 Cmdlet 會取回 Azure Stream Analytics 工作，但不會返回其輸入、輸出和轉換的資訊。</span><span class="sxs-lookup"><span data-stu-id="d226b-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="d226b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d226b-123">-ResourceGroupName</span></span>
<span data-ttu-id="d226b-124">指定 Azure Stream Analytics 工作所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d226b-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d226b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d226b-125">CommonParameters</span></span>
<span data-ttu-id="d226b-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d226b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d226b-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d226b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d226b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="d226b-128">INPUTS</span></span>

### <span data-ttu-id="d226b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d226b-129">System.String</span></span>

### <span data-ttu-id="d226b-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d226b-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d226b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d226b-131">OUTPUTS</span></span>

### <span data-ttu-id="d226b-132">Microsoft.Azure.Commands.StreamAnalytics.models.PSJob</span><span class="sxs-lookup"><span data-stu-id="d226b-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="d226b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d226b-133">NOTES</span></span>

## <span data-ttu-id="d226b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d226b-134">RELATED LINKS</span></span>

[<span data-ttu-id="d226b-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d226b-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="d226b-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d226b-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="d226b-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d226b-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="d226b-138">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d226b-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


