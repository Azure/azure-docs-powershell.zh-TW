---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: ba4eee78732e4217a6652fb6770ab5df8de05174
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797825"
---
# <span data-ttu-id="33aee-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="33aee-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="33aee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33aee-102">SYNOPSIS</span></span>
<span data-ttu-id="33aee-103">測試輸出的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="33aee-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="33aee-104">句法</span><span class="sxs-lookup"><span data-stu-id="33aee-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33aee-105">說明</span><span class="sxs-lookup"><span data-stu-id="33aee-105">DESCRIPTION</span></span>
<span data-ttu-id="33aee-106">**AzStreamAnalyticsOutput** Cmdlet 會測試資料流程分析程式連接到輸出的能力。</span><span class="sxs-lookup"><span data-stu-id="33aee-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="33aee-107">示例</span><span class="sxs-lookup"><span data-stu-id="33aee-107">EXAMPLES</span></span>

### <span data-ttu-id="33aee-108">範例1：測試輸出的線上狀態</span><span class="sxs-lookup"><span data-stu-id="33aee-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="33aee-109">這會測試 StreamingJob 中輸出輸出的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="33aee-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="33aee-110">參數</span><span class="sxs-lookup"><span data-stu-id="33aee-110">PARAMETERS</span></span>

### <span data-ttu-id="33aee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33aee-111">-DefaultProfile</span></span>
<span data-ttu-id="33aee-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="33aee-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33aee-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="33aee-113">-JobName</span></span>
<span data-ttu-id="33aee-114">指定所要的 Azure 資料流程分析輸出所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="33aee-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="33aee-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="33aee-115">-Name</span></span>
<span data-ttu-id="33aee-116">指定要測試的 Azure 資料流程分析輸出的名稱。</span><span class="sxs-lookup"><span data-stu-id="33aee-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="33aee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33aee-117">-ResourceGroupName</span></span>
<span data-ttu-id="33aee-118">指定 Azure 資料流程分析輸出所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="33aee-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="33aee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33aee-119">CommonParameters</span></span>
<span data-ttu-id="33aee-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33aee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33aee-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="33aee-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33aee-122">輸入</span><span class="sxs-lookup"><span data-stu-id="33aee-122">INPUTS</span></span>

### <span data-ttu-id="33aee-123">System.object</span><span class="sxs-lookup"><span data-stu-id="33aee-123">System.String</span></span>

## <span data-ttu-id="33aee-124">輸出</span><span class="sxs-lookup"><span data-stu-id="33aee-124">OUTPUTS</span></span>

### <span data-ttu-id="33aee-125">System.object</span><span class="sxs-lookup"><span data-stu-id="33aee-125">System.Boolean</span></span>

## <span data-ttu-id="33aee-126">筆記</span><span class="sxs-lookup"><span data-stu-id="33aee-126">NOTES</span></span>

## <span data-ttu-id="33aee-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="33aee-127">RELATED LINKS</span></span>

[<span data-ttu-id="33aee-128">AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="33aee-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="33aee-129">新-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="33aee-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="33aee-130">移除-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="33aee-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


