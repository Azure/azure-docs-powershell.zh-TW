---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: bfaf9773582b201de8f6066a30a55c0fd5f5b7ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970881"
---
# <span data-ttu-id="6a1c6-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6a1c6-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="6a1c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6a1c6-102">SYNOPSIS</span></span>
<span data-ttu-id="6a1c6-103">修改應用程式閘道的 SKU。</span><span class="sxs-lookup"><span data-stu-id="6a1c6-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="6a1c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="6a1c6-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a1c6-105">說明</span><span class="sxs-lookup"><span data-stu-id="6a1c6-105">DESCRIPTION</span></span>
<span data-ttu-id="6a1c6-106">**AzApplicationGatewaySku** Cmdlet 會修改應用程式閘道的庫存單位 (SKU) 。</span><span class="sxs-lookup"><span data-stu-id="6a1c6-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="6a1c6-107">示例</span><span class="sxs-lookup"><span data-stu-id="6a1c6-107">EXAMPLES</span></span>

### <span data-ttu-id="6a1c6-108">範例1：更新應用程式閘道 SKU</span><span class="sxs-lookup"><span data-stu-id="6a1c6-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="6a1c6-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將其儲存在名為 ResourceGroup01 的資源群組中，然後將其儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="6a1c6-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6a1c6-110">第二個命令會更新應用程式閘道的 SKU。</span><span class="sxs-lookup"><span data-stu-id="6a1c6-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="6a1c6-111">參數</span><span class="sxs-lookup"><span data-stu-id="6a1c6-111">PARAMETERS</span></span>

### <span data-ttu-id="6a1c6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a1c6-112">-ApplicationGateway</span></span>
<span data-ttu-id="6a1c6-113">指定此 Cmdlet 關聯 SKU 的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="6a1c6-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a1c6-114">-容量</span><span class="sxs-lookup"><span data-stu-id="6a1c6-114">-Capacity</span></span>
<span data-ttu-id="6a1c6-115">指定應用程式閘道的實例計數。</span><span class="sxs-lookup"><span data-stu-id="6a1c6-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a1c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a1c6-116">-DefaultProfile</span></span>
<span data-ttu-id="6a1c6-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a1c6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a1c6-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a1c6-118">-Name</span></span>
<span data-ttu-id="6a1c6-119">指定應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a1c6-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="6a1c6-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6a1c6-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a1c6-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="6a1c6-121">Standard_Small</span></span>
- <span data-ttu-id="6a1c6-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="6a1c6-122">Standard_Medium</span></span>
- <span data-ttu-id="6a1c6-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="6a1c6-123">Standard_Large</span></span>
- <span data-ttu-id="6a1c6-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="6a1c6-124">WAF_Medium</span></span>
- <span data-ttu-id="6a1c6-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="6a1c6-125">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a1c6-126">層級</span><span class="sxs-lookup"><span data-stu-id="6a1c6-126">-Tier</span></span>
<span data-ttu-id="6a1c6-127">指定應用程式閘道的層級。</span><span class="sxs-lookup"><span data-stu-id="6a1c6-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="6a1c6-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6a1c6-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a1c6-129">標準</span><span class="sxs-lookup"><span data-stu-id="6a1c6-129">Standard</span></span>
- <span data-ttu-id="6a1c6-130">WAF</span><span class="sxs-lookup"><span data-stu-id="6a1c6-130">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, WAF, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a1c6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a1c6-131">CommonParameters</span></span>
<span data-ttu-id="6a1c6-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6a1c6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a1c6-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6a1c6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a1c6-134">輸入</span><span class="sxs-lookup"><span data-stu-id="6a1c6-134">INPUTS</span></span>

### <span data-ttu-id="6a1c6-135">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6a1c6-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6a1c6-136">輸出</span><span class="sxs-lookup"><span data-stu-id="6a1c6-136">OUTPUTS</span></span>

### <span data-ttu-id="6a1c6-137">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6a1c6-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6a1c6-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6a1c6-138">NOTES</span></span>

## <span data-ttu-id="6a1c6-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a1c6-139">RELATED LINKS</span></span>

[<span data-ttu-id="6a1c6-140">AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6a1c6-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="6a1c6-141">新-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6a1c6-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


