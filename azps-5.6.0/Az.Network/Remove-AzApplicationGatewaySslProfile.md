---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ab8afdb01a2993330c75b23b02392ee583cad297
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913470"
---
# <span data-ttu-id="d8f79-101">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d8f79-101">Remove-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="d8f79-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d8f79-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f79-103">從應用程式閘道移除 ssl 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d8f79-103">Removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="d8f79-104">語法</span><span class="sxs-lookup"><span data-stu-id="d8f79-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8f79-105">描述</span><span class="sxs-lookup"><span data-stu-id="d8f79-105">DESCRIPTION</span></span>
<span data-ttu-id="d8f79-106">**Remove-AzApplicationGatewaySslProfile** Cmdlet 會從應用程式閘道移除 ssl 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d8f79-106">The **Remove-AzApplicationGatewaySslProfile** cmdlet removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="d8f79-107">例子</span><span class="sxs-lookup"><span data-stu-id="d8f79-107">EXAMPLES</span></span>

### <span data-ttu-id="d8f79-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="d8f79-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

<span data-ttu-id="d8f79-109">第一個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="d8f79-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="d8f79-110">第二個命令會從儲存在 $AppGw 的應用程式閘道移除名為 SslProfile01 的 ssl 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d8f79-110">The second command removes the ssl profile named SslProfile01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="d8f79-111">參數</span><span class="sxs-lookup"><span data-stu-id="d8f79-111">PARAMETERS</span></span>

### <span data-ttu-id="d8f79-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8f79-112">-ApplicationGateway</span></span>
<span data-ttu-id="d8f79-113">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="d8f79-113">The applicationGateway</span></span>

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

### <span data-ttu-id="d8f79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f79-114">-DefaultProfile</span></span>
<span data-ttu-id="d8f79-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8f79-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8f79-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8f79-116">-Name</span></span>
<span data-ttu-id="d8f79-117">ssl 設定檔的名稱</span><span class="sxs-lookup"><span data-stu-id="d8f79-117">The name of the ssl profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f79-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f79-118">CommonParameters</span></span>
<span data-ttu-id="d8f79-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d8f79-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f79-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8f79-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f79-121">輸入</span><span class="sxs-lookup"><span data-stu-id="d8f79-121">INPUTS</span></span>

### <span data-ttu-id="d8f79-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8f79-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8f79-123">輸出</span><span class="sxs-lookup"><span data-stu-id="d8f79-123">OUTPUTS</span></span>

### <span data-ttu-id="d8f79-124">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8f79-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8f79-125">筆記</span><span class="sxs-lookup"><span data-stu-id="d8f79-125">NOTES</span></span>

## <span data-ttu-id="d8f79-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8f79-126">RELATED LINKS</span></span>

[<span data-ttu-id="d8f79-127">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d8f79-127">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d8f79-128">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d8f79-128">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d8f79-129">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d8f79-129">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d8f79-130">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d8f79-130">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)