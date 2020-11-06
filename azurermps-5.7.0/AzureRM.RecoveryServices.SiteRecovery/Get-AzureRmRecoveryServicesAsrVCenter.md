---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 689f432f117e67a3770518a3b2e86f1678f3662b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450551"
---
# <span data-ttu-id="8042d-101">Get-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="8042d-101">Get-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="8042d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8042d-102">SYNOPSIS</span></span>
<span data-ttu-id="8042d-103">取得在 ASR 結構指定之設定伺服器上登錄探索的 vCenter 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8042d-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8042d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8042d-104">SYNTAX</span></span>

### <span data-ttu-id="8042d-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="8042d-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8042d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8042d-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8042d-107">ByName</span><span class="sxs-lookup"><span data-stu-id="8042d-107">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8042d-108">說明</span><span class="sxs-lookup"><span data-stu-id="8042d-108">DESCRIPTION</span></span>
<span data-ttu-id="8042d-109">**AzureRmRecoveryServicesAsrvCenter** Cmdlet 會取得在 ASR 結構指定的設定伺服器上註冊探索的 vCenter 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8042d-109">The **Get-AzureRmRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="8042d-110">示例</span><span class="sxs-lookup"><span data-stu-id="8042d-110">EXAMPLES</span></span>

### <span data-ttu-id="8042d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8042d-111">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

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

<span data-ttu-id="8042d-112">根據 fabric name 和 vCenter 的名稱，取得 azure site recovery vCenter。</span><span class="sxs-lookup"><span data-stu-id="8042d-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="8042d-113">範例2</span><span class="sxs-lookup"><span data-stu-id="8042d-113">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="8042d-114">透過 fabric name 取得 azure site recovery vCenter 清單。</span><span class="sxs-lookup"><span data-stu-id="8042d-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="8042d-115">參數</span><span class="sxs-lookup"><span data-stu-id="8042d-115">PARAMETERS</span></span>

### <span data-ttu-id="8042d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8042d-116">-DefaultProfile</span></span>
<span data-ttu-id="8042d-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8042d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8042d-118">-結構</span><span class="sxs-lookup"><span data-stu-id="8042d-118">-Fabric</span></span>
<span data-ttu-id="8042d-119">代表佈建服務器的 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="8042d-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8042d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8042d-120">-Name</span></span>
<span data-ttu-id="8042d-121">VCenter 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8042d-121">Name of the vCenter server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8042d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8042d-122">-ResourceId</span></span>
<span data-ttu-id="8042d-123">指定 vCenter 的 resourceId。</span><span class="sxs-lookup"><span data-stu-id="8042d-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8042d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8042d-124">CommonParameters</span></span>
<span data-ttu-id="8042d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8042d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8042d-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8042d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8042d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8042d-127">INPUTS</span></span>

### <span data-ttu-id="8042d-128">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="8042d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="8042d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="8042d-129">OUTPUTS</span></span>

### <span data-ttu-id="8042d-130">System.object. IEnumerable "1 [ASRvCenter，RecoveryServices. SiteRecovery，Version = 0.1.1.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="8042d-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8042d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8042d-131">NOTES</span></span>

## <span data-ttu-id="8042d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="8042d-132">RELATED LINKS</span></span>
