---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 6256fc57d4084a55b2288875b56c6c616b16f8b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454459"
---
# <span data-ttu-id="32a84-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="32a84-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="32a84-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32a84-102">SYNOPSIS</span></span>
<span data-ttu-id="32a84-103">測試輸入的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="32a84-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32a84-104">句法</span><span class="sxs-lookup"><span data-stu-id="32a84-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32a84-105">說明</span><span class="sxs-lookup"><span data-stu-id="32a84-105">DESCRIPTION</span></span>
<span data-ttu-id="32a84-106">**AzureRmStreamAnalyticsInput** Cmdlet 會測試資料流程分析程式連接至輸入的能力。</span><span class="sxs-lookup"><span data-stu-id="32a84-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="32a84-107">示例</span><span class="sxs-lookup"><span data-stu-id="32a84-107">EXAMPLES</span></span>

### <span data-ttu-id="32a84-108">範例1：測試輸入資料流程的線上狀態</span><span class="sxs-lookup"><span data-stu-id="32a84-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="32a84-109">這會測試 StreamingJob 中輸入 EntryStream 的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="32a84-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="32a84-110">參數</span><span class="sxs-lookup"><span data-stu-id="32a84-110">PARAMETERS</span></span>

### <span data-ttu-id="32a84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a84-111">-DefaultProfile</span></span>
<span data-ttu-id="32a84-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="32a84-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32a84-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="32a84-113">-JobName</span></span>
<span data-ttu-id="32a84-114">指定 Azure 串流分析輸入所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="32a84-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="32a84-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="32a84-115">-Name</span></span>
<span data-ttu-id="32a84-116">指定要測試的 Azure 資料流程分析輸入的名稱。</span><span class="sxs-lookup"><span data-stu-id="32a84-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="32a84-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32a84-117">-ResourceGroupName</span></span>
<span data-ttu-id="32a84-118">指定 Azure 串流分析輸入所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="32a84-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="32a84-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a84-119">CommonParameters</span></span>
<span data-ttu-id="32a84-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32a84-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a84-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="32a84-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a84-122">輸入</span><span class="sxs-lookup"><span data-stu-id="32a84-122">INPUTS</span></span>

### <span data-ttu-id="32a84-123">System.object</span><span class="sxs-lookup"><span data-stu-id="32a84-123">System.String</span></span>

## <span data-ttu-id="32a84-124">輸出</span><span class="sxs-lookup"><span data-stu-id="32a84-124">OUTPUTS</span></span>

### <span data-ttu-id="32a84-125">System.object</span><span class="sxs-lookup"><span data-stu-id="32a84-125">System.Boolean</span></span>

## <span data-ttu-id="32a84-126">筆記</span><span class="sxs-lookup"><span data-stu-id="32a84-126">NOTES</span></span>

## <span data-ttu-id="32a84-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="32a84-127">RELATED LINKS</span></span>

[<span data-ttu-id="32a84-128">AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="32a84-128">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="32a84-129">新-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="32a84-129">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="32a84-130">移除-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="32a84-130">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


