---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4BF1E20A-46EA-48E2-8C7A-F121AE6815AF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 1b01fef6563fef97f78913f916a6481acd6f6ed3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625954"
---
# <span data-ttu-id="ea8b8-101">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="ea8b8-101">New-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="ea8b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea8b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8b8-103">在虛擬網路之間建立對應。</span><span class="sxs-lookup"><span data-stu-id="ea8b8-103">Creates a mapping between virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea8b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="ea8b8-104">SYNTAX</span></span>

### <span data-ttu-id="ea8b8-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="ea8b8-105">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea8b8-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="ea8b8-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork> -AzureVMNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea8b8-107">說明</span><span class="sxs-lookup"><span data-stu-id="ea8b8-107">DESCRIPTION</span></span>
<span data-ttu-id="ea8b8-108">**新的-AzureRMSiteRecoveryNetworkMapping** Cmdlet 會在兩個虛擬網路之間建立對應，並傳回 Azure Site Recovery 作業來進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="ea8b8-108">The **New-AzureRMSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="ea8b8-109">示例</span><span class="sxs-lookup"><span data-stu-id="ea8b8-109">EXAMPLES</span></span>

## <span data-ttu-id="ea8b8-110">參數</span><span class="sxs-lookup"><span data-stu-id="ea8b8-110">PARAMETERS</span></span>

### <span data-ttu-id="ea8b8-111">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="ea8b8-111">-AzureVMNetworkId</span></span>
<span data-ttu-id="ea8b8-112">指定 Azure 虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="ea8b8-112">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8b8-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea8b8-113">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8b8-114">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="ea8b8-114">-PrimaryNetwork</span></span>
<span data-ttu-id="ea8b8-115">指定主要網路物件。</span><span class="sxs-lookup"><span data-stu-id="ea8b8-115">Specifies the primary network object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8b8-116">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="ea8b8-116">-RecoveryNetwork</span></span>
<span data-ttu-id="ea8b8-117">指定復原網路物件。</span><span class="sxs-lookup"><span data-stu-id="ea8b8-117">Specifies the recovery network object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea8b8-118">-DefaultProfile</span></span>
<span data-ttu-id="ea8b8-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea8b8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea8b8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8b8-120">CommonParameters</span></span>
<span data-ttu-id="ea8b8-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea8b8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8b8-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ea8b8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8b8-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ea8b8-123">INPUTS</span></span>

### <span data-ttu-id="ea8b8-124">ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="ea8b8-124">ASRNetwork</span></span>
<span data-ttu-id="ea8b8-125">形參 "PrimaryNetwork" 接受管線中 "ASRNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ea8b8-125">Parameter 'PrimaryNetwork' accepts value of type 'ASRNetwork' from the pipeline</span></span>

## <span data-ttu-id="ea8b8-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ea8b8-126">OUTPUTS</span></span>

### <span data-ttu-id="ea8b8-127">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ea8b8-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ea8b8-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ea8b8-128">NOTES</span></span>

## <span data-ttu-id="ea8b8-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea8b8-129">RELATED LINKS</span></span>

[<span data-ttu-id="ea8b8-130">AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="ea8b8-130">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="ea8b8-131">移除-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="ea8b8-131">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
