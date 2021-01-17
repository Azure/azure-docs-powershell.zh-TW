---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: a1e6bd507b7ddcc0a70405136cb76bba9231a7f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436792"
---
# <span data-ttu-id="6bb39-101">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="6bb39-101">Get-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="6bb39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6bb39-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb39-103">取得應用程式閘道 SSL 設定檔的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="6bb39-103">Gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="6bb39-104">句法</span><span class="sxs-lookup"><span data-stu-id="6bb39-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bb39-105">說明</span><span class="sxs-lookup"><span data-stu-id="6bb39-105">DESCRIPTION</span></span>
<span data-ttu-id="6bb39-106">**AzApplicationGatewaySslProfilePolicy** Cmdlet 會取得應用程式閘道 ssl 設定檔的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="6bb39-106">The **Get-AzApplicationGatewaySslProfilePolicy** cmdlet gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="6bb39-107">示例</span><span class="sxs-lookup"><span data-stu-id="6bb39-107">EXAMPLES</span></span>

### <span data-ttu-id="6bb39-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6bb39-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

<span data-ttu-id="6bb39-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="6bb39-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="6bb39-110">第二個命令會針對 $AppGw 取得名為 SslProfile01 的 SSL 設定檔，並將它儲存 $SslProfile 變數。</span><span class="sxs-lookup"><span data-stu-id="6bb39-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="6bb39-111">最後一個命令會從 SSL 設定檔中取得 SSL 原則 $SslProfile 並將它儲存在 $sslpolicy 變數中。</span><span class="sxs-lookup"><span data-stu-id="6bb39-111">The last command gets the SSL policy from the SSL profile $SslProfile and stores it in the $sslpolicy variable.</span></span>

## <span data-ttu-id="6bb39-112">參數</span><span class="sxs-lookup"><span data-stu-id="6bb39-112">PARAMETERS</span></span>

### <span data-ttu-id="6bb39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb39-113">-DefaultProfile</span></span>
<span data-ttu-id="6bb39-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6bb39-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bb39-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="6bb39-115">-SslProfile</span></span>
<span data-ttu-id="6bb39-116">應用程式閘道 SSL 設定檔</span><span class="sxs-lookup"><span data-stu-id="6bb39-116">The application Gateway SSL profile</span></span>

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

### <span data-ttu-id="6bb39-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb39-117">CommonParameters</span></span>
<span data-ttu-id="6bb39-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6bb39-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb39-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6bb39-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb39-120">輸入</span><span class="sxs-lookup"><span data-stu-id="6bb39-120">INPUTS</span></span>

### <span data-ttu-id="6bb39-121">PSApplicationGatewaySslProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6bb39-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="6bb39-122">輸出</span><span class="sxs-lookup"><span data-stu-id="6bb39-122">OUTPUTS</span></span>

### <span data-ttu-id="6bb39-123">PSApplicationGatewaySslPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6bb39-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="6bb39-124">筆記</span><span class="sxs-lookup"><span data-stu-id="6bb39-124">NOTES</span></span>

## <span data-ttu-id="6bb39-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bb39-125">RELATED LINKS</span></span>

[<span data-ttu-id="6bb39-126">新-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="6bb39-126">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="6bb39-127">附加 AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="6bb39-127">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="6bb39-128">移除-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="6bb39-128">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="6bb39-129">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="6bb39-129">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)