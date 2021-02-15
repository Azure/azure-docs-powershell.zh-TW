---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130466"
---
# <span data-ttu-id="5cb64-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5cb64-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="5cb64-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5cb64-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb64-103">測試資料流程分析是否可連線至函數。</span><span class="sxs-lookup"><span data-stu-id="5cb64-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="5cb64-104">句法</span><span class="sxs-lookup"><span data-stu-id="5cb64-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cb64-105">說明</span><span class="sxs-lookup"><span data-stu-id="5cb64-105">DESCRIPTION</span></span>
<span data-ttu-id="5cb64-106">**AzStreamAnalyticsFunction** Cmdlet 會測試 Azure 串流分析是否可連線至函數。</span><span class="sxs-lookup"><span data-stu-id="5cb64-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="5cb64-107">示例</span><span class="sxs-lookup"><span data-stu-id="5cb64-107">EXAMPLES</span></span>

### <span data-ttu-id="5cb64-108">範例1：測試資料流程分析函數</span><span class="sxs-lookup"><span data-stu-id="5cb64-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="5cb64-109">這個命令會在名為 StreamJob22 的作業中測試名為 ScoreTweet 的函數的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="5cb64-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="5cb64-110">參數</span><span class="sxs-lookup"><span data-stu-id="5cb64-110">PARAMETERS</span></span>

### <span data-ttu-id="5cb64-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb64-111">-DefaultProfile</span></span>
<span data-ttu-id="5cb64-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5cb64-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cb64-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="5cb64-113">-JobName</span></span>
<span data-ttu-id="5cb64-114">指定函數所屬的資料流程分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="5cb64-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="5cb64-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="5cb64-115">-Name</span></span>
<span data-ttu-id="5cb64-116">指定此 Cmdlet 測試的資料流程分析函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="5cb64-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="5cb64-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb64-117">-ResourceGroupName</span></span>
<span data-ttu-id="5cb64-118">指定 Stream Analytics 函數所歸屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5cb64-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="5cb64-119">這個 Cmdlet 會測試此參數指定之資源群組中的函數。</span><span class="sxs-lookup"><span data-stu-id="5cb64-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5cb64-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb64-120">CommonParameters</span></span>
<span data-ttu-id="5cb64-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5cb64-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb64-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5cb64-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb64-123">輸入</span><span class="sxs-lookup"><span data-stu-id="5cb64-123">INPUTS</span></span>

### <span data-ttu-id="5cb64-124">System.object</span><span class="sxs-lookup"><span data-stu-id="5cb64-124">System.String</span></span>

## <span data-ttu-id="5cb64-125">輸出</span><span class="sxs-lookup"><span data-stu-id="5cb64-125">OUTPUTS</span></span>

### <span data-ttu-id="5cb64-126">System.object</span><span class="sxs-lookup"><span data-stu-id="5cb64-126">System.Boolean</span></span>

## <span data-ttu-id="5cb64-127">筆記</span><span class="sxs-lookup"><span data-stu-id="5cb64-127">NOTES</span></span>

## <span data-ttu-id="5cb64-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="5cb64-128">RELATED LINKS</span></span>

[<span data-ttu-id="5cb64-129">AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5cb64-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="5cb64-130">新-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5cb64-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="5cb64-131">移除-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5cb64-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


