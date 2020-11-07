---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3DDC8DD8-889C-4C76-B32E-3D2C2AD0AC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverypolicyassociationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
ms.openlocfilehash: 140bec7738d107574db5d0d157cc3f8cfac46583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625399"
---
# <span data-ttu-id="801bb-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span><span class="sxs-lookup"><span data-stu-id="801bb-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span></span>

## <span data-ttu-id="801bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="801bb-102">SYNOPSIS</span></span>
<span data-ttu-id="801bb-103">啟動網站恢復複製原則關聯作業。</span><span class="sxs-lookup"><span data-stu-id="801bb-103">Starts a Site Recovery replication policy association job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="801bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="801bb-104">SYNTAX</span></span>

### <span data-ttu-id="801bb-105">EnterpriseToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="801bb-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="801bb-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="801bb-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="801bb-107">說明</span><span class="sxs-lookup"><span data-stu-id="801bb-107">DESCRIPTION</span></span>
<span data-ttu-id="801bb-108">**AzureRmSiteRecoveryPolicyAssociationJob** Cmdlet 會啟動關聯作業，以將複製原則與 Azure Site Recovery 保護容器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="801bb-108">The **Start-AzureRmSiteRecoveryPolicyAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="801bb-109">示例</span><span class="sxs-lookup"><span data-stu-id="801bb-109">EXAMPLES</span></span>

## <span data-ttu-id="801bb-110">參數</span><span class="sxs-lookup"><span data-stu-id="801bb-110">PARAMETERS</span></span>

### <span data-ttu-id="801bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="801bb-111">-DefaultProfile</span></span>
<span data-ttu-id="801bb-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="801bb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="801bb-113">-原則</span><span class="sxs-lookup"><span data-stu-id="801bb-113">-Policy</span></span>
<span data-ttu-id="801bb-114">指定網站恢復原則物件。</span><span class="sxs-lookup"><span data-stu-id="801bb-114">Specifies the Site Recovery policy object.</span></span>

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

### <span data-ttu-id="801bb-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="801bb-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="801bb-116">指定要套用保護設定檔設定的主要保護容器。</span><span class="sxs-lookup"><span data-stu-id="801bb-116">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

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

### <span data-ttu-id="801bb-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="801bb-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="801bb-118">指定要套用保護設定檔設定的復原保護容器。</span><span class="sxs-lookup"><span data-stu-id="801bb-118">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

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

### <span data-ttu-id="801bb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="801bb-119">CommonParameters</span></span>
<span data-ttu-id="801bb-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="801bb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="801bb-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="801bb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="801bb-122">輸入</span><span class="sxs-lookup"><span data-stu-id="801bb-122">INPUTS</span></span>

### <span data-ttu-id="801bb-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="801bb-123">ASRPolicy</span></span>
<span data-ttu-id="801bb-124">形參 "Policy" 接受管線中 "ASRPolicy" 類型的值</span><span class="sxs-lookup"><span data-stu-id="801bb-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="801bb-125">輸出</span><span class="sxs-lookup"><span data-stu-id="801bb-125">OUTPUTS</span></span>

### <span data-ttu-id="801bb-126">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="801bb-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="801bb-127">筆記</span><span class="sxs-lookup"><span data-stu-id="801bb-127">NOTES</span></span>

## <span data-ttu-id="801bb-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="801bb-128">RELATED LINKS</span></span>

