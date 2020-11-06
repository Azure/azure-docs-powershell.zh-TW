---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: c554caf7230b54db3e1161a20e001f9873f6dfff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450011"
---
# <span data-ttu-id="b73b1-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b73b1-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="b73b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b73b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b73b1-103">更新 CDN 來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="b73b1-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b73b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="b73b1-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b73b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="b73b1-105">DESCRIPTION</span></span>
<span data-ttu-id="b73b1-106">**AzureRmCdnOrigin** Cmdlet 會更新 Azure 內容傳遞網路 (CDN) 來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="b73b1-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="b73b1-107">示例</span><span class="sxs-lookup"><span data-stu-id="b73b1-107">EXAMPLES</span></span>

## <span data-ttu-id="b73b1-108">參數</span><span class="sxs-lookup"><span data-stu-id="b73b1-108">PARAMETERS</span></span>

### <span data-ttu-id="b73b1-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b73b1-109">-CdnOrigin</span></span>
<span data-ttu-id="b73b1-110">指定此 Cmdlet 更新的原始伺服器。</span><span class="sxs-lookup"><span data-stu-id="b73b1-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b73b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b73b1-111">-DefaultProfile</span></span>
<span data-ttu-id="b73b1-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b73b1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b73b1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b73b1-113">CommonParameters</span></span>
<span data-ttu-id="b73b1-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b73b1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b73b1-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b73b1-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b73b1-116">輸入</span><span class="sxs-lookup"><span data-stu-id="b73b1-116">INPUTS</span></span>

### <span data-ttu-id="b73b1-117">PSOrigin</span><span class="sxs-lookup"><span data-stu-id="b73b1-117">PSOrigin</span></span>
<span data-ttu-id="b73b1-118">參數 ' CdnOrigin' 從管線接受類型 ' PSOrigin' 的值</span><span class="sxs-lookup"><span data-stu-id="b73b1-118">Parameter 'CdnOrigin' accepts value of type 'PSOrigin' from the pipeline</span></span>

## <span data-ttu-id="b73b1-119">輸出</span><span class="sxs-lookup"><span data-stu-id="b73b1-119">OUTPUTS</span></span>

### <span data-ttu-id="b73b1-120">PSOrigin 中的 [Microsoft.]</span><span class="sxs-lookup"><span data-stu-id="b73b1-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="b73b1-121">筆記</span><span class="sxs-lookup"><span data-stu-id="b73b1-121">NOTES</span></span>

## <span data-ttu-id="b73b1-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="b73b1-122">RELATED LINKS</span></span>

[<span data-ttu-id="b73b1-123">AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b73b1-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


