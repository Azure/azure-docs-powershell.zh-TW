---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 11CE6244-D287-4B99-9585-E3EA2D36A4F9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 950c5c8e2007568add1aba1122356de670884c07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454028"
---
# <span data-ttu-id="81ac5-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="81ac5-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="81ac5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81ac5-102">SYNOPSIS</span></span>
<span data-ttu-id="81ac5-103">將原則與保護容器產生關聯，以建立 Azure Site Recovery 保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="81ac5-103">Creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81ac5-104">句法</span><span class="sxs-lookup"><span data-stu-id="81ac5-104">SYNTAX</span></span>

### <span data-ttu-id="81ac5-105">EnterpriseToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="81ac5-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81ac5-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="81ac5-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81ac5-107">說明</span><span class="sxs-lookup"><span data-stu-id="81ac5-107">DESCRIPTION</span></span>
<span data-ttu-id="81ac5-108">**新的-AzureRmSiteRecoveryProtectionContainerMapping** Cmdlet 會將原則與保護容器產生關聯，以建立 Azure Site Recovery 保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="81ac5-108">The **New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

## <span data-ttu-id="81ac5-109">示例</span><span class="sxs-lookup"><span data-stu-id="81ac5-109">EXAMPLES</span></span>

## <span data-ttu-id="81ac5-110">參數</span><span class="sxs-lookup"><span data-stu-id="81ac5-110">PARAMETERS</span></span>

### <span data-ttu-id="81ac5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ac5-111">-DefaultProfile</span></span>
<span data-ttu-id="81ac5-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81ac5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81ac5-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="81ac5-113">-Name</span></span>
<span data-ttu-id="81ac5-114">指定保護容器對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="81ac5-114">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="81ac5-115">-原則</span><span class="sxs-lookup"><span data-stu-id="81ac5-115">-Policy</span></span>
<span data-ttu-id="81ac5-116">指定 Azure Site Recovery 策略物件。</span><span class="sxs-lookup"><span data-stu-id="81ac5-116">Specifies the Azure Site Recovery Policy object.</span></span>

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

### <span data-ttu-id="81ac5-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="81ac5-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="81ac5-118">指定主要保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="81ac5-118">Specifies the primary Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ac5-119">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="81ac5-119">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="81ac5-120">指定復原保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="81ac5-120">Specifies the Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ac5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ac5-121">CommonParameters</span></span>
<span data-ttu-id="81ac5-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81ac5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ac5-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81ac5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ac5-124">輸入</span><span class="sxs-lookup"><span data-stu-id="81ac5-124">INPUTS</span></span>

### <span data-ttu-id="81ac5-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="81ac5-125">ASRPolicy</span></span>
<span data-ttu-id="81ac5-126">形參 "Policy" 接受管線中 "ASRPolicy" 類型的值</span><span class="sxs-lookup"><span data-stu-id="81ac5-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="81ac5-127">輸出</span><span class="sxs-lookup"><span data-stu-id="81ac5-127">OUTPUTS</span></span>

### <span data-ttu-id="81ac5-128">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="81ac5-128">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="81ac5-129">筆記</span><span class="sxs-lookup"><span data-stu-id="81ac5-129">NOTES</span></span>

## <span data-ttu-id="81ac5-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="81ac5-130">RELATED LINKS</span></span>

[<span data-ttu-id="81ac5-131">AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="81ac5-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="81ac5-132">移除-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="81ac5-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
