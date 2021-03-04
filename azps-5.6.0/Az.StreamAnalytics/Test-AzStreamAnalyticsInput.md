---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: 09cf95f6fd7feb17053063952ae7110098353c86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914998"
---
# <span data-ttu-id="1267a-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1267a-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="1267a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1267a-102">SYNOPSIS</span></span>
<span data-ttu-id="1267a-103">測試輸入的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="1267a-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="1267a-104">語法</span><span class="sxs-lookup"><span data-stu-id="1267a-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1267a-105">描述</span><span class="sxs-lookup"><span data-stu-id="1267a-105">DESCRIPTION</span></span>
<span data-ttu-id="1267a-106">**Test-AzStreamAnalyticsInput** Cmdlet 會測試 Stream Analytics 連接至輸入的能力。</span><span class="sxs-lookup"><span data-stu-id="1267a-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="1267a-107">例子</span><span class="sxs-lookup"><span data-stu-id="1267a-107">EXAMPLES</span></span>

### <span data-ttu-id="1267a-108">範例 1：測試輸入串流的連接狀態</span><span class="sxs-lookup"><span data-stu-id="1267a-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="1267a-109">這會測試 StreamingJob 中輸入 EntryStream 的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="1267a-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="1267a-110">參數</span><span class="sxs-lookup"><span data-stu-id="1267a-110">PARAMETERS</span></span>

### <span data-ttu-id="1267a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1267a-111">-DefaultProfile</span></span>
<span data-ttu-id="1267a-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1267a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1267a-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="1267a-113">-JobName</span></span>
<span data-ttu-id="1267a-114">指定 Azure Stream Analytics 輸入所屬的 Azure Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="1267a-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="1267a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1267a-115">-Name</span></span>
<span data-ttu-id="1267a-116">指定要測試的 Azure Stream Analytics 輸入名稱。</span><span class="sxs-lookup"><span data-stu-id="1267a-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="1267a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1267a-117">-ResourceGroupName</span></span>
<span data-ttu-id="1267a-118">指定 Azure Stream Analytics 輸入所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="1267a-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="1267a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1267a-119">CommonParameters</span></span>
<span data-ttu-id="1267a-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1267a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1267a-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1267a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1267a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="1267a-122">INPUTS</span></span>

### <span data-ttu-id="1267a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="1267a-123">System.String</span></span>

## <span data-ttu-id="1267a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="1267a-124">OUTPUTS</span></span>

### <span data-ttu-id="1267a-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1267a-125">System.Boolean</span></span>

## <span data-ttu-id="1267a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="1267a-126">NOTES</span></span>

## <span data-ttu-id="1267a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="1267a-127">RELATED LINKS</span></span>

[<span data-ttu-id="1267a-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1267a-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="1267a-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1267a-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="1267a-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1267a-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


