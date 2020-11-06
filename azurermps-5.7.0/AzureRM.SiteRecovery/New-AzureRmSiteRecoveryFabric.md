---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 38a7f8ee32f02db10dc971d5be2016d5dea0b538
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444347"
---
# <span data-ttu-id="9cf4b-101">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="9cf4b-101">New-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="9cf4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9cf4b-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf4b-103">建立 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="9cf4b-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cf4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9cf4b-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cf4b-105">說明</span><span class="sxs-lookup"><span data-stu-id="9cf4b-105">DESCRIPTION</span></span>
<span data-ttu-id="9cf4b-106">**新的-AzureRmSiteRecoveryFabric** Cmdlet 會建立指定類型的 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="9cf4b-106">The **New-AzureRmSiteRecoveryFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="9cf4b-107">示例</span><span class="sxs-lookup"><span data-stu-id="9cf4b-107">EXAMPLES</span></span>

## <span data-ttu-id="9cf4b-108">參數</span><span class="sxs-lookup"><span data-stu-id="9cf4b-108">PARAMETERS</span></span>

### <span data-ttu-id="9cf4b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf4b-109">-DefaultProfile</span></span>
<span data-ttu-id="9cf4b-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9cf4b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cf4b-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="9cf4b-111">-Name</span></span>
<span data-ttu-id="9cf4b-112">指定 Azure 網站復原結構的名稱</span><span class="sxs-lookup"><span data-stu-id="9cf4b-112">Specifies the name of the Azure Site Recovery Fabric</span></span>

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

### <span data-ttu-id="9cf4b-113">-類型</span><span class="sxs-lookup"><span data-stu-id="9cf4b-113">-Type</span></span>
<span data-ttu-id="9cf4b-114">指定 Azure Site Recovery 結構類型。</span><span class="sxs-lookup"><span data-stu-id="9cf4b-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf4b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf4b-115">CommonParameters</span></span>
<span data-ttu-id="9cf4b-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9cf4b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf4b-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9cf4b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf4b-118">輸入</span><span class="sxs-lookup"><span data-stu-id="9cf4b-118">INPUTS</span></span>

### <span data-ttu-id="9cf4b-119">所有</span><span class="sxs-lookup"><span data-stu-id="9cf4b-119">None</span></span>
<span data-ttu-id="9cf4b-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9cf4b-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9cf4b-121">輸出</span><span class="sxs-lookup"><span data-stu-id="9cf4b-121">OUTPUTS</span></span>

### <span data-ttu-id="9cf4b-122">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="9cf4b-122">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9cf4b-123">筆記</span><span class="sxs-lookup"><span data-stu-id="9cf4b-123">NOTES</span></span>

## <span data-ttu-id="9cf4b-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cf4b-124">RELATED LINKS</span></span>

[<span data-ttu-id="9cf4b-125">AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="9cf4b-125">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="9cf4b-126">移除-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="9cf4b-126">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
