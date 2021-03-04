---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 54c90e4dac97084ed371e0f5f9011bbcef0a254e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915269"
---
# <span data-ttu-id="5d759-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="5d759-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="5d759-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5d759-102">SYNOPSIS</span></span>
<span data-ttu-id="5d759-103">針對目前的儲存庫，獲得網站修復所管理之網路的資訊。</span><span class="sxs-lookup"><span data-stu-id="5d759-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="5d759-104">語法</span><span class="sxs-lookup"><span data-stu-id="5d759-104">SYNTAX</span></span>

### <span data-ttu-id="5d759-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="5d759-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d759-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5d759-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d759-107">By有LylyName</span><span class="sxs-lookup"><span data-stu-id="5d759-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d759-108">描述</span><span class="sxs-lookup"><span data-stu-id="5d759-108">DESCRIPTION</span></span>
<span data-ttu-id="5d759-109">**Get-AzRecoveryServicesAsrNetwork** Cmdlet 會取得目前 Azure 網站修復庫的 Azure 網站修復網路相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5d759-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="5d759-110">例子</span><span class="sxs-lookup"><span data-stu-id="5d759-110">EXAMPLES</span></span>

### <span data-ttu-id="5d759-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="5d759-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="5d759-112">獲得指定結構內的所有已知網路。</span><span class="sxs-lookup"><span data-stu-id="5d759-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="5d759-113">參數</span><span class="sxs-lookup"><span data-stu-id="5d759-113">PARAMETERS</span></span>

### <span data-ttu-id="5d759-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d759-114">-DefaultProfile</span></span>
<span data-ttu-id="5d759-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d759-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5d759-116">-布料</span><span class="sxs-lookup"><span data-stu-id="5d759-116">-Fabric</span></span>
<span data-ttu-id="5d759-117">ASR 布料物件</span><span class="sxs-lookup"><span data-stu-id="5d759-117">ASR fabric object</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d759-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5d759-118">-FriendlyName</span></span>
<span data-ttu-id="5d759-119">網路 ASR 物件的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="5d759-119">Friendly name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d759-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="5d759-120">-Name</span></span>
<span data-ttu-id="5d759-121">網路 ASR 物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d759-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="5d759-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d759-122">CommonParameters</span></span>
<span data-ttu-id="5d759-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5d759-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d759-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d759-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d759-125">輸入</span><span class="sxs-lookup"><span data-stu-id="5d759-125">INPUTS</span></span>

### <span data-ttu-id="5d759-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="5d759-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="5d759-127">輸出</span><span class="sxs-lookup"><span data-stu-id="5d759-127">OUTPUTS</span></span>

### <span data-ttu-id="5d759-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="5d759-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="5d759-129">筆記</span><span class="sxs-lookup"><span data-stu-id="5d759-129">NOTES</span></span>

## <span data-ttu-id="5d759-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d759-130">RELATED LINKS</span></span>
