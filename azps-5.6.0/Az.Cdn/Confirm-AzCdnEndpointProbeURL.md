---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: afc2400feb8694e74dd46731969429d6d7784369
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916270"
---
# <span data-ttu-id="9c182-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="9c182-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="9c182-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9c182-102">SYNOPSIS</span></span>
<span data-ttu-id="9c182-103">驗證探索 URL。</span><span class="sxs-lookup"><span data-stu-id="9c182-103">Validates a probe URL.</span></span>

## <span data-ttu-id="9c182-104">語法</span><span class="sxs-lookup"><span data-stu-id="9c182-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c182-105">描述</span><span class="sxs-lookup"><span data-stu-id="9c182-105">DESCRIPTION</span></span>
<span data-ttu-id="9c182-106">**Confirm-AzCdnEndpointProbeURL Cmdlet** 會確認所提供的探索 URL 是否可用於動態網站加速。</span><span class="sxs-lookup"><span data-stu-id="9c182-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="9c182-107">例子</span><span class="sxs-lookup"><span data-stu-id="9c182-107">EXAMPLES</span></span>

### <span data-ttu-id="9c182-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9c182-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="9c182-109">驗證探索 url http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="9c182-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="9c182-110">參數</span><span class="sxs-lookup"><span data-stu-id="9c182-110">PARAMETERS</span></span>

### <span data-ttu-id="9c182-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c182-111">-DefaultProfile</span></span>
<span data-ttu-id="9c182-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c182-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c182-113">-Url</span><span class="sxs-lookup"><span data-stu-id="9c182-113">-ProbeUrl</span></span>
<span data-ttu-id="9c182-114">建議要驗證的探索 URL 名稱。</span><span class="sxs-lookup"><span data-stu-id="9c182-114">Proposed probe URL name to validate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c182-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c182-115">CommonParameters</span></span>
<span data-ttu-id="9c182-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9c182-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c182-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c182-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c182-118">輸入</span><span class="sxs-lookup"><span data-stu-id="9c182-118">INPUTS</span></span>

### <span data-ttu-id="9c182-119">沒有</span><span class="sxs-lookup"><span data-stu-id="9c182-119">None</span></span>

## <span data-ttu-id="9c182-120">輸出</span><span class="sxs-lookup"><span data-stu-id="9c182-120">OUTPUTS</span></span>

### <span data-ttu-id="9c182-121">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="9c182-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="9c182-122">筆記</span><span class="sxs-lookup"><span data-stu-id="9c182-122">NOTES</span></span>

## <span data-ttu-id="9c182-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c182-123">RELATED LINKS</span></span>
