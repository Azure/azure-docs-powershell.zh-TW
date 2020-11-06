---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: 179b4b028c7dd9338e75d07f559a61052b3d2bcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446431"
---
# <span data-ttu-id="e3a17-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e3a17-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="e3a17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3a17-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a17-103">更新 CDN 來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="e3a17-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3a17-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3a17-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3a17-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3a17-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a17-106">**AzureRmCdnOrigin** Cmdlet 會更新 Azure 內容傳遞網路 (CDN) 來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="e3a17-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="e3a17-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3a17-107">EXAMPLES</span></span>

## <span data-ttu-id="e3a17-108">參數</span><span class="sxs-lookup"><span data-stu-id="e3a17-108">PARAMETERS</span></span>

### <span data-ttu-id="e3a17-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e3a17-109">-CdnOrigin</span></span>
<span data-ttu-id="e3a17-110">指定此 Cmdlet 更新的原始伺服器。</span><span class="sxs-lookup"><span data-stu-id="e3a17-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: PSOrigin
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a17-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a17-111">-DefaultProfile</span></span>
<span data-ttu-id="e3a17-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e3a17-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3a17-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a17-113">CommonParameters</span></span>
<span data-ttu-id="e3a17-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3a17-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a17-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3a17-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a17-116">輸入</span><span class="sxs-lookup"><span data-stu-id="e3a17-116">INPUTS</span></span>

### <span data-ttu-id="e3a17-117">PSOrigin</span><span class="sxs-lookup"><span data-stu-id="e3a17-117">PSOrigin</span></span>
<span data-ttu-id="e3a17-118">參數 ' CdnOrigin' 從管線接受類型 ' PSOrigin' 的值</span><span class="sxs-lookup"><span data-stu-id="e3a17-118">Parameter 'CdnOrigin' accepts value of type 'PSOrigin' from the pipeline</span></span>

## <span data-ttu-id="e3a17-119">輸出</span><span class="sxs-lookup"><span data-stu-id="e3a17-119">OUTPUTS</span></span>

### <span data-ttu-id="e3a17-120">PSOrigin 中的 [Microsoft.]</span><span class="sxs-lookup"><span data-stu-id="e3a17-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="e3a17-121">筆記</span><span class="sxs-lookup"><span data-stu-id="e3a17-121">NOTES</span></span>

## <span data-ttu-id="e3a17-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3a17-122">RELATED LINKS</span></span>

[<span data-ttu-id="e3a17-123">AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e3a17-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


