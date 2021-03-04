---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: 8583227cee19a9429a7dfe4cd6bd8678e72d33ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907385"
---
# <span data-ttu-id="44e62-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="44e62-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="44e62-102">簡介</span><span class="sxs-lookup"><span data-stu-id="44e62-102">SYNOPSIS</span></span>
<span data-ttu-id="44e62-103">獲得有關區域串流單位配額的資訊。</span><span class="sxs-lookup"><span data-stu-id="44e62-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="44e62-104">語法</span><span class="sxs-lookup"><span data-stu-id="44e62-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44e62-105">描述</span><span class="sxs-lookup"><span data-stu-id="44e62-105">DESCRIPTION</span></span>
<span data-ttu-id="44e62-106">**Get-AzStreamAnalyticsQuota** Cmdlet 會取得有關區域串流單元配額的資訊。</span><span class="sxs-lookup"><span data-stu-id="44e62-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="44e62-107">例子</span><span class="sxs-lookup"><span data-stu-id="44e62-107">EXAMPLES</span></span>

### <span data-ttu-id="44e62-108">範例 1：取得有關區域串流單元配額的資訊</span><span class="sxs-lookup"><span data-stu-id="44e62-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="44e62-109">此命令會返回美國西部地區的串流單位配額及使用量相關資訊。</span><span class="sxs-lookup"><span data-stu-id="44e62-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="44e62-110">參數</span><span class="sxs-lookup"><span data-stu-id="44e62-110">PARAMETERS</span></span>

### <span data-ttu-id="44e62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44e62-111">-DefaultProfile</span></span>
<span data-ttu-id="44e62-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="44e62-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44e62-113">-位置</span><span class="sxs-lookup"><span data-stu-id="44e62-113">-Location</span></span>
<span data-ttu-id="44e62-114">指定要取得串流單位配額資訊的 Azure 地區或資料中心位置名稱。</span><span class="sxs-lookup"><span data-stu-id="44e62-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="44e62-115">請參閱 http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services 支援的 Azure 區域清單。</span><span class="sxs-lookup"><span data-stu-id="44e62-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="44e62-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44e62-116">CommonParameters</span></span>
<span data-ttu-id="44e62-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="44e62-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44e62-118">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="44e62-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44e62-119">輸入</span><span class="sxs-lookup"><span data-stu-id="44e62-119">INPUTS</span></span>

### <span data-ttu-id="44e62-120">System.String</span><span class="sxs-lookup"><span data-stu-id="44e62-120">System.String</span></span>

## <span data-ttu-id="44e62-121">輸出</span><span class="sxs-lookup"><span data-stu-id="44e62-121">OUTPUTS</span></span>

### <span data-ttu-id="44e62-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span><span class="sxs-lookup"><span data-stu-id="44e62-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="44e62-123">筆記</span><span class="sxs-lookup"><span data-stu-id="44e62-123">NOTES</span></span>

## <span data-ttu-id="44e62-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="44e62-124">RELATED LINKS</span></span>

[<span data-ttu-id="44e62-125">Azure Stream Analytics Cmdlet</span><span class="sxs-lookup"><span data-stu-id="44e62-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


