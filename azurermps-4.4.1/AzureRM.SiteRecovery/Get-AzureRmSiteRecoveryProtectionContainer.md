---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 77F1556C-323D-49CA-BD6C-75B2D4E0F894
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
ms.openlocfilehash: 2595d8feaa01c2f3ccd9f16ca193be195a8e303a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455591"
---
# <span data-ttu-id="3dcda-101">Get-AzureRmSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3dcda-101">Get-AzureRmSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="3dcda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3dcda-102">SYNOPSIS</span></span>
<span data-ttu-id="3dcda-103">取得目前網站恢復電子倉庫的保護容器。</span><span class="sxs-lookup"><span data-stu-id="3dcda-103">Gets protection containers for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dcda-104">句法</span><span class="sxs-lookup"><span data-stu-id="3dcda-104">SYNTAX</span></span>

### <span data-ttu-id="3dcda-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="3dcda-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dcda-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="3dcda-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dcda-107">ByObjectWithNameLegacy</span><span class="sxs-lookup"><span data-stu-id="3dcda-107">ByObjectWithNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3dcda-108">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3dcda-108">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dcda-109">ByObjectWithFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="3dcda-109">ByObjectWithFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3dcda-110">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="3dcda-110">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3dcda-111">說明</span><span class="sxs-lookup"><span data-stu-id="3dcda-111">DESCRIPTION</span></span>
<span data-ttu-id="3dcda-112">**AzureRmSiteRecoveryProtectionContainer** Cmdlet 會取得目前 Azure Site Recovery 保存庫的保護容器。</span><span class="sxs-lookup"><span data-stu-id="3dcda-112">The **Get-AzureRmSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="3dcda-113">保護容器是受保護物件（例如虛擬電腦）的邏輯容器。</span><span class="sxs-lookup"><span data-stu-id="3dcda-113">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="3dcda-114">保護原則定義受保護專案的複製設定，而且可以與保護容器相關聯，並套用到受保護的實體。</span><span class="sxs-lookup"><span data-stu-id="3dcda-114">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="3dcda-115">示例</span><span class="sxs-lookup"><span data-stu-id="3dcda-115">EXAMPLES</span></span>

## <span data-ttu-id="3dcda-116">參數</span><span class="sxs-lookup"><span data-stu-id="3dcda-116">PARAMETERS</span></span>

### <span data-ttu-id="3dcda-117">-結構</span><span class="sxs-lookup"><span data-stu-id="3dcda-117">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName, ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dcda-118">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3dcda-118">-FriendlyName</span></span>
<span data-ttu-id="3dcda-119">指定保護容器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="3dcda-119">Specifies the friendly name of the protection container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName, ByObjectWithFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcda-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="3dcda-120">-Name</span></span>
<span data-ttu-id="3dcda-121">指定保護容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3dcda-121">Specifies the name of the protection container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName, ByObjectWithNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcda-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dcda-122">-DefaultProfile</span></span>
<span data-ttu-id="3dcda-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3dcda-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dcda-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dcda-124">CommonParameters</span></span>
<span data-ttu-id="3dcda-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3dcda-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dcda-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3dcda-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dcda-127">輸入</span><span class="sxs-lookup"><span data-stu-id="3dcda-127">INPUTS</span></span>

### <span data-ttu-id="3dcda-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="3dcda-128">ASRFabric</span></span>
<span data-ttu-id="3dcda-129">形參 "Fabric" 接受來自管線的 "ASRFabric" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3dcda-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="3dcda-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3dcda-130">OUTPUTS</span></span>

### <span data-ttu-id="3dcda-131">System.object. IEnumerable ' 1 [SiteRecovery. ASRProtectionContainer] （）</span><span class="sxs-lookup"><span data-stu-id="3dcda-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer]</span></span>

## <span data-ttu-id="3dcda-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3dcda-132">NOTES</span></span>

## <span data-ttu-id="3dcda-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="3dcda-133">RELATED LINKS</span></span>

