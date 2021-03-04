---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: c309b855b6ae8491e8b4a97301a902367a5377e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908366"
---
# <span data-ttu-id="fd4b7-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fd4b7-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="fd4b7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fd4b7-102">SYNOPSIS</span></span>
<span data-ttu-id="fd4b7-103">獲得目前儲存庫的網站復原網路地圖相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fd4b7-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="fd4b7-104">語法</span><span class="sxs-lookup"><span data-stu-id="fd4b7-104">SYNTAX</span></span>

### <span data-ttu-id="fd4b7-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="fd4b7-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd4b7-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="fd4b7-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd4b7-107">描述</span><span class="sxs-lookup"><span data-stu-id="fd4b7-107">DESCRIPTION</span></span>
<span data-ttu-id="fd4b7-108">**Get-AzRecoveryServicesAsrNetworkMapping** Cmdlet 會取得復原服務庫的 Azure 網站修復網路地圖相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fd4b7-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="fd4b7-109">例子</span><span class="sxs-lookup"><span data-stu-id="fd4b7-109">EXAMPLES</span></span>

### <span data-ttu-id="fd4b7-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="fd4b7-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="fd4b7-111">為傳遞的網路獲取所有網路地圖。</span><span class="sxs-lookup"><span data-stu-id="fd4b7-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="fd4b7-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="fd4b7-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="fd4b7-113">在指定的 Azure 網站復原結構中，以提供的名稱進行網路地圖。</span><span class="sxs-lookup"><span data-stu-id="fd4b7-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="fd4b7-114">參數</span><span class="sxs-lookup"><span data-stu-id="fd4b7-114">PARAMETERS</span></span>

### <span data-ttu-id="fd4b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd4b7-115">-DefaultProfile</span></span>
<span data-ttu-id="fd4b7-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd4b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd4b7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd4b7-117">-Name</span></span>
<span data-ttu-id="fd4b7-118">要取得之 ASR 網路地圖物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd4b7-118">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="fd4b7-119">-網路</span><span class="sxs-lookup"><span data-stu-id="fd4b7-119">-Network</span></span>
<span data-ttu-id="fd4b7-120">取得對應到指定網路 ASR 物件的 ASR 網路對應。</span><span class="sxs-lookup"><span data-stu-id="fd4b7-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

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

### <span data-ttu-id="fd4b7-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="fd4b7-121">-PrimaryFabric</span></span>
<span data-ttu-id="fd4b7-122">取得對應到指定主要結構物件的 ASR 網路對應。</span><span class="sxs-lookup"><span data-stu-id="fd4b7-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

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

### <span data-ttu-id="fd4b7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd4b7-123">CommonParameters</span></span>
<span data-ttu-id="fd4b7-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fd4b7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd4b7-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd4b7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd4b7-126">輸入</span><span class="sxs-lookup"><span data-stu-id="fd4b7-126">INPUTS</span></span>

### <span data-ttu-id="fd4b7-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="fd4b7-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="fd4b7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="fd4b7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="fd4b7-129">輸出</span><span class="sxs-lookup"><span data-stu-id="fd4b7-129">OUTPUTS</span></span>

### <span data-ttu-id="fd4b7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fd4b7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="fd4b7-131">筆記</span><span class="sxs-lookup"><span data-stu-id="fd4b7-131">NOTES</span></span>

## <span data-ttu-id="fd4b7-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd4b7-132">RELATED LINKS</span></span>

[<span data-ttu-id="fd4b7-133">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fd4b7-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="fd4b7-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fd4b7-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
