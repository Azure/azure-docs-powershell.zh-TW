---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 56F63287-0247-4921-9C99-E581E075F4D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvaultsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: ef0ee9f4b2c068f5484932fa74da73e6f2a99585
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454039"
---
# <span data-ttu-id="299b2-101">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="299b2-101">Get-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="299b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="299b2-102">SYNOPSIS</span></span>
<span data-ttu-id="299b2-103">取得目前網站恢復電子倉庫的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="299b2-103">Gets settings information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="299b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="299b2-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVaultSettings [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="299b2-105">說明</span><span class="sxs-lookup"><span data-stu-id="299b2-105">DESCRIPTION</span></span>
<span data-ttu-id="299b2-106">**AzureRmSiteRecoveryVaultSettings** Cmdlet 會取得與目前 Azure Site Recovery 保存庫相關的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="299b2-106">The **Get-AzureRmSiteRecoveryVaultSettings** cmdlet gets settings information related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="299b2-107">示例</span><span class="sxs-lookup"><span data-stu-id="299b2-107">EXAMPLES</span></span>

## <span data-ttu-id="299b2-108">參數</span><span class="sxs-lookup"><span data-stu-id="299b2-108">PARAMETERS</span></span>

### <span data-ttu-id="299b2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="299b2-109">-DefaultProfile</span></span>
<span data-ttu-id="299b2-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="299b2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="299b2-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299b2-111">CommonParameters</span></span>
<span data-ttu-id="299b2-112">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="299b2-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299b2-113">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="299b2-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299b2-114">輸入</span><span class="sxs-lookup"><span data-stu-id="299b2-114">INPUTS</span></span>

### <span data-ttu-id="299b2-115">所有</span><span class="sxs-lookup"><span data-stu-id="299b2-115">None</span></span>
<span data-ttu-id="299b2-116">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="299b2-116">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="299b2-117">輸出</span><span class="sxs-lookup"><span data-stu-id="299b2-117">OUTPUTS</span></span>

### <span data-ttu-id="299b2-118">ASRVaultSettings 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="299b2-118">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="299b2-119">筆記</span><span class="sxs-lookup"><span data-stu-id="299b2-119">NOTES</span></span>

## <span data-ttu-id="299b2-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="299b2-120">RELATED LINKS</span></span>

[<span data-ttu-id="299b2-121">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="299b2-121">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
