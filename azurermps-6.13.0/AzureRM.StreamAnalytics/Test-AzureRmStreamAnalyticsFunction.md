---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: c62d829da193ae36f10a64149260cf34c6bc20ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454467"
---
# <span data-ttu-id="1197b-101">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1197b-101">Test-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="1197b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1197b-102">SYNOPSIS</span></span>
<span data-ttu-id="1197b-103">測試資料流程分析是否可連線至函數。</span><span class="sxs-lookup"><span data-stu-id="1197b-103">Tests whether Stream Analytics can connect to a function.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1197b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1197b-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1197b-105">說明</span><span class="sxs-lookup"><span data-stu-id="1197b-105">DESCRIPTION</span></span>
<span data-ttu-id="1197b-106">**AzureRmStreamAnalyticsFunction** Cmdlet 會測試 Azure 串流分析是否可連線至函數。</span><span class="sxs-lookup"><span data-stu-id="1197b-106">The **Test-AzureRmStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="1197b-107">示例</span><span class="sxs-lookup"><span data-stu-id="1197b-107">EXAMPLES</span></span>

### <span data-ttu-id="1197b-108">範例1：測試資料流程分析函數</span><span class="sxs-lookup"><span data-stu-id="1197b-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="1197b-109">這個命令會在名為 StreamJob22 的作業中測試名為 ScoreTweet 的函數的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="1197b-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="1197b-110">參數</span><span class="sxs-lookup"><span data-stu-id="1197b-110">PARAMETERS</span></span>

### <span data-ttu-id="1197b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1197b-111">-DefaultProfile</span></span>
<span data-ttu-id="1197b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1197b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1197b-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="1197b-113">-JobName</span></span>
<span data-ttu-id="1197b-114">指定函數所屬的資料流程分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="1197b-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="1197b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1197b-115">-Name</span></span>
<span data-ttu-id="1197b-116">指定此 Cmdlet 測試的資料流程分析函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="1197b-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="1197b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1197b-117">-ResourceGroupName</span></span>
<span data-ttu-id="1197b-118">指定 Stream Analytics 函數所歸屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1197b-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="1197b-119">這個 Cmdlet 會測試此參數指定之資源群組中的函數。</span><span class="sxs-lookup"><span data-stu-id="1197b-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1197b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1197b-120">CommonParameters</span></span>
<span data-ttu-id="1197b-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1197b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1197b-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1197b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1197b-123">輸入</span><span class="sxs-lookup"><span data-stu-id="1197b-123">INPUTS</span></span>

### <span data-ttu-id="1197b-124">System.object</span><span class="sxs-lookup"><span data-stu-id="1197b-124">System.String</span></span>

## <span data-ttu-id="1197b-125">輸出</span><span class="sxs-lookup"><span data-stu-id="1197b-125">OUTPUTS</span></span>

### <span data-ttu-id="1197b-126">System.object</span><span class="sxs-lookup"><span data-stu-id="1197b-126">System.Boolean</span></span>

## <span data-ttu-id="1197b-127">筆記</span><span class="sxs-lookup"><span data-stu-id="1197b-127">NOTES</span></span>

## <span data-ttu-id="1197b-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="1197b-128">RELATED LINKS</span></span>

[<span data-ttu-id="1197b-129">AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1197b-129">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="1197b-130">新-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1197b-130">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="1197b-131">移除-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1197b-131">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)


