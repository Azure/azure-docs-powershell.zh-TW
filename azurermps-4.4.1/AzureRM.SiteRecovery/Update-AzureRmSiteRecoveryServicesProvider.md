---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 31eda861294d4c678e141da8f40d1f5d6c5a4ca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625059"
---
# <span data-ttu-id="2e38d-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="2e38d-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="2e38d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e38d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e38d-103">更新從 Azure Site Recovery 服務提供者收到的資訊。</span><span class="sxs-lookup"><span data-stu-id="2e38d-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e38d-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e38d-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e38d-105">說明</span><span class="sxs-lookup"><span data-stu-id="2e38d-105">DESCRIPTION</span></span>
<span data-ttu-id="2e38d-106">**AzureRmSiteRecoveryServicesProvider** Cmdlet 會更新從 Azure Site Recovery 服務提供者收到的資訊。</span><span class="sxs-lookup"><span data-stu-id="2e38d-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="2e38d-107">您可以使用這個 Cmdlet 觸發從復原服務提供者收到的資訊重新整理。</span><span class="sxs-lookup"><span data-stu-id="2e38d-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="2e38d-108">示例</span><span class="sxs-lookup"><span data-stu-id="2e38d-108">EXAMPLES</span></span>

## <span data-ttu-id="2e38d-109">參數</span><span class="sxs-lookup"><span data-stu-id="2e38d-109">PARAMETERS</span></span>

### <span data-ttu-id="2e38d-110">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="2e38d-110">-ServicesProvider</span></span>
<span data-ttu-id="2e38d-111">指定 Azure Site Recovery 服務提供者物件。</span><span class="sxs-lookup"><span data-stu-id="2e38d-111">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e38d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e38d-112">-DefaultProfile</span></span>
<span data-ttu-id="2e38d-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e38d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e38d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e38d-114">CommonParameters</span></span>
<span data-ttu-id="2e38d-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e38d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e38d-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e38d-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e38d-117">輸入</span><span class="sxs-lookup"><span data-stu-id="2e38d-117">INPUTS</span></span>

### <span data-ttu-id="2e38d-118">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="2e38d-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="2e38d-119">形參 "ServicesProvider" 接受管線中 "ASRRecoveryServicesProvider" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2e38d-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="2e38d-120">輸出</span><span class="sxs-lookup"><span data-stu-id="2e38d-120">OUTPUTS</span></span>

## <span data-ttu-id="2e38d-121">筆記</span><span class="sxs-lookup"><span data-stu-id="2e38d-121">NOTES</span></span>

## <span data-ttu-id="2e38d-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e38d-122">RELATED LINKS</span></span>

[<span data-ttu-id="2e38d-123">AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="2e38d-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="2e38d-124">移除-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="2e38d-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
