---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139807"
---
# <span data-ttu-id="2f4a4-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="2f4a4-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="2f4a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f4a4-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4a4-103">取得適用于應用程式閘道之 ssl 原則的所有可用 ssl 選項。</span><span class="sxs-lookup"><span data-stu-id="2f4a4-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="2f4a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f4a4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f4a4-105">說明</span><span class="sxs-lookup"><span data-stu-id="2f4a4-105">DESCRIPTION</span></span>
<span data-ttu-id="2f4a4-106">**AzApplicationGatewayAvailableSslOption** Cmdlet 會取得 ssl 原則的所有可用 ssl 選項</span><span class="sxs-lookup"><span data-stu-id="2f4a4-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="2f4a4-107">示例</span><span class="sxs-lookup"><span data-stu-id="2f4a4-107">EXAMPLES</span></span>

### <span data-ttu-id="2f4a4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2f4a4-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="2f4a4-109">這個命令會傳回 ssl 原則的所有可用 ssl 選項。</span><span class="sxs-lookup"><span data-stu-id="2f4a4-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="2f4a4-110">參數</span><span class="sxs-lookup"><span data-stu-id="2f4a4-110">PARAMETERS</span></span>

### <span data-ttu-id="2f4a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4a4-111">-DefaultProfile</span></span>
<span data-ttu-id="2f4a4-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f4a4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f4a4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4a4-113">CommonParameters</span></span>
<span data-ttu-id="2f4a4-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f4a4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4a4-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2f4a4-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4a4-116">輸入</span><span class="sxs-lookup"><span data-stu-id="2f4a4-116">INPUTS</span></span>

### <span data-ttu-id="2f4a4-117">所有</span><span class="sxs-lookup"><span data-stu-id="2f4a4-117">None</span></span>

## <span data-ttu-id="2f4a4-118">輸出</span><span class="sxs-lookup"><span data-stu-id="2f4a4-118">OUTPUTS</span></span>

### <span data-ttu-id="2f4a4-119">PSApplicationGatewayAvailableSslOptions 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2f4a4-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="2f4a4-120">筆記</span><span class="sxs-lookup"><span data-stu-id="2f4a4-120">NOTES</span></span>

## <span data-ttu-id="2f4a4-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f4a4-121">RELATED LINKS</span></span>
