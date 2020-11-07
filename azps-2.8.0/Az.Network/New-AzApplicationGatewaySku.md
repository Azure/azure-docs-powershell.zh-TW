---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 1d737733deb167510196555af4ad7b357cc60154
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789405"
---
# <span data-ttu-id="3bf17-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3bf17-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="3bf17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3bf17-102">SYNOPSIS</span></span>
<span data-ttu-id="3bf17-103">建立應用程式閘道的 SKU。</span><span class="sxs-lookup"><span data-stu-id="3bf17-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="3bf17-104">句法</span><span class="sxs-lookup"><span data-stu-id="3bf17-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bf17-105">說明</span><span class="sxs-lookup"><span data-stu-id="3bf17-105">DESCRIPTION</span></span>
<span data-ttu-id="3bf17-106">**新的-AzApplicationGatewaySku** Cmdlet 會為 Azure 應用程式閘道建立一個庫存單位 (SKU) 。</span><span class="sxs-lookup"><span data-stu-id="3bf17-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="3bf17-107">示例</span><span class="sxs-lookup"><span data-stu-id="3bf17-107">EXAMPLES</span></span>

### <span data-ttu-id="3bf17-108">範例1：建立 Azure 應用程式閘道的 SKU</span><span class="sxs-lookup"><span data-stu-id="3bf17-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="3bf17-109">這個命令會針對 Azure 應用程式閘道建立名為 Standard_Small 的 SKU，並將結果儲存在名為 $SKU 的變數中。</span><span class="sxs-lookup"><span data-stu-id="3bf17-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="3bf17-110">參數</span><span class="sxs-lookup"><span data-stu-id="3bf17-110">PARAMETERS</span></span>

### <span data-ttu-id="3bf17-111">-容量</span><span class="sxs-lookup"><span data-stu-id="3bf17-111">-Capacity</span></span>
<span data-ttu-id="3bf17-112">指定應用程式閘道的實例數。</span><span class="sxs-lookup"><span data-stu-id="3bf17-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="3bf17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bf17-113">-DefaultProfile</span></span>
<span data-ttu-id="3bf17-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bf17-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bf17-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3bf17-115">-Name</span></span>
<span data-ttu-id="3bf17-116">指定 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bf17-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="3bf17-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3bf17-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3bf17-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="3bf17-118">Standard_Small</span></span>
- <span data-ttu-id="3bf17-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="3bf17-119">Standard_Medium</span></span>
- <span data-ttu-id="3bf17-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="3bf17-120">Standard_Large</span></span>
- <span data-ttu-id="3bf17-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="3bf17-121">WAF_Medium</span></span>
- <span data-ttu-id="3bf17-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="3bf17-122">WAF_Large</span></span>

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

### <span data-ttu-id="3bf17-123">層級</span><span class="sxs-lookup"><span data-stu-id="3bf17-123">-Tier</span></span>
<span data-ttu-id="3bf17-124">指定 SKU 的層級。</span><span class="sxs-lookup"><span data-stu-id="3bf17-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="3bf17-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3bf17-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3bf17-126">標準</span><span class="sxs-lookup"><span data-stu-id="3bf17-126">Standard</span></span>
- <span data-ttu-id="3bf17-127">WAF</span><span class="sxs-lookup"><span data-stu-id="3bf17-127">WAF</span></span>

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

### <span data-ttu-id="3bf17-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bf17-128">CommonParameters</span></span>
<span data-ttu-id="3bf17-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3bf17-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bf17-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3bf17-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bf17-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3bf17-131">INPUTS</span></span>

### <span data-ttu-id="3bf17-132">所有</span><span class="sxs-lookup"><span data-stu-id="3bf17-132">None</span></span>

## <span data-ttu-id="3bf17-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3bf17-133">OUTPUTS</span></span>

### <span data-ttu-id="3bf17-134">PSApplicationGatewaySku 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3bf17-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="3bf17-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3bf17-135">NOTES</span></span>

## <span data-ttu-id="3bf17-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bf17-136">RELATED LINKS</span></span>

[<span data-ttu-id="3bf17-137">AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3bf17-137">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="3bf17-138">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3bf17-138">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)

