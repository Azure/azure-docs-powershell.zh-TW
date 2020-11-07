---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 01AE09A8-B779-475A-9E86-776E0774E89E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 1e7e53d4f14649ac5cb8691a1e3d938809658771
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625435"
---
# <span data-ttu-id="cac24-101">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cac24-101">Get-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="cac24-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cac24-102">SYNOPSIS</span></span>
<span data-ttu-id="cac24-103">取得目前電子倉庫之網站復原網路對應的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cac24-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cac24-104">句法</span><span class="sxs-lookup"><span data-stu-id="cac24-104">SYNTAX</span></span>

### <span data-ttu-id="cac24-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="cac24-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cac24-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="cac24-106">EnterpriseToEnterprise</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cac24-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="cac24-107">EnterpriseToAzure</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> [-Azure]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cac24-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="cac24-108">EnterpriseToAzureLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-Azure] -PrimaryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cac24-109">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="cac24-109">EnterpriseToEnterpriseLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cac24-110">說明</span><span class="sxs-lookup"><span data-stu-id="cac24-110">DESCRIPTION</span></span>
<span data-ttu-id="cac24-111">**AzureRmSiteRecoveryNetworkMapping** Cmdlet 會取得目前網站復原電子倉庫的 Azure 網站復原網路對應的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cac24-111">The **Get-AzureRmSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="cac24-112">示例</span><span class="sxs-lookup"><span data-stu-id="cac24-112">EXAMPLES</span></span>

## <span data-ttu-id="cac24-113">參數</span><span class="sxs-lookup"><span data-stu-id="cac24-113">PARAMETERS</span></span>

### <span data-ttu-id="cac24-114">-Azure</span><span class="sxs-lookup"><span data-stu-id="cac24-114">-Azure</span></span>
<span data-ttu-id="cac24-115">指出命令在對應至 Azure 虛擬網路的主要伺服器上取得網路的網路對應清單。</span><span class="sxs-lookup"><span data-stu-id="cac24-115">Indicates that the command gets a list of network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cac24-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac24-116">-DefaultProfile</span></span>
<span data-ttu-id="cac24-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cac24-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cac24-118">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="cac24-118">-PrimaryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cac24-119">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="cac24-119">-PrimaryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToAzureLegacy, EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cac24-120">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="cac24-120">-RecoveryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cac24-121">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="cac24-121">-RecoveryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cac24-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac24-122">CommonParameters</span></span>
<span data-ttu-id="cac24-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cac24-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac24-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cac24-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac24-125">輸入</span><span class="sxs-lookup"><span data-stu-id="cac24-125">INPUTS</span></span>

### <span data-ttu-id="cac24-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="cac24-126">ASRFabric</span></span>
<span data-ttu-id="cac24-127">形參 "PrimaryFabric" 接受管線中 "ASRFabric" 類型的值</span><span class="sxs-lookup"><span data-stu-id="cac24-127">Parameter 'PrimaryFabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="cac24-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="cac24-128">ASRServer</span></span>
<span data-ttu-id="cac24-129">形參 "PrimaryServer" 接受管線中 "ASRServer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="cac24-129">Parameter 'PrimaryServer' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="cac24-130">輸出</span><span class="sxs-lookup"><span data-stu-id="cac24-130">OUTPUTS</span></span>

### <span data-ttu-id="cac24-131">System.object. IEnumerable ' 1 [SiteRecovery. ASRNetworkMapping] （）</span><span class="sxs-lookup"><span data-stu-id="cac24-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping]</span></span>

## <span data-ttu-id="cac24-132">筆記</span><span class="sxs-lookup"><span data-stu-id="cac24-132">NOTES</span></span>

## <span data-ttu-id="cac24-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="cac24-133">RELATED LINKS</span></span>

[<span data-ttu-id="cac24-134">新-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cac24-134">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="cac24-135">移除-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cac24-135">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
