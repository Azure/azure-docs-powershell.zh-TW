---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 74af4f7c4bc4f211f22be111bff4ecf0a8b9831a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788626"
---
# <span data-ttu-id="f7519-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="f7519-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="f7519-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7519-102">SYNOPSIS</span></span>
<span data-ttu-id="f7519-103">更新 CDN 來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="f7519-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="f7519-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7519-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7519-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7519-105">DESCRIPTION</span></span>
<span data-ttu-id="f7519-106">**AzCdnOrigin** Cmdlet 會更新 Azure 內容傳遞網路 (CDN) 來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="f7519-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="f7519-107">示例</span><span class="sxs-lookup"><span data-stu-id="f7519-107">EXAMPLES</span></span>

## <span data-ttu-id="f7519-108">參數</span><span class="sxs-lookup"><span data-stu-id="f7519-108">PARAMETERS</span></span>

### <span data-ttu-id="f7519-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="f7519-109">-CdnOrigin</span></span>
<span data-ttu-id="f7519-110">指定此 Cmdlet 更新的原始伺服器。</span><span class="sxs-lookup"><span data-stu-id="f7519-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7519-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7519-111">-DefaultProfile</span></span>
<span data-ttu-id="f7519-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f7519-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7519-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7519-113">CommonParameters</span></span>
<span data-ttu-id="f7519-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7519-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7519-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7519-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7519-116">輸入</span><span class="sxs-lookup"><span data-stu-id="f7519-116">INPUTS</span></span>

### <span data-ttu-id="f7519-117">PSOrigin 中的 [Microsoft.]</span><span class="sxs-lookup"><span data-stu-id="f7519-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="f7519-118">輸出</span><span class="sxs-lookup"><span data-stu-id="f7519-118">OUTPUTS</span></span>

### <span data-ttu-id="f7519-119">PSOrigin 中的 [Microsoft.]</span><span class="sxs-lookup"><span data-stu-id="f7519-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="f7519-120">筆記</span><span class="sxs-lookup"><span data-stu-id="f7519-120">NOTES</span></span>

## <span data-ttu-id="f7519-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7519-121">RELATED LINKS</span></span>

[<span data-ttu-id="f7519-122">AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="f7519-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


