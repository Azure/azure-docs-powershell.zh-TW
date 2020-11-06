---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 2481fa04c8c31e9537fcb53801edad181b3812d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446721"
---
# <span data-ttu-id="0666f-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0666f-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="0666f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0666f-102">SYNOPSIS</span></span>
<span data-ttu-id="0666f-103">從應用程式閘道移除後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="0666f-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0666f-104">句法</span><span class="sxs-lookup"><span data-stu-id="0666f-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0666f-105">說明</span><span class="sxs-lookup"><span data-stu-id="0666f-105">DESCRIPTION</span></span>
<span data-ttu-id="0666f-106">Remove-AzureRmApplicationGatewayBackendHttpSettings Cmdlet 會從 Azure 應用程式閘道 (HTTP) 設定中移除後端超文字傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0666f-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="0666f-107">示例</span><span class="sxs-lookup"><span data-stu-id="0666f-107">EXAMPLES</span></span>

### <span data-ttu-id="0666f-108">範例1：從應用程式閘道移除後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="0666f-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="0666f-109">第一個命令會取得一個名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="0666f-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="0666f-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 BackEndSetting02 的後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="0666f-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="0666f-111">參數</span><span class="sxs-lookup"><span data-stu-id="0666f-111">PARAMETERS</span></span>

### <span data-ttu-id="0666f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0666f-112">-ApplicationGateway</span></span>
<span data-ttu-id="0666f-113">指定此 Cmdlet 移除後端 HTTP 設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0666f-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="0666f-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="0666f-114">-Name</span></span>
<span data-ttu-id="0666f-115">指定此 Cmdlet 移除之後端 HTTP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="0666f-115">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0666f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0666f-116">-DefaultProfile</span></span>
<span data-ttu-id="0666f-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0666f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0666f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0666f-118">CommonParameters</span></span>
<span data-ttu-id="0666f-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0666f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0666f-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0666f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0666f-121">輸入</span><span class="sxs-lookup"><span data-stu-id="0666f-121">INPUTS</span></span>

### <span data-ttu-id="0666f-122">System.object</span><span class="sxs-lookup"><span data-stu-id="0666f-122">System.String</span></span>

## <span data-ttu-id="0666f-123">輸出</span><span class="sxs-lookup"><span data-stu-id="0666f-123">OUTPUTS</span></span>

### <span data-ttu-id="0666f-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0666f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0666f-125">筆記</span><span class="sxs-lookup"><span data-stu-id="0666f-125">NOTES</span></span>

## <span data-ttu-id="0666f-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="0666f-126">RELATED LINKS</span></span>

[<span data-ttu-id="0666f-127">附加 AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0666f-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="0666f-128">新-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0666f-128">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="0666f-129">AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0666f-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="0666f-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0666f-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

