---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 49d55a48f9e9b769854a5cd01929188fd7993d35
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415558"
---
# <span data-ttu-id="f5d23-101">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f5d23-101">Get-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="f5d23-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f5d23-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d23-103">獲得應用程式閘道 SSL 設定檔的 SSL 策略。</span><span class="sxs-lookup"><span data-stu-id="f5d23-103">Gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="f5d23-104">語法</span><span class="sxs-lookup"><span data-stu-id="f5d23-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5d23-105">描述</span><span class="sxs-lookup"><span data-stu-id="f5d23-105">DESCRIPTION</span></span>
<span data-ttu-id="f5d23-106">**Get-AzApplicationGatewaySslProfilePolicy** Cmdlet 會取得應用程式閘道 SSL 設定檔的 SSL 策略。</span><span class="sxs-lookup"><span data-stu-id="f5d23-106">The **Get-AzApplicationGatewaySslProfilePolicy** cmdlet gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="f5d23-107">例子</span><span class="sxs-lookup"><span data-stu-id="f5d23-107">EXAMPLES</span></span>

### <span data-ttu-id="f5d23-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f5d23-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

<span data-ttu-id="f5d23-109">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="f5d23-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="f5d23-110">第二個命令會獲得名稱為 SslProfile01 的 SSL 設定檔，$AppGw儲存為$SslProfile變數。</span><span class="sxs-lookup"><span data-stu-id="f5d23-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="f5d23-111">最後一個命令會從 SSL 設定檔中$SslProfile SSL 策略，並儲存在$sslpolicy變數中。</span><span class="sxs-lookup"><span data-stu-id="f5d23-111">The last command gets the SSL policy from the SSL profile $SslProfile and stores it in the $sslpolicy variable.</span></span>

## <span data-ttu-id="f5d23-112">參數</span><span class="sxs-lookup"><span data-stu-id="f5d23-112">PARAMETERS</span></span>

### <span data-ttu-id="f5d23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5d23-113">-DefaultProfile</span></span>
<span data-ttu-id="f5d23-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5d23-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5d23-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="f5d23-115">-SslProfile</span></span>
<span data-ttu-id="f5d23-116">應用程式閘道 SSL 設定檔</span><span class="sxs-lookup"><span data-stu-id="f5d23-116">The application Gateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5d23-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d23-117">CommonParameters</span></span>
<span data-ttu-id="f5d23-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f5d23-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d23-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5d23-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d23-120">輸入</span><span class="sxs-lookup"><span data-stu-id="f5d23-120">INPUTS</span></span>

### <span data-ttu-id="f5d23-121">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f5d23-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="f5d23-122">輸出</span><span class="sxs-lookup"><span data-stu-id="f5d23-122">OUTPUTS</span></span>

### <span data-ttu-id="f5d23-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f5d23-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="f5d23-124">筆記</span><span class="sxs-lookup"><span data-stu-id="f5d23-124">NOTES</span></span>

## <span data-ttu-id="f5d23-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5d23-125">RELATED LINKS</span></span>



[<span data-ttu-id="f5d23-126">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f5d23-126">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="f5d23-127">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f5d23-127">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)
