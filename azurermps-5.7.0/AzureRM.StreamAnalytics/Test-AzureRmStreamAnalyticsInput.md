---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 34e1c2813292801d29a93a6914abf11b2725ec14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445920"
---
# <span data-ttu-id="7968b-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7968b-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="7968b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7968b-102">SYNOPSIS</span></span>
<span data-ttu-id="7968b-103">測試輸入的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="7968b-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7968b-104">句法</span><span class="sxs-lookup"><span data-stu-id="7968b-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7968b-105">說明</span><span class="sxs-lookup"><span data-stu-id="7968b-105">DESCRIPTION</span></span>
<span data-ttu-id="7968b-106">**AzureRmStreamAnalyticsInput** Cmdlet 會測試資料流程分析程式連接至輸入的能力。</span><span class="sxs-lookup"><span data-stu-id="7968b-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="7968b-107">示例</span><span class="sxs-lookup"><span data-stu-id="7968b-107">EXAMPLES</span></span>

### <span data-ttu-id="7968b-108">範例1：測試輸入資料流程的線上狀態</span><span class="sxs-lookup"><span data-stu-id="7968b-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="7968b-109">這會測試 StreamingJob 中輸入 EntryStream 的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="7968b-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="7968b-110">參數</span><span class="sxs-lookup"><span data-stu-id="7968b-110">PARAMETERS</span></span>

### <span data-ttu-id="7968b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7968b-111">-DefaultProfile</span></span>
<span data-ttu-id="7968b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7968b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7968b-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="7968b-113">-JobName</span></span>
<span data-ttu-id="7968b-114">指定 Azure 串流分析輸入所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="7968b-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="7968b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="7968b-115">-Name</span></span>
<span data-ttu-id="7968b-116">指定要測試的 Azure 資料流程分析輸入的名稱。</span><span class="sxs-lookup"><span data-stu-id="7968b-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="7968b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7968b-117">-ResourceGroupName</span></span>
<span data-ttu-id="7968b-118">指定 Azure 串流分析輸入所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7968b-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="7968b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7968b-119">CommonParameters</span></span>
<span data-ttu-id="7968b-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7968b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7968b-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7968b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7968b-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7968b-122">INPUTS</span></span>

### <span data-ttu-id="7968b-123">所有</span><span class="sxs-lookup"><span data-stu-id="7968b-123">None</span></span>
<span data-ttu-id="7968b-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="7968b-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7968b-125">輸出</span><span class="sxs-lookup"><span data-stu-id="7968b-125">OUTPUTS</span></span>

### <span data-ttu-id="7968b-126">System.object</span><span class="sxs-lookup"><span data-stu-id="7968b-126">System.Object</span></span>

## <span data-ttu-id="7968b-127">筆記</span><span class="sxs-lookup"><span data-stu-id="7968b-127">NOTES</span></span>

## <span data-ttu-id="7968b-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="7968b-128">RELATED LINKS</span></span>

[<span data-ttu-id="7968b-129">AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7968b-129">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="7968b-130">新-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7968b-130">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="7968b-131">移除-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7968b-131">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


