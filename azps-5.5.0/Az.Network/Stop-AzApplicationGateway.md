---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 4c7001bf69e6dc8f418f1bc56867154bf9d769ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128674"
---
# <span data-ttu-id="ced87-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ced87-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="ced87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ced87-102">SYNOPSIS</span></span>
<span data-ttu-id="ced87-103">停止應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="ced87-103">Stops an application gateway</span></span>

## <span data-ttu-id="ced87-104">句法</span><span class="sxs-lookup"><span data-stu-id="ced87-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ced87-105">說明</span><span class="sxs-lookup"><span data-stu-id="ced87-105">DESCRIPTION</span></span>
<span data-ttu-id="ced87-106">**AzApplicationGateway** Cmdlet 會停止應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ced87-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="ced87-107">示例</span><span class="sxs-lookup"><span data-stu-id="ced87-107">EXAMPLES</span></span>

### <span data-ttu-id="ced87-108">範例1：停止應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="ced87-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="ced87-109">這個命令會停止儲存在 $AppGw 變數中的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ced87-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="ced87-110">參數</span><span class="sxs-lookup"><span data-stu-id="ced87-110">PARAMETERS</span></span>

### <span data-ttu-id="ced87-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ced87-111">-ApplicationGateway</span></span>
<span data-ttu-id="ced87-112">指定此 Cmdlet 停止的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ced87-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="ced87-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ced87-113">-AsJob</span></span>
<span data-ttu-id="ced87-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ced87-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced87-115">-DefaultProfile</span></span>
<span data-ttu-id="ced87-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ced87-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ced87-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced87-117">CommonParameters</span></span>
<span data-ttu-id="ced87-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ced87-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced87-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ced87-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced87-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ced87-120">INPUTS</span></span>

### <span data-ttu-id="ced87-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ced87-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ced87-122">輸出</span><span class="sxs-lookup"><span data-stu-id="ced87-122">OUTPUTS</span></span>

### <span data-ttu-id="ced87-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ced87-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ced87-124">筆記</span><span class="sxs-lookup"><span data-stu-id="ced87-124">NOTES</span></span>

## <span data-ttu-id="ced87-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="ced87-125">RELATED LINKS</span></span>

[<span data-ttu-id="ced87-126">AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ced87-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="ced87-127">新-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ced87-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="ced87-128">移除-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ced87-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="ced87-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ced87-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="ced87-130">開始-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ced87-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


