---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 74b8664a9b57089fd116620779354515ea984c79
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800338"
---
# <span data-ttu-id="88239-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88239-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="88239-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88239-102">SYNOPSIS</span></span>
<span data-ttu-id="88239-103">停止應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="88239-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88239-104">句法</span><span class="sxs-lookup"><span data-stu-id="88239-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88239-105">說明</span><span class="sxs-lookup"><span data-stu-id="88239-105">DESCRIPTION</span></span>
<span data-ttu-id="88239-106">**AzureRmApplicationGateway** Cmdlet 會停止應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="88239-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="88239-107">示例</span><span class="sxs-lookup"><span data-stu-id="88239-107">EXAMPLES</span></span>

### <span data-ttu-id="88239-108">範例1：停止應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="88239-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="88239-109">這個命令會停止儲存在 $AppGw 變數中的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="88239-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="88239-110">參數</span><span class="sxs-lookup"><span data-stu-id="88239-110">PARAMETERS</span></span>

### <span data-ttu-id="88239-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88239-111">-ApplicationGateway</span></span>
<span data-ttu-id="88239-112">指定此 Cmdlet 停止的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="88239-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="88239-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88239-113">-AsJob</span></span>
<span data-ttu-id="88239-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="88239-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88239-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88239-115">-DefaultProfile</span></span>
<span data-ttu-id="88239-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88239-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88239-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88239-117">CommonParameters</span></span>
<span data-ttu-id="88239-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88239-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88239-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88239-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88239-120">輸入</span><span class="sxs-lookup"><span data-stu-id="88239-120">INPUTS</span></span>

### <span data-ttu-id="88239-121">System.object</span><span class="sxs-lookup"><span data-stu-id="88239-121">System.String</span></span>

## <span data-ttu-id="88239-122">輸出</span><span class="sxs-lookup"><span data-stu-id="88239-122">OUTPUTS</span></span>

### <span data-ttu-id="88239-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="88239-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="88239-124">筆記</span><span class="sxs-lookup"><span data-stu-id="88239-124">NOTES</span></span>

## <span data-ttu-id="88239-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="88239-125">RELATED LINKS</span></span>

[<span data-ttu-id="88239-126">AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88239-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="88239-127">新-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88239-127">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="88239-128">移除-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88239-128">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="88239-129">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88239-129">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="88239-130">開始-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88239-130">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


