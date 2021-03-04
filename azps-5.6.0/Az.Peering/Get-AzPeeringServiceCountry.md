---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservicecountry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceCountry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceCountry.md
ms.openlocfilehash: 4f13c0be9681fb2eda6fa509e321c2fa161049ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911477"
---
# <span data-ttu-id="f3b1a-101">Get-AzPeeringServiceCountry</span><span class="sxs-lookup"><span data-stu-id="f3b1a-101">Get-AzPeeringServiceCountry</span></span>

## <span data-ttu-id="f3b1a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f3b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b1a-103">列出可供對等服務使用的國家/地區。</span><span class="sxs-lookup"><span data-stu-id="f3b1a-103">Lists the countries available for peering service.</span></span>

## <span data-ttu-id="f3b1a-104">語法</span><span class="sxs-lookup"><span data-stu-id="f3b1a-104">SYNTAX</span></span>

```
Get-AzPeeringServiceCountry [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3b1a-105">描述</span><span class="sxs-lookup"><span data-stu-id="f3b1a-105">DESCRIPTION</span></span>
<span data-ttu-id="f3b1a-106">列出可供對等服務使用的國家/地區。</span><span class="sxs-lookup"><span data-stu-id="f3b1a-106">Lists the countries available for peering service.</span></span>

## <span data-ttu-id="f3b1a-107">例子</span><span class="sxs-lookup"><span data-stu-id="f3b1a-107">EXAMPLES</span></span>

### <span data-ttu-id="f3b1a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f3b1a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceCountry
```

<span data-ttu-id="f3b1a-109">提供對等服務的國家/地區清單。</span><span class="sxs-lookup"><span data-stu-id="f3b1a-109">List of countries available for peering service.</span></span>

## <span data-ttu-id="f3b1a-110">參數</span><span class="sxs-lookup"><span data-stu-id="f3b1a-110">PARAMETERS</span></span>

### <span data-ttu-id="f3b1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3b1a-111">-DefaultProfile</span></span>
<span data-ttu-id="f3b1a-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3b1a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3b1a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b1a-113">CommonParameters</span></span>
<span data-ttu-id="f3b1a-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f3b1a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b1a-115">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3b1a-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b1a-116">輸入</span><span class="sxs-lookup"><span data-stu-id="f3b1a-116">INPUTS</span></span>

### <span data-ttu-id="f3b1a-117">沒有</span><span class="sxs-lookup"><span data-stu-id="f3b1a-117">None</span></span>

## <span data-ttu-id="f3b1a-118">輸出</span><span class="sxs-lookup"><span data-stu-id="f3b1a-118">OUTPUTS</span></span>

### <span data-ttu-id="f3b1a-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="f3b1a-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="f3b1a-120">筆記</span><span class="sxs-lookup"><span data-stu-id="f3b1a-120">NOTES</span></span>

## <span data-ttu-id="f3b1a-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3b1a-121">RELATED LINKS</span></span>
