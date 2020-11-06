---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/confirm-azurermcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
ms.openlocfilehash: d6cf25c352c89592112aaa0a60cf7ba14ff7acf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450277"
---
# <span data-ttu-id="b2f6e-101">Confirm-AzureRmCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="b2f6e-101">Confirm-AzureRmCdnEndpointProbeURL</span></span>

## <span data-ttu-id="b2f6e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f6e-103">驗證探測 URL。</span><span class="sxs-lookup"><span data-stu-id="b2f6e-103">Validates a probe URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2f6e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2f6e-104">SYNTAX</span></span>

```
Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2f6e-105">說明</span><span class="sxs-lookup"><span data-stu-id="b2f6e-105">DESCRIPTION</span></span>
<span data-ttu-id="b2f6e-106">**Confirm AzureRmCdnEndpointProbeURL** Cmdlet 會確認提供的探測 URL 是否可用於動態網站加速。</span><span class="sxs-lookup"><span data-stu-id="b2f6e-106">The **Confirm-AzureRmCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="b2f6e-107">示例</span><span class="sxs-lookup"><span data-stu-id="b2f6e-107">EXAMPLES</span></span>

### <span data-ttu-id="b2f6e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b2f6e-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="b2f6e-109">驗證探測 url " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="b2f6e-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="b2f6e-110">參數</span><span class="sxs-lookup"><span data-stu-id="b2f6e-110">PARAMETERS</span></span>

### <span data-ttu-id="b2f6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f6e-111">-DefaultProfile</span></span>
<span data-ttu-id="b2f6e-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b2f6e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2f6e-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="b2f6e-113">-ProbeUrl</span></span>
<span data-ttu-id="b2f6e-114">要驗證的建議探測 URL 名稱。</span><span class="sxs-lookup"><span data-stu-id="b2f6e-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="b2f6e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f6e-115">CommonParameters</span></span>
<span data-ttu-id="b2f6e-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2f6e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f6e-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b2f6e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f6e-118">輸入</span><span class="sxs-lookup"><span data-stu-id="b2f6e-118">INPUTS</span></span>

### <span data-ttu-id="b2f6e-119">所有</span><span class="sxs-lookup"><span data-stu-id="b2f6e-119">None</span></span>

## <span data-ttu-id="b2f6e-120">輸出</span><span class="sxs-lookup"><span data-stu-id="b2f6e-120">OUTPUTS</span></span>

### <span data-ttu-id="b2f6e-121">[PSValidateProbeOutput] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="b2f6e-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="b2f6e-122">筆記</span><span class="sxs-lookup"><span data-stu-id="b2f6e-122">NOTES</span></span>

## <span data-ttu-id="b2f6e-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2f6e-123">RELATED LINKS</span></span>
