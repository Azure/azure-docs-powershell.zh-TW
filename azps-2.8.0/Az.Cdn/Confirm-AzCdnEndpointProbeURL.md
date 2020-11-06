---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: 517fb30fd95bfc435fcc847a7f9f0765befc21c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613563"
---
# <span data-ttu-id="da1b9-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="da1b9-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="da1b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="da1b9-103">驗證探測 URL。</span><span class="sxs-lookup"><span data-stu-id="da1b9-103">Validates a probe URL.</span></span>

## <span data-ttu-id="da1b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="da1b9-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da1b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="da1b9-105">DESCRIPTION</span></span>
<span data-ttu-id="da1b9-106">**Confirm AzCdnEndpointProbeURL** Cmdlet 會確認提供的探測 URL 是否可用於動態網站加速。</span><span class="sxs-lookup"><span data-stu-id="da1b9-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="da1b9-107">示例</span><span class="sxs-lookup"><span data-stu-id="da1b9-107">EXAMPLES</span></span>

### <span data-ttu-id="da1b9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="da1b9-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="da1b9-109">驗證探測 url " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="da1b9-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="da1b9-110">參數</span><span class="sxs-lookup"><span data-stu-id="da1b9-110">PARAMETERS</span></span>

### <span data-ttu-id="da1b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da1b9-111">-DefaultProfile</span></span>
<span data-ttu-id="da1b9-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="da1b9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da1b9-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="da1b9-113">-ProbeUrl</span></span>
<span data-ttu-id="da1b9-114">要驗證的建議探測 URL 名稱。</span><span class="sxs-lookup"><span data-stu-id="da1b9-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="da1b9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da1b9-115">CommonParameters</span></span>
<span data-ttu-id="da1b9-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da1b9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da1b9-117">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="da1b9-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da1b9-118">輸入</span><span class="sxs-lookup"><span data-stu-id="da1b9-118">INPUTS</span></span>

### <span data-ttu-id="da1b9-119">所有</span><span class="sxs-lookup"><span data-stu-id="da1b9-119">None</span></span>

## <span data-ttu-id="da1b9-120">輸出</span><span class="sxs-lookup"><span data-stu-id="da1b9-120">OUTPUTS</span></span>

### <span data-ttu-id="da1b9-121">[PSValidateProbeOutput] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="da1b9-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="da1b9-122">筆記</span><span class="sxs-lookup"><span data-stu-id="da1b9-122">NOTES</span></span>

## <span data-ttu-id="da1b9-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="da1b9-123">RELATED LINKS</span></span>
