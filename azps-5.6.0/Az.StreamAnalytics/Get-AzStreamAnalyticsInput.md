---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: 726d9d9294c4cf6e5789399ec821d4657e6f787e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907390"
---
# <span data-ttu-id="86302-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="86302-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="86302-102">簡介</span><span class="sxs-lookup"><span data-stu-id="86302-102">SYNOPSIS</span></span>
<span data-ttu-id="86302-103">獲得 Stream Analytics 的工作輸入。</span><span class="sxs-lookup"><span data-stu-id="86302-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="86302-104">語法</span><span class="sxs-lookup"><span data-stu-id="86302-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86302-105">描述</span><span class="sxs-lookup"><span data-stu-id="86302-105">DESCRIPTION</span></span>
<span data-ttu-id="86302-106">**Get-AzStreamAnalyticsInput** Cmdlet 會列出 Stream Analytics 工作定義的所有輸入，或取得特定輸入的資訊。</span><span class="sxs-lookup"><span data-stu-id="86302-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="86302-107">例子</span><span class="sxs-lookup"><span data-stu-id="86302-107">EXAMPLES</span></span>

### <span data-ttu-id="86302-108">範例 1：取得有關在工作上定義之輸入的資訊</span><span class="sxs-lookup"><span data-stu-id="86302-108">Example 1: Get information about the inputs defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="86302-109">此命令會返回有關在 Job StreamingJob 上定義之所有輸入的資訊。</span><span class="sxs-lookup"><span data-stu-id="86302-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="86302-110">範例 2：取得有關在工作上定義之特定輸入的資訊</span><span class="sxs-lookup"><span data-stu-id="86302-110">Example 2: Get information about a specific input defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="86302-111">此命令會返回在 Job StreamingJob 上定義之名為 EntryStream 之輸入的資訊。</span><span class="sxs-lookup"><span data-stu-id="86302-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="86302-112">參數</span><span class="sxs-lookup"><span data-stu-id="86302-112">PARAMETERS</span></span>

### <span data-ttu-id="86302-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86302-113">-DefaultProfile</span></span>
<span data-ttu-id="86302-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="86302-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86302-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="86302-115">-JobName</span></span>
<span data-ttu-id="86302-116">指定 Azure Stream Analytics 輸入所屬的 Azure Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="86302-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="86302-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="86302-117">-Name</span></span>
<span data-ttu-id="86302-118">指定要取回的 Azure Stream Analytics 輸入名稱。</span><span class="sxs-lookup"><span data-stu-id="86302-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="86302-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86302-119">-ResourceGroupName</span></span>
<span data-ttu-id="86302-120">指定 Azure Stream Analytics 輸入所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="86302-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="86302-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86302-121">CommonParameters</span></span>
<span data-ttu-id="86302-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="86302-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86302-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="86302-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86302-124">輸入</span><span class="sxs-lookup"><span data-stu-id="86302-124">INPUTS</span></span>

### <span data-ttu-id="86302-125">System.String</span><span class="sxs-lookup"><span data-stu-id="86302-125">System.String</span></span>

## <span data-ttu-id="86302-126">輸出</span><span class="sxs-lookup"><span data-stu-id="86302-126">OUTPUTS</span></span>

### <span data-ttu-id="86302-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="86302-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="86302-128">筆記</span><span class="sxs-lookup"><span data-stu-id="86302-128">NOTES</span></span>

## <span data-ttu-id="86302-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="86302-129">RELATED LINKS</span></span>

[<span data-ttu-id="86302-130">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="86302-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="86302-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="86302-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="86302-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="86302-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


