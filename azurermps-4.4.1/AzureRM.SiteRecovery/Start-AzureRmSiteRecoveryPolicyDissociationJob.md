---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4F71DC85-B2E0-4E0B-96F6-69D52C577B22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
ms.openlocfilehash: 7dc64ea2bdbfb5dcbc648143dd094313eb765782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447940"
---
# <span data-ttu-id="7bba6-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span><span class="sxs-lookup"><span data-stu-id="7bba6-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span></span>

## <span data-ttu-id="7bba6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7bba6-102">SYNOPSIS</span></span>
<span data-ttu-id="7bba6-103">在與網站復原保護容器相關聯的複寫原則上啟動 dissociation 作業。</span><span class="sxs-lookup"><span data-stu-id="7bba6-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bba6-104">句法</span><span class="sxs-lookup"><span data-stu-id="7bba6-104">SYNTAX</span></span>

### <span data-ttu-id="7bba6-105">EnterpriseToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="7bba6-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7bba6-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="7bba6-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bba6-107">說明</span><span class="sxs-lookup"><span data-stu-id="7bba6-107">DESCRIPTION</span></span>
<span data-ttu-id="7bba6-108">**AzureRmSiteRecoveryPolicyDissociationJob** Cmdlet 會在與 Azure Site Recovery 保護容器相關聯的複寫原則上啟動 dissociation 作業。</span><span class="sxs-lookup"><span data-stu-id="7bba6-108">The **Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="7bba6-109">示例</span><span class="sxs-lookup"><span data-stu-id="7bba6-109">EXAMPLES</span></span>

## <span data-ttu-id="7bba6-110">參數</span><span class="sxs-lookup"><span data-stu-id="7bba6-110">PARAMETERS</span></span>

### <span data-ttu-id="7bba6-111">-原則</span><span class="sxs-lookup"><span data-stu-id="7bba6-111">-Policy</span></span>
<span data-ttu-id="7bba6-112">指定 Azure Site Recovery 策略物件。</span><span class="sxs-lookup"><span data-stu-id="7bba6-112">Specifies an Azure Site Recovery policy object.</span></span>

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

### <span data-ttu-id="7bba6-113">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7bba6-113">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="7bba6-114">指定主要保護容器。</span><span class="sxs-lookup"><span data-stu-id="7bba6-114">Specifies a primary protection container.</span></span>

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

### <span data-ttu-id="7bba6-115">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7bba6-115">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="7bba6-116">指定復原保護容器。</span><span class="sxs-lookup"><span data-stu-id="7bba6-116">Specifies a recovery protection container.</span></span>

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

### <span data-ttu-id="7bba6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bba6-117">-DefaultProfile</span></span>
<span data-ttu-id="7bba6-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7bba6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bba6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bba6-119">CommonParameters</span></span>
<span data-ttu-id="7bba6-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7bba6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bba6-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7bba6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bba6-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7bba6-122">INPUTS</span></span>

### <span data-ttu-id="7bba6-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="7bba6-123">ASRPolicy</span></span>
<span data-ttu-id="7bba6-124">形參 "Policy" 接受管線中 "ASRPolicy" 類型的值</span><span class="sxs-lookup"><span data-stu-id="7bba6-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="7bba6-125">輸出</span><span class="sxs-lookup"><span data-stu-id="7bba6-125">OUTPUTS</span></span>

### <span data-ttu-id="7bba6-126">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7bba6-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7bba6-127">筆記</span><span class="sxs-lookup"><span data-stu-id="7bba6-127">NOTES</span></span>

## <span data-ttu-id="7bba6-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bba6-128">RELATED LINKS</span></span>

