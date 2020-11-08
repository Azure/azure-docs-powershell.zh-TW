---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 9635031d6eaea5a7920a6862fb8cf20ce536c1db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969914"
---
# <span data-ttu-id="17748-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="17748-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="17748-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17748-102">SYNOPSIS</span></span>
<span data-ttu-id="17748-103">更新 CDN 來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="17748-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="17748-104">句法</span><span class="sxs-lookup"><span data-stu-id="17748-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17748-105">說明</span><span class="sxs-lookup"><span data-stu-id="17748-105">DESCRIPTION</span></span>
<span data-ttu-id="17748-106">**AzCdnOrigin** Cmdlet 會更新 Azure 內容傳遞網路 (CDN) 來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="17748-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="17748-107">示例</span><span class="sxs-lookup"><span data-stu-id="17748-107">EXAMPLES</span></span>

## <span data-ttu-id="17748-108">參數</span><span class="sxs-lookup"><span data-stu-id="17748-108">PARAMETERS</span></span>

### <span data-ttu-id="17748-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="17748-109">-CdnOrigin</span></span>
<span data-ttu-id="17748-110">指定此 Cmdlet 更新的原始伺服器。</span><span class="sxs-lookup"><span data-stu-id="17748-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="17748-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17748-111">-DefaultProfile</span></span>
<span data-ttu-id="17748-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="17748-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17748-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17748-113">CommonParameters</span></span>
<span data-ttu-id="17748-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17748-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17748-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="17748-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17748-116">輸入</span><span class="sxs-lookup"><span data-stu-id="17748-116">INPUTS</span></span>

### <span data-ttu-id="17748-117">PSOrigin 中的 [Microsoft.]</span><span class="sxs-lookup"><span data-stu-id="17748-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="17748-118">輸出</span><span class="sxs-lookup"><span data-stu-id="17748-118">OUTPUTS</span></span>

### <span data-ttu-id="17748-119">PSOrigin 中的 [Microsoft.]</span><span class="sxs-lookup"><span data-stu-id="17748-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="17748-120">筆記</span><span class="sxs-lookup"><span data-stu-id="17748-120">NOTES</span></span>

## <span data-ttu-id="17748-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="17748-121">RELATED LINKS</span></span>

[<span data-ttu-id="17748-122">AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="17748-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


