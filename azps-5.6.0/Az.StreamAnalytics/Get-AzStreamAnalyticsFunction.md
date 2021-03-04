---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 681782db0e1621e8d1126ca1f3425ce87e8e30d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907402"
---
# <span data-ttu-id="4dc70-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4dc70-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="4dc70-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4dc70-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc70-103">在 Stream Analytics 工作中獲取函數。</span><span class="sxs-lookup"><span data-stu-id="4dc70-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="4dc70-104">語法</span><span class="sxs-lookup"><span data-stu-id="4dc70-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dc70-105">描述</span><span class="sxs-lookup"><span data-stu-id="4dc70-105">DESCRIPTION</span></span>
<span data-ttu-id="4dc70-106">**Get-AzStreamAnalytics Functiondlet** 會取得 Azure Stream Analytics 工作所定義之函數的清單，或特定函數的資訊。</span><span class="sxs-lookup"><span data-stu-id="4dc70-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="4dc70-107">例子</span><span class="sxs-lookup"><span data-stu-id="4dc70-107">EXAMPLES</span></span>

### <span data-ttu-id="4dc70-108">範例 1：取得所有 Stream Analytics 函數</span><span class="sxs-lookup"><span data-stu-id="4dc70-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="4dc70-109">此命令會獲得在名為 StreamJob22 的工作上定義的函數。</span><span class="sxs-lookup"><span data-stu-id="4dc70-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="4dc70-110">範例 2：取得特定的 Stream Analytics 函數</span><span class="sxs-lookup"><span data-stu-id="4dc70-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="4dc70-111">此命令會取得名稱為 ScoreTweet 的函數在名為 StreamJob22 的工作上定義的資訊。</span><span class="sxs-lookup"><span data-stu-id="4dc70-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="4dc70-112">參數</span><span class="sxs-lookup"><span data-stu-id="4dc70-112">PARAMETERS</span></span>

### <span data-ttu-id="4dc70-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc70-113">-DefaultProfile</span></span>
<span data-ttu-id="4dc70-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4dc70-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dc70-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="4dc70-115">-JobName</span></span>
<span data-ttu-id="4dc70-116">指定函數所屬的 Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="4dc70-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="4dc70-117">此 Cmdlet 會針對此參數指定的工作獲得函數。</span><span class="sxs-lookup"><span data-stu-id="4dc70-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="4dc70-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="4dc70-118">-Name</span></span>
<span data-ttu-id="4dc70-119">指定此 Cmdlet 所獲得 Stream Analytics 函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="4dc70-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4dc70-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dc70-120">-ResourceGroupName</span></span>
<span data-ttu-id="4dc70-121">指定 Stream Analytics 函數所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4dc70-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="4dc70-122">此 Cmdlet 會針對此參數指定的群組獲得函數。</span><span class="sxs-lookup"><span data-stu-id="4dc70-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4dc70-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc70-123">CommonParameters</span></span>
<span data-ttu-id="4dc70-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4dc70-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc70-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4dc70-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc70-126">輸入</span><span class="sxs-lookup"><span data-stu-id="4dc70-126">INPUTS</span></span>

### <span data-ttu-id="4dc70-127">System.String</span><span class="sxs-lookup"><span data-stu-id="4dc70-127">System.String</span></span>

## <span data-ttu-id="4dc70-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4dc70-128">OUTPUTS</span></span>

### <span data-ttu-id="4dc70-129">Microsoft.Azure.Commands.StreamAnalytics.models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="4dc70-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="4dc70-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4dc70-130">NOTES</span></span>

## <span data-ttu-id="4dc70-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4dc70-131">RELATED LINKS</span></span>

[<span data-ttu-id="4dc70-132">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4dc70-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="4dc70-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4dc70-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="4dc70-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4dc70-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


