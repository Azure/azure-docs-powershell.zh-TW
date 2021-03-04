---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 2490896fa66a3d06a8887e386c2bf6db6ff2f829
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912762"
---
# <span data-ttu-id="44185-101">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="44185-101">Get-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="44185-102">簡介</span><span class="sxs-lookup"><span data-stu-id="44185-102">SYNOPSIS</span></span>
<span data-ttu-id="44185-103">獲得應用程式閘道的 SSL 設定檔。</span><span class="sxs-lookup"><span data-stu-id="44185-103">Gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="44185-104">語法</span><span class="sxs-lookup"><span data-stu-id="44185-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44185-105">描述</span><span class="sxs-lookup"><span data-stu-id="44185-105">DESCRIPTION</span></span>
<span data-ttu-id="44185-106">**Get-AzApplicationGatewayslProfile** Cmdlet 會取得應用程式閘道的 SSL 設定檔。</span><span class="sxs-lookup"><span data-stu-id="44185-106">The **Get-AzApplicationGatewaySslProfile** cmdlet gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="44185-107">例子</span><span class="sxs-lookup"><span data-stu-id="44185-107">EXAMPLES</span></span>

### <span data-ttu-id="44185-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="44185-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

<span data-ttu-id="44185-109">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在 $AppGw 變數中。第二個命令會獲得 ssl profile SslProfile01 for $AppGw，並儲存在$profile變數中。</span><span class="sxs-lookup"><span data-stu-id="44185-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the SSL profile SslProfile01 for $AppGw and stores it in the $profile variable.</span></span>

## <span data-ttu-id="44185-110">參數</span><span class="sxs-lookup"><span data-stu-id="44185-110">PARAMETERS</span></span>

### <span data-ttu-id="44185-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="44185-111">-ApplicationGateway</span></span>
<span data-ttu-id="44185-112">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="44185-112">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44185-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44185-113">-DefaultProfile</span></span>
<span data-ttu-id="44185-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="44185-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44185-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="44185-115">-Name</span></span>
<span data-ttu-id="44185-116">ssl 設定檔的名稱</span><span class="sxs-lookup"><span data-stu-id="44185-116">The name of the ssl profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44185-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44185-117">CommonParameters</span></span>
<span data-ttu-id="44185-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="44185-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44185-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44185-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44185-120">輸入</span><span class="sxs-lookup"><span data-stu-id="44185-120">INPUTS</span></span>

### <span data-ttu-id="44185-121">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="44185-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="44185-122">輸出</span><span class="sxs-lookup"><span data-stu-id="44185-122">OUTPUTS</span></span>

### <span data-ttu-id="44185-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="44185-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="44185-124">筆記</span><span class="sxs-lookup"><span data-stu-id="44185-124">NOTES</span></span>

## <span data-ttu-id="44185-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="44185-125">RELATED LINKS</span></span>

[<span data-ttu-id="44185-126">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="44185-126">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="44185-127">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="44185-127">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="44185-128">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="44185-128">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="44185-129">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="44185-129">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)