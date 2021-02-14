---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: fdcd725c79a6f789879ab3103cec90b09c828e74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128982"
---
# <span data-ttu-id="bcb78-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="bcb78-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="bcb78-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcb78-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb78-103">取得應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="bcb78-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="bcb78-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcb78-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcb78-105">說明</span><span class="sxs-lookup"><span data-stu-id="bcb78-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb78-106">**AzApplicationGatewayFirewallPolicy** Cmdlet 會取得應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="bcb78-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="bcb78-107">示例</span><span class="sxs-lookup"><span data-stu-id="bcb78-107">EXAMPLES</span></span>

### <span data-ttu-id="bcb78-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bcb78-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bcb78-109">這個命令會取得名為「ResourceGroup01」資源群組的應用程式閘道防火牆原則，並將其儲存在 $AppGwFirewallPolicy 變數中。</span><span class="sxs-lookup"><span data-stu-id="bcb78-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="bcb78-110">參數</span><span class="sxs-lookup"><span data-stu-id="bcb78-110">PARAMETERS</span></span>

### <span data-ttu-id="bcb78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb78-111">-DefaultProfile</span></span>
<span data-ttu-id="bcb78-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcb78-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcb78-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="bcb78-113">-Name</span></span>
<span data-ttu-id="bcb78-114">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="bcb78-114">The resource name.</span></span>

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

### <span data-ttu-id="bcb78-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcb78-115">-ResourceGroupName</span></span>
<span data-ttu-id="bcb78-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcb78-116">The resource group name.</span></span>

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

### <span data-ttu-id="bcb78-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb78-117">CommonParameters</span></span>
<span data-ttu-id="bcb78-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcb78-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb78-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bcb78-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb78-120">輸入</span><span class="sxs-lookup"><span data-stu-id="bcb78-120">INPUTS</span></span>

### <span data-ttu-id="bcb78-121">System.object</span><span class="sxs-lookup"><span data-stu-id="bcb78-121">System.String</span></span>

## <span data-ttu-id="bcb78-122">輸出</span><span class="sxs-lookup"><span data-stu-id="bcb78-122">OUTPUTS</span></span>

### <span data-ttu-id="bcb78-123">PSApplicationGatewayWebApplicationFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bcb78-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="bcb78-124">筆記</span><span class="sxs-lookup"><span data-stu-id="bcb78-124">NOTES</span></span>

## <span data-ttu-id="bcb78-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcb78-125">RELATED LINKS</span></span>
