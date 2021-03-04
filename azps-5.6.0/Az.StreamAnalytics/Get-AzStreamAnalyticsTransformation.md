---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 0c009ed05b475e466ab0b2c0dd7c6f18e70c2f9d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907382"
---
# <span data-ttu-id="04639-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="04639-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="04639-102">簡介</span><span class="sxs-lookup"><span data-stu-id="04639-102">SYNOPSIS</span></span>
<span data-ttu-id="04639-103">獲得 Stream Analytics 工作轉換的資訊。</span><span class="sxs-lookup"><span data-stu-id="04639-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="04639-104">語法</span><span class="sxs-lookup"><span data-stu-id="04639-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04639-105">描述</span><span class="sxs-lookup"><span data-stu-id="04639-105">DESCRIPTION</span></span>
<span data-ttu-id="04639-106">**Get-AzStreamAnalyticsTransformation** Cmdlet 會取得 Stream Analytics 工作上定義的轉換相關資訊。</span><span class="sxs-lookup"><span data-stu-id="04639-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="04639-107">例子</span><span class="sxs-lookup"><span data-stu-id="04639-107">EXAMPLES</span></span>

### <span data-ttu-id="04639-108">範例 1：取得 Stream Analytics 轉換的資訊</span><span class="sxs-lookup"><span data-stu-id="04639-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="04639-109">此命令會回到名為 StreamingJob 的工作上稱為 StreamingJob 的轉換相關資訊。</span><span class="sxs-lookup"><span data-stu-id="04639-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="04639-110">參數</span><span class="sxs-lookup"><span data-stu-id="04639-110">PARAMETERS</span></span>

### <span data-ttu-id="04639-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04639-111">-DefaultProfile</span></span>
<span data-ttu-id="04639-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="04639-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04639-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="04639-113">-JobName</span></span>
<span data-ttu-id="04639-114">指定 Azure Stream Analytics 轉換所屬的 Azure Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="04639-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="04639-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="04639-115">-Name</span></span>
<span data-ttu-id="04639-116">指定要取回的 Azure Stream Analytics 轉換名稱。</span><span class="sxs-lookup"><span data-stu-id="04639-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="04639-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04639-117">-ResourceGroupName</span></span>
<span data-ttu-id="04639-118">指定 Azure Stream Analytics 轉換所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="04639-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="04639-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04639-119">CommonParameters</span></span>
<span data-ttu-id="04639-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="04639-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04639-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="04639-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04639-122">輸入</span><span class="sxs-lookup"><span data-stu-id="04639-122">INPUTS</span></span>

### <span data-ttu-id="04639-123">System.String</span><span class="sxs-lookup"><span data-stu-id="04639-123">System.String</span></span>

## <span data-ttu-id="04639-124">輸出</span><span class="sxs-lookup"><span data-stu-id="04639-124">OUTPUTS</span></span>

### <span data-ttu-id="04639-125">Microsoft.Azure.Commands.StreamAnalytics.models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="04639-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="04639-126">筆記</span><span class="sxs-lookup"><span data-stu-id="04639-126">NOTES</span></span>

## <span data-ttu-id="04639-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="04639-127">RELATED LINKS</span></span>

[<span data-ttu-id="04639-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="04639-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


