---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: a0a8c3d3f2e058fa51283a02ecb53df62c0b8970
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795436"
---
# <span data-ttu-id="ae4e6-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ae4e6-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="ae4e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae4e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4e6-103">修改應用程式閘道的 SKU。</span><span class="sxs-lookup"><span data-stu-id="ae4e6-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="ae4e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae4e6-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae4e6-105">說明</span><span class="sxs-lookup"><span data-stu-id="ae4e6-105">DESCRIPTION</span></span>
<span data-ttu-id="ae4e6-106">**AzApplicationGatewaySku** Cmdlet 會修改應用程式閘道的庫存單位 (SKU) 。</span><span class="sxs-lookup"><span data-stu-id="ae4e6-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="ae4e6-107">示例</span><span class="sxs-lookup"><span data-stu-id="ae4e6-107">EXAMPLES</span></span>

### <span data-ttu-id="ae4e6-108">範例1：更新應用程式閘道 SKU</span><span class="sxs-lookup"><span data-stu-id="ae4e6-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="ae4e6-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將其儲存在名為 ResourceGroup01 的資源群組中，然後將其儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="ae4e6-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="ae4e6-110">第二個命令會更新應用程式閘道的 SKU。</span><span class="sxs-lookup"><span data-stu-id="ae4e6-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="ae4e6-111">參數</span><span class="sxs-lookup"><span data-stu-id="ae4e6-111">PARAMETERS</span></span>

### <span data-ttu-id="ae4e6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae4e6-112">-ApplicationGateway</span></span>
<span data-ttu-id="ae4e6-113">指定此 Cmdlet 關聯 SKU 的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="ae4e6-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="ae4e6-114">-容量</span><span class="sxs-lookup"><span data-stu-id="ae4e6-114">-Capacity</span></span>
<span data-ttu-id="ae4e6-115">指定應用程式閘道的實例計數。</span><span class="sxs-lookup"><span data-stu-id="ae4e6-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae4e6-116">-DefaultProfile</span></span>
<span data-ttu-id="ae4e6-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae4e6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4e6-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae4e6-118">-Name</span></span>
<span data-ttu-id="ae4e6-119">指定應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae4e6-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="ae4e6-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ae4e6-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae4e6-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="ae4e6-121">Standard_Small</span></span>
- <span data-ttu-id="ae4e6-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="ae4e6-122">Standard_Medium</span></span>
- <span data-ttu-id="ae4e6-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="ae4e6-123">Standard_Large</span></span>
- <span data-ttu-id="ae4e6-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="ae4e6-124">WAF_Medium</span></span>
- <span data-ttu-id="ae4e6-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="ae4e6-125">WAF_Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4e6-126">層級</span><span class="sxs-lookup"><span data-stu-id="ae4e6-126">-Tier</span></span>
<span data-ttu-id="ae4e6-127">指定應用程式閘道的層級。</span><span class="sxs-lookup"><span data-stu-id="ae4e6-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="ae4e6-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ae4e6-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae4e6-129">標準</span><span class="sxs-lookup"><span data-stu-id="ae4e6-129">Standard</span></span>
- <span data-ttu-id="ae4e6-130">WAF</span><span class="sxs-lookup"><span data-stu-id="ae4e6-130">WAF</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4e6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4e6-131">CommonParameters</span></span>
<span data-ttu-id="ae4e6-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae4e6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4e6-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ae4e6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4e6-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ae4e6-134">INPUTS</span></span>

### <span data-ttu-id="ae4e6-135">System.object</span><span class="sxs-lookup"><span data-stu-id="ae4e6-135">System.String</span></span>

## <span data-ttu-id="ae4e6-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ae4e6-136">OUTPUTS</span></span>

### <span data-ttu-id="ae4e6-137">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ae4e6-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ae4e6-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ae4e6-138">NOTES</span></span>

## <span data-ttu-id="ae4e6-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae4e6-139">RELATED LINKS</span></span>

[<span data-ttu-id="ae4e6-140">AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ae4e6-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="ae4e6-141">新-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ae4e6-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


