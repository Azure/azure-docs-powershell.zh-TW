---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 1f99fe982496fc6cef3ee9579d8e0be555880aaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916005"
---
# <span data-ttu-id="f9aac-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f9aac-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="f9aac-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f9aac-102">SYNOPSIS</span></span>
<span data-ttu-id="f9aac-103">為應用程式閘道建立 SKU。</span><span class="sxs-lookup"><span data-stu-id="f9aac-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="f9aac-104">語法</span><span class="sxs-lookup"><span data-stu-id="f9aac-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9aac-105">描述</span><span class="sxs-lookup"><span data-stu-id="f9aac-105">DESCRIPTION</span></span>
<span data-ttu-id="f9aac-106">**New-AzApplicationGatewaySku** Cmdlet 會為 Azure 應用程式閘道 (SKU) 庫存單位。</span><span class="sxs-lookup"><span data-stu-id="f9aac-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="f9aac-107">例子</span><span class="sxs-lookup"><span data-stu-id="f9aac-107">EXAMPLES</span></span>

### <span data-ttu-id="f9aac-108">範例 1：為 Azure 應用程式閘道建立 SKU</span><span class="sxs-lookup"><span data-stu-id="f9aac-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="f9aac-109">此命令會為 Azure 應用程式閘道Standard_Small名為 SKU，並儲存在名為 $SKU 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f9aac-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="f9aac-110">參數</span><span class="sxs-lookup"><span data-stu-id="f9aac-110">PARAMETERS</span></span>

### <span data-ttu-id="f9aac-111">-容量</span><span class="sxs-lookup"><span data-stu-id="f9aac-111">-Capacity</span></span>
<span data-ttu-id="f9aac-112">指定應用程式閘道的實例數目。</span><span class="sxs-lookup"><span data-stu-id="f9aac-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="f9aac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9aac-113">-DefaultProfile</span></span>
<span data-ttu-id="f9aac-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9aac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9aac-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9aac-115">-Name</span></span>
<span data-ttu-id="f9aac-116">指定 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9aac-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="f9aac-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f9aac-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f9aac-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="f9aac-118">Standard_Small</span></span>
- <span data-ttu-id="f9aac-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="f9aac-119">Standard_Medium</span></span>
- <span data-ttu-id="f9aac-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="f9aac-120">Standard_Large</span></span>
- <span data-ttu-id="f9aac-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="f9aac-121">WAF_Medium</span></span>
- <span data-ttu-id="f9aac-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="f9aac-122">WAF_Large</span></span>
- <span data-ttu-id="f9aac-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="f9aac-123">Standard_v2</span></span>
- <span data-ttu-id="f9aac-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="f9aac-124">WAF_v2</span></span>

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

### <span data-ttu-id="f9aac-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="f9aac-125">-Tier</span></span>
<span data-ttu-id="f9aac-126">指定 SKU 的層級。</span><span class="sxs-lookup"><span data-stu-id="f9aac-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="f9aac-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f9aac-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f9aac-128">標準</span><span class="sxs-lookup"><span data-stu-id="f9aac-128">Standard</span></span>
- <span data-ttu-id="f9aac-129">WAF</span><span class="sxs-lookup"><span data-stu-id="f9aac-129">WAF</span></span>
- <span data-ttu-id="f9aac-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="f9aac-130">Standard_v2</span></span>
- <span data-ttu-id="f9aac-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="f9aac-131">WAF_v2</span></span>

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

### <span data-ttu-id="f9aac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9aac-132">CommonParameters</span></span>
<span data-ttu-id="f9aac-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f9aac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9aac-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f9aac-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9aac-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f9aac-135">INPUTS</span></span>

### <span data-ttu-id="f9aac-136">沒有</span><span class="sxs-lookup"><span data-stu-id="f9aac-136">None</span></span>

## <span data-ttu-id="f9aac-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f9aac-137">OUTPUTS</span></span>

### <span data-ttu-id="f9aac-138">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f9aac-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="f9aac-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f9aac-139">NOTES</span></span>

## <span data-ttu-id="f9aac-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9aac-140">RELATED LINKS</span></span>

[<span data-ttu-id="f9aac-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f9aac-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="f9aac-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f9aac-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


