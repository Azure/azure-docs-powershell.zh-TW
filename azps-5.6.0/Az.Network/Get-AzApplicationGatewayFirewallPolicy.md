---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 122e011336b9fcdb8b8eb19622632e1ff295a01c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913497"
---
# <span data-ttu-id="33d68-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="33d68-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="33d68-102">簡介</span><span class="sxs-lookup"><span data-stu-id="33d68-102">SYNOPSIS</span></span>
<span data-ttu-id="33d68-103">獲得應用程式閘道防火牆政策。</span><span class="sxs-lookup"><span data-stu-id="33d68-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="33d68-104">語法</span><span class="sxs-lookup"><span data-stu-id="33d68-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33d68-105">描述</span><span class="sxs-lookup"><span data-stu-id="33d68-105">DESCRIPTION</span></span>
<span data-ttu-id="33d68-106">**Get-AzApplicationGatewayFirewallPolicy** Cmdlet 會取得應用程式閘道防火牆策略。</span><span class="sxs-lookup"><span data-stu-id="33d68-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="33d68-107">例子</span><span class="sxs-lookup"><span data-stu-id="33d68-107">EXAMPLES</span></span>

### <span data-ttu-id="33d68-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="33d68-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="33d68-109">此命令會獲得名為 FirewallPolicy1 的應用程式閘道防火牆策略，該策略屬於名為 ResourceGroup01 的資源群組，並儲存在 $AppGwFirewallPolicy 變數中。</span><span class="sxs-lookup"><span data-stu-id="33d68-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="33d68-110">參數</span><span class="sxs-lookup"><span data-stu-id="33d68-110">PARAMETERS</span></span>

### <span data-ttu-id="33d68-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d68-111">-DefaultProfile</span></span>
<span data-ttu-id="33d68-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="33d68-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33d68-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="33d68-113">-Name</span></span>
<span data-ttu-id="33d68-114">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="33d68-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33d68-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33d68-115">-ResourceGroupName</span></span>
<span data-ttu-id="33d68-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="33d68-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33d68-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d68-117">CommonParameters</span></span>
<span data-ttu-id="33d68-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="33d68-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d68-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33d68-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d68-120">輸入</span><span class="sxs-lookup"><span data-stu-id="33d68-120">INPUTS</span></span>

### <span data-ttu-id="33d68-121">System.String</span><span class="sxs-lookup"><span data-stu-id="33d68-121">System.String</span></span>

## <span data-ttu-id="33d68-122">輸出</span><span class="sxs-lookup"><span data-stu-id="33d68-122">OUTPUTS</span></span>

### <span data-ttu-id="33d68-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="33d68-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="33d68-124">筆記</span><span class="sxs-lookup"><span data-stu-id="33d68-124">NOTES</span></span>

## <span data-ttu-id="33d68-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="33d68-125">RELATED LINKS</span></span>
