---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136264"
---
# <span data-ttu-id="21023-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="21023-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="21023-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21023-102">SYNOPSIS</span></span>
<span data-ttu-id="21023-103">建立 office 365 流量排列原則物件。</span><span class="sxs-lookup"><span data-stu-id="21023-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="21023-104">句法</span><span class="sxs-lookup"><span data-stu-id="21023-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21023-105">說明</span><span class="sxs-lookup"><span data-stu-id="21023-105">DESCRIPTION</span></span>
<span data-ttu-id="21023-106">建立要與 New-AzVpnSite 與 Update-AzVpnSite Cmdlet 搭配使用的 office 365 專題原則。</span><span class="sxs-lookup"><span data-stu-id="21023-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="21023-107">示例</span><span class="sxs-lookup"><span data-stu-id="21023-107">EXAMPLES</span></span>

### <span data-ttu-id="21023-108">範例1</span><span class="sxs-lookup"><span data-stu-id="21023-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="21023-109">建立 office 365 流量排列原則，並允許 [允許] 和 [優化] 類別的流量。</span><span class="sxs-lookup"><span data-stu-id="21023-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="21023-110">參數</span><span class="sxs-lookup"><span data-stu-id="21023-110">PARAMETERS</span></span>

### <span data-ttu-id="21023-111">-允許</span><span class="sxs-lookup"><span data-stu-id="21023-111">-Allow</span></span>
<span data-ttu-id="21023-112">將 [允許] 類別流量分類。</span><span class="sxs-lookup"><span data-stu-id="21023-112">Breakout the allow category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21023-113">-預設值</span><span class="sxs-lookup"><span data-stu-id="21023-113">-Default</span></span>
<span data-ttu-id="21023-114">將預設類別交通劃分成專題討論。</span><span class="sxs-lookup"><span data-stu-id="21023-114">Breakout the default category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21023-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21023-115">-DefaultProfile</span></span>
<span data-ttu-id="21023-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21023-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21023-117">-優化</span><span class="sxs-lookup"><span data-stu-id="21023-117">-Optimize</span></span>
<span data-ttu-id="21023-118">將 [優化] 類別流量分類。</span><span class="sxs-lookup"><span data-stu-id="21023-118">Breakout the optimize category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21023-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21023-119">CommonParameters</span></span>
<span data-ttu-id="21023-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21023-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21023-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="21023-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21023-122">輸入</span><span class="sxs-lookup"><span data-stu-id="21023-122">INPUTS</span></span>

### <span data-ttu-id="21023-123">所有</span><span class="sxs-lookup"><span data-stu-id="21023-123">None</span></span>

## <span data-ttu-id="21023-124">輸出</span><span class="sxs-lookup"><span data-stu-id="21023-124">OUTPUTS</span></span>

### <span data-ttu-id="21023-125">PSO365PolicyProperties 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="21023-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="21023-126">筆記</span><span class="sxs-lookup"><span data-stu-id="21023-126">NOTES</span></span>

## <span data-ttu-id="21023-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="21023-127">RELATED LINKS</span></span>