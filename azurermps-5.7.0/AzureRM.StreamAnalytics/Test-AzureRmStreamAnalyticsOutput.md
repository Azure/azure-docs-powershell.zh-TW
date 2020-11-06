---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 5e93638489749702a3da2608927318f794bc4a3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452968"
---
# <span data-ttu-id="86102-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="86102-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="86102-102">摘要</span><span class="sxs-lookup"><span data-stu-id="86102-102">SYNOPSIS</span></span>
<span data-ttu-id="86102-103">測試輸出的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="86102-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86102-104">句法</span><span class="sxs-lookup"><span data-stu-id="86102-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86102-105">說明</span><span class="sxs-lookup"><span data-stu-id="86102-105">DESCRIPTION</span></span>
<span data-ttu-id="86102-106">**AzureRmStreamAnalyticsOutput** Cmdlet 會測試資料流程分析程式連接到輸出的能力。</span><span class="sxs-lookup"><span data-stu-id="86102-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="86102-107">示例</span><span class="sxs-lookup"><span data-stu-id="86102-107">EXAMPLES</span></span>

### <span data-ttu-id="86102-108">範例1：測試輸出的線上狀態</span><span class="sxs-lookup"><span data-stu-id="86102-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="86102-109">這會測試 StreamingJob 中輸出輸出的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="86102-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="86102-110">參數</span><span class="sxs-lookup"><span data-stu-id="86102-110">PARAMETERS</span></span>

### <span data-ttu-id="86102-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86102-111">-DefaultProfile</span></span>
<span data-ttu-id="86102-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="86102-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86102-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="86102-113">-JobName</span></span>
<span data-ttu-id="86102-114">指定所要的 Azure 資料流程分析輸出所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="86102-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86102-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="86102-115">-Name</span></span>
<span data-ttu-id="86102-116">指定要測試的 Azure 資料流程分析輸出的名稱。</span><span class="sxs-lookup"><span data-stu-id="86102-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86102-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86102-117">-ResourceGroupName</span></span>
<span data-ttu-id="86102-118">指定 Azure 資料流程分析輸出所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="86102-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86102-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86102-119">CommonParameters</span></span>
<span data-ttu-id="86102-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="86102-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86102-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="86102-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86102-122">輸入</span><span class="sxs-lookup"><span data-stu-id="86102-122">INPUTS</span></span>

### <span data-ttu-id="86102-123">所有</span><span class="sxs-lookup"><span data-stu-id="86102-123">None</span></span>
<span data-ttu-id="86102-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="86102-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="86102-125">輸出</span><span class="sxs-lookup"><span data-stu-id="86102-125">OUTPUTS</span></span>

### <span data-ttu-id="86102-126">System.object</span><span class="sxs-lookup"><span data-stu-id="86102-126">System.Object</span></span>

## <span data-ttu-id="86102-127">筆記</span><span class="sxs-lookup"><span data-stu-id="86102-127">NOTES</span></span>

## <span data-ttu-id="86102-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="86102-128">RELATED LINKS</span></span>

[<span data-ttu-id="86102-129">AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="86102-129">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="86102-130">新-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="86102-130">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="86102-131">移除-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="86102-131">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


