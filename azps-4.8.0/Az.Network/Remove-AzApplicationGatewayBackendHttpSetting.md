---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 9db92f11a7401eec1643156490079da8ff2b00d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127495"
---
# <span data-ttu-id="a6de6-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a6de6-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="a6de6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6de6-102">SYNOPSIS</span></span>
<span data-ttu-id="a6de6-103">從應用程式閘道移除後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="a6de6-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="a6de6-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6de6-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6de6-105">說明</span><span class="sxs-lookup"><span data-stu-id="a6de6-105">DESCRIPTION</span></span>
<span data-ttu-id="a6de6-106">Remove-AzApplicationGatewayBackendHttpSetting Cmdlet 會從 Azure 應用程式閘道 (HTTP) 設定中移除後端超文字傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a6de6-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="a6de6-107">示例</span><span class="sxs-lookup"><span data-stu-id="a6de6-107">EXAMPLES</span></span>

### <span data-ttu-id="a6de6-108">範例1：從應用程式閘道移除後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="a6de6-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="a6de6-109">第一個命令會取得一個名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="a6de6-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a6de6-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 BackEndSetting02 的後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="a6de6-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a6de6-111">參數</span><span class="sxs-lookup"><span data-stu-id="a6de6-111">PARAMETERS</span></span>

### <span data-ttu-id="a6de6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a6de6-112">-ApplicationGateway</span></span>
<span data-ttu-id="a6de6-113">指定此 Cmdlet 移除後端 HTTP 設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="a6de6-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="a6de6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6de6-114">-DefaultProfile</span></span>
<span data-ttu-id="a6de6-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6de6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6de6-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6de6-116">-Name</span></span>
<span data-ttu-id="a6de6-117">指定此 Cmdlet 移除之後端 HTTP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6de6-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6de6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6de6-118">CommonParameters</span></span>
<span data-ttu-id="a6de6-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6de6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6de6-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6de6-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6de6-121">輸入</span><span class="sxs-lookup"><span data-stu-id="a6de6-121">INPUTS</span></span>

### <span data-ttu-id="a6de6-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a6de6-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a6de6-123">輸出</span><span class="sxs-lookup"><span data-stu-id="a6de6-123">OUTPUTS</span></span>

### <span data-ttu-id="a6de6-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a6de6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a6de6-125">筆記</span><span class="sxs-lookup"><span data-stu-id="a6de6-125">NOTES</span></span>

## <span data-ttu-id="a6de6-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6de6-126">RELATED LINKS</span></span>

[<span data-ttu-id="a6de6-127">附加 AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a6de6-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="a6de6-128">新-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a6de6-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="a6de6-129">AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a6de6-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="a6de6-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a6de6-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

