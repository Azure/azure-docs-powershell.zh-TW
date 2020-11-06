---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: f09ca4bb6c033b954542d6c734b27bf5f2236d87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444343"
---
# <span data-ttu-id="a06df-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a06df-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="a06df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a06df-102">SYNOPSIS</span></span>
<span data-ttu-id="a06df-103">移除網站復原複製原則。</span><span class="sxs-lookup"><span data-stu-id="a06df-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a06df-104">句法</span><span class="sxs-lookup"><span data-stu-id="a06df-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a06df-105">說明</span><span class="sxs-lookup"><span data-stu-id="a06df-105">DESCRIPTION</span></span>
<span data-ttu-id="a06df-106">**AzureRMSiteRecoveryPolicy** Cmdlet 會移除 Azure Site Recovery 複製原則。</span><span class="sxs-lookup"><span data-stu-id="a06df-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="a06df-107">示例</span><span class="sxs-lookup"><span data-stu-id="a06df-107">EXAMPLES</span></span>

## <span data-ttu-id="a06df-108">參數</span><span class="sxs-lookup"><span data-stu-id="a06df-108">PARAMETERS</span></span>

### <span data-ttu-id="a06df-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06df-109">-DefaultProfile</span></span>
<span data-ttu-id="a06df-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a06df-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a06df-111">-原則</span><span class="sxs-lookup"><span data-stu-id="a06df-111">-Policy</span></span>
<span data-ttu-id="a06df-112">指定網站恢復原則物件。</span><span class="sxs-lookup"><span data-stu-id="a06df-112">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a06df-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06df-113">CommonParameters</span></span>
<span data-ttu-id="a06df-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a06df-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06df-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a06df-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06df-116">輸入</span><span class="sxs-lookup"><span data-stu-id="a06df-116">INPUTS</span></span>

### <span data-ttu-id="a06df-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="a06df-117">ASRPolicy</span></span>
<span data-ttu-id="a06df-118">形參 "Policy" 接受管線中 "ASRPolicy" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a06df-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="a06df-119">輸出</span><span class="sxs-lookup"><span data-stu-id="a06df-119">OUTPUTS</span></span>

## <span data-ttu-id="a06df-120">筆記</span><span class="sxs-lookup"><span data-stu-id="a06df-120">NOTES</span></span>

## <span data-ttu-id="a06df-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="a06df-121">RELATED LINKS</span></span>

[<span data-ttu-id="a06df-122">AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a06df-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="a06df-123">新-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a06df-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
