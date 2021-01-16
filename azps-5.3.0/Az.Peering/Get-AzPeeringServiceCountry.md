---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicecountry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceCountry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceCountry.md
ms.openlocfilehash: f1e324d03990b5a9ec82a315d9e84e0a1832de64
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288551"
---
# <span data-ttu-id="1b05a-101">Get-AzPeeringServiceCountry</span><span class="sxs-lookup"><span data-stu-id="1b05a-101">Get-AzPeeringServiceCountry</span></span>

## <span data-ttu-id="1b05a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b05a-102">SYNOPSIS</span></span>
<span data-ttu-id="1b05a-103">列出對等服務可用的國家/地區。</span><span class="sxs-lookup"><span data-stu-id="1b05a-103">Lists the countries available for peering service.</span></span>

## <span data-ttu-id="1b05a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b05a-104">SYNTAX</span></span>

```
Get-AzPeeringServiceCountry [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b05a-105">說明</span><span class="sxs-lookup"><span data-stu-id="1b05a-105">DESCRIPTION</span></span>
<span data-ttu-id="1b05a-106">列出對等服務可用的國家/地區。</span><span class="sxs-lookup"><span data-stu-id="1b05a-106">Lists the countries available for peering service.</span></span>

## <span data-ttu-id="1b05a-107">示例</span><span class="sxs-lookup"><span data-stu-id="1b05a-107">EXAMPLES</span></span>

### <span data-ttu-id="1b05a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1b05a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceCountry
```

<span data-ttu-id="1b05a-109">對等服務可用的國家/地區清單。</span><span class="sxs-lookup"><span data-stu-id="1b05a-109">List of countries available for peering service.</span></span>

## <span data-ttu-id="1b05a-110">參數</span><span class="sxs-lookup"><span data-stu-id="1b05a-110">PARAMETERS</span></span>

### <span data-ttu-id="1b05a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b05a-111">-DefaultProfile</span></span>
<span data-ttu-id="1b05a-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b05a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b05a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b05a-113">CommonParameters</span></span>
<span data-ttu-id="1b05a-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b05a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b05a-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1b05a-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b05a-116">輸入</span><span class="sxs-lookup"><span data-stu-id="1b05a-116">INPUTS</span></span>

### <span data-ttu-id="1b05a-117">所有</span><span class="sxs-lookup"><span data-stu-id="1b05a-117">None</span></span>

## <span data-ttu-id="1b05a-118">輸出</span><span class="sxs-lookup"><span data-stu-id="1b05a-118">OUTPUTS</span></span>

### <span data-ttu-id="1b05a-119">PSPeeringServiceLocation 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="1b05a-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="1b05a-120">筆記</span><span class="sxs-lookup"><span data-stu-id="1b05a-120">NOTES</span></span>

## <span data-ttu-id="1b05a-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b05a-121">RELATED LINKS</span></span>
