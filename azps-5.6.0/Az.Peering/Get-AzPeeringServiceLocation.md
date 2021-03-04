---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 84cc6f2e8e51de6176b4ab8a04296aab8516a967
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911474"
---
# <span data-ttu-id="b600a-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="b600a-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="b600a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b600a-102">SYNOPSIS</span></span>
<span data-ttu-id="b600a-103">獲得 Microsoft 提供的對等服務位置清單。</span><span class="sxs-lookup"><span data-stu-id="b600a-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="b600a-104">語法</span><span class="sxs-lookup"><span data-stu-id="b600a-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b600a-105">描述</span><span class="sxs-lookup"><span data-stu-id="b600a-105">DESCRIPTION</span></span>
<span data-ttu-id="b600a-106">列出對等位置。</span><span class="sxs-lookup"><span data-stu-id="b600a-106">List peering locations.</span></span>

## <span data-ttu-id="b600a-107">例子</span><span class="sxs-lookup"><span data-stu-id="b600a-107">EXAMPLES</span></span>

### <span data-ttu-id="b600a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b600a-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="b600a-109">為華盛頓州取回對等位置。</span><span class="sxs-lookup"><span data-stu-id="b600a-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="b600a-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="b600a-110">Example 2</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States"

Country     : United States
State       : Alabama
AzureRegion : East US
Name        : Alabama
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

Country     : United States
State       : Arizona
AzureRegion : West US
Name        : Arizona
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

...
```

<span data-ttu-id="b600a-111">為華盛頓州取回對等位置。</span><span class="sxs-lookup"><span data-stu-id="b600a-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="b600a-112">參數</span><span class="sxs-lookup"><span data-stu-id="b600a-112">PARAMETERS</span></span>

### <span data-ttu-id="b600a-113">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="b600a-113">-Country</span></span>
<span data-ttu-id="b600a-114">國家/地區篩選</span><span class="sxs-lookup"><span data-stu-id="b600a-114">The country filter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b600a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b600a-115">-DefaultProfile</span></span>
<span data-ttu-id="b600a-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b600a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b600a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b600a-117">CommonParameters</span></span>
<span data-ttu-id="b600a-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b600a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b600a-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b600a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b600a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="b600a-120">INPUTS</span></span>

### <span data-ttu-id="b600a-121">沒有</span><span class="sxs-lookup"><span data-stu-id="b600a-121">None</span></span>

## <span data-ttu-id="b600a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="b600a-122">OUTPUTS</span></span>

### <span data-ttu-id="b600a-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="b600a-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="b600a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="b600a-124">NOTES</span></span>

## <span data-ttu-id="b600a-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="b600a-125">RELATED LINKS</span></span>
