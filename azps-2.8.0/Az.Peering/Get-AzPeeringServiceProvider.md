---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 786a8009d1423b6b12fae4d7eb8da6899a8cd108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791737"
---
# <span data-ttu-id="ca4f2-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="ca4f2-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="ca4f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="ca4f2-103">取得與 Microsoft 合作的對等服務提供者的清單。</span><span class="sxs-lookup"><span data-stu-id="ca4f2-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="ca4f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca4f2-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca4f2-105">說明</span><span class="sxs-lookup"><span data-stu-id="ca4f2-105">DESCRIPTION</span></span>
<span data-ttu-id="ca4f2-106">清單對等服務提供者</span><span class="sxs-lookup"><span data-stu-id="ca4f2-106">List peering service providers</span></span>

## <span data-ttu-id="ca4f2-107">示例</span><span class="sxs-lookup"><span data-stu-id="ca4f2-107">EXAMPLES</span></span>

### <span data-ttu-id="ca4f2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ca4f2-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="ca4f2-109">取得可用的對等服務提供者</span><span class="sxs-lookup"><span data-stu-id="ca4f2-109">Gets available peering service providers</span></span>

## <span data-ttu-id="ca4f2-110">參數</span><span class="sxs-lookup"><span data-stu-id="ca4f2-110">PARAMETERS</span></span>

### <span data-ttu-id="ca4f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca4f2-111">-DefaultProfile</span></span>
<span data-ttu-id="ca4f2-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca4f2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca4f2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca4f2-113">CommonParameters</span></span>
<span data-ttu-id="ca4f2-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca4f2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca4f2-115">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ca4f2-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca4f2-116">輸入</span><span class="sxs-lookup"><span data-stu-id="ca4f2-116">INPUTS</span></span>

### <span data-ttu-id="ca4f2-117">所有</span><span class="sxs-lookup"><span data-stu-id="ca4f2-117">None</span></span>

## <span data-ttu-id="ca4f2-118">輸出</span><span class="sxs-lookup"><span data-stu-id="ca4f2-118">OUTPUTS</span></span>

### <span data-ttu-id="ca4f2-119">PSPeeringServiceProvider 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="ca4f2-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="ca4f2-120">筆記</span><span class="sxs-lookup"><span data-stu-id="ca4f2-120">NOTES</span></span>

## <span data-ttu-id="ca4f2-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca4f2-121">RELATED LINKS</span></span>
