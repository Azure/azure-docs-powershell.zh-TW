---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 3b01e089271cc131af5a4258c46836a87104ef62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624129"
---
# <span data-ttu-id="41239-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="41239-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="41239-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41239-102">SYNOPSIS</span></span>
<span data-ttu-id="41239-103">移除網站復原複製原則。</span><span class="sxs-lookup"><span data-stu-id="41239-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41239-104">句法</span><span class="sxs-lookup"><span data-stu-id="41239-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41239-105">說明</span><span class="sxs-lookup"><span data-stu-id="41239-105">DESCRIPTION</span></span>
<span data-ttu-id="41239-106">**AzureRMSiteRecoveryPolicy** Cmdlet 會移除 Azure Site Recovery 複製原則。</span><span class="sxs-lookup"><span data-stu-id="41239-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="41239-107">示例</span><span class="sxs-lookup"><span data-stu-id="41239-107">EXAMPLES</span></span>

## <span data-ttu-id="41239-108">參數</span><span class="sxs-lookup"><span data-stu-id="41239-108">PARAMETERS</span></span>

### <span data-ttu-id="41239-109">-原則</span><span class="sxs-lookup"><span data-stu-id="41239-109">-Policy</span></span>
<span data-ttu-id="41239-110">指定網站恢復原則物件。</span><span class="sxs-lookup"><span data-stu-id="41239-110">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41239-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41239-111">-DefaultProfile</span></span>
<span data-ttu-id="41239-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41239-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41239-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41239-113">CommonParameters</span></span>
<span data-ttu-id="41239-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41239-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41239-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41239-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41239-116">輸入</span><span class="sxs-lookup"><span data-stu-id="41239-116">INPUTS</span></span>

### <span data-ttu-id="41239-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="41239-117">ASRPolicy</span></span>
<span data-ttu-id="41239-118">形參 "Policy" 接受管線中 "ASRPolicy" 類型的值</span><span class="sxs-lookup"><span data-stu-id="41239-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="41239-119">輸出</span><span class="sxs-lookup"><span data-stu-id="41239-119">OUTPUTS</span></span>

## <span data-ttu-id="41239-120">筆記</span><span class="sxs-lookup"><span data-stu-id="41239-120">NOTES</span></span>

## <span data-ttu-id="41239-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="41239-121">RELATED LINKS</span></span>

[<span data-ttu-id="41239-122">AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="41239-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="41239-123">新-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="41239-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
