---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 63E9894A-3AC5-4397-9B21-D0A72EBA5C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 70d0876be32b80d314dfb7a464d0626b7c534fea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444331"
---
# <span data-ttu-id="872a8-101">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="872a8-101">Remove-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="872a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="872a8-102">SYNOPSIS</span></span>
<span data-ttu-id="872a8-103">移除 Site Recovery 保存庫。</span><span class="sxs-lookup"><span data-stu-id="872a8-103">Removes a Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="872a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="872a8-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryVault -Vault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="872a8-105">說明</span><span class="sxs-lookup"><span data-stu-id="872a8-105">DESCRIPTION</span></span>
<span data-ttu-id="872a8-106">**AzureRmSiteRecoveryVault** Cmdlet 會刪除 Azure Site Recovery 保存庫。</span><span class="sxs-lookup"><span data-stu-id="872a8-106">The **Remove-AzureRmSiteRecoveryVault** cmdlet deletes an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="872a8-107">示例</span><span class="sxs-lookup"><span data-stu-id="872a8-107">EXAMPLES</span></span>

## <span data-ttu-id="872a8-108">參數</span><span class="sxs-lookup"><span data-stu-id="872a8-108">PARAMETERS</span></span>

### <span data-ttu-id="872a8-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="872a8-109">-DefaultProfile</span></span>
<span data-ttu-id="872a8-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="872a8-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="872a8-111">-保存庫</span><span class="sxs-lookup"><span data-stu-id="872a8-111">-Vault</span></span>
<span data-ttu-id="872a8-112">指定 Site Recovery 保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="872a8-112">Specifies the Site Recovery vault object.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="872a8-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872a8-113">CommonParameters</span></span>
<span data-ttu-id="872a8-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="872a8-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872a8-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="872a8-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872a8-116">輸入</span><span class="sxs-lookup"><span data-stu-id="872a8-116">INPUTS</span></span>

### <span data-ttu-id="872a8-117">ASRVault</span><span class="sxs-lookup"><span data-stu-id="872a8-117">ASRVault</span></span>
<span data-ttu-id="872a8-118">參數 "Vault" 接受來自管線的 "ASRVault" 類型值</span><span class="sxs-lookup"><span data-stu-id="872a8-118">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="872a8-119">輸出</span><span class="sxs-lookup"><span data-stu-id="872a8-119">OUTPUTS</span></span>

## <span data-ttu-id="872a8-120">筆記</span><span class="sxs-lookup"><span data-stu-id="872a8-120">NOTES</span></span>

## <span data-ttu-id="872a8-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="872a8-121">RELATED LINKS</span></span>

[<span data-ttu-id="872a8-122">AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="872a8-122">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="872a8-123">新-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="872a8-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)
