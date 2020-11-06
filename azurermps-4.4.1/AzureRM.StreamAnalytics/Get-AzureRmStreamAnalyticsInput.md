---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: e9f4017156a72b1284de8b62d1ae2ebf7d8321ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448819"
---
# <span data-ttu-id="74f86-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="74f86-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="74f86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74f86-102">SYNOPSIS</span></span>
<span data-ttu-id="74f86-103">取得串流分析作業輸入。</span><span class="sxs-lookup"><span data-stu-id="74f86-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74f86-104">句法</span><span class="sxs-lookup"><span data-stu-id="74f86-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74f86-105">說明</span><span class="sxs-lookup"><span data-stu-id="74f86-105">DESCRIPTION</span></span>
<span data-ttu-id="74f86-106">**AzureRmStreamAnalyticsInput** Cmdlet 會列出資料流程分析作業中定義的所有輸入，或取得特定輸入的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="74f86-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="74f86-107">示例</span><span class="sxs-lookup"><span data-stu-id="74f86-107">EXAMPLES</span></span>

### <span data-ttu-id="74f86-108">範例1：取得作業中定義之輸入的相關資訊</span><span class="sxs-lookup"><span data-stu-id="74f86-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="74f86-109">這個命令會傳回有關作業 StreamingJob 上所定義之所有輸入的資訊。</span><span class="sxs-lookup"><span data-stu-id="74f86-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="74f86-110">範例2：取得作業中定義之特定輸入的相關資訊</span><span class="sxs-lookup"><span data-stu-id="74f86-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="74f86-111">這個命令會傳回在作業 StreamingJob 上定義之名為 EntryStream 的輸入資訊。</span><span class="sxs-lookup"><span data-stu-id="74f86-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="74f86-112">參數</span><span class="sxs-lookup"><span data-stu-id="74f86-112">PARAMETERS</span></span>

### <span data-ttu-id="74f86-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="74f86-113">-JobName</span></span>
<span data-ttu-id="74f86-114">指定 Azure 串流分析輸入所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="74f86-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="74f86-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="74f86-115">-Name</span></span>
<span data-ttu-id="74f86-116">指定要檢索之 Azure 串流分析輸入的名稱。</span><span class="sxs-lookup"><span data-stu-id="74f86-116">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="74f86-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74f86-117">-ResourceGroupName</span></span>
<span data-ttu-id="74f86-118">指定 Azure 串流分析輸入所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="74f86-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="74f86-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f86-119">-DefaultProfile</span></span>
<span data-ttu-id="74f86-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74f86-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74f86-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f86-121">CommonParameters</span></span>
<span data-ttu-id="74f86-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74f86-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f86-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74f86-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f86-124">輸入</span><span class="sxs-lookup"><span data-stu-id="74f86-124">INPUTS</span></span>

## <span data-ttu-id="74f86-125">輸出</span><span class="sxs-lookup"><span data-stu-id="74f86-125">OUTPUTS</span></span>

### <span data-ttu-id="74f86-126">[System.object]. 清單 ' 1 [StreamAnalytics. PSInput，StreamAnalytics]]]]]]]]]]]]</span><span class="sxs-lookup"><span data-stu-id="74f86-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="74f86-127">筆記</span><span class="sxs-lookup"><span data-stu-id="74f86-127">NOTES</span></span>

## <span data-ttu-id="74f86-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="74f86-128">RELATED LINKS</span></span>

[<span data-ttu-id="74f86-129">新-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="74f86-129">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="74f86-130">移除-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="74f86-130">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="74f86-131">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="74f86-131">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


