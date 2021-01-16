---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447980"
---
# <span data-ttu-id="f3bd5-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f3bd5-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="f3bd5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="f3bd5-103">取得串流分析作業資訊。</span><span class="sxs-lookup"><span data-stu-id="f3bd5-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="f3bd5-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3bd5-104">SYNTAX</span></span>

### <span data-ttu-id="f3bd5-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f3bd5-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3bd5-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="f3bd5-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3bd5-107">說明</span><span class="sxs-lookup"><span data-stu-id="f3bd5-107">DESCRIPTION</span></span>
<span data-ttu-id="f3bd5-108">**AzStreamAnalyticsJob** Cmdlet 會列出 Azure 訂閱或指定資源群組中定義的所有串流分析作業，或取得資源群組中特定作業的工作資訊。</span><span class="sxs-lookup"><span data-stu-id="f3bd5-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="f3bd5-109">示例</span><span class="sxs-lookup"><span data-stu-id="f3bd5-109">EXAMPLES</span></span>

### <span data-ttu-id="f3bd5-110">範例1：取得訂閱中所有作業的相關資訊</span><span class="sxs-lookup"><span data-stu-id="f3bd5-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="f3bd5-111">這個命令會傳回有關 Azure 訂閱中所有串流分析作業的資訊。</span><span class="sxs-lookup"><span data-stu-id="f3bd5-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="f3bd5-112">範例2：取得資源群組中所有工作的相關資訊</span><span class="sxs-lookup"><span data-stu-id="f3bd5-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="f3bd5-113">這個命令會傳回有關 [資源群組 StreamAnalytics] 中所有串流分析作業的資訊-預設值-西部-美國。</span><span class="sxs-lookup"><span data-stu-id="f3bd5-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="f3bd5-114">範例3：取得資源群組中特定作業的相關資訊</span><span class="sxs-lookup"><span data-stu-id="f3bd5-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="f3bd5-115">這個命令會傳回有關 [資源] 群組中 [資料流程分析作業 StreamingJob] 的資訊 StreamAnalytics-預設值-西部-美國。</span><span class="sxs-lookup"><span data-stu-id="f3bd5-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="f3bd5-116">參數</span><span class="sxs-lookup"><span data-stu-id="f3bd5-116">PARAMETERS</span></span>

### <span data-ttu-id="f3bd5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3bd5-117">-DefaultProfile</span></span>
<span data-ttu-id="f3bd5-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3bd5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3bd5-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3bd5-119">-Name</span></span>
<span data-ttu-id="f3bd5-120">指定要檢索之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3bd5-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

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

### <span data-ttu-id="f3bd5-121">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="f3bd5-121">-NoExpand</span></span>
<span data-ttu-id="f3bd5-122">指示 Cmdlet 將會檢索 Azure 資料流程分析作業，但不會傳回其輸入、輸出及轉換的資訊。</span><span class="sxs-lookup"><span data-stu-id="f3bd5-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="f3bd5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3bd5-123">-ResourceGroupName</span></span>
<span data-ttu-id="f3bd5-124">指定 Azure 資料流程分析作業所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3bd5-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="f3bd5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3bd5-125">CommonParameters</span></span>
<span data-ttu-id="f3bd5-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3bd5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3bd5-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3bd5-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3bd5-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f3bd5-128">INPUTS</span></span>

### <span data-ttu-id="f3bd5-129">System.object</span><span class="sxs-lookup"><span data-stu-id="f3bd5-129">System.String</span></span>

### <span data-ttu-id="f3bd5-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f3bd5-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f3bd5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f3bd5-131">OUTPUTS</span></span>

### <span data-ttu-id="f3bd5-132">PSJob 中的 StreamAnalytics。</span><span class="sxs-lookup"><span data-stu-id="f3bd5-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="f3bd5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f3bd5-133">NOTES</span></span>

## <span data-ttu-id="f3bd5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3bd5-134">RELATED LINKS</span></span>

[<span data-ttu-id="f3bd5-135">新-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f3bd5-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f3bd5-136">移除-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f3bd5-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f3bd5-137">開始-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f3bd5-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f3bd5-138">停止 AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f3bd5-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


