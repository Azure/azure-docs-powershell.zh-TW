---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: e353e1e8be820c96f1eb1381274a8e245f542947
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283219"
---
# <span data-ttu-id="4de58-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4de58-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="4de58-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4de58-102">SYNOPSIS</span></span>
<span data-ttu-id="4de58-103">測試輸入的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="4de58-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="4de58-104">句法</span><span class="sxs-lookup"><span data-stu-id="4de58-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4de58-105">說明</span><span class="sxs-lookup"><span data-stu-id="4de58-105">DESCRIPTION</span></span>
<span data-ttu-id="4de58-106">**AzStreamAnalyticsInput** Cmdlet 會測試資料流程分析程式連接至輸入的能力。</span><span class="sxs-lookup"><span data-stu-id="4de58-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="4de58-107">示例</span><span class="sxs-lookup"><span data-stu-id="4de58-107">EXAMPLES</span></span>

### <span data-ttu-id="4de58-108">範例1：測試輸入資料流程的線上狀態</span><span class="sxs-lookup"><span data-stu-id="4de58-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="4de58-109">這會測試 StreamingJob 中輸入 EntryStream 的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="4de58-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="4de58-110">參數</span><span class="sxs-lookup"><span data-stu-id="4de58-110">PARAMETERS</span></span>

### <span data-ttu-id="4de58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de58-111">-DefaultProfile</span></span>
<span data-ttu-id="4de58-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4de58-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4de58-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="4de58-113">-JobName</span></span>
<span data-ttu-id="4de58-114">指定 Azure 串流分析輸入所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="4de58-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="4de58-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="4de58-115">-Name</span></span>
<span data-ttu-id="4de58-116">指定要測試的 Azure 資料流程分析輸入的名稱。</span><span class="sxs-lookup"><span data-stu-id="4de58-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="4de58-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de58-117">-ResourceGroupName</span></span>
<span data-ttu-id="4de58-118">指定 Azure 串流分析輸入所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4de58-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="4de58-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de58-119">CommonParameters</span></span>
<span data-ttu-id="4de58-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4de58-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de58-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4de58-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de58-122">輸入</span><span class="sxs-lookup"><span data-stu-id="4de58-122">INPUTS</span></span>

### <span data-ttu-id="4de58-123">System.object</span><span class="sxs-lookup"><span data-stu-id="4de58-123">System.String</span></span>

## <span data-ttu-id="4de58-124">輸出</span><span class="sxs-lookup"><span data-stu-id="4de58-124">OUTPUTS</span></span>

### <span data-ttu-id="4de58-125">System.object</span><span class="sxs-lookup"><span data-stu-id="4de58-125">System.Boolean</span></span>

## <span data-ttu-id="4de58-126">筆記</span><span class="sxs-lookup"><span data-stu-id="4de58-126">NOTES</span></span>

## <span data-ttu-id="4de58-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="4de58-127">RELATED LINKS</span></span>

[<span data-ttu-id="4de58-128">AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4de58-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="4de58-129">新-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4de58-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="4de58-130">移除-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4de58-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


