---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140751"
---
# <span data-ttu-id="840b8-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="840b8-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="840b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="840b8-102">SYNOPSIS</span></span>
<span data-ttu-id="840b8-103">取得有關資料流程分析作業轉換的資訊。</span><span class="sxs-lookup"><span data-stu-id="840b8-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="840b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="840b8-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="840b8-105">說明</span><span class="sxs-lookup"><span data-stu-id="840b8-105">DESCRIPTION</span></span>
<span data-ttu-id="840b8-106">**AzStreamAnalyticsTransformation** Cmdlet 會取得對流分析作業上所定義轉換的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="840b8-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="840b8-107">示例</span><span class="sxs-lookup"><span data-stu-id="840b8-107">EXAMPLES</span></span>

### <span data-ttu-id="840b8-108">範例1：取得資料流程分析轉換的相關資訊</span><span class="sxs-lookup"><span data-stu-id="840b8-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="840b8-109">這個命令會傳回稱為 StreamingJob 的作業上稱為 StreamingJob 轉換的資訊。</span><span class="sxs-lookup"><span data-stu-id="840b8-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="840b8-110">參數</span><span class="sxs-lookup"><span data-stu-id="840b8-110">PARAMETERS</span></span>

### <span data-ttu-id="840b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="840b8-111">-DefaultProfile</span></span>
<span data-ttu-id="840b8-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="840b8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="840b8-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="840b8-113">-JobName</span></span>
<span data-ttu-id="840b8-114">指定 Azure 資料流程分析轉換所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="840b8-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="840b8-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="840b8-115">-Name</span></span>
<span data-ttu-id="840b8-116">指定要檢索之 Azure 串流分析轉換的名稱。</span><span class="sxs-lookup"><span data-stu-id="840b8-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="840b8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="840b8-117">-ResourceGroupName</span></span>
<span data-ttu-id="840b8-118">指定 Azure 資料流程分析轉換所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="840b8-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="840b8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="840b8-119">CommonParameters</span></span>
<span data-ttu-id="840b8-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="840b8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="840b8-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="840b8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="840b8-122">輸入</span><span class="sxs-lookup"><span data-stu-id="840b8-122">INPUTS</span></span>

### <span data-ttu-id="840b8-123">System.object</span><span class="sxs-lookup"><span data-stu-id="840b8-123">System.String</span></span>

## <span data-ttu-id="840b8-124">輸出</span><span class="sxs-lookup"><span data-stu-id="840b8-124">OUTPUTS</span></span>

### <span data-ttu-id="840b8-125">PSTransformation 中的 StreamAnalytics。</span><span class="sxs-lookup"><span data-stu-id="840b8-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="840b8-126">筆記</span><span class="sxs-lookup"><span data-stu-id="840b8-126">NOTES</span></span>

## <span data-ttu-id="840b8-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="840b8-127">RELATED LINKS</span></span>

[<span data-ttu-id="840b8-128">新-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="840b8-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


