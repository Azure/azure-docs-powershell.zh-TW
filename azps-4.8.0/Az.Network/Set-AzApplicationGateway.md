---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: c7d8e147d227ac630709d28dca069955cb9dc512
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135777"
---
# <span data-ttu-id="5e25e-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e25e-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="5e25e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e25e-102">SYNOPSIS</span></span>
<span data-ttu-id="5e25e-103">更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5e25e-103">Updates an application gateway.</span></span>

## <span data-ttu-id="5e25e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e25e-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e25e-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e25e-105">DESCRIPTION</span></span>
<span data-ttu-id="5e25e-106">**AzApplicationGateway** Cmdlet 會更新 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5e25e-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="5e25e-107">示例</span><span class="sxs-lookup"><span data-stu-id="5e25e-107">EXAMPLES</span></span>

### <span data-ttu-id="5e25e-108">範例1：更新應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="5e25e-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="5e25e-109">這個命令會使用 $AppGw 變數中的設定來更新應用程式閘道，並將更新的閘道儲存在 $UpdatedAppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="5e25e-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="5e25e-110">參數</span><span class="sxs-lookup"><span data-stu-id="5e25e-110">PARAMETERS</span></span>

### <span data-ttu-id="5e25e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e25e-111">-ApplicationGateway</span></span>
<span data-ttu-id="5e25e-112">指定代表應用程式閘道應該設定之狀態的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="5e25e-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="5e25e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e25e-113">-AsJob</span></span>
<span data-ttu-id="5e25e-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5e25e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e25e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e25e-115">-DefaultProfile</span></span>
<span data-ttu-id="5e25e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e25e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e25e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e25e-117">CommonParameters</span></span>
<span data-ttu-id="5e25e-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e25e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e25e-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5e25e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e25e-120">輸入</span><span class="sxs-lookup"><span data-stu-id="5e25e-120">INPUTS</span></span>

### <span data-ttu-id="5e25e-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5e25e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e25e-122">輸出</span><span class="sxs-lookup"><span data-stu-id="5e25e-122">OUTPUTS</span></span>

### <span data-ttu-id="5e25e-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5e25e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e25e-124">筆記</span><span class="sxs-lookup"><span data-stu-id="5e25e-124">NOTES</span></span>

## <span data-ttu-id="5e25e-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e25e-125">RELATED LINKS</span></span>

[<span data-ttu-id="5e25e-126">開始-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e25e-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


