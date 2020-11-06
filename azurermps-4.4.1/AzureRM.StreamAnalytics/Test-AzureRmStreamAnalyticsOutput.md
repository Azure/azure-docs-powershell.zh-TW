---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 5c961289267b0680a88cd16d58574c906a9f4408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451575"
---
# <span data-ttu-id="e9627-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e9627-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="e9627-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9627-102">SYNOPSIS</span></span>
<span data-ttu-id="e9627-103">測試輸出的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="e9627-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9627-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9627-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9627-105">說明</span><span class="sxs-lookup"><span data-stu-id="e9627-105">DESCRIPTION</span></span>
<span data-ttu-id="e9627-106">**AzureRmStreamAnalyticsOutput** Cmdlet 會測試資料流程分析程式連接到輸出的能力。</span><span class="sxs-lookup"><span data-stu-id="e9627-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="e9627-107">示例</span><span class="sxs-lookup"><span data-stu-id="e9627-107">EXAMPLES</span></span>

### <span data-ttu-id="e9627-108">範例1：測試輸出的線上狀態</span><span class="sxs-lookup"><span data-stu-id="e9627-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="e9627-109">這會測試 StreamingJob 中輸出輸出的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="e9627-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="e9627-110">參數</span><span class="sxs-lookup"><span data-stu-id="e9627-110">PARAMETERS</span></span>

### <span data-ttu-id="e9627-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="e9627-111">-JobName</span></span>
<span data-ttu-id="e9627-112">指定所要的 Azure 資料流程分析輸出所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9627-112">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="e9627-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9627-113">-Name</span></span>
<span data-ttu-id="e9627-114">指定要測試的 Azure 資料流程分析輸出的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9627-114">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="e9627-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9627-115">-ResourceGroupName</span></span>
<span data-ttu-id="e9627-116">指定 Azure 資料流程分析輸出所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9627-116">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="e9627-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9627-117">-DefaultProfile</span></span>
<span data-ttu-id="e9627-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9627-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9627-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9627-119">CommonParameters</span></span>
<span data-ttu-id="e9627-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9627-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9627-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e9627-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9627-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e9627-122">INPUTS</span></span>

## <span data-ttu-id="e9627-123">輸出</span><span class="sxs-lookup"><span data-stu-id="e9627-123">OUTPUTS</span></span>

### <span data-ttu-id="e9627-124">System.object</span><span class="sxs-lookup"><span data-stu-id="e9627-124">System.Object</span></span>

## <span data-ttu-id="e9627-125">筆記</span><span class="sxs-lookup"><span data-stu-id="e9627-125">NOTES</span></span>

## <span data-ttu-id="e9627-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9627-126">RELATED LINKS</span></span>

[<span data-ttu-id="e9627-127">AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e9627-127">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="e9627-128">新-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e9627-128">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="e9627-129">移除-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e9627-129">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


