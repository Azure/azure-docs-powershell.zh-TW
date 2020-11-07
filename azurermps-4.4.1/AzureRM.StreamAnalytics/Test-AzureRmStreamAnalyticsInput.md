---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: d0357e06257ad1df97b47ea7be59a1797e0f6902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624530"
---
# <span data-ttu-id="e3109-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="e3109-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="e3109-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3109-102">SYNOPSIS</span></span>
<span data-ttu-id="e3109-103">測試輸入的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="e3109-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3109-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3109-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3109-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3109-105">DESCRIPTION</span></span>
<span data-ttu-id="e3109-106">**AzureRmStreamAnalyticsInput** Cmdlet 會測試資料流程分析程式連接至輸入的能力。</span><span class="sxs-lookup"><span data-stu-id="e3109-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="e3109-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3109-107">EXAMPLES</span></span>

### <span data-ttu-id="e3109-108">範例1：測試輸入資料流程的線上狀態</span><span class="sxs-lookup"><span data-stu-id="e3109-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="e3109-109">這會測試 StreamingJob 中輸入 EntryStream 的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="e3109-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="e3109-110">參數</span><span class="sxs-lookup"><span data-stu-id="e3109-110">PARAMETERS</span></span>

### <span data-ttu-id="e3109-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="e3109-111">-JobName</span></span>
<span data-ttu-id="e3109-112">指定 Azure 串流分析輸入所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3109-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="e3109-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3109-113">-Name</span></span>
<span data-ttu-id="e3109-114">指定要測試的 Azure 資料流程分析輸入的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3109-114">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="e3109-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3109-115">-ResourceGroupName</span></span>
<span data-ttu-id="e3109-116">指定 Azure 串流分析輸入所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3109-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="e3109-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3109-117">-DefaultProfile</span></span>
<span data-ttu-id="e3109-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3109-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3109-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3109-119">CommonParameters</span></span>
<span data-ttu-id="e3109-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3109-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3109-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3109-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3109-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e3109-122">INPUTS</span></span>

## <span data-ttu-id="e3109-123">輸出</span><span class="sxs-lookup"><span data-stu-id="e3109-123">OUTPUTS</span></span>

### <span data-ttu-id="e3109-124">System.object</span><span class="sxs-lookup"><span data-stu-id="e3109-124">System.Object</span></span>

## <span data-ttu-id="e3109-125">筆記</span><span class="sxs-lookup"><span data-stu-id="e3109-125">NOTES</span></span>

## <span data-ttu-id="e3109-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3109-126">RELATED LINKS</span></span>

[<span data-ttu-id="e3109-127">AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="e3109-127">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="e3109-128">新-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="e3109-128">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="e3109-129">移除-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="e3109-129">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


