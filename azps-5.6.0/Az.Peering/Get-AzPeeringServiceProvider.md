---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: cfc25f735d2785a688f29fd3eb3064337b5c6e8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911470"
---
# <span data-ttu-id="98016-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="98016-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="98016-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98016-102">SYNOPSIS</span></span>
<span data-ttu-id="98016-103">獲得與 Microsoft 合作之對等服務提供者的清單。</span><span class="sxs-lookup"><span data-stu-id="98016-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="98016-104">語法</span><span class="sxs-lookup"><span data-stu-id="98016-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98016-105">描述</span><span class="sxs-lookup"><span data-stu-id="98016-105">DESCRIPTION</span></span>
<span data-ttu-id="98016-106">清單對等服務提供者</span><span class="sxs-lookup"><span data-stu-id="98016-106">List peering service providers</span></span>

## <span data-ttu-id="98016-107">例子</span><span class="sxs-lookup"><span data-stu-id="98016-107">EXAMPLES</span></span>

### <span data-ttu-id="98016-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="98016-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="98016-109">獲得可用的對等服務提供者</span><span class="sxs-lookup"><span data-stu-id="98016-109">Gets available peering service providers</span></span>

## <span data-ttu-id="98016-110">參數</span><span class="sxs-lookup"><span data-stu-id="98016-110">PARAMETERS</span></span>

### <span data-ttu-id="98016-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98016-111">-DefaultProfile</span></span>
<span data-ttu-id="98016-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="98016-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98016-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98016-113">CommonParameters</span></span>
<span data-ttu-id="98016-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98016-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98016-115">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98016-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98016-116">輸入</span><span class="sxs-lookup"><span data-stu-id="98016-116">INPUTS</span></span>

### <span data-ttu-id="98016-117">沒有</span><span class="sxs-lookup"><span data-stu-id="98016-117">None</span></span>

## <span data-ttu-id="98016-118">輸出</span><span class="sxs-lookup"><span data-stu-id="98016-118">OUTPUTS</span></span>

### <span data-ttu-id="98016-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="98016-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="98016-120">筆記</span><span class="sxs-lookup"><span data-stu-id="98016-120">NOTES</span></span>

## <span data-ttu-id="98016-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="98016-121">RELATED LINKS</span></span>
