---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: eb1f0dadd905ff4b57a58c46f763f3c2dd51f256
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454308"
---
# <span data-ttu-id="41240-101">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="41240-101">New-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="41240-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41240-102">SYNOPSIS</span></span>
<span data-ttu-id="41240-103">建立應用程式閘道的 SKU。</span><span class="sxs-lookup"><span data-stu-id="41240-103">Creates a SKU for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41240-104">句法</span><span class="sxs-lookup"><span data-stu-id="41240-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41240-105">說明</span><span class="sxs-lookup"><span data-stu-id="41240-105">DESCRIPTION</span></span>
<span data-ttu-id="41240-106">**新的-AzureRmApplicationGatewaySku** Cmdlet 會為 Azure 應用程式閘道建立一個庫存單位 (SKU) 。</span><span class="sxs-lookup"><span data-stu-id="41240-106">The **New-AzureRmApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="41240-107">示例</span><span class="sxs-lookup"><span data-stu-id="41240-107">EXAMPLES</span></span>

### <span data-ttu-id="41240-108">範例1：建立 Azure 應用程式閘道的 SKU</span><span class="sxs-lookup"><span data-stu-id="41240-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="41240-109">這個命令會針對 Azure 應用程式閘道建立名為 Standard_Small 的 SKU，並將結果儲存在名為 $SKU 的變數中。</span><span class="sxs-lookup"><span data-stu-id="41240-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="41240-110">參數</span><span class="sxs-lookup"><span data-stu-id="41240-110">PARAMETERS</span></span>

### <span data-ttu-id="41240-111">-容量</span><span class="sxs-lookup"><span data-stu-id="41240-111">-Capacity</span></span>
<span data-ttu-id="41240-112">指定應用程式閘道的實例數。</span><span class="sxs-lookup"><span data-stu-id="41240-112">Specifies the number of instances of an application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41240-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="41240-113">-Name</span></span>
<span data-ttu-id="41240-114">指定 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="41240-114">Specifies the name of the SKU.</span></span>

<span data-ttu-id="41240-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="41240-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41240-116">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="41240-116">Standard_Small</span></span>
- <span data-ttu-id="41240-117">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="41240-117">Standard_Medium</span></span>
- <span data-ttu-id="41240-118">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="41240-118">Standard_Large</span></span>
- <span data-ttu-id="41240-119">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="41240-119">WAF_Medium</span></span>
- <span data-ttu-id="41240-120">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="41240-120">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41240-121">層級</span><span class="sxs-lookup"><span data-stu-id="41240-121">-Tier</span></span>
<span data-ttu-id="41240-122">指定 SKU 的層級。</span><span class="sxs-lookup"><span data-stu-id="41240-122">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="41240-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="41240-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41240-124">標準</span><span class="sxs-lookup"><span data-stu-id="41240-124">Standard</span></span>
- <span data-ttu-id="41240-125">WAF</span><span class="sxs-lookup"><span data-stu-id="41240-125">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41240-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41240-126">-DefaultProfile</span></span>
<span data-ttu-id="41240-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41240-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41240-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41240-128">CommonParameters</span></span>
<span data-ttu-id="41240-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41240-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41240-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41240-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41240-131">輸入</span><span class="sxs-lookup"><span data-stu-id="41240-131">INPUTS</span></span>

### <span data-ttu-id="41240-132">System.object</span><span class="sxs-lookup"><span data-stu-id="41240-132">System.String</span></span>

## <span data-ttu-id="41240-133">輸出</span><span class="sxs-lookup"><span data-stu-id="41240-133">OUTPUTS</span></span>

### <span data-ttu-id="41240-134">PSApplicationGatewaySku 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="41240-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="41240-135">筆記</span><span class="sxs-lookup"><span data-stu-id="41240-135">NOTES</span></span>

## <span data-ttu-id="41240-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="41240-136">RELATED LINKS</span></span>

[<span data-ttu-id="41240-137">AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="41240-137">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="41240-138">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="41240-138">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


