---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140047"
---
# <span data-ttu-id="946ee-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="946ee-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="946ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="946ee-102">SYNOPSIS</span></span>
<span data-ttu-id="946ee-103">取得目前電子倉庫的網站復原所管理網路的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="946ee-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="946ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="946ee-104">SYNTAX</span></span>

### <span data-ttu-id="946ee-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="946ee-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="946ee-106">ByName</span><span class="sxs-lookup"><span data-stu-id="946ee-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="946ee-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="946ee-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="946ee-108">說明</span><span class="sxs-lookup"><span data-stu-id="946ee-108">DESCRIPTION</span></span>
<span data-ttu-id="946ee-109">**AzRecoveryServicesAsrNetwork** Cmdlet 會取得目前 Azure site recovery 保存庫的 Azure site recovery 網路相關資訊。</span><span class="sxs-lookup"><span data-stu-id="946ee-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="946ee-110">示例</span><span class="sxs-lookup"><span data-stu-id="946ee-110">EXAMPLES</span></span>

### <span data-ttu-id="946ee-111">範例1</span><span class="sxs-lookup"><span data-stu-id="946ee-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="946ee-112">取得指定結構中的所有已知網路。</span><span class="sxs-lookup"><span data-stu-id="946ee-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="946ee-113">參數</span><span class="sxs-lookup"><span data-stu-id="946ee-113">PARAMETERS</span></span>

### <span data-ttu-id="946ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="946ee-114">-DefaultProfile</span></span>
<span data-ttu-id="946ee-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="946ee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="946ee-116">-結構</span><span class="sxs-lookup"><span data-stu-id="946ee-116">-Fabric</span></span>
<span data-ttu-id="946ee-117">ASR fabric 物件</span><span class="sxs-lookup"><span data-stu-id="946ee-117">ASR fabric object</span></span>

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

### <span data-ttu-id="946ee-118">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="946ee-118">-FriendlyName</span></span>
<span data-ttu-id="946ee-119">網路 ASR 物件的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="946ee-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="946ee-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="946ee-120">-Name</span></span>
<span data-ttu-id="946ee-121">網路 ASR 物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="946ee-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="946ee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="946ee-122">CommonParameters</span></span>
<span data-ttu-id="946ee-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="946ee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="946ee-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="946ee-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="946ee-125">輸入</span><span class="sxs-lookup"><span data-stu-id="946ee-125">INPUTS</span></span>

### <span data-ttu-id="946ee-126">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="946ee-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="946ee-127">輸出</span><span class="sxs-lookup"><span data-stu-id="946ee-127">OUTPUTS</span></span>

### <span data-ttu-id="946ee-128">RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="946ee-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="946ee-129">筆記</span><span class="sxs-lookup"><span data-stu-id="946ee-129">NOTES</span></span>

## <span data-ttu-id="946ee-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="946ee-130">RELATED LINKS</span></span>
