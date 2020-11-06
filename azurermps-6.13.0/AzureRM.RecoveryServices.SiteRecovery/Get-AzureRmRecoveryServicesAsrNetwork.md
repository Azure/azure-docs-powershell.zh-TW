---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 4eac63104f9e75643119c371d2a4d0e882945966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448959"
---
# <span data-ttu-id="53387-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="53387-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="53387-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53387-102">SYNOPSIS</span></span>
<span data-ttu-id="53387-103">取得目前電子倉庫的網站復原所管理網路的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="53387-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53387-104">句法</span><span class="sxs-lookup"><span data-stu-id="53387-104">SYNTAX</span></span>

### <span data-ttu-id="53387-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="53387-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53387-106">ByName</span><span class="sxs-lookup"><span data-stu-id="53387-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53387-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="53387-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53387-108">說明</span><span class="sxs-lookup"><span data-stu-id="53387-108">DESCRIPTION</span></span>
<span data-ttu-id="53387-109">**AzureRmRecoveryServicesAsrNetwork** Cmdlet 會取得目前 Azure site recovery 保存庫的 Azure site recovery 網路相關資訊。</span><span class="sxs-lookup"><span data-stu-id="53387-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="53387-110">示例</span><span class="sxs-lookup"><span data-stu-id="53387-110">EXAMPLES</span></span>

### <span data-ttu-id="53387-111">範例1</span><span class="sxs-lookup"><span data-stu-id="53387-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="53387-112">取得指定結構中的所有已知網路。</span><span class="sxs-lookup"><span data-stu-id="53387-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="53387-113">參數</span><span class="sxs-lookup"><span data-stu-id="53387-113">PARAMETERS</span></span>

### <span data-ttu-id="53387-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53387-114">-DefaultProfile</span></span>
<span data-ttu-id="53387-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53387-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="53387-116">-結構</span><span class="sxs-lookup"><span data-stu-id="53387-116">-Fabric</span></span>
<span data-ttu-id="53387-117">ASR fabric 物件</span><span class="sxs-lookup"><span data-stu-id="53387-117">ASR fabric object</span></span>

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

### <span data-ttu-id="53387-118">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="53387-118">-FriendlyName</span></span>
<span data-ttu-id="53387-119">網路 ASR 物件的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="53387-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="53387-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="53387-120">-Name</span></span>
<span data-ttu-id="53387-121">網路 ASR 物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="53387-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="53387-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53387-122">CommonParameters</span></span>
<span data-ttu-id="53387-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53387-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53387-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53387-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53387-125">輸入</span><span class="sxs-lookup"><span data-stu-id="53387-125">INPUTS</span></span>

### <span data-ttu-id="53387-126">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="53387-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="53387-127">輸出</span><span class="sxs-lookup"><span data-stu-id="53387-127">OUTPUTS</span></span>

### <span data-ttu-id="53387-128">System.object. IEnumerable "1 [ASRNetwork，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="53387-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="53387-129">筆記</span><span class="sxs-lookup"><span data-stu-id="53387-129">NOTES</span></span>

## <span data-ttu-id="53387-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="53387-130">RELATED LINKS</span></span>
