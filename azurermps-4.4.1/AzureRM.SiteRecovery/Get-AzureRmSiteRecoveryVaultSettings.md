---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 56F63287-0247-4921-9C99-E581E075F4D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: e17b5cea1c26ccf63c6c9347b19ef0f8dc0be1b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625063"
---
# <span data-ttu-id="42992-101">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="42992-101">Get-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="42992-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42992-102">SYNOPSIS</span></span>
<span data-ttu-id="42992-103">取得目前網站恢復電子倉庫的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="42992-103">Gets settings information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42992-104">句法</span><span class="sxs-lookup"><span data-stu-id="42992-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVaultSettings [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42992-105">說明</span><span class="sxs-lookup"><span data-stu-id="42992-105">DESCRIPTION</span></span>
<span data-ttu-id="42992-106">**AzureRmSiteRecoveryVaultSettings** Cmdlet 會取得與目前 Azure Site Recovery 保存庫相關的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="42992-106">The **Get-AzureRmSiteRecoveryVaultSettings** cmdlet gets settings information related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="42992-107">示例</span><span class="sxs-lookup"><span data-stu-id="42992-107">EXAMPLES</span></span>

## <span data-ttu-id="42992-108">參數</span><span class="sxs-lookup"><span data-stu-id="42992-108">PARAMETERS</span></span>

### <span data-ttu-id="42992-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42992-109">-DefaultProfile</span></span>
<span data-ttu-id="42992-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="42992-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42992-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42992-111">CommonParameters</span></span>
<span data-ttu-id="42992-112">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42992-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42992-113">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42992-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42992-114">輸入</span><span class="sxs-lookup"><span data-stu-id="42992-114">INPUTS</span></span>

## <span data-ttu-id="42992-115">輸出</span><span class="sxs-lookup"><span data-stu-id="42992-115">OUTPUTS</span></span>

### <span data-ttu-id="42992-116">ASRVaultSettings 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="42992-116">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="42992-117">筆記</span><span class="sxs-lookup"><span data-stu-id="42992-117">NOTES</span></span>

## <span data-ttu-id="42992-118">相關連結</span><span class="sxs-lookup"><span data-stu-id="42992-118">RELATED LINKS</span></span>

[<span data-ttu-id="42992-119">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="42992-119">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
