---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: de676da4e276cf7e2b49558c81e9d7f6876d158b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450420"
---
# <span data-ttu-id="1520d-101">Get-AzureRmStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="1520d-101">Get-AzureRmStreamAnalyticsQuota</span></span>

## <span data-ttu-id="1520d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1520d-102">SYNOPSIS</span></span>
<span data-ttu-id="1520d-103">取得區域之流式處理單位配額的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1520d-103">Gets information about the Streaming Unit quota for a region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1520d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1520d-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1520d-105">說明</span><span class="sxs-lookup"><span data-stu-id="1520d-105">DESCRIPTION</span></span>
<span data-ttu-id="1520d-106">**AzureRmStreamAnalyticsQuota** Cmdlet 會取得某個區域之流式處理單位配額的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1520d-106">The **Get-AzureRmStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="1520d-107">示例</span><span class="sxs-lookup"><span data-stu-id="1520d-107">EXAMPLES</span></span>

### <span data-ttu-id="1520d-108">範例1：取得地區資料流程單位配額的相關資訊</span><span class="sxs-lookup"><span data-stu-id="1520d-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="1520d-109">這個命令會傳回有關 [西部美國] 地區的流式處理單位配額及使用量的資訊。</span><span class="sxs-lookup"><span data-stu-id="1520d-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="1520d-110">參數</span><span class="sxs-lookup"><span data-stu-id="1520d-110">PARAMETERS</span></span>

### <span data-ttu-id="1520d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1520d-111">-DefaultProfile</span></span>
<span data-ttu-id="1520d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1520d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1520d-113">-位置</span><span class="sxs-lookup"><span data-stu-id="1520d-113">-Location</span></span>
<span data-ttu-id="1520d-114">指定要取得流式處理單位配額資訊的 Azure 區域或資料中心位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="1520d-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="1520d-115"> https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services如需支援的 Azure 區域清單，請參閱。</span><span class="sxs-lookup"><span data-stu-id="1520d-115">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="1520d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1520d-116">CommonParameters</span></span>
<span data-ttu-id="1520d-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1520d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1520d-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1520d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1520d-119">輸入</span><span class="sxs-lookup"><span data-stu-id="1520d-119">INPUTS</span></span>

### <span data-ttu-id="1520d-120">所有</span><span class="sxs-lookup"><span data-stu-id="1520d-120">None</span></span>
<span data-ttu-id="1520d-121">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1520d-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1520d-122">輸出</span><span class="sxs-lookup"><span data-stu-id="1520d-122">OUTPUTS</span></span>

### <span data-ttu-id="1520d-123">[System.object]. 清單 ' 1 [StreamAnalytics. PSQuota，StreamAnalytics]]]]]]]]]]]]</span><span class="sxs-lookup"><span data-stu-id="1520d-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="1520d-124">筆記</span><span class="sxs-lookup"><span data-stu-id="1520d-124">NOTES</span></span>

## <span data-ttu-id="1520d-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="1520d-125">RELATED LINKS</span></span>

[<span data-ttu-id="1520d-126">Azure 資料流程分析 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1520d-126">Azure Stream Analytics Cmdlets</span></span>](./AzureRM.StreamAnalytics.md)


