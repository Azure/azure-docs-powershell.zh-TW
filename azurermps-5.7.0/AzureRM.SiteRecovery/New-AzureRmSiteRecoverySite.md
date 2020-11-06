---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 053cd7695768be44cf3cecc5964e037f12f0b84e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450471"
---
# <span data-ttu-id="7b1a1-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="7b1a1-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="7b1a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b1a1-102">SYNOPSIS</span></span>
<span data-ttu-id="7b1a1-103">建立網站恢復網站。</span><span class="sxs-lookup"><span data-stu-id="7b1a1-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b1a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b1a1-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b1a1-105">說明</span><span class="sxs-lookup"><span data-stu-id="7b1a1-105">DESCRIPTION</span></span>
<span data-ttu-id="7b1a1-106">**新的 AzureRmSiteRecoverySite** Cmdlet 會在目前的電子倉庫中建立 Azure Site Recovery 網站。</span><span class="sxs-lookup"><span data-stu-id="7b1a1-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="7b1a1-107">示例</span><span class="sxs-lookup"><span data-stu-id="7b1a1-107">EXAMPLES</span></span>

## <span data-ttu-id="7b1a1-108">參數</span><span class="sxs-lookup"><span data-stu-id="7b1a1-108">PARAMETERS</span></span>

### <span data-ttu-id="7b1a1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b1a1-109">-DefaultProfile</span></span>
<span data-ttu-id="7b1a1-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b1a1-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b1a1-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b1a1-111">-Name</span></span>
<span data-ttu-id="7b1a1-112">指定網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b1a1-112">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b1a1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b1a1-113">CommonParameters</span></span>
<span data-ttu-id="7b1a1-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b1a1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b1a1-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7b1a1-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b1a1-116">輸入</span><span class="sxs-lookup"><span data-stu-id="7b1a1-116">INPUTS</span></span>

### <span data-ttu-id="7b1a1-117">所有</span><span class="sxs-lookup"><span data-stu-id="7b1a1-117">None</span></span>
<span data-ttu-id="7b1a1-118">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="7b1a1-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b1a1-119">輸出</span><span class="sxs-lookup"><span data-stu-id="7b1a1-119">OUTPUTS</span></span>

## <span data-ttu-id="7b1a1-120">筆記</span><span class="sxs-lookup"><span data-stu-id="7b1a1-120">NOTES</span></span>

## <span data-ttu-id="7b1a1-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b1a1-121">RELATED LINKS</span></span>

[<span data-ttu-id="7b1a1-122">AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="7b1a1-122">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="7b1a1-123">移除-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="7b1a1-123">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
