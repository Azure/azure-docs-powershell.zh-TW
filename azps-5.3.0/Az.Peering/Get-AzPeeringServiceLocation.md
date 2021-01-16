---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 6f869cee7258c38e941ca8fbb7c8ac31b47171af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288548"
---
# <span data-ttu-id="e284c-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="e284c-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="e284c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e284c-102">SYNOPSIS</span></span>
<span data-ttu-id="e284c-103">取得 Microsoft 所提供的對等服務位置清單。</span><span class="sxs-lookup"><span data-stu-id="e284c-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="e284c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e284c-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e284c-105">說明</span><span class="sxs-lookup"><span data-stu-id="e284c-105">DESCRIPTION</span></span>
<span data-ttu-id="e284c-106">清單對等位置。</span><span class="sxs-lookup"><span data-stu-id="e284c-106">List peering locations.</span></span>

## <span data-ttu-id="e284c-107">示例</span><span class="sxs-lookup"><span data-stu-id="e284c-107">EXAMPLES</span></span>

### <span data-ttu-id="e284c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e284c-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="e284c-109">檢索華盛頓的對等位置。</span><span class="sxs-lookup"><span data-stu-id="e284c-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="e284c-110">範例2</span><span class="sxs-lookup"><span data-stu-id="e284c-110">Example 2</span></span>
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

<span data-ttu-id="e284c-111">檢索華盛頓的對等位置。</span><span class="sxs-lookup"><span data-stu-id="e284c-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="e284c-112">參數</span><span class="sxs-lookup"><span data-stu-id="e284c-112">PARAMETERS</span></span>

### <span data-ttu-id="e284c-113">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="e284c-113">-Country</span></span>
<span data-ttu-id="e284c-114">[國家/地區] 篩選</span><span class="sxs-lookup"><span data-stu-id="e284c-114">The country filter</span></span>

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

### <span data-ttu-id="e284c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e284c-115">-DefaultProfile</span></span>
<span data-ttu-id="e284c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e284c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e284c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e284c-117">CommonParameters</span></span>
<span data-ttu-id="e284c-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e284c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e284c-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e284c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e284c-120">輸入</span><span class="sxs-lookup"><span data-stu-id="e284c-120">INPUTS</span></span>

### <span data-ttu-id="e284c-121">所有</span><span class="sxs-lookup"><span data-stu-id="e284c-121">None</span></span>

## <span data-ttu-id="e284c-122">輸出</span><span class="sxs-lookup"><span data-stu-id="e284c-122">OUTPUTS</span></span>

### <span data-ttu-id="e284c-123">PSPeeringServiceLocation 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="e284c-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="e284c-124">筆記</span><span class="sxs-lookup"><span data-stu-id="e284c-124">NOTES</span></span>

## <span data-ttu-id="e284c-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="e284c-125">RELATED LINKS</span></span>
