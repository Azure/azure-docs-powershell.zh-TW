---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BDEA3F9D-AC23-402D-BA1F-AC617C7480A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 481d2d414cde32e9d0b99cedd5b942b7bed9b248
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454015"
---
# <span data-ttu-id="53689-101">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="53689-101">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="53689-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53689-102">SYNOPSIS</span></span>
<span data-ttu-id="53689-103">從目前的網站恢復電子倉庫移除網路對應。</span><span class="sxs-lookup"><span data-stu-id="53689-103">Removes a network mapping from the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53689-104">句法</span><span class="sxs-lookup"><span data-stu-id="53689-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53689-105">說明</span><span class="sxs-lookup"><span data-stu-id="53689-105">DESCRIPTION</span></span>
<span data-ttu-id="53689-106">**AzureRMSiteRecoveryNetworkMapping** Cmdlet 會從目前的 Azure Site Recovery 保存庫中移除網路對應。</span><span class="sxs-lookup"><span data-stu-id="53689-106">The **Remove-AzureRMSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="53689-107">示例</span><span class="sxs-lookup"><span data-stu-id="53689-107">EXAMPLES</span></span>

## <span data-ttu-id="53689-108">參數</span><span class="sxs-lookup"><span data-stu-id="53689-108">PARAMETERS</span></span>

### <span data-ttu-id="53689-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53689-109">-DefaultProfile</span></span>
<span data-ttu-id="53689-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53689-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53689-111">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="53689-111">-NetworkMapping</span></span>
<span data-ttu-id="53689-112">指定網路對應物件。</span><span class="sxs-lookup"><span data-stu-id="53689-112">Specifies the network mapping object.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53689-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53689-113">CommonParameters</span></span>
<span data-ttu-id="53689-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53689-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53689-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53689-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53689-116">輸入</span><span class="sxs-lookup"><span data-stu-id="53689-116">INPUTS</span></span>

### <span data-ttu-id="53689-117">ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="53689-117">ASRNetworkMapping</span></span>
<span data-ttu-id="53689-118">形參 "NetworkMapping" 接受管線中 "ASRNetworkMapping" 類型的值</span><span class="sxs-lookup"><span data-stu-id="53689-118">Parameter 'NetworkMapping' accepts value of type 'ASRNetworkMapping' from the pipeline</span></span>

## <span data-ttu-id="53689-119">輸出</span><span class="sxs-lookup"><span data-stu-id="53689-119">OUTPUTS</span></span>

### <span data-ttu-id="53689-120">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="53689-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="53689-121">筆記</span><span class="sxs-lookup"><span data-stu-id="53689-121">NOTES</span></span>

## <span data-ttu-id="53689-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="53689-122">RELATED LINKS</span></span>

[<span data-ttu-id="53689-123">AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="53689-123">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="53689-124">新-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="53689-124">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)
