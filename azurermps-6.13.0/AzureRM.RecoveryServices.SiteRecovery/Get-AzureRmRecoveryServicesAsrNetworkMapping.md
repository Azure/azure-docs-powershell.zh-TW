---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: d85de944742d7ad265c1e7e979dddb15808df95e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451087"
---
# <span data-ttu-id="fdabb-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fdabb-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="fdabb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fdabb-102">SYNOPSIS</span></span>
<span data-ttu-id="fdabb-103">取得目前電子倉庫之網站復原網路對應的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fdabb-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdabb-104">句法</span><span class="sxs-lookup"><span data-stu-id="fdabb-104">SYNTAX</span></span>

### <span data-ttu-id="fdabb-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="fdabb-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdabb-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="fdabb-106">ByFabricObject</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdabb-107">說明</span><span class="sxs-lookup"><span data-stu-id="fdabb-107">DESCRIPTION</span></span>
<span data-ttu-id="fdabb-108">**AzureRmRecoveryServicesAsrNetworkMapping** Cmdlet 會取得有關恢復服務電子倉庫之 Azure Site Recovery 網路對應的資訊。</span><span class="sxs-lookup"><span data-stu-id="fdabb-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="fdabb-109">示例</span><span class="sxs-lookup"><span data-stu-id="fdabb-109">EXAMPLES</span></span>

### <span data-ttu-id="fdabb-110">範例1</span><span class="sxs-lookup"><span data-stu-id="fdabb-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="fdabb-111">取得已傳送網路的所有網路對應。</span><span class="sxs-lookup"><span data-stu-id="fdabb-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="fdabb-112">範例2</span><span class="sxs-lookup"><span data-stu-id="fdabb-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="fdabb-113">在指定的 azure 網站復原結構中取得已提供名稱的網路對應。</span><span class="sxs-lookup"><span data-stu-id="fdabb-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="fdabb-114">參數</span><span class="sxs-lookup"><span data-stu-id="fdabb-114">PARAMETERS</span></span>

### <span data-ttu-id="fdabb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdabb-115">-DefaultProfile</span></span>
<span data-ttu-id="fdabb-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fdabb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fdabb-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fdabb-117">-Name</span></span>
<span data-ttu-id="fdabb-118">要取得之 ASR 網路對應物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdabb-118">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="fdabb-119">-網路</span><span class="sxs-lookup"><span data-stu-id="fdabb-119">-Network</span></span>
<span data-ttu-id="fdabb-120">取得與指定的網路 ASR 物件相對應的 ASR 網路對應。</span><span class="sxs-lookup"><span data-stu-id="fdabb-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdabb-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="fdabb-121">-PrimaryFabric</span></span>
<span data-ttu-id="fdabb-122">取得與指定的主要結構物件相對應的 ASR 網路對應。</span><span class="sxs-lookup"><span data-stu-id="fdabb-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdabb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdabb-123">CommonParameters</span></span>
<span data-ttu-id="fdabb-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fdabb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdabb-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fdabb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdabb-126">輸入</span><span class="sxs-lookup"><span data-stu-id="fdabb-126">INPUTS</span></span>

### <span data-ttu-id="fdabb-127">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="fdabb-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="fdabb-128">輸出</span><span class="sxs-lookup"><span data-stu-id="fdabb-128">OUTPUTS</span></span>

### <span data-ttu-id="fdabb-129">System.object. IEnumerable "1 [ASRNetworkMapping，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="fdabb-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fdabb-130">筆記</span><span class="sxs-lookup"><span data-stu-id="fdabb-130">NOTES</span></span>

## <span data-ttu-id="fdabb-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="fdabb-131">RELATED LINKS</span></span>

[<span data-ttu-id="fdabb-132">新-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fdabb-132">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="fdabb-133">移除-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fdabb-133">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
