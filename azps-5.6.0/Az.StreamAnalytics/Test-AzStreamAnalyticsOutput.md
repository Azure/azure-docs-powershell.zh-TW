---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 28a595b3e63a01439417ed07f6fd47c1cfc40a79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909413"
---
# <span data-ttu-id="e5a14-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e5a14-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="e5a14-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e5a14-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a14-103">測試輸出的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="e5a14-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="e5a14-104">語法</span><span class="sxs-lookup"><span data-stu-id="e5a14-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5a14-105">描述</span><span class="sxs-lookup"><span data-stu-id="e5a14-105">DESCRIPTION</span></span>
<span data-ttu-id="e5a14-106">**Test-AzStreamAnalyticsOutput** Cmdlet 會測試 Stream Analytics 連接至輸出的能力。</span><span class="sxs-lookup"><span data-stu-id="e5a14-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="e5a14-107">例子</span><span class="sxs-lookup"><span data-stu-id="e5a14-107">EXAMPLES</span></span>

### <span data-ttu-id="e5a14-108">範例 1：測試輸出的連接狀態</span><span class="sxs-lookup"><span data-stu-id="e5a14-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="e5a14-109">這會測試 StreamingJob 中輸出輸出的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="e5a14-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="e5a14-110">參數</span><span class="sxs-lookup"><span data-stu-id="e5a14-110">PARAMETERS</span></span>

### <span data-ttu-id="e5a14-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a14-111">-DefaultProfile</span></span>
<span data-ttu-id="e5a14-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5a14-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5a14-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="e5a14-113">-JobName</span></span>
<span data-ttu-id="e5a14-114">指定您想要的 Azure Stream Analytics 輸出所屬的 Azure Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="e5a14-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="e5a14-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5a14-115">-Name</span></span>
<span data-ttu-id="e5a14-116">指定要測試的 Azure Stream Analytics 輸出名稱。</span><span class="sxs-lookup"><span data-stu-id="e5a14-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="e5a14-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5a14-117">-ResourceGroupName</span></span>
<span data-ttu-id="e5a14-118">指定 Azure Stream Analytics 輸出所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e5a14-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="e5a14-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a14-119">CommonParameters</span></span>
<span data-ttu-id="e5a14-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e5a14-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a14-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e5a14-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a14-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e5a14-122">INPUTS</span></span>

### <span data-ttu-id="e5a14-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e5a14-123">System.String</span></span>

## <span data-ttu-id="e5a14-124">輸出</span><span class="sxs-lookup"><span data-stu-id="e5a14-124">OUTPUTS</span></span>

### <span data-ttu-id="e5a14-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e5a14-125">System.Boolean</span></span>

## <span data-ttu-id="e5a14-126">筆記</span><span class="sxs-lookup"><span data-stu-id="e5a14-126">NOTES</span></span>

## <span data-ttu-id="e5a14-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5a14-127">RELATED LINKS</span></span>

[<span data-ttu-id="e5a14-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e5a14-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="e5a14-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e5a14-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="e5a14-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e5a14-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


