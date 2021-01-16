---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435788"
---
# <span data-ttu-id="cdd28-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cdd28-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="cdd28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cdd28-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd28-103">建立應用程式閘道的 SKU。</span><span class="sxs-lookup"><span data-stu-id="cdd28-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="cdd28-104">句法</span><span class="sxs-lookup"><span data-stu-id="cdd28-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdd28-105">說明</span><span class="sxs-lookup"><span data-stu-id="cdd28-105">DESCRIPTION</span></span>
<span data-ttu-id="cdd28-106">**新的-AzApplicationGatewaySku** Cmdlet 會為 Azure 應用程式閘道建立一個庫存單位 (SKU) 。</span><span class="sxs-lookup"><span data-stu-id="cdd28-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="cdd28-107">示例</span><span class="sxs-lookup"><span data-stu-id="cdd28-107">EXAMPLES</span></span>

### <span data-ttu-id="cdd28-108">範例1：建立 Azure 應用程式閘道的 SKU</span><span class="sxs-lookup"><span data-stu-id="cdd28-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="cdd28-109">這個命令會針對 Azure 應用程式閘道建立名為 Standard_Small 的 SKU，並將結果儲存在名為 $SKU 的變數中。</span><span class="sxs-lookup"><span data-stu-id="cdd28-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="cdd28-110">參數</span><span class="sxs-lookup"><span data-stu-id="cdd28-110">PARAMETERS</span></span>

### <span data-ttu-id="cdd28-111">-容量</span><span class="sxs-lookup"><span data-stu-id="cdd28-111">-Capacity</span></span>
<span data-ttu-id="cdd28-112">指定應用程式閘道的實例數。</span><span class="sxs-lookup"><span data-stu-id="cdd28-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="cdd28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd28-113">-DefaultProfile</span></span>
<span data-ttu-id="cdd28-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cdd28-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdd28-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="cdd28-115">-Name</span></span>
<span data-ttu-id="cdd28-116">指定 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdd28-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="cdd28-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cdd28-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cdd28-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="cdd28-118">Standard_Small</span></span>
- <span data-ttu-id="cdd28-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="cdd28-119">Standard_Medium</span></span>
- <span data-ttu-id="cdd28-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="cdd28-120">Standard_Large</span></span>
- <span data-ttu-id="cdd28-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="cdd28-121">WAF_Medium</span></span>
- <span data-ttu-id="cdd28-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="cdd28-122">WAF_Large</span></span>
- <span data-ttu-id="cdd28-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="cdd28-123">Standard_v2</span></span>
- <span data-ttu-id="cdd28-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="cdd28-124">WAF_v2</span></span>

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

### <span data-ttu-id="cdd28-125">層級</span><span class="sxs-lookup"><span data-stu-id="cdd28-125">-Tier</span></span>
<span data-ttu-id="cdd28-126">指定 SKU 的層級。</span><span class="sxs-lookup"><span data-stu-id="cdd28-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="cdd28-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cdd28-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cdd28-128">標準</span><span class="sxs-lookup"><span data-stu-id="cdd28-128">Standard</span></span>
- <span data-ttu-id="cdd28-129">WAF</span><span class="sxs-lookup"><span data-stu-id="cdd28-129">WAF</span></span>
- <span data-ttu-id="cdd28-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="cdd28-130">Standard_v2</span></span>
- <span data-ttu-id="cdd28-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="cdd28-131">WAF_v2</span></span>

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

### <span data-ttu-id="cdd28-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd28-132">CommonParameters</span></span>
<span data-ttu-id="cdd28-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cdd28-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd28-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cdd28-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd28-135">輸入</span><span class="sxs-lookup"><span data-stu-id="cdd28-135">INPUTS</span></span>

### <span data-ttu-id="cdd28-136">所有</span><span class="sxs-lookup"><span data-stu-id="cdd28-136">None</span></span>

## <span data-ttu-id="cdd28-137">輸出</span><span class="sxs-lookup"><span data-stu-id="cdd28-137">OUTPUTS</span></span>

### <span data-ttu-id="cdd28-138">PSApplicationGatewaySku 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cdd28-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="cdd28-139">筆記</span><span class="sxs-lookup"><span data-stu-id="cdd28-139">NOTES</span></span>

## <span data-ttu-id="cdd28-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="cdd28-140">RELATED LINKS</span></span>

[<span data-ttu-id="cdd28-141">AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cdd28-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="cdd28-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cdd28-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


