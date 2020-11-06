---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 11CE6244-D287-4B99-9585-E3EA2D36A4F9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 44addca6ee4f658f4cc6f8081e0f7a0c39ba4a58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452343"
---
# <span data-ttu-id="13ec4-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="13ec4-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="13ec4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13ec4-102">SYNOPSIS</span></span>
<span data-ttu-id="13ec4-103">將原則與保護容器產生關聯，以建立 Azure Site Recovery 保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="13ec4-103">Creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13ec4-104">句法</span><span class="sxs-lookup"><span data-stu-id="13ec4-104">SYNTAX</span></span>

### <span data-ttu-id="13ec4-105">EnterpriseToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="13ec4-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13ec4-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="13ec4-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13ec4-107">說明</span><span class="sxs-lookup"><span data-stu-id="13ec4-107">DESCRIPTION</span></span>
<span data-ttu-id="13ec4-108">**新的-AzureRmSiteRecoveryProtectionContainerMapping** Cmdlet 會將原則與保護容器產生關聯，以建立 Azure Site Recovery 保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="13ec4-108">The **New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

## <span data-ttu-id="13ec4-109">示例</span><span class="sxs-lookup"><span data-stu-id="13ec4-109">EXAMPLES</span></span>

## <span data-ttu-id="13ec4-110">參數</span><span class="sxs-lookup"><span data-stu-id="13ec4-110">PARAMETERS</span></span>

### <span data-ttu-id="13ec4-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="13ec4-111">-Name</span></span>
<span data-ttu-id="13ec4-112">指定保護容器對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="13ec4-112">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ec4-113">-原則</span><span class="sxs-lookup"><span data-stu-id="13ec4-113">-Policy</span></span>
<span data-ttu-id="13ec4-114">指定 Azure Site Recovery 策略物件。</span><span class="sxs-lookup"><span data-stu-id="13ec4-114">Specifies the Azure Site Recovery Policy object.</span></span>

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

### <span data-ttu-id="13ec4-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="13ec4-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="13ec4-116">指定主要保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="13ec4-116">Specifies the primary Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ec4-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="13ec4-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="13ec4-118">指定復原保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="13ec4-118">Specifies the Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ec4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ec4-119">-DefaultProfile</span></span>
<span data-ttu-id="13ec4-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="13ec4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13ec4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ec4-121">CommonParameters</span></span>
<span data-ttu-id="13ec4-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13ec4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ec4-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13ec4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ec4-124">輸入</span><span class="sxs-lookup"><span data-stu-id="13ec4-124">INPUTS</span></span>

### <span data-ttu-id="13ec4-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="13ec4-125">ASRPolicy</span></span>
<span data-ttu-id="13ec4-126">形參 "Policy" 接受管線中 "ASRPolicy" 類型的值</span><span class="sxs-lookup"><span data-stu-id="13ec4-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="13ec4-127">輸出</span><span class="sxs-lookup"><span data-stu-id="13ec4-127">OUTPUTS</span></span>

### <span data-ttu-id="13ec4-128">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="13ec4-128">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="13ec4-129">筆記</span><span class="sxs-lookup"><span data-stu-id="13ec4-129">NOTES</span></span>

## <span data-ttu-id="13ec4-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="13ec4-130">RELATED LINKS</span></span>

[<span data-ttu-id="13ec4-131">AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="13ec4-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="13ec4-132">移除-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="13ec4-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
