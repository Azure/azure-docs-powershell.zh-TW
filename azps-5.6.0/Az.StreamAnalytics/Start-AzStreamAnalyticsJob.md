---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: cd7d6aaa9a295f888d8e765d12b4088525eff1fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912533"
---
# <span data-ttu-id="92186-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92186-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="92186-102">簡介</span><span class="sxs-lookup"><span data-stu-id="92186-102">SYNOPSIS</span></span>
<span data-ttu-id="92186-103">啟動 Stream Analytics 工作。</span><span class="sxs-lookup"><span data-stu-id="92186-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="92186-104">語法</span><span class="sxs-lookup"><span data-stu-id="92186-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92186-105">描述</span><span class="sxs-lookup"><span data-stu-id="92186-105">DESCRIPTION</span></span>
<span data-ttu-id="92186-106">**Start-AzStreamAnalyticsJob** Cmdlet 會非同步部署並開始 Azure 中的 Stream Analytics 工作。</span><span class="sxs-lookup"><span data-stu-id="92186-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="92186-107">例子</span><span class="sxs-lookup"><span data-stu-id="92186-107">EXAMPLES</span></span>

### <span data-ttu-id="92186-108">範例 1：啟動 Stream Analytics 工作</span><span class="sxs-lookup"><span data-stu-id="92186-108">Example 1: Start a Stream Analytics job</span></span>
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="92186-109">此命令會啟動 Job StreamingJob，並指定輸出事件串流應在時間戳記 2014-07-03T01：00Z 開始。</span><span class="sxs-lookup"><span data-stu-id="92186-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="92186-110">參數</span><span class="sxs-lookup"><span data-stu-id="92186-110">PARAMETERS</span></span>

### <span data-ttu-id="92186-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92186-111">-DefaultProfile</span></span>
<span data-ttu-id="92186-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="92186-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92186-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="92186-113">-Name</span></span>
<span data-ttu-id="92186-114">指定要啟動的 Azure Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="92186-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="92186-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="92186-115">-OutputStartMode</span></span>
<span data-ttu-id="92186-116">指定工作的開始模式。</span><span class="sxs-lookup"><span data-stu-id="92186-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="92186-117">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="92186-117">Valid values are:</span></span> 
- <span data-ttu-id="92186-118">JobStartTime - 此值表示工作開始時，輸出事件串流的起點應該會啟動。</span><span class="sxs-lookup"><span data-stu-id="92186-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="92186-119">CustomTime - 此值表示輸出事件串流的起點應該從 *OutputStartTime* 參數指定的自訂時間開始。</span><span class="sxs-lookup"><span data-stu-id="92186-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="92186-120">LastOutputEventTime - 此值表示輸出事件串流的起點應從最後一個事件輸出時間開始。</span><span class="sxs-lookup"><span data-stu-id="92186-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="92186-121">如果屬性不存在，預設值為 JobStartTime。</span><span class="sxs-lookup"><span data-stu-id="92186-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="92186-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="92186-122">-OutputStartTime</span></span>
<span data-ttu-id="92186-123">指定輸出開始時間。</span><span class="sxs-lookup"><span data-stu-id="92186-123">Specifies the output start time.</span></span>
<span data-ttu-id="92186-124">此值是 ISO-8601 格式化的時間戳記，指出輸出事件串流的起點，或 $Null 表示輸出事件串流在串流作業開始時會啟動。</span><span class="sxs-lookup"><span data-stu-id="92186-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="92186-125">如果 *OutputStartMode* 設定為 CustomTime，則此屬性必須有值。</span><span class="sxs-lookup"><span data-stu-id="92186-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

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

### <span data-ttu-id="92186-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92186-126">-ResourceGroupName</span></span>
<span data-ttu-id="92186-127">指定 Azure Stream Analytics 工作所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="92186-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="92186-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92186-128">CommonParameters</span></span>
<span data-ttu-id="92186-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="92186-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92186-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="92186-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92186-131">輸入</span><span class="sxs-lookup"><span data-stu-id="92186-131">INPUTS</span></span>

### <span data-ttu-id="92186-132">System.String</span><span class="sxs-lookup"><span data-stu-id="92186-132">System.String</span></span>

### <span data-ttu-id="92186-133">System.Nullable'1[[System.DateTime， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="92186-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="92186-134">輸出</span><span class="sxs-lookup"><span data-stu-id="92186-134">OUTPUTS</span></span>

### <span data-ttu-id="92186-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92186-135">System.Boolean</span></span>

## <span data-ttu-id="92186-136">筆記</span><span class="sxs-lookup"><span data-stu-id="92186-136">NOTES</span></span>

## <span data-ttu-id="92186-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="92186-137">RELATED LINKS</span></span>

[<span data-ttu-id="92186-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92186-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="92186-139">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92186-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="92186-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92186-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="92186-141">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92186-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


