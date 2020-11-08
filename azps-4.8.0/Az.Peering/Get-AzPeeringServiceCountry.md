---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicecountry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceCountry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceCountry.md
ms.openlocfilehash: f1e324d03990b5a9ec82a315d9e84e0a1832de64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970847"
---
# <span data-ttu-id="f65f2-101">Get-AzPeeringServiceCountry</span><span class="sxs-lookup"><span data-stu-id="f65f2-101">Get-AzPeeringServiceCountry</span></span>

## <span data-ttu-id="f65f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f65f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f65f2-103">列出對等服務可用的國家/地區。</span><span class="sxs-lookup"><span data-stu-id="f65f2-103">Lists the countries available for peering service.</span></span>

## <span data-ttu-id="f65f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="f65f2-104">SYNTAX</span></span>

```
Get-AzPeeringServiceCountry [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f65f2-105">說明</span><span class="sxs-lookup"><span data-stu-id="f65f2-105">DESCRIPTION</span></span>
<span data-ttu-id="f65f2-106">列出對等服務可用的國家/地區。</span><span class="sxs-lookup"><span data-stu-id="f65f2-106">Lists the countries available for peering service.</span></span>

## <span data-ttu-id="f65f2-107">示例</span><span class="sxs-lookup"><span data-stu-id="f65f2-107">EXAMPLES</span></span>

### <span data-ttu-id="f65f2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f65f2-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceCountry
```

<span data-ttu-id="f65f2-109">對等服務可用的國家/地區清單。</span><span class="sxs-lookup"><span data-stu-id="f65f2-109">List of countries available for peering service.</span></span>

## <span data-ttu-id="f65f2-110">參數</span><span class="sxs-lookup"><span data-stu-id="f65f2-110">PARAMETERS</span></span>

### <span data-ttu-id="f65f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f65f2-111">-DefaultProfile</span></span>
<span data-ttu-id="f65f2-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f65f2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f65f2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f65f2-113">CommonParameters</span></span>
<span data-ttu-id="f65f2-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f65f2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f65f2-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f65f2-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f65f2-116">輸入</span><span class="sxs-lookup"><span data-stu-id="f65f2-116">INPUTS</span></span>

### <span data-ttu-id="f65f2-117">所有</span><span class="sxs-lookup"><span data-stu-id="f65f2-117">None</span></span>

## <span data-ttu-id="f65f2-118">輸出</span><span class="sxs-lookup"><span data-stu-id="f65f2-118">OUTPUTS</span></span>

### <span data-ttu-id="f65f2-119">PSPeeringServiceLocation 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="f65f2-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="f65f2-120">筆記</span><span class="sxs-lookup"><span data-stu-id="f65f2-120">NOTES</span></span>

## <span data-ttu-id="f65f2-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="f65f2-121">RELATED LINKS</span></span>