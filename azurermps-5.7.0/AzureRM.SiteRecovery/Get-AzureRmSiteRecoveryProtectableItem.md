---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BE2D05F5-70CE-4EAA-9363-6CA89A312DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
ms.openlocfilehash: 2a857c538188c2b9ddf7516ccebda291f3161e1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454063"
---
# <span data-ttu-id="7d4ec-101">Get-AzureRmSiteRecoveryProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7d4ec-101">Get-AzureRmSiteRecoveryProtectableItem</span></span>

## <span data-ttu-id="7d4ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d4ec-102">SYNOPSIS</span></span>
<span data-ttu-id="7d4ec-103">在保護容器中取得能存取的專案。</span><span class="sxs-lookup"><span data-stu-id="7d4ec-103">Get the protectable items in a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d4ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d4ec-104">SYNTAX</span></span>

### <span data-ttu-id="7d4ec-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="7d4ec-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d4ec-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="7d4ec-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d4ec-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7d4ec-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d4ec-108">說明</span><span class="sxs-lookup"><span data-stu-id="7d4ec-108">DESCRIPTION</span></span>
<span data-ttu-id="7d4ec-109">**AzureRmSiteRecoveryProtectableItem** Cmdlet 會取得 Azure Site Recovery 保護容器中的可保護專案。</span><span class="sxs-lookup"><span data-stu-id="7d4ec-109">The **Get-AzureRmSiteRecoveryProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="7d4ec-110">示例</span><span class="sxs-lookup"><span data-stu-id="7d4ec-110">EXAMPLES</span></span>

## <span data-ttu-id="7d4ec-111">參數</span><span class="sxs-lookup"><span data-stu-id="7d4ec-111">PARAMETERS</span></span>

### <span data-ttu-id="7d4ec-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d4ec-112">-DefaultProfile</span></span>
<span data-ttu-id="7d4ec-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d4ec-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d4ec-114">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7d4ec-114">-FriendlyName</span></span>
<span data-ttu-id="7d4ec-115">指定 Azure 網站復原能保護專案的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="7d4ec-115">Specifies the friendly name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4ec-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d4ec-116">-Name</span></span>
<span data-ttu-id="7d4ec-117">指定 Azure 網站復原的 [復原] 專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d4ec-117">Specifies the name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4ec-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7d4ec-118">-ProtectionContainer</span></span>
<span data-ttu-id="7d4ec-119">指定 Azure Site Recovery 保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="7d4ec-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d4ec-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d4ec-120">CommonParameters</span></span>
<span data-ttu-id="7d4ec-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d4ec-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d4ec-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d4ec-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d4ec-123">輸入</span><span class="sxs-lookup"><span data-stu-id="7d4ec-123">INPUTS</span></span>

### <span data-ttu-id="7d4ec-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7d4ec-124">ASRProtectionContainer</span></span>
<span data-ttu-id="7d4ec-125">形參 "ProtectionContainer" 接受管線中 "ASRProtectionContainer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="7d4ec-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="7d4ec-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7d4ec-126">OUTPUTS</span></span>

### <span data-ttu-id="7d4ec-127">System.object. IEnumerable "1 [ASRProtectableItem，SiteRecovery，Version = 2.0.1.0，Culture = 中性，PublicKeyToken = null]] （SiteRecovery =，Culture = 中立）</span><span class="sxs-lookup"><span data-stu-id="7d4ec-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7d4ec-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7d4ec-128">NOTES</span></span>

## <span data-ttu-id="7d4ec-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d4ec-129">RELATED LINKS</span></span>

[<span data-ttu-id="7d4ec-130">AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7d4ec-130">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="7d4ec-131">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7d4ec-131">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
