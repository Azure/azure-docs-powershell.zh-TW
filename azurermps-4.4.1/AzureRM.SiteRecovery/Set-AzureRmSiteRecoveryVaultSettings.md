---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 133668A0-0D11-4034-A743-4C0D3CE0FAF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: 9c252649ea668e666c98719ab2045e99e729a836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452327"
---
# <span data-ttu-id="98a92-101">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="98a92-101">Set-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="98a92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98a92-102">SYNOPSIS</span></span>
<span data-ttu-id="98a92-103">設定網站復原電子倉庫內容以進行進一步的操作。</span><span class="sxs-lookup"><span data-stu-id="98a92-103">Sets the Site Recovery vault context for further operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98a92-104">句法</span><span class="sxs-lookup"><span data-stu-id="98a92-104">SYNTAX</span></span>

### <span data-ttu-id="98a92-105">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="98a92-105">AzureSiteRecoveryVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ASRVault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98a92-106">AzureRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="98a92-106">AzureRecoveryServicesVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ARSVault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98a92-107">說明</span><span class="sxs-lookup"><span data-stu-id="98a92-107">DESCRIPTION</span></span>
<span data-ttu-id="98a92-108">**AzureRmSiteRecoveryVaultSettings** Cmdlet 會設定 Azure Site Recovery 保存庫內容以進行進一步的操作。</span><span class="sxs-lookup"><span data-stu-id="98a92-108">The **Set-AzureRmSiteRecoveryVaultSettings** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>
<span data-ttu-id="98a92-109">這不適用於復原服務電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="98a92-109">This does not apply to recovery services vaults.</span></span>

## <span data-ttu-id="98a92-110">示例</span><span class="sxs-lookup"><span data-stu-id="98a92-110">EXAMPLES</span></span>

## <span data-ttu-id="98a92-111">參數</span><span class="sxs-lookup"><span data-stu-id="98a92-111">PARAMETERS</span></span>

### <span data-ttu-id="98a92-112">-ARSVault</span><span class="sxs-lookup"><span data-stu-id="98a92-112">-ARSVault</span></span>
<span data-ttu-id="98a92-113">指定 **ARSVault** 物件。</span><span class="sxs-lookup"><span data-stu-id="98a92-113">Specifies an **ARSVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98a92-114">-ASRVault</span><span class="sxs-lookup"><span data-stu-id="98a92-114">-ASRVault</span></span>
<span data-ttu-id="98a92-115">指定 **ASRVault** 物件。</span><span class="sxs-lookup"><span data-stu-id="98a92-115">Specifies an **ASRVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: AzureSiteRecoveryVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98a92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a92-116">-DefaultProfile</span></span>
<span data-ttu-id="98a92-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98a92-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98a92-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a92-118">CommonParameters</span></span>
<span data-ttu-id="98a92-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98a92-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a92-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="98a92-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a92-121">輸入</span><span class="sxs-lookup"><span data-stu-id="98a92-121">INPUTS</span></span>

### <span data-ttu-id="98a92-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="98a92-122">ARSVault</span></span>
<span data-ttu-id="98a92-123">形參 "ARSVault" 接受管線中 "ARSVault" 類型的值</span><span class="sxs-lookup"><span data-stu-id="98a92-123">Parameter 'ARSVault' accepts value of type 'ARSVault' from the pipeline</span></span>

### <span data-ttu-id="98a92-124">ASRVault</span><span class="sxs-lookup"><span data-stu-id="98a92-124">ASRVault</span></span>
<span data-ttu-id="98a92-125">形參 "ASRVault" 接受管線中 "ASRVault" 類型的值</span><span class="sxs-lookup"><span data-stu-id="98a92-125">Parameter 'ASRVault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="98a92-126">輸出</span><span class="sxs-lookup"><span data-stu-id="98a92-126">OUTPUTS</span></span>

### <span data-ttu-id="98a92-127">ASRVaultSettings 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="98a92-127">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="98a92-128">筆記</span><span class="sxs-lookup"><span data-stu-id="98a92-128">NOTES</span></span>

## <span data-ttu-id="98a92-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="98a92-129">RELATED LINKS</span></span>

[<span data-ttu-id="98a92-130">AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="98a92-130">Get-AzureRmSiteRecoveryVaultSettings</span></span>](./Get-AzureRmSiteRecoveryVaultSettings.md)
