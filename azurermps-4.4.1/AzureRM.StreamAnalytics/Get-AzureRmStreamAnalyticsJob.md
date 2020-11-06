---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 7b1130d222e36d53fbef1dcbb60f6d74615c5b11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449474"
---
# <span data-ttu-id="d2d4c-101">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d2d4c-101">Get-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="d2d4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="d2d4c-103">取得串流分析作業資訊。</span><span class="sxs-lookup"><span data-stu-id="d2d4c-103">Gets Stream Analytics jobs information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2d4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2d4c-104">SYNTAX</span></span>

### <span data-ttu-id="d2d4c-105">在指定資源群組中的串流分析物件</span><span class="sxs-lookup"><span data-stu-id="d2d4c-105">For stream analytics objects in the given resource group</span></span>
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2d4c-106">針對指定訂閱中的串流分析物件</span><span class="sxs-lookup"><span data-stu-id="d2d4c-106">For stream analytics objects in the given subscription</span></span>
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2d4c-107">說明</span><span class="sxs-lookup"><span data-stu-id="d2d4c-107">DESCRIPTION</span></span>
<span data-ttu-id="d2d4c-108">**AzureRmStreamAnalyticsJob** Cmdlet 會列出 Azure 訂閱或指定資源群組中定義的所有串流分析作業，或取得資源群組中特定作業的工作資訊。</span><span class="sxs-lookup"><span data-stu-id="d2d4c-108">The **Get-AzureRmStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="d2d4c-109">示例</span><span class="sxs-lookup"><span data-stu-id="d2d4c-109">EXAMPLES</span></span>

### <span data-ttu-id="d2d4c-110">範例1：取得訂閱中所有作業的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d2d4c-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

<span data-ttu-id="d2d4c-111">這個命令會傳回有關 Azure 訂閱中所有串流分析作業的資訊。</span><span class="sxs-lookup"><span data-stu-id="d2d4c-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="d2d4c-112">範例2：取得資源群組中所有工作的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d2d4c-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="d2d4c-113">這個命令會傳回有關 [資源群組 StreamAnalytics] 中所有串流分析作業的資訊-預設值-西部-美國。</span><span class="sxs-lookup"><span data-stu-id="d2d4c-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="d2d4c-114">範例3：取得資源群組中特定作業的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d2d4c-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="d2d4c-115">這個命令會傳回有關 [資源] 群組中 [資料流程分析作業 StreamingJob] 的資訊 StreamAnalytics-預設值-西部-美國。</span><span class="sxs-lookup"><span data-stu-id="d2d4c-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="d2d4c-116">參數</span><span class="sxs-lookup"><span data-stu-id="d2d4c-116">PARAMETERS</span></span>

### <span data-ttu-id="d2d4c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2d4c-117">-Name</span></span>
<span data-ttu-id="d2d4c-118">指定要檢索之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2d4c-118">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: For stream analytics objects in the given resource group
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2d4c-119">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="d2d4c-119">-NoExpand</span></span>
<span data-ttu-id="d2d4c-120">指示 Cmdlet 將會檢索 Azure 資料流程分析作業，但不會傳回其輸入、輸出及轉換的資訊。</span><span class="sxs-lookup"><span data-stu-id="d2d4c-120">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="d2d4c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2d4c-121">-ResourceGroupName</span></span>
<span data-ttu-id="d2d4c-122">指定 Azure 資料流程分析作業所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2d4c-122">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: For stream analytics objects in the given resource group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2d4c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2d4c-123">-DefaultProfile</span></span>
<span data-ttu-id="d2d4c-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2d4c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2d4c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2d4c-125">CommonParameters</span></span>
<span data-ttu-id="d2d4c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2d4c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2d4c-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2d4c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2d4c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="d2d4c-128">INPUTS</span></span>

## <span data-ttu-id="d2d4c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d2d4c-129">OUTPUTS</span></span>

### <span data-ttu-id="d2d4c-130">[System.object]. 清單 ' 1 [StreamAnalytics. PSJob，StreamAnalytics]]]]]]]]]]]]</span><span class="sxs-lookup"><span data-stu-id="d2d4c-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="d2d4c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d2d4c-131">NOTES</span></span>

## <span data-ttu-id="d2d4c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2d4c-132">RELATED LINKS</span></span>

[<span data-ttu-id="d2d4c-133">新-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d2d4c-133">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d2d4c-134">移除-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d2d4c-134">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d2d4c-135">開始-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d2d4c-135">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d2d4c-136">停止 AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d2d4c-136">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


