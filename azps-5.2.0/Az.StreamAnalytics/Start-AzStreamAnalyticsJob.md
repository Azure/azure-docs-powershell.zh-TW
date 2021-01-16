---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: 1194a730293d6f0f7b4aca58f508f808a2c6193e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283231"
---
# <span data-ttu-id="9b015-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9b015-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="9b015-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b015-102">SYNOPSIS</span></span>
<span data-ttu-id="9b015-103">啟動資料流程分析作業。</span><span class="sxs-lookup"><span data-stu-id="9b015-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="9b015-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b015-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b015-105">說明</span><span class="sxs-lookup"><span data-stu-id="9b015-105">DESCRIPTION</span></span>
<span data-ttu-id="9b015-106">**AzStreamAnalyticsJob** Cmdlet 會在 Azure 中非同步部署和啟動資料流程分析作業。</span><span class="sxs-lookup"><span data-stu-id="9b015-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="9b015-107">示例</span><span class="sxs-lookup"><span data-stu-id="9b015-107">EXAMPLES</span></span>

### <span data-ttu-id="9b015-108">範例1：啟動資料流程分析作業</span><span class="sxs-lookup"><span data-stu-id="9b015-108">Example 1: Start a Stream Analytics job</span></span>
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="9b015-109">這個命令會啟動作業 StreamingJob，並指定輸出事件資料流程應該在 timestamp 2014-03T01：00Z 啟動。</span><span class="sxs-lookup"><span data-stu-id="9b015-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="9b015-110">參數</span><span class="sxs-lookup"><span data-stu-id="9b015-110">PARAMETERS</span></span>

### <span data-ttu-id="9b015-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b015-111">-DefaultProfile</span></span>
<span data-ttu-id="9b015-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b015-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b015-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b015-113">-Name</span></span>
<span data-ttu-id="9b015-114">指定要啟動之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b015-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="9b015-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="9b015-115">-OutputStartMode</span></span>
<span data-ttu-id="9b015-116">指定作業的開始模式。</span><span class="sxs-lookup"><span data-stu-id="9b015-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="9b015-117">有效值為：</span><span class="sxs-lookup"><span data-stu-id="9b015-117">Valid values are:</span></span> 
- <span data-ttu-id="9b015-118">JobStartTime-這個值表示輸出事件資料流程的起始點應該在作業啟動時開始。</span><span class="sxs-lookup"><span data-stu-id="9b015-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="9b015-119">CustomTime-此值表示輸出事件資料流程的起始點應從在 *OutputStartTime* 參數中指定的自訂時間開始。</span><span class="sxs-lookup"><span data-stu-id="9b015-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="9b015-120">LastOutputEventTime-這個值表示輸出事件資料流程的起點應該從最後一個事件輸出時間開始。</span><span class="sxs-lookup"><span data-stu-id="9b015-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="9b015-121">如果屬性不存在，則預設值為 JobStartTime。</span><span class="sxs-lookup"><span data-stu-id="9b015-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="9b015-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="9b015-122">-OutputStartTime</span></span>
<span data-ttu-id="9b015-123">指定輸出開始時間。</span><span class="sxs-lookup"><span data-stu-id="9b015-123">Specifies the output start time.</span></span>
<span data-ttu-id="9b015-124">這個值是一個 ISO-8601 格式化的時間戳記，可指出輸出事件資料流程的起點，或 $Null 來指示每當資料流程作業啟動時，都會開始進行輸出事件資料流程。</span><span class="sxs-lookup"><span data-stu-id="9b015-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="9b015-125">如果 *OutputStartMode* 設定為 CustomTime，則這個屬性必須有值。</span><span class="sxs-lookup"><span data-stu-id="9b015-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

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

### <span data-ttu-id="9b015-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b015-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b015-127">指定 Azure 資料流程分析作業所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b015-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="9b015-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b015-128">CommonParameters</span></span>
<span data-ttu-id="9b015-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b015-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b015-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b015-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b015-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9b015-131">INPUTS</span></span>

### <span data-ttu-id="9b015-132">System.object</span><span class="sxs-lookup"><span data-stu-id="9b015-132">System.String</span></span>

### <span data-ttu-id="9b015-133">System.object Null ' 1 [CoreLib，System.object = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9b015-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9b015-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9b015-134">OUTPUTS</span></span>

### <span data-ttu-id="9b015-135">System.object</span><span class="sxs-lookup"><span data-stu-id="9b015-135">System.Boolean</span></span>

## <span data-ttu-id="9b015-136">筆記</span><span class="sxs-lookup"><span data-stu-id="9b015-136">NOTES</span></span>

## <span data-ttu-id="9b015-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b015-137">RELATED LINKS</span></span>

[<span data-ttu-id="9b015-138">AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9b015-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="9b015-139">新-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9b015-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="9b015-140">移除-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9b015-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="9b015-141">停止 AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9b015-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


