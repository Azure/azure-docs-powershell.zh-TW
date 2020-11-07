---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 97dc4b46f4a9156bc43e7902d50414a586d0f337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795368"
---
# <span data-ttu-id="c873e-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c873e-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="c873e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c873e-102">SYNOPSIS</span></span>
<span data-ttu-id="c873e-103">停止應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="c873e-103">Stops an application gateway</span></span>

## <span data-ttu-id="c873e-104">句法</span><span class="sxs-lookup"><span data-stu-id="c873e-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c873e-105">說明</span><span class="sxs-lookup"><span data-stu-id="c873e-105">DESCRIPTION</span></span>
<span data-ttu-id="c873e-106">**AzApplicationGateway** Cmdlet 會停止應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="c873e-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="c873e-107">示例</span><span class="sxs-lookup"><span data-stu-id="c873e-107">EXAMPLES</span></span>

### <span data-ttu-id="c873e-108">範例1：停止應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="c873e-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="c873e-109">這個命令會停止儲存在 $AppGw 變數中的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="c873e-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="c873e-110">參數</span><span class="sxs-lookup"><span data-stu-id="c873e-110">PARAMETERS</span></span>

### <span data-ttu-id="c873e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c873e-111">-ApplicationGateway</span></span>
<span data-ttu-id="c873e-112">指定此 Cmdlet 停止的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="c873e-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="c873e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c873e-113">-AsJob</span></span>
<span data-ttu-id="c873e-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c873e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c873e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c873e-115">-DefaultProfile</span></span>
<span data-ttu-id="c873e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c873e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c873e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c873e-117">CommonParameters</span></span>
<span data-ttu-id="c873e-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c873e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c873e-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c873e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c873e-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c873e-120">INPUTS</span></span>

### <span data-ttu-id="c873e-121">System.object</span><span class="sxs-lookup"><span data-stu-id="c873e-121">System.String</span></span>

## <span data-ttu-id="c873e-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c873e-122">OUTPUTS</span></span>

### <span data-ttu-id="c873e-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c873e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c873e-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c873e-124">NOTES</span></span>

## <span data-ttu-id="c873e-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c873e-125">RELATED LINKS</span></span>

[<span data-ttu-id="c873e-126">AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c873e-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="c873e-127">新-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c873e-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="c873e-128">移除-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c873e-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="c873e-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c873e-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="c873e-130">開始-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c873e-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


