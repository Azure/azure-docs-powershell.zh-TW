---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: 8d2022f79dff5263f07737d525169dad3566fcda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915365"
---
# <span data-ttu-id="4e8ec-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="4e8ec-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="4e8ec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4e8ec-102">SYNOPSIS</span></span>
<span data-ttu-id="4e8ec-103">針對應用程式閘道的 ssl 策略，獲得所有可用的 ssl 選項。</span><span class="sxs-lookup"><span data-stu-id="4e8ec-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="4e8ec-104">語法</span><span class="sxs-lookup"><span data-stu-id="4e8ec-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e8ec-105">描述</span><span class="sxs-lookup"><span data-stu-id="4e8ec-105">DESCRIPTION</span></span>
<span data-ttu-id="4e8ec-106">**Get-AzApplicationGatewayAvailableSlOption** Cmdlet 會取得 ssl 政策的所有可用 ssl 選項</span><span class="sxs-lookup"><span data-stu-id="4e8ec-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="4e8ec-107">例子</span><span class="sxs-lookup"><span data-stu-id="4e8ec-107">EXAMPLES</span></span>

### <span data-ttu-id="4e8ec-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4e8ec-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="4e8ec-109">這個命令會針對 ssl 策略，會返回所有可用的 ssl 選項。</span><span class="sxs-lookup"><span data-stu-id="4e8ec-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="4e8ec-110">參數</span><span class="sxs-lookup"><span data-stu-id="4e8ec-110">PARAMETERS</span></span>

### <span data-ttu-id="4e8ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e8ec-111">-DefaultProfile</span></span>
<span data-ttu-id="4e8ec-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e8ec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e8ec-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e8ec-113">CommonParameters</span></span>
<span data-ttu-id="4e8ec-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4e8ec-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e8ec-115">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e8ec-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e8ec-116">輸入</span><span class="sxs-lookup"><span data-stu-id="4e8ec-116">INPUTS</span></span>

### <span data-ttu-id="4e8ec-117">沒有</span><span class="sxs-lookup"><span data-stu-id="4e8ec-117">None</span></span>

## <span data-ttu-id="4e8ec-118">輸出</span><span class="sxs-lookup"><span data-stu-id="4e8ec-118">OUTPUTS</span></span>

### <span data-ttu-id="4e8ec-119">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayAvailableSlOptions</span><span class="sxs-lookup"><span data-stu-id="4e8ec-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="4e8ec-120">筆記</span><span class="sxs-lookup"><span data-stu-id="4e8ec-120">NOTES</span></span>

## <span data-ttu-id="4e8ec-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e8ec-121">RELATED LINKS</span></span>
