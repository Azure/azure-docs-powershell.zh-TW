---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796857"
---
# <span data-ttu-id="8fc6b-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="8fc6b-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="8fc6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8fc6b-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc6b-103">取得目前電子倉庫的網站復原所管理網路的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8fc6b-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="8fc6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8fc6b-104">SYNTAX</span></span>

### <span data-ttu-id="8fc6b-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="8fc6b-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fc6b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8fc6b-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fc6b-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8fc6b-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fc6b-108">說明</span><span class="sxs-lookup"><span data-stu-id="8fc6b-108">DESCRIPTION</span></span>
<span data-ttu-id="8fc6b-109">**AzRecoveryServicesAsrNetwork** Cmdlet 會取得目前 Azure site recovery 保存庫的 Azure site recovery 網路相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8fc6b-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="8fc6b-110">示例</span><span class="sxs-lookup"><span data-stu-id="8fc6b-110">EXAMPLES</span></span>

### <span data-ttu-id="8fc6b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8fc6b-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="8fc6b-112">取得指定結構中的所有已知網路。</span><span class="sxs-lookup"><span data-stu-id="8fc6b-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="8fc6b-113">參數</span><span class="sxs-lookup"><span data-stu-id="8fc6b-113">PARAMETERS</span></span>

### <span data-ttu-id="8fc6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc6b-114">-DefaultProfile</span></span>
<span data-ttu-id="8fc6b-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8fc6b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8fc6b-116">-結構</span><span class="sxs-lookup"><span data-stu-id="8fc6b-116">-Fabric</span></span>
<span data-ttu-id="8fc6b-117">ASR fabric 物件</span><span class="sxs-lookup"><span data-stu-id="8fc6b-117">ASR fabric object</span></span>

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

### <span data-ttu-id="8fc6b-118">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8fc6b-118">-FriendlyName</span></span>
<span data-ttu-id="8fc6b-119">網路 ASR 物件的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="8fc6b-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="8fc6b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8fc6b-120">-Name</span></span>
<span data-ttu-id="8fc6b-121">網路 ASR 物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fc6b-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="8fc6b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc6b-122">CommonParameters</span></span>
<span data-ttu-id="8fc6b-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8fc6b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc6b-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8fc6b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc6b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="8fc6b-125">INPUTS</span></span>

### <span data-ttu-id="8fc6b-126">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="8fc6b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="8fc6b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="8fc6b-127">OUTPUTS</span></span>

### <span data-ttu-id="8fc6b-128">RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="8fc6b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="8fc6b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="8fc6b-129">NOTES</span></span>

## <span data-ttu-id="8fc6b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="8fc6b-130">RELATED LINKS</span></span>