---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/start-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 20bd934a35fdf0cf907e83f22c8148fdfe5425db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454468"
---
# <span data-ttu-id="6ab1b-101">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6ab1b-101">Start-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="6ab1b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ab1b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab1b-103">啟動資料流程分析作業。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-103">Starts a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ab1b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ab1b-104">SYNTAX</span></span>

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ab1b-105">說明</span><span class="sxs-lookup"><span data-stu-id="6ab1b-105">DESCRIPTION</span></span>
<span data-ttu-id="6ab1b-106">**AzureRmStreamAnalyticsJob** Cmdlet 會在 Azure 中非同步部署和啟動資料流程分析作業。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-106">The **Start-AzureRmStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="6ab1b-107">示例</span><span class="sxs-lookup"><span data-stu-id="6ab1b-107">EXAMPLES</span></span>

### <span data-ttu-id="6ab1b-108">範例1：啟動資料流程分析作業</span><span class="sxs-lookup"><span data-stu-id="6ab1b-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="6ab1b-109">這個命令會啟動作業 StreamingJob，並指定輸出事件資料流程應該在 timestamp 2014-03T01：00Z 啟動。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="6ab1b-110">參數</span><span class="sxs-lookup"><span data-stu-id="6ab1b-110">PARAMETERS</span></span>

### <span data-ttu-id="6ab1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab1b-111">-DefaultProfile</span></span>
<span data-ttu-id="6ab1b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ab1b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ab1b-113">-Name</span></span>
<span data-ttu-id="6ab1b-114">指定要啟動之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="6ab1b-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="6ab1b-115">-OutputStartMode</span></span>
<span data-ttu-id="6ab1b-116">指定作業的開始模式。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="6ab1b-117">有效值為：</span><span class="sxs-lookup"><span data-stu-id="6ab1b-117">Valid values are:</span></span> 
- <span data-ttu-id="6ab1b-118">JobStartTime-這個值表示輸出事件資料流程的起始點應該在作業啟動時開始。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="6ab1b-119">CustomTime-此值表示輸出事件資料流程的起始點應從在 *OutputStartTime* 參數中指定的自訂時間開始。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 <span data-ttu-id="6ab1b-120">--LastOutputEventTime-此值表示輸出事件資料流程的起始點應該從最後一個事件輸出時間開始。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-120">-- LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="6ab1b-121">如果屬性不存在，則預設值為 JobStartTime。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="6ab1b-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="6ab1b-122">-OutputStartTime</span></span>
<span data-ttu-id="6ab1b-123">指定輸出開始時間。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-123">Specifies the output start time.</span></span>
<span data-ttu-id="6ab1b-124">這個值是一個 ISO-8601 格式化的時間戳記，可指出輸出事件資料流程的起點，或 $Null 來指示每當資料流程作業啟動時，都會開始進行輸出事件資料流程。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="6ab1b-125">如果 *OutputStartMode* 設定為 CustomTime，則這個屬性必須有值。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab1b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ab1b-126">-ResourceGroupName</span></span>
<span data-ttu-id="6ab1b-127">指定 Azure 資料流程分析作業所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="6ab1b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab1b-128">CommonParameters</span></span>
<span data-ttu-id="6ab1b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab1b-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ab1b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab1b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="6ab1b-131">INPUTS</span></span>

### <span data-ttu-id="6ab1b-132">System.object</span><span class="sxs-lookup"><span data-stu-id="6ab1b-132">System.String</span></span>

### <span data-ttu-id="6ab1b-133">系統. Nullable "1 [[System. DateTime，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6ab1b-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6ab1b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6ab1b-134">OUTPUTS</span></span>

### <span data-ttu-id="6ab1b-135">System.object</span><span class="sxs-lookup"><span data-stu-id="6ab1b-135">System.Boolean</span></span>

## <span data-ttu-id="6ab1b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="6ab1b-136">NOTES</span></span>

## <span data-ttu-id="6ab1b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ab1b-137">RELATED LINKS</span></span>

[<span data-ttu-id="6ab1b-138">AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6ab1b-138">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="6ab1b-139">新-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6ab1b-139">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="6ab1b-140">移除-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6ab1b-140">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="6ab1b-141">停止 AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6ab1b-141">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


