---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: eb358a0caf2b1ea5ccba8d92c39562d2c39706c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913137"
---
# <span data-ttu-id="57230-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="57230-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="57230-102">簡介</span><span class="sxs-lookup"><span data-stu-id="57230-102">SYNOPSIS</span></span>
<span data-ttu-id="57230-103">在 ASR 結構指定的 Configuration 伺服器上，獲得註冊用於探索的 vCenter 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="57230-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="57230-104">語法</span><span class="sxs-lookup"><span data-stu-id="57230-104">SYNTAX</span></span>

### <span data-ttu-id="57230-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="57230-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57230-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="57230-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57230-107">ByName</span><span class="sxs-lookup"><span data-stu-id="57230-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57230-108">描述</span><span class="sxs-lookup"><span data-stu-id="57230-108">DESCRIPTION</span></span>
<span data-ttu-id="57230-109">**Get-AzRecoveryServicesAsrvCenter Cmdlet** 會取得在 ASR 結構指定的 Configuration 伺服器上註冊用於探索的 vCenter 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="57230-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="57230-110">例子</span><span class="sxs-lookup"><span data-stu-id="57230-110">EXAMPLES</span></span>

### <span data-ttu-id="57230-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="57230-111">Example 1</span></span>
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

<span data-ttu-id="57230-112">根據結構名稱和 vCenter 名稱取得 Azure 網站復原 vCenter。</span><span class="sxs-lookup"><span data-stu-id="57230-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="57230-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="57230-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="57230-114">根據結構名稱取得 Azure 網站復原 vCenter清單。</span><span class="sxs-lookup"><span data-stu-id="57230-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="57230-115">參數</span><span class="sxs-lookup"><span data-stu-id="57230-115">PARAMETERS</span></span>

### <span data-ttu-id="57230-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57230-116">-DefaultProfile</span></span>
<span data-ttu-id="57230-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="57230-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57230-118">-布料</span><span class="sxs-lookup"><span data-stu-id="57230-118">-Fabric</span></span>
<span data-ttu-id="57230-119">代表 Configuration Server 的 ASR 結構物件。</span><span class="sxs-lookup"><span data-stu-id="57230-119">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="57230-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="57230-120">-Name</span></span>
<span data-ttu-id="57230-121">vCenter 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="57230-121">Name of the vCenter server.</span></span>

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

### <span data-ttu-id="57230-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57230-122">-ResourceId</span></span>
<span data-ttu-id="57230-123">指定 vCenter 的資源Id。</span><span class="sxs-lookup"><span data-stu-id="57230-123">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="57230-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57230-124">CommonParameters</span></span>
<span data-ttu-id="57230-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="57230-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57230-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57230-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57230-127">輸入</span><span class="sxs-lookup"><span data-stu-id="57230-127">INPUTS</span></span>

### <span data-ttu-id="57230-128">System.String</span><span class="sxs-lookup"><span data-stu-id="57230-128">System.String</span></span>

### <span data-ttu-id="57230-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="57230-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="57230-130">輸出</span><span class="sxs-lookup"><span data-stu-id="57230-130">OUTPUTS</span></span>

### <span data-ttu-id="57230-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="57230-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="57230-132">筆記</span><span class="sxs-lookup"><span data-stu-id="57230-132">NOTES</span></span>

## <span data-ttu-id="57230-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="57230-133">RELATED LINKS</span></span>
