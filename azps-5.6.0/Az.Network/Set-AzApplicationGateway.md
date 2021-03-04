---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: ca59a1b2e156bc23b082a8307eb034b13b78105e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915337"
---
# <span data-ttu-id="d7fd8-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7fd8-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="d7fd8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d7fd8-102">SYNOPSIS</span></span>
<span data-ttu-id="d7fd8-103">更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d7fd8-103">Updates an application gateway.</span></span>

## <span data-ttu-id="d7fd8-104">語法</span><span class="sxs-lookup"><span data-stu-id="d7fd8-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7fd8-105">描述</span><span class="sxs-lookup"><span data-stu-id="d7fd8-105">DESCRIPTION</span></span>
<span data-ttu-id="d7fd8-106">**Set-AzApplicationGateway** Cmdlet 會更新 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d7fd8-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="d7fd8-107">例子</span><span class="sxs-lookup"><span data-stu-id="d7fd8-107">EXAMPLES</span></span>

### <span data-ttu-id="d7fd8-108">範例 1：更新應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="d7fd8-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name Test -ResourceGroupName Appgwtest
PS C:\>$AppGw.Tag = @{"key"="value"}
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="d7fd8-109">這些命令會以 $AppGw 變數中的設定更新應用程式閘道，並儲存更新後的閘道$UpdatedAppGw變數。</span><span class="sxs-lookup"><span data-stu-id="d7fd8-109">These commands update the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="d7fd8-110">參數</span><span class="sxs-lookup"><span data-stu-id="d7fd8-110">PARAMETERS</span></span>

### <span data-ttu-id="d7fd8-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7fd8-111">-ApplicationGateway</span></span>
<span data-ttu-id="d7fd8-112">指定代表應設定應用程式閘道之狀態的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="d7fd8-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="d7fd8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7fd8-113">-AsJob</span></span>
<span data-ttu-id="d7fd8-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d7fd8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7fd8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7fd8-115">-DefaultProfile</span></span>
<span data-ttu-id="d7fd8-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d7fd8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7fd8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7fd8-117">CommonParameters</span></span>
<span data-ttu-id="d7fd8-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d7fd8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7fd8-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7fd8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7fd8-120">輸入</span><span class="sxs-lookup"><span data-stu-id="d7fd8-120">INPUTS</span></span>

### <span data-ttu-id="d7fd8-121">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7fd8-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d7fd8-122">輸出</span><span class="sxs-lookup"><span data-stu-id="d7fd8-122">OUTPUTS</span></span>

### <span data-ttu-id="d7fd8-123">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7fd8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d7fd8-124">筆記</span><span class="sxs-lookup"><span data-stu-id="d7fd8-124">NOTES</span></span>

## <span data-ttu-id="d7fd8-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7fd8-125">RELATED LINKS</span></span>

[<span data-ttu-id="d7fd8-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7fd8-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


