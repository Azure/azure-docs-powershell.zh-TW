---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d45a46cd0ff38f925a218c2bbab6edf70b97a4ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904797"
---
# <span data-ttu-id="db5b1-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="db5b1-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="db5b1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="db5b1-102">SYNOPSIS</span></span>
<span data-ttu-id="db5b1-103">測試 Stream Analytics 是否可以連接到函數。</span><span class="sxs-lookup"><span data-stu-id="db5b1-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="db5b1-104">語法</span><span class="sxs-lookup"><span data-stu-id="db5b1-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db5b1-105">描述</span><span class="sxs-lookup"><span data-stu-id="db5b1-105">DESCRIPTION</span></span>
<span data-ttu-id="db5b1-106">**Test-AzStreamAnalytics Functiondlet 會** 測試 Azure Stream Analytics 是否可以連接到函數。</span><span class="sxs-lookup"><span data-stu-id="db5b1-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="db5b1-107">例子</span><span class="sxs-lookup"><span data-stu-id="db5b1-107">EXAMPLES</span></span>

### <span data-ttu-id="db5b1-108">範例 1：測試 Stream Analytics 函數</span><span class="sxs-lookup"><span data-stu-id="db5b1-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="db5b1-109">此命令會測試名為 StreamJob22 的工作中名為 ScoreTweet 的函數之連接狀態。</span><span class="sxs-lookup"><span data-stu-id="db5b1-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="db5b1-110">參數</span><span class="sxs-lookup"><span data-stu-id="db5b1-110">PARAMETERS</span></span>

### <span data-ttu-id="db5b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db5b1-111">-DefaultProfile</span></span>
<span data-ttu-id="db5b1-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="db5b1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db5b1-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="db5b1-113">-JobName</span></span>
<span data-ttu-id="db5b1-114">指定函數所屬的 Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="db5b1-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="db5b1-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="db5b1-115">-Name</span></span>
<span data-ttu-id="db5b1-116">指定此 Cmdlet 測試的 Stream Analytics 函數名稱。</span><span class="sxs-lookup"><span data-stu-id="db5b1-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="db5b1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db5b1-117">-ResourceGroupName</span></span>
<span data-ttu-id="db5b1-118">指定 Stream Analytics 函數所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="db5b1-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="db5b1-119">此 Cmdlet 會測試此參數指定之資源群組中的函數。</span><span class="sxs-lookup"><span data-stu-id="db5b1-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="db5b1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db5b1-120">CommonParameters</span></span>
<span data-ttu-id="db5b1-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="db5b1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db5b1-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="db5b1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db5b1-123">輸入</span><span class="sxs-lookup"><span data-stu-id="db5b1-123">INPUTS</span></span>

### <span data-ttu-id="db5b1-124">System.String</span><span class="sxs-lookup"><span data-stu-id="db5b1-124">System.String</span></span>

## <span data-ttu-id="db5b1-125">輸出</span><span class="sxs-lookup"><span data-stu-id="db5b1-125">OUTPUTS</span></span>

### <span data-ttu-id="db5b1-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db5b1-126">System.Boolean</span></span>

## <span data-ttu-id="db5b1-127">筆記</span><span class="sxs-lookup"><span data-stu-id="db5b1-127">NOTES</span></span>

## <span data-ttu-id="db5b1-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="db5b1-128">RELATED LINKS</span></span>

[<span data-ttu-id="db5b1-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="db5b1-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="db5b1-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="db5b1-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="db5b1-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="db5b1-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


