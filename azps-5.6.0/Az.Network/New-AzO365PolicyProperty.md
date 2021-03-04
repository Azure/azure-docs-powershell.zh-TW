---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: a2b3a4878db022018bd0fae1d8e43e3700dd5e35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903513"
---
# <span data-ttu-id="5e355-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="5e355-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="5e355-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5e355-102">SYNOPSIS</span></span>
<span data-ttu-id="5e355-103">建立 Office 365 流量中斷策略物件。</span><span class="sxs-lookup"><span data-stu-id="5e355-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="5e355-104">語法</span><span class="sxs-lookup"><span data-stu-id="5e355-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e355-105">描述</span><span class="sxs-lookup"><span data-stu-id="5e355-105">DESCRIPTION</span></span>
<span data-ttu-id="5e355-106">建立 Office 365 分組討論策略，以與 New-AzVpnSite 和 Update-AzVpnSite一起使用。</span><span class="sxs-lookup"><span data-stu-id="5e355-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="5e355-107">例子</span><span class="sxs-lookup"><span data-stu-id="5e355-107">EXAMPLES</span></span>

### <span data-ttu-id="5e355-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="5e355-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="5e355-109">建立 Office 365 流量中斷策略，並允許中斷，以允許並優化流量類別。</span><span class="sxs-lookup"><span data-stu-id="5e355-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="5e355-110">參數</span><span class="sxs-lookup"><span data-stu-id="5e355-110">PARAMETERS</span></span>

### <span data-ttu-id="5e355-111">-允許</span><span class="sxs-lookup"><span data-stu-id="5e355-111">-Allow</span></span>
<span data-ttu-id="5e355-112">中斷允許類別流量。</span><span class="sxs-lookup"><span data-stu-id="5e355-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="5e355-113">-預設</span><span class="sxs-lookup"><span data-stu-id="5e355-113">-Default</span></span>
<span data-ttu-id="5e355-114">中斷預設類別流量。</span><span class="sxs-lookup"><span data-stu-id="5e355-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="5e355-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e355-115">-DefaultProfile</span></span>
<span data-ttu-id="5e355-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e355-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e355-117">-優化</span><span class="sxs-lookup"><span data-stu-id="5e355-117">-Optimize</span></span>
<span data-ttu-id="5e355-118">分組優化類別流量。</span><span class="sxs-lookup"><span data-stu-id="5e355-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="5e355-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e355-119">CommonParameters</span></span>
<span data-ttu-id="5e355-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5e355-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e355-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e355-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e355-122">輸入</span><span class="sxs-lookup"><span data-stu-id="5e355-122">INPUTS</span></span>

### <span data-ttu-id="5e355-123">沒有</span><span class="sxs-lookup"><span data-stu-id="5e355-123">None</span></span>

## <span data-ttu-id="5e355-124">輸出</span><span class="sxs-lookup"><span data-stu-id="5e355-124">OUTPUTS</span></span>

### <span data-ttu-id="5e355-125">Microsoft.Azure.Commands.Network.models.PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="5e355-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="5e355-126">筆記</span><span class="sxs-lookup"><span data-stu-id="5e355-126">NOTES</span></span>

## <span data-ttu-id="5e355-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e355-127">RELATED LINKS</span></span>
