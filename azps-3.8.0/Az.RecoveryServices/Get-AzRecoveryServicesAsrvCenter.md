---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 49adcdefac7fe3f06cfd9678137dd58cff021f52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956837"
---
# <span data-ttu-id="d5536-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="d5536-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="d5536-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5536-102">SYNOPSIS</span></span>
<span data-ttu-id="d5536-103">取得在 ASR 結構指定之設定伺服器上登錄探索的 vCenter 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d5536-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="d5536-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5536-104">SYNTAX</span></span>

### <span data-ttu-id="d5536-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="d5536-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5536-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d5536-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5536-107">ByName</span><span class="sxs-lookup"><span data-stu-id="d5536-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5536-108">說明</span><span class="sxs-lookup"><span data-stu-id="d5536-108">DESCRIPTION</span></span>
<span data-ttu-id="d5536-109">**AzRecoveryServicesAsrvCenter** Cmdlet 會取得在 ASR 結構指定的設定伺服器上註冊探索的 vCenter 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d5536-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="d5536-110">示例</span><span class="sxs-lookup"><span data-stu-id="d5536-110">EXAMPLES</span></span>

### <span data-ttu-id="d5536-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d5536-111">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

FriendlyName          : inmtest81
Server                : 10.150.209.27
Port                  : 443
Name                  : inmtest81
ID                    : /Subscriptions/xxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxx/replicationvCenters/inmtest81
FabricArmResourceName : d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9
ProcessServerId       : 526C9B6C-4039-D841-97A92FB0BD153B53
AccountId             : 2
DiscoveryStatus       : Pending
LastHeartbeat         :
```

<span data-ttu-id="d5536-112">根據 fabric name 和 vCenter 的名稱，取得 azure site recovery vCenter。</span><span class="sxs-lookup"><span data-stu-id="d5536-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="d5536-113">範例2</span><span class="sxs-lookup"><span data-stu-id="d5536-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="d5536-114">透過 fabric name 取得 azure site recovery vCenter 清單。</span><span class="sxs-lookup"><span data-stu-id="d5536-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="d5536-115">參數</span><span class="sxs-lookup"><span data-stu-id="d5536-115">PARAMETERS</span></span>

### <span data-ttu-id="d5536-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5536-116">-DefaultProfile</span></span>
<span data-ttu-id="d5536-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5536-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5536-118">-結構</span><span class="sxs-lookup"><span data-stu-id="d5536-118">-Fabric</span></span>
<span data-ttu-id="d5536-119">代表佈建服務器的 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="d5536-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5536-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d5536-120">-Name</span></span>
<span data-ttu-id="d5536-121">VCenter 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5536-121">Name of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5536-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5536-122">-ResourceId</span></span>
<span data-ttu-id="d5536-123">指定 vCenter 的 resourceId。</span><span class="sxs-lookup"><span data-stu-id="d5536-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5536-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5536-124">CommonParameters</span></span>
<span data-ttu-id="d5536-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5536-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5536-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d5536-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5536-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d5536-127">INPUTS</span></span>

### <span data-ttu-id="d5536-128">System.object</span><span class="sxs-lookup"><span data-stu-id="d5536-128">System.String</span></span>

### <span data-ttu-id="d5536-129">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d5536-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d5536-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d5536-130">OUTPUTS</span></span>

### <span data-ttu-id="d5536-131">RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="d5536-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="d5536-132">筆記</span><span class="sxs-lookup"><span data-stu-id="d5536-132">NOTES</span></span>

## <span data-ttu-id="d5536-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5536-133">RELATED LINKS</span></span>
