---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
ms.openlocfilehash: c758131685787ec8627f6e0cd3760e2ee42107c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456011"
---
# <span data-ttu-id="c3706-101">Get-AzureRmExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="c3706-101">Get-AzureRmExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="c3706-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3706-102">SYNOPSIS</span></span>
<span data-ttu-id="c3706-103">取得 ExpressRoutePort 連結設定。</span><span class="sxs-lookup"><span data-stu-id="c3706-103">Gets an ExpressRoutePort link configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3706-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3706-104">SYNTAX</span></span>

### <span data-ttu-id="c3706-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c3706-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3706-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3706-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> -ResourceId <String> 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3706-107">說明</span><span class="sxs-lookup"><span data-stu-id="c3706-107">DESCRIPTION</span></span>
<span data-ttu-id="c3706-108">**AzureRmExpressRoutePortLinkConfig** Cmdlet 會檢索 ExpressRoutePort 連結的設定。</span><span class="sxs-lookup"><span data-stu-id="c3706-108">The **Get-AzureRmExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="c3706-109">示例</span><span class="sxs-lookup"><span data-stu-id="c3706-109">EXAMPLES</span></span>

### <span data-ttu-id="c3706-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c3706-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="c3706-111">取得 ExpressRoutePort $erport 的 Link1 設定</span><span class="sxs-lookup"><span data-stu-id="c3706-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="c3706-112">範例2</span><span class="sxs-lookup"><span data-stu-id="c3706-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="c3706-113">取得 ExpressRoutePort $erport 中與 ResourceId $id 連結的設定</span><span class="sxs-lookup"><span data-stu-id="c3706-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="c3706-114">參數</span><span class="sxs-lookup"><span data-stu-id="c3706-114">PARAMETERS</span></span>

### <span data-ttu-id="c3706-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3706-115">-DefaultProfile</span></span>
<span data-ttu-id="c3706-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3706-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3706-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c3706-117">-ExpressRoutePort</span></span>
<span data-ttu-id="c3706-118">ExpressRoutePort 資源的參照。</span><span class="sxs-lookup"><span data-stu-id="c3706-118">The reference of the ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3706-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3706-119">-Name</span></span>
<span data-ttu-id="c3706-120">連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3706-120">Name of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3706-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3706-121">-ResourceId</span></span>
<span data-ttu-id="c3706-122">連結的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="c3706-122">ResourceId of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3706-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3706-123">CommonParameters</span></span>
<span data-ttu-id="c3706-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3706-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3706-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3706-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3706-126">輸入</span><span class="sxs-lookup"><span data-stu-id="c3706-126">INPUTS</span></span>

### <span data-ttu-id="c3706-127">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c3706-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="c3706-128">輸出</span><span class="sxs-lookup"><span data-stu-id="c3706-128">OUTPUTS</span></span>

### <span data-ttu-id="c3706-129">PSExpressRouteLink 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c3706-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="c3706-130">筆記</span><span class="sxs-lookup"><span data-stu-id="c3706-130">NOTES</span></span>

## <span data-ttu-id="c3706-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3706-131">RELATED LINKS</span></span>
