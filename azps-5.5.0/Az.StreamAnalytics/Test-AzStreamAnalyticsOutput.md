---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 69e9d06a790fa473a278e50e79ad90be93f0527c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130459"
---
# <span data-ttu-id="813ad-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="813ad-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="813ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="813ad-102">SYNOPSIS</span></span>
<span data-ttu-id="813ad-103">測試輸出的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="813ad-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="813ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="813ad-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="813ad-105">說明</span><span class="sxs-lookup"><span data-stu-id="813ad-105">DESCRIPTION</span></span>
<span data-ttu-id="813ad-106">**AzStreamAnalyticsOutput** Cmdlet 會測試資料流程分析程式連接到輸出的能力。</span><span class="sxs-lookup"><span data-stu-id="813ad-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="813ad-107">示例</span><span class="sxs-lookup"><span data-stu-id="813ad-107">EXAMPLES</span></span>

### <span data-ttu-id="813ad-108">範例1：測試輸出的線上狀態</span><span class="sxs-lookup"><span data-stu-id="813ad-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="813ad-109">這會測試 StreamingJob 中輸出輸出的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="813ad-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="813ad-110">參數</span><span class="sxs-lookup"><span data-stu-id="813ad-110">PARAMETERS</span></span>

### <span data-ttu-id="813ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="813ad-111">-DefaultProfile</span></span>
<span data-ttu-id="813ad-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="813ad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="813ad-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="813ad-113">-JobName</span></span>
<span data-ttu-id="813ad-114">指定所要的 Azure 資料流程分析輸出所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="813ad-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="813ad-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="813ad-115">-Name</span></span>
<span data-ttu-id="813ad-116">指定要測試的 Azure 資料流程分析輸出的名稱。</span><span class="sxs-lookup"><span data-stu-id="813ad-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="813ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="813ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="813ad-118">指定 Azure 資料流程分析輸出所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="813ad-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="813ad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813ad-119">CommonParameters</span></span>
<span data-ttu-id="813ad-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="813ad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813ad-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="813ad-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813ad-122">輸入</span><span class="sxs-lookup"><span data-stu-id="813ad-122">INPUTS</span></span>

### <span data-ttu-id="813ad-123">System.object</span><span class="sxs-lookup"><span data-stu-id="813ad-123">System.String</span></span>

## <span data-ttu-id="813ad-124">輸出</span><span class="sxs-lookup"><span data-stu-id="813ad-124">OUTPUTS</span></span>

### <span data-ttu-id="813ad-125">System.object</span><span class="sxs-lookup"><span data-stu-id="813ad-125">System.Boolean</span></span>

## <span data-ttu-id="813ad-126">筆記</span><span class="sxs-lookup"><span data-stu-id="813ad-126">NOTES</span></span>

## <span data-ttu-id="813ad-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="813ad-127">RELATED LINKS</span></span>

[<span data-ttu-id="813ad-128">AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="813ad-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="813ad-129">新-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="813ad-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="813ad-130">移除-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="813ad-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


